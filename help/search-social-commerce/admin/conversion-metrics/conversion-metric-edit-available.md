---
title: Alterar as métricas de conversão disponíveis em exibições de gerenciamento e relatórios
description: Saiba como disponibilizar métricas de conversão em suas visualizações de gerenciamento e relatórios.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Alterar as métricas de conversão disponíveis em exibições de gerenciamento e relatórios

Quando o Adobe Advertising rastreia uma métrica de [conversão](/help/search-social-commerce/glossary.md#c-d) para um anunciante, ela é inicialmente excluída dos objetivos do portfólio, dos relatórios e das exibições de gerenciamento. Para tornar uma métrica de conversão visível, você deve disponibilizá-la explicitamente e, opcionalmente, alterar o nome de exibição padrão, que é o nome mostrado. A única exceção é que as conversões rastreadas pelas tags de rastreamento de evento universal [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] ficam automaticamente disponíveis e visíveis.

Da mesma forma, é possível ocultar uma métrica de conversão dos objetivos do portfólio, dos relatórios e das visualizações de gerenciamento. Quando você oculta uma métrica de conversão que estava visível anteriormente, ela é removida de qualquer métrica derivada que contenha a métrica de conversão.

A partir da lista de métricas de conversão disponíveis, cada usuário com acesso aos dados do anunciante pode personalizar as métricas que visualizam para exibições de gerenciamento e relatórios, incluindo ou omitindo métricas específicas à sua escolha.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Todas as métricas de conversão coletadas para o anunciante e todos os nomes diferentes especificados para exibição são listados.

1. (Opcional) Filtre a lista:

   * Para procurar um nome de métrica ou nome para exibição específico, clique em ![Pesquisar](/help/search-social-commerce/assets/search.png "Pesquisar"), digite a palavra ou a cadeia de caracteres no campo de entrada e pressione a tecla **[!DNL Enter]**.

     Você pode pesquisar cadeias de caracteres que apareçam em qualquer lugar dentro da frase (como a primeira letra ou as três últimas letras), e os termos de pesquisa não diferenciam maiúsculas de minúsculas[1&rbrace;.](/help/search-social-commerce/glossary.md#c-d)

   * Para procurar métricas de conversão por sua disponibilidade em exibições de gerenciamento e relatórios, clique em ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") e selecione o filtro **[!UICONTROL Show in UI and Reports]**. Em seguida, selecione **[!UICONTROL Show]** (para exibir as métricas de conversão disponíveis para inclusão nos relatórios e exibições de gerenciamento) ou **[!UICONTROL Hide]** (para exibir as métricas de conversão não disponíveis nos relatórios e exibições de gerenciamento).

1. Altere as métricas de conversão disponíveis para exibições de gerenciamento e relatórios:

   * Para mostrar ou ocultar uma única métrica, clique na opção na coluna **[!UICONTROL Show in UI and Reports]** para alterar a configuração.

   * Para mostrar ou ocultar várias métricas, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada métrica de conversão.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Na barra de ferramentas acima da tabela de dados, clique em ![Mostrar](/help/search-social-commerce/assets/show.png "Mostrar") para mostrar as métricas ou ![Ocultar](/help/search-social-commerce/assets/hide.png "Ocultar") para ocultar as métricas.

      1. (Para ocultar métricas) Na mensagem de confirmação, clique em **[!UICONTROL Yes]** para ocultar as métricas, incluindo a remoção delas de qualquer métrica derivada que contenha as métricas.

1. (Opcional) [Altere o nome que aparece nos cabeçalhos de coluna](conversion-metric-edit-display-name.md) para qualquer uma das métricas de conversão.

   O nome de exibição padrão para cada métrica de conversão visível é o nome da métrica conforme é digitado nos dados recuperados.

>[!NOTE]
>
>Se o Adobe Advertising coletar dados para novas métricas de conversão, as novas métricas — exceto para conversões rastreadas pelas tags de rastreamento de evento universal [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] — serão automaticamente excluídas das exibições e dos relatórios de gerenciamento até que você as inclua. Novas conversões controladas por [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] marcas de rastreamento de eventos universais estão sempre disponíveis automaticamente.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento das métricas de conversão de um anunciante](conversion-metric-about.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](conversion-metric-view-tracked.md)
>* [Alterar o nome para exibição de uma métrica de conversão](conversion-metric-edit-display-name.md)
