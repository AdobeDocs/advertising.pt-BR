---
title: Tipos de relatórios de desempenho em visualizações do Campaign Management
description: Saiba mais sobre os dados do relatório incluídos nas visualizações de gerenciamento de campanha.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Tipos de relatórios de desempenho em visualizações do Campaign Management

As visualizações de gerenciamento de campanha incluem dados de relatório abrangentes. Os relatórios disponíveis ajudam a identificar os pacotes e posicionamentos que estão apresentando um bom desempenho e aqueles que precisam de sua atenção. Os botões de ação rápida também tornam você mais produtivo.

## Visualização de todas as campanhas

A variável [!UICONTROL Campaigns] view é aberto em um conjunto de gráficos de dados de desempenho e uma lista de todas as campanhas em sua conta.

### Exibição de gráfico {#chart-view}

Você pode [personalizar gráficos de tendência de série temporal](campaign-data-views-manage.md#data-visualizations-manage) em todas as campanhas usando três métricas. Por padrão, os dados para [!UICONTROL Net Spend], [!UICONTROL Impressions], e [!UICONTROL Net CPM] são incluídos em gráficos separados (gráficos de tralha). Opcionalmente, é possível alterar as métricas. Para habilitar dados por hora nos gráficos de tendência de série temporal, altere sua seleção de data para um único dia ([!UICONTROL Today], [!UICONTROL Yesterday]ou um dia específico).

![gráficos de tendência separados para três métricas](/help/dsp/assets/trend-chart-separate.png)

Como opção, também é possível sobrepor as três métricas para facilitar a detecção de anomalias e áreas nas quais melhorar a escala ou o desempenho.

![gráfico de tendências com sobreposição](/help/dsp/assets/trend-chart.png)

### Exibição de tabela

![Lista de campanhas](/help/dsp/assets/campaigns-list.png)

Por padrão, cada linha de campanha inclui métricas de ritmo e entrega. As métricas de ritmo incluem [!UICONTROL Gross Spend (Lifetime)], que inclui um medidor do gasto real no destino em relação ao gasto esperado no destino em todos os pacotes da campanha, para que você possa identificar campanhas com baixo desempenho rapidamente. Opcionalmente, é possível [alterar a exibição de coluna](campaign-data-views-manage.md#column-view-change) ou até mesmo [criar uma exibição de coluna personalizada](campaign-data-views-manage.md#column-view-create).

Você pode continuar [personalizar as tabelas de dados](campaign-data-views-manage.md#data-tables-manage) de formas adicionais e [filtrar os dados visíveis](campaign-data-views-manage.md#filter-data-tables).

<!--
An "Alerts" column indicates when a campaign (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

Para exibir uma campanha com mais detalhes, clique no seu nome.

## Relatórios de campanha única {#single-campaign-reporting}

Em uma campanha, você pode filtrar dados com base na entidade da campanha: [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]. Você pode continuar [filtrar os dados visíveis](campaign-data-views-manage.md#filter-data-tables) para incluir apenas os pacotes, disposições ou anúncios que deseja ver.

![Guias de entidade de campanha](/help/dsp/assets/campaign-subtabs.png)

### Exibição de gráfico

Para cada campanha, você pode [personalizar gráficos de tendência de série temporal](campaign-data-views-manage.md#data-visualizations-manage) com três métricas, que estão disponíveis em cada visualização de entidade. As mesmas métricas são mantidas em todos os gráficos de tendências da campanha.

Consulte a [Seção &quot;Exibição de gráfico&quot; sobre métricas entre campanhas](#chart-view) para obter mais informações.

### Exibição de tabela

Em cada guia de entidade, cada linha inclui métricas de ritmo e entrega por padrão, mas você pode [alterar a exibição de coluna](campaign-data-views-manage.md#column-view-change) ou até mesmo [criar uma exibição de coluna personalizada](campaign-data-views-manage.md#column-view-create) para aplicar em todas as subguias da campanha. Você pode continuar [personalizar as tabelas de dados](campaign-data-views-manage.md#data-tables-manage) de formas adicionais. Cada tabela de dados inclui um [!UICONTROL Subtotals] linha, que mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

<!--
An "Alerts" column indicates when a package, placement, or ad &mdash; or any child entity under a package or placement &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

### Outros tipos de relatórios no nível da campanha

Para outros detalhamentos de dados, exibir [as páginas de relatórios no nível da campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md). O relatório inclui seções sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], e [!UICONTROL Audience Performance] dados.

### Outros tipos de relatórios de nível de posicionamento

Para outros detalhamentos de dados, exibir [as páginas de relatórios no nível de posicionamento](/help/dsp/campaign-management/placements/placement-view-report.md). O relatório inclui seções sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications], e [!UICONTROL Ads] dados.

Além disso, você pode exibir os seguintes dados nas configurações de posicionamento:

* [A (visualização detalhada [!UICONTROL Inspector])](placement-details-view.md), que mostra todos os sites direcionados, anúncios, dados de frequência e ofertas para um posicionamento.

* A [relatório de previsão de posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md)

* [Relatórios de diagnóstico de posicionamento](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Outros tipos de relatórios no nível do anúncio

Para outros detalhamentos de dados, exibir [as páginas de relatórios no nível do anúncio](/help/dsp/campaign-management/ads/ad-view-report.md). O relatório inclui [!UICONTROL Overview], [!UICONTROL Geography], e [!UICONTROL Viewability] dados.

>[!MORELIKETHIS]
>
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Gerenciar As Visualizações De Dados Do Campaign](campaign-data-views-manage.md)
>* [Exportar dados de uma visualização do Campaign Management](campaign-export-data.md)
>* [Exibir um relatório detalhado de uma campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
