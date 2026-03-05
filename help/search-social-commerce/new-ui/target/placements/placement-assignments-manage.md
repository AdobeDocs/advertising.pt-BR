---
title: Gerenciar atribuições de restrição para disposições
description: Saiba como atribuir restrições a inserções.
feature: Search Optimization, Search Campaign Management
hide: true
source-git-commit: 0e863a638d8f3d055fd566db65d7967126fd5f89
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# (Nova interface de usuário) Gerenciar atribuições de restrições para disposições

*recurso do Beta*

Você pode atribuir e remover restrições de licitação das seguintes entidades de pesquisa: campanha, grupo de anúncios, palavra-chave, disposição, grupo de produtos no nível da unidade e público-alvo da pesquisa dinâmica. Cada entidade pode ter apenas uma restrição.

As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Desatribuir uma restrição não exclui a restrição nem os próprios componentes da conta.

>[!NOTE]
>
>* Posteriormente, se você editar uma palavra-chave ou a cópia de um anúncio — criando assim uma nova palavra-chave ou anúncio — a restrição não será atribuída à nova entidade.
>* As restrições ativas restringem os lances somente para unidades de lance atribuídas em portfólios de nível de palavra-chave herdada otimizados. Elas são ignoradas para unidades de oferta que estão em portfólios ativos, estão em portfólios híbridos ou não estão em portfólios.

## Atribuir uma restrição aos posicionamentos selecionados da nova exibição [!UICONTROL Placements]

Você pode atribuir uma única restrição a uma ou mais disposições.

1. No menu principal, clique em **[!UICONTROL Target]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, marque a caixa de seleção ao lado de cada posicionamento ao qual você atribuirá uma única restrição.

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

## Desatribuir restrições de posicionamentos selecionados da nova visualização [!UICONTROL Placements]

1. No menu principal, clique em **[!UICONTROL Target]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, marque a caixa de seleção ao lado de cada posicionamento do qual você cancelará a atribuição de restrições.

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
>* [Gerenciar atribuições de restrição para campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para grupos de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para anúncios](/help/search-social-commerce/new-ui/manage/ads/ad-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para palavras-chave](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
