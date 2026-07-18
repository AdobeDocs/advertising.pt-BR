---
title: Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica
description: Saiba como criar e gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 82db1b4d0d8703229a4002e932d5b2f52f845814
workflow-type: tm+mt
source-wordcount: 718
ht-degree: 0%

---

# Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica

*[!DNL Google Ads]somente contas*

Você pode criar, editar e alterar o status de destinos de pesquisa dinâmica para [!DNL Google Ads] campanhas que usam a rede de pesquisa.

## O que são destinos de pesquisa dinâmica?

Os destinos de pesquisa dinâmica definem se a rede de anúncios usa todas as páginas do site ou um subconjunto delas para direcionar seus anúncios de pesquisa dinâmica. Configure alvos de pesquisa dinâmica no nível do grupo de publicidade; eles se aplicam a todos os anúncios de pesquisa dinâmica no mesmo grupo de publicidade.

Dependendo das configurações da campanha, os destinos de pesquisa dinâmica podem ser obrigatórios ou opcionais:

* Você deve criar destinos de pesquisa dinâmica quando não especificar um domínio de site e idioma na seção &quot;[!UICONTROL DSA Options]&quot; da campanha.

* Opcionalmente, é possível criar destinos de pesquisa dinâmica ao especificar um domínio de site e idioma na seção &quot;[!UICONTROL DSA Options]&quot; da campanha.

  O [!DNL Google Ads] mostra automaticamente seus anúncios de pesquisa dinâmica com base no conteúdo de um site especificado com essas configurações.

Para melhor rastrear o desempenho, configure sua campanha com um grupo de anúncios por público alvo de pesquisa dinâmica e inclua um grupo de anúncios que segmente todos os critérios.

Para obter mais informações sobre [!DNL Google Ads] anúncios de pesquisa dinâmica, consulte https://support.google.com/google-ads/answer/2471185.

## A visualização [!UICONTROL Auto Targets]

A exibição [!UICONTROL Auto Targets] lista todos os destinos de pesquisa dinâmica na exibição filtrada para a conta de anunciante selecionada.

Você pode criar, editar e alterar o status de destinos de pesquisa dinâmica na exibição [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Auto Targets].

Você também pode [aplicar um rótulo](/help/search-social-commerce/campaign-management/label-classifications/classification-values-assign-campaign-management.md) a qualquer destino.

### Ações disponíveis

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Atribuir restrições a destinos de pesquisa dinâmica](#constraint-assign) e [cancelar atribuição de restrições a destinos de pesquisa dinâmica](#constraint-unassign)

* [Atribuir classificações de rótulo](#classification-values-assign) aos destinos de pesquisa dinâmica e [remover classificações de rótulo](#classification-values-remove) dos destinos de pesquisa dinâmica

>[!NOTE]
>
>Você pode criar e editar grandes quantidades de dados de destino (incluindo rótulos e atribuições de restrições) ao mesmo tempo, carregando [arquivos de bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e postando-os na rede de publicidade.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Atribuir uma restrição aos destinos de pesquisa dinâmica selecionados da nova exibição [!UICONTROL Auto Targets] {#constraint-assign}

1. No menu principal, clique em **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

## Desatribuir restrições dos destinos de pesquisa dinâmica selecionados da nova exibição [!UICONTROL Auto Targets] {#constraint-unassign}

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Atribuir valores de classificação aos destinos de pesquisa dinâmica {#classification-values-assign}

>[!NOTE]
>
>Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

1. No menu principal, clique em **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica ao qual você atribuirá um valor de rótulo.

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

## Remover valores de classificação de etiquetas dos destinos de pesquisa dinâmica{#classification-values-remove}

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

1. No menu principal, clique em **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica do qual você removerá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nova interface do usuário) Gerenciar classificações de rótulos](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
