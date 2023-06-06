---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Modelo de anúncio de texto - Filtro de feed

**\[Filtro do feed\]:** Quais linhas devem ser propagadas no arquivo de feed:

* *[!UICONTROL Propagate all rows found in feed:]* (O padrão) Para propagar dados para todas as linhas.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Para propagar dados somente para linhas que atendam a até dez condições especificadas. Especifique os filtros a serem aplicados:

   1. Selecione a operação booleana a ser usada para todos os filtros:  **[!UICONTROL AND]** ou **[!UICONTROL OR]**.

   1. Selecione um nome de coluna no primeiro menu, selecione um operador no segundo menu e, em seguida, insira os valores aplicáveis ou deixe o campo de entrada em branco para propagar dados para linhas sem condições.

   A lista de colunas inclui todas as colunas disponíveis no feed.

   Os operadores disponíveis incluem *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (não é igual a), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]*, e *[!UICONTROL greater than]*. Quando você seleciona o operador &quot;[!UICONTROL in],&quot; você pode inserir uma lista de valores separados por vírgulas; se um registro corresponder a qualquer um dos valores especificados, os dados serão propagados para essas linhas. Para todos os outros operadores, insira apenas um valor. Os valores não diferenciam maiúsculas de minúsculas.

   Por exemplo, se você selecionou a coluna &quot;product_type&quot; e deseja retornar somente linhas para nomes de produtos contendo &quot;shoes&quot;, então selecione &quot;**[!UICONTROL contains]**&quot; e insira `shoes` no campo de entrada.

   1. (Para aplicar até nove filtros adicionais) Para cada filtro adicional, clique em **[!UICONTROL Add Condition]** e especifique o filtro adicional por Etapa 2.
