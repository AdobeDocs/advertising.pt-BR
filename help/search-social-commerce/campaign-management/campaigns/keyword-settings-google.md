---
title: '[!DNL Google Ads] configurações de palavra-chave'
description: Referenciar as configurações de [!DNL Google Ads] palavras-chave.
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] configurações de palavra-chave

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

Consulte a ajuda do Google Ads para [limites de palavra-chave por conta](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Google Ads] corresponder a sintaxe de palavras-chave e espaços reservados. [!DNL Google Ads] As contas do exigem palavras-chave com os seguintes atributos:

* O comprimento máximo por palavra-chave é de 80 caracteres e não mais de 10 palavras.
* A palavra-chave pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [] ' + . / :`

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas a partir do [!UICONTROL Keywords] > [!UICONTROL Negatives] exibir e nas configurações do grupo de anúncios e da campanha.
>* Alterar um [!DNL Google Ads] palavra-chave ou tipo de correspondência exclui a palavra-chave existente e cria uma nova.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param1]:** A string a ser usada como o valor de substituição se o URL base ou o modelo de rastreamento contiver [o `{param1}`](https://support.google.com/google-ads/answer/6305348) cadeia de caracteres de substituição dinâmica.

**[!UICONTROL Param2]:** A string a ser usada como o valor de substituição se o URL base ou o modelo de rastreamento contiver [o `{param2}`](https://support.google.com/google-ads/answer/6305348) cadeia de caracteres de substituição dinâmica.

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
