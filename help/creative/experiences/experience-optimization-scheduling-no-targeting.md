---
title: Personalizar a otimização criativa e o agendamento de uma experiência
description: Saiba como configurar a otimização e o agendamento de anúncios para experiências sem direcionamento.
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---

# Personalize a otimização criativa e o agendamento de uma experiência sem o direcionamento da árvore de decisão

*Experiências somente com criações existentes*

Por padrão, a rotação criativa de uma tag de experiência de anúncio é determinada de forma algorítmica para otimizar a taxa geral de cliques, e as configurações de otimização criativa se aplicam a todas as criações atribuídas. Você pode personalizar a rotação criativa para executar manualmente as criações de acordo com pesos relativos ou otimizar de forma algorítmica para uma meta personalizada do Advertising DSP especificada. Você também pode programar criações específicas para serem executadas durante períodos de tempo sequenciais especificados e aplicar configurações de rotação de criação personalizadas para cada programação.

## Configurar otimização criativa sem programação

Quando o agendamento criativo está desativado, as configurações de otimização criativa se aplicam a todas as criações atribuídas.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**.

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Agendamento de anúncios](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Creative Optimization]**.&lt;!— O Tag Manager tem apenas uma visualização de lista, mas nenhuma visualização de cartão, a partir de 2/2. >

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

Opcionalmente, é possível agendar criações específicas usadas para uma tag de experiência de anúncio para execução durante períodos de tempo sequenciais especificados entre as datas de início e término da experiência e aplicar configurações personalizadas de rotação criativa para cada agendamento. Por exemplo, você pode agendar o Creative 1 para execução durante as duas primeiras semanas para otimizar a taxa de cliques e o Creative 2 para execução durante as duas semanas seguintes para otimizar uma meta personalizada especificada.

Ao usar o agendamento, você deve agendar criações pela duração da experiência.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**.

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Agendamento de anúncios](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Creative Optimization]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— O Tag Manager tem apenas uma visualização de lista, mas nenhuma visualização de cartão, a partir de 2/2. >

1. Habilitar **[!UICONTROL Schedule]**.

1. Para o primeiro agendamento:

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada criação a ser adicionada à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Gira as criações manualmente de acordo com os pesos relativos. Insira o peso de cada criação como uma porcentagem. Os pesos de todas as criações selecionadas devem somar 100.

      * *[!UICONTROL Algorithmic]:* Gira as criações de forma algorítmica, de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]*, (experiências de anúncio de vídeo padrão) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* Gira os pacotes criativos associados em uma ordem especificada (com o Pacote 1 entregue primeiro, Pacote 2 entregue segundo e assim por diante), com um número total especificado de impressões em cada sequência de pacote. Os tamanhos dos anúncios exibidos são determinados pelo inventário disponível. Você pode configurar o pacote final na sequência para a\) ser exibido indefinidamente (o padrão) ou b\) voltar para o primeiro pacote. Por exemplo, você pode exibir qualquer criação no Pacote 1 para três (3) impressões e, em seguida, exibir qualquer criação no Pacote 2 para uma (1) impressão e, em seguida, exibir qualquer uma das criações no Pacote 3 para duas (2) impressões e, em seguida, iniciar o loop novamente. Como alternativa, uma vez que as criações no Pacote 3 sejam exibidas, você pode continuar a exibir as criações no Pacote 3 indefinidamente, em vez de criar um loop. Ao habilitar o sequenciamento:

         1. Arraste e solte os pacotes atribuídos na ordem desejada.

            Por padrão, os pacotes atribuídos são sequenciados na ordem em que foram adicionados à experiência.

         1. Insira o número de impressões para cada sequência.

         1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Para cada agendamento adicional:

   1. Clique em **[!UICONTROL + Add Schedule]**.

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada criação a ser adicionada à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Gira as criações manualmente de acordo com os pesos relativos. Insira o peso de cada criação como uma porcentagem. Os pesos de todas as criações selecionadas devem somar 100.

      * *[!UICONTROL Algorithmic]:* Gira as criações de forma algorítmica, de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* Gira os pacotes criativos associados em uma ordem especificada, com um número total especificado de impressões em cada sequência de pacote. Ao habilitar o sequenciamento:

         1. Arraste e solte os pacotes atribuídos na ordem desejada.

            Por padrão, os pacotes atribuídos são sequenciados na ordem em que foram adicionados à experiência.

         1. Insira o número de impressões para cada sequência.

         1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Crie manualmente uma marca de anúncio para um tamanho criativo aplicável](/help/creative/experiences/experience-tag-create-manually.md)
>* [Atribuir criações a uma marca de anúncio para experiências sem direcionamento](experience-tag-assign-creatives.md)
>* [Personalizar as URLs de rastreamento para uma experiência sem o direcionamento da árvore de decisão](experience-tracking-urls-no-targeting.md)
