---
title: Personalizar a otimização criativa e o agendamento de uma experiência
description: Saiba como
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 7bcafc7c70333bb6f523873ed08f2bc5123823f7
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Personalize a otimização criativa e o agendamento de uma experiência com direcionamento de árvore de decisão

*Nós do Target somente com criações existentes*

Por padrão, a rotação criativa de uma experiência é determinada de forma algorítmica para otimizar a taxa geral de cliques, e as configurações de otimização criativa se aplicam a todos os pacotes atribuídos. Você pode, alternativamente, otimizar de forma algorítmica para uma meta personalizada do Advertising DSP especificada; girar pacotes de acordo com uma sequência de pacotes especificada, com um número especificado de impressões em cada sequência de pacotes; ou de acordo com pesos relativos. Você também pode agendar pacotes criativos específicos para execução durante períodos de tempo sequenciais especificados e aplicar configurações de rotação criativa personalizadas para cada agendamento.

>[!NOTE]
>
>Esses recursos não estão disponíveis para nós que usam as criações padrão em vez das criações atribuídas.

## Configurar otimização criativa sem programação

Quando o agendamento criativo está desativado, as configurações de otimização criativa se aplicam a todas as criações atribuídas.

1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Desabilitar **[!UICONTROL Schedule]**.

1. Selecione o tipo de rotação criativa para variantes de anúncios nos pacotes associados:

   * *[!UICONTROL Weighted]:* Mostra as variantes de anúncios nos pacotes criativos associados de acordo com pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar até 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* mostra as variantes de anúncios mais eficazes com mais frequência, com base em uma meta especificada.

      * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]*, (experiências de anúncio de vídeo padrão) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

   * *[!UICONTROL Sequencing]:* Mostra os pacotes criativos associados em uma ordem especificada (com o Pacote 1 entregue primeiro, Pacote 2 entregue segundo e assim por diante), com um número total especificado de impressões em cada sequência de pacote. Os tamanhos dos anúncios exibidos são determinados pelo inventário disponível. Você pode configurar o pacote final na sequência para a\) ser exibido indefinidamente (o padrão) ou b\) voltar para o primeiro pacote. Por exemplo, você pode exibir qualquer uma das variantes de anúncios no Pacote 1 para três (3) impressões, em seguida, exibir qualquer variante de anúncios no Pacote 2 para uma (1) impressão, em seguida, exibir qualquer uma das variantes de anúncios no Pacote 3 para duas (2) impressões e, em seguida, iniciar o loop novamente. Como alternativa, uma vez que as variantes de anúncios no Pacote 3 sejam exibidas, você pode continuar a exibir as variantes de anúncios no Pacote 3 indefinidamente, em vez de criar um loop. Ao habilitar o sequenciamento:

      1. Arraste e solte os pacotes atribuídos na ordem desejada.

     Por padrão, os pacotes atribuídos são sequenciados na ordem em que foram adicionados à experiência.

      1. Insira o número de impressões para cada sequência.

      1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Clique em **[!UICONTROL Save]**.

## Configurar a otimização criativa com programação criativa

Opcionalmente, é possível agendar pacotes de criação específicos para execução durante períodos de tempo sequenciais especificados entre as datas de início e término da experiência e aplicar configurações personalizadas de rotação de criação para cada programação. Por exemplo, você pode agendar o Pacote 1 para execução durante as duas primeiras semanas para otimizar a taxa de click-through e o Pacote 2 para execução durante as duas semanas seguintes para otimizar para uma meta personalizada especificada.

Ao usar o agendamento, você deve agendar pacotes pela duração da experiência.

1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para o primeiro agendamento:

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Gira manualmente as criações em cada pacote de acordo com pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar 100.

      * *[!UICONTROL Algorithmic]:* Gira as criações em cada pacote de forma algorítmica, de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]*, (experiências de anúncio de vídeo padrão) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:* Gira os pacotes criativos associados em uma ordem especificada (com o Pacote 1 entregue primeiro, Pacote 2 entregue segundo e assim por diante), com um número total especificado de impressões em cada sequência de pacote. Os tamanhos dos anúncios exibidos são determinados pelo inventário disponível. Você pode configurar o pacote final na sequência para a\) ser exibido indefinidamente (o padrão) ou b\) voltar para o primeiro pacote. Por exemplo, você pode exibir qualquer criação no Pacote 1 para três (3) impressões e, em seguida, exibir qualquer criação no Pacote 2 para uma (1) impressão e, em seguida, exibir qualquer uma das criações no Pacote 3 para duas (2) impressões e, em seguida, iniciar o loop novamente. Como alternativa, uma vez que as criações no Pacote 3 sejam exibidas, você pode continuar a exibir as criações no Pacote 3 indefinidamente, em vez de criar um loop. Ao habilitar o sequenciamento:

         1. Arraste e solte os pacotes atribuídos na ordem desejada.

            Por padrão, os pacotes atribuídos são sequenciados na ordem em que foram adicionados à experiência.

         1. Insira o número de impressões para cada sequência.

         1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Para cada agendamento adicional:

   1. Clique em **[!UICONTROL + Add Schedule]**.

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Gira manualmente as criações em cada pacote de acordo com pesos relativos. Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar 100.

      * *[!UICONTROL Algorithmic]:* Gira as criações em cada pacote de forma algorítmica, de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:* Gira os pacotes criativos associados em uma ordem especificada, com um número total especificado de impressões em cada sequência de pacote. Ao habilitar o sequenciamento:

         1. Arraste e solte os pacotes atribuídos na ordem desejada.

            Por padrão, os pacotes atribuídos são sequenciados na ordem em que foram adicionados à experiência.

         1. Insira o número de impressões para cada sequência.

         1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar as URLs de rastreamento para criações](/help/creative/experiences/experience-tracking-urls-targeting.md)
