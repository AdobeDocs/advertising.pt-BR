---
title: Configurações de palavra-chave [!DNL LY Ads]
description: Referencie as configurações de [!DNL LY Ads] palavras-chave.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%
---
# Configurações de palavra-chave [!DNL LY Ads]

## [!UICONTROL Basic Settings]

*Somente novas palavras-chave*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave. O comprimento máximo é de 80 caracteres, incluindo qualquer [[!DNL LY Ads] sintaxe de tipo de correspondência](https://ads-help.yahoo-net.jp/s/article/H000044997) para palavras-chave.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas na guia [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* [!DNL LY Ads] palavras-chave e tipos correspondentes são mutáveis, o que significa que você pode editá-las sem excluir a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. O padrão para novas palavras-chave é *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver o `{param1}` [parâmetro personalizado](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver o `{param2}` [parâmetro personalizado](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](keyword-manage.md)
