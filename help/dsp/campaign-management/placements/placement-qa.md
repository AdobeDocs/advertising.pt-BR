---
title: Revisar e editar configurações de posicionamento usando bulksheets
description: Saiba como revisar e editar as configurações de posicionamento de chave em massa usando planilhas.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: c9e93fff986b524896e660203a5873fc4adda438
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Revisar e editar configurações de posicionamento usando bulksheets

Você pode baixar as configurações para um ou mais posicionamentos, ou para todos os posicionamentos em uma campanha, no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. Use esse recurso para analisar rapidamente detalhes como:

* O público alvo da campanha.
* Quando os posicionamentos começam a entregar e quando param.
* Quais anúncios são anexados aos posicionamentos.

Para atualizar várias configurações de uma só vez, você pode fazer alterações em campos selecionados, salvar o arquivo e fazer upload do arquivo de bulksheet editado de volta para o DSP. Os campos editáveis incluem a maioria das configurações editáveis.

>[!TIP]
>
>Para editar rapidamente mais campos para um ou mais posicionamentos, consulte &quot;[Editar Posicionamentos](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Configurações de download para todos os posicionamentos em uma campanha

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Ao lado da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Clique no nome da campanha. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Na caixa de diálogo [!UICONTROL Bulksheet Download], desmarque todos os componentes da campanha cujas configurações você deseja excluir do arquivo baixado e clique em **[!UICONTROL Download]**.

Por padrão, as configurações para todos os posicionamentos e anúncios associados aos pacotes são selecionadas.

Uma mensagem de notificação indica quando o arquivo está disponível para download.

1. Para baixar o arquivo, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

   O arquivo é salvo na pasta Downloads do navegador.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

## Configurações de download para disposições específicas

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada posicionamento cujas configurações você deseja baixar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Uma mensagem de notificação indica quando o arquivo de bulksheet está disponível para download.

1. Para baixar a bulksheet, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

   O arquivo é salvo na pasta Downloads do navegador.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

   Para editar qualquer uma das configurações, edite o arquivo diretamente e faça upload das alterações.  Todas as colunas editáveis são destacadas em azul. Para usar o formato correto para um campo, selecione e copie o valor da configuração relevante do pacote ou da configuração de posicionamento. Para algumas configurações do target, como dayparting, metas personalizadas e métricas de conversão, uma opção de cópia está disponível na configuração.

## Fazer upload de uma bulksheet com configurações de posicionamento {#upload-bulksheet-placement}

Você pode fazer upload das configurações para suas inserções e para os anúncios e pacotes associados às inserções em um arquivo de bulksheet.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Ao lado da campanha pai, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Clique no nome da campanha. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Esta opção está disponível nas guias [!UICONTROL Packages], [!UICONTROL Placements] ou [!UICONTROL Ads].

   * No submenu, clique em **[!UICONTROL Placements]** e marque a caixa de seleção para qualquer posicionamento. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. No diálogo [!UICONTROL Upload Bulksheet]:

   1. Arraste e solte um arquivo na caixa ou clique dentro dela para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

1. (Opcional) Para verificar se as atualizações foram processadas, clique em ![Trabalhos](/help/dsp/assets/downloads.png) à direita da barra de menu superior.

Quando qualquer atualização de configuração falhar, você pode baixar um arquivo de erro de bulksheet com codificação de cores para mostrar quais configurações (linhas) foram salvas e quais falharam, com um motivo para cada falha. Você pode então resolver os problemas no mesmo arquivo e carregá-lo novamente para processar as informações corrigidas.

<!--
## Placement Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded bulksheet, all editable columns are highlighted in blue.

### [!UICONTROL Placements] Sheet

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |

### [!UICONTROL Placement_AdSchedules] Sheet

| [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Ad ID] | The numeric ID of the ad. | &mdash; |
| [!UICONTROL Ad Name] | The name of the ad. | Yes |
| [!UICONTROL Start Date] | The start date of the ad. | &mdash; |
| [!UICONTROL End Date] | The end date of the ad. | &mdash; |
| [!UICONTROL Adobe Ad Approval Status] | The status of the Advertising DSP approval process, such as *Approved* or *Incomplete*. | &mdash; |
| [!UICONTROL Flight 1 Start Date] - [!UICONTROL Flight 12 Start Date] | The start date for a specific flight. | Yes |
| [!UICONTROL Flight 1 End Date] - [!UICONTROL Flight 12 End Date] | The end date for a specific flight. | Yes |
| [!UICONTROL Flight 1 Weight] - [!UICONTROL Flight 12 Weight] | How to rotate a specific ad for a specific flight:  *Even* to rotate the ad evenly, or a relative weight by which to rotate the ad, as a percentage (such as `40` for 40%); the total weights for all ads in the flight must equal 100. | Yes |

### [!UICONTROL Placement_BidMultipliers] Sheet

*Available in campaign-level bulksheets only*

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Country] | The bid multiplier and the name of the country, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL State] | The bid multiplier and the name of the state. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL City] | The bid multiplier and the name of the city, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL DMA] | (U.S. locations only) The bid multiplier and the designated market area, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Geo] | [!UICONTROL Postal code] | The bid multiplier and the postal code, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Source] | The bid multiplier and the public inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory Feed] | The bid multiplier and the public inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Source] | The bid multiplier and the OnDemand inventory source, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL OnDemand Inventory Feed] | The bid multiplier and the OnDemand inventory feed, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Domains] | The bid multiplier and the domains, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Sites/Apps] | [!UICONTROL Category] | The bid multiplier and the site/app category, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Daypart] | The bid multiplier and the daypart interval, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Audience] | [!UICONTROL Topics - Comscore] | The bid multiplier and the [!DNL Comscore] topics, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Ads.txt] | The bid multiplier and the level of [Ads.txt](https://iabtechlab.com/ads-txt-about/) pre-bid filtering to use, separated with a comma. Each target is followed by a semi-colon (;). | &mdash; |

-->

<!-- LOTS MORE THAN I HAD ORIGINALLY DOCUMENTED -- BELOW ARE THE LAST, BUT NOT ALL:

| Brand Safety | Brand Safety - Contextual Filtering # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Fraud blocking # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Viewability # |  |  |
| Brand Safety | Site Safety Block |  |  |
| Tracking | Tracking Pixels # |  |  |
| Tracking | Conversion Pixels # |  |  |
| Tracking | 3rd-party fees |  |  |
| # of Ads Attached |  |  |
| Ads |  Ad Names |  |  |
| Ads | Attached Ad ID |  |  |
| Environment | Environment |  |  |
-->

<!-- 
Check on Brand Safety - Contextual Filtering # with new DV feature/fct change.
-->

>[!MORELIKETHIS]
>
>* [Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar posicionamentos](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
