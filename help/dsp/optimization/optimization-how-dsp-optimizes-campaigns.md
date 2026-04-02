---
title: Como o DSP otimiza suas campanhas
description: Saiba como a DSP otimiza os pacotes em suas campanhas.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
TQID: https://experienceleague.adobe.com/rSt1uwd3p4hawA3HHdgw2AL3fXeY36nbewI90YbFhaY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 679
ht-degree: 0%

---

# Como o Advertising DSP otimiza suas campanhas

Esta página descreve como o mecanismo de otimização do DSP, que é acionado pelo [!DNL Adobe AI], otimiza os pacotes em suas campanhas. Para obter dicas e truques sobre como otimizar manualmente suas campanhas, entre em contato com a equipe de conta da Adobe. <!-- add link to trading playbook if we add it to help -->

As metas de otimização de pacotes operam em dois níveis:

* Para cada pacote: o DSP aloca orçamento para cada posicionamento no pacote com base no desempenho do posicionamento em relação ao KPI selecionado.

* Para cada colocação/leilão do pacote: o DSP calcula o valor do KPI econômico em tempo real para cada leilão por colocação e usa esse valor para determinar o lance.

  >[!NOTE]
  >
  >O valor econômico pode ser pesadamente ponderado com base no quão bem uma colocação está gastando. Se uma colocação estiver por trás de sua meta de gastos, então é permitido comprar leilões de qualidade mais baixa. Se uma inserção estiver facilmente atingindo sua meta de gastos, o foco será transferido para leilões de maior qualidade.

## Otimização de pacote

O DSP pode otimizar sua entrega de duas maneiras fundamentais, com 20 variações disponíveis para se alinhar à sua meta específica de desempenho. Você pode optar por:

* Priorizar a taxa de desempenho

* Priorizar o equilíbrio entre a eficiência de custos e a taxa de desempenho

Consulte [Metas de otimização e como usá-las](optimization-goals.md) para determinar qual meta de otimização pode ajudá-lo a atingir seus KPIs.

### Pacotes que priorizam a taxa de desempenho

Para metas de otimização que priorizam a taxa de desempenho, a DSP prevê o desempenho de cada leilão e sempre dá lances no Lance máximo. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate] e assim por diante.

Esse modo de otimização funciona bem se:

* Você já conhece o nível de CPM efetivo/aceitável (por exemplo, um referencial histórico).

* Você está disposto a ajustar manualmente o [!UICONTROL Max Bid] para cada posicionamento se tiver desafios com o dimensionamento.

* Você está priorizando a escala em detrimento da eficiência.

#### Lógica de ritmo {#pacing-logic-performance}

* Se os gastos estiverem no ritmo, a licitação se torna mais seletiva para que você lance apenas em leilões previstos com altas taxas de desempenho.

* Se os gastos estiverem atrasados, a licitação se torna menos seletiva para que você lance em leilões previstos com taxas de desempenho mais baixas a fim de alcançar a meta de ritmo.

#### Limpando o sombreamento de preço/oferta {#clearing-price-performance}

Depois de executar a lógica de ritmo, o DSP executa a oferta proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima da taxa de vitória, então a oferta é diminuída de acordo com a previsão.

### Pacotes que priorizam o equilíbrio entre a eficiência de custos e a taxa de desempenho

Para algumas metas de otimização, a DSP prevê o desempenho de cada leilão e ajusta os preços de compra automaticamente, nunca excedendo o [!UICONTROL Max Bid] de uma disposição. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click] e assim por diante.

#### Lógica de ritmo {#pacing-logic-balanced}

* Se os gastos estiverem no ritmo, o DSP se tornará mais sensível ao preço, oferecendo valores menores para trocar a taxa de ganho com o plano de ritmo.

* Se uma métrica de desempenho também estiver sendo balanceada (todas as metas exceto [!UICONTROL Lowest CPM]), o KPI previsto será mesclado à quantidade oferecida. Portanto, você faz lances mais altos para leilões que se prevê terem melhor desempenho com base no &quot;custo por&quot;.

* Se os gastos estiverem atrasados, a DSP se tornará menos sensível ao preço e oferecerá valores mais altos, até [!UICONTROL Max Bid], para trocar a taxa de ganhos com o plano de ritmo.

#### Limpando o sombreamento de preço/oferta {#clearing-price-balanced}

Depois de executar a lógica de ritmo, o DSP executa a oferta proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima da taxa de vitória, então a oferta é diminuída de acordo com a previsão.

## Otimização de posicionamento

Os filtros de pré-oferta de posicionamento são a maneira mais rigorosa de garantir um desempenho sólido. O DSP usa filtros de pré-oferta estrategicamente em diferentes tipos de anúncio para atingir metas de desempenho em posicionamentos dentro de cada pacote. Você pode usar filtros de pré-oferta simultaneamente com otimização no nível do pacote ou de maneira independente.

>[!NOTE]
>
>Os filtros de pré-oferta disponíveis variam de acordo com o tipo de anúncio. Por exemplo, para um posicionamento de exibição padrão, é possível filtrar por taxa de cliques e visibilidade, mas não por taxa de conclusão.

Consulte [Filtros de pré-oferta de nível de posicionamento e como usá-los](optimization-pre-bid-filters.md) para determinar qual filtro de pré-oferta pode ajudar a obter seus KPIs.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Filtros de pré-oferta no nível de posicionamento e como usá-los](optimization-pre-bid-filters.md)
>* [Solução de problemas de desempenho](/help/dsp/optimization/troubleshooting-performance.md)
