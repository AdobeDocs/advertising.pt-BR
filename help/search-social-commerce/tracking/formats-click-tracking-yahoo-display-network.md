---
title: Formatos de rastreamento de cliques para [!DNL Yahoo! Display Network]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Yahoo! Display Network] contas.
exl-id: 62ea592c-9138-4a8e-9616-c8f2475fea26
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados no [!DNL Yahoo! Display Network]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
>* [Formatos para o código de rastreamento da ID do AMO](amo-id-tracking-parameter.md)
