---
title: Usando a  [!DNL Last Event Service] Biblioteca da JavaScript com [!DNL Web SDK]
description: Saiba mais sobre as etapas para alternar do uso da biblioteca  [!DNL Analytics] [!DNL visitorAPI] para a biblioteca  [!DNL Experience Platform] [!DNL Web SDK] na sua implementação do  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Usando a Biblioteca JavaScript [!DNL Last Event Service] com o Adobe Experience Platform [!DNL Web SDK]

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

Se a sua organização usar a biblioteca herdada do Adobe Analytics `visitorAPI.js` para coleta de dados, você poderá, opcionalmente, mudar para a biblioteca [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`), que permite a você interagir com os vários serviços Experience Cloud por meio do [!DNL Edge Network].

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

## Etapa 2: usar [!DNL Web SDK] para enviar [!DNL StitchID] como Dados XDM para [!DNL Analytics]

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
