---
title: Formatos de rastreamento de cliques para [!DNL Yahoo! Japan Ads]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Yahoo! Japan Ads] contas.
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados no [!DNL Yahoo! Japan Ads]

Os seguintes formatos de modelo de rastreamento base se aplicam aos anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

ou, quando a opção de marcação automática estiver definida para a conta no [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* `<the landing page>` é uma variável que representa o URL do site para o qual os usuários finais são direcionados.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para o código de rastreamento da ID do AMO](skwcid-tracking-parameter.md)
