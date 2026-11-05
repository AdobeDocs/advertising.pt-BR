---
title: Gerenciar exclusões de público alvo para campanhas e grupos de anúncios
description: Saiba mais sobre as exclusões de público do Google Ads e do Microsoft Advertising, incluindo como excluir exclusões de Google Ads.
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
source-wordcount: '269'
ht-degree: 0%
---
# Gerenciar exclusões de público alvo para campanhas e grupos de anúncios

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

Uma exclusão de público-alvo impede que os anúncios em uma campanha ou grupo de anúncios sejam exibidos aos usuários em um [público-alvo](audience-manage.md) específico.

Para contas do [!DNL Google Ads], você pode excluir qualquer tipo de público-alvo. Para contas do [!DNL Microsoft Advertising], você pode excluir somente públicos de remarketing dinâmicos.

>[!NOTE]
>
>As exclusões sempre substituem [públicos-alvo](audience-targets-manage.md).

## Sobre a exibição [!UICONTROL Exclusions] {#audience-exclusions-view-about}

A exibição [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] lista as exclusões de público-alvo na exibição filtrada para o anunciante selecionado.

A visualização dos dados requer a permissão [!UICONTROL View Audiences]. Selecionar linhas e excluir exclusões com suporte requer a permissão [!UICONTROL Edit Audience Exclusions].

### Ações disponíveis

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Excluir exclusões de público](#audience-exclusions-delete)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Excluir exclusões de público {#audience-exclusions-delete}

*[!DNL Google Ads]exclusões somente*

Você pode excluir uma ou mais [!DNL Google Ads] exclusões de público-alvo. Não há suporte para a exclusão de [!DNL Microsoft Advertising] exclusões neste modo de exibição.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e depois clique na guia **[!UICONTROL Exclusions]**.

1. (Opcional) Filtre a lista para incluir exclusões específicas de público-alvo.

1. Marque a caixa de seleção ao lado de cada exclusão de [!DNL Google Ads] a ser excluída. Não inclua exclusões de outra rede de anúncios na seleção.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gerenciar públicos-alvo](audience-manage.md)
>* [Gerenciar metas de público-alvo para campanhas e grupos de anúncios](audience-targets-manage.md)
