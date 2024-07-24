---
title: Configurações do pacote
description: Consulte descrições das configurações de pacote disponíveis.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 5ca730f519ab8273cd6aaf910b5b09487ed4d77e
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# Configurações do pacote

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** O nome do pacote. O comprimento máximo é de 60 caracteres.

**[!UICONTROL Description]:** (Opcional) Uma descrição do pacote.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Uma taxa estática de terceiros a ser rastreada como um custo não faturável:

* **[!UICONTROL CPM]:** O custo por 1000 impressões (CPM).

* **[!UICONTROL Description]:** Uma descrição da taxa de CPM.

>[!NOTE]
>
>Taxas faturáveis são refletidas na métrica [!UICONTROL Net CPM].

Você pode substituir a configuração no nível do pacote no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Somente leitura para pacotes existentes) Em que nível colocar e limitar posicionamentos no pacote:

* **[!UICONTROL Package level pacing]:** Essa estratégia de ritmo opera acompanhando e limitando todos os posicionamentos incluídos como um *grupo*. Essa estratégia garante que todos os posicionamentos em um determinado pacote sejam otimizados de forma holística, distribuindo gastos com base no desempenho e dimensionando para indicadores principais de desempenho (KPIs) selecionados.

* **[!UICONTROL Placement level pacing]:** Essa estratégia de ritmo opera acompanhando e limitando todos os posicionamentos incluídos *individualmente*. A prática recomendada é usar essa estratégia apenas para executar negócios garantidos de mercados privados.

**[!UICONTROL Flight Dates]:** A data de início e a data de término gerais do pacote. As datas de voo devem ser incluídas nas datas de voo da campanha.

>[!NOTE]
>
>* As datas de voo de todas as colocações atribuídas a este pacote devem ser incluídas nessas datas.
> * Não é possível editar a data de início do pacote quando a iluminação personalizada está ativada.

**[!UICONTROL Activate Custom Flighting]:** Permite criar voos não uniformes para o pacote na seção [!UICONTROL Flighting] abaixo. Depois de habilitar a pesquisa personalizada e salvar o pacote, não é possível desabilitar a pesquisa personalizada nem editar a data de início do pacote.

**[!UICONTROL Budget]:** (Pacotes com ritmo no nível do pacote somente) O limite de orçamento bruto e o intervalo de orçamento.

Para pacotes com fluxo personalizado, o intervalo de orçamento é sempre *[!UICONTROL All time]*. Para pacotes sem sinalização personalizada, especifique o intervalo de orçamento: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pacotes com ritmo no nível de pacote e gerenciamento dinâmico de margem apenas) O limite de orçamento bruto para a duração do pacote.

**[!UICONTROL Optimization Goal]:** (Pacotes com ritmo no nível de pacote somente) A meta de otimização do pacote. Consulte as descrições de cada meta de otimização em [Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Pacotes com apenas as metas de otimização &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) Uma [meta personalizada](/help/dsp/optimization/custom-goal.md) que inclui os eventos de receita ou conversão usados para calcular a métrica de CPA ou ROAS. A meta personalizada pode incluir, opcionalmente, eventos ponderados adicionais de funil superior (como visitas a páginas e adições ao carrinho de compras) a serem usados além da métrica de CPA ou ROAS para otimização de pacote. Para obter mais informações sobre metas personalizadas, incluindo as práticas recomendadas de criação de metas personalizadas e campanhas que as utilizam, consulte &quot;[Metas Personalizadas](/help/dsp/optimization/custom-goal.md)&quot; e &quot;[Práticas Recomendadas para Configurar Campanhas de Desempenho](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Opcional; pacotes com as metas de otimização &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; somente) Diz ao modelo de otimização para aprender somente a partir de conversões baseadas em cliques. Caso contrário, o modelo de otimização aprende com conversões baseadas em cliques e impressões.

**[!UICONTROL Conversion Metric]:** (Opcional; pacotes com as metas de otimização &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; somente) O evento de conversão final (como inscrições) ou o valor de evento de receita/venda (como compras e valores de compra) a serem usados para calcular o retorno sobre o gasto com anúncios ou o custo por aquisição. Selecione em uma lista de todos os eventos principais (&quot;métricas de meta&quot;) mapeados para a meta personalizada selecionada. Se a lista estiver vazia, edite a meta personalizada para incluir pelo menos um dos eventos subjacentes como uma métrica de meta.

**[!UICONTROL Package Goal Type]:** (pacotes com metas de otimização personalizadas apenas) A finalidade do pacote. Esta configuração ajuda a determinar como otimizar o pacote:

* *[!UICONTROL Prospecting]:* A prospecção de pacotes tem como foco a aquisição de novos clientes.

* *[!UICONTROL Retargeting]:* Os pacotes de redirecionamento se concentram em expor novamente visitantes ou clientes anteriores.

* *[!UICONTROL Other]:* Todas as outras finalidades.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Pacotes com metas de otimização personalizadas apenas) Outro pacote cujos dados históricos são usados como entrada para a otimização do pacote.

**[!UICONTROL Target]:** (Pacotes com ritmo no nível de pacote somente) A meta de destino, que é usada para acompanhar o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para decisões.

**[!UICONTROL Frequency Cap]:** (Pacotes com ritmo no nível do pacote somente) O número de vezes que um dispositivo exclusivo, ID universal ou pessoa (dependendo do [!UICONTROL Cross Device Level] especificado para a campanha e da configuração [!UICONTROL Targeting] do posicionamento) pode receber anúncios do pacote. As opções incluem *[!UICONTROL Unlimited]* ou um valor específico por dia, semana ou mês.

>[!NOTE]
>
>* Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.
>* A prática recomendada é definir limites de frequência para prospecção e redirecionamento no nível do pacote.
> * Limites de frequência mais altos resultam em gastos e impressões mais altos, mas com menor alcance. Limites de frequência mais baixos resultam em gastos e impressões mais baixos, mas em maior alcance.

**[!UICONTROL Pace on]:** (Pacotes somente com ritmo de nível de pacote) Em que o ritmo se baseia:

* *[!UICONTROL Budget]:* (Padrão) Essa opção fornece o máximo de impressões possível dentro do orçamento do pacote alocado.

* *[!UICONTROL Impressions]:* Essa opção fornece impressões até que uma quantidade especificada seja atingida dentro de um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *Todos os tempos,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pacotes com ritmo no nível do pacote somente) Como acompanhar e entregar durante todo o voo:

* *[!UICONTROL Even]:* Acompanha a entrega uniformemente em cada voo, com uma meta de 50% da entrega na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (o padrão) Acelera a entrega para que esteja 55 a 65% concluído na metade da duração do voo.

* *[!UICONTROL Frontload]:* acelera a entrega, de modo que esteja 65 a 75% concluído na metade do processo.

* *[!UICONTROL Aggressive Frontload]:* acelera a entrega, de modo que esteja 75 a 85% concluído na metade do processo.

**[!UICONTROL Intraday pacing]:** (Pacotes com ritmo no nível do pacote somente) Como acompanhar e entregar em cada dia dentro do voo:

* *[!UICONTROL Even]:* (padrão) Dimensiona a entrega com base na disponibilidade de estoque. Geralmente, mais anúncios são entregues por hora durante o dia, quando o volume do leilão é maior, e menos anúncios são entregues de manhã e à noite.

* *[!UICONTROL ASAP]:* acelera a entrega para o dobro da velocidade de *Even*.

  >[!CAUTION]
  >
  >Essa opção pode afetar negativamente o desempenho. Use-a somente quando estiver priorizando totalmente o delivery e o gasto em relação à otimização de desempenho.

## [!UICONTROL Flighting]

(Pacotes com ritmo no nível do pacote) Os períodos de execução do pacote, incluindo quaisquer períodos de execução personalizados dentro do [!UICONTROL Flight Dates] geral do pacote. Você pode configurar voos personalizados somente quando a opção [!UICONTROL Activate Custom Flighting] está habilitada na seção [!UICONTROL Goals & Budget].

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (Disponível somente quando a opção [!UICONTROL Activate Custom Flighting] está habilitada) Adiciona automaticamente qualquer orçamento restante do voo anterior ao orçamento existente do próximo voo.

Na exibição [!UICONTROL Packages] e na exibição [!DNL Package Name] > [!UICONTROL Flights], o campo [!UICONTROL Interval Goal], que mostra a meta de voo atual, inclui qualquer orçamento de substituição.

**[!DNL Flight N]:** (Disponível somente quando a opção [!UICONTROL Activate Custom Flighting] estiver habilitada) Para cada voo, especifique a data de início, a data de término e a meta de gastos. Para adicionar outro voo, clique em **[!UICONTROL Add Flight]**.

Para pacotes existentes sem a opção &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; habilitada, você pode opcionalmente reabrir as configurações para inserir um valor na coluna **[!UICONTROL Rollover]** para qualquer voo para adicionar um orçamento não gasto potencial para o próximo voo.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Anexar um Posicionamento a um Pacote](package-attach-placement.md)
>* [Exibir o Log de Alterações de um Pacote](package-change-log.md)
>* [Perguntas frequentes sobre o Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
