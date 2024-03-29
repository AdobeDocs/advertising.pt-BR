---
title: '[!DNL Yandex] configurações de palavra-chave'
description: Referenciar as configurações de [!DNL Yandex] palavras-chave.
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] configurações de palavra-chave

As palavras-chave do Yandex são usadas para redes de pesquisa e exibição (conteúdo).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As frases de palavras-chave, incluindo qualquer [Sintaxe de tipo de correspondência do Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palavras-chave. Cada palavra-chave pode ter no máximo sete palavras, exceto palavras de interrupção.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Alterar um [!DNL Yandex] palavra-chave ou tipo de correspondência exclui a palavra-chave existente e cria uma nova.
>* Cada grupo de anúncios do Yandex pode incluir no máximo 200 palavras-chave.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** O valor de `{param1}` e `{param2}` variáveis de substituição, que são substituídas por quaisquer instâncias de {param1} e {param2} no URL base para anúncios e sitelinks quando a palavra-chave é usada para exibir o anúncio. O comprimento máximo é de 255 bytes.

Caracteres especiais são automaticamente codificados em UTF-8. Por exemplo, se o anúncio associado tiver um URL de base de &quot;http://www.example.com/{param1} e o valor de nível de palavra-chave de {param1} é &quot;shoes/flats.html&quot;, então o anúncio leva a http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
