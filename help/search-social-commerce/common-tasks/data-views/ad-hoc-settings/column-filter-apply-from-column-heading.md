---
title: Aplicar filtros de dados a partir de um menu de cabeçalho de coluna
description: Saiba como filtrar os dados da página no menu de cabeçalho de coluna.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Aplicar um filtro de dados a partir de um menu de cabeçalho de coluna

É possível aplicar quantos filtros desejar a uma coluna, um de cada vez. Todos os filtros são unidos por meio do operador AND. Para adicionar mais de um filtro por vez usando todas as métricas disponíveis, consulte &quot;[Aplicar filtros de dados na barra de ferramentas](column-filter-apply-from-toolbar.md).&quot;

1. No lado direito do cabeçalho da coluna, clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Seta para baixo")e clique em **[!UICONTROL Add Filter]**.

1. Defina o filtro na coluna:

   * (Filtros sem campos de entrada) Marque as caixas de seleção ao lado de cada valor a ser incluído e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

   * (Filtros com campos de entrada) Selecione um operador no segundo menu, insira o valor aplicável e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

      Por exemplo, se você selecionou a opção &quot;[!UICONTROL Clicks]&quot; e quiser retornar apenas linhas com mais de 100 cliques, depois selecione *[!UICONTROL greater than]*&quot; e insira `100` no campo de entrada Dependendo do tipo de dados, os operadores disponíveis podem incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* Os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você filtrar por campanhas com &quot;loan&quot; no nome, os resultados incluem &quot;Consumer Loans&quot; e &quot;loan applications&quot;.
      >* Você pode aplicar apenas um filtro numérico simples (como [!UICONTROL Impressions] \> 100) por coluna.

