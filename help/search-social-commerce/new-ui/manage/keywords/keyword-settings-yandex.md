---
title: Configurações de palavra-chave [!DNL Yandex]
description: Referencie as configurações de [!DNL Yandex] palavras-chave.
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
source-wordcount: '227'
ht-degree: 0%
---
# Configurações de palavra-chave [!DNL Yandex]

[!DNL Yandex] palavras-chave são usadas para redes de pesquisa e exibição (conteúdo).

## [!UICONTROL Basic Settings]

*Somente novas palavras-chave*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As frases de palavras-chave, incluindo qualquer [[!DNL Yandex] sintaxe de tipo de correspondência](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palavras-chave. Cada palavra-chave pode ter no máximo sete palavras, exceto palavras de interrupção.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Alterar uma palavra-chave [!DNL Yandex] ou um tipo de correspondência exclui a palavra-chave existente e cria uma nova.
>* Cada grupo de anúncios [!DNL Yandex] pode incluir no máximo 200 palavras-chave.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. O padrão para novas palavras-chave é *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>Caracteres especiais são automaticamente codificados em UTF-8. Por exemplo, se o anúncio associado tiver uma URL base de `http://www.example.com/{param1}` e o valor de nível de palavra-chave de `{param1}` for `shoes/flats.html`, o anúncio levará a `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base contiver a cadeia de caracteres de substituição dinâmica `{param1}` para anúncios e sitelinks quando a palavra-chave for usada para exibir o anúncio. O comprimento máximo é de 255 bytes.

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base contiver a cadeia de caracteres de substituição dinâmica `{param2}` para anúncios e sitelinks quando a palavra-chave for usada para exibir o anúncio. O comprimento máximo é de 255 bytes.

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](keyword-manage.md)
