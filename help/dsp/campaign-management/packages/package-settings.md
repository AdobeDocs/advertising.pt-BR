---
title: Configurações do pacote
description: Consulte descrições das configurações de pacote disponíveis.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 5a173c53bdd0a5673c968b1ebc6348a40e99c80c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Configurações do pacote

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** O nome do pacote. O comprimento máximo é de 60 caracteres.

**[!UICONTROL Description]:** (Opcional) Uma descrição do pacote.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Uma taxa estática de terceiros a ser rastreada como um custo não faturável:

>[!NOTE]
>
>As taxas faturáveis são refletidas na [!UICONTROL Net CPM] métrica.
>
* **[!UICONTROL CPM]:** O custo por 1000 impressões (CPM).

* **[!UICONTROL CPM Description]:** Uma descrição da taxa de CPM.

É possível substituir a configuração no nível do pacote na [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Somente leitura para pacotes existentes) Em que nível colocar e limitar as disposições no pacote:

* **[!UICONTROL Package level pacing]:** Essa estratégia de ritmo opera acompanhando e limitando todos os posicionamentos incluídos como um *grupo*. Essa estratégia garante que todos os posicionamentos em um determinado pacote sejam otimizados de forma holística, distribuindo gastos com base no desempenho e dimensionando para indicadores principais de desempenho (KPIs) selecionados.

* **[!UICONTROL Placement level pacing]:**  Essa estratégia de ritmo opera acompanhando e limitando todos os posicionamentos incluídos *individualmente*. A prática recomendada é usar essa estratégia apenas para executar negócios garantidos de mercados privados.

**[!UICONTROL Flight Dates]:** A data inicial e a data final do pacote.

Como opção, para criar voos não uniformes para o pacote, selecione *[!UICONTROL *Activate Custom Flighting]** e configurar os voos personalizados no [!UICONTROL Flighting] abaixo. Depois de habilitar a sinalização personalizada e salvar o pacote, não é possível desativar a sinalização personalizada.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha. Além disso, as datas de voo de todas as colocações atribuídas a este pacote devem ser incluídas nessas datas.
> * Não é possível editar a data de início do pacote quando a iluminação personalizada está ativada.

**[!UICONTROL Budget]:** (Pacotes com ritmo no nível do pacote somente) O limite de orçamento bruto e o intervalo de orçamento.

Para pacotes com configuração personalizada, o intervalo do orçamento é sempre *[!UICONTROL All time]*. Para pacotes sem configuração personalizada, especifique o intervalo do orçamento: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pacotes com ritmo no nível do pacote e gerenciamento dinâmico de margem somente) O limite de orçamento bruto para a duração do pacote.

**[!UICONTROL Optimization Goal]:** (Pacotes com ritmo no nível do pacote somente) A meta de otimização do pacote. Consulte descrições de cada meta de otimização em [Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Pacotes com o &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; metas de otimização apenas) Uma [meta personalizada](/help/dsp/optimization/custom-goal.md) que inclui os eventos de receita ou conversão usados para calcular a métrica de CPA ou ROAS. A meta personalizada pode incluir, opcionalmente, eventos ponderados adicionais de funil superior (como visitas a páginas e adições ao carrinho de compras) a serem usados além da métrica de CPA ou ROAS para otimização de pacote. Para obter mais informações sobre as práticas recomendadas para metas personalizadas e campanhas que as usam, consulte [Práticas recomendadas para a criação de uma meta personalizada](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) e [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md).<!-- At some point, all of the objectives will be prefixed with "ADSP " -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Opcional; pacotes com &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; (somente metas de otimização) Instrui o modelo de otimização a aprender somente com conversões baseadas em cliques. Caso contrário, o modelo de otimização aprende com conversões baseadas em cliques e impressões.

**[!UICONTROL Conversion Metric]:** (Opcional; pacotes com &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; somente metas de otimização) O evento de conversão final (como inscrições) ou o valor de evento/venda de receita (como compras e valores de compra) a ser usado para calcular o retorno do investimento em anúncios ou o custo por aquisição. Selecione em uma lista de todos os eventos principais (&quot;métricas de meta&quot;) mapeados para a meta personalizada selecionada. Se a lista estiver vazia, edite a meta personalizada para incluir pelo menos um dos eventos subjacentes como uma métrica de meta.

**[!UICONTROL Package Goal Type]:** (Pacotes somente com metas de otimização personalizadas) A finalidade do pacote. Esta configuração ajuda a determinar como otimizar o pacote:

* *[!UICONTROL Prospecting]:* Os pacotes de prospecção se concentram na aquisição de novos clientes.

* *[!UICONTROL Retargeting]:* Os pacotes de redirecionamento se concentram na reexposição de visitantes ou clientes anteriores.

* *[!UICONTROL Other]:* Todos os outros fins.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Pacotes somente com metas de otimização personalizadas) Outro pacote cujos dados históricos são usados como entrada para otimização do pacote.

**[!UICONTROL Target]:** (Pacotes com ritmo no nível do pacote somente) A meta do, que é usada para rastrear o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para decisões.

**[!UICONTROL Frequency Cap]:** (Pacotes com ritmo no nível do pacote somente) O número de vezes que um dispositivo exclusivo, ID universal ou pessoa (dependendo do estado especificado) [!UICONTROL Cross Device Level] para a campanha e o posicionamento [!UICONTROL Targeting] ) podem ser veiculadas com anúncios do pacote. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
>* Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.
>* A prática recomendada é definir limites de frequência para prospecção e redirecionamento no nível do pacote.
> * Limites de frequência mais altos resultam em gastos e impressões mais altos, mas com menor alcance. Limites de frequência mais baixos resultam em gastos e impressões mais baixos, mas em maior alcance.

**[!UICONTROL Pace on]:** (Pacotes com ritmo no nível do pacote somente) Em que ritmo se baseia:

* *[!UICONTROL Budget]:* (Padrão) Essa opção fornece o máximo de impressões possível dentro do orçamento do pacote alocado.

* *[!UICONTROL Impressions]:* Essa opção fornece impressões até que uma quantidade especificada seja atingida em um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *O tempo todo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pacotes com ritmo no nível do pacote somente) Como acompanhar e entregar durante todo o voo:

* *[!UICONTROL Even]:* Acompanha o delivery de forma uniforme em cada voo, com uma meta de 50% do delivery na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (O padrão) Acelera a entrega para que esteja 55 a 65% concluído na metade da duração do voo.

* *[!UICONTROL Frontload]:* Acelera a entrega para que esteja 65 a 75% concluído na metade do voo.

* *[!UICONTROL Aggressive Frontload]:* Acelera a entrega para que esteja 75 a 85% concluído na metade do voo.

**[!UICONTROL Intraday pacing]:** (Pacotes com ritmo no nível do pacote somente) Como acompanhar e entregar em cada dia dentro do voo:

* *[!UICONTROL Even]:* (O padrão) Dimensiona a entrega com base na disponibilidade do inventário. Geralmente, mais anúncios são entregues por hora durante o dia, quando o volume do leilão é maior, e menos anúncios são entregues de manhã e à noite.

* *[!UICONTROL ASAP]:* Acelera a entrega para o dobro da velocidade de *Par*.

  >[!CAUTION]
  >
  >Essa opção pode afetar negativamente o desempenho. Use-a somente quando estiver priorizando totalmente o delivery e o gasto em relação à otimização de desempenho.

## [!UICONTROL Flighting]

(Pacotes com ritmo no nível do pacote e com &quot;[!UICONTROL Activate Custom Flighting]&quot; ativado) Períodos de voo personalizados dentro do intervalo [!UICONTROL Flight Dates] especificado na [!UICONTROL Goals & Budget] seção.

Para cada voo, insira a data de início, a data de término e a meta de gastos. Para adicionar outro voo, clique em **[!UICONTROL Add Flight]**.

Para pacotes existentes, você pode opcionalmente informar um valor no campo [!UICONTROL Rollover] para qualquer voo para adicionar um orçamento potencial não gasto ao próximo voo. O valor projetado no [!UICONTROL Adjusted Goal (Goal + Rollover)] é alterada de acordo.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Anexar um posicionamento a um pacote](package-attach-placement.md)
>* [Exibir o Log de Alterações de um Pacote](package-change-log.md)
>* [Perguntas frequentes sobre o Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
