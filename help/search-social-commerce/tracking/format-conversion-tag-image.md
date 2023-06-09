---
title: Formato das tags de rastreamento de conversão de imagem
description: Referencie o formato de tags de rastreamento de conversão de imagem.
source-git-commit: b230c593d93dfa868b8f075939fc9940ea74fa13
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Formato das tags de rastreamento de conversão de imagem

>[!NOTE]
>
>Para obter informações sobre quando usar tags de imagem ou tags JavaScript, consulte [Perguntas frequentes sobre tags de rastreamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Tags não seguras para sites com HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Tags seguras para sites com HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

em que:

* `<ef-userid>` é uma ID de usuário exclusiva e numérica que o Search, Social e Commerce atribui ao anunciante.

* `<propertyname>` é a conversão que será rastreada. Por exemplo, se você estiver rastreando uma conversão chamada &quot;registro&quot;, a tag incluirá o parâmetro `ev_registration=<registration>`e você precisaria passar a receita real para cada transação (como `ev_registration=1`). Quando várias propriedades são rastreadas, elas são unidas por um E comercial (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por exemplo, `ev_registration=1&ev_sale=12.99`). **Nota:**  O nome da propriedade não pode incluir caracteres especiais.

* `<transid>` é uma ID de transação exclusiva (como uma ID de pedido real) que o anunciante gera e transmite para identificar uma transação. É incluído somente quando o &quot;[!UICONTROL Include unique transaction IDs]&quot; está selecionada.

  Search, Social, &amp; Commerce usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e valor de propriedade. A ID da transação está incluída na variável [!UICONTROL Transaction Report], que você pode usar para validar dados no Adobe Advertising com os dados do anunciante. **Nota:** Se os dados do anunciante não incluírem uma ID exclusiva por transação, Search, Social e Commerce ainda gerarão uma com base no tempo da transação.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Sobre as tags de rastreamento de conversão de publicidade do Adobe](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma tag de conversão Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 2](format-conversion-tag-jsv2.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 3](format-conversion-tag-jsv3.md)
