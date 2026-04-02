---
title: Dados do [!DNL Analytics] no Adobe Advertising
description: Dados do [!DNL Analytics] no Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
TQID: https://experienceleague.adobe.com/Op96b-n8lH2vLwBfUjlJdunp65Y5o2-gYxaEWFwH2m8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 0%

---

# Dados do [!DNL Analytics] no Adobe Advertising

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

## Segmentos do Analytics

Todos os segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

Os novos segmentos levam de 24 a 48 horas para serem exibidos no Adobe Advertising. As atualizações de segmentos existentes são sincronizadas em cerca de oito horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de engajamento do site

>[!NOTE]
>
>* [!DNL Analytics] passa eventos para EF ID [!DNL eVar] para o Adobe Advertising.  A integração padrão não oferece suporte ao envio de métricas calculadas ou outras dimensões ([!DNL eVars]) para o Adobe Advertising. No entanto, se a métrica calculada puder ser totalmente capturada em um evento personalizado, o Adobe Advertising poderá assimilar o evento personalizado.
>* [!DNL Analytics] passa dados para o Adobe Advertising de hora em hora.

* [!UICONTROL Timespent_secs_1stvisit]: o número de segundos gastos no site durante a primeira visita.
* [!UICONTROL Timespent_secs_total]: o número total de segundos gastos no site em todas as visitas na janela de retrospectiva de cliques.
* [!UICONTROL Pageviews_1stvisit]: o número de exibições de página no site durante a primeira visita.
* [!UICONTROL Pageviews_total]: o número total de exibições de página no site em todas as visitas na janela de retrospectiva de cliques.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=pt-BR)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=pt-BR)
* [!UICONTROL ef_id_instances]: O número de vezes que [!DNL Analytics] coletou um [!UICONTROL EF ID].

## Métricas de conversão

[!DNL Analytics] passa métricas de conversão para o Adobe Advertising diariamente.

### Métricas de conversão padrão

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=pt-BR)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=pt-BR)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=pt-BR)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=pt-BR)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=pt-BR)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=pt-BR)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=pt-BR)

### Métricas de conversão personalizadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

### Métricas de conversão personalizadas criadas de [!DNL eVars] e [!DNL Props]

As métricas disponíveis variam para cada cliente. Consulte &quot;[Criar Métricas de Conversão do Adobe Analytics [!DNL eVars] and [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;.

### Métricas de conversão reservadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Métricas do Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
