---
title: Formato das tags de rastreamento de conversão de imagem
description: Referencie o formato de tags de rastreamento de conversão de imagem.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TQMACo5-LkbCU2SiMmUE-ZDBRTb8NERQPQ9ISzU0DdU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 0%

---

# Formato das tags de rastreamento de conversão de imagem

>[!NOTE]
>
>Para obter informações sobre quando usar tags de imagem ou tags do JavaScript, consulte as [Perguntas frequentes sobre tags de rastreamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Tags não seguras para sites com HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Tags seguras para sites com HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

em que:

* `<ef-userid>` é uma ID de usuário exclusiva e numérica que o Search, Social e Commerce atribui ao anunciante.

* `<propertyname>` é a conversão a ser monitorada. Por exemplo, se você estiver rastreando uma conversão chamada &quot;registro&quot;, a tag incluirá o parâmetro `ev_registration=<registration>` e você precisará passar a receita real para cada transação (como `ev_registration=1`). Quando várias propriedades são rastreadas, elas são unidas por um E comercial (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por exemplo, `ev_registration=1&ev_sale=12.99`). **Observação:** o nome da propriedade não pode incluir caracteres especiais.

* `<transid>` é um identificador de transação exclusivo (como um identificador de pedido real) que o anunciante gera e transmite para identificar uma transação. É incluído somente quando a opção &quot;[!UICONTROL Include unique transaction IDs]&quot; é selecionada.

  O Search, Social e Commerce usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e valor de propriedade. A ID da transação está incluída no [!UICONTROL Transaction Report], que você pode usar para validar dados no Adobe Advertising com os dados do anunciante. **Observação:** se os dados do anunciante não incluírem uma ID exclusiva por transação, Search, Social e Commerce ainda gerarão uma com base no tempo de transação.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma marca de conversão do Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](format-conversion-tag-jsv3.md)
