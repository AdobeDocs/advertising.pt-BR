---
title: Revisar e editar configurações de pacote usando bulksheets
description: Saiba como revisar e editar as principais configurações de pacote em massa usando planilhas.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Revisar e editar configurações de pacote usando bulksheets

É possível baixar as configurações de um ou mais pacotes no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. A planilha inclui uma guia separada com informações de voo.

Para atualizar várias configurações de uma só vez, siga um destes procedimentos:

* Faça alterações nos campos selecionados, salve o arquivo e faça upload do arquivo de bulksheet editado de volta para DSP.

* Para fazer alterações em pacotes adicionais e nas configurações para qualquer posicionamento ou anúncio, baixe um modelo de planilha em branco que inclua guias para cada tipo de componente da campanha, insira ou cole configurações novas ou atualizadas no arquivo de modelo e, em seguida, faça upload do arquivo para fazer as alterações. Para obter instruções, consulte &quot;[Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Os campos editáveis incluem a maioria das configurações que normalmente são editáveis.

>[!TIP]
>
>Para editar rapidamente mais campos para um ou mais pacotes, consulte &quot;[Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configurações de download para todos os pacotes em uma campanha

Ao baixar configurações para todos os pacotes em uma campanha, a planilha inclui guias separadas para as configurações do pacote e para as informações de voo. Opcionalmente, é possível incluir configurações para os posicionamentos e anúncios associados aos pacotes; guias adicionais são incluídas para configurações de posicionamento e anúncio.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Na caixa de diálogo [!UICONTROL QA Sheet Download], desmarque todos os componentes da campanha cujas configurações você deseja excluir do arquivo baixado e clique em **[!UICONTROL Download]**.

Por padrão, as configurações para todos os posicionamentos e anúncios associados aos pacotes são selecionadas.

Uma mensagem de notificação indica quando o arquivo está disponível para download.

1. Para baixar o arquivo, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

     O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

>[!NOTE]
>
>Você não pode editar e fazer upload novamente de planilhas de controle de qualidade no nível da campanha. Para fazer alterações nas configurações do componente de campanha nesses arquivos, baixe um modelo de bulksheet separado, insira ou cole linhas da folha de controle de qualidade no modelo de bulksheet e salve o arquivo e, em seguida, faça upload da bulksheet preenchida. Para obter instruções, consulte &quot;[Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

## Configurações de download para um ou mais pacotes

Ao baixar configurações para pacotes específicos, o arquivo de bulksheet inclui guias separadas para as configurações de pacote e para as informações de voo, e o arquivo é editável.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Packages]**.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Uma mensagem de notificação indica quando o arquivo de bulksheet está disponível para download.

1. Para baixar a bulksheet, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

     O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Fazer upload de uma Bulksheet com configurações de pacote {#upload-bulksheet-package}

Você pode fazer upload das configurações dos pacotes, incluindo os posicionamentos e anúncios associados aos pacotes, em um arquivo de bulksheet.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. No diálogo [!UICONTROL Upload Bulksheet]:

   1. Arraste e solte um arquivo na caixa ou clique dentro dela para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

1. (Opcional) Para verificar se as atualizações foram processadas, clique em ![Trabalhos](/help/dsp/assets/downloads.png) à direita da barra de menu superior.

## Colunas de configuração de pacote em planilhas baixadas/carregadas{#qa-sheet-columns-packages}

>[!TIP]
>
> Em uma planilha baixada, todas as colunas editáveis são destacadas em azul.

### Guia [!UICONTROL Package]

| Seção | Coluna | Descrição | Editável? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | A ID numérica do pacote. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | O nome do pacote. | Sim |
| [!UICONTROL Basic details] | [!UICONTROL Status] | O status do pacote: *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Sim |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Uma descrição opcional do pacote. | Sim |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Uma taxa de taxa estática de terceiros que deve ser rastreada como um custo não faturável por 1000 impressões, se aplicável. | Sim |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Uma descrição opcional da taxa de taxa de terceiros, se aplicável. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | A data de início do pacote. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | A data final do pacote. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Em qual nível colocar e limitar posicionamentos no pacote: *[!UICONTROL Package]* ou *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | O orçamento do pacote. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | O intervalo de orçamento: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Um limite de intervalo de orçamento opcional. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | O intervalo para o limite de intervalo de orçamento opcional: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | O objetivo do pacote. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | O valor de destino da meta. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Pacotes somente com as metas de otimização &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;)Uma [meta personalizada](/help/dsp/optimization/custom-goal.md) que inclui os eventos de receita ou conversão usados para calcular a métrica de CPA ou ROAS. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Opcional; pacotes com apenas as metas de otimização &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) O evento de conversão final ou o valor de evento de receita/venda a ser usado para calcular o retorno sobre o gasto com anúncios ou o custo por aquisição. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Pacotes somente com metas de otimização personalizadas) A finalidade do pacote, que ajuda a determinar como otimizá-lo: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* ou *[!UICONTROL Other]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Pacotes somente com metas de otimização personalizadas) A ID do pacote de outro pacote cujos dados históricos são usados como entrada para otimizar o pacote. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Pacotes somente com metas de otimização personalizadas) Outro pacote cujos dados históricos são usados como entrada para otimização do pacote. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Se o pacote está se aproximando de *[!UICONTROL budget]* ou *[!UICONTROL primary_goal]* (para impressões). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Ao colocar o pacote em impressões) O número alvo de impressões durante o intervalo de tempo especificado. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Quando você coloca o pacote em impressões) O intervalo de tempo para o número alvo de impressões. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | A estratégia de ritmo de execução do pacote: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | A estratégia de ritmo intradiário do pacote: *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | O limite de frequência primária do pacote durante o [!UICONTROL Frequency Cap Interval] especificado. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | O intervalo para o limite de frequência primária: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos aos quais o [!UICONTROL Frequency Cap] principal se aplica. Por exemplo, se o limite principal for de 12 impressões por mês, o valor aqui será `12`. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundário do pacote durante o [!UICONTROL Secondary Frequency Cap Interval] especificado | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundário: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pelo [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos aos quais o [!UICONTROL Secondary Frequency Cap] se aplica. Por exemplo, se o limite secundário for de três impressões a cada seis horas, o valor aqui será `6`. | Sim |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Determina se deve ser criada uma jornada não-uniforme para o pacote *T* (true) ou *F* (false). Depois de habilitar a pesquisa personalizada e salvar o pacote, não é possível desabilitar a pesquisa personalizada nem editar a data de início do pacote. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Disponível somente quando a opção [!UICONTROL Activate Custom Flighting] estiver habilitada) Determina se o orçamento restante do voo anterior deve ou não ser adicionado automaticamente ao orçamento existente para o próximo voo: *T* (true) ou *F* (false). | Sim |
| [!UICONTROL Error] | [!UICONTROL Error] | Quaisquer erros relevantes. | — |

### Guia [!UICONTROL Package_Flights] {#qa-sheet-columns-package-flights}

| Seção | Coluna | Descrição | Editável? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | A ID numérica do pacote. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | A ID numérica do voo. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | A primeira data do voo. | Sim |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | A data final do voo. | Sim |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | A meta de gastos para o voo. | Sim |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Pacotes existentes sem a opção &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; ativada) Uma quantidade de orçamento potencialmente não gasto para ser adicionada ao próximo voo. | Sim |

>[!MORELIKETHIS]
>
>* [Revisar e editar configurações do componente de campanha usando bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
