---
title: Tipos de relatórios de desempenho em visualizações do Campaign Management
description: Saiba mais sobre os dados do relatório incluídos nas visualizações de gerenciamento de campanha.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 4e82caa995286635b4a181f186d6a1fabb09847d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Tipos de relatórios de desempenho em visualizações do Campaign Management

As visualizações de gerenciamento de campanha incluem dados de relatório abrangentes. Os relatórios disponíveis ajudam a identificar os pacotes e posicionamentos que estão apresentando um bom desempenho e aqueles que precisam de sua atenção. Os botões de ação rápida também tornam você mais produtivo.

## Visualização de todas as campanhas

A visualização do [!UICONTROL Campaigns] é aberta para um conjunto de gráficos de dados de desempenho e uma lista de todas as campanhas em sua conta.

### Exibição de gráfico {#chart-view}

Você pode [personalizar os gráficos de tendência da série temporal](campaign-data-views-manage.md#data-visualizations-manage) em todas as campanhas usando três métricas. Por padrão, os dados de [!UICONTROL Net Spend], [!UICONTROL Impressions] e [!UICONTROL Net CPM] são incluídos em gráficos separados (gráficos de lista tripla). Opcionalmente, é possível alterar as métricas. Para habilitar dados por hora nos gráficos de tendência de série temporal, altere sua seleção de data para um único dia ([!UICONTROL Today], [!UICONTROL Yesterday] ou um dia específico).

![separar gráficos de tendências para três métricas](/help/dsp/assets/trend-chart-separate.png)

Como opção, também é possível sobrepor as três métricas para facilitar a detecção de anomalias e áreas nas quais melhorar a escala ou o desempenho.

![gráfico de tendências com sobreposição](/help/dsp/assets/trend-chart.png)

### Exibição de tabela

![Lista de campanhas](/help/dsp/assets/campaigns-list.png)

Por padrão, cada linha de campanha inclui métricas de ritmo e entrega. As métricas de ritmo incluem [!UICONTROL Gross Spend (Lifetime)], que inclui um medidor do gasto real no destino versus o gasto esperado no destino em todos os pacotes da campanha, para que você possa identificar campanhas com baixo desempenho rapidamente. Opcionalmente, você pode [alterar a exibição de coluna](campaign-data-views-manage.md#column-view-change) ou até [criar uma exibição de coluna personalizada](campaign-data-views-manage.md#column-view-create).

Você pode [personalizar ainda mais as tabelas de dados](campaign-data-views-manage.md#data-tables-manage) de maneiras adicionais e [filtrar os dados visíveis](campaign-data-views-manage.md#filter-data-tables).

Para exibir uma campanha com mais detalhes, clique no seu nome.

#### Indicadores de alerta

*recurso do Beta*

Uma coluna &quot;[!UICONTROL Alerts]&quot; indica quando uma campanha ou qualquer entidade filha abaixo dela tem um problema. Um ícone [!UICONTROL Pulse Panel] à direita da barra de ferramentas também indica se há alertas disponíveis para as entidades listadas. Consulte &quot;[Exibir Alertas](campaign-alerts.md)&quot; para obter mais informações.

## Relatórios de campanha única {#single-campaign-reporting}

Em uma campanha, você pode filtrar dados com base na entidade da campanha: [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]. Você pode [filtrar mais os dados visíveis](campaign-data-views-manage.md#filter-data-tables) para incluir apenas os pacotes, posicionamentos ou anúncios que deseja ver.

![Guias de entidade de campanha](/help/dsp/assets/campaign-subtabs.png)

### Exibição de gráfico

Para cada campanha, você pode [personalizar os gráficos de tendência de série temporal](campaign-data-views-manage.md#data-visualizations-manage) com três métricas, que estão disponíveis em cada exibição de entidade. As mesmas métricas são mantidas em todos os gráficos de tendências da campanha.

Consulte a seção [&quot;Exibição de gráfico&quot; sobre métricas entre campanhas](#chart-view) para obter mais informações.

### Exibição de tabela

Em cada guia de entidade, cada linha inclui métricas de ritmo e entrega, por padrão, mas você pode [alterar a exibição de coluna](campaign-data-views-manage.md#column-view-change) ou até [criar uma exibição de coluna personalizada](campaign-data-views-manage.md#column-view-create) para aplicar em todas as subguias da campanha. Você pode [personalizar ainda mais as tabelas de dados](campaign-data-views-manage.md#data-tables-manage) de maneiras adicionais. Cada tabela de dados inclui uma linha [!UICONTROL Subtotals], que mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

#### Indicadores de alerta

*recurso do Beta*

Uma coluna &quot;[!UICONTROL Alerts]&quot; indica quando um pacote, posicionamento ou anúncio — ou qualquer entidade filha em um pacote ou posicionamento — tem um problema. Uma coluna &quot;[!UICONTROL Alerts]&quot; indica quando uma campanha ou qualquer entidade filha abaixo dela tem um problema. Um ícone [!UICONTROL Pulse Panel] à direita da barra de ferramentas também indica se há alertas disponíveis para as entidades listadas. Consulte &quot;[Exibir Alertas](campaign-alerts.md)&quot; para obter mais informações.

### Outros tipos de relatórios no nível da campanha

Para outros data breakouts, visualize [as páginas de relatórios no nível da campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md). O relatório inclui seções nos dados [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] e [!UICONTROL Audience Performance].

### Outros tipos de relatórios de nível de posicionamento

Para outros detalhamentos de dados, exiba [as páginas de relatórios no nível de posicionamento](/help/dsp/campaign-management/placements/placement-view-report.md). O relatório inclui seções nos dados [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] e [!UICONTROL Ads].

Além disso, você pode exibir os seguintes dados nas configurações de posicionamento:

* [A (exibição detalhada [!UICONTROL Inspector])](placement-details-view.md), que mostra todos os sites, anúncios, dados de frequência e ofertas direcionados para um posicionamento.

* Um [relatório de previsão de posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Relatórios de diagnóstico de posicionamento](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Outros tipos de relatórios no nível do anúncio

Para outros detalhamentos de dados, exiba [as páginas de relatórios no nível do anúncio](/help/dsp/campaign-management/ads/ad-view-report.md). O relatório inclui dados de [!UICONTROL Overview], [!UICONTROL Geography] e [!UICONTROL Viewability].

>[!MORELIKETHIS]
>
>* [Exibir os Sites, Anúncios e Detalhes de Frequência de um Posicionamento](placement-details-view.md)
>* [Gerenciar As Visualizações De Dados Do Campaign](campaign-data-views-manage.md)
>* [Exportar Dados de um Modo de Exibição do Campaign Management](campaign-export-data.md)
>* [Exibir um relatório detalhado de uma campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Exibir Alertas](campaign-alerts.md)
