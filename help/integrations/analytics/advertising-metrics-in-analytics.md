---
title: Métricas de publicidade Adobe no Analysis Workspace
description: Métricas de publicidade Adobe no Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Métricas de publicidade Adobe no Analysis Workspace

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

>[!NOTE]
>
>* O Adobe Advertising passa métricas e dimensões de tráfego para o [!DNL Analytics] diariamente.
>* [!DNL Analytics] captura click-throughs e view-throughs de publicidade em Adobe em tempo real.
   > Para [!DNL Search, Social, & Commerce], esse recurso é compatível com a maioria das redes de anúncios e tipos de campanha. Consulte &quot;Inventário suportado&quot; no [!DNL Search, Social, & Commerce] Guia para obter mais informações.<!-- add link when that's published in ExL -->


## Métricas de tráfego da publicidade de Adobe

>[!NOTE]
>
>Todas as métricas de tráfego de publicidade de Adobe no [!DNL Analytics] comece com &quot;AMO&quot;.

| Métrica de tráfego | Descrição |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | O número de impressões de Anúncios Adobe. |
| [!UICONTROL AMO Clicks] | O número total de cliques de anúncio de Adobe. |
| [!UICONTROL AMO Cost] | O Adobe Anúncios gastos na moeda do conjunto de relatórios. |
| [!UICONTROL AMO ID Instance] | O número de vezes que a ID de anúncio do Adobe foi definida. |
| [!UICONTROL AMO Minutes Viewed] | O número de minutos em que um vídeo de Adobe Advertising foi visualizado. |
| [!UICONTROL AMO Views] | O número de visualizações em um anúncio. Uma exibição é contada quando o visualizador inicia o vídeo de anúncio de Adobe. |
| [!UICONTROL AMO Views 25% Complete] | O número de visualizações para as quais pelo menos 25% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 50% Complete] | O número de visualizações para as quais pelo menos 50% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 75% Complete] | O número de visualizações para as quais pelo menos 75% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO Views 100% Complete] | O número de visualizações para as quais 100% de um vídeo de Publicidade de Adobe foi assistido. |
| [!UICONTROL AMO Viewable Impressions] | O número de impressões medidas para serem visualizadas de acordo com a configuração de posicionamento. |
| [!UICONTROL AMO Not Viewable Impressions] | O número de impressões que foram determinadas como não visíveis. Esse valor é calculado como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | O número de impressões servidas para as quais a instrumentação de visibilidade foi inicializada com êxito. Esse valor é calculado como (impressões instrumentadas - o número de impressões não mensuráveis). |

## Dimension de publicidade Adobe

>[!NOTE]
>
>Todas as dimensões de publicidade do Adobe em [!DNL Analytics] são seguidos por &quot;(ID AMO)&quot;.

| Dimension | Dados de publicidade do Adobe aplicáveis | Descrição |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | DSP de publicidade ou o nome do mecanismo de pesquisa |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | O nome da conta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | SRT ([!DNL DSP]) ou o nome da rede de publicidade ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | O nome da campanha. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | O pacote ([!DNL DSP]) ou portfólio ([!DNL Search, Social, & Commerce]) nome. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] dados | O nome do posicionamento. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] dados | O nome do grupo de anúncios. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] dados | A palavra-chave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] dados | O tipo de correspondência da pesquisa. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] dados | A palavra-chave e o tipo de correspondência. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | O tipo de anúncio, como `text`, `video`, `display`ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | O tipo de anúncio ([!DNL DSP]) ou título do anúncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | A descrição do anúncio ([!DNL DSP]) ou corpo do anúncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] dados | O URL exibido no anúncio. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] dados | O URL de destino do anúncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dados | Se a entrada da página de aterrissagem era uma visualização ou um click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] dados | O público alvo do produto para um anúncio de lista de produtos. |

## Métricas calculadas personalizadas úteis para publicidade em Adobe

Considere a criação das seguintes métricas para seus dados de anúncio de Adobe.

* Cliques para a instância da página inicial ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): esta é a % de pessoas que clicaram no anúncio e o direcionaram para a página inicial.
* Taxa Mensurável ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Taxa de impressão visível ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Custo por visualização ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Custo por clique ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dados em publicidade de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

