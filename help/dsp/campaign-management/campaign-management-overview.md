---
title: Visão geral do gerenciamento de campanhas no Advertising DSP
description: Saiba mais sobre a hierarquia e os componentes do gerenciamento de campanhas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464aid: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Visão geral do gerenciamento de campanhas no Advertising DSP

As campanhas do DSP têm a seguinte hierarquia:

* Campaign
   * Pacote(s)
      * Posicionamento(s)
         * Anúncio(s)
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campanhas](/help/dsp/campaign-management/campaigns/campaign-about.md) são a estrutura abrangente das configurações de voo. Cada campanha é configurada com um anunciante, datas de início e término, um orçamento geral, uma opção de direcionamento entre dispositivos e limite de frequência padrão, além de opções de relatórios para visibilidade, fraude, segurança da marca e verificação de público-alvo. Todas as configurações no nível da campanha se aplicam automaticamente a cada pacote e posicionamento na campanha.

## [!UICONTROL Packages]

Cada campanha pode conter um ou mais [pacotes](/help/dsp/campaign-management/packages/package-about.md), cada um deles incluindo um conjunto de posicionamentos.

Use pacotes para agrupar disposições para entrega em um orçamento definido, meta de desempenho e estratégia de ritmo personalizada. A DSP otimiza os pacotes, transferindo os orçamentos para os posicionamentos de melhor desempenho no pacote. Você pode organizar pacotes por formato de posicionamento, tipo de inventário, provedor de dados, persona ou outras características distinguíveis.

Os pacotes são opcionais, mas são recomendados.

## [!UICONTROL Placements]

Um [posicionamento](/help/dsp/campaign-management/placements/placement-about.md) armazena parâmetros de direcionamento para um ou mais anúncios do mesmo tipo de anúncio. Você pode criar uma disposição para uma única campanha ou pacote e depois atribuir anúncios a ela.

## [!UICONTROL Ads]

[Anúncios](/help/dsp/campaign-management/ads/ad-about.md) incluem ativos criativos e URLs de rastreamento. É possível fazer upload de tags de veiculação de anúncios de terceiros individualmente ou em massa usando folhas de tags do parceiro ou o modelo de tag em massa. Você também pode criar manualmente anúncios de exibição nativos para o DSP veicular.

Depois que seus anúncios forem configurados, é necessário anexar cada anúncio a um posicionamento para começar a executá-lo. Você pode anexar um único anúncio a um ou mais posicionamentos.

Todos os anúncios ativos e aprovados em uma disposição ativa em uma campanha ativa estão qualificados para execução com base nos parâmetros de direcionamento de disposição.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de campanhas no Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Sobre o gerenciamento de pacotes no Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [Sobre o gerenciamento de posicionamento no Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [Sobre o gerenciamento de anúncios no Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de verificação de inicialização da campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipos de relatórios de desempenho em exibições de gerenciamento de campanhas](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gerenciar suas visualizações de dados de campanha](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Vídeo: estrutura de conta e interface de usuário do DSP](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
