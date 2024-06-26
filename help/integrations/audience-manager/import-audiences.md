---
title: Importar segmentos do Adobe Audience Manager para direcionamento de anúncios
description: Saiba como importar seus [!DNL Adobe] públicos-alvo na Advertising DSP e na pesquisa usando o Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importar segmentos do Adobe Audience Manager para direcionamento de anúncios

Advertising DSP e [!DNL Advertising Search, Social, & Commerce] Cada um pode obter metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os anúncios ou agências [!DNL Adobe] públicos<!-- segments or audiences? Standardize terms per AAM's docs -->, incluindo:

* Segmentos do Adobe Audience Manager

* Segmentos do Adobe Analytics publicados no Adobe Experience Cloud

* Segmentos criados usando a Adobe Experience Cloud [!DNL Audience Library]

* Segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager

Para acessar o [!DNL Adobe] públicos no DSP ou [!DNL Creative], você deve importar os públicos-alvo para o DSP. Para acessar o [!DNL Adobe] públicos-alvo na [!DNL Search, Social, & Commerce], você deve importar os públicos para o [!DNL Search, Social, & Commerce].

## Pré-requisitos

* O anunciante deve implementar [o [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) versão 2.0 ou superior. A variável [!DNL Identity Service] O fornece uma ID persistente e universal que identifica os visitantes em todas as soluções do Experience Cloud.

  A implementação inclui a adição de [!DNL Identity service] para cada página da Web nos sites do anunciante.

* A organização deve ser [habilitado para serviços Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) e têm um Experience Cloud [!DNL Organization ID] (anteriormente chamado de [!DNL IMS org ID]).

  A variável [!UICONTROL Organization ID] O permite que organizações com vários produtos da Adobe Experience Cloud compartilhem dados entre alguns dos produtos.

* (Anunciantes com [!DNL Analytics]) O anunciante deve [implementar [!DNL Analytics] usar `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) versão 1.6.4 ou superior.

* Os visitantes do site do anunciante não incluem um grande volume de [!DNL Apple Safari] usuários.

* (Recomendado quando o anunciante usa Audience Manager e [!DNL Analytics]) Para reduzir as chamadas para cada página da Web, remova o Audience Manager existente [!DNL Data Integration Library] para a coleta de dados e habilitar o encaminhamento pelo lado do servidor para cada [!DNL Analytics] conjunto de relatórios. Para obter mais informações, consulte &quot;[Visão geral do encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recomendado) Para taxas de correspondência mais altas, envie somente dados de sites primários para o Adobe Advertising. Se o anunciante agrupar dados de terceiros ou dados offline de um sistema de gerenciamento de relacionamento com o cliente, o vazamento de dados pode reduzir as taxas de correspondência.

## Importar públicos-alvo do Audience Manager para o DSP

### Etapas para importar públicos-alvo para DSP

A variável [!DNL Adobe] as equipes de operações de conta e dados executam as etapas a seguir.

1. A equipe da conta do Adobe deve definir a configuração no nível do anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. A equipe de conta do Adobe deve enviar uma solicitação à equipe de operações de dados para importar os segmentos de Audience Manager da organização usando a integração de API nativa do Advertising DSP.

### Quais alterações resultam no Audience Manager?

A API automaticamente:

* Cria dois destinos DSP no Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mapeia os dois destinos para todos os segmentos de Audience Manager, permitindo que o Audience Manager compartilhe os segmentos com a conta de anunciante do DSP associada ao mesmo Experience Cloud [!DNL Organization ID] usado para Audience Manager.

  Como opção, a organização pode remover segmentos desnecessários dos destinos dentro do Audience Manager.

* Adiciona o seguinte pixel de sincronização de cookies do Exchange ao contêiner de Audience Manager da organização para melhorar o alcance das campanhas do cliente:

   * Adobe AdCloud: 411 (Esse pixel é fornecido padrão e automaticamente como parte da [!DNL Identity Service] versão 2.0. Organizações com [!DNL Identity Service] as versões anteriores à 2.0 devem adicionar esse pixel ao contêiner de Audience Manager.

## Importar públicos do Audience Manager para o [!DNL Search, Social, & Commerce]

### Etapas para importar públicos para o [!DNL Search, Social, & Commerce]

[!DNL Adobe] A equipe do executa a maioria ou todas as etapas a seguir.

1. A equipe da conta do Adobe deve enviar uma solicitação à equipe de operações de dados para configurar uma integração entre [!DNL Search, Social, & Commerce] e Audience Manager. Inclua os nomes dos segmentos de Audience Manager para os quais você deseja exportar [!DNL Search, Social, & Commerce].

1. No Audience Manager, configure destinos para [!DNL Search, Social, & Commerce]:

   1. Criar dois novos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] é um nome antigo de [!DNL Search, Social, & Commerce].

   1. Especifique os segmentos para cada destino.

      Com o [!UICONTROL Automatically map all current and future segments] todos os segmentos são mapeados e sincronizados diariamente.

      A variável [!UICONTROL Manually map segments] permite mapear manualmente os segmentos a serem sincronizados com o destino do lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Nenhum segmento precisa ser mapeado manualmente para o destino HTTP.

1. Dentro de [!DNL Search, Social, & Commerce], ou o [!DNL Search, Social, & Commerce] a equipe de implementação ou um usuário com a função de gerente do cliente de acesso direto deve iniciar a importação do [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   O Experience Cloud da organização [!DNL Organization ID] ([!DNL IMS org ID]) é obrigatório. A ID deve ser igual à usada para a conta Audience Manager da organização.

### Quais alterações resultam no Audience Manager?

Dois [!DNL Search, Social, & Commerce] os destinos se tornam disponíveis para a organização no Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Sincronização de dados

A importação inicial leva cerca de 24 horas. Após a importação inicial, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.

Os dados de associação do segmento são enviados somente após um dos seguintes eventos ocorrer:

* (Anunciantes com DSP):

   * O segmento é direcionado em um anúncio de exibição de Adobe Advertising.

   * O segmento é adicionado à variável [!DNL Adobe AdCloud Cross-Channel] destinos em lote e em tempo real na interface do usuário do Audience Manager.

* (Anunciantes com [!DNL Search, Social, & Commerce]):

   * O segmento é direcionado em um anúncio de pesquisa de Adobe Advertising.

   * O segmento é adicionado à variável [!DNL Adobe Media Optimizer] destinos batch e HTTP na interface do usuário do Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Como o DSP sincroniza os dados

O DSP sincroniza os dados automaticamente usando o [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante a sincronização, a variável [!DNL ECID Service] chama Adobe Advertising em [!DNL cm.everesttech.net]. Como o Adobe Advertising é um domínio confiável, as sincronizações de ID ocorrem de páginas principais em vez de nos iframes de publicação de destino, como fazem com a maioria dos parceiros de ativação de terceiros. O Audience Manager identifica usuários únicos por IDs de dispositivo, usando o [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), também chamado de [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Como o Search, Social e Commerce sincroniza os dados

O Search, Social e Commerce sincroniza os dados automaticamente usando o [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante a sincronização, a variável [!DNL ECID Service] chama Adobe Advertising em [!DNL cm.everesttech.net], que é um domínio confiável e pertence ao Adobe Advertising. O Audience Manager identifica usuários únicos por IDs de dispositivo, usando o [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), também chamado de [!DNL Device ID].

## Onde encontrar os segmentos sincronizados

### No DSP

O DSP organiza os nomes de segmento pela taxonomia Audience Manager e inclui as contagens de associação de segmento correspondentes em:

* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Na guia [!UICONTROL Adobe Segments] guia do [!UICONTROL Audience Targeting] seção.

* Entrada [configurações de público](/help/dsp/audiences/audience-settings.md): Na guia [!UICONTROL Adobe Segments] guia.

### No Advertising Creative

Entrada [!DNL Creative], os segmentos estão disponíveis nas configurações de experiência para nós de destino.

### Entrada [!DNL Advertising Search, Social, & Commerce]

Entrada [!DNL Search, Social, & Commerce], os segmentos ficam disponíveis quando você cria um [!DNL Google] público-alvo usando o [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada [!DNL Google] público-alvo que você cria, [!DNL Google] fornece o tamanho do público.

>[!MORELIKETHIS]
>
>* [Integrações de Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
