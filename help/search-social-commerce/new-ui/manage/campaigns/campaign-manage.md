---
title: Gerenciar campanhas
description: Saiba como criar e gerenciar campanhas de publicidade.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6b67f3e2759ddd80300c86df610b36684b7a07e2
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# Gerenciar campanhas

*recurso do Beta*

Uma campanha é o componente principal de uma conta de rede de anúncios. Para a maioria dos tipos de campanha, ele consiste em um conjunto de grupos de anúncios ou conjuntos de anúncios. As configurações da campanha incluem parâmetros de orçamento da campanha, metas de anúncios e parâmetros de rastreamento opcionais para todos os anúncios na campanha. Os parâmetros de rastreamento no nível da campanha substituem os parâmetros no nível da conta, mas podem ser substituídos em um nível inferior.

Depois que você [tornar uma conta de rede de publicidade acessível por meio de uma conexão de API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e o Search, Social e Commerce tiver sincronizado os dados da conta com a rede de publicidade, você poderá criar novas campanhas com [tipos de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md). Você também pode editar e alterar o status de campanhas.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Sobre a exibição [!UICONTROL Campaigns] {#campaign-view-about}

A exibição [!UICONTROL Manage] > [!UICONTROL Campaigns] lista todas as campanhas na exibição filtrada para a conta de anunciante selecionada. Você pode abrir uma lista de grupos de anúncios na campanha clicando no nome dela.

À medida que você adiciona e edita dados de campanha nas [!UICONTROL Campaigns] exibições, o Search, Social e Commerce envia imediatamente as alterações de dados para a rede de publicidade. Search, Social e Commerce também extrai dados de estrutura de campanha e dados de cliques diariamente ou com mais frequência quando novas campanhas são detectadas. Para todas as redes de anúncios sincronizadas, você também pode sincronizar contas sob demanda, conforme necessário.

O Search, Social e Commerce extrai dados de desempenho de hora em hora nas contas [!DNL Google Ads] e [!DNL Microsoft Advertising] sincronizadas e diariamente para outras contas de rede de anúncios sincronizadas.

### Ações disponíveis

* [Criar uma campanha](#campaign-create)

* [Renomear uma campanha dentro da linha](#campaign-rename)

* [Editar configurações da campanha](#campaign-edit)

* [Alterar o status ou excluir uma campanha dentro da linha](#campaign-status)

* [Atribuir campanhas a um portfólio e remover campanhas de um portfólio](#campaign-portfolio)

* [Exibir um gráfico de desempenho na exibição [!UICONTROL Campaigns]](#campaign-performance-graph)

* [Atribuir restrições de lance a campanhas e cancelar a atribuição de restrições a campanhas](#campaign-constraints)

* [Atribuir restrições do target às campanhas e cancelar a atribuição de restrições do target às campanhas](#campaign-target-constraints)

* [Atribuir classificações de rótulo a campanhas e remover classificações de rótulo de campanhas](#campaign-classifications)

* [Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Campaigns]](#campaign-reports)

## Criar uma campanha {#campaign-create}

>[!NOTE]
>
>* Antes de criar uma campanha, [implemente as tags de rastreamento de conversão](/help/search-social-commerce/tracking/conversion-tracking-about.md) nas páginas da Web do anunciante.
>* Para criar um grande número de campanhas ao mesmo tempo, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Clique em **[!UICONTROL Create Campaign]**.

1. Especifique as configurações de campanha do [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md).

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") e altere as configurações da campanha.

1. Clique em **[!UICONTROL Create]**.

Dependendo da rede de publicidade na qual a campanha foi criada, talvez seja necessário criar grupos de publicidade e anúncios associados antes que a campanha seja enviada para a rede de publicidade.

## Renomear uma campanha {#campaign-rename}

Renomear rapidamente uma campanha sem abrir as configurações completas.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Mantenha o cursor sobre a linha da campanha e clique em **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite o nome e clique em **[!UICONTROL Apply]**.

## Editar configurações da campanha {#campaign-edit}

Você pode editar configurações para campanhas individuais. Você também pode editar alguns campos para várias campanhas ao mesmo tempo, incluindo alguns detalhes da campanha, opções de orçamento e opções de URL que são comuns a todas as campanhas selecionadas.

>[!TIP]
>
>Também é possível editar dados em massa usando o <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre o nome da entidade e clique em **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Marque a caixa de seleção ao lado da campanha. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite o [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md) configurações de campanha.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") e altere as configurações da campanha.

1. Clique em **[!UICONTROL Update]**.

Dependendo da rede de anúncios na qual a campanha foi criada, talvez seja necessário incluir grupos de anúncios e anúncios antes de enviá-los para a rede de anúncios.

## Alterar o status de uma campanha {#campaign-status}

Alterar rapidamente o status de uma campanha sem abrir as configurações completas da campanha.

Você pode pausar qualquer campanha ativa em uma rede de anúncios compatível para desativar a licitação nela. Posteriormente, é possível retomar o lance alterando o status para ativo.

Também é possível excluir qualquer campanha ativa ou pausada. As campanhas excluídas são excluídas da rede de anúncios. Elas ainda estarão visíveis ao serem incluídas no filtro de dados, mas não poderão ser alteradas.

### Ativar ou pausar uma campanha

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Mantenha o cursor sobre a linha da campanha e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da coluna [!UICONTROL Status].

1. Alterar o status:

   * Para ativar uma campanha pausada, selecione **[!UICONTROL Active]**.

   * Para pausar uma campanha ativa, selecione **[!UICONTROL Paused]**.

### Excluir uma campanha

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha da campanha e clique em **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Mantenha o cursor sobre a linha da campanha e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado da coluna [!UICONTROL Status]. Selecione **[!UICONTROL Deleted]**.

## Atribuir campanhas a um portfólio {#campaign-portfolio}

Atribuir uma campanha a um portfólio otimizado permite que o Search, Social e Commerce otimize ofertas, orçamentos de campanha e metas de estratégia de ofertas para palavras-chave e anúncios na campanha. Você pode atribuir campanhas a um portfólio na exibição [!UICONTROL Campaigns], ao criar o portfólio ou editando as configurações de um portfólio.

Nem todos os tipos de campanha e redes de anúncios estão qualificados para otimização. Consulte uma lista de [tipos de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md) que você pode incluir em um portfólio. Além disso, verifique o [suporte à otimização para cada estratégia de oferta de campanha](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Cada campanha pode ser atribuída a apenas um portfólio. Se você atribuir uma campanha que já está associada a outro portfólio para um novo portfólio, ela será removida do portfólio original.

### Atribuir campanhas a um portfólio existente a partir da exibição [!UICONTROL Campaigns]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha para atribuir a um único portfólio.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]**.

1. Selecione o portfólio.

1. Clique em **[!UICONTROL Assign Now]**.

### Atribuir campanhas a um novo portfólio a partir da exibição [!UICONTROL Campaigns]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha para a qual deseja criar o novo portfólio.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. Na tela [!UICONTROL Create Portfolio], especifique as configurações do portfólio.

   As campanhas selecionadas anteriormente já estão atribuídas à campanha. Opcionalmente, é possível editar a lista de campanhas do portfólio.

   Para obter mais informações sobre as configurações do portfólio, consulte o Guia de otimização, disponível no Search, Social e Commerce.

1. Clique em **[!UICONTROL Review and Save]**.

### Alterar atribuições de campanha para um portfólio da exibição [!UICONTROL Portfolios]

Quando você remove uma campanha de um portfólio, o Search, o Social e o Commerce não podem otimizar ofertas, orçamentos de campanha e metas de estratégia de oferta para essa campanha.

A ação é registrada no histórico de alterações do portfólio.

Para obter mais informações sobre otimização, consulte o Guia de otimização, que está disponível no Search, Social e Commerce.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Marque a caixa de seleção ao lado do portfólio.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Nas configurações do portfólio, vá para a seção [!UICONTROL Assign Campaigns] e altere as atribuições da campanha.

   Para obter mais informações sobre as configurações do portfólio, consulte o Guia de otimização, disponível no Search, Social e Commerce.

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as configurações e faça as alterações necessárias, e clique em **[!UICONTROL Save]**.

## Gerenciar atribuições de restrição de lance para campanhas {#campaign-constraints}

Cada entidade pode ter apenas uma restrição. As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Desatribuir uma restrição não exclui a restrição nem os próprios componentes da conta.

>[!NOTE]
>
>As restrições ativas restringem os lances somente para unidades de lance atribuídas em portfólios de nível de palavra-chave herdada otimizados. Elas são ignoradas para unidades de oferta que estão em portfólios ativos, estão em portfólios híbridos ou não estão em portfólios.

### Atribuir uma restrição de lance às campanhas selecionadas da nova visualização [!UICONTROL Campaigns]

Você pode atribuir uma única restrição a uma ou mais campanhas.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha à qual você atribuirá uma única restrição.

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

### Remover restrições de lance de campanhas selecionadas da nova visualização [!UICONTROL Campaigns]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha da qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

### Remover restrições de licitação das unidades de oferta de pesquisa das [!UICONTROL Campaigns] exibições herdadas

>[!NOTE]
>
>Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;Excluir restrições para unidades de oferta de pesquisa&quot; no capítulo do Guia de Otimização em &quot;Restrições de Oferta&quot;, que está disponível no Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. Em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selecione a exibição de componente de conta.

1. Marque a caixa de seleção ao lado de cada componente do qual deseja remover a restrição.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL More]** e em **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. No diálogo de confirmação, selecione **[!UICONTROL Yes, Unassign]**.

## Gerenciar atribuições de restrição do target para campanhas {#campaign-target-constraints}

### Atribuir uma restrição de direcionamento às campanhas selecionadas da nova visualização [!UICONTROL Campaigns]

Você pode atribuir uma única restrição de target a uma ou mais campanhas.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha à qual você atribuirá uma única restrição de target.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

### Remover restrições de destino de campanhas selecionadas da nova visualização [!UICONTROL Campaigns]

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha da qual você cancelará a atribuição de uma restrição de público alvo.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Atribuir classificações de etiquetas a campanhas {#campaign-classifications}

>[!NOTE]
>
>Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

### Atribuir valores de classificação a campanhas

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha à qual você atribuirá um valor de rótulo.

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

### Remover valores de classificação de etiquetas das campanhas

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Marque a caixa de seleção ao lado de cada campanha da qual você removerá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## Exibir um gráfico de desempenho na exibição [!UICONTROL Campaigns] {#campaign-performance-graph}

Abra e configure um gráfico de desempenho com até três métricas totalizadas em todas as campanhas na exibição para o intervalo de datas especificado.

### Exibir um gráfico de desempenho

1. Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Especifique a moeda e até três métricas para incluir no gráfico.

### Ocultar um gráfico de desempenho visível

* Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Campaigns] {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Gere um relatório que inclua as linhas de dados de uma ou mais campanhas na exibição [!UICONTROL Campaigns] e baixe o relatório como um arquivo de planilha do Microsoft Excel (formato XLXS). O relatório inclui todas as colunas visíveis na visualização.

É possível excluir qualquer relatório gerado.

Consulte também &quot;>* [(Interface herdada) Baixar dados de uma exibição de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interface herdada) Excluir um relatório de dados de desempenho ou arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Gerar um relatório com as linhas de dados filtradas

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Especifique as campanhas cujos dados você deseja baixar:

   * Para baixar dados de campanhas específicas, marque as caixas de seleção ao lado das campanhas.

   * Para baixar dados para todas as campanhas, não é necessário marcar nenhuma caixa de seleção. Todas as campanhas são incluídas por padrão.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Nas configurações de [!UICONTROL Grid Reports], insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o arquivo é nomeado como &quot;campaign_YYYYMMDD_NNNN&quot;, onde &quot;NNNN&quot; é o número sequencial do trabalho (como &quot;campaign_20250402_1326).

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

>[!MORELIKETHIS]
>
>* [Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gerenciar atribuições de restrição para grupos de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para palavras-chave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para posicionamentos](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(Interface herdada) Baixar dados de uma exibição de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Interface herdada) Excluir um relatório de dados de desempenho ou um arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

