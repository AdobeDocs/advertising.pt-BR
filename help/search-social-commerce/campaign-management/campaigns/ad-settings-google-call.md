---
title: '[!DNL Google Ads] configurações de anúncio somente de chamada'
description: Referencie as configurações de  [!DNL Google Ads] anúncios somente chamada.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] configurações de anúncio somente de chamada

Você pode criar anúncios de texto somente para chamada para campanhas que usam a rede de pesquisa.

A Search, Social e Commerce rastreia anúncios somente de chamada usando o sufixo da página de aterrissagem no nível da conta e o modelo de rastreamento, mas você pode, opcionalmente, substituir o rastreamento no nível da conta no nível do anúncio no Gerenciador do [!DNL Google Ads].

Consulte a ajuda do [!DNL Google Ads] para [limites de anúncios por conta](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** O nome da empresa. O comprimento máximo é de 25 caracteres ou 12 caracteres de byte duplo.

**[!UICONTROL Country]:** (Opcional) O país em que a empresa está localizada.

**[!UICONTROL Phone Number]:** O número de telefone da empresa. Exemplos: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** A primeira e a segunda linhas do corpo do anúncio. O comprimento máximo de cada linha é de 35 caracteres ou 17 caracteres de byte duplo.

A sintaxe de substituição de palavra-chave não conta para o comprimento máximo. Por exemplo, &quot;`{Description1: Free Account Analysis!}`&quot; é tratado como 22 caracteres (somente a parte &quot;Análise de Conta Gratuita\!&quot;).

>[!NOTE]
>
>Os campos de descrição não podem incluir números de telefone.

**[!UICONTROL Display URL]:** A URL exibida no anúncio. O URL de exibição deve corresponder a um domínio associado à sua empresa, mas o anúncio não envia pessoas para uma página de aterrissagem.

O comprimento máximo é de 35 caracteres de byte único ou 17 caracteres de byte duplo. A sintaxe de substituição de palavra-chave não conta para o comprimento máximo. Por exemplo, &quot;`{DisplayURL: example.com}`&quot; é tratado como 11 caracteres (somente a parte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Opcional) Uma página da Web na qual o número de telefone do seu anúncio aparece como texto, para que [!DNL Google Ads] possa verificar se o número de telefone é válido. Ele deve ter o mesmo domínio que o URL de exibição do anúncio.

**[!UICONTROL Is Tracked]:** Habilita o rastreamento de chamadas e conversões somente de chamadas.

**[!UICONTROL Count calls as phone call conversions]:** (Quando &quot;[!UICONTROL Is Tracked]&quot; é selecionado; opcional) Atribui todas as chamadas que resultam do anúncio a um tipo específico de conversão de chamadas telefônicas, quando uma é especificada. Caso contrário, o [!DNL Google Ads] criará uma ação de conversão padrão chamada &quot;[!UICONTROL Calls from ads]&quot; depois que registrar pelo menos uma conversão de seus números de encaminhamento e atribuir chamadas a ele.

**[!UICONTROL Count Action]:** (Quando &quot;[!UICONTROL Count calls as phone call conversions]&quot; é selecionado; opcional) A ação de conversão existente à qual as chamadas são atribuídas.

Você pode criar e gerenciar ações de conversão no [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Sobre anúncios](ad-about.md)
>* [Gerenciar anúncios](ad-manage.md)
>* [[!DNL Google Ads] configurações expandidas de anúncios de pesquisa dinâmica](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] configurações responsivas de pesquisa e publicidade](ad-settings-google-rsa.md)
