---
title: Gerenciar grupos de anúncios
description: Saiba como criar e gerenciar grupos de anúncios.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e120af366651028227306e993e73f125f29a431f
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# Gerenciar grupos de anúncios

<!-- Go through all -->

*recurso do Beta*

Um grupo de anúncios inclui um conjunto de anúncios e suas palavras-chave relacionadas. Um grupo de anúncios em uma campanha direcionada à rede de exibição também pode incluir disposições, que são locais na rede de exibição nos quais seus anúncios podem aparecer. As configurações dos grupos de anúncios, que se aplicam a todos os componentes do grupo de anúncios, variam de acordo com a rede de anúncios.

Depois que você [tornar uma conta de rede de publicidade acessível por meio de uma conexão de API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e o Search, Social e Commerce tiver sincronizado os dados da conta com a rede de publicidade, você poderá criar grupos de publicidade para um [tipo de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md). Você também pode editar e alterar o status de grupos de anúncios.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Sobre a exibição [!UICONTROL Ad Groups] {#ad-group-view-about}

A exibição [!UICONTROL Manage] > [!UICONTROL Ad Groups] lista todos os grupos de anúncios na exibição filtrada para a conta de anunciante selecionada.

### Ações disponíveis

* [Criar um grupo de publicidade](#ad-group-create)

* [Renomear um grupo de anúncios dentro da linha](#ad-group-rename)

* [Editar configurações do grupo de publicidade](#ad-group-edit)

* [Alterar o status ou excluir um grupo de anúncios dentro da linha](#ad-group-status)

* [Exibir um gráfico de desempenho na exibição [!UICONTROL Ad Groups]](#ad-group-performance-graph)

* [Atribuir restrições de lance a grupos de anúncios e desatribuir restrições de grupos de anúncios](#ad-group-constraints)

* [Atribua classificações de etiquetas a grupos de anúncios e remova classificações de etiquetas de grupos de anúncios](#ad-group-classifications)

* [Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Ad Groups]](#ad-group-reports)

## Criar um grupo de publicidade {#ad-group-create}

>[!TIP]
>
>Para criar um grande número de grupos de anúncios ao mesmo tempo, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Clique em **[!UICONTROL Create Ad Group]**.

1. Especifique as configurações dos grupos de anúncios do [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md).

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") e altere as configurações do grupo de anúncios.

1. Clique em **[!UICONTROL Create]**.

Posteriormente, é possível substituir os lances de nível de grupo de anúncios definindo lances para palavras-chave individuais ou posicionamentos no grupo de anúncios.

## Renomear um grupo de anúncios {#ad-group-rename}

Renomeie rapidamente um grupo de anúncios sem abrir as configurações completas do grupo de anúncios.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Mantenha o cursor sobre a linha do grupo de anúncios e clique em **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite o nome e clique em **[!UICONTROL Apply]**.

## Editar configurações do grupo de publicidade {#ad-group-edit}

É possível editar configurações para grupos de anúncios individuais. Você também pode editar alguns campos para vários grupos de anúncios ao mesmo tempo, incluindo alguns detalhes do grupo de anúncios, opções de orçamento e opções de URL que são comuns a todos os grupos de anúncios selecionados.

>[!TIP]
>
>Também é possível editar dados em massa usando o <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre o nome da entidade e clique em **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Marque a caixa de seleção ao lado do grupo de anúncios. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite as configurações do grupo de anúncios do [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md).

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") e altere as configurações do grupo de anúncios.

1. Clique em **[!UICONTROL Update]**.

## Alterar o status de um grupo de publicidade {#ad-group-status}

Altere rapidamente o status de um grupo de publicidade sem abrir as configurações completas do grupo de publicidade.

Você pode pausar qualquer grupo de anúncios ativo em uma rede de anúncios compatível para desativar a licitação. Posteriormente, é possível retomar o lance alterando o status para ativo.

Você também pode excluir qualquer grupo de anúncios ativo ou pausado. Os grupos de anúncios excluídos são excluídos da rede de anúncios. Elas ainda estarão visíveis ao serem incluídas no filtro de dados, mas não poderão ser alteradas.

### Ativar ou pausar um grupo de anúncios

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Mantenha o cursor sobre a linha do grupo de anúncios e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da coluna [!UICONTROL Status].

1. Alterar o status:

   * Para ativar um grupo de anúncios pausados, selecione **[!UICONTROL Active]**.

   * Para pausar um grupo de anúncios ativo, selecione **[!UICONTROL Paused]**.

### Excluir um grupo de publicidade

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha do grupo de anúncios e clique em **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Mantenha o cursor sobre a linha do grupo de anúncios e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da coluna [!UICONTROL Status]. Selecione **[!UICONTROL Deleted]**.

## Gerenciar atribuições de restrição de lance para grupos de anúncios {#ad-group-constraints}

Cada entidade pode ter apenas uma restrição. As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Desatribuir uma restrição não exclui a restrição nem os próprios componentes da conta.

### Atribuir uma restrição de lance aos grupos de anúncios selecionados da nova visualização [!UICONTROL Ad Groups]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

### Atribuir uma restrição de lance às unidades de oferta de pesquisa selecionadas das [!UICONTROL Campaigns] exibições herdadas

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de componente de conta.

1. Marque a caixa de seleção ao lado de cada linha relevante.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL More]** e em **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição aplicável.

1. (Opcional) Insira detalhes adicionais:

   1. Ao lado de [!UICONTROL Additional Details], clique em **[!UICONTROL Open]** para expandir os detalhes.

   1. Digite um **[!UICONTROL Project Name]** opcional e/ou **[!UICONTROL Description]** opcional.

1. Clique em **[!UICONTROL Save]**.

### Remover restrições de licitação dos grupos de anúncios selecionados da nova visualização [!UICONTROL Ad Groups]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

### Remover restrições de licitação das unidades de oferta de pesquisa das [!UICONTROL Campaigns] exibições herdadas

>[!NOTE]
>
>Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;Excluir restrições para unidades de oferta de pesquisa&quot; no capítulo do Guia de Otimização em &quot;Restrições de oferta&quot;, que está disponível no Search, Social e Commerce.

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de componente de conta.

1. Marque a caixa de seleção ao lado de cada componente do qual deseja remover a restrição.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL More]** e em **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. No diálogo de confirmação, selecione **[!UICONTROL Yes, Unassign]**.

## Atribuir classificações de etiquetas a grupos de anúncios {#ad-group-classifications}

>[!NOTE]
>
>Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

### Atribuir valores de classificação a grupos de anúncios

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade ao qual você atribuirá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Para cada valor de classificação aplicável, faça o seguinte:

   1. Na coluna **[!UICONTROL Classifications]**, especifique a classificação:

      * Para usar uma classificação existente, clique no nome da classificação para expandi-la.

      * Para criar uma classificação, clique em [!UICONTROL +] no cabeçalho da coluna. No campo de entrada, insira o nome da classificação e clique em ![Salvar](/help/search-social-commerce/assets/save-checkmark.png "Salvar") para salvar imediatamente a classificação. Para usar a nova classificação, clique no nome da classificação para expandi-la.

        O nome deve consistir em [caracteres ASCII 32-126](https://www.asciitable.com/), e o comprimento máximo é de 27 caracteres de byte único.

   1. Na coluna **[!UICONTROL Value Name]**, especifique o valor da classificação selecionada:

      * Para usar um valor existente, selecione o valor.

      * Para criar um valor, clique em [!UICONTROL +] no cabeçalho da coluna. No campo de entrada, insira o valor e clique em ![Salvar](/help/search-social-commerce/assets/save-checkmark.png "Salvar") para salvar imediatamente o valor e selecioná-lo por padrão.

        O comprimento máximo é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

1. Clique em **+[!UICONTROL Assign Now]**.

### Remover os valores de classificação de etiquetas dos grupos de anúncios

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Marque a caixa de seleção ao lado de cada grupo de publicidade do qual você removerá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## Exibir um gráfico de desempenho na exibição [!UICONTROL Ad Groups] {#ad-group-performance-graph}

Abra e configure um gráfico de desempenho com até três métricas totalizadas em todos os grupos de anúncios na exibição para o intervalo de datas especificado.

### Exibir um gráfico de desempenho

1. Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Especifique a moeda e até três métricas para incluir no gráfico.

### Ocultar um gráfico de desempenho visível

* Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Ad Groups] {#ad-group-reports}

Gere um relatório que inclua as linhas de dados de um ou mais grupos de anúncios na exibição [!UICONTROL Ad Groups] e baixe o relatório como um arquivo de planilha do Microsoft Excel (formato XLXS). O relatório inclui todas as colunas visíveis na visualização.

É possível excluir qualquer relatório gerado.

Consulte também &quot;>* [(Interface herdada) Baixar dados de uma exibição de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interface herdada) Excluir um relatório de dados de desempenho ou arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Gerar um relatório com as linhas de dados filtradas

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Especifique os grupos de anúncios cujos dados você deseja baixar:

   * Para baixar dados de grupos de anúncios específicos, marque as caixas de seleção ao lado dos grupos de anúncios.

   * Para baixar dados para todos os grupos de anúncios, não é necessário marcar nenhuma caixa de seleção. Todos os grupos de anúncios são incluídos por padrão.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Nas configurações de [!UICONTROL Grid Reports], insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o arquivo é nomeado como &quot;ad group_YYYMMDD_NNNN&quot;, onde &quot;NNNN&quot; é o número sequencial do trabalho (como &quot;ad group_20250402_1326).

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

>[!MORELIKETHIS]
>
>* [Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gerenciar atribuições de restrição para campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para palavras-chave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para posicionamentos](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(Interface herdada) Baixar dados de uma exibição de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Interface herdada) Excluir um relatório de dados de desempenho ou um arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)
>* [[!DNL LY Ads] configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)
