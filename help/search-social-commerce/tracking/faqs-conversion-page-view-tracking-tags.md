---
title: Perguntas frequentes sobre a conversão do Adobe Advertising e as tags de rastreamento de exibição de página
description: Consulte uma comparação das tags de rastreamento de conversão e exibição de página do Adobe Advertising.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ckLRjqXGTShwM2TTyULRKjPwL5RYVWkiVVSkwMmvxE8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 45b15880c20d516e4bab1ec664a45ebdf8ffbdcc
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 0%

---

# Perguntas frequentes sobre a conversão do Adobe Advertising e as tags de rastreamento de exibição de página

O seguinte se aplica às tags de rastreamento de conversão do Adobe Advertising e às tags de rastreamento de exibição de página.

| | Tags JS com ECID | Tags da versão 3 do JS | Tags do JS versão 2 | Tags de imagem |
| ---- | ---- | ---- | ---- | ---- |
| Pode ser usado na mesma página da Web que outra versão do JS | — | — | — | n/d |
| Permite o uso de várias tags com as mesmas IDs de usuário do anunciante na mesma página da Web | Sim | Sim | Sim | — |
| Permite o uso de várias tags com diferentes IDs de usuário anunciante na mesma página da Web | Sim | Sim | — | — |
| Usado pela extensão do Adobe Advertising para Adobe Experience Platform e compatível com outras tags geradas usando o Experience Platform | Sim | Sim | — | — |
| Permite que todas as conversões originadas de [!DNL Apple Safari] e [!DNL Mozilla Firefox] sejam rastreadas quando usadas com a marca de mapeamento de conversão do Adobe Advertising JavaScript | Sim | Sim | Sim | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Todas as novas implementações usam o JavaScript versão 3.
>* A marca JavaScript com ECID usa o [Serviço da Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html), bem como a ef_id e gsurferid herdadas para medir as conversões. Esta tag mais recente cria [cookies próprios s_ecid da CX Enterprise](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) e fornece uma integração mais estreita com outros produtos da CX Enterprise.
>* Use as tags do JavaScript versão 2 somente quando elas já estiverem implementadas nas páginas da Web do anunciante.
>* A prática recomendada é usar tags do JavaScript em vez de tags de imagem, a menos que o site tenha uma política contra sua utilização.
>* As tags da JavaScript são necessárias para anunciantes que desejam direcionar públicos-alvo criados na Adobe CX Enterprise, criados na Adobe Audience Manager ou publicados na Adobe CX Enterprise a partir da Audience Manager ou da Adobe Analytics.

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Gerar uma marca de conversão do Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
