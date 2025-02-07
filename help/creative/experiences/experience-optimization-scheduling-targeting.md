---
title: Personalizar a otimização criativa e o agendamento de uma experiência
description: Saiba como
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Personalize a otimização criativa e o agendamento de uma experiência com direcionamento de árvore de decisão

*Nós do Target somente com criações existentes*
*Beta fechado*

Por padrão, a rotação criativa de uma experiência é determinada de forma algorítmica para otimizar a taxa geral de cliques, e as configurações de otimização criativa se aplicam a todos os pacotes atribuídos. Você pode personalizar a rotação criativa para executar manualmente as criações em cada pacote de acordo com pesos relativos ou otimizar de forma algorítmica para uma meta personalizada do Advertising DSP especificada. <!-- verify --> Também é possível agendar a execução de pacotes criativos específicos durante períodos sequenciais especificados e aplicar configurações personalizadas de rotação de criação para cada agendamento.

>[!NOTE]
>
>Esses recursos não estão disponíveis para nós que usam as criações de imagem padrão em vez de criações atribuídas.

## Configurar otimização criativa sem programação

Quando o agendamento criativo está desativado, as configurações de otimização criativa se aplicam a todas as criações atribuídas.

1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Desabilitar **[!UICONTROL Schedule]**.

1. Selecione o tipo de rotação criativa:

   * ** *Ponderado* ** — Gira os elementos de criação em cada pacote manualmente de acordo com os pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes devem somar 100.

   * ** *Algorítmico* ** — Gira as criações em cada pacote de forma algorítmica de acordo com uma meta de otimização especificada.

   * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Clique em **[!UICONTROL Save]**.

## Configurar a otimização criativa com programação criativa

Opcionalmente, é possível agendar pacotes de criação específicos para execução durante períodos de tempo sequenciais especificados entre as datas de início e término da experiência e aplicar configurações personalizadas de rotação de criação para cada programação. Por exemplo, você pode agendar o Pacote 1 para execução durante as duas primeiras semanas para otimizar a taxa de click-through e o Pacote 2 para execução durante as duas semanas seguintes para otimizar para uma meta personalizada especificada.

Ao usar o agendamento, você deve agendar pacotes pela duração da experiência.

1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para o primeiro agendamento:

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * ** *Ponderado* ** — Gira os elementos de criação em cada pacote manualmente de acordo com os pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar 100.

      * ** *Algorítmico* ** — Gira as criações em cada pacote de forma algorítmica de acordo com uma meta de otimização especificada.

      * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Para cada agendamento adicional:

   1. Clique em **[!UICONTROL + Add Schedule]**.

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * ** *Ponderado* ** — Gira os elementos de criação em cada pacote manualmente de acordo com os pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar 100.

      * ** *Algorítmico* ** — Gira as criações em cada pacote de forma algorítmica de acordo com uma meta de otimização especificada.

      * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar as URLs de rastreamento para criações](/help/creative/experiences/experience-tracking-urls-targeting.md)
