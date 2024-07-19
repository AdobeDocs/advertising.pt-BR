---
title: Formatos de rastreamento de cliques para  [!DNL Yahoo! Display Network]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do  [!DNL Yahoo! Display Network] .
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Yahoo! Display Network]

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
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](/help/integrations/analytics/ids.md#amo-id-formats)
