---
title: Métricas de Adobe Advertising no Analysis Workspace
description: Métricas de Adobe Advertising no Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Métricas de Adobe Advertising no Analysis Workspace

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

>[!NOTE]
>
>* O Adobe Advertising transmite métricas e dimensões de tráfego para [!DNL Analytics] diariamente.
>* [!DNL Analytics] captura click-throughs e view-throughs Adobe Advertising em tempo real.
>* Para [!DNL Search, Social, & Commerce], esse recurso tem suporte para a maioria das redes de anúncios e tipos de campanha. Consulte &quot;[Inventário com Suporte](/help/search-social-commerce/introduction/supported-inventory.md)&quot; no Guia do [!DNL Search, Social, & Commerce] para obter mais informações.

## Métricas de tráfego do Adobe Advertising

As métricas de tráfego de Adobe Advertising em [!DNL Analytics] geralmente começam com &quot;Adobe Advertising&quot;, exceto por &quot;[!UICONTROL AMO ID Instances]&quot;. No entanto, para clientes de longo prazo que usaram um evento personalizado (em vez de um evento reservado) para criar originalmente métricas para cliques, custo e impressões, essas métricas ainda começam com &quot;AMO&quot;.

| Métrica de tráfego | Descrição |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] ou (alguns clientes herdados) [!UICONTROL AMO Clicks] | O número total de cliques em Adobe Advertising. |
| [!UICONTROL Adobe Advertising Cost] ou (alguns clientes herdados) [!UICONTROL AMO Cost] | O Adobe Advertising gasto na moeda do conjunto de relatórios. |
| [!UICONTROL Adobe Advertising Impressions] ou (alguns clientes herdados) [!UICONTROL AMO Impressions] | O número de impressões de Adobe Advertising. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | O número de impressões servidas para as quais a instrumentação de visibilidade foi inicializada com êxito. Esse valor é calculado como (impressões instrumentadas - o número de impressões não mensuráveis). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | O número de minutos durante os quais um vídeo de Adobe Advertising foi exibido. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | O número de impressões que foram determinadas como não visíveis. Este valor é calculado como ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | O número de impressões medidas para serem visualizadas de acordo com a configuração de posicionamento. |
| [!UICONTROL Adobe Advertising Views] | O número de visualizações em um anúncio. Uma exibição é contada quando o visualizador inicia o vídeo do Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | O número de visualizações para as quais pelo menos 25% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | O número de visualizações para as quais pelo menos 50% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | O número de visualizações para as quais pelo menos 75% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | O número de visualizações para as quais 100% de um vídeo de Adobe Advertising foi assistido. |
| [!UICONTROL AMO ID Instances] | O número de vezes que [!UICONTROL AMO ID] foi definido. |

## Dimension Adobe Advertising

>[!NOTE]
>
>Todas as dimensões de Adobe Advertising em [!DNL Analytics] são seguidas por &quot;[!DNL (AMO ID)]&quot;.

| Dimensão | Dados de Adobe Advertising aplicáveis | Descrição |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | Advertising DSP ou o nome do mecanismo de pesquisa |
| [!UICONTROL Account (AMO ID] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | O nome da conta. |
| [!UICONTROL Network (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | RTB ([!DNL DSP]) ou o nome da rede de publicidade ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | O nome da campanha. |
| [!UICONTROL Optimization (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | O nome do pacote ([!DNL DSP]) ou do portfólio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | Dados de [!DNL DSP] | O nome do posicionamento. |
| [!UICONTROL Ad Group (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | O nome do grupo de anúncios. |
| [!UICONTROL Keyword (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | A palavra-chave. |
| [!UICONTROL Match Type (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | O tipo de correspondência da pesquisa. |
| [!UICONTROL Keyword Match Type (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | A palavra-chave e o tipo de correspondência. |
| [!UICONTROL Ad Type (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | O tipo de anúncio, como `text`, `video`, `display` ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | O tipo de anúncio ([!DNL DSP]) ou o título do anúncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | A descrição do anúncio ([!DNL DSP]) ou o corpo do anúncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | O URL exibido no anúncio. |
| [!UICONTROL Ad Destination URL (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | O URL de destino do anúncio. |
| [!UICONTROL Landing Type (AMO ID)] | Dados de [!DNL DSP] e [!DNL Search, Social, & Commerce] | Se a entrada da página de aterrissagem era uma visualização ou um click-through. |
| [!UICONTROL Product Target (AMO ID)] | Dados de [!DNL Search, Social, & Commerce] | O público alvo do produto para um anúncio de lista de produtos. |

## Métricas calculadas personalizadas úteis do Adobe Advertising

Considere a criação das seguintes métricas para seus dados de Adobe Advertising.

* Cliques para a instância da página de aterrissagem ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): esta é a % de pessoas que clicaram no anúncio e o direcionaram para a página de aterrissagem.
* Taxa Mensurável ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Taxa de Impressão Visível ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Custo por visualização ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Custo por clique ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
