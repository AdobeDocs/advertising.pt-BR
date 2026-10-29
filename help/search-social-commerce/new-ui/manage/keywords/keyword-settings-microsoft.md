---
title: Configurações de palavra-chave [!DNL Microsoft Advertising]
description: Referencie as configurações de [!DNL Microsoft Advertising] palavras-chave.
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
source-wordcount: '281'
ht-degree: 0%
---
# Configurações de palavra-chave [!DNL Microsoft Advertising]

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

## [!UICONTROL Basic Settings]

*Somente novas palavras-chave*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Microsoft Advertising], correspondem à sintaxe e aos espaços reservados. O comprimento máximo por palavra-chave é de 100 caracteres.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas na guia [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* Alterar uma palavra-chave [!DNL Microsoft Advertising] exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. O padrão para novas palavras-chave é *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, a descrição ou a URL base do anúncio contiver [a `{Param1}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, a descrição ou a URL base do anúncio contiver [a `{Param2}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Opcionalmente, este campo pode incluir as variáveis de substituição dinâmica `{Param1}` e `{Param2}`.

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](keyword-manage.md)
