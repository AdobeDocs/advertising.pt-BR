---
title: Gerenciar atribuições de restrição para grupos de anúncios
description: Saiba como atribuir restrições a grupos de anúncios.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: c9960b5a-4b6c-4ef0-8501-5478af2c40da
TQID: https://experienceleague.adobe.com/6z4-Pt25RaQpLiEYdnp-BXD0guz9S2zQLmamf8uSSXU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 0%

---

# (Nova interface) Gerenciar atribuições de restrições para grupos de anúncios

*recurso do Beta*

Você pode atribuir e remover restrições de licitação das seguintes entidades de pesquisa: campanha, grupo de anúncios, palavra-chave, disposição, grupo de produtos no nível da unidade e público-alvo da pesquisa dinâmica. Cada entidade pode ter apenas uma restrição.

As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Desatribuir uma restrição não exclui a restrição nem os próprios componentes da conta.

## Atribuir uma restrição aos grupos de anúncios selecionados da nova exibição [!UICONTROL Ad Groups]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

## Atribuir uma restrição às unidades de oferta de pesquisa selecionadas das [!UICONTROL Campaigns] exibições herdadas

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de componente de conta.

1. Marque a caixa de seleção ao lado de cada linha relevante.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL More]** e em **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição aplicável.

1. (Opcional) Insira detalhes adicionais:

   1. Ao lado de [!UICONTROL Additional Details], clique em **[!UICONTROL Open]** para expandir os detalhes.

   1. Digite um **[!UICONTROL Project Name]** opcional e/ou **[!UICONTROL Description]** opcional.

1. Clique em **[!UICONTROL Save]**.

## Remover restrições dos grupos de anúncios selecionados da nova visualização [!UICONTROL Ad Groups]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Cancelar atribuição de restrições das unidades de oferta de pesquisa das [!UICONTROL Campaigns] exibições herdadas

>[!NOTE]
>
>Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;Excluir restrições para unidades de oferta de pesquisa&quot; no capítulo do Guia de Otimização em &quot;Restrições de Oferta&quot;, que está disponível no Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de componente de conta.

1. Marque a caixa de seleção ao lado de cada componente do qual deseja remover a restrição.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL More]** e em **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. No diálogo de confirmação, selecione **[!UICONTROL Yes, Unassign]**.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nova interface do usuário) Gerenciar atribuições de restrição para campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [(Nova interface do usuário) Gerenciar atribuições de restrição para palavras-chave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [(Nova interface do usuário) Gerenciar atribuições de restrição para posicionamentos](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
