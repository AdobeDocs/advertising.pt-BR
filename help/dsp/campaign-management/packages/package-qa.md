---
title: Revisar e editar configurações de pacote usando planilhas
description: Saiba como revisar e editar as principais configurações de pacote usando planilhas.
feature: DSP Packages
source-git-commit: ad00092c4ef5d44c364ab0593826220054f715c3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Revisar e editar configurações de pacote usando planilhas

É possível baixar as configurações de um ou mais pacotes no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. A planilha inclui uma guia separada com informações de voo. Em seguida, é possível fazer alterações em campos selecionados em ambas as guias e fazer upload dos dados de volta para o DSP de uma só vez. Os campos editáveis incluem a maioria das configurações que normalmente são editáveis.

>[!TIP]
>
>Para editar mais campos para um ou mais pacotes, consulte &quot;[Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Configurações de download para um ou mais pacotes

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Packages]**.

1. Marque a caixa de seleção ao lado de cada pacote cujas configurações você deseja baixar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

O arquivo é salvo automaticamente na pasta Download do navegador. Consulte &quot;[Colunas do Pacote em Planilhas Baixadas/Carregadas](#qa-sheet-columns-packages)&quot; para obter uma lista das colunas incluídas.

## Configurações de Carregamento de Um ou Mais Pacotes

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Packages]**.

1. Marque a caixa de seleção ao lado de cada pacote cujas configurações você deseja fazer upload.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. No diálogo [!UICONTROL Edit in Excel]:

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

### Guia [!UICONTROL Package_Flights]

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
>* [Editar Pacotes](/help/dsp/campaign-management/packages/package-edit.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
