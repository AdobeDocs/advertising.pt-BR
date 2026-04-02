---
title: Configurações de palavra-chave [!DNL Microsoft Advertising]
description: Referencie as configurações de  [!DNL Microsoft Advertising] palavras-chave.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/fA0ZDCw5Ici0wOfpd1kXdjbQA6DtUFxOSBEtrlJl4Oo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Configurações de palavra-chave [!DNL Microsoft Advertising]

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Microsoft Advertising], correspondem à sintaxe e aos espaços reservados. O comprimento máximo por palavra-chave é de 100 caracteres.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas no modo de exibição [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* Alterar uma palavra-chave [!DNL Microsoft Advertising] exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param2]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, a descrição ou a URL base do anúncio contiver [a `{Param2}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

**[!UICONTROL Param3]:** A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, a descrição ou a URL base do anúncio contiver [a `{Param3}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

## Opções de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Opcionalmente, este campo pode incluir as variáveis de substituição dinâmica `{Param2}` e `{Param3}`.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
