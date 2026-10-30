---
title: Personalizar a otimização criativa e o agendamento de uma experiência
description: Saiba como configurar a otimização e o agendamento de anúncios para experiências direcionadas.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%
---
# Personalize a otimização criativa e o agendamento de uma experiência com direcionamento de árvore de decisão

*Nós do Target somente com criações existentes*

Por padrão, uma experiência otimiza a rotação criativa para a taxa geral de cliques em todos os pacotes atribuídos. Você pode personalizar as configurações de rotação ou agendar pacotes específicos para execução durante períodos sequenciais, com configurações de rotação separadas para cada agendamento.

>[!NOTE]
>
>Esses recursos não estão disponíveis para nós que usam as criações padrão em vez das criações atribuídas.

Você pode definir essas configurações diretamente na tela do editor orientado por IA (Beta) ou no editor manual. Em qualquer editor, salvar a caixa de diálogo de pacote atualiza a árvore de trabalho. Você também deve [salvar a experiência](#save) do cabeçalho da árvore.

## Configurações de rotação {#rotation-settings}

* **[!UICONTROL Weighted]:** Mostra as variantes de anúncios nos pacotes criativos associados de acordo com pesos relativos.

* **[!UICONTROL Algorithmic]:** mostra as variantes de anúncios mais eficazes com mais frequência, com base em uma meta de otimização especificada, como a taxa de cliques ou uma meta personalizada de Advertising DSP.

* **[!UICONTROL Sequence] (editor orientado por IA) ou [!UICONTROL Sequencing] (editor manual):** Mostra os pacotes criativos associados em uma ordem especificada, com um número especificado de impressões para cada pacote na sequência. Por padrão, os pacotes são sequenciados na ordem em que foram adicionados à experiência. Os tamanhos dos anúncios exibidos são determinados pelo inventário disponível. O pacote final pode servir indefinidamente (o padrão) ou a sequência pode retornar ao primeiro pacote.

  Por exemplo, uma sequência pode servir variantes de anúncio do Pacote 1 para três impressões, Pacote 2 para uma impressão e Pacote 3 para duas impressões e, em seguida, repetir. Sem looping, o Pacote 3 continua a servir indefinidamente.

## Configurar otimização criativa sem programação

Quando o agendamento criativo está desativado, as configurações de otimização criativa se aplicam a todas as criações atribuídas.

### Uso do editor orientado por IA (Beta) {#without-scheduling-ai}

1. Enquanto você estiver [criando](experience-create-targeting.md#ai-editor) ou [editando](experience-edit-targeting.md#ai-editor) a experiência, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** no nó de folha criativo.

   Para um nó final sem pacotes, clique em **[!UICONTROL Assign Bundles]** e [atribuir os pacotes](experience-assign-creative-bundles.md#ai-editor) primeiro.

1. Abra a guia **[!UICONTROL Creative optimisation]**.

1. Desabilitar **[!UICONTROL Schedule]**.

1. Selecione o tipo de rotação criativa e defina suas configurações:

   * **[!UICONTROL Weighted]:** Insira o peso relativo para cada linha do pacote. Os pesos devem totalizar 100. Para distribuir pesos igualmente, clique em **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** Selecione uma opção **[!UICONTROL Optimization goals]**. Se você escolher um objetivo personalizado, selecione a [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente em **[!UICONTROL Custom objective]**.

   * **[!UICONTROL Sequence]:** Arraste os pacotes na ordem desejada e insira o número de impressões para cada sequência. Habilite **[!UICONTROL Keep in loop]** para repetir a sequência ou deixe-a desabilitada para definir as impressões do último pacote como **[!UICONTROL Infinite]**.

1. Clique em **[!UICONTROL Save]** no diálogo.

1. [Salve a experiência](#save).

### Usar o editor manual {#without-scheduling-manual}

[Abra o editor manual](experience-edit-targeting.md#experience-open) antes de seguir essas etapas.

1. Ao [criar](experience-create-targeting.md) ou [editar](experience-edit-targeting.md) a experiência, abra as configurações de otimização criativa:

   1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e faça o seguinte:

      * Para pacotes existentes, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Para novos pacotes, clique em **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** e [atribuir os pacotes](experience-assign-creative-bundles.md).

   1. Clique na guia **[!UICONTROL Creative Optimization]**.

1. Desabilitar **[!UICONTROL Schedule]**.

1. Selecione o tipo de rotação criativa para variantes de anúncios nos pacotes associados:

   * *[!UICONTROL Weighted]:* Insira o peso de cada pacote como uma porcentagem. Para aplicar pesos iguais a todos os pacotes associados, clique em (![Aplicar peso igual](/help/creative/assets/apply-equal-weight.png "Aplicar peso igual")). Os pesos de todos os pacotes selecionados devem somar 100.

   * *[!UICONTROL Algorithmic]:* Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]*, (experiências de anúncio de vídeo padrão) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*. Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

   * *[!UICONTROL Sequencing]:*

     1. Arraste e solte os pacotes atribuídos na ordem desejada.

     1. Insira o número de impressões para cada sequência.

     1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Clique em **[!UICONTROL Save]**.

## Configurar a otimização criativa com programação criativa

Opcionalmente, é possível agendar pacotes de criação específicos para execução durante períodos de tempo sequenciais especificados entre as datas de início e término da experiência e aplicar configurações personalizadas de rotação de criação para cada programação. Por exemplo, você pode agendar o Pacote 1 para execução durante as duas primeiras semanas para otimizar a taxa de click-through e o Pacote 2 para execução durante as duas semanas seguintes para otimizar para uma meta personalizada especificada.

Ao usar o agendamento, você deve agendar pacotes pela duração da experiência.

### Uso do editor orientado por IA (Beta) {#with-scheduling-ai}

1. Enquanto você estiver [criando](experience-create-targeting.md#ai-editor) ou [editando](experience-edit-targeting.md#ai-editor) a experiência, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** no nó de folha criativo.

   Para um nó final sem pacotes, clique em **[!UICONTROL Assign Bundles]** e [atribuir os pacotes](experience-assign-creative-bundles.md#ai-editor) primeiro.

1. Abra a guia **[!UICONTROL Creative optimisation]** e habilite **[!UICONTROL Schedule]**.

1. Selecione o **[!UICONTROL Timezone]** para o cronograma.

1. Para o primeiro agendamento:

   1. Marque a caixa de seleção ao lado de cada pacote a ser incluído na coluna à esquerda.

   1. Especifique as datas e horas de início e término.

   1. Selecione o tipo de rotação criativa e defina suas configurações:

      * **[!UICONTROL Weighted]:** Insira o peso relativo para cada linha do pacote na agenda. Os pesos devem totalizar 100. Para distribuir pesos igualmente, clique em **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** Selecione uma opção **[!UICONTROL Optimization goals]**. Se você escolher um objetivo personalizado, selecione a [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente em **[!UICONTROL Custom objective]**.

      * **[!UICONTROL Sequence]:** Arraste os pacotes na ordem desejada e insira o número de impressões para cada sequência. Habilite **[!UICONTROL Keep in loop]** para repetir a sequência ou deixe-a desabilitada para definir as impressões do último pacote como **[!UICONTROL Infinite]**.

1. Para cada agendamento adicional, clique em **[!UICONTROL + Add Schedule]**, selecione seu cartão de agendamento e configure seus pacotes, datas e horas, além das configurações de rotação.

   As caixas de seleção de pacote se aplicam à programação selecionada, não a todas as programações. Verifique se os agendamentos cobrem toda a duração da experiência com pacotes atribuídos.

1. Clique em **[!UICONTROL Save]** no diálogo.

1. [Salve a experiência](#save).

### Usar o editor manual {#with-scheduling-manual}

[Abra o editor manual](experience-edit-targeting.md#experience-open) antes de seguir essas etapas.

1. Ao [criar](experience-create-targeting.md) ou [editar](experience-edit-targeting.md) a experiência, abra as configurações de otimização criativa:

   1. Mantenha o cursor sobre o nó folha criativa abaixo do nó de destino e faça o seguinte:

      * Para pacotes existentes, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Para novos pacotes, clique em **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** e [atribuir os pacotes](experience-assign-creative-bundles.md).

   1. Clique na guia **[!UICONTROL Creative Optimization]**.

1. Habilitar **[!UICONTROL Schedule]**.

1. Para o primeiro agendamento:

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique a data e hora de início e a data e hora de término para o cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Insira o peso de cada pacote como uma porcentagem. Para aplicar pesos iguais a todos os pacotes no agendamento, clique em (![Aplicar peso igual](/help/creative/assets/apply-equal-weight.png "Aplicar peso igual")). Os pesos de todos os pacotes selecionados devem somar 100.

      * *[!UICONTROL Algorithmic]:* Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]*, (experiências de anúncio de vídeo padrão) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*. Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:*

        1. Arraste e solte os pacotes atribuídos na ordem desejada.

        1. Insira o número de impressões para cada sequência.

        1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Para cada agendamento adicional:

   1. Clique em **[!UICONTROL + Add Schedule]**.

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada pacote criativo a ser adicionado à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * *[!UICONTROL Weighted]:* Insira o peso de cada pacote como uma porcentagem. Os pesos de todos os pacotes selecionados devem somar 100.

      * *[!UICONTROL Algorithmic]:* Para **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*. Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.

      * *[!UICONTROL Sequencing]:*

        1. Arraste e solte os pacotes atribuídos na ordem desejada.

        1. Insira o número de impressões para cada sequência.

        1. Para a última sequência, altere para a\) exibir o pacote final na sequência indefinidamente (*[!UICONTROL Infinite]* (o padrão) ou b\) voltar para o primeiro pacote após o pacote final ser exibido (*[!UICONTROL Keep in Loop]*).

1. Clique em **[!UICONTROL Save]**.

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizar as URLs de rastreamento para criações](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [Exibir o log de alterações para uma experiência](/help/creative/experiences/experience-view-change-log.md)
