---
title: Personalizar a otimização criativa e o agendamento de uma experiência
description: Saiba como
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 4d0f4b2a46a65c7fa1afec0a4ef419e58b8f8f59
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Personalize a otimização criativa e o agendamento de uma experiência sem o direcionamento da árvore de decisão

*Experiências somente com criações existentes*
*Beta fechado*

Por padrão, a rotação criativa de uma tag de experiência de anúncio é determinada de forma algorítmica para otimizar a taxa geral de cliques, e as configurações de otimização criativa se aplicam a todas as criações atribuídas. Você pode personalizar a rotação criativa para executar manualmente as criações de acordo com pesos relativos ou otimizar de forma algorítmica para uma meta personalizada do Advertising DSP especificada. <!-- verify --> Você também pode agendar criações específicas para execução durante períodos de tempo sequenciais especificados e aplicar configurações personalizadas de rotação de criação para cada agendamento.

## Configurar otimização criativa sem programação

Quando o agendamento criativo está desativado, as configurações de otimização criativa se aplicam a todas as criações atribuídas.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Agendamento de anúncios](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— O Tag Manager tem apenas uma visualização de lista, mas nenhuma visualização de cartão, a partir de 2/2. >

1. Desabilitar **[!UICONTROL Schedule]**.

1. Selecione o tipo de rotação criativa:

   * &amp;ast;&amp;ast; *Ponderado* &amp;ast;&amp;ast; — Gira as criações manualmente de acordo com os pesos relativos. Insira o peso de cada criação como uma porcentagem. Os pesos de todas as criações selecionadas devem somar 100.

   * &amp;ast;&amp;ast; *Algorítmico* &amp;ast;&amp;ast; — Gira as criações de forma algorítmica de acordo com uma meta de otimização especificada.

      * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Clique em **[!UICONTROL Save]**.

## Configurar a otimização criativa com programação criativa

Opcionalmente, é possível agendar criações específicas usadas para uma tag de experiência de anúncio para execução durante períodos de tempo sequenciais especificados entre as datas de início e término da experiência e aplicar configurações personalizadas de rotação criativa para cada agendamento. Por exemplo, você pode agendar a execução do Creative 1 durante as primeiras duas semanas para otimizar a taxa de cliques e o Creative 2 para execução durante as duas semanas seguintes para otimizar uma meta personalizada especificada.

Ao usar o agendamento, você deve agendar criações pela duração da experiência.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Agendamento de anúncios](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— O Tag Manager tem apenas uma visualização de lista, mas nenhuma visualização de cartão, a partir de 2/2. >

1. Habilitar **[!UICONTROL Schedule]**.

1. Para o primeiro agendamento:

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada criação a ser adicionada à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * &amp;ast;&amp;ast; *Ponderado* &amp;ast;&amp;ast; — Gira as criações manualmente de acordo com os pesos relativos. Insira o peso de cada criação como uma porcentagem. Os pesos de todas as criações selecionadas devem somar 100.

      * &amp;ast;&amp;ast; *Algorítmico* &amp;ast;&amp;ast; — Gira as criações de forma algorítmica de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Para cada agendamento adicional:

   1. Clique em **[!UICONTROL + Add Schedule]**.

   1. Na coluna à esquerda, marque a caixa de seleção ao lado de cada criação a ser adicionada à primeira programação.

   1. Especifique as datas de início e término do cronograma.

   1. Selecione o tipo de rotação criativa:

      * &amp;ast;&amp;ast; *Ponderado* &amp;ast;&amp;ast; — Gira as criações manualmente de acordo com os pesos relativos. Insira o peso de cada criação como uma porcentagem. Os pesos de todas as criações selecionadas devem somar 100.

      * &amp;ast;&amp;ast; *Algorítmico* &amp;ast;&amp;ast; — Gira as criações de forma algorítmica de acordo com uma meta de otimização especificada.

         * Para o **[!UICONTROL Optimization Goal]**, selecione *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Se você selecionar *[!UICONTROL Custom Objective]*, selecione uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) existente.<!-- Verify -->

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Crie manualmente uma marca de anúncio para um tamanho criativo aplicável](/help/creative/experiences/experience-tag-create-manually.md)
>* [Atribuir criações a uma marca de anúncio para experiências sem direcionamento](experience-tag-assign-creatives.md)
>* [Personalizar as URLs de rastreamento para uma experiência sem o direcionamento da árvore de decisão](experience-tracking-urls-no-targeting.md)
