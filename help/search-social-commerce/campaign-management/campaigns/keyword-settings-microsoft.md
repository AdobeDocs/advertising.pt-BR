---
title: '[!DNL Microsoft Advertising] configurações de palavra-chave'
description: Referenciar as configurações de [!DNL Microsoft Advertising] palavras-chave.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configurações de palavra-chave

Você pode criar palavras-chave para campanhas que usam as redes de pesquisa e exibição.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave, incluindo qualquer [!DNL Microsoft Advertising] corresponder sintaxe e espaços reservados. O comprimento máximo por palavra-chave é de 100 caracteres.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Você pode criar palavras-chave negativas a partir do [!UICONTROL Keywords] > [!UICONTROL Negatives] exibir e nas configurações do grupo de anúncios e da campanha.
>* Alterar um [!DNL Microsoft Advertising] palavra-chave exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param2]:** A sequência de caracteres a ser usada como valor de substituição se o URL base da palavra-chave ou o título, a descrição ou o URL base do anúncio contiver [o `{Param2}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

**[!UICONTROL Param3]:** A sequência de caracteres a ser usada como valor de substituição se o URL base da palavra-chave ou o título, a descrição ou o URL base do anúncio contiver [o `{Param3}` cadeia de caracteres de substituição dinâmica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres).

## Opções de URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Como opção, esse campo pode incluir a variável `{Param2}` e `{Param3}` variáveis de substituição dinâmicas.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
