---
title: Sobre a personalização de dados em visualizações de gerenciamento de campanha
description: Saiba mais sobre os tipos de dados que você pode personalizar nas visualizações de dados do Campaign.
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---
# Sobre a personalização de dados em visualizações de gerenciamento de campanha

Na maioria das visualizações de dados do Campaign, é possível personalizar os dados exibidos na tabela de dados. Você pode personalizar os dados das seguintes maneiras:

* [Edite as configurações de todo o modo de exibição padrão](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit) de um modo de exibição de entidade específico (como [!UICONTROL Campaigns]) para incluir uma ordem de coluna específica, filtros, intervalo de datas, regra de atribuição e muito mais — e aplique as configurações temporariamente ou salve-as. Você também pode [criar exibições personalizadas adicionais](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view), [clonar exibições existentes](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone) e [aplicar qualquer uma de suas exibições](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view).

* [Altere as colunas e sua ordem de classificação](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md) usando o controle [!UICONTROL Custom Columns] na barra de ferramentas. Na nova interface, se a barra de ferramentas for muito estreita para mostrar o controle, clique em **[!UICONTROL Actions]>[!UICONTROL Custom Columns]**. Você também pode [alterar rapidamente apenas as colunas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) de qualquer cabeçalho de coluna na exibição.

* (Somente interface de usuário herdada) [No painel de navegação esquerdo](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md), é possível:

  * Procure ou pesquise entidades por rede de anúncios e filtre pelo status da entidade e o status da conta, da campanha e do grupo de anúncios ou conjunto de anúncios. Clique em qualquer entidade ou grupo de entidades no painel para carregar uma exibição das entidades filhas (por exemplo, clique em um nome de campanha para exibir seus grupos de anúncios filhos).

  * Procure ou pesquise campanhas por portfólio ou grupo de portfólio e filtre pelo status da entidade e o status do grupo de portfólio, portfólio e campanha. Clique em qualquer grupo, portfólio ou campanha do portfólio no painel para carregar dados para o grupo, portfólio ou campanha do portfólio na exibição de entidade atual.

  * Acesse, edite e redefina as exibições padrão, e acesse, edite e exclua as exibições personalizadas. Clicar em qualquer nome de exibição carrega a exibição apropriada.

* Aplique filtros em qualquer coluna de dados disponível para alterar os dados exibidos na guia atual. Você pode criar filtros [a partir dos títulos das colunas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md) ou [a partir de um botão na barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md). Para exibições de gerenciamento de campanha, os filtros são mantidos conforme aplicável quando você abre entidades filhas. Por exemplo, se você exibir campanhas com \> 100 cliques e, em seguida, abrir um grupo de anúncios nessa campanha, somente grupos de anúncios com \> 100 cliques serão mostrados.

* [Altere o intervalo de datas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md) usado em todas as exibições padrão e personalizadas para as quais você não salvou intervalos de datas específicos.

* [Reclassificar os dados](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md) de acordo com os valores em uma coluna específica.

* Controla se deve exibir 25 linhas, 50 linhas, 100 linhas, (somente interface do usuário herdada) 200 linhas ou (somente interface do usuário herdada) [!UICONTROL Continuous Scroll] na parte inferior de qualquer página.

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
