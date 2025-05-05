---
title: Visão geral do Campaign Management no Advertising DSP
description: Saiba mais sobre a hierarquia e os componentes do gerenciamento de campanhas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Visão geral do Campaign Management no Advertising DSP

As campanhas de DSP têm a seguinte hierarquia:

* Campaign
   * Pacote(s)
      * Posicionamento(s)
         * Anúncio(s)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campanhas](/help/dsp/campaign-management/campaigns/campaign-about.md) são a estrutura abrangente das configurações de voo. Cada campanha é configurada com um anunciante, datas de início e término, um orçamento geral, uma opção de direcionamento entre dispositivos e limite de frequência padrão, além de opções de relatórios para visibilidade, fraude, segurança da marca e verificação de público-alvo. Todas as configurações no nível da campanha se aplicam automaticamente a cada pacote e posicionamento na campanha.

## [!UICONTROL Packages]

Cada campanha pode conter um ou mais [pacotes](/help/dsp/campaign-management/packages/package-about.md), cada um deles incluindo um conjunto de posicionamentos.

Use pacotes para agrupar disposições para entrega em um orçamento definido, meta de desempenho e estratégia de ritmo personalizada. O DSP otimiza os pacotes, transferindo os orçamentos para os posicionamentos de melhor desempenho no pacote. Você pode organizar pacotes por formato de posicionamento, tipo de inventário, provedor de dados, persona ou outras características distinguíveis.

Os pacotes são opcionais, mas são recomendados.

## [!UICONTROL Placements]

Um [posicionamento](/help/dsp/campaign-management/placements/placement-about.md) armazena parâmetros de direcionamento para um ou mais anúncios do mesmo tipo de anúncio. Você pode criar uma disposição para uma única campanha ou pacote e depois atribuir anúncios a ela.

## [!UICONTROL Ads]

[Anúncios](/help/dsp/campaign-management/ads/ad-about.md) incluem ativos criativos e URLs de rastreamento. É possível fazer upload de tags de veiculação de anúncios de terceiros individualmente ou em massa usando folhas de tags do parceiro ou o modelo de tag em massa. Você também pode criar manualmente anúncios de exibição nativos para o DSP atender.

Depois que seus anúncios forem configurados, é necessário anexar cada anúncio a um posicionamento para começar a executá-lo. Você pode anexar um único anúncio a um ou mais posicionamentos.

Todos os anúncios ativos e aprovados em uma disposição ativa em uma campanha ativa estão qualificados para execução com base nos parâmetros de direcionamento de disposição.

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Sobre o Gerenciamento de Pacotes](/help/dsp/campaign-management/packages/package-about.md)
>* [Sobre o Gerenciamento de Posicionamento](/help/dsp/campaign-management/placements/placement-about.md)
>* [Sobre o Gerenciamento de Anúncios](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de Verificação de Inicialização da Campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipos de Relatórios de Desempenho em Exibições do Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gerenciar As Visualizações De Dados Do Campaign](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Vídeo: Estrutura de Conta e Interface de Usuário do DSP](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=pt-BR)
