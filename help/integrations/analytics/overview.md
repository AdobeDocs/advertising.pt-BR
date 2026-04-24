---
title: Visão geral de  [!DNL Analytics for Advertising]
description: Visão geral de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
TQID: https://experienceleague.adobe.com/OHxJO1mtbzOtt5oGDJF26xSuVLG-HnRDdIGDrUH2pzk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1306
ht-degree: 0%

---

# Visão geral do [!DNL Analytics for Advertising]

*Anunciantes com Advertising Creative, Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O [!DNL Analytics for Advertising] integra o Adobe Analytics e o Adobe Advertising para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem interações do site de click-through e view-through em suas instâncias do [!DNL Analytics], permitindo que as marcas vejam como seus gastos com publicidade levam ao engajamento do site e aos objetivos comerciais críticos.

Além disso, o Adobe Advertising pode acessar os vastos dados primários que o [!DNL Analytics] coleta usando as tags do [!DNL Analytics] já existentes no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. A Adobe Advertising pode usar ainda mais os dados do [!DNL Analytics] para otimização de gastos e ofertas.

Quando adequadamente empregado, o [!DNL Analytics for Advertising] ofusca as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e compreensão desse engajamento do site por meio da análise da Web.

Principais benefícios:

* Envie [!DNL Analytics] segmentos diretamente para a Adobe Advertising para remarketing de site próprio.
* Use [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Aproveite o Analysis Workspace [!DNL Analytics] para entender melhor os pontos de entrada do site e o comportamento da visita.
* Permita uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Use IDs de view-through e click-through persistentes do Adobe Advertising no [!DNL Analytics] para entender o engajamento do site.
* Aprimore os relatórios tradicionais de mídia paga no Analysis Workspace com métricas, dimensões e atividades do site personalizadas que não são viáveis ao exportar dados ou pixels para servidores de publicidade ou outros DSPs.
* Aproveite o código [!DNL Analytics] que já está no seu site para rastreamento e otimização no Adobe Advertising.

>[!TIP]
>
> Watch a [video introduction to [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Using Analytics for paid media reporting

[!DNL Analytics for Advertising] improves reporting and insight on how your advertising drives site behavior by allowing you to:

* Use IDs de view-through e click-through persistentes do Adobe Advertising no [!DNL Analytics] para entender o engajamento do site.
* Take advantage of Analysis Workspace to better understand site entry points and visit behavior. You can access paid media dimensional and event data, which include Adobe Advertising campaign entity names (down to placements and ads) and their associated metrics, such as clicks, impressions, and cost.

To use [!DNL Analytics] as your paid media reporting tool, your organization needs an Adobe CX Enterprise (formerly Adobe Experience Cloud) login with access to Analysis Workspace. Your Adobe Advertising team will help you to map your Adobe Advertising data to individual report suites in Analysis Workspace. You can send Adobe Advertising data to any report suite, but you should be aware of the report suites that have been mapped to Adobe Advertising and those that haven&#39;t. Depending on the report suite, this may change the data reported.

[Adobe Advertising IDs within [!DNL Analytics]](ids.md) work like other [!DNL eVars], with a custom, persistent expiration. By default, the attribution lookback window is set to 60 days during the Adobe Advertising implementation. To change this setting, work with your Adobe Account Team.

Adobe Advertising dimensions are appended with the suffix &quot;(AMO ID)&quot; (such as &quot;Ad Type (AMO ID)&quot;). See &quot;[Adobe Advertising Metrics in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; for a list of the available dimensions.

>[!NOTE]
>
> When you view Adobe Advertising data (or any data set) within [!DNL Analytics], be aware that metrics and reports are based on the rules that are set within [!DNL Analytics]. The data could be different than what you see within other reporting systems, such as ad server reports, [!DNL DSP] reports, or search engine reports. To understand the data differences in [!DNL Analytics], you need to know when [!DNL eVar] data expires, what defines a visit, what is considered last touch attribution versus total persisting attribution, and other factors. For more information, see [Expected data variances between [!DNL Analytics] and Adobe Advertising](data-variances.md).

## Using Analytics to power Adobe Advertising campaigns and portfolios

Without requiring any additional pixels, [!DNL Analytics for Advertising] enables better optimization and easier audience segmentation by sending two main signals to Adobe Advertising:

* Conversion metrics to be used as bid signals:
   * standard metrics, such as [!UICONTROL Revenue] and [!UICONTROL Cart Views].
   * site engagement metrics, such as page view and visit metrics.
   * custom revenue metrics.
   * métricas de receita reservadas.
* Segmentos criados em [!DNL Analytics] e publicados no CX Enterprise.

  Você pode usar [!DNL Analytics] segmentos para redirecionamento de site próprio em [!DNL DSP], [!DNL Creative] e anúncios de pesquisa pagos.

  ([!DNL Search, Social, & Commerce] somente) Anunciantes com [!DNL Analytics], mas não com o Audience Manager, também podem criar públicos com base em marcas de site da Google (listas de remarketing) e públicos com correspondência de clientes (listas de clientes) de [!DNL Analytics] segmentos que são compartilhados com o CX Enterprise.

### Métricas de conversão do site como sinais de oferta

Você pode usar seus eventos padrão e personalizados do [!DNL Analytics] para criar objetivos ponderados no Adobe Advertising. Os objetivos informam as decisões de licitação para seus pacotes do [!DNL DSP] e portfólios de Pesquisa, Social e Commerce.

Para campanhas de [!DNL Google Ads] e [!DNL Google Microsoft Advertising] em portfólios híbridos de Pesquisa, Social e Commerce, você pode, opcionalmente, fazer upload dos objetivos — incluindo quaisquer eventos [!DNL Analytics] nos objetivos — diretamente para as redes de anúncios, onde eles ficam disponíveis como ações de conversão para metas de conversão personalizadas a nível de conta e de campanha.

>[!NOTE]
>
> Você não pode mapear métricas calculadas de [!DNL Analytics] para o Adobe Advertising.

A equipe do Adobe Advertising ajudará você a identificar e mapear os eventos aplicáveis ao desempenho de mídia paga no Adobe Advertising.

Consulte &quot;[Métricas do Analytics no Adobe Advertising](analytics-data-in-advertising.md)&quot; para obter uma lista das métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

A Adobe Advertising pode assimilar [!DNL Analytics] segmentos para fins de remarketing para os anúncios [!DNL Creative], [!DNL DSP] e [!DNL Search, Social, & Commerce] usando a integração nativa de Públicos-alvo da CX Enterprise entre o [!DNL Analytics] e a CX Enterprise.

Para acessar os segmentos [!DNL Analytics], uma conta de anunciante deve habilitar o [Serviço de Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). Quando o Serviço de ID está ativado, todos os segmentos do CX Enterprise ficam disponíveis no Adobe Advertising assim que são processados. Os segmentos do CX Enterprise incluem segmentos criados no [!DNL Analytics] e publicados no CX Enterprise, segmentos criados no Adobe Audience Manager, segmentos criados no CX Enterprise usando o [!DNL People core service] e segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager.

[!DNL Analytics] segmentos estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço CX Enterprise Audiences, consulte [CX Enterprise Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemplos de como usar a integração do {#integration-examples}

### Uso de dados do Adobe Advertising no Analysis Workspace

Para saber como você pode usar os dados do Adobe Advertising para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Uso de conversões de view-through de TV conectada em relatórios

*Somente usuários do Advertising DSP*

Você pode medir a eficácia do funnel completo de suas campanhas de TV conectada (CTV) vinculando a exposição de anúncios em dispositivos de CTV a conversões no site. O novo filtro [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; divide as conversões em linhas separadas para valores [!UICONTROL Click Through], [!UICONTROL View Through] e [!UICONTROL View Through (CTV)].

Para visualizar suas métricas de conversão de view-through de CTV, use a exibição Disposição ou a exibição Canal de marketing no Analysis Workspace.

Uso da exibição de Posicionamento:

1. Incluir posicionamentos de gastos com CTV na exibição de relatório.

1. Inclua as métricas desejadas, como &quot;Impressões&quot;, &quot;Cliques&quot; e assim por diante.

1. Aplique os seguintes filtros:

   Plataforma de publicidade: `Advertising Cloud DSP`

   Página de aterrissagem: `View-Through (CTV)`

Uso da exibição Canal de marketing:

1. Incluir a dimensão `Marketing Channel`.

1. Inclua as métricas desejadas, como &quot;Impressões&quot;, &quot;Cliques&quot; e assim por diante.

1. Aplique os seguintes filtros:

   Plataforma de publicidade: `Advertising Cloud DSP`

   Página de aterrissagem: `View-Through (CTV)`

### Criação de painéis do Adobe Advertising

Para saber como você pode acompanhar seus dados do Adobe Advertising em relação às suas metas no Analysis Workspace, assista ao vídeo &quot;[Criar painéis do Adobe Advertising com o Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Uso da Adobe Advertising ID para análise de entrada de site

Para saber como criar um relatório de entrada de site do Adobe Advertising para monitorar influências de dia da semana, hora do dia, navegador e geográficas, assista ao vídeo &quot;[Criar relatórios de entrada de site do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

## Como iniciar uma implementação do [!DNL Analytics for Advertising]

Entre em contato com a equipe de conta da Adobe, que concluirá a configuração inicial necessária para começar e ajudará você a planejar a implementação e o uso de dados com base nas necessidades da organização.

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising IDs usadas pelo Analytics](ids.md)
>* [Código JavaScript do Analytics para Advertising](/help/integrations/analytics/javascript.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](data-variances.md)
>* [Métricas do Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
