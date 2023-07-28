---
title: '[!DNL Baidu] configurações de palavra-chave'
description: Referenciar as configurações de [!DNL Baidu] palavras-chave.
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] configurações de palavra-chave

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** As palavras-chave. O tamanho máximo por palavra-chave é de 30 caracteres de byte único ou 15 caracteres de byte duplo

Você pode inserir ou colar até 2000 palavras-chave. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas. Use a seguinte sintaxe:

* `keyword` para correspondência ampla
* `"keyword"` para correspondência de frase
* `[keyword]` para correspondência exata

>[!NOTE]
>
>* [!DNL Baidu] permite somente um tipo de correspondência por palavra-chave por grupo de publicidade. Por exemplo, o Grupo de anúncios 1 não pode incluir ambos `"keyword"` e `[keyword]`.
>* Você pode criar palavras-chave negativas a partir do [!UICONTROL Keywords] > [!UICONTROL Negatives] exibir e nas configurações do grupo de anúncios e da campanha.
>* Alterar um [!DNL Baidu] palavra-chave exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.

**[!UICONTROL Status]:** O status de exibição da palavra-chave: *Ativo* ou *Pausado*. O padrão para novas palavras-chave é *Ativo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opções de URL

**[!UICONTROL Base URL]:** (Campanhas somente com rastreamento em nível de palavra-chave; opcional) O URL da página inicial para a qual os usuários são levados quando clicam em seu anúncio. Ele pode incluir redirecionamento e código de rastreamento de terceiros. Se você inserir um valor, ele substituirá o URL base do anúncio.

Depois de salvar o registro, o URL base inclui todos os parâmetros de acréscimo configurados para a campanha ou conta.

Se você usar o serviço de rastreamento de conversão de Adobe Advertising e as configurações da campanha incluírem o uso de [!UICONTROL EF Redirect] Além disso, adicionar rastreamento no nível de palavra-chave, Pesquisar, Social e Comércio adiciona automaticamente seu próprio código de rastreamento de cliques.

>[!MORELIKETHIS]
>
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
