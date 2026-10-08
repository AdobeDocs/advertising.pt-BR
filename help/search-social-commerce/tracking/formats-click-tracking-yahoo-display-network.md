---
title: Formatos de rastreamento de cliques para [!DNL Yahoo DSP]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do [!DNL Yahoo DSP].
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/sQo6hr3UHQwN9GgazCKv2ba-m4ZXf2ZrhdemCpbVYvU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%
---
# Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Yahoo DSP]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
>* `<the landing page>` é uma variável que representa a URL do site para a qual os usuários finais são direcionados.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
