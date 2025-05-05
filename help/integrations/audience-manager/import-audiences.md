---
title: Importar segmentos do Adobe Audience Manager para direcionamento de anúncios
description: Saiba como importar públicos-alvo do  [!DNL Adobe]  para o Advertising DSP e pesquisar usando o Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importar segmentos do Adobe Audience Manager para direcionamento de anúncios

A Advertising DSP e o [!DNL Advertising Search, Social, & Commerce] podem obter metadados, dados de hierarquia e dados de público-alvo exclusivos para todos os [!DNL Adobe] públicos-alvo<!-- segments or audiences? Standardize terms per AAM's docs --> de um anunciante ou agência, incluindo:

* Segmentos do Adobe Audience Manager

* Segmentos do Adobe Analytics publicados no Adobe Experience Cloud

* Segmentos criados usando o Adobe Experience Cloud [!DNL Audience Library]

* Segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager

Para acessar [!DNL Adobe] públicos-alvo no DSP ou [!DNL Creative], você deve importar os públicos-alvo para DSP. Para acessar [!DNL Adobe] públicos-alvo em [!DNL Search, Social, & Commerce], você deve importar os públicos-alvo para [!DNL Search, Social, & Commerce].

## Pré-requisitos

* O anunciante deve implementar [o [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/pt-br/docs/id-service/using/intro/overview) versão 2.0 ou superior. O [!DNL Identity Service] fornece uma ID contínua e universal que identifica os visitantes em todas as soluções no Experience Cloud.

  A implementação inclui a adição do código [!DNL Identity service] a cada página da Web nos sites do anunciante.

* A organização deve ser [habilitada para serviços Experience Cloud](https://experienceleague.adobe.com/pt-br/docs/core-services/interface/services/overview) e ter um Experience Cloud [!DNL Organization ID] (anteriormente chamado [!DNL IMS org ID]).

  O [!UICONTROL Organization ID] permite que organizações com vários produtos da Adobe Experience Cloud compartilhem dados entre alguns dos produtos.

* (Anunciantes com [!DNL Analytics]) O anunciante deve [implementar [!DNL Analytics] usando `appMeasurement.js`](https://experienceleague.adobe.com/pt-br/docs/analytics/implementation/js/overview) versão 1.6.4 ou superior.

* Os visitantes do site do anunciante não incluem um grande volume de [!DNL Apple Safari] usuários.

* (Recomendado quando o anunciante usa Audience Manager e [!DNL Analytics]) Para reduzir as chamadas para cada página da Web, remova o código de Audience Manager [!DNL Data Integration Library] existente para a coleta de dados e ative o encaminhamento pelo lado do servidor para cada conjunto de relatórios [!DNL Analytics]. Para obter mais informações, consulte &quot;[Visão geral do encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/pt-br/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recomendado) Para taxas de correspondência mais altas, envie somente dados de sites primários para o Adobe Advertising. Se o anunciante agrupar dados de terceiros ou dados offline de um sistema de gerenciamento de relacionamento com o cliente, o vazamento de dados pode reduzir as taxas de correspondência.

## Importar públicos-alvo do Audience Manager para o DSP

### Etapas para importar públicos-alvo para DSP

As equipes de operações de dados e contas do [!DNL Adobe] executam as etapas a seguir.

1. A equipe da conta do Adobe deve definir a configuração no nível do anunciante &quot;[!UICONTROL Adobe Analytics Cloud]&quot;.

1. A equipe de contas do Adobe deve enviar uma solicitação à equipe de operações de dados para importar os segmentos de Audience Manager da organização usando a integração de API nativa do Advertising DSP.

### Quais alterações resultam no Audience Manager?

A API automaticamente:

* Cria dois destinos DSP no Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mapeia os dois destinos para todos os segmentos de Audience Manager, permitindo que o Audience Manager compartilhe os segmentos com a conta de anunciante do DSP associada ao mesmo Experience Cloud [!DNL Organization ID] usado para Audience Manager.

  Como opção, a organização pode remover segmentos desnecessários dos destinos dentro do Audience Manager.

* Adiciona o seguinte pixel de sincronização de cookies do Exchange ao contêiner de Audience Manager da organização para melhorar o alcance das campanhas do cliente:

   * Adobe AdCloud: 411 (Esse pixel é fornecido padrão e automaticamente como parte da versão 2.0 do [!DNL Identity Service]. Organizações com [!DNL Identity Service] versões inferiores a 2.0 devem adicionar esse pixel ao contêiner de Audience Manager.

## Importar públicos-alvo do Audience Manager para [!DNL Search, Social, & Commerce]

### Etapas para importar públicos para [!DNL Search, Social, & Commerce]

A equipe do [!DNL Adobe] executa a maioria ou todas as etapas a seguir.

1. A Equipe de Conta do Adobe deve enviar uma solicitação à equipe de operações de dados para configurar uma integração entre [!DNL Search, Social, & Commerce] e o Audience Manager. Inclua os nomes dos segmentos de Audience Manager que você deseja exportar para [!DNL Search, Social, & Commerce].

1. No Audience Manager, configure destinos para [!DNL Search, Social, & Commerce]:

   1. Crie dois novos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] é um nome antigo de [!DNL Search, Social, & Commerce].

   1. Especifique os segmentos para cada destino.

      Com a opção [!UICONTROL Automatically map all current and future segments], todos os segmentos são mapeados e sincronizados diariamente.

      A opção [!UICONTROL Manually map segments] permite mapear manualmente os segmentos a serem sincronizados com o destino do lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Nenhum segmento precisa ser mapeado manualmente para o destino HTTP.

1. Em [!DNL Search, Social, & Commerce], a equipe de implementação [!DNL Search, Social, & Commerce] ou um usuário com a função de gerente de cliente de acesso direto deve iniciar a importação de [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   O Experience Cloud da organização [!DNL Organization ID] ([!DNL IMS org ID]) é obrigatório. A ID deve ser igual à usada para a conta Audience Manager da organização.

### Quais alterações resultam no Audience Manager?

Dois destinos [!DNL Search, Social, & Commerce] ficam disponíveis para a organização no Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Sincronização de dados

A importação inicial leva cerca de 24 horas. Após a importação inicial, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.

Os dados de associação do segmento são enviados somente após um dos seguintes eventos ocorrer:

* (Anunciantes com DSP):

   * O segmento é direcionado em um anúncio de exibição de Adobe Advertising.

   * O segmento é adicionado ao lote [!DNL Adobe AdCloud Cross-Channel] e aos destinos em tempo real na interface do usuário do Audience Manager.

* (Anunciantes com [!DNL Search, Social, & Commerce]):

   * O segmento é direcionado em um anúncio de pesquisa de Adobe Advertising.

   * O segmento é adicionado ao lote [!DNL Adobe Media Optimizer] e aos destinos HTTP na interface do usuário do Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Como o DSP sincroniza os dados

O DSP sincroniza os dados automaticamente usando o [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante a sincronização, o [!DNL ECID Service] chama o Adobe Advertising em [!DNL cm.everesttech.net]. Como o Adobe Advertising é um domínio confiável, as sincronizações de ID ocorrem de páginas principais em vez de nos iframes de publicação de destino, como fazem com a maioria dos parceiros de ativação de terceiros. Audience Manager identifica usuários únicos por IDs de dispositivo, usando o [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/pt-br/docs/audience-manager/user-guide/reference/ids-in-aam), também chamado de [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Como o Search, Social e Commerce sincroniza os dados

O Search, Social e Commerce sincroniza os dados automaticamente usando o [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante a sincronização, o [!DNL ECID Service] chama o Adobe Advertising em [!DNL cm.everesttech.net], que é um domínio confiável que pertence ao Adobe Advertising. Audience Manager identifica usuários únicos por IDs de dispositivo, usando o [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/pt-br/docs/audience-manager/user-guide/reference/ids-in-aam), também chamado de [!DNL Device ID].

## Onde encontrar os segmentos sincronizados

### No DSP

O DSP organiza os nomes de segmento pela taxonomia Audience Manager e inclui as contagens de associação de segmento correspondentes em:

* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): na guia [!UICONTROL Adobe Segments] da seção [!UICONTROL Audience Targeting].

* Em [configurações de público-alvo](/help/dsp/audiences/audience-settings.md): na guia [!UICONTROL Adobe Segments].

### No Advertising Creative

No [!DNL Creative], os segmentos estão disponíveis nas configurações de experiência para nós de destino.

### Em [!DNL Advertising Search, Social, & Commerce]

No [!DNL Search, Social, & Commerce], os segmentos ficam disponíveis quando você cria um público-alvo do [!DNL Google] usando o [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada público-alvo do [!DNL Google] que você criar, o [!DNL Google] fornece o tamanho do público-alvo.

>[!MORELIKETHIS]
>
>* [Integrações de Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
