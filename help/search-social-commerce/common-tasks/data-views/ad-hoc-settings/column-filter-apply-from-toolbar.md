---
title: Aplicar filtros de dados na barra de ferramentas
description: Saiba como filtrar os dados da página na barra de ferramentas.
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Aplicar filtros de dados na barra de ferramentas

É possível aplicar quantos filtros desejar a uma exibição. Todos os filtros são unidos por meio do operador AND.

1. Na barra de ferramentas, clique em ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro").

1. Nas configurações de filtro, execute um dos procedimentos a seguir:

   * Para adicionar um filtro, clique em ![Adicionar filtro](/help/search-social-commerce/assets/add.png "Adicionar filtro") **[!UICONTROL ADD FILTER]**, e faça o seguinte:

      1. (Opcional) Para filtrar os nomes das colunas por sequência de texto, insira a sequência de pesquisa na **[!UICONTROL ADD FILTER]** campo de entrada.

      1. Selecione um nome de coluna no menu de colunas.

      1. Defina o filtro na coluna:

         * (Filtros sem campos de entrada) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado do segundo menu e, em seguida, marque as caixas de seleção ao lado de cada valor a ser incluído.

         * (Filtros com campos de entrada) Selecione um operador no segundo menu e insira o valor aplicável.

           Por exemplo, se você selecionou a opção &quot;[!UICONTROL Clicks]&quot; e quiser retornar apenas linhas com mais de 100 cliques, depois selecione *[!UICONTROL greater than]*&quot; e insira `100` no campo de entrada.

           Dependendo do tipo de dados, os operadores disponíveis podem incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

           **Nota:** Os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você filtrar por campanhas com &quot;loan&quot; no nome, os resultados incluirão &quot;Consumer Loans&quot; e &quot;loan applications&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements], e [!UICONTROL Auto Targets] somente exibições; opcional) Alterar a configuração para &quot;[!UICONTROL Include rows with performance data only].&quot;

           **Aviso:** Se você desmarcar a opção e a exibição incluir muitas entidades sem dados de desempenho, os dados levarão mais tempo para serem exibidos.

   * Para editar um filtro existente, clique no filtro, altere a definição do filtro e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

   * Para remover um filtro existente, clique em **[!UICONTROL X]** ao lado da definição do filtro.

1. Clique em **[!UICONTROL Apply]**.
