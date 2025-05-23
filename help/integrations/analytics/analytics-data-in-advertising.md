---
title: '[!DNL Analytics] Dados no Adobe Advertising'
description: '[!DNL Analytics] Dados no Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] Dados no Adobe Advertising

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

## Segmentos do Analytics

Todos os segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

Novos segmentos levam de 24 a 48 horas para serem exibidos no Adobe Advertising. As atualizações de segmentos existentes são sincronizadas em cerca de oito horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de engajamento do site

>[!NOTE]
>
>* [!DNL Analytics] passa eventos para EF ID [!DNL eVar] para Adobe Advertising.  A integração padrão não oferece suporte ao envio de métricas calculadas ou outras dimensões ([!DNL eVars]) para o Adobe Advertising. No entanto, se a métrica calculada puder ser totalmente capturada em um evento personalizado, o Adobe Advertising poderá assimilar o evento personalizado.
>* [!DNL Analytics] passa dados para Adobe Advertising por hora.

* [!UICONTROL Timespent_secs_1stvisit]: o número de segundos gastos no site durante a primeira visita.
* [!UICONTROL Timespent_secs_total]: o número total de segundos gastos no site em todas as visitas na janela de retrospectiva de cliques.
* [!UICONTROL Pageviews_1stvisit]: o número de exibições de página no site durante a primeira visita.
* [!UICONTROL Pageviews_total]: o número total de exibições de página no site em todas as visitas na janela de retrospectiva de cliques.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=pt-BR)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=pt-BR)
* [!UICONTROL ef_id_instances]: O número de vezes que [!DNL Analytics] coletou um [!UICONTROL EF ID].

## Métricas de conversão

[!DNL Analytics] passa métricas de conversão para Adobe Advertising diariamente.

### Métricas de conversão padrão

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=pt-BR)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=pt-BR)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=pt-BR)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=pt-BR)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=pt-BR)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=pt-BR)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=pt-BR)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=pt-BR)

### Métricas de conversão personalizadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

### Métricas de Conversão Personalizadas Criadas de [!DNL eVars] e [!DNL Props]

As métricas disponíveis variam para cada cliente. Consulte &quot;[Criar Métricas de Conversão do Adobe Analytics [!DNL eVars] and [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;.

### Métricas de conversão reservadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Métricas de Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
