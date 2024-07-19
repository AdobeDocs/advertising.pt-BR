---
title: Formato das tags de rastreamento de conversão do JavaScript versão 2
description: Consulte o formato das tags de rastreamento de conversão do JavaScript versão 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Formato das tags de rastreamento de conversão do JavaScript versão 2

O formato a seguir é para sites que usam HTTPS. Para sites que usam HTTP, os URLs devem começar com &quot;http&quot;.

>[!NOTE]
>
>Para obter informações sobre quando usar a Versão 2 versus a Versão 3, consulte as [Perguntas frequentes sobre tags de rastreamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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

* `<propertyname>` é a conversão a ser monitorada. Por exemplo, se você estiver rastreando uma conversão chamada &quot;registro&quot;, a tag incluirá o parâmetro `ev_registration=<registration>` e você precisará passar a receita real para cada transação (como `ev_registration=1`). Quando várias propriedades são rastreadas, elas são unidas por um E comercial (`&`), como `ev_registration=<registration>&ev_sale=<sale>` (por exemplo, `ev_registration=1&ev_sale=12.99`). **Observação:** o nome da propriedade não pode incluir caracteres especiais.

* `<transid>` é um identificador de transação exclusivo (como um identificador de pedido real) que o anunciante gera e transmite para identificar uma transação. É incluído somente quando a opção &quot;[!UICONTROL Include unique transaction IDs]&quot; é selecionada.

  O Search, Social e Commerce usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e valor de propriedade. A ID da transação está incluída no [!UICONTROL Transaction Report], que você pode usar para validar dados no Adobe Advertising com os dados do anunciante. **Observação:** se os dados do anunciante não incluírem uma ID exclusiva por transação, Search, Social e Commerce ainda gerarão uma com base no tempo de transação.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma marca de conversão de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão de imagem](format-conversion-tag-image.md)
