---
title: Sobre simulações
description: Saiba mais sobre simulações de portfólio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
source-git-commit: 73528e2aa905216584d1aa294f5581d2bca88432
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 0%

---

# Sobre simulações

*recurso do Beta*

Os relatórios de simulação mostram o valor do custo marginal estimado para objetivo, o custo, o número de cliques e o valor do objetivo que você pode esperar de um portfólio em vários níveis de gastos (custo) e os orçamentos diários correspondentes ou outras metas. Opcionalmente, você pode [personalizar a exibição](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para ver métricas de tráfego adicionais, configurações de simulação e apenas um tipo de simulação específico ([!UICONTROL Weekly] ou [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipos de simulações

* Simulações semanais automatizadas

* Simulações personalizadas geradas pelo usuário

### Simulações semanais automatizadas

Os relatórios de simulação são executados automaticamente toda semana usando as configurações atuais do portfólio. As simulações semanais automatizadas estão disponíveis apenas para períodos em que o portfólio está [otimizado ou ativo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

#### Simulações semanais baixadas

Cada simulação semanal baixada consiste em uma pasta de trabalho. Cada pasta de trabalho inclui a meta para cada um dos 20 níveis de etapa e o custo projetado, os cliques, a receita ponderada (valor do objetivo) e as métricas de conversão incluídas no objetivo, com base na meta correspondente. Para as primeiras 20 linhas de dados, as restrições não eram aplicadas; para as linhas de dados restantes, as restrições eram aplicadas.

#### Detalhes da simulação semanal na tela

Os detalhes da simulação na tela mostram insights visuais e tabulares em nível de portfólio. Para dados por campanha, grupos de anúncios, unidades de oferta ou dispositivo, [baixe a simulação](simulation-download.md).

##### Exibição em gráfico

A exibição em gráfico mostra o valor do objetivo esperado ou outra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para a meta de gastos para cada um dos 20 níveis de gastos. O ponto médio de destino é identificado, e você pode, opcionalmente, alterar o ponto médio de destino para ver os dados previstos usando esse valor. Mantenha o cursor sobre qualquer ponto do gráfico para ver os dados desse ponto.

Você pode exibir os dados com e sem restrições aplicadas, com restrições aplicadas e sem restrições aplicadas. Quando você exibe dados que consideram restrições, as restrições aplicadas são identificadas acima do gráfico.

##### Visualização em tabela

A exibição de tabela mostra a meta de gasto para cada um dos 20 níveis de gasto. Também inclui o custo estimado correspondente, o custo marginal para o valor do objetivo, cliques, valor do objetivo e métricas de conversão no objetivo do portfólio para cada nível de gastos. O ponto médio de destino é identificado, e você pode, opcionalmente, alterar o ponto médio de destino para ver os dados previstos usando esse valor.

Você pode exibir os dados com e sem restrições aplicadas, com restrições aplicadas e sem restrições aplicadas. Quando você exibe dados que consideram restrições, as restrições aplicadas são identificadas acima do gráfico.

##### Configurações de simulação

As configurações da simulação são mostradas como somente leitura abaixo do gráfico ou tabela.

##### Configurações do Portfolio

Para ver as configurações somente leitura do portfólio aplicável, clique em **[!UICONTROL Portfolio Settings]** no canto superior direito.

### Simulações personalizadas geradas pelo usuário

Você pode criar um relatório de simulação personalizado para um único portfólio [otimizado ou ativo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) usando as configurações atuais do portfólio ou usando configurações personalizadas do portfólio, com ou sem restrições de nível de unidade de oferta aplicadas, para ver os resultados que essas configurações produziriam sem realmente alterá-los. Por exemplo, você pode criar uma simulação personalizada para ver o efeito de usar uma estratégia de gastos ou orçamento de aprendizado diferente sem considerar as restrições ativas em unidades de oferta no portfólio. Você pode visualizar o desempenho estimado nos níveis de portfólio, campanha, unidade de oferta e dispositivo.

#### Simulações personalizadas baixadas

Cada simulação personalizada baixada consiste em uma pasta de trabalho. Cada pasta de trabalho inclui uma planilha para cada nível de simulação de entidade especificado (portfólios, campanhas, grupos de anúncios, unidades de oferta) quando os dados estiverem disponíveis para esse nível. Quando você especifica dados de nível de dispositivo, cada planilha inclui uma coluna [!UICONTROL Device]. Cada planilha inclui uma linha com dados para cada entidade aplicável e (quando especificado para o relatório) e tipo de dispositivo para cada uma das 20 etapas (por exemplo, uma linha por campanha). Os dados em cada linha incluem o custo marginal projetado para a receita, o custo, os cliques, a receita ponderada (valor do objetivo), o tipo de dispositivo e as métricas de conversão incluídas no objetivo, com base no destino correspondente. A planilha de nível de portfólio também inclui o target para os níveis da etapa, e a planilha de nível de entidade inclui a rede de publicidade, a conta, a campanha e (quando aplicável) o grupo de publicidade.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Detalhes da simulação personalizada na tela

Os detalhes da simulação na tela mostram insights visuais e tabulares em nível de portfólio. Para dados por campanha, grupos de anúncios, unidades de oferta ou dispositivo, [baixe a simulação](simulation-download.md).

#### Exibição em gráfico

A exibição em gráfico mostra o valor do objetivo esperado ou outra métrica especificada ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) para o destino de gasto para o número especificado de níveis de gasto (etapas) para a simulação. O ponto médio do público-alvo é identificado. Mantenha o cursor sobre qualquer ponto do gráfico para ver os dados desse ponto.

Quando a simulação é criada levando-se em consideração as restrições, as restrições aplicadas são identificadas acima do gráfico.

##### Visualização em tabela

A exibição de tabela mostra a meta de gasto para cada um dos números especificados de níveis de gasto (etapas) para a simulação. Ele também mostra o custo estimado correspondente, o custo marginal para o valor do objetivo, cliques, valor do objetivo e métricas de conversão no objetivo do portfólio para cada nível de gastos. O ponto médio do público-alvo é identificado.

Quando a simulação é criada levando-se em consideração as restrições, as restrições aplicadas são identificadas acima do gráfico.

##### Configurações de simulação

As configurações da simulação são mostradas como somente leitura abaixo do gráfico ou tabela.

##### Configurações do Portfolio

Para ver as configurações somente leitura do portfólio aplicável, clique em **[!UICONTROL Portfolio Settings]** no canto superior direito.

## A visualização [!UICONTROL Simulations]

A exibição [!UICONTROL Simulations] lista simulações semanais e simulações personalizadas. O administrador e alguns outros tipos de usuário<!-- Verify which --> podem ver simulações personalizadas criadas por outros usuários. Todos os outros usuários podem ver somente as simulações personalizadas que criam.

A tabela de dados inclui o progresso de cada simulação; uma coluna [!UICONTROL Target Midpoint] preenchida para cada linha; e colunas para previsões de valor de custo/impressão/clique/objetivo, valores reais e precisão. Opcionalmente, é possível adicionar mais colunas personalizadas (incluindo métricas de aumento, como o valor do objetivo real dividido pelo custo).

### Ações disponíveis {#simulations-actions}

* [Personalize a exibição](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) para incluir métricas adicionais, incluindo as impressões estimadas; o custo real, os cliques, as impressões e o valor do objetivo; o valor do custo para o objetivo; a precisão do custo, a precisão do clique e a precisão do valor do objetivo; e a diferença (delta) entre o valor do objetivo previsto e real e o valor do custo para o objetivo. Você também pode incluir colunas para a maioria das configurações de simulação e o tipo de simulação ([!UICONTROL Custom] ou [!UICONTROL Weekly]).

* [Gere ou execute novamente uma simulação personalizada](simulation-create.md) para um único portfólio. Você pode criar uma nova simulação ou gerar novamente uma simulação existente na lista.

* [Exibir uma simulação semanal ou personalizada na tela](simulation-view.md).

* [Baixar simulações semanais e personalizadas](simulation-download.md) como [!DNL Microsoft Excel] pastas de trabalho em arquivos ZIP.

* Usando o botão [!UICONTROL Spend Planner], abra a ferramenta herdada Recomendação de gasto, que ajuda a identificar a distribuição de gastos ideal entre portfólios.

## Práticas recomendadas

Monitore relatórios de simulação nas seguintes situações:

* Antes de iniciar um portfólio para estimar o desempenho que você pode esperar com as configurações correspondentes; use pelo menos duas semanas de dados. Se os resultados da simulação indicarem um desempenho menor do que o esperado com base nos dados históricos das campanhas incluídas, investigue e resolva os problemas antes de iniciar o portfólio.

* Após qualquer alteração importante em um portfólio, como adicionar uma campanha ou alterar o objetivo. Se você fizer alterações na data de início da modelagem do portfólio, no peso de uma métrica de conversão ou no valor de clique de um objetivo, aguarde até depois de 17:00 PST no dia seguinte para executar a simulação, quando modelos de custo e receita atualizados estiverem disponíveis.

* Periodicamente, para monitorar tendências de desempenho no nível da métrica de conversão.

>[!MORELIKETHIS]
>
>* [Executar ou executar novamente uma simulação](simulation-create.md)
>* [Exibir detalhes da simulação](simulation-view.md)
>* [Baixar simulações](simulation-download.md)
