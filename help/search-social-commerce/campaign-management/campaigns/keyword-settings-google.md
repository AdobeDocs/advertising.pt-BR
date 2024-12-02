---
title: Configurações de palavra-chave [!DNL Google Ads]
description: Referencie as configurações de  [!DNL Google Ads] palavras-chave.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Configurações de palavra-chave [!DNL Google Ads]

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

Consulte a ajuda do Google Ads para [limites de palavras-chave por conta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Google Ads], correspondem à sintaxe para palavras-chave e espaços reservados. As contas do [!DNL Google Ads] exigem palavras-chave com os seguintes atributos:

* O comprimento máximo por palavra-chave é de 80 caracteres e não mais de 10 palavras.
* A palavra-chave pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [] ' + . / :`

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas no modo de exibição [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* Alterar uma palavra-chave [!DNL Google Ads] ou um tipo de correspondência exclui a palavra-chave existente e cria uma nova.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param1]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver [a cadeia de caracteres de substituição dinâmica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base ou o modelo de rastreamento contiver [a cadeia de caracteres de substituição dinâmica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## Opções de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
