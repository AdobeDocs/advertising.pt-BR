---
title: '[!DNL Google Ads] configurações de anúncios somente para chamada'
description: Referenciar as configurações de [!DNL Google Ads] anúncios somente para chamada.
exl-id: 1f810c2b-9c30-43c6-bda6-07609423ef79
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] configurações de anúncio somente de chamada

Você pode criar anúncios de texto somente para chamada para campanhas que usam a rede de pesquisa.

O Search, Social e Commerce rastreia anúncios somente chamada usando o sufixo da página de aterrissagem em nível de conta e o modelo de rastreamento, mas é possível substituir o rastreamento em nível de conta no nível de anúncio no [!DNL Google Ads] Gerente.

Consulte a [!DNL Google Ads] ajuda para [limites de publicidade por conta](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** O nome da empresa. O comprimento máximo é de 25 caracteres ou 12 caracteres de byte duplo.

**[!UICONTROL Country]:** (Opcional) O país em que a empresa está localizada.

**[!UICONTROL Phone Number]:** O telefone da empresa. Exemplos: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** A primeira e a segunda linhas do corpo do anúncio. O comprimento máximo de cada linha é de 35 caracteres ou 17 caracteres de byte duplo.

A sintaxe de substituição de palavra-chave não conta para o comprimento máximo. Por exemplo, &quot;`{Description1: Free Account Analysis!}`&quot; é tratado como 22 caracteres (somente a parte &quot;Análise de conta gratuita\!&quot;).

>[!NOTE]
>
>Os campos de descrição não podem incluir números de telefone.

**[!UICONTROL Display URL]:** O URL exibido no anúncio. O URL de exibição deve corresponder a um domínio associado à sua empresa, mas o anúncio não envia pessoas para uma página de aterrissagem.

O comprimento máximo é de 35 caracteres de byte único ou 17 caracteres de byte duplo. A sintaxe de substituição de palavra-chave não conta para o comprimento máximo. Por exemplo, &quot;`{DisplayURL: example.com}`&quot; é tratado como 11 caracteres (somente a parte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Opcional) Uma página da Web na qual o número de telefone do anúncio é exibido como texto, para que [!DNL Google Ads] O pode verificar se o número de telefone é válido. Ele deve ter o mesmo domínio que o URL de exibição do anúncio.

**[!UICONTROL Is Tracked]:** Habilita o rastreamento de chamadas e conversões somente de chamada.

**[!UICONTROL Count calls as phone call conversions]:** (Quando &quot;[!UICONTROL Is Tracked]&quot; é selecionado; opcional) Atribui todas as chamadas que resultam do anúncio a um tipo específico de conversão de chamada telefônica, quando uma for especificada. Caso contrário, [!DNL Google Ads] O cria uma ação de conversão padrão chamada &quot;[!UICONTROL Calls from ads]&quot; depois de registrar pelo menos uma conversão dos números de encaminhamento e, em seguida, atribuir chamadas a ele.

**[!UICONTROL Count Action]:** (Quando &quot;[!UICONTROL Count calls as phone call conversions]&quot; é selecionado; opcional) A ação de conversão existente à qual as chamadas são atribuídas.

Você pode criar e gerenciar ações de conversão no [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Sobre anúncios](ad-about.md)
>* [Gerenciar anúncios](ad-manage.md)
>* [[!DNL Google Ads] configurações expandidas de anúncios de pesquisa dinâmica](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] configurações de anúncio de pesquisa responsiva](ad-settings-google-rsa.md)
