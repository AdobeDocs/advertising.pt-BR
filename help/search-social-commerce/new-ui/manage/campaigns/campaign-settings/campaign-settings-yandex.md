---
title: Configurações de campanha de [!DNL Yandex]
description: Referencie as configurações de  [!DNL Yandex] campanhas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# Configurações de campanha de [!DNL Yandex]

## \[Início da página]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign Type]:** Onde colocar anúncios:

* *[!UICONTROL Search Network Only]:* Exibe anúncios de texto na rede de pesquisa. Você deve especificar palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Search and Display Network]:* Exibe anúncios de texto na rede de pesquisa e no [!DNL Yandex Advertising Network]. Para anúncios de pesquisa, você deve especificar palavras-chave de pesquisa para cada grupo de anúncios. Para anúncios de exibição, você deve especificar palavras-chave para os sites nos quais deseja anunciar cada grupo de anúncios.

* *[!UICONTROL Display Network Only]:* Exibe anúncios de texto no [!DNL Yandex Advertising Network]. Para cada grupo de publicidade, você deve especificar palavras-chave para os sites nos quais deseja anunciar.

## Guia [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## Guia [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** O orçamento, que é a quantidade que você deseja gastar diariamente (em média) ou durante o tempo de vida da campanha, dependendo do tipo de orçamento da conta. O orçamento mínimo é py6 300, EUR 10, ou USD 10.

**Notas:**

* Novas campanhas têm a estratégia de gerenciamento de ofertas &quot;Posição mais alta disponível&quot;.

* Dependendo das condições de pesquisa, se você atribuir essa campanha a um portfólio configurado para permitir que os limites de orçamento da campanha sejam ajustados automaticamente, será possível gastar mais ou menos do que o orçamento especificado em um determinado dia, mês ou duração.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## Guia [!UICONTROL Additional Campaign Information]

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Somente para [!UICONTROL EF Redirect]; somente leitura) O nível no qual os cliques e a receita devem ser rastreados. Somente *[!UICONTROL Creative]* está disponível para [!DNL Yandex] — os dados são rastreados somente no nível de anúncio (criativo).

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
