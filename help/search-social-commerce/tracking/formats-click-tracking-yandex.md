---
title: Formatos de rastreamento de cliques para [!DNL Yandex]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Yandex] contas.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para anúncios patrocinados no [!DNL Yandex]

O formato de URL de destino básico a seguir se aplica a anúncios patrocinados:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* `<the landing page>` é uma variável que representa o URL do site para o qual os usuários finais são direcionados.
>
>* `source_type`  é o tipo de correspondência.
>
>* `source` é se o anúncio foi exibido em um site de pesquisa ou baseado em conteúdo.
>
>* `position` é o número da posição do anúncio no bloco. Para tráfego que não é de pesquisa, o valor é &quot;0&quot;.
>
>* `position_type` é o bloco no qual o anúncio foi exibido [!DNL Yandex]. Valores possíveis: &quot;premium&quot; (bloco superior), &quot;other&quot; (bloco direito) ou &quot;none&quot; (tráfego que não é de pesquisa).

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID do AMO](/help/integrations/analytics/ids.md#amo-id-formats)
