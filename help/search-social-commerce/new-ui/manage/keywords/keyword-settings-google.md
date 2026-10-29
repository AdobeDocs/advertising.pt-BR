---
title: Configurações de palavra-chave [!DNL Google Ads]
description: Referencie as configurações de [!DNL Google Ads] palavras-chave.
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# Configurações de palavra-chave [!DNL Google Ads]

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

Consulte a ajuda do [!DNL Google Ads] para [limites de palavras-chave por conta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*Somente novas palavras-chave*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Google Ads], correspondem à sintaxe para palavras-chave e espaços reservados. As contas do [!DNL Google Ads] exigem palavras-chave com os seguintes atributos:

* O comprimento máximo por palavra-chave é de 80 caracteres e não mais de 10 palavras.

* A palavra-chave pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [] ' + . / :`

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas na guia [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* Alterar uma palavra-chave [!DNL Google Ads] ou um tipo de correspondência exclui a palavra-chave existente e cria uma nova.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. O padrão para novas palavras-chave é *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver [a cadeia de caracteres de substituição dinâmica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver [a cadeia de caracteres de substituição dinâmica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](keyword-manage.md)
