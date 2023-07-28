---
title: Formato das tags de rastreamento de conversão do JavaScript versão 2
description: Consulte o formato das tags de rastreamento de conversão do JavaScript versão 2.
exl-id: c4845694-10ac-41f8-bafb-ca813e42d190
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Formato das tags de rastreamento de conversão do JavaScript versão 2

O formato a seguir é para sites que usam HTTPS. Para sites que usam HTTP, os URLs devem começar com &quot;http&quot;.

>[!NOTE]
>
>Para obter informações sobre quando usar a Versão 2 ou a Versão 3, consulte [Perguntas frequentes sobre tags de rastreamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

em que:

* `<ef-userid>` é uma ID de usuário exclusiva e numérica que o Search, Social e Commerce atribui ao anunciante.

* `<propertyname>` é a conversão que será rastreada. Por exemplo, se você estiver rastreando uma conversão chamada &quot;registro&quot;, a tag incluirá o parâmetro `ev_registration=<registration>`e você precisaria passar a receita real para cada transação (como `ev_registration=1`). Quando várias propriedades são rastreadas, elas são unidas por um E comercial (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por exemplo, `ev_registration=1&ev_sale=12.99`). **Nota:**  O nome da propriedade não pode incluir caracteres especiais.

* `<transid>` é uma ID de transação exclusiva (como uma ID de pedido real) que o anunciante gera e transmite para identificar uma transação. É incluído somente quando o &quot;[!UICONTROL Include unique transaction IDs]&quot; está selecionada.

  Search, Social, &amp; Commerce usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e valor de propriedade. A ID da transação está incluída na variável [!UICONTROL Transaction Report], que você pode usar para validar dados no Adobe Advertising com os dados do anunciante. **Nota:** Se os dados do anunciante não incluírem uma ID exclusiva por transação, Search, Social e Commerce ainda gerarão uma com base no tempo da transação.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Sobre as tags de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma tag de conversão de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 2](format-conversion-tag-jsv2.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 3](format-conversion-tag-jsv3.md)
>* [Formato das tags de rastreamento de conversão de imagem](format-conversion-tag-image.md)
