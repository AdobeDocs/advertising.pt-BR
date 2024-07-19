---
title: Formato das tags de rastreamento de conversão do JavaScript versão 3
description: Consulte o formato das tags de rastreamento de conversão do JavaScript versão 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Formato das tags de rastreamento de conversão do JavaScript versão 3

O formato a seguir é para sites que usam HTTPS. Para sites que usam HTTP, os URLs devem começar com &quot;http&quot;.

>[!NOTE]
>
>Para obter informações sobre quando usar a Versão 2 versus a Versão 3, consulte as [Perguntas frequentes sobre tags de rastreamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
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
>* [Formato das marcas de rastreamento de conversão de imagem](format-conversion-tag-image.md)
