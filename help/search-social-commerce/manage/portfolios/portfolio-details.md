---
title: (Nova interface de usuário) Exibir detalhes de desempenho do portfólio
description: Saiba como visualizar o desempenho do portfólio, os detalhes da unidade de oferta de palavra-chave, as previsões e o histórico de ofertas, além de exportar o histórico de unidades de oferta no Adobe Advertising Search, Social e Commerce.
feature: Search Portfolios, Search Optimization
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
TQID: 'https://experienceleague.adobe.com/5hNxKu6YjJTWI4KGEc6aaYnpgXK6k3OsN0-YfetzENw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 157c45d4939eff028543a0181397a59e6346309e
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 0%
---
# (Nova interface de usuário) Exibir detalhes de desempenho do portfólio

*recurso do Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

A exibição detalhada do portfólio inclui as seguintes informações sobre um portfólio:

* Os valores real e previsto para até três métricas de desempenho. Os relatórios incluem os valores de métrica total do portfólio e o detalhamento de métrica por data.<!-- Not for active portfolios only?  -->

* Dados de precisão do modelo para portfólios ativos, que mostra quanto os modelos se desviaram das previsões. O relatório mostra a precisão geral diária ou contínua dos custos por sete dias, a precisão de cliques e a precisão do valor do objetivo.

  Você pode exibir os dados como um gráfico de tendências (o padrão) ou como uma tabela.

* A meta de gastos em relação ao gasto real para portfólios ativos. Opcionalmente, também é possível incluir os orçamentos totais da campanha para o portfólio.

* A precisão das previsões de custo, clique ou [valor do objetivo](/help/search-social-commerce/glossary.md#o-p) para portfólios ativos por rede de anúncios.<!-- Verify -->

* As configurações do portfólio.

  Opcionalmente, é possível abrir as configurações do portfólio para editá-las.

* Listas das redes de anúncios, contas, campanhas, grupos de anúncios e palavras-chave no portfólio, com dados de desempenho.

  Para palavras-chave individuais, você pode exibir detalhes da unidade de lance, incluindo previsões, informações históricas e informações hierárquicas. A exibição [!UICONTROL Bid Unit Details] inclui as seguintes previsões, informações históricas e hierárquicas para a unidade de oferta selecionada:

  * Guia [!UICONTROL Forecast]: os cliques, custo, custo por clique, posição e receita projetados no momento para a unidade de oferta a preços de oferta diferentes. Os dados são exibidos para todos os dispositivos e para cada tipo de dispositivo ([!UICONTROL Mobile], [!UICONTROL Computer] e [!UICONTROL Tablet]).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. -->

    **Observação:** não há dados de previsão disponíveis para um tipo de dispositivo quando não há dados específicos do dispositivo suficientes disponíveis para criar modelos e definir ajustes para esse tipo de dispositivo. **Observação:** para ver a precisão de custo ou a precisão de receita para cada unidade de oferta em um portfólio que recebeu um clique durante um intervalo de datas específico, consulte os detalhes de precisão de custo ou de precisão de receita do portfólio, respectivamente.

  * Guia [!UICONTROL History]: todos os lances nos últimos 36 dias, incluindo os seguintes dados para cada um dos lances: a data e a hora, as impressões, os cliques, o custo total, o CPC médio, a posição média e a receita ponderada mostrada pela data do clique. Os dados são exibidos para todos os dispositivos e para cada tipo de dispositivo (celular, computador e tablet).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. **Note:** Whenever the optimization method changes from v6 to v7 and vice-versa, the history data is reset the same day. -->

  * Guia [!UICONTROL Details]: a palavra-chave, o tipo de correspondência (quando aplicável) e o grupo de publicidade principal, a campanha, a conta de rede de publicidade e o portfólio ao qual a unidade de oferta pertence.

## Abrir detalhes de desempenho de um portfólio

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenha o cursor sobre o nome do portfólio e clique em ![Visão geral do Portfolio](/help/search-social-commerce/assets/portfolio-overview.png "Visão geral do Portfolio").

1. (Opcional) Para alterar o intervalo de datas dos detalhes do portfólio, clique no intervalo de datas no canto superior direito, especifique o intervalo de datas e clique em **[!UICONTROL Apply]**.

1. (Opcional) No menu **[!UICONTROL Data Aggregation]**, altere a unidade de tempo dos dados incluídos em cada linha: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly].*

   As opções disponíveis dependem do intervalo de datas selecionado. Se a agregação atual não estiver disponível para um novo intervalo de datas, outra agregação disponível será selecionada automaticamente.

1. (Opcional) No menu **[!UICONTROL Conversion Based On]**, no cabeçalho da página, selecione **[!UICONTROL Click Date]** ou **[!UICONTROL Transaction Date]**.

   Essa configuração se aplica aos dados de conversão nos relatórios de portfólio e nas listas de componentes.

Para exibir detalhes de outro portfólio, use o seletor de portfólio ao lado do nome do portfólio.

## Personalizar a guia [!UICONTROL Portfolio Overview]

* (Opcional) Para personalizar os relatórios do [!UICONTROL Portfolio Performance], siga um destes procedimentos:

  * Para alterar as métricas de desempenho usadas para as métricas totais e detalhadas, clique em **[!UICONTROL Metrics]** e selecione até três métricas.

    As métricas padrão são *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* e *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

  * Para obter as métricas detalhadas:

    * Mova o switch ao lado de **[!UICONTROL Display predictions]** para mostrar ou ocultar os valores de métrica previstos.

    * Alternar entre a exibição de gráfico (![Exibição de Gráfico](/help/search-social-commerce/assets/chart-view.png "Exibição de Gráfico")) e a exibição de tabela (![Exibição de tabela](/help/search-social-commerce/assets/table-view.png "Exibição de tabela")).

    * (Na exibição de gráfico) Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

    * (Na exibição de gráfico) Para aplicar zoom, selecione uma área no gráfico.

    * (Quando os marcadores de alteração de configuração do portfólio forem exibidos) Para exibir o histórico de alterações do portfólio para uma data marcada, clique no marcador no gráfico. Para obter mais informações sobre o histórico, consulte &quot;[Exibir o histórico de alterações de um portfólio](portfolio-view-change-history.md#portfolio-change-history)&quot;.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Model accuracy], siga um destes procedimentos:

  * Alternar entre a exibição de gráfico (![Exibição de Gráfico](/help/search-social-commerce/assets/chart-view.png "Exibição de Gráfico")) e a exibição de tabela (![Exibição de tabela](/help/search-social-commerce/assets/table-view.png "Exibição de tabela")).

  * Alternar entre a exibição de dados sobre o *[!UICONTROL Daily Accuracy]* e o *[!UICONTROL 7 Day Rolling Accuracy]*.

    [!UICONTROL 7 Day Rolling Accuracy] é a precisão média da previsão para os sete dias anteriores, expressa como uma porcentagem. Por exemplo, o valor para 8 de maio de 2025 é a precisão média para o período de 1 de maio a 7 de maio de 2025.

    [!UICONTROL 7 Day Rolling Accuracy] está disponível somente quando [!UICONTROL Data Aggregation] está definido como [!UICONTROL Daily].

  * (Na exibição de gráfico) Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Target vs actual spend], siga um destes procedimentos:

  * Mova o switch ao lado de **[!UICONTROL Display budget]** para mostrar ou ocultar o orçamento total da campanha para cada data.

  * Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

* (Opcional) Para personalizar o gráfico de tendências [!UICONTROL Network Accuracy], siga um destes procedimentos:

  * Alterar a métrica relatada para *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Objective Value]*.

  * Quando os dados estiverem disponíveis para mais de uma rede, selecione a rede no menu ao lado do menu de métricas.

  * Para ver os dados de qualquer ponto no gráfico, mantenha o cursor sobre esse ponto.

  * Para aplicar o zoom, selecione uma área no gráfico.

## Personalizar as listas de componentes do portfólio

As guias [!UICONTROL Networks], [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Keywords] incluem os seguintes controles:

* Para pesquisar por nome, informe o texto no campo de pesquisa acima da tabela e envie a pesquisa.

* Para [filtrar os dados](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md), clique em ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro"). É possível editar ou remover filtros aplicados usando os controles de filtro acima da tabela.

* Para exibir os componentes de uma rede, conta, campanha ou grupo de anúncios na próxima guia, clique no nome. O pai selecionado é mostrado na navegação estrutural acima da tabela, e os filtros aplicáveis são transportados à medida que você faz drill-down. As seleções principais podem continuar a restringir a lista quando você troca de guias.

  Para remover uma seleção detalhada (como um nome de conta ou rede), clique em **[!UICONTROL X]** ao lado do nome do componente na navegação estrutural acima da tabela. As seleções principais de nível superior podem permanecer em vigor. Para retornar a todos os componentes no portfólio, remova as seleções principais restantes e quaisquer outros filtros.

* Para atualizar os dados, clique em ![Atualizar](/help/search-social-commerce/assets/refresh-new.png "Atualizar").

* (Somente as guias [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Keywords]) Para alterar as colunas exibidas ou a ordem de classificação, clique em ![Colunas Personalizadas](/help/search-social-commerce/assets/custom-columns-new.png "Colunas Personalizadas") e [editar o conjunto de colunas e as opções de classificação](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md).


## Listar as redes de anúncios no portfólio

* Clique na guia **[!UICONTROL Networks]**.

## Listar as contas no portfólio

* Para exibir todas as contas no portfólio, clique na guia **[!UICONTROL Accounts]**.

* Para exibir contas de uma rede específica do portfólio, clique na guia **[!UICONTROL Networks]** e, em seguida, clique no nome da rede.

## Listar as campanhas no portfólio

Os detalhes sobre cada campanha incluem a estratégia de oferta; o custo real e previsto, os cliques e o valor do objetivo; e a precisão do valor de custo, clique e objetivo.

* Para exibir todas as campanhas no portfólio, clique na guia **[!UICONTROL Campaigns]**.

* Para exibir campanhas para uma conta específica no portfólio, clique na guia **[!UICONTROL Accounts]** e clique no nome da conta.

## Listar os grupos de publicidade no portfólio

Os detalhes sobre cada grupo de anúncios incluem a rede, a oferta padrão, o custo, os cliques, o CPC, as impressões, o valor do objetivo e as métricas de conversão usadas no objetivo do portfólio.

* Para exibir todos os grupos de anúncios no portfólio, clique na guia **[!UICONTROL Ad Groups]**.

* Para exibir todos os grupos de anúncios em uma campanha no portfólio, clique na guia **[!UICONTROL Campaigns]** e, em seguida, clique no nome da campanha.

## Listar e exibir detalhes sobre palavras-chave no portfólio {#bid-unit-details}

Os detalhes de cada palavra-chave incluem a ID da unidade de oferta; o tipo de correspondência; o custo real e previsto, os cliques e o valor do objetivo; e a diferença entre o custo, o clique e o valor do objetivo. Você pode exibir detalhes da unidade de oferta sobre uma palavra-chave individual.

1. Liste as palavras-chave:

   * Para exibir todas as palavras-chave do portfólio, clique na guia **[!UICONTROL Keywords]**.

   * Para exibir todas as palavras-chave em um grupo de anúncios dentro do portfólio, clique na guia **[!UICONTROL Ad Groups]** e, em seguida, clique no nome do grupo de anúncios.

1. (Opcional) Para exibir detalhes sobre uma unidade de oferta específica, clique no valor na coluna **[!UICONTROL Bid Unit ID]**. Clique em qualquer guia no [!UICONTROL Bid Unit Details] para obter mais informações.

### Exibir e baixar o histórico de uma unidade de oferta individual {#bid-unit-history}

1. [Abra os detalhes da unidade de oferta](#bid-unit-details).

1. Clique na guia **[!UICONTROL History]**.

1. (Opcional) No menu de dispositivos acima da tabela, selecione um tipo de dispositivo cujo histórico deseja exibir. Por padrão, os dados de todos os dispositivos são exibidos.

1. (Opcional) Quando os dados do histórico estiverem disponíveis, clique em **[!UICONTROL Export as csv]** para baixar o histórico exibido.

O arquivo é baixado de acordo com o procedimento normal do navegador.

Para exibir o histórico de lances de todo o portfólio e alterar seu intervalo de datas, consulte &quot;[Exibir o histórico de alterações de lances de um portfólio](portfolio-view-change-history.md#portfolio-bid-change-history)&quot;.

## Exibir e editar as configurações do portfólio

* Para exibir ou ocultar as configurações do portfólio, clique em **[!UICONTROL Portfolio Settings]**.

  * Para editar configurações visíveis do portfólio, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da seção de configuração e [editar as configurações do portfólio](portfolio-edit.md).

Para obter mais informações sobre as configurações do portfólio, consulte o Guia de otimização, disponível no Search, Social e Commerce.

## Baixe relatórios de desempenho do portfólio e listas dos componentes do portfólio

* Para fazer download de relatórios de desempenho e listas de componentes:

  1. Na barra de ferramentas, clique em **[!UICONTROL Download report]**.

  1. Marque a caixa de seleção ao lado de cada relatório de desempenho e tipo de componente de portfólio a ser incluído.

     Os componentes do portfólio disponíveis são *[!UICONTROL Campaigns table]*, *[!UICONTROL Ad groups table]* e *[!UICONTROL Keywords table]*. As tabelas [!UICONTROL Networks] e [!UICONTROL Accounts] não estão incluídas neste download.

     Para relatórios de desempenho com ambas as opções, selecione **[!UICONTROL As chart]**, **[!UICONTROL As table]** ou ambos. O relatório [!UICONTROL Network accuracy chart] está disponível apenas como um gráfico.

  1. Clique em **[!UICONTROL Download report]**.

* Para baixar um relatório [!UICONTROL Model accuracy] com tipos específicos de dados:

  1. Na barra de ferramentas de [!UICONTROL Model accuracy], clique em **[!UICONTROL Download report]**.

  1. Selecione **[!UICONTROL Cost Accuracy]**, **[!UICONTROL Objective Value Accuracy]** ou ambos.

  1. Para cada tipo de dados selecionado, selecione **[!UICONTROL By Bid Unit]**, **[!UICONTROL By Click Volume]** ou ambos.

  1. Clique em **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(Nova Interface do Usuário) Sobre portfólios](portfolio-about.md)
>* [(Nova interface do usuário) Editar um portfólio](portfolio-edit.md)
>* [(Nova interface do usuário) Baixar dados na [!UICONTROL Portfolios] exibição](portfolio-view-report.md)
