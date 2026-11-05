---
title: Gerenciar metas de público-alvo para campanhas e grupos de anúncios
description: Saiba como gerenciar metas de público-alvo e seus ajustes de oferta para o Google Ads e o Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%
---
# Gerenciar metas de público-alvo para campanhas e grupos de anúncios

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

[!DNL Google Ads] campanhas e grupos de anúncios, e [!DNL Microsoft Advertising] grupos de anúncios, podem direcionar [públicos-alvo](audience-manage.md) específicos da mesma rede de anúncios. A rede de anúncios determina o tamanho que um público-alvo deve ter para ser direcionado.

Uma meta de público-alvo associa um público-alvo existente a uma campanha ou grupo de anúncios. É possível editar o ajuste de oferta e o status das metas existentes.

>[!NOTE]
>
>[Exclusões de público](audience-exclusions.md) sempre substituem destinos.

## Sobre a exibição [!UICONTROL Targets] {#audience-targets-view-about}

A exibição [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] lista os destinos de público-alvo na exibição filtrada para o anunciante selecionado.

A visualização dos dados requer a permissão [!UICONTROL View Audiences]. Editar, alterar o status e excluir destinos requer a permissão [!UICONTROL Edit Audience Targets].

### Ações disponíveis

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Editar ajustes e status da oferta de público-alvo](#audience-targets-edit)

* [Alterar o status ou excluir alvos de público](#audience-targets-status)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Editar ajustes e status da oferta de público-alvo {#audience-targets-edit}

É possível editar um ou mais direcionamentos de público-alvo por vez. Suas alterações se aplicam a todos os alvos selecionados.

>[!NOTE]
>
>O Search, Social e Commerce otimiza automaticamente o modificador de oferta quando a campanha principal usa a estratégia de oferta CPC e está em um portfólio configurado para otimizar automaticamente os valores de ajuste de oferta para metas de público-alvo. Os modificadores de oferta para [!DNL Microsoft Advertising] públicos alvo de remarketing dinâmico não estão otimizados.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e depois clique na guia **[!UICONTROL Targets]**.

1. Marque a caixa de seleção ao lado de cada target a ser editado.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite o **[!UICONTROL Bid Modifier]** ou o **[!UICONTROL Status]**, ou ambos. Consulte as [configurações de edição](#audience-targets-edit-settings).

   Deixe um campo inalterado para reter o valor existente.

1. (Opcional) Expanda **[!UICONTROL ADDITIONAL DETAILS]** e insira um **[!UICONTROL Project Name]** e **[!UICONTROL Description]**.

1. Clique em **[!UICONTROL Save]**.

Você também pode editar o ajuste de oferta de um único target diretamente na tabela de dados clicando em seu valor na coluna **[!UICONTROL Bid Adjustment]**.

## Alterar o status ou excluir alvos de público {#audience-targets-status}

Você pode pausar um público-alvo ativo para desativar a licitação para esse público-alvo e depois retomar a licitação ativando-o. Também é possível excluir destinos ativos ou pausados.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e depois clique na guia **[!UICONTROL Targets]**.

1. (Opcional) Filtre a lista para incluir públicos-alvo específicos.

1. Marque a caixa de seleção ao lado de cada alvo cujo status você deseja alterar.

1. Na barra de ferramentas de ações em massa, clique em uma das seguintes opções:

   * **[!UICONTROL Activate]** para ativar os destinos selecionados.

   * **[!UICONTROL Pause]** para pausar os destinos selecionados.

   * **[!UICONTROL Delete]** para excluir os destinos selecionados.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Configurações de edição do Audience Target {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** Como alterar o ajuste da oferta de público:

* *[!UICONTROL Set To]:* Substitua o ajuste de oferta existente pela porcentagem especificada.

* *[!UICONTROL Increase]:* Aumente o valor existente de acordo com a porcentagem especificada.

* *[!UICONTROL Decrease]:* Diminua o valor existente de acordo com a porcentagem especificada.

Para [!UICONTROL Increase] e [!UICONTROL Decrease], insira um valor não negativo.

Para um valor definido, 0% não ajusta a oferta. Outros valores compatíveis variam de -90% a 900%. Por exemplo, se a oferta no nível da palavra-chave for 1 USD e o ajuste de oferta do público-alvo for de 50%, a oferta desse público-alvo aumentará para 1,50 USD.

**[!UICONTROL Status]:** Selecione **[!UICONTROL Active]** para habilitar lances ou **[!UICONTROL Paused]** para desabilitar lances para o destino.

>[!MORELIKETHIS]
>
>* [Gerenciar públicos-alvo](audience-manage.md)
>* [Gerenciar exclusões de público alvo para campanhas e grupos de anúncios](audience-exclusions.md)
