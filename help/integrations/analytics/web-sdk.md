---
title: Usar o [!DNL Last Event Service] Biblioteca JavaScript com [!DNL Web SDK]
description: Saiba mais sobre as etapas para alternar usando o [!DNL Analytics] [!DNL visitorAPI] para a [!DNL Experience Platform] [!DNL Web SDK] biblioteca para seu [!DNL Analytics for Advertising] execução.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Usar o [!DNL Last Event Service] Biblioteca JavaScript com Adobe Experience Platform [!DNL Web SDK]

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

Se sua organização usar o Adobe Analytics herdado `visitorAPI.js` para coleta de dados, você pode, opcionalmente, mudar para usando a [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) biblioteca (`alloy.js`), que permite interagir com os vários serviços de Experience Cloud por meio da [!DNL Edge Network].

A variável [!DNL Analytics for Advertising] [!DNL Last Event Service] A biblioteca do JavaScript do, como está, registra eventos de view-through e click-through e os une às conversões associadas usando uma ID complementar (`SDID`). A variável [!DNL Web SDK] no entanto, a biblioteca não fornece uma [!DNL stitch ID]. Para usar o [!DNL Web SDK] para [!DNL Analytics for Advertising], será necessário modificar 1) a [!DNL Last Event Service] tag que você usa nas páginas da Web e 2) sua [!DNL Web SDK] `sendEvent` comandos adequadamente.

## Etapa 1: Editar o [!DNL Last Event Service] Tag para gerar um `[!DNL StitchID]`

No [!DNL Analytics for Advertising] [!DNL Last Event Service] tag usada nas páginas da Web, adicione o código para gerar a `[!DNL StitchID]` usando o gerador de ID aleatório que está empacotado na biblioteca.

**Tag herdada:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Nova tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Etapa 2: Uso [!DNL Web SDK] para enviar o [!DNL StitchID] como dados XDM para [!DNL Analytics]

Insira a seguinte propriedade em seu [!DNL Web SDK] `sendEvent` comando para enviar a [!DNL StitchID] para [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) para [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] usará o valor como um `SDID`.

**Propriedade a adicionar:**

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
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

