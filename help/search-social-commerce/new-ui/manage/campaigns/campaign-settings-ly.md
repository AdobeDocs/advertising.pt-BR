---
title: Configurações de campanha de [!DNL LY Ads]
description: Referencie as configurações de  [!DNL LY Ads] campanhas.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Configurações de campanha de [!DNL LY Ads]

## \[Início da página]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign Type]:** Onde colocar anúncios: a única opção é *[!UICONTROL Search Network Only]* para exibir anúncios de texto na rede de pesquisa.

## Guia [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** O orçamento, que é a quantidade que você deseja gastar diariamente, em média. O orçamento diário mínimo é de 100 JPY.

Se você atribuir essa campanha a um portfólio para o qual os limites de orçamento de campanha são ajustados automaticamente, então, dependendo das condições de pesquisa, você pode realmente gastar mais ou menos do que o orçamento especificado em um determinado período.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

## Guia [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-yahoo-japan.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Somente para [!UICONTROL EF Redirect]) O nível em que os cliques e as receitas devem ser rastreados, adicionando um redirecionamento (quando relevante) e anexando parâmetros às URLs relevantes:

* *[!UICONTROL Keyword]:* Para rastrear dados somente no nível da palavra-chave.

* *[!UICONTROL Creative]:* Para rastrear dados somente no nível de anúncio (criativo).

* *[!UICONTROL Creative and Keyword]:* Para rastrear dados nos níveis de anúncio (criativo) e palavra-chave.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Adiciona um parâmetro de URL a anúncios na conta ou campanha para rastreamento de conversão.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
