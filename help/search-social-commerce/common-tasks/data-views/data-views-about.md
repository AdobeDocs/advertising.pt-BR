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
source-git-commit: 972ed9c0662fc3b74bc5c3597f010170fbce69d7
workflow-type: tm+mt
source-wordcount: '672'
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

## (Nova interface do usuário) Controles de tabela de dados {#data-table-tools-new-ui}

Use a barra de ferramentas acima da tabela de dados para gerenciar os dados e alterar sua exibição. As ferramentas disponíveis dependem da visualização e de suas permissões.

Se a barra de ferramentas for muito estreita para mostrar uma ferramenta, procure-a no menu **[!UICONTROL Actions]**.

Quando disponível, você pode:

* Selecione *[!UICONTROL Click Date]* ou *[!UICONTROL Transaction Date]* de [!UICONTROL Conversion based on] para controlar como os dados de conversão são relatados.

* Compare o desempenho de dois períodos e escolha como exibir a diferença. Consulte &quot;[Filtrar dados por intervalo de datas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)&quot;.

* Ative ou desative o espaçamento compacto da tabela usando **[!UICONTROL Compressed Mode]** na barra de ferramentas ou no menu **[!UICONTROL Actions]**.

  O botão da barra de ferramentas é selecionado quando o modo compactado está ativado. Em [!UICONTROL Actions], uma opção indica o estado atual.

* Mostrar ou ocultar gráficos usando **[!UICONTROL Charts]** na barra de ferramentas ou no menu **[!UICONTROL Actions]**.

  O botão da barra de ferramentas é selecionado quando os gráficos são exibidos. Em [!UICONTROL Actions], uma opção indica se os gráficos são mostrados. Clique no controle novamente para ocultar os gráficos.

## (Nova interface de usuário) Larguras de coluna e valores de tabela {#column-widths-values-new-ui}

Nas tabelas de dados da campanha:

* Redimensionar uma coluna arrastando o limite entre os cabeçalhos da coluna. Você também pode redimensionar [colunas bloqueadas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-lock-unlock.md) qualificadas sem desbloqueá-las primeiro. As larguras mínimas ajudam a manter os valores legíveis. Algumas colunas de ícone e ação têm larguras fixas e não podem ser redimensionadas.

* Mantenha o cursor sobre um nome de entidade truncado para ver o nome completo.

* Para abrir os detalhes de uma entidade cujo nome é um link, pressione **Tab** até que o nome seja realçado e pressione **Enter**.

* Um traço (-) indica um valor ausente, NULO ou não aplicável. Os valores zero e false permanecem visíveis.
