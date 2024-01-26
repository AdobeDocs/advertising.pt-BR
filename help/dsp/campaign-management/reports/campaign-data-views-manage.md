---
title: Gerenciar As Visualizações De Dados Do Campaign
description: Saiba como personalizar suas visualizações de dados para campanhas, pacotes, posicionamentos e anúncios.
feature: DSP Campaign Data Views
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Gerenciar As Visualizações De Dados Do Campaign

Você pode personalizar os dados que aparecem nas visualizações de gerenciamento de campanhas ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]).

## Gerenciar visualizações de dados {#data-visualizations-manage}

É possível alterar as métricas e o modo de gráfico para todas as visualizações de dados em campanhas ou para uma única campanha. As alterações em uma única campanha são aplicadas em todas as visualizações de dados da campanha, incluindo aquelas no [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads] exibições.

### Alterar as métricas para uma visualização de dados

1. No canto superior direito da visualização de dados, clique em ![Configurações](/help/dsp/assets/settings-chart.png).

1. Selecione as métricas.

   Não é possível selecionar a mesma métrica duas vezes.

1. Clique em **[!UICONTROL Apply]**.

### Alterar o modo de exibição de uma visualização de dados

* No canto superior direito da visualização de dados, clique no [!UICONTROL Overlay] alternar (![Chave de sobreposição](/help/dsp/assets/overlay.png)) para alterar entre o modo de sobreposição (todos os gráficos sobrepostos) e o modo de gráfico de treliça (três gráficos separados).

## Gerenciar Tabelas de Dados {#data-tables-manage}

Em todas as exibições de gerenciamento de campanha ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]), é possível personalizar os dados exibidos na tabela de dados.

### Gerenciar Exibições de Coluna {#column-views-manage}

Cada nível de gerenciamento de campanha ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]) inclui incorporado [!UICONTROL Pacing] e [!UICONTROL Performance] exibições que incluem métricas relevantes para essa entidade. Por padrão, a variável [!UICONTROL Pacing] é exibida para que você possa identificar campanhas com baixo desempenho e componentes da campanha rapidamente. Opcionalmente, é possível criar e editar conjuntos de colunas personalizados.

![seletor de exibição de coluna](/help/dsp/assets/column-view-selector.png)

O DSP salva a visualização mais recente como a visualização padrão para que, sempre que você retornar à página, sempre visualize as métricas pertinentes a você.

#### Alterar a Exibição de Coluna {#column-view-change}

* No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique no nome da exibição de coluna desejada.

#### Criar uma Exibição de coluna personalizada {#column-view-create}

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique em **[!UICONTROL Create View]**.

1. Especifique as métricas a serem incluídas na exibição:

   1. Na lista de métricas disponíveis, marque a caixa de seleção ao lado de cada métrica a ser incluída.

      Todas as métricas estão em ordem alfabética por categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (métricas padrão rastreadas pelo DSP), [!UICONTROL Viewability], e [!UICONTROL Conversions]. Métricas anexadas com &quot;([!UICONTROL Lifetime])&quot; retornam valores do início da campanha, independentemente do intervalo de datas selecionado na página.

   1. Edite a ordem da coluna, conforme necessário, clicando nos nomes das colunas no painel direito e arrastando-as para as posições necessárias.

   Algumas colunas têm posições fixas e não podem ser movidas ou removidas.

1. Aplique ou salve as configurações:

   * Para aplicar as configurações temporariamente sem salvá-las na exibição, clique em **[!UICONTROL Apply].**

   * Para salvar as configurações em uma exibição de coluna nova e personalizada, clique em **[!UICONTROL Save As]**. No [!UICONTROL Save View] insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

#### Editar uma Exibição de Coluna {#column-view-edit}

>[!NOTE]
>
>Você não pode salvar alterações em um modo de exibição de coluna padrão (predefinido), mas pode aplicar as alterações temporariamente ou salvá-las em um novo modo de exibição personalizado.

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e, em seguida, clique no nome da exibição de coluna existente.

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique em **[!UICONTROL Edit View]**.

1. Edite as métricas a serem incluídas na exibição:

   1. Na lista de métricas disponíveis, marque a caixa de seleção ao lado de cada métrica a ser incluída e desmarque a caixa de seleção ao lado de cada métrica a ser excluída.

      Todas as métricas estão em ordem alfabética por categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (métricas padrão rastreadas pelo DSP), [!UICONTROL Viewability], e [!UICONTROL Conversions]. Métricas anexadas com &quot;([!UICONTROL Lifetime])&quot; retornam valores do início da campanha, independentemente do intervalo de datas selecionado na página.

   1. Edite a ordem da coluna, conforme necessário, clicando nos nomes das colunas no painel direito e arrastando-as para as posições necessárias.

   Algumas colunas têm posições fixas e não podem ser movidas ou removidas.

1. Aplique ou salve as configurações:

   * (Somente exibições personalizadas) Para salvar as configurações, clique em **[!UICONTROL Save]**.

   * Para aplicar as configurações temporariamente sem salvá-las na exibição, clique em **[!UICONTROL Apply].**

   * Para salvar as configurações em uma exibição de coluna nova e personalizada, clique em **[!UICONTROL Save As]**. No [!UICONTROL Save View] insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

### Filtrar dados de campanha {#filter-data-tables}

Os filtros alteram os dados exibidos na guia atual. Os filtros disponíveis variam de acordo com o tipo de entidade, mas podem incluir nome da entidade, status e colunas de propriedade adicionais.

1. Na barra de ferramentas principal, clique em ![Botão Filtrar](/help/dsp/assets/filter.png).
1. Para cada filtro que deseja aplicar, clique no nome do filtro na coluna à esquerda e especifique os valores do filtro.
1. Clique em **[!UICONTROL Apply]**.

#### Filtros disponíveis

Os seguintes filtros estão disponíveis para o seu [!UICONTROL Campaigns], [!UICONTROL Packages], e [!UICONTROL Placements] exibições:

* [!UICONTROL Campaigns] exibir filtros:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] exibir filtros:
   * [!UICONTROL Custom flights] (se existem ou não)
   * [!UICONTROL Custom goal] (se aplicável)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] exibir filtros:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (se aplicável)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than]ou [!UICONTROL equal to] um valor especificado)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] ou [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] exibir filtros:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### Alterar o intervalo de datas

Altere o intervalo de datas usado em todas as exibições padrão e personalizadas usando o seletor de intervalo de datas acima de qualquer tabela de dados.

![Seletor de intervalo de datas](/help/dsp/assets/date-range-selector.png "Seletor de intervalo de datas")

* Para um intervalo predefinido: selecione na lista de incrementos de tempo comuns. O padrão é [!UICONTROL Last 30 days]*.

* Para um intervalo específico, siga um destes procedimentos:

   * Clique em ![Calendário](/help/dsp/assets/calendar.png "Calendário")e, em seguida, clique na data de início e na data de término dentro do calendário.

   * Clique dentro do intervalo de datas e, em seguida, insira uma data de início e uma data de término ou selecione-as no calendário.

     Você pode inserir valores numéricos (de M-D-AA a MM-DD-AAAA) e/ou nomes de meses ou abreviações (como Jan ou Janeiro).

### Classificar uma Coluna de Dados

Você pode classificar qualquer coluna de dados em ordem crescente (A a Z ou 1 a 10) ou decrescente (Z a A ou 10 a 1).

* Clique no cabeçalho da coluna para alternar entre ordem crescente e decrescente.


### Especificar o Número de Linhas de Dados

Na parte inferior direita de qualquer página, ao lado de **[!UICONTROL Items per page]** , selecione *[!UICONTROL 25]*, *[!UICONTROL 50]* ou *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios de Desempenho em Visualizações do Campaign Management](campaign-reports-about.md)
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Exibir o Relatório de Previsão de Posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Exibir os Relatórios de Diagnóstico de Posicionamento](placement-diagnostics.md)
>* [Exportar dados de uma visualização do Campaign Management](campaign-export-data.md)
>* [Vídeo: Estrutura de conta e interface do usuário do DSP](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
