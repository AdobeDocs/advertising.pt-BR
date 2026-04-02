---
title: Formatos de rastreamento de cliques para  [!DNL Baidu]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do  [!DNL Baidu] .
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
TQID: https://experienceleague.adobe.com/iV5-TNxdMov1LoPZzwP3RqkP93fp8A9TvAlY-2R-ZGo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Baidu]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
>* `<campaignID>` é uma variável para a ID numérica da campanha.
>
>* `<the landing page>` é uma variável que representa a URL do site para a qual os usuários finais são direcionados.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](https://experienceleague.adobe.com/pt-br/docs/analytics/components/dimensions/amo-id#dimension-items)
