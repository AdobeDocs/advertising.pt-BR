---
title: Gerenciar grupos de produtos de compras
description: Saiba como criar e gerenciar grupos de produtos de compras em campanhas de compras.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Gerenciar grupos de produtos de compras

*[!DNL Google Ads]e [!DNL Microsoft Advertising] campanhas de compras somente*

Você pode criar e editar grupos de produtos, além de excluir grupos de produtos e seus grupos de produtos filhos, na [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] exibição.

## Criar um &quot;[!UICONTROL All Products]&quot; grupo de produtos

Antes de criar grupos de produtos com atributos específicos, primeiro você deve criar um grupo de produtos com tudo incluído chamado &quot;[!UICONTROL All Products].&quot; Cada grupo de publicidade pode ter apenas um &quot;[!UICONTROL All Products]&quot;grupo.

>[!TIP]
>
>Para criar muitos componentes da conta de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade, a conta, a campanha e o grupo de publicidade e clique em **[!UICONTROL Continue]**.

1. Especifique a [[!DNL Google Ads] configurações do grupo de produtos](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] configurações do grupo de produtos](product-group-settings-microsoft.md).

1. Clique em **[!UICONTROL Post]**.

## Criar um nó filho de grupo de produtos em um grupo de produtos existente

Depois de criar pelo menos uma &quot;[!UICONTROL All Products]&quot;para um grupo de anúncios, você pode criar nós filhos de grupos de produtos para subconjuntos de produtos a serem incluídos ou excluídos de ofertas, com um ou mais grupos de produtos direcionados ao mesmo atributo em cada nível (por exemplo, [!UICONTROL Brand]=Acme para um grupo de produtos e [!UICONTROL Brand]=AcmePlus para outro no mesmo nível. Você pode criar até sete níveis de nós de grupos de produtos secundários, sem incluir &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Você não pode criar um grupo de produtos filho para um &quot;[!UICONTROL Everything Else]&quot; grupo de produtos.

>[!TIP]
>
>Para criar muitos componentes da conta de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para exibir um grupo de produtos e seus nós filhos do grupo de produtos na Exibição de árvore, mantenha o cursor sobre o nome do grupo de produtos, clique em ![Ícone do menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Ícone do menu")e selecione **[!UICONTROL Tree View]**.

1. Mantenha o cursor sobre o nome do grupo de produtos, clique em ![Menu Suspenso de Setas](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu Suspenso de Setas")e selecione **[!UICONTROL + Add Node]**.

1. Especifique a [[!DNL Google Ads] configurações do grupo de produtos](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] configurações do grupo de produtos](product-group-settings-microsoft.md), incluindo a dimensão do produto e o atributo.

1. Clique em **[!UICONTROL Post]**.

## Editar configurações do nó do grupo de produtos

É possível editar o modelo de oferta e rastreamento para nós de grupo de produtos de unidade (grupos de produtos sem nós de grupo de produtos filho) incluídos em um grupo de publicidade. Você não pode editar nenhuma informação para grupos de produtos de unidade excluídos ou para nós de subdivisão incluídos ou excluídos, que são grupos de produtos com nós de grupo de produtos secundários.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Para exibir um grupo de produtos e seus nós filhos do grupo de produtos na Exibição de árvore, mantenha o cursor sobre o nome do grupo de produtos, clique em ![Ícone do menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Ícone do menu")e selecione **[!UICONTROL Tree View]**.

1. Siga um destes procedimentos:

   1. (Para editar configurações para um único nó de grupo de produtos) Mantenha o cursor sobre o nome do grupo de produtos, clique em ![Ícone do menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Ícone do menu")e selecione **[!UICONTROL + Edit Node]**.

   1. (Para editar configurações para um ou mais grupos de anúncios) Faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada nó.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite o [[!DNL Google Ads] configurações do grupo de produtos](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] configurações do grupo de produtos](product-group-settings-microsoft.md).

   Para vários nós, as alterações são aplicadas a todos os nós selecionados. Para o [!UICONTROL Bid] você tem opções para alterar valores existentes para um valor especificado ou para aumentar ou diminuir o valor em uma porcentagem especificada ou valor monetário, com um limite. Para o [!UICONTROL Tracking Template] , é possível alterar valores existentes para um valor especificado, substituir uma string existente por uma string especificada, adicionar um prefixo especificado ao início de cada valor ou anexar um sufixo ao final de cada valor.

1. (Opcional) Clique em **[!UICONTROL Additional Details]** e, opcionalmente, informe um nome de projeto e uma descrição.

1. Clique em **[!UICONTROL Post]**.

## Excluir nós do grupo de produtos

Você pode excluir qualquer grupo de produtos, exceto um grupo &quot;Tudo mais&quot; quando outros grupos de produtos existem no mesmo nível, usado para determinar quais produtos na conta da central de atendimento são incluídos nos anúncios de compras do grupo de anúncios. A exclusão de um grupo de produtos exclui todos os grupos de produtos secundários.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Opcional) Filtre a lista para incluir grupos de produtos específicos.

1. Siga um destes procedimentos:

   * Para excluir um grupo de produtos, clique no link **[!UICONTROL Status]** e selecione **[!UICONTROL Delete]**.

   * Para excluir um ou mais grupos de produtos, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada grupo de produtos que deseja excluir.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Na barra de ferramentas, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e selecione **[!UICONTROL Delete]**.

      1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre grupos de produtos de compras](product-group-about.md)
>* [[!DNL Google Ads] configurações do grupo de produtos](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] configurações do grupo de produtos](product-group-settings-microsoft.md)

