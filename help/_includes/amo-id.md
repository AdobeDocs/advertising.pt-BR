---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# IDs do Adobe Advertising AMO

## IDs do Adobe Advertising AMO {#amo-id}

A ID do AMO rastreia cada combinação única de anúncios em um nível menos granular e é usada para a classificação de dados do [!DNL Analytics] e do Customer Journey Analytics, além da assimilação de métricas de publicidade (como impressões, cliques e custo) do Adobe Advertising.

Para [!DNL Analytics], a ID do AMO é armazenada em uma [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou dimensão de rVar (ID do AMO).

Para o Customer Journey Analytics, a ID do AMO é armazenada na propriedade `trackingCode` do objeto `conversionDetails`, que faz parte do [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é pronunciado como &quot;[!DNL squid]&quot;.
