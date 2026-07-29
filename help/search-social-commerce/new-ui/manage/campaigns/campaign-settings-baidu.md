---
title: Configurações de campanha de [!DNL Baidu]
description: Referencie as configurações de  [!DNL Baidu] campanhas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# Configurações de campanha de [!DNL Baidu]

## \[Início da página]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign Type]:** Onde colocar anúncios e quais tipos de anúncios a campanha pode conter. A única opção é *Pesquisar Somente Rede*.

## Guia [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Aplicável a campanhas direcionadas a públicos na União Europeia (UE)) Se a campanha contém ou não anúncios políticos de acordo com os requisitos para anúncios veiculados na União Europeia nos termos do Regulamento UE 2024/90: *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## Guia [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** A estratégia de oferta para a campanha:

* *[!UICONTROL Maximize Conversions]:* A rede de publicidade — não Search, Social e Commerce — otimiza ofertas para maximizar as conversões. Opcionalmente, insira um **[!UICONTROL Target CPA]** (custo por aquisição). **Observação:** use esta opção para campanhas em portfólios com otimização de nível de campanha. Em portfólios com otimização no nível da campanha, o Search, Social e Commerce otimiza o CPA do Target.

* *[!UICONTROL Maximize Conversion Value]:* A rede de publicidade — não Search, Social e Commerce — otimiza ofertas para maximizar o valor de conversão. Opcionalmente, insira um **[!UICONTROL Target Return on Ad Spend]** (ROAS) como uma porcentagem. **Observação:** use esta opção para campanhas em portfólios com otimização de nível de campanha. Em portfólios com otimização no nível da campanha, o Search, Social e Commerce otimiza o ROAS do Target.

## Guia [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** O idioma do anúncio, que deve corresponder ao idioma dos sites nos quais o anúncio pode aparecer. A rede de publicidade determina o idioma de um usuário a partir de vários sinais, incluindo o query do usuário, o país do editor e a configuração de idioma do usuário.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## Guia [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### Guia [!UICONTROL Campaign Tracking]

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
