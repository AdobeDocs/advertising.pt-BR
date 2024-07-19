---
title: Perguntas frequentes sobre a conversão de Adobe Advertising e as tags de rastreamento de exibição de página
description: Consulte uma comparação das tags de rastreamento de conversão de Adobe Advertising e exibição de página.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Perguntas frequentes sobre a conversão de Adobe Advertising e as tags de rastreamento de exibição de página

O seguinte se aplica às tags de rastreamento de conversão Adobe Advertising e às tags de rastreamento de exibição de página.

| | Tags JS com ECID | Tags da versão 3 do JS | Tags do JS versão 2 | Tags de imagem |
| ---- | ---- | ---- | ---- | ---- |
| Pode ser usado na mesma página da Web que outra versão do JS | — | — | — | n/d |
| Permite o uso de várias tags com as mesmas IDs de usuário do anunciante na mesma página da Web | Sim | Sim | Sim | — |
| Permite o uso de várias tags com diferentes IDs de usuário anunciante na mesma página da Web | Sim | Sim | Não | Não |
| Usado pela extensão Adobe Advertising para Adobe Experience Platform e compatível com outras tags geradas usando o Experience Platform | Sim | Sim | — | — |
| Permite que todas as conversões originadas de [!DNL Apple Safari] e [!DNL Mozilla Firefox] sejam rastreadas quando usadas com a tag de mapeamento de conversão Adobe Advertising JavaScript | Sim | Sim | Sim | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Todas as novas implementações usam o JavaScript versão 3.
>* A marca JavaScript com ECID usa o [Serviço da Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html), bem como a ef_id e gsurferid herdadas para medir as conversões. Esta tag mais recente cria [cookies próprios s_ecid de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) e fornece uma integração mais estreita com outros produtos de Experience Cloud.
>* Use as tags do JavaScript versão 2 somente quando elas já estiverem implementadas nas páginas da Web do anunciante.
>* A prática recomendada é usar tags do JavaScript em vez de tags de imagem, a menos que o site tenha uma política contra sua utilização.
>* As tags da JavaScript são necessárias para anunciantes que desejam direcionar públicos-alvo criados no Adobe Experience Cloud, criados no Adobe Audience Manager ou publicados no Adobe Experience Cloud a partir do Audience Manager ou do Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma marca de conversão de Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
