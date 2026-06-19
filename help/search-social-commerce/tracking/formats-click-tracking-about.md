---
title: Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising
description: Saiba mais sobre os formatos de rastreamento de cliques para redes de anúncios compatíveis.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising

Os templates de rastreamento, sufixos de landing page (sufixos de URL final) e URLs de destino para contas de anúncio e campanhas que usam o serviço de rastreamento de conversão do Adobe Advertising têm o seguinte formato:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

em que:

* `http://pixel.everesttech.net` redireciona o usuário para os servidores de pixels da Adobe Advertising.

* `<advertiser_ID>` é uma variável para a ID de usuário exclusiva atribuída ao anunciante no Adobe Advertising.

* `<token passing parameter>` é uma variável para um dos seguintes:

   * `cq?` ou `rq` indica que a transmissão de tokens está habilitada.

   * `c?` ou `r` indica que a passagem do token está desabilitada.

* `<ad network ID>` é uma variável da ID numérica da rede de publicidade especificada, como *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL LY Ads] (antigo [!DNL Yahoo! Japan Ads]), *105* para [!DNL Yahoo Native] (obsoleto) ou *106* para [!DNL Pinterest] (obsoleto).

* `<tracking ID>` é uma variável de uma cadeia de caracteres de ID de rastreamento gerada pelo sistema que identifica uma palavra-chave, anúncio ou posicionamento exclusivo na conta. A string varia de acordo com a rede de anúncios.

* `<the landing page>` é uma variável que representa a URL do site para a qual os usuários finais são direcionados. Para contas com URLs de destino, esse valor é um URL. Para contas com modelos de rastreamento, esse valor é um parâmetro (como `{lpurl}`) que representa a URL final.

Consulte as páginas separadas indicando os [[!DNL Baidu] formatos](formats-click-tracking-baidu.md), [[!DNL Google Ads] formatos](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formatos](formats-click-tracking-microsoft.md), [[!DNL Naver] formatos](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formatos](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formatos](formats-click-tracking-yahoo-japan.md) e [[!DNL Yandex] formatos](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formatos de rastreamento de cliques para [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formatos de rastreamento de cliques para [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Yandex]](formats-click-tracking-yandex.md)
