---
title: Alterar as propriedades de transação disponíveis em exibições de gerenciamento e relatórios
description: Saiba como disponibilizar propriedades de transação em suas visualizações de gerenciamento e relatórios.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: Search Admin, Search Transaction Properties
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Alterar as propriedades de transação disponíveis em exibições de gerenciamento e relatórios

Quando o Adobe Advertising rastreia um [propriedade de transação](/help/search-social-commerce/glossary.md#s-t) para um anunciante, ele é inicialmente excluído dos objetivos do portfólio, dos relatórios e das visualizações de gerenciamento. Para tornar uma propriedade visível, você deve torná-la disponível explicitamente e, opcionalmente, alterar o nome de exibição padrão, que é o nome mostrado. A única exceção é que as conversões são rastreadas pelo [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] as tags universais de rastreamento de eventos estão disponíveis e visíveis automaticamente.

Da mesma forma, você pode ocultar uma propriedade de objetivos de portfólio, relatórios e exibições de gerenciamento. Quando você oculta uma propriedade que estava visível anteriormente, ela é removida de qualquer métrica derivada que contenha a propriedade.

Na lista de propriedades que estão disponíveis, cada usuário com acesso aos dados do anunciante pode personalizar as propriedades que visualizam para exibições de gerenciamento e relatórios, incluindo ou omitindo propriedades específicas à sua escolha.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Todas as propriedades de transação que foram coletadas para o anunciante e todos os nomes diferentes que foram especificados para exibição são listados.

1. (Opcional) Filtre a lista:

   * Para procurar um nome de propriedade ou nome de exibição específico, clique em ![Pesquisar](/help/search-social-commerce/assets/search.png "Pesquisar"), insira a palavra ou a string no campo de entrada e pressione a tecla **[!DNL Enter]** chave.

     Você pode pesquisar cadeias de caracteres que apareçam em qualquer lugar dentro da frase (como a primeira letra ou as três últimas letras) e os termos de pesquisa não [diferencia maiúsculas de minúsculas](/help/search-social-commerce/glossary.md#c-d).

   * Para pesquisar propriedades por sua disponibilidade em exibições de gerenciamento e relatórios, clique em ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro")e selecione o filtro **[!UICONTROL Show in UI and Reports]**. Em seguida, selecione **[!UICONTROL Show]** (para exibir as propriedades disponíveis para inclusão em relatórios e exibições de gerenciamento) ou **[!UICONTROL Hide]** (para exibir as propriedades não disponíveis em relatórios e exibições de gerenciamento).

1. Altere as propriedades disponíveis para exibições e relatórios de gerenciamento:

   * Para mostrar ou ocultar uma única propriedade, clique na opção no **[!UICONTROL Show in UI and Reports]** para alterar a configuração.

   * Para mostrar ou ocultar várias propriedades, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada propriedade.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Na barra de ferramentas acima da tabela de dados, clique em ![Mostrar](/help/search-social-commerce/assets/show.png "Mostrar") para mostrar as propriedades ou ![Ocultar](/help/search-social-commerce/assets/hide.png "Ocultar") para ocultar as propriedades.

      1. (Para ocultar propriedades) Na mensagem de confirmação, clique em **[!UICONTROL Yes]** para ocultar as propriedades, incluindo a remoção delas de qualquer métrica derivada que contenha as propriedades.

1. (Opcional) [Alterar o nome que aparece nos cabeçalhos de coluna](transaction-property-edit-display-name.md) para qualquer uma das propriedades.

   O nome de exibição padrão para cada propriedade visível é o nome da propriedade conforme é digitado nos dados recuperados.

>[!NOTE]
>
>Se o Adobe Advertising coletar dados para novas propriedades, as novas propriedades — exceto as conversões rastreadas pelo [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] tags de rastreamento de evento universal — são excluídas automaticamente das exibições e relatórios de gerenciamento até que você os inclua. Novas conversões rastreadas por [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] as tags universais de rastreamento de eventos estão sempre disponíveis automaticamente.

>[!MORELIKETHIS]
>
* [Sobre o gerenciamento das propriedades de transação de um anunciante](transaction-property-about.md)
* [Exibir as propriedades de transação rastreadas para um anunciante](transaction-property-view-tracked.md)
* [Alterar o nome de exibição de uma propriedade de transação](transaction-property-edit-display-name.md)
