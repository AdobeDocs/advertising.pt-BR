---
title: Revisar e editar configurações de pacote usando bulksheets
description: Saiba como revisar e editar as principais configurações de pacote em massa usando planilhas.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Revisar e editar configurações de pacote usando bulksheets

É possível baixar as configurações de um ou mais pacotes no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. O arquivo *bulksheet* inclui uma guia separada com informações de voo.

Para atualizar várias configurações de uma só vez, siga um destes procedimentos:

* Faça alterações nos campos selecionados, salve o arquivo e faça upload do arquivo de bulksheet editado novamente no DSP.

* Para fazer alterações em pacotes, disposições ou anúncios adicionais na campanha, baixe uma bulksheet para a campanha. Insira ou cole as configurações atualizadas no arquivo e, em seguida, faça upload do arquivo para fazer as alterações. Para obter instruções, consulte &quot;[Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Os campos editáveis incluem a maioria das configurações que normalmente são editáveis.

>[!TIP]
>
>Para editar rapidamente mais campos para um ou mais pacotes, consulte &quot;[Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configurações de download para todos os pacotes em uma campanha

Ao baixar configurações para todos os pacotes em uma campanha, a bulksheet inclui guias separadas para as configurações de pacote e para as informações de voo. Opcionalmente, é possível incluir configurações para os posicionamentos e anúncios associados aos pacotes; guias adicionais são incluídas para configurações de posicionamento e anúncio.

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

     Para editar qualquer uma das configurações, edite o arquivo diretamente e faça upload das alterações. Todas as colunas editáveis são destacadas em azul.

## Configurações de download para pacotes específicos

Ao baixar configurações para pacotes específicos, o arquivo de bulksheet inclui guias separadas para as configurações de pacote e para as informações de voo, e o arquivo é editável.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Packages]**.

1. Marque as caixas de seleção dos pacotes cujas configurações você deseja baixar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Uma mensagem de notificação indica quando o arquivo de bulksheet está disponível para download.

1. Para baixar a bulksheet, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

     O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de Posicionamento em Bulksheets Baixados/Carregados](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

     Para editar qualquer uma das configurações, edite o arquivo diretamente e faça upload das alterações. Todas as colunas editáveis são destacadas em azul. Para usar o formato correto para um campo, selecione e copie o valor da configuração relevante do pacote ou da configuração de posicionamento. Para algumas configurações do target, como dayparting, metas personalizadas e métricas de conversão, uma opção de cópia está disponível na configuração.

## Fazer upload de uma Bulksheet com configurações de pacote {#upload-bulksheet-package}

Você pode fazer upload das configurações dos pacotes, incluindo os posicionamentos e anúncios associados aos pacotes, em um arquivo de bulksheet.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Ao lado da campanha pai, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Clique no nome da campanha. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Esta opção está disponível nas guias [!UICONTROL Packages], [!UICONTROL Placements] ou [!UICONTROL Ads].

   * No submenu, clique em **[!UICONTROL Packages]** e marque a caixa de seleção de qualquer pacote. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. No diálogo [!UICONTROL Upload Bulksheet]:

   1. Arraste e solte um arquivo na caixa ou clique dentro dela para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

1. (Opcional) Para verificar se as atualizações foram processadas, clique em ![Trabalhos](/help/dsp/assets/downloads.png) à direita da barra de menu superior.

Quando qualquer atualização de configuração falhar, você pode baixar um arquivo de erro de bulksheet com codificação de cores para mostrar quais configurações (linhas) foram salvas e quais falharam, com um motivo para cada falha. Você pode então resolver os problemas no mesmo arquivo e carregá-lo novamente para processar as informações corrigidas.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
