---
title: '[!DNL Analytics] Dados no Adobe Advertising'
description: '[!DNL Analytics] Dados no Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: b382184072af88273570fc045d0bcebe24ed81fb
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# [!DNL Analytics] Dados no Adobe Advertising

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

## Segmentos do Analytics

Todos os segmentos criados no [!DNL Analytics] e publicado no Experience Cloud.

Novos segmentos levam de 24 a 48 horas para serem exibidos no Adobe Advertising. As atualizações de segmentos existentes são sincronizadas em cerca de oito horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de engajamento do site

>[!NOTE]
>
>* [!DNL Analytics] transmite eventos para o eVar EF ID para o Adobe Advertising.  A integração padrão não é compatível com o envio de métricas calculadas ou outras dimensões (eVars) para o Adobe Advertising. No entanto, se a métrica calculada puder ser totalmente capturada em um evento personalizado, o Adobe Advertising poderá assimilar o evento personalizado.
>* [!DNL Analytics] transmite dados para o Adobe Advertising por hora.

* [!UICONTROL Timespent_secs_1stvisit]: o número de segundos gastos no site durante a primeira visita.
* [!UICONTROL Timespent_secs_total]: o número total de segundos gastos no site em todas as visitas na janela de retrospectiva de cliques.
* [!UICONTROL Pageviews_1stvisit]: o número de exibições de página no site durante a primeira visita.
* [!UICONTROL Pageviews_total]: o número total de exibições de página no site em todas as visitas na janela de retrospectiva de cliques.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: o número de vezes que [!DNL Analytics] coletou um [!UICONTROL EF ID].

## Métricas de conversão

[!DNL Analytics] O transmite métricas de conversão para o Adobe Advertising diariamente.

### Métricas de conversão padrão

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Métricas de conversão personalizadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

### Métricas de conversão personalizadas criadas de eVars e Props

As métricas disponíveis variam para cada cliente. Consulte &quot;[Criar métricas de conversão a partir de eVars e props do Adobe Analytics](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Métricas de conversão reservadas

Essas métricas são específicas para o conjunto de relatórios, de modo que as métricas disponíveis variam para cada cliente e conjunto de relatórios.

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Métricas de Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
