---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# IDs EF do Adobe Advertising

## IDs EF do Adobe Advertising

A ID de EF é um token exclusivo que o Adobe Advertising usa para associar a atividade a um clique ou exposição de anúncios online em um navegador ou dispositivo individual. As EF IDs atuam principalmente como chaves para enviar dados do [!DNL Analytics] e dados do Customer Journey Analytics para a Adobe Advertising para otimização de relatórios e ofertas no Adobe Advertising.

Para [!DNL Analytics], a ID EF é armazenada em [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (reservada [!DNL eVar]) dimensão (ID EF Adobe Advertising).

Para o Customer Journey Analytics, a ID EF é armazenada na propriedade `trackingIdentities` do objeto `conversionDetails`, que faz parte de [o [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### Formatos de ID EF {#ef-id-formats}

Consulte os [formatos dos itens de dimensão da EF ID](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items) no &quot;Guia de Componentes do Adobe Analytics&quot;.

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma implementação do [!DNL Analytics] ou do Customer Journey Analytics forçar o rastreamento de URL em minúsculas, o Adobe Advertising não reconhecerá a EF ID. Isso afeta os lances e os relatórios da Adobe Advertising, mas não afeta os relatórios do Adobe Advertising no [!DNL Analytics] ou na Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
