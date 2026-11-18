---
title: (Nova interface do usuário) Advertising Insights
description: Saiba como configurar e visualizar painéis de publicidade do insight para precisão de modelo, desempenho, simulações, limites de orçamento e conversões.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 54920f5e0e08c1bf6f960b4d96aa4161dfa11143
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# (Nova interface do usuário) Advertising Insights

Os insights do Advertising apresentam dados visuais e acionáveis para ajudar você a avaliar o desempenho do portfólio, identificar problemas de otimização e comparar dados de conversão. Cada insight é gerado sob demanda e exibido como um painel na tela.

A exibição **[!UICONTROL Reports]>[!UICONTROL Insights]** exibe os insights disponíveis em **[!UICONTROL Dashboards]**. O cabeçalho da página é **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>Esta página descreve os painéis do insight na nova interface do usuário beta. A disponibilidade depende do seu acesso e dos insights disponíveis para o anunciante selecionado. Os [Advertising Insights herdados](/help/search-social-commerce/advertising-insights/insight-about.md) incluem um conjunto diferente de análises e procedimentos para arquivos gerados.

## Tipos de insights {#insight-types}

| Insight | Descrição |
| --- | --- |
| [!UICONTROL Model Accuracy] | Identifica como o Search, Social e Commerce prevê o custo e a receita de um portfólio. Você pode analisar a precisão do modelo nos níveis de portfólio, rede de publicidade e campanha. |
| [!UICONTROL Performance Insights] | Compara o desempenho do portfólio antes e depois de uma alteração de status de otimização, alteração de objetivo ou data especificada. O painel inclui resumos de desempenho, uma auditoria de alterações que afetam a otimização, comparações de campanha, tendências e análise de valor de objetivo. |
| [!UICONTROL Portfolio Simulation Analysis] | Compara uma simulação personalizada existente com o desempenho real. Você pode revisar os dados do portfólio e da campanha, analisar a precisão da simulação e explorar o desempenho estimado em diferentes níveis de gasto direcionados. |
| [!UICONTROL Campaign Budget Cap Analysis] | Indica se o gasto de um portfólio foi limitado por limites de orçamento de campanha. O painel inclui gastos limitados, campanhas afetadas, impressões perdidas estimadas, tendências diárias e de dia da semana e recomendações para configurações de portfólio. |
| [!UICONTROL Modeled Conversions] | Compara os valores de conversão do Adobe com os valores relatados pela rede de publicidade, incluindo dados modelados. Você pode analisar contas, portfólios ou campanhas e comparar valores medidos pela Adobe e pela Adobe e modelados com valores relatados pelo editor. |
| [!UICONTROL Delayed Revenue Analysis] | Mede o atraso de conversão (o tempo decorrido entre um clique de anúncio ou view-through e uma conversão subsequente) e mostra seu impacto no valor objetivo, no retorno sobre o investimento (ROI) e na precisão do modelo. A análise está disponível somente para portfólios com atribuição de receita baseada em cliques ou view-through. |

## Gerar uma insight {#insight-generate}

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Insights]**.

1. Clique na insight que deseja gerar.

1. No painel **[!UICONTROL Configure]**, especifique as [configurações do insight](#insight-settings).

1. Clique em **[!UICONTROL Generate Insight]**.

   O painel de configuração é fechado e o painel exibe a análise.

1. Revise os [resultados do insight](#insight-results).

Para alterar as configurações, clique em **[!UICONTROL Configure]**, altere os valores e clique novamente em **[!UICONTROL Generate Insight]**. Para retornar à lista do insight, clique em **[!UICONTROL Analysis List]** na navegação estrutural.

## Configurações do insight {#insight-settings}

### Precisão do modelo {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** Selecione um portfólio.

* **[!UICONTROL Choose Revenue Type]:** Selecione **[!UICONTROL Actual Revenue]** (padrão) ou **[!UICONTROL Delayed Revenue]**.

* **[!UICONTROL Date Range]:** Selecione as datas a serem analisadas. Consulte [Configurações de intervalo de datas](#date-range-settings).

### Insights de desempenho {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** Selecione um portfólio.

* **[!UICONTROL Revenue Type]:** Selecione **[!UICONTROL Actual Revenue]** (padrão) ou **[!UICONTROL Delayed Revenue]**.

* **Data do evento:** Selecione o tipo de data sobre a qual comparar o desempenho:

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (o padrão): selecione uma data de alteração de status de otimização disponível para o portfólio.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Selecione uma data de alteração de objetivo disponível para o portfólio.

  * **[!UICONTROL Specific Date]:** Especifique uma data usando o seletor de datas.

  Selecione a data do evento antes de configurar os períodos de comparação. Se nenhuma data de evento estiver disponível para o portfólio selecionado, você poderá usar **[!UICONTROL Specific Date]**.

* **[!UICONTROL Pre Days]:** Especifique o período antes da data do evento:

  * Selecione **[!UICONTROL 7]** (padrão), **[!UICONTROL 14]** ou **[!UICONTROL 30]**.

  * Selecione **[!UICONTROL Pre Start Date]** e especifique o **[!UICONTROL Custom Pre Date]**.

  * Selecione **[!UICONTROL Custom Pre Days]** e insira um número positivo de dias.

* **[!UICONTROL Post Days]:** Especifique o período após a data do evento:

  * Selecione **[!UICONTROL 7]** (padrão), **[!UICONTROL 14]** ou **[!UICONTROL 30]**.

  * Selecione **[!UICONTROL Post End Date]** e especifique o **[!UICONTROL Custom Post Date]**.

  * Selecione **[!UICONTROL Custom Post Days]** e insira um número positivo de dias.

  A data do evento em si não está incluída em nenhum dos períodos de comparação.

* **[!UICONTROL Date Exclusion]:** (Opcional) Excluir datas da análise:

  1. Clique em **[!UICONTROL Select Dates]**.

  1. Selecione as datas a serem excluídas:

     * Clique em datas individuais para selecioná-las ou desmarcá-las.

     * Mantenha **[!UICONTROL Shift]** pressionado enquanto clica para selecionar um intervalo.

     * Para remover todas as exclusões, clique em **[!UICONTROL Clear All]**.

  1. Clique em **[!UICONTROL Done]** quando terminar.

### Análise de simulação do Portfolio {#simulation-settings}

* **[!UICONTROL Portfolios]:** Selecione um portfólio com uma simulação personalizada existente.

* **[!UICONTROL Simulation Date]:** Selecione a data da simulação a ser analisada. Se várias simulações estiverem disponíveis para essa data, selecione também a simulação por nome.

  Se nenhuma simulação personalizada estiver disponível, [gere uma simulação personalizada](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md) antes de usar esta insight.

* **[!UICONTROL Actual Days]:** Selecione **[!UICONTROL 7]** (padrão), **[!UICONTROL 14]** ou **[!UICONTROL 30]** dias de dados de desempenho real. Para especificar outro número, selecione **[!UICONTROL Enter Actual Days]** e insira um valor de 1 a 90.

* **[!UICONTROL Type]:** Selecione **[!UICONTROL Transaction Date]** (padrão) ou **[!UICONTROL Click Date]** para atribuição de conversão.

### Análise do limite de orçamento da campanha {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** Selecione um portfólio.

* **[!UICONTROL Date Range]:** Selecione as datas a serem analisadas. Consulte [Configurações de intervalo de datas](#date-range-settings).

### Conversões modeladas {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** Selecione **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (padrão) ou **[!UICONTROL Campaign]**.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]** ou **[!UICONTROL Campaigns]:** Selecione as entidades aplicáveis para o nível de análise. É possível selecionar várias entidades.

* **[!UICONTROL Date Range]:** Selecione as datas a serem analisadas. Consulte [Configurações de intervalo de datas](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Selecione a propriedade de conversão do Adobe para comparar.

* **[!UICONTROL Publisher Conversion]:** Selecione a propriedade de conversão do publicador a ser comparada.

  As propriedades de conversão disponíveis dependem do nível de análise, das entidades selecionadas e do intervalo de datas. Ambas as propriedades de conversão são necessárias para a comparação.

### Análise de Receita Atrasada {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** Selecione um portfólio com atribuição de receita baseada em cliques ou view-through.

* **[!UICONTROL Date Range]:** Selecione as datas a serem analisadas. Consulte [Configurações de intervalo de datas](#date-range-settings).

### Configurações do intervalo de datas {#date-range-settings}

Para insights com uma configuração **[!UICONTROL Date Range]**, selecione **[!UICONTROL Last 7 days]** (padrão), **[!UICONTROL Last 14 days]** ou **[!UICONTROL Last 30 days]**.

Para especificar outro período, selecione **[!UICONTROL Custom Date]** e insira o **[!UICONTROL Start Date]** e **[!UICONTROL End Date]**. Você pode selecionar datas nos últimos 90 dias, até a data atual.

## Exibir resultados do insight {#insight-results}

### Precisão do modelo {#model-accuracy-results}

Revise os detalhes do portfólio e use as seguintes guias:

* **[!UICONTROL Portfolio]:** Revise a precisão do modelo em nível de portfólio e as comparações de orçamento.

* **[!UICONTROL Ad Network]:** Examine as comparações de orçamento e precisão do modelo por rede de anúncios.

* **[!UICONTROL Campaigns]:** Revise a precisão e o destino do modelo de nível de campanha versus o desempenho real.

* **[!UICONTROL Playground Beta]:** Comparar a precisão do modelo para várias campanhas.

Para gráficos de precisão de campanha, selecione o **[!UICONTROL Comparison Options]** e **[!UICONTROL Campaign]**. Em **[!UICONTROL Playground Beta]**, você pode selecionar várias campanhas. Clique em **[!UICONTROL Table View]** para alternar entre um gráfico e seus dados subjacentes.

### Insights de desempenho {#performance-insights-results}

O painel mostra **[!UICONTROL Pre Period]** e **[!UICONTROL Post Period]**, métricas de desempenho agregadas para ambos os períodos e detalhes do portfólio.

O **[!UICONTROL Audit Trail]** resume as alterações nos fatores que afetam a otimização, incluindo orçamento do portfólio, estratégia de gastos, gasto mínimo da campanha e múltiplo limite de gastos. Quando as alterações tiverem detalhes disponíveis, clique em **[!UICONTROL View Details]** para inspecioná-las.

Use as guias **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]** e **[!UICONTROL Objective Value And Analysis]** para explorar a comparação.

### Análise de simulação do Portfolio {#simulation-results}

Revise os detalhes da simulação e use as seguintes guias:

* **[!UICONTROL Portfolio]:** Revise os dados de simulação de nível de portfólio. Nesta guia:

  * **[!UICONTROL Simulation Data]** mostra as métricas de simulação e o desempenho de meta de gastos.

  * **[!UICONTROL Simulation Vs Actual]** compara o desempenho simulado e real.

  * **[!UICONTROL Try New Target]** permite que você insira uma meta de gastos em **[!UICONTROL Explore Target Spend]** para visualizar os cliques, custos e receita estimados. Essa é uma análise do desempenho estimado; ela não altera a meta de gastos do portfólio.

* **[!UICONTROL Campaigns]:** Revise as comparações de simulação de nível de campanha.

* **[!UICONTROL Accuracy Analysis]:** Revise a precisão da simulação.

### Análise do limite de orçamento da campanha {#budget-cap-results}

Revise os detalhes do portfólio e as métricas de resumo:

* **[!UICONTROL Total Capped Spend]:** a porcentagem de gastos em dias quando os orçamentos da campanha foram atingidos.

* **[!UICONTROL Capped Campaigns]:** O número de campanhas que atingiram seus orçamentos pelo menos uma vez.

* **[!UICONTROL Est. Lost Impressions]:** Impressões estimadas ausentes devido a limites de orçamento.

* **[!UICONTROL Peak Capping Day]:** O dia da semana com o gasto mais limitado.

Os gráficos **[!UICONTROL Spend on Capped Campaigns by Day]** e **[!UICONTROL Capped Spend by Weekday]** mostram tendências de limite. **[!UICONTROL Capped Campaign Performance]** de revisão para obter detalhes da campanha e **[!UICONTROL Portfolio Settings Recommendations]** para alterações de configurações sugeridas.

### Conversões modeladas {#modeled-conversions-results}

Revise as seguintes tabelas para as entidades e o intervalo de datas selecionados:

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** Compara os valores de conversão medidos diretamente pelo Adobe com os valores relatados pelo editor, que incluem dados medidos e modelados.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** Compara valores de conversão medidos e modelados pela Adobe com valores relatados pelo editor.

Ambas as tabelas incluem o nome e a ID da entidade, o valor do Adobe, o valor relatado pelo editor, a diferença absoluta e a diferença de porcentagem.

Se nenhum dado estiver disponível, verifique se você selecionou as duas propriedades de conversão e se há dados para as entidades e o intervalo de datas selecionados.

### Análise de Receita Atrasada {#delayed-revenue-results}

O **[!UICONTROL Key Insights Summary]** mostra a receita ponderada esperada (agora chamada de &quot;[valor do objetivo](/help/search-social-commerce/glossary.md#o-p)&quot;), o ROI e as informações de precisão do modelo.

A seção **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** mostra a porcentagem de conversões realizadas no dia 0 e nos dias 3, 7, 14 e 28 para cada propriedade de receita.

Em **[!UICONTROL Performance Over Time]**, selecione **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]** ou **[!UICONTROL Model Accuracy]** para comparar a data de clique, a data da transação e o desempenho esperado. Clique em **[!UICONTROL Table View]** para alternar entre o gráfico e seus dados subjacentes.

Em **[!UICONTROL Metrics Definitions]**, clique em **[!UICONTROL Show]** para obter explicações sobre as datas e métricas usadas na análise, ou em **[!UICONTROL Hide]** para recolhê-las.

Se a análise não for aplicável, selecione um portfólio com atribuição de receita baseada em cliques ou view-through. Se nenhum dado estiver disponível, verifique se existem dados para o portfólio e o intervalo de datas selecionados.
