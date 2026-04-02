---
title: Usando a biblioteca  [!DNL Last Event Service] JavaScript com [!DNL Web SDK]
description: Saiba mais sobre as etapas para alternar do uso da biblioteca  [!DNL Analytics] [!DNL visitorAPI] para a biblioteca  [!DNL Experience Platform] [!DNL Web SDK] na sua implementação do  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# Usando a biblioteca JavaScript [!DNL Last Event Service] com o Adobe Experience Platform [!DNL Web SDK]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Se sua organização usar a biblioteca herdada do Adobe Analytics `visitorAPI.js` para coleta de dados, você poderá, opcionalmente, mudar para a biblioteca do [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR) (`alloy.js`), que permite a interação com os vários serviços da Experience Cloud por meio do [!DNL Edge Network].

A biblioteca JavaScript do [!DNL Analytics for Advertising] [!DNL Last Event Service], como está, registra eventos de view-through e click-through e os une às conversões associadas usando uma ID complementar (`SDID`). No entanto, a biblioteca [!DNL Web SDK] não fornece um [!DNL stitch ID]. Para usar o [!DNL Web SDK] para [!DNL Analytics for Advertising], você deve modificar 1) a tag [!DNL Last Event Service] que você usa em suas páginas da Web e 2) seus comandos [!DNL Web SDK] `sendEvent` adequadamente.

## Etapa 1: edite sua tag [!DNL Last Event Service] para gerar um `[!DNL StitchID]`

Na tag [!DNL Analytics for Advertising] [!DNL Last Event Service] usada em suas páginas da Web, adicione o código para gerar o `[!DNL StitchID]` usando o gerador de ID aleatório fornecido na biblioteca.

**Marca herdada:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nova marca:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Etapa 2: usar [!DNL Web SDK] para enviar o [!DNL StitchID] como dados XDM para [!DNL Analytics]

Insira a seguinte propriedade no comando [!DNL Web SDK] `sendEvent` para enviar [!DNL StitchID] para [!DNL Experience Edge] como dados [!DNL Experience Data Model] (XDM) de [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] usa o valor como um `SDID`.

**Propriedade a ser adicionada:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exemplo:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
