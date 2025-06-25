---
title: Gerenciar [!DNL Microsoft Advertising] públicos de remarketing dinâmicos
description: Saiba como criar e gerenciar [!DNL Microsoft Advertising] públicos de remarketing dinâmicos.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Gerenciar públicos de remarketing dinâmicos do [!DNL Microsoft Advertising]

*[!DNL Microsoft Advertising]somente contas*

Você pode criar um público de remarketing dinâmico do [!DNL Microsoft Advertising] ao usar a tag de rastreamento de conversão e público-alvo do JavaScript do mecanismo de pesquisa nas suas páginas da Web. Cada público é criado usando uma tag específica incluída nas páginas da Web cujos usuários compõem o público. Você pode criar vários públicos-alvo com a mesma tag de rastreamento. Você também pode alterar o nome e a fonte de dados de públicos existentes ou excluir públicos existentes.

Os públicos de remarketing dinâmicos têm o tipo de público &quot;[!UICONTROL Dynamic Remarketing] \&lt;Visitor Type\>&quot; (como &quot;Compradores antigos de remarketing dinâmico&quot;).

Para obter mais informações sobre remarketing dinâmico e como implementar a marca JavaScript necessária, consulte a [[!DNL Microsoft Advertising] documentação sobre remarketing dinâmico](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Criar um público de remarketing dinâmico

>[!NOTE]
>
>Para contas do [!DNL Microsoft Advertising], a marca JavaScript deve incluir a [ID do produto e os parâmetros de tipo de página](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifique o nome da tag UET [!DNL Microsoft Advertising] incluída nas páginas da Web a partir das quais o público-alvo será criado.

   Você precisará do nome da tag em uma etapa posterior.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Especifique as informações do público:

   1. No menu **[!UICONTROL Data Source]**, selecione **[!UICONTROL Dynamic Remarketing List]**.

   1. Insira o **[!UICONTROL Audience Name]**.

   1. Em uma lista de todas as tags disponíveis para a conta do mecanismo de pesquisa, selecione o nome da tag UET [!DNL Microsoft Advertising] incluída nas páginas da Web cujos usuários compõem o público.

   1. Selecione o tipo de visitante para o público, que é baseado nas ações do visitante nas páginas da Web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Especifique o número de **[!UICONTROL Membership Days]**, que é o número de dias que um cookie do usuário permanece no público-alvo. Os valores podem variar de 1 (um) a 180.

      Use o período de tempo durante o qual você espera que seu anúncio seja relevante para o usuário.

1. Clique em **[!UICONTROL Post]**.

>[!NOTE]
>
>Suas listas de remarketing dinâmicas do [!DNL Microsoft Advertising] estarão qualificadas para direcionamento uma vez que incluírem pelo menos 300 usuários.

## Editar um público de remarketing dinâmico

Você pode alterar o nome e a fonte de dados de um público de remarketing dinâmico [!DNL Microsoft Advertising]. Você não pode editar o valor da configuração [!UICONTROL Membership Days].

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Marque a caixa de seleção ao lado do público-alvo para editar.

1. Na barra de ferramentas acima da tabela, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite as informações do público:

   1. Na seção **[!UICONTROL Data Source]**, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

   1. (Opcional) Altere o **[!UICONTROL Audience Name]**.

   1. (Opcional) Em uma lista de todas as tags disponíveis para a conta de rede de publicidade, altere o nome da tag UET [!DNL Microsoft Advertising] incluída nas páginas da Web cujos usuários compõem o público.

   1. (Opcional) Altere o tipo de visitante do público, que se baseia nas ações do visitante nas páginas da Web relevantes: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Clique em **[!UICONTROL Post]**.

## Excluir um público de remarketing dinâmico

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Opcional) Filtre a lista para incluir públicos-alvo específicos.

1. Marque a caixa de seleção ao lado de cada público-alvo a ser excluído.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](audience-about.md)
>* [Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](google-audience-from-adobe-audience.md)
>* [Criar um [!DNL Google Ads] público-alvo de correspondência do cliente a partir de uma lista de emails do Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
