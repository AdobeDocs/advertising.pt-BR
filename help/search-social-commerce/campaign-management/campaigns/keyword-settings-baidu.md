---
title: Configurações de palavra-chave [!DNL Baidu]
description: Referencie as configurações de  [!DNL Baidu] palavras-chave.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/uMU0oAkL8rmsOIMXYR8qgp9-upe2qWIK-ev1YtPQUb4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# Configurações de palavra-chave [!DNL Baidu]

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave. O tamanho máximo por palavra-chave é de 30 caracteres de byte único ou 15 caracteres de byte duplo

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas. Use a seguinte sintaxe:

* `keyword` para correspondência ampla
* `"keyword"` para correspondência de frase
* `[keyword]` para correspondência exata

>[!NOTE]
>
>* [!DNL Baidu] permite somente um tipo de correspondência por palavra-chave por grupo de publicidade. Por exemplo, o Grupo de Anúncios 1 não pode incluir `"keyword"` e `[keyword]`.
>* Você pode criar palavras-chave negativas no modo de exibição [!UICONTROL Keywords] > [!UICONTROL Negatives] e nas configurações de grupo de anúncios e campanha.
>* Alterar uma palavra-chave [!DNL Baidu] exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opções de URL

**[!UICONTROL Base URL]:** (Campanhas somente com rastreamento de nível de palavra-chave; opcional) A URL da página de aterrissagem para a qual os usuários são levados quando clicam em seu anúncio. Pode incluir
redirecionamento e código de rastreamento de terceiros. Se você inserir um valor, ele substituirá o URL base do anúncio.

Depois de salvar o registro, o URL base inclui todos os parâmetros de acréscimo configurados para a campanha ou conta.

Se você usar o serviço de rastreamento de conversão da Adobe Advertising e as configurações da campanha incluírem o uso de [!UICONTROL EF Redirect] e a adição de rastreamento no nível da palavra-chave, o Search, o Social e o Commerce adicionarão automaticamente seu próprio código de rastreamento de cliques.

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
