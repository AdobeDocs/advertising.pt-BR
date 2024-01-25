---
title: Gerenciar as visualizações de dados do Campaign
description: Saiba como personalizar as visualizações de dados para campanhas, pacotes, posicionamentos e anúncios.
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Gerenciar as visualizações de dados do Campaign

## Gerenciar visualizações de dados

É possível alterar as métricas e o modo de gráfico para todas as visualizações de dados em campanhas ou para uma única campanha. As alterações em uma única campanha são aplicadas em todas as visualizações de dados da campanha, incluindo a [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads] guias.

### Alterar as métricas para uma visualização de dados

1. No canto superior direito da visualização de dados, clique em ![Configurações](/help/dsp/assets/settings-chart.png).
1. Selecione as métricas.
Não é possível selecionar a mesma métrica duas vezes.
1. Clique em **[!UICONTROL Apply]**.

### Alterar o modo de exibição de uma visualização de dados

* No canto superior direito da visualização de dados, clique no [!UICONTROL Overlay] alternar (![Chave de sobreposição](/help/dsp/assets/overlay.png)) para alterar entre o modo de sobreposição (todos os gráficos sobrepostos) e o modo de gráfico de treliça (três gráficos separados).

## Gerenciar Tabelas de Dados

Em todas as exibições de gerenciamento de campanha ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]), é possível personalizar os dados exibidos na tabela de dados.

### Alterar a Exibição de Coluna

* No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique no nome da exibição de coluna desejada.

### Criar uma Exibição de coluna personalizada

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique em **[!UICONTROL Create View]**.

1. Especifique as métricas a serem incluídas na exibição:

   1. Na lista de métricas disponíveis, marque a caixa de seleção ao lado de cada métrica a ser incluída.

   1. Edite a ordem da coluna, conforme necessário, clicando nos nomes das colunas no painel direito e arrastando-as para as posições necessárias.

   Algumas colunas têm posições fixas e não podem ser movidas ou removidas.

1. Aplique ou salve as configurações:

   * Para aplicar as configurações temporariamente sem salvá-las na exibição, clique em **[!UICONTROL Apply].**

   * Para salvar as configurações em uma exibição de coluna nova e personalizada, clique em **[!UICONTROL Save As]**. No [!UICONTROL Save View] insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

### Editar uma Exibição de coluna personalizada

>[!NOTE]
>
>Não é possível editar uma exibição de coluna padrão (predefinida).

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e, em seguida, clique no nome da exibição de coluna existente.

1. No Seletor de exibições, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png)e clique em **[!UICONTROL Edit View]**.

1. Edite as métricas a serem incluídas na exibição:

   1. Na lista de métricas disponíveis, marque a caixa de seleção ao lado de cada métrica a ser incluída e desmarque a caixa de seleção ao lado de cada métrica a ser excluída.

   1. Edite a ordem da coluna, conforme necessário, clicando nos nomes das colunas no painel direito e arrastando-as para as posições necessárias.

   Algumas colunas têm posições fixas e não podem ser movidas ou removidas.

1. Aplique ou salve as configurações:

   * Para aplicar as configurações temporariamente sem salvá-las na exibição, clique em **[!UICONTROL Apply].**

   * Para salvar as configurações em uma exibição de coluna nova e personalizada, clique em **[!UICONTROL Save As]**. No [!UICONTROL Save View] insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

### Filtrar dados de campanha

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

### Classificar uma Coluna de Dados

Você pode classificar qualquer coluna de dados em ordem crescente (A a Z ou 1 a 10) ou decrescente (Z a A ou 10 a 1).

* Clique no cabeçalho da coluna para alternar entre ordem crescente e decrescente.

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Na Plataforma](campaign-reports-about.md)
>* [Gerenciar visualizações de dados](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Alterar a Exibição de Coluna](column-view-change.md)
>* [Criar uma Exibição de coluna personalizada](column-view-create.md)
>* [Editar uma Exibição de coluna personalizada](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filtrar dados de campanha](campaign-data-filter.md)
>* [Classificar uma Coluna de Dados](campaign-data-sort.md)
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Exibir o Relatório de Previsão de Posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Exibir os Relatórios de Diagnóstico de Posicionamento](placement-diagnostics.md)
>* [Exportar dados de uma visualização do Campaign Management](campaign-export-data.md)
>* [Vídeo: Estrutura de conta e interface do usuário do DSP](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
