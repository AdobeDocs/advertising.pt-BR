---
title: Formatos de rastreamento de cliques para  [!DNL Yandex]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do  [!DNL Yandex] .
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
TQID: https://experienceleague.adobe.com/iw-C9oApjU-LeXi3XJol3lgCJPGPegHgzFJIL-3HHSA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados em [!DNL Yandex]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
>* `<the landing page>` é uma variável que representa a URL do site para a qual os usuários finais são direcionados.
>
>* `source_type` é o tipo de correspondência.
>
>* `source` indica se o anúncio foi mostrado em um site de pesquisa ou baseado em conteúdo.
>
>* `position` é o número da posição do anúncio no bloco. Para tráfego que não é de pesquisa, o valor é &quot;0&quot;.
>
>* `position_type` é o bloco no qual o anúncio foi exibido em [!DNL Yandex]. Valores possíveis: &quot;premium&quot; (bloco superior), &quot;other&quot; (bloco direito) ou &quot;none&quot; (tráfego que não é de pesquisa).

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão da Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
