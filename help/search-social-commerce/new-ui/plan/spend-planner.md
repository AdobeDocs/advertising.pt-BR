---
title: Usando o [!UICONTROL Spend Planner]
description: Saiba como usar o [!UICONTROL Spend Planner] para identificar a distribuição de gastos ideal entre portfólios.
feature: Search Optimization, Search Portfolios, Search Simulations
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
source-git-commit: ff4deeb1cfbcd863e5b0ef2ac9b2f7124906c3dd
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Usando o [!UICONTROL Spend Planner]

<!-- When this becomes a menu item, move file and TOC entry accordingly -->

A [!UICONTROL Spend Planner] (chamada de &quot;Ferramenta de recomendação de gastos&quot; na interface do usuário herdada) identifica a distribuição de gastos ideal entre portfólios otimizados e ativos com o mesmo objetivo e moeda para que você possa maximizar a receita ou direcionar metas para o conjunto de portfólios.

Ao exibir um relatório de recomendação de gastos para portfólios com orçamentos diários, você pode alterar os orçamentos de qualquer um dos portfólios para os orçamentos recomendados.

## Dados no relatório [!UICONTROL Spend Planner]

Para portfólios com o objetivo [!UICONTROL Maximize Clicks], o relatório inclui recomendações de gastos e projeções de cliques. Para todos os outros objetivos, o relatório inclui recomendações de gastos e projeções de receita.

Os relatórios de recomendação de gastos incluem os seguintes dados:

* Um gráfico de linhas de dispersão mostra a receita ou os cliques máximos previstos que podem ser obtidos com um determinado custo total para o conjunto de portfólios quando as metas de gastos individuais são definidas de maneira ideal. O custo previsto para cada ponto de receita ou de clique é incluído.

* Dois gráficos de rosca mostrando o gasto e a receita esperada ou a distribuição de cliques por portfólio para 1\) as metas de gastos atuais e 2\) as metas de gastos propostas.

* Um gráfico de barras para cada um dos portfólios, mostrando o gasto diário recomendado (custo) e a distribuição de receita prevista ou a distribuição de cliques quando você mantém a meta de gasto diário total atual em todos os portfólios selecionados, ou para uma meta de gasto total proposta. Opcionalmente, é possível aplicar as metas de gastos recomendadas aos portfólios selecionados, o que afeta a licitação no próximo ciclo de execução de lances.

## (Nova interface do usuário) Gerar um relatório [!UICONTROL Spend Planner]

1. Siga um destes procedimentos:

   * No menu principal, clique em **[!UICONTROL Plan]>[!UICONTROL Spend Planner]**.

   * No menu principal, clique em **[!UICONTROL Plan]>[!UICONTROL Simulations]**. Na barra de ferramentas acima da tabela de dados, clique em ![Planejador de gastos](/help/search-social-commerce/assets/spend-planner-icon.png "Planejador de gastos").

   A ferramenta [!UICONTROL Spend Recommendation] é aberta na interface do usuário herdada.

1. Visualizar dados usando os orçamentos combinados atuais para os portfólios selecionados:

   1. Selecione o objetivo do portfólio.

   1. Selecione a moeda.

   1. (Opcional) Selecione uma estratégia de gastos do portfólio para filtrar ainda mais a lista de portfólios.

   1. Marque a caixa de seleção ao lado de cada portfólio a ser incluído. Para selecionar todos os portfólios, marque a caixa de seleção ao lado de [!UICONTROL Portfolios].

      Somente portfólios otimizados e ativos com os parâmetros selecionados são listados.

   1. Clique em **[!UICONTROL Update]**.

   1. (Opcional) Para ver o custo e a receita de qualquer ponto no gráfico, mantenha o cursor sobre o ponto.

1. (Opcional) Para exibir o gasto diário recomendado e a receita prevista para cada um dos portfólios usando uma nova meta de gasto total, insira uma meta de gasto diário total proposta em todos os portfólios no campo [!UICONTROL Total Spend Target]. Pressione a tecla **Enter**.

   A ferramenta de recomendação de gastos usa dados de simulações semanais, de modo que o gasto total recomendado é a correspondência mais próxima da meta de gastos proposta com a combinação de gastos ideal.

## (Interface herdada) Gerar um relatório [!UICONTROL Spend Recommendation] a partir da exibição [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation]

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**.

1. Visualizar dados usando os orçamentos combinados atuais para os portfólios selecionados:

   1. Selecione o objetivo do portfólio.

   1. Selecione a moeda.

   1. (Opcional) Selecione uma estratégia de gastos do portfólio para filtrar ainda mais a lista de portfólios.

   1. Marque a caixa de seleção ao lado de cada portfólio a ser incluído. Para selecionar todos os portfólios, marque a caixa de seleção ao lado de [!UICONTROL Portfolios].

      Somente portfólios otimizados e ativos com os parâmetros selecionados são listados.

   1. Clique em **[!UICONTROL Update]**.

   1. (Opcional) Para ver o custo e a receita de qualquer ponto no gráfico, mantenha o cursor sobre o ponto.

1. (Opcional) Para exibir o gasto diário recomendado e a receita prevista para cada um dos portfólios usando uma nova meta de gasto total, insira uma meta de gasto diário total proposta em todos os portfólios no campo [!UICONTROL Total Spend Target]. Pressione a tecla **Enter**.

   A ferramenta de recomendação de gastos usa dados de simulações semanais, de modo que o gasto total recomendado é a correspondência mais próxima da meta de gastos proposta com a combinação de gastos ideal.

## Aplicar recomendações de gastos

*Portfólios com orçamentos diários apenas*

>[!NOTE]
>
>* Se as alterações aplicadas aumentarem ou diminuírem a meta de gastos de qualquer portfólio em mais de 20%, você receberá uma notificação e deverá aprovar a alteração.
>* Quando a meta de gastos de um portfólio é alterada em mais de 20%, o Search, Social e Commerce leva de 3 a 4 dias para ajustar seus modelos e atingir a nova meta.

1. Exibir o relatório de recomendações de gastos para um ou mais portfólios com orçamentos diários.

1. Marque a caixa de seleção ao lado de cada portfólio para o qual deseja aplicar o target de gasto recomendado. Para selecionar todos os portfólios, marque a caixa de seleção ao lado de [!UICONTROL Select All Recommendations].

1. Clique em **[!UICONTROL Apply Selected Recommendations]**.

1. (Se qualquer um dos orçamentos for alterado em mais de 20%) Na mensagem de confirmação, clique em **[!UICONTROL Yes]** para aprovar as alterações.

## Abrir ou salvar dados em um arquivo

Você pode exportar dados de relatório de qualquer seção do relatório [!UICONTROL Spend Recommendation]. Você pode abrir ou salvar os dados como um arquivo de pasta de trabalho [!DNL Microsoft Excel].

1. Gerar um relatório de recomendações de gastos para portfólios selecionados.

1. Acima do relatório, clique em ![Baixar](/help/search-social-commerce/assets/download-spend-recommendation.png "Baixar").

   Abra ou salve o arquivo de acordo com o procedimento normal do navegador.  Para obter mais informações, consulte a ajuda online do navegador.
