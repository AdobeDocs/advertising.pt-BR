---
title: Configurações de palavra-chave [!DNL Yandex]
description: Referencie as configurações de  [!DNL Yandex] palavras-chave.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/-PRiQ9myH0XNYF8pc2OVBuLOK-8BpxzqruOP2hzPW0I
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# Configurações de palavra-chave [!DNL Yandex]

As palavras-chave do Yandex são usadas para redes de pesquisa e exibição (conteúdo).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As frases de palavras-chave, incluindo qualquer [sintaxe de tipo de correspondência do Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para palavras-chave. Cada palavra-chave pode ter no máximo sete palavras, exceto palavras de interrupção.

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

>[!NOTE]
>
>* Alterar uma palavra-chave [!DNL Yandex] ou um tipo de correspondência exclui a palavra-chave existente e cria uma nova.
>* Cada grupo de anúncios do Yandex pode incluir no máximo 200 palavras-chave.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaços reservados

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** O valor das variáveis de substituição `{param1}` e `{param2}`, que são substituídas por quaisquer instâncias de {param1} e {param2} na URL base para anúncios e sitelinks quando a palavra-chave é usada para exibir o anúncio. O comprimento máximo é de 255 bytes.

Caracteres especiais são automaticamente codificados em UTF-8. Por exemplo, se o anúncio associado tiver uma URL base de &quot;http://www.example.com/{param1} e o valor de nível de palavra-chave de {param1} for &quot;shoes/flats.html&quot;, o anúncio levará para http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
