---
title: Formatos de rastreamento de cliques para  [!DNL Naver]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do  [!DNL Naver] .
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
TQID: https://experienceleague.adobe.com/c1zAy1aKgr4MRpyiitdmO4VxP7kfKfFWHzYk88lvX2w
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Naver]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
* `<the landing page>` é uma variável que representa a URL do site para a qual os usuários finais são direcionados.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
