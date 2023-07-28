---
title: Editar filtros de coluna
description: Saiba como editar filtros de coluna.
exl-id: 6e42e006-089b-44b9-b9b1-66835b680413
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Editar filtros de coluna

## Editar um conjunto de filtros

1. Clique em ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") na barra de ferramentas.

1. Nas configurações de filtro, execute um dos procedimentos a seguir:

   * Para adicionar um filtro, clique em ![Adicionar filtro](/help/search-social-commerce/assets/add.png "Adicionar filtro") **[!UICONTROL ADD FILTER]** , e faça o seguinte:

      1. (Opcional) Para filtrar os nomes das colunas por sequência de texto, insira a sequência de pesquisa na **[!UICONTROL ADD FILTER]** campo de entrada.

      1. Selecione um nome de coluna no menu de colunas.

      1. Defina o filtro na coluna:

         * (Filtros sem campos de entrada) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado do segundo menu, marque as caixas de seleção ao lado de cada valor a ser incluído e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

         * (Filtros com campos de entrada) Selecione um operador no segundo menu, insira o valor aplicável e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

           Por exemplo, se você selecionou a opção &quot;[!UICONTROL Clicks]&quot; e quiser retornar apenas linhas com mais de 100 cliques, depois selecione *[!UICONTROL greater than]*&quot; e insira `100` no campo de entrada.

           Dependendo do tipo de dados, os operadores disponíveis podem incluir *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* ou *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

           **Nota:** Os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você pesquisar campanhas com &quot;loan&quot; no nome, os resultados incluirão &quot;Consumer Loans&quot; e &quot;loan applications&quot;.

   * Para editar um filtro existente, clique no filtro, altere a definição do filtro e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

   * Para remover um filtro existente, clique em **[!UICONTROL X]** ao lado da definição do filtro.

1. ([!UICONTROL Keywords] somente visualização; opcional) Selecione ou desmarque a configuração como &quot;[!UICONTROL Include rows with no performance data].&quot;

   >[!WARNING]
   >
   >Selecionar essa opção aumenta o tempo de carregamento da página.

1. Clique em **[!UICONTROL Apply]**.

## Editar um único filtro

1. (Se necessário) No conjunto de filtros acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais") para expandir o conjunto de filtros.

1. Acima da tabela de dados, clique na definição do filtro.

1. Edite os filtros a serem aplicados:

   1. (Opcional) Edite o nome da coluna no menu de colunas.

   1. (Opcional) Redefina o filtro na coluna:

      * (Filtros sem campos de entrada) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado do segundo menu, marque as caixas de seleção ao lado de cada valor a ser incluído e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

      * (Filtros com campos de entrada) Selecione um operador no segundo menu, insira o valor aplicável e clique em ![Atualizar filtro](/help/search-social-commerce/assets/select.png "Atualizar filtro").

        Por exemplo, se você selecionou a opção &quot;[!UICONTROL Clicks]&quot; e quiser retornar apenas linhas com mais de 100 cliques, depois selecione *[!UICONTROL greater than]*&quot; e insira `100` no campo de entrada

        Dependendo do tipo de dados, os operadores disponíveis podem incluir *[!UICONTROL greater than]*, *menor que*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *não contém* ou *começa com.*

        **Nota:** Os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você pesquisar campanhas com &quot;loan&quot; no nome, os resultados incluirão &quot;Consumer Loans&quot; e &quot;loan applications&quot;.
