---
title: Formatos de rastreamento de cliques para [!DNL Naver]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Naver] contas.
exl-id: ff243eb5-d768-4e5c-b5b3-015fe22c9d5a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados no [!DNL Naver]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
* `<the landing page>` é uma variável que representa o URL do site para o qual os usuários finais são direcionados.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para o código de rastreamento s\_kwcid](skwcid-tracking-parameter.md)
