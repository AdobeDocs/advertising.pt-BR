---
title: Como o DSP otimiza suas campanhas
description: Saiba como o DSP otimiza os pacotes em suas campanhas.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Como o DSP de publicidade otimiza suas campanhas

Esta página descreve como o mecanismo de otimização para DSP, que é alimentado pelo [!DNL Adobe Sensei]O otimiza os pacotes em suas campanhas. Para obter dicas e truques sobre como otimizar manualmente suas campanhas, entre em contato com a equipe de conta do Adobe. <!-- add link to trading playbook if we add it to help -->

As metas de otimização de pacotes operam em dois níveis:

* Para cada pacote: o DSP aloca orçamento para cada posicionamento no pacote com base no desempenho do posicionamento em relação ao KPI selecionado.

* Para cada posicionamento/leilão no pacote: O DSP calcula o valor do KPI econômico em tempo real para cada leilão por posicionamento e, em seguida, usa esse valor para determinar o lance.

  >[!NOTE]
  >
  >O valor econômico pode ser pesadamente ponderado com base no quão bem uma colocação está gastando. Se uma colocação estiver por trás de sua meta de gastos, então é permitido comprar leilões de qualidade mais baixa. Se uma inserção estiver facilmente atingindo sua meta de gastos, o foco será transferido para leilões de maior qualidade.

## Otimização de pacote

O DSP pode otimizar sua entrega de duas maneiras fundamentais, com 20 variações disponíveis para se alinhar a sua meta específica de desempenho. Você pode optar por:

* Priorizar a taxa de desempenho

* Priorizar o equilíbrio entre a eficiência de custos e a taxa de desempenho

Consulte [Metas de otimização e como usá-las](optimization-goals.md) para determinar qual meta de otimização ajudará você a atingir seus KPIs.

### Pacotes que priorizam a taxa de desempenho

Para metas de otimização que priorizam a taxa de desempenho, o DSP prevê o desempenho de cada leilão e sempre dá lances no Lance máximo. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]e assim por diante.

Esse modo de otimização funciona bem se:

* Você já conhece o nível de CPM efetivo/aceitável (por exemplo, um referencial histórico).

* Você está disposto a ajustar manualmente o [!UICONTROL Max Bid] para cada posicionamento se tiver desafios com o dimensionamento.

* Você está priorizando a escala em detrimento da eficiência.

#### Lógica de ritmo {#pacing-logic-performance}

* Se os gastos estiverem no ritmo, a licitação se torna mais seletiva, de modo que você só licitará em leilões previstos com altas taxas de desempenho.

* Se os gastos estiverem atrasados, a licitação se torna menos seletiva, de modo que você licitará em leilões previstos com taxas de desempenho mais baixas para alcançar a meta de ritmo.

#### Limpando o Sombreamento de Preço/Oferta {#clearing-price-performance}

Depois de executar a lógica de ritmo, o DSP executa a oferta proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima da taxa de vitória, então a oferta é diminuída de acordo com a previsão.

### Pacotes que priorizam o equilíbrio da eficiência de custos com a taxa de desempenho

Para algumas metas de otimização, o DSP prevê o desempenho de cada leilão e ajusta os preços de compra automaticamente, nunca excedendo os valores de uma colocação [!UICONTROL Max Bid]. Exemplos de metas de otimização aplicáveis incluem [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]e assim por diante.

#### Lógica de ritmo {#pacing-logic-balanced}

* Se os gastos estiverem no ritmo, o DSP se torna mais sensível ao preço, oferecendo valores menores para trocar a taxa de ganho com o plano de ritmo.

* Se uma métrica de desempenho também estiver sendo balanceada (todas as metas exceto [!UICONTROL Lowest CPM]), o KPI previsto é mesclado ao valor oferecido. Portanto, você faz lances mais altos para leilões que se prevê terem melhor desempenho com base no &quot;custo por&quot;.

* Se a despesa estiver atrasada, o DSP torna-se menos sensível ao preço e oferece valores mais elevados, até ao [!UICONTROL Max Bid], para trocar a taxa de ganho com o plano de ritmo.

#### Limpando o Sombreamento de Preço/Oferta {#clearing-price-balanced}

Depois de executar a lógica de ritmo, o DSP executa a oferta proposta por meio de um modelo de previsão de preço de compensação. Se a previsão indicar que a oferta pode ser reduzida com uma diminuição mínima da taxa de vitória, então a oferta é diminuída de acordo com a previsão.

## Otimização de posicionamento

Os filtros de pré-oferta de posicionamento são a maneira mais rigorosa de garantir um desempenho sólido. O DSP usa filtros de pré-oferta estrategicamente em diferentes tipos de anúncio para atingir metas de desempenho em posicionamentos dentro de cada pacote. Você pode usar filtros de pré-oferta simultaneamente com otimização no nível do pacote ou de maneira independente.

>[!NOTE]
>
>Os filtros de pré-oferta disponíveis variam de acordo com o tipo de anúncio. Por exemplo, para um posicionamento de exibição padrão, é possível filtrar por taxa de cliques e visibilidade, mas não por taxa de conclusão.

Consulte [Filtros pré-oferta no nível de posicionamento e como usá-los](optimization-pre-bid-filters.md) para determinar qual filtro de pré-oferta ajudará você a atingir seus KPIs.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Filtros pré-oferta no nível de posicionamento e como usá-los](optimization-pre-bid-filters.md)
>* [Solução de problemas de desempenho](/help/dsp/optimization/troubleshooting-performance.md)
