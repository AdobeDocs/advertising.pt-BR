---
title: (Nova interface de usuário) Exibir detalhes de desempenho do portfólio
description: Saiba como visualizar detalhes do desempenho do portfólio, incluindo métricas reais e previstas no nível de portfólio e para cada campanha atribuída.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: fee9c6e4649c348cad7561f81a9d45d92eb672ec
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# (Nova interface de usuário) Exibir detalhes de desempenho do portfólio

*recurso do Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

A exibição detalhada do portfólio inclui as seguintes informações sobre um portfólio:

* Os valores real e previsto para até três métricas de desempenho. Os relatórios incluem os valores de métrica total do portfólio e o detalhamento de métrica por data.<!-- Not for active portfolios only?  -->

* Dados de precisão do modelo para portfólios ativos, que mostra quanto os modelos se desviaram das previsões. O relatório mostra a precisão geral diária ou contínua dos custos por sete dias, a precisão de cliques e a precisão do valor do objetivo.

  Você pode exibir dados por data de clique (o padrão) ou por data de transação.   Você também pode exibir os dados como um gráfico de tendências (o padrão) ou como uma tabela.

* A meta de gastos em relação ao gasto real para portfólios ativos. Opcionalmente, também é possível incluir os orçamentos totais da campanha para o portfólio.

* A precisão das previsões de custo, clique ou [valor do objetivo](/help/search-social-commerce/glossary.md#o-p) para portfólios ativos por rede de anúncios.<!-- Verify -->

* As configurações do portfólio.

  Opcionalmente, é possível abrir as configurações do portfólio para editá-las.

## Abrir detalhes de desempenho de um portfólio

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Clique no nome do portfólio.

1. (Opcional) No menu **[!UICONTROL Granularity]**, altere a granularidade dos dados entre *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly].*

1. (Opcional) Para alterar o intervalo de datas dos detalhes do portfólio, clique no intervalo de datas no canto superior direito, especifique o intervalo de datas e clique em **[!UICONTROL Apply]**.

## Personalizar a guia [!UICONTROL Portfolio Overview]

* (Opcional) Para personalizar os relatórios do [!UICONTROL Portfolio Performance], siga um destes procedimentos:

   * Para alterar as métricas de desempenho usadas para as métricas totais e detalhadas, clique em **[!UICONTROL Metrics]** e selecione até três métricas.

     As métricas padrão são *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* e *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Para obter as métricas detalhadas:

      * Mova o switch ao lado de **[!UICONTROL Display predictions]** para mostrar ou ocultar os valores de métrica previstos.

      * Alternar entre a exibição de gráfico (![Exibição de Gráfico](/help/search-social-commerce/assets/chart-view.png "Exibição de Gráfico")) e a exibição de tabela (![Exibição de tabela](/help/search-social-commerce/assets/table-view.png "Exibição de tabela")).

      * (Na exibição de gráfico) Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Model accuracy], siga um destes procedimentos:

   * Alternar entre a exibição de gráfico (![Exibição de Gráfico](/help/search-social-commerce/assets/chart-view.png "Exibição de Gráfico")) e a exibição de tabela (![Exibição de tabela](/help/search-social-commerce/assets/table-view.png "Exibição de tabela")).

   * Alternar entre a exibição de dados por *[!UICONTROL Click Date]* e *[!UICONTROL Transaction Date]*.

   * Alternar entre a exibição de dados sobre o *[!UICONTROL Daily Accuracy]* e o *[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] é a precisão média da previsão para os sete dias anteriores, expressa como uma porcentagem. Por exemplo, o valor para 8 de maio de 2025 é a precisão média para o período de 1 de maio a 7 de maio de 2025.

   * (Na exibição de gráfico) Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Target vs actual spend], siga um destes procedimentos:

   * Mova o switch ao lado de **[!UICONTROL Display budget]** para mostrar ou ocultar o orçamento total da campanha para cada data.

   * Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Network Accuracy], siga um destes procedimentos:

   * Alterar a métrica relatada para *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Objective Value]*.

   * Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

1. Clique em **[!UICONTROL Download report]**.

## Listar as campanhas no portfólio

* Clique na guia **[!UICONTROL Campaigns]**.

## Listar os grupos de publicidade no portfólio

* Para exibir todos os grupos de anúncios em uma campanha no portfólio, clique na guia **[!UICONTROL Campaigns]** e, em seguida, clique no nome da campanha.

## Listar as palavras-chave no portfólio

* Para exibir todas as palavras-chave do portfólio, clique na guia **[!UICONTROL Keywords]**.

* Para exibir todas as palavras-chave em um grupo de anúncios dentro do portfólio, clique na guia **[!UICONTROL Ad Groups]** e, em seguida, clique no nome do grupo de anúncios.

## Exibir e editar as configurações do portfólio

* Para exibir ou ocultar as configurações do portfólio, clique em **[!UICONTROL Portfolio Settings]**.

   * Para editar configurações visíveis do portfólio, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da seção de configuração e [editar as configurações do portfólio](portfolio-edit.md).

Para obter mais informações sobre as configurações do portfólio, consulte o Guia de otimização, disponível no Search, Social e Commerce.

## Baixe relatórios de desempenho do portfólio e listas dos componentes do portfólio

1. Na barra de ferramentas, clique em **[!UICONTROL Download report]**.

1. Marque a caixa de seleção ao lado de cada relatório de desempenho e tipo de componente de portfólio a ser incluído.

   Para alguns relatórios de desempenho, você pode escolher se deseja baixar os dados como um carrinho ou uma tabela.

>[!MORELIKETHIS]
>
>* [(Nova Interface do Usuário) Sobre portfólios](portfolio-about.md)
>* [(Nova interface do usuário) Editar um portfólio](portfolio-edit.md)
>* [(Nova interface do usuário) Baixar dados na [!UICONTROL Portfolios] exibição](portfolio-view-report.md)
