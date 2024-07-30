---
title: A tag de mapeamento de conversão do Adobe Advertising
description: Saiba mais sobre a tag de mapeamento de conversão baseada em JavaScript para ITP 2.2, que permite que o Adobe Advertising rastreie um evento de conversão que ocorre em uma página que não é a página inicial.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# A tag de mapeamento de conversão do Adobe Advertising JavaScript

*Anunciantes somente com rastreamento de conversão de Adobe Advertising*

A tag de mapeamento de conversão baseada em JavaScript do Adobe Advertising, quando usada além da tag de rastreamento de conversão do Adobe Advertising JavaScript v2 ou v3, permite que o Adobe Advertising rastreie um evento de conversão que ocorre em uma página que não é a página inicial. A solução ITP 2.2 armazena o cookie de um usuário no armazenamento local em um iFrame de propriedade do anunciante. O armazenamento local pode manter o valor do cookie do downstream de clique para a página de conversão.

Use a tag de mapeamento de conversão para garantir que o Adobe Advertising possa rastrear todas as conversões que ocorrem nos navegadores Apple Safari e Mozilla Firefox, que limitam a persistência de cookies primários. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

Para usar a tag de mapeamento de conversão:

1. [Implante a marca de mapeamento de conversão](#deploy-conversion-mapping-tag).

1. Se sua organização usa várias IDs de organização do Serviço de identidade da Adobe Experience Cloud (antes chamadas de IDs de organização IMS), [atualize suas tags de conversão](#update-conversion-tags) para incluir a ID de organização.

1. [Validar a implantação da marca](#validate-conversion-mapping).

## Implante a tag de mapeamento de conversão do JavaScript para ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Se estiver usando a marca de mapeamento de conversão do JavaScript para ITP 2.0, substitua a marca existente em todas as páginas de conversão por uma das seguintes marcas.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Se sua organização usar uma única ID de organização, que é usada para sua conta do Search, Social e Commerce, use a seguinte tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  onde você substitui `{AMO User ID}` pela ID de usuário exclusiva da sua conta do Search, Social e Commerce.

* Se sua organização usar várias IDs de organização, use a seguinte tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  em que:

   * você substitui o valor `{xxxxxx@AdobeOrg}` pela ID da organização para a qual as conversões da página são rastreadas. Use a mesma ID de organização para todas as páginas de conversão.

   * você substitui `{AMO User ID}` pela ID de usuário exclusiva da sua conta do Search, Social e Commerce.

* Se você estiver usando um sistema de gerenciamento de tags que não oferece suporte à adição da variável `imsorgid` à tag de script, use o seguinte código:

  *Se sua organização usar uma única ID de organização:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  onde você substitui `{AMO User ID}` pela ID de usuário exclusiva da sua conta do Search, Social e Commerce.

   * Se sua organização usar várias IDs de organização:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     em que:

      * você substitui o valor `{xxxxxx@AdobeOrg}` pela ID da organização para a qual as conversões da página são rastreadas. Use a mesma ID de organização para todas as páginas de conversão.

      * você substitui `{AMO User ID}` pela ID de usuário exclusiva da sua conta do Search, Social e Commerce.

Se você não souber o valor da ID da organização ou da ID de usuário de Pesquisa, Social e Commerce, pergunte à equipe de conta do Adobe.

### Exemplos

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Onde adicionar a tag

Adicione a tag em qualquer página que possa ser uma página de aterrissagem a partir de um clique de pesquisa (idealmente, em todas as páginas, já que as páginas de aterrissagem podem mudar com o tempo). Ele deve ser carregado antes da tag de rastreamento de conversão do Adobe Advertising JavaScript v3.

Se for colocado em um iframe ou tag container, então:

* O iframe deve estar no mesmo nível que o domínio de nível superior.

* A tag de mapeamento de conversão deve estar somente um (1) nível abaixo do domínio de nível superior.

## Atualizar as tags de conversão do JavaScript {#update-conversion-tags}

Se sua organização usar várias IDs de organização, adicione a ID de organização para a qual as conversões de uma página são rastreadas às suas tags de conversão do JavaScript existentes.

Se sua organização usar uma ID de organização, essa etapa não será necessária.

### Tags do JavaScript V2

Adicione a seguinte string no início da tag do script de conversão:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

onde você substitui o valor `{xxxxxx@AdobeOrg}` pela ID da organização para a qual as conversões da página são rastreadas.

Exemplo:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### Tags do JavaScript V3

Depois que `window.EF` for definido, adicione a seguinte cadeia de caracteres:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

onde você substitui o valor `{xxxxxx@AdobeOrg}` pela ID da organização para a qual as conversões da página são rastreadas.

Exemplo:

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
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## Validar a implantação de tags {#validate-conversion-mapping}

Peça ajuda à sua equipe de conta do Adobe para validar a tag de mapeamento de conversão e a tag de conversão regular (se você a atualizou).
