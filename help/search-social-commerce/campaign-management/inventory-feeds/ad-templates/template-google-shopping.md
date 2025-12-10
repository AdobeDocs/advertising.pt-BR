---
title: '[!DNL Google Ads] configurações de modelo de anúncio de compra para feeds de inventário'
description: Referencie as configurações de  [!DNL Google Ads] modelos de anúncios de compras para feeds de inventário.
exl-id: 36cbe719-f984-4456-8575-94b9d3e6094e
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# [!DNL Google Ads] configurações de modelo de anúncio de compra para feeds de inventário

Use modelos de anúncios de compras para configurar esses anúncios.

>[!NOTE]
>
>* Os seguintes caracteres são reservados para designar nomes de coluna e nomes de modificadores no modelo e, portanto, são proibidos como texto em todos os campos de atributo: `[ ] < > `

## \[Acima de todas as guias\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Painel esquerdo\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (opcional para modelos para arquivos de feed de cliente) O modelo de rastreamento de nível de campanha, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora a URL final em um parâmetro. Esse valor substitui a configuração no nível da conta, mas os modelos de rastreamento em níveis mais granulares (com a palavra-chave como o mais granular) substituem esse valor.

Para o rastreamento de conversão do Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, use o [formato de modelo de rastreamento para campanhas de compras do Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Se a conta inteira for dedicada a anúncios de compras, você poderá definir um modelo de rastreamento no nível da conta.

Para redirecionamentos e rastreamento de terceiros, insira um valor.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** A ID do cliente da conta de comerciante cujos produtos são usados para a campanha.

**[!UICONTROL Sales Country]:** O país no qual os produtos da campanha são vendidos. Como os produtos estão associados
com os países de destino, essa configuração determina quais produtos são anunciados na campanha.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** As redes nas quais colocar anúncios. *[!UICONTROL Search]* já está selecionado. Para incluir ofertas em listagens para [!DNL Google Ads] parceiros de pesquisa, marque a caixa de seleção ao lado de **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** A prioridade com a qual a campanha é usada quando várias campanhas anunciam o
mesmo produto: *[!UICONTROL Low]* (o padrão para novas campanhas), *[!UICONTROL Medium]* ou *[!UICONTROL High]*. Quando o mesmo produto é incluído em mais de uma campanha, a rede de publicidade usa
a prioridade da campanha primeiro para determinar qual campanha (e lances associados) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**([!DNL Google Ads] e [!DNL Microsoft Advertising] campanhas somente; aplicável a campanhas direcionadas a públicos na União Europeia (UE)) Se a campanha contém ou não anúncios políticos de acordo com os requisitos para anúncios veiculados na União Europeia nos termos do Regulamento UE 2024/90: *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (opcional) um modelo de rastreamento de nível de grupo de anúncios, que especifica todos os redirecionamentos e parâmetros de rastreamento de domínio fora da aterrissagem e incorpora a URL final em um parâmetro. Esse valor substitui as configurações no nível da conta e da campanha, mas os modelos de rastreamento em níveis mais granulares substituem esse valor.

Para o rastreamento de conversão do Adobe Advertising, não é necessário inserir um valor. O valor no nível da campanha é suficiente.

Para redirecionamentos e rastreamento de terceiros, insira um valor.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** o grupo de produtos padrão, completo, &quot;[!UICONTROL All products].&quot; Você não pode excluir este grupo de produtos principal, mas ele é excluído automaticamente quando todas as camadas inferiores estão ausentes do feed.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unidades sem grupos de produtos filho; opcional) O modelo de rastreamento do produto
grupo, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora a URL final em um parâmetro [!DNL ValueTrack]. Esse template substitui templates em níveis superiores.

Para o rastreamento de conversão do Adobe Advertising, não é necessário inserir um valor. O valor no nível da campanha é suficiente.

Para redirecionamentos e rastreamento de terceiros, insira um valor.

**[!UICONTROL Initial Bid]:** O lance inicial para cada anúncio.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Sobre a automatização do gerenciamento de anúncios usando feeds de inventário](../inventory-feeds-about.md)
>* [Gerenciando modificadores](../modifiers-manage.md)
>* [Gerenciamento de arquivos de feed de dados de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagar dados de feed por meio de modelos](../feed-data-propagate.md)
>* [Postar dados de campanha dos feeds de inventário nas redes de anúncios](../propagated-data-post.md)
