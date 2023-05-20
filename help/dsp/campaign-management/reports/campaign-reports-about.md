---
title: Sobre Relatórios Na Plataforma
description: Saiba mais sobre os dados do relatório incluídos nas visualizações de gerenciamento de campanha.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Sobre Relatórios Na Plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
As visualizações de gerenciamento de campanha incluem dados de relatório abrangentes. Os relatórios disponíveis ajudam a identificar os pacotes e posicionamentos que estão apresentando um bom desempenho e aqueles que precisam de sua atenção. Os botões de ação rápida também tornam você mais produtivo.

## Visualização de todas as campanhas

A variável [!UICONTROL Campaigns] view é aberto em um conjunto de gráficos de dados de desempenho e uma lista de todas as campanhas em sua conta.

### Exibição de gráfico {#chart-view}

Você pode [personalizar gráficos de tendência de série temporal](campaign-data-visualization-manage.md) em todas as campanhas usando três métricas. Por padrão, os dados para [!UICONTROL Net Spend], [!UICONTROL Impressions], e [!UICONTROL Net CPM] são incluídos em gráficos separados (gráficos de tralha). Opcionalmente, é possível alterar as métricas. Para habilitar dados por hora nos gráficos de tendência de série temporal, altere sua seleção de data para um único dia ([!UICONTROL Today], [!UICONTROL Yesterday]ou um dia específico).

![gráficos de tendência separados para três métricas](/help/dsp/assets/trend-chart-separate.png)

Como opção, também é possível sobrepor as três métricas para facilitar a detecção de anomalias e áreas nas quais melhorar a escala ou o desempenho.

![gráfico de tendências com sobreposição](/help/dsp/assets/trend-chart.png)

### Exibição de tabela

![Lista de campanhas](/help/dsp/assets/campaigns-list.png)

Por padrão, cada linha de campanha inclui métricas de ritmo e entrega. As métricas de ritmo incluem [!UICONTROL Gross Spend (Lifetime)], que inclui um medidor do gasto real no destino em relação ao gasto esperado no destino em todos os pacotes da campanha, para que você possa identificar campanhas com baixo desempenho rapidamente. Opcionalmente, é possível [alterar a exibição de coluna](column-view-change.md) ou até mesmo [criar uma exibição de coluna personalizada](column-view-create.md).

Você pode continuar [personalizar as tabelas de dados](campaign-data-views-about.md) de formas adicionais e [filtrar os dados visíveis](campaign-data-filter.md).

Para exibir uma campanha com mais detalhes, clique no seu nome.

## Relatórios de campanha única {#single-campaign-reporting}

Em uma campanha, você pode filtrar dados com base na entidade da campanha: [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]. Você pode continuar [filtrar os dados visíveis](campaign-data-filter.md) para incluir apenas os pacotes, disposições ou anúncios que deseja ver.

![Guias de entidade de campanha](/help/dsp/assets/campaign-subtabs.png)

### Exibição de gráfico

Para cada campanha, você pode [personalizar gráficos de tendência de série temporal](campaign-data-visualization-manage.md) com três métricas, que estão disponíveis em cada visualização de entidade. As mesmas métricas são mantidas em todos os gráficos de tendências da campanha.

Consulte a [Seção &quot;Exibição de gráfico&quot; sobre métricas entre campanhas](#chart-view) para obter mais informações.

### Exibição de tabela

Em cada guia de entidade, cada linha inclui métricas de ritmo e entrega por padrão, mas você pode [alterar a exibição de coluna](column-view-change.md) ou até mesmo [criar uma exibição de coluna personalizada](column-view-create.md) para aplicar em todas as subguias da campanha. Você pode continuar [personalizar as tabelas de dados](campaign-data-views-about.md) de formas adicionais. Cada tabela de dados inclui um [!UICONTROL Subtotals] linha, que mostra a soma ou o valor médio de cada métrica em todas as linhas visíveis.

### Posicionamento [!UICONTROL Inspector] {#placement-inspector}

Para cada posicionamento, é possível [abrir uma (exibição detalhada [!UICONTROL Inspector])](placement-details-view.md), que inclui os seguintes dados detalhados:

* **[!UICONTROL Sites]:** Todos os sites nos quais o posicionamento teve impressões.

   A variável [!UICONTROL Sites] inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e um [!UICONTROL Exclude] em cada linha, para excluir rapidamente um site do posicionamento.

* **[!UICONTROL Ads]:** Todos os anúncios no posicionamento.

   A variável [!UICONTROL Ads] A guia inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e botões de ação rápida em cada linha, como [!UICONTROL Pause] (para pausar rapidamente um anúncio).

* **[!UICONTROL Frequency]:** Dados para cada nível de frequência de anúncio para o posicionamento, incluindo:
   * o nível de frequência do anúncio (como &quot;1&quot; para todas as instâncias em que os usuários viram um anúncio uma vez)
   * o número exclusivo estimado de dispositivos/navegadores ou pessoas (dependendo da [!UICONTROL Cross Device Level] para a campanha) que receberam impressões no nível de frequência especificado
   * o número estimado de impressões no nível de frequência especificado
   * a frequência média estimada para o nível de frequência especificado. Esse valor é igual a (Impressões estimadas)/(Únicos estimados).

* **[!UICONTROL Inventory]:** Informações sobre todas as ofertas direcionadas pelo posicionamento.

   A variável [!UICONTROL Inventory] permite a solução rápida de problemas ao mostrar estatísticas de desempenho, como [!UICONTROL Auctions], [!UICONTROL Bids], e [!UICONTROL Win Rate]. A guia inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e botões de ação rápida em cada linha, incluindo [!UICONTROL Edit], [!UICONTROL View Report], e [[!UICONTROL Auction Insights] para obter mais soluções de problemas](/help/dsp/inventory/private-deal-auction-insights.md).

#### Solução de problemas de inventário

| Problema | Causa possível | Ações a serem executadas |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | O editor não começou a enviar solicitações de oferta. | Entre em contato com o editor para ativar o negócio. |
|  | O negócio foi configurado incorretamente, por exemplo, inserindo uma ID de negócio externa incorreta. | Confirme os detalhes da negociação e edite-a. |
| [!UICONTROL Auctions but no Bids] | O direcionamento de posicionamento não corresponde às solicitações de oferta recebidas para a oferta. <br><br> Por exemplo, uma inserção pode ter como alvo uma região geográfica que não é elegível para o negócio. | Edite os destinos de posicionamento conforme necessário para evitar incompatibilidades de direcionamento. |
|  | O posicionamento não tem um anúncio ativo com o tipo de mídia necessário para o negócio. | Crie e anexe um anúncio com o tipo de mídia correto ao posicionamento. |
|  | O posicionamento não tem orçamento adequado. | Aumentar o orçamento de posicionamento para permitir lances em solicitações recebidas. |
|  | As datas de voo de posicionamento não se sobrepõem às datas de entrega de impressão da negociação. | Edite as datas de voo da disposição conforme necessário. |
| [!UICONTROL Low Win Rate] | O lance máximo da disposição (piso ou fixo) está abaixo do mínimo exigido pela negociação. | Aumentar a posição [!UICONTROL Max Bid] conforme necessário. |
|  | O posicionamento usa filtros pré-oferta que limitam a oferta. | Diminua os limites dos filtros pré-oferta para permitir mais lances. |
|  | O direcionamento de público-alvo para o posicionamento é muito restritivo. | Verifique se os públicos-alvo especificados têm usuários ativos suficientes e expanda o público-alvo, se possível. |

![inserção Inspetor](/help/dsp/assets/placement-inspector.png)

É possível exportar os dados no [!UICONTROL Sites], [!UICONTROL Ads]ou [!UICONTROL Frequency] para a pasta de download padrão do navegador como um relatório no formato XLSM.

### Outros tipos de relatórios no nível da campanha

Para outros detalhamentos de dados, exibir [as páginas de relatórios no nível da campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md). A variável <!--legacy --> O relatório inclui seções sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], e [!UICONTROL Audience Performance] dados.

>[!MORELIKETHIS]
>
>* [Exibir os sites, anúncios e detalhes de frequência de uma disposição](placement-details-view.md)
>* [Sobre as visualizações de dados do Campaign](campaign-data-views-about.md)
>* [Criar uma Exibição de coluna personalizada](column-view-create.md)
>* [Alterar a Exibição de Coluna](column-view-change.md)
>* [Gerenciar visualizações de dados](campaign-data-visualization-manage.md)
>* [Exportar dados de uma visualização do Campaign Management](campaign-export-data.md)
>* [Exibir um relatório detalhado de uma campanha](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

