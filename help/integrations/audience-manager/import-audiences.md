---
title: Importar segmentos do Adobe Audience Manager para direcionamento de anúncios
description: Saiba como importar seus [!DNL Adobe] públicos-alvo na Advertising DSP e na pesquisa usando o Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Importar segmentos do Adobe Audience Manager para direcionamento de anúncios

DSP de publicidade e [!DNL Advertising Search, Social, & Commerce] Cada um pode obter metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os anúncios ou agências [!DNL Adobe] públicos<!-- segments or audiences? Standardize terms per AAM's docs -->. Isso inclui dados para:

* Segmentos do Adobe Audience Manager

* Segmentos do Adobe Analytics publicados no Adobe Experience Cloud

* Segmentos criados usando a Adobe Experience Cloud [!DNL Audience Library]

* Segmentos criados no Adobe Experience Platform e enviados à publicidade do Adobe via Audience Manager

Para acessar o [!DNL Adobe] públicos no DSP ou [!DNL Creative], você deve importar os públicos-alvo para o DSP. Para acessar o [!DNL Adobe] públicos-alvo na [!DNL Search, Social, & Commerce], você deve importar os públicos para o [!DNL Search, Social, & Commerce].

## Pré-requisitos

* O anunciante deve implementar [o [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versão 2.0 ou superior. A variável [!DNL Identity Service] O fornece uma ID persistente e universal que identifica os visitantes em todas as soluções do Experience Cloud.

   A implementação inclui a adição de [!DNL Identity service] para cada página da Web nos sites do anunciante.

* A organização deve ser [habilitado para serviços Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) e têm um Experience Cloud [!DNL Organization ID] (anteriormente chamado de [!DNL IMS org ID]).

   A variável [!UICONTROL Organization ID] O permite que organizações com vários produtos da Adobe Experience Cloud compartilhem dados entre alguns dos produtos.

* (Anunciantes com [!DNL Analytics]) O anunciante deve [implementar [!DNL Analytics] usar `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versão 1.6.4 ou superior.

* Os visitantes do site do anunciante não incluem um grande volume de [!DNL Apple Safari] usuários.

* (Recomendado quando o anunciante usa Audience Manager e [!DNL Analytics]) Para reduzir as chamadas para cada página da Web, remova o Audience Manager existente [!DNL Data Integration Library] para a coleta de dados e habilitar o encaminhamento pelo lado do servidor para cada [!DNL Analytics] conjunto de relatórios. Para obter mais informações, consulte &quot;[Visão geral do encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recomendado) Para taxas de correspondência mais altas, envie somente dados de sites primários para a Adobe Advertising. Se o anunciante agrupar dados de terceiros ou dados offline de um sistema de gerenciamento de relacionamento com o cliente, o vazamento de dados pode reduzir as taxas de correspondência.

## Importar públicos-alvo do Audience Manager para o DSP

### Etapas para importar públicos-alvo para DSP

A variável [!DNL Adobe] as equipes de operações de conta e dados executarão as etapas a seguir.

1. A equipe da conta do Adobe deve definir a configuração no nível do anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. A equipe da conta do Adobe deve enviar uma solicitação<!-- Submit a request as a JIRA task? --> para a equipe de operações de dados<!-- implementation team? --> para importar os segmentos de Audience Manager da organização usando a integração da API nativa DSP do Advertising.

### Quais alterações resultam no Audience Manager?

A API automaticamente:

* Cria dois destinos DSP no Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mapeia os dois destinos para todos os segmentos de Audience Manager, permitindo que o Audience Manager compartilhe os segmentos com a conta de anunciante do DSP associada ao mesmo Experience Cloud [!DNL Organization ID] usado para Audience Manager. <!-- Verify -->

   Como opção, a organização pode remover segmentos desnecessários dos destinos dentro do Audience Manager.

* Adiciona o seguinte pixel de sincronização de cookies do Exchange ao contêiner de Audience Manager da organização para melhorar o alcance das campanhas do cliente:

   * Adobe AdCloud: 411 (Isso é padrão e faz parte automaticamente do [!DNL Identity Service] versão 2.0. Organizações com [!DNL Identity Service] as versões anteriores à 2.0 devem adicionar esse pixel ao contêiner de Audience Manager.

## Importar públicos do Audience Manager para o [!DNL Search, Social, & Commerce]

### Etapas para importar públicos para o [!DNL Search, Social, & Commerce]

[!DNL Adobe] A equipe do executará a maioria ou todas as etapas a seguir.

1. A equipe da conta do Adobe deve enviar uma solicitação à equipe de operações de dados para configurar uma integração entre [!DNL Search, Social, & Commerce] e Audience Manager. Inclua os nomes dos segmentos de Audience Manager para os quais você deseja exportar [!DNL Search, Social, & Commerce].

1. No Audience Manager, configure destinos para [!DNL Search, Social, & Commerce]:

   1. Criar dois novos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] é um nome antigo de [!DNL Search, Social, & Commerce].

   1. Especifique os segmentos para cada destino.

      Com o [!UICONTROL Automatically map all current and future segments] todos os segmentos são mapeados e sincronizados diariamente.

      A variável [!UICONTROL Manually map segments] permite mapear manualmente os segmentos a serem sincronizados com o destino do lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Nenhum segmento precisa ser mapeado manualmente para o destino HTTP.

1. Dentro de [!DNL Search, Social, & Commerce], ou o [!DNL Search, Social, & Commerce] a equipe de implementação ou um usuário com a função de gerente do cliente de acesso direto deve iniciar a importação do [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Você precisará entrar no Experience Cloud da organização [!DNL Organization ID] ([!DNL IMS org ID]). A ID deve ser igual à usada para a conta Audience Manager da organização.

### Quais alterações resultam no Audience Manager?

A organização verá dois [!DNL Search, Social, & Commerce] destinos na Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronização de dados

A importação inicial leva cerca de 24 horas. Após a importação inicial, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Onde encontrar os segmentos sincronizados

### No DSP

No DSP, os nomes de segmentos são organizados pela taxonomia Audience Manager e estão disponíveis com as contagens de associação de segmento correspondentes em:

* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Na guia [!UICONTROL Adobe Segments] guia do [!UICONTROL Audience Targeting] seção.

* Entrada [configurações de público](/help/dsp/audiences/audience-settings.md): Na guia [!UICONTROL Adobe Segments] guia.

### Na Advertising Creative

Entrada [!DNL Creative], os segmentos estão disponíveis nas configurações de experiência para nós de destino.

### Entrada [!DNL Advertising Search, Social, & Commerce]

Entrada [!DNL Search, Social, & Commerce], os segmentos ficam disponíveis quando você cria um [!DNL Google] público-alvo usando o [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada [!DNL Google] público-alvo que você cria, [!DNL Google] fornece o tamanho do público.

>[!MORELIKETHIS]
>
>* [Integrações de publicidade do Adobe com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

