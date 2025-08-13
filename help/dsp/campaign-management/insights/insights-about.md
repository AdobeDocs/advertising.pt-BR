---
title: Sobre Insights
description: Saiba mais sobre insights de desempenho com visualizações.
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: 99b9c110de5efbf646e35979eee6baac1d34f6ed
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Sobre Insights

*recurso do Beta*

Insights de desempenho de alto nível com visualizações fornecem as informações necessárias para otimizar suas campanhas com eficiência e descobrir novas oportunidades para dimensionar o desempenho. Você pode visualizar dados em campanhas para um anunciante especificado ou detalhar para um nível inferior.

Use insights de desempenho para:

* Acompanhe tendências de longo prazo para planejamento estratégico e tomada de decisões informadas.

* Identificar oportunidades para alcançar melhores resultados.

* Melhore a eficiência reduzindo o tempo entre a obtenção de dados brutos e a obtenção de insights acionáveis.

É possível exportar todas as visualizações de uma guia para um arquivo do PDF ou baixar os dados de uma insight específica sem visualizações no formato de planilha do Microsoft Excel (XLSX).

Você também pode [alterar o intervalo de datas, configurar o modo de exibição e salvar um modo de exibição personalizado](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} da mesma forma que pode para modos de exibição de gerenciamento de campanha.

## Tipos de insights

### Guia [!UICONTROL Home]

A guia [!UICONTROL Home] fornece métricas principais de padrão, desempenho e visibilidade em todas as campanhas de um anunciante. Por padrão, são exibidos dados de posicionamento cruzado para um anunciante específico e uma meta personalizada. Opcionalmente, é possível configurar filtros para mostrar dados de um anunciante diferente, uma meta personalizada diferente ou um posicionamento específico. <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. --> Os insights incluem:

* **[!UICONTROL Trends]:** Um gráfico de tendências para três métricas especificadas pelo cliente (por padrão, [!UICONTROL Net Spend], [!UICONTROL Impressions] e [!UICONTROL Net CPM]).

* **[!UICONTROL Delivery Breakdown]:** Um detalhamento dos dados de métricas específicas por três dimensões especificadas pelo cliente, como campanha, editor e tipo de mídia. Para cada detalhamento dimensional, você pode escolher uma métrica diferente.

### Guia [!UICONTROL Household Reach]

A guia [!UICONTROL Household Reach] fornece métricas de alcance doméstico em todas as campanhas de um anunciante. Por padrão, os dados entre campanhas são exibidos. Opcionalmente, é possível configurar filtros para mostrar dados de um anunciante diferente, de uma campanha específica, em pacotes ou posicionamentos, ou de um pacote ou posicionamento específico. Os insights incluem:

* **[!UICONTROL Trends]:** Um gráfico de tendências por dia ou por semana para três métricas especificadas pelo cliente (por padrão, [!UICONTROL Net Spend], [!UICONTROL Unique Reach] e [!UICONTROL Net CPM]).

* **[!UICONTROL Incremental Household Reach]:** Um gráfico de rosca mostrando o alcance doméstico incremental por [!UICONTROL Media Type], [!UICONTROL Device Type] ou [!UICONTROL Inventory Type]. *Alcance doméstico incremental* é definido como um agregado doméstico alcançado exclusivamente por meio de uma única mídia, dispositivo ou tipo de inventário.

* **[!UICONTROL Reach Breakdown]:** O alcance doméstico exclusivo incremental vs. alcance doméstico sobreposto por [!UICONTROL Media Type], [!UICONTROL Device Type] ou [!UICONTROL Inventory Type].

  *Alcance doméstico incremental* é definido como um agregado doméstico alcançado exclusivamente por meio de uma única mídia, dispositivo ou tipo de inventário. *A sobreposição de alcance doméstico* é definida como uma família atingida por vários tipos de mídia, dispositivo ou inventário.

* **[!UICONTROL Top Performers]:** Campanhas, posicionamentos, pacotes, editores, sites/aplicativos, tipos de mídia, tipos de inventário ou tipos de dispositivo de melhor desempenho por [!UICONTROL Unique Reach], [!UICONTROL Net Spend] e [!UICONTROL Cost per Reach].

* **[!UICONTROL Performance Analysis]:** O [!UICONTROL Cost per Reach] e [!UICONTROL Net Spend] por pacote, editor ou site/aplicativo. Use esta insight para ver quais pacotes, editores ou sites/aplicativos mostram o potencial para alcance incremental significativo.

  O tamanho de cada bolha indica a pontuação de alcance incremental, com bolhas maiores indicando um alcance incremental mais alto em média. Para ver o nome completo da entidade e as métricas principais de qualquer bolha, mantenha o cursor sobre a bolha.

  Os níveis de impacto incluem:

   * **Alto impacto:** Considere aumentar o orçamento.
   * **Impacto moderado**
   * **Impacto limitado:** requer atenção

### Guia [!UICONTROL Household Conversion]

A guia [!UICONTROL Household Conversion] fornece métricas de conversão doméstica em todas as campanhas de um anunciante<!-- active only? -->. Por padrão, são exibidos dados entre campanhas para um anunciante específico e uma métrica de conversão específica. Opcionalmente, é possível configurar filtros para mostrar dados de um anunciante ou métrica de conversão diferente, para uma campanha específica, entre pacotes ou posicionamentos, ou para um pacote ou posicionamento específico. Os insights incluem:

* **[!UICONTROL Trends]:** Um gráfico de tendências por dia ou por semana para três métricas especificadas pelo cliente (por padrão, [!UICONTROL Net Spend], [!UICONTROL Conversions] e [!UICONTROL Net CPM]).

* **[!UICONTROL Conversion Participation Overview]:** Um gráfico de barras que mostra quais tipos de mídia, tipos de inventário e tipos de dispositivo resultam na maioria das conversões domésticas.

  As impressões entregues dentro do período de lookback (30 dias) são consideradas válidas para a participação de conversão.

* **[!UICONTROL Top Performers]:** Uma tabela das campanhas, pacotes, posicionamentos, editores, sites/aplicativos, tipos de mídia e tipos de inventário que direcionam o desempenho para três métricas especificadas pelo cliente (por padrão, [!UICONTROL Net Spend], [!UICONTROL CPA] e [!UICONTROL Conversions]). O executor superior é listado primeiro.

* **[!UICONTROL Performance Analysis]:** O [!UICONTROL CPA] e [!UICONTROL Net Spend] por pacote, editor ou site/aplicativo. Use esta insight para ver quais pacotes, editores ou sites/aplicativos mostram o potencial para alcance incremental significativo.

  O tamanho de cada bolha indica a pontuação de alcance incremental, com bolhas maiores indicando um alcance incremental mais alto em média. Para ver o nome completo da entidade e as métricas principais de qualquer bolha, mantenha o cursor sobre a bolha.

  Os níveis de impacto incluem:

   * **Alto impacto:** Considere aumentar o orçamento.
   * **Impacto moderado**
   * **Impacto limitado:** requer atenção

## Abrir Insights de Desempenho

* (Para abrir insights para todas as campanhas) No menu principal, clique em **[!UICONTROL Insights BETA]**.

* (Para abrir insights para uma campanha, pacote ou posicionamento específico) Ao lado do nome da entidade na exibição [!UICONTROL Campaigns], [!UICONTROL Packages] ou [!UICONTROL Placements], clique em **[!UICONTROL ...]** > **[!UICONTROL Insights]**.

## Aplicar filtros a uma guia

1. Na barra de ferramentas na parte superior da guia, clique em ![Botão Filtrar](/help/dsp/assets/filter.png).

1. Na coluna da esquerda, selecione uma dimensão e, em seguida, selecione um ou mais valores na coluna da direita, conforme aplicável.

   Você pode selecionar apenas um anunciante por vez.

1. Clique em **[!UICONTROL Apply]**.

1. (Opcional) Para restringir ainda mais os dados, selecione o tipo de entidade na barra de ferramentas e, em seguida, selecione um valor de entidade específico (uma única campanha, pacote ou posicionamento).

## Alterar o Dimension reportado para uma Insight

* No menu suspenso, à esquerda superior da insight, selecione a dimensão.

## Alterar as métricas relatadas de uma Insight

1. Na parte superior direita do insight, clique em ![Configurações de métrica](/help/dsp/assets/metric-settings.png "Configurações de métrica").

1. Selecione as métricas e clique em **[!UICONTROL Apply]**.

## Exportar todas as visualizações de uma guia para um arquivo do PDF

* Acima da guia, clique em **[!UICONTROL ...]** > **[!UICONTROL Export]**.

  O arquivo é salvo na pasta de downloads padrão do navegador.

## Baixar um Insight específico em um arquivo XLSX

* No canto superior direito da insight, clique em ![Download](/help/creative/assets/download.png "Download").

  O arquivo é salvo na pasta de downloads padrão do navegador.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Tipos de Relatórios de Desempenho em Exibições de Gerenciamento de Campanha](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
>* [Gerenciar As Visualizações De Dados Do Campaign](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
