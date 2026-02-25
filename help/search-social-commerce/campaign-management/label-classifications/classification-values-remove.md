---
title: Remover dos componentes da conta os valores de classificação de etiquetas
description: Saiba como remover associações entre valores de classificação de etiquetas e componentes de conta.
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Remover dos componentes da conta os valores de classificação de etiquetas

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

>[!NOTE]
>
>Para excluir um valor de uma classificação de etiqueta, consulte &quot;[Excluir valores de classificação de etiquetas](classification-values-delete.md)&quot;.

## (Nova interface do usuário) Remoção dos valores de classificação de etiquetas dos componentes da conta

É possível remover valores de classificação de qualquer componente de conta aplicável que esteja disponível na nova interface.

1. Abra a exibição de entidade no menu **[!UICONTROL Manage]** ou **[!UICONTROL Target]**.

1. Marque a caixa de seleção ao lado de cada linha relevante.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## (Interface herdada) Remover valores de classificação de etiquetas dos componentes da conta

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de entidade.

1. Siga um destes procedimentos:

   * (Para remover valores de uma única entidade) Mantenha o cursor sobre o nome da entidade, clique em ![Botão Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Botão Menu") e selecione **[!UICONTROL Classification]**.

   * (Para remover valores de uma ou mais entidades) Faça o seguinte:

      * Marque a caixa de seleção ao lado de cada linha.

        Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * Na barra de ferramentas acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e em **[!UICONTROL Classification]**.

1. Em [!UICONTROL Assignment Details], selecione **[!UICONTROL Remove]**.

1. Para cada valor de classificação a ser removido, faça o seguinte:

   * Na coluna **[!UICONTROL Classification]**, clique no nome da classificação para expandi-la.

   * Na coluna **[!UICONTROL Value Name]**, clique no nome do valor para selecioná-lo.

1. (Opcional) Insira detalhes adicionais:

   * Ao lado de **[!UICONTROL Additional Details]**, clique em ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para expandir os detalhes.

   * Digite um **[!UICONTROL Project Name]** opcional e/ou **[!UICONTROL Description]** opcional.

   * Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre as classificações de rótulo](classification-about.md)
>* [Criar uma classificação de etiqueta](classification-create.md)
>* [Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha](classification-values-assign-campaign-management.md)
>* [Atribuir valores de classificação aos componentes da conta usando bulksheets](classification-values-assign-bulksheets.md)
>* [Excluir valores de classificação de etiquetas](classification-values-delete.md)
>* [Excluir classificações de etiquetas](classification-delete.md)
