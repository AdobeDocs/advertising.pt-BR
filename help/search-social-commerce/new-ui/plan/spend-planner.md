---
title: Usando o [!UICONTROL Spend Planner]
description: Saiba como gerar, baixar e aplicar recomendações de orçamento de portfólio para ajudar você a alcançar a distribuição de gastos ideal em seus portfólios.
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 111739ac2da47170575d9b4dad39cfefe812fe0f
workflow-type: tm+mt
source-wordcount: 798
ht-degree: 0%

---

# Usando o [!UICONTROL Spend Planner]

O [!UICONTROL Spend Planner] (chamado de &quot;[!UICONTROL Spend Recommendation Tool]&quot; na interface do usuário herdada) identifica a distribuição de gastos ideal entre portfólios otimizados e ativos com o mesmo objetivo e moeda para que você possa maximizar a receita ou direcionar metas para o conjunto de portfólios.

Ao exibir um relatório de recomendação de gastos para portfólios com orçamentos diários, você pode alterar os orçamentos de qualquer um dos portfólios para os orçamentos recomendados.

## Dados no relatório [!UICONTROL Spend Planner]

Para portfólios com o objetivo [!UICONTROL Maximize Clicks], o relatório inclui recomendações de gastos e projeções de cliques. Para todos os outros objetivos, o relatório inclui recomendações de gastos e projeções de receita.

Os relatórios de recomendação de gastos incluem os seguintes dados:

* Um gráfico de linhas de dispersão mostra a receita ou os cliques máximos previstos que podem ser obtidos com um determinado custo total para o conjunto de portfólios quando as metas de gastos individuais são definidas de maneira ideal. O custo previsto para cada ponto de receita ou de clique é incluído.

* Dois gráficos de rosca mostrando o gasto e a receita esperada ou a distribuição de cliques por portfólio para 1\) as metas de gastos atuais e 2\) as metas de gastos propostas.

* Um gráfico de barras para cada um dos portfólios, mostrando o gasto diário recomendado (custo) e a distribuição de receita prevista ou a distribuição de cliques quando você mantém a meta de gasto diário total atual em todos os portfólios selecionados, ou para uma meta de gasto total proposta. Opcionalmente, é possível aplicar as metas de gastos recomendadas aos portfólios selecionados, o que afeta a licitação no próximo ciclo de execução de lances.

## Ações disponíveis

* Gerar um relatório [!UICONTROL Spend Planner] a partir da [nova interface](#spend-recommendations-generate) ou da [interface herdada](#spend-recommendations-generate-legacy)

* [Aplicar recomendações de gastos](#spend-recommendations-apply) aos portfólios correspondentes.

* [Abrir ou salvar dados de relatório de recomendações de gastos em um arquivo](#spend-recommendations-download)

## (Nova interface do usuário) Gerar um relatório [!UICONTROL Spend Planner] {#spend-recommendations-generate}

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

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To view the recommended daily spend and predicted revenue for each of the portfolios using a new total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## (Interface herdada) Gerar um relatório [!UICONTROL Spend Recommendation] a partir da exibição [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation] {#spend-recommendations-generate-legacy}

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

## Aplicar recomendações de gastos {#spend-recommendations-apply}

*Portfólios com orçamentos diários apenas*

>[!NOTE]
>
>* Se as alterações aplicadas aumentarem ou diminuírem a meta de gastos de qualquer portfólio em mais de 20%, você deverá aprovar a alteração.
>* Quando a meta de gastos de um portfólio é alterada em mais de 20%, o Search, Social e Commerce leva de 3 a 4 dias para ajustar seus modelos e atingir a nova meta.

1. Exibir o relatório de recomendações de gastos para um ou mais portfólios com orçamentos diários.

1. Marque a caixa de seleção ao lado de cada portfólio para o qual deseja aplicar o target de gasto recomendado. Para selecionar todos os portfólios, marque a caixa de seleção ao lado de **[!UICONTROL Select All Recommendations]**.

1. Clique em **[!UICONTROL Apply Selected Recommendations]**.

1. (Se qualquer um dos orçamentos for alterado em mais de 20%) Na mensagem de confirmação, clique em **[!UICONTROL Yes]** para aprovar as alterações.

<!-- 

New UI: Verify/edit all steps and edit accordingly:

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.
...

 -->

## Abrir ou salvar dados como um arquivo de pasta de trabalho [!DNL Microsoft Excel] {#spend-recommendations-download}

1. Gerar um relatório de recomendações de gastos para portfólios selecionados.

1. Acima do relatório, clique em ![Baixar](/help/search-social-commerce/assets/download-spend-recommendation.png "Baixar").

   Abra ou salve o arquivo de acordo com o procedimento normal do navegador. Para obter mais informações, consulte a ajuda online do navegador.

<!--

New UI:  Verify/edit all steps and edit accordingly:

1. [Generate a spend recommendation report](#spend-recommendations-generate).
...
-->
