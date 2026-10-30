---
title: Editar uma experiência com direcionamento de árvore de decisão
description: Saiba como editar uma experiência de anúncio direcionada usando o editor de árvore decisória manual ou orientado por IA.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
source-wordcount: '655'
ht-degree: 0%
---
# Editar uma experiência com direcionamento de árvore de decisão

O editor orientado por IA (Beta) é aberto por padrão para experiências com direcionamento. Você pode trabalhar com o agente de IA, editar a tela diretamente ou abrir o editor manual existente.

## Abrir a experiência {#experience-open}

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir experiências específicas.

1. Siga um destes procedimentos:

   * Para abrir o editor orientado por IA:

     * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Edit]**.

     * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Edit]**.

   * Para abrir o editor manual:

     * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * No editor orientado por IA,

## Editar usando o editor orientado por IA (Beta) {#ai-editor}

1. [Abrir a experiência](#experience-open).

1. Descreva as alterações de direcionamento que você deseja na conversa. Identifique a ramificação afetada por seus destinos ou, quando mostrado na tela, pela ID do nó.

1. Revise a árvore atualizada e descreva outras alterações. Aguarde o assistente concluir o processamento antes de interagir com a tela.

1. (Opcional) Faça alterações diretamente na tela:

   * [Adicionar um destino de nível final](experience-target-node-add-final.md#ai-editor), [inserir um nível de destino](experience-target-node-add-inner.md#ai-editor) ou [adicionar um destino irmão](experience-target-node-add-sibling.md#ai-editor).

   * Edite os critérios de um destino clicando em **[!UICONTROL ...]** > **[!UICONTROL Edit]** ao lado do destino, alterando os valores e clicando em **[!UICONTROL Edit Node]**.

   * [Copiar nós e criações filho](experience-target-node-copy.md#ai-editor) ou [excluir um nó](experience-target-node-delete.md#ai-editor).

   * [Atribuir ou cancelar atribuição de pacotes criativos](experience-assign-creative-bundles.md#ai-editor).

   * [Personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) ou [as URLs de rastreamento](experience-tracking-urls-targeting.md#ai-editor).

1. [Salve a experiência](#save).

## Editar usando o editor manual {#manual-editor}

1. [Abrir a experiência](#experience-open).

1. (Experiências com status `[processing](experience-about.md#experience-statuses)`) Se for solicitado sobre um rascunho existente, não publicado, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Continue editing draft]** para revisar e continuar editando o rascunho.

   * Clique em **[!UICONTROL Discard and start again]** para descartar o rascunho e começar a partir da versão ao vivo.

   * Clique em **[!UICONTROL Cancel this edit]** para interromper a edição.

1. (Opcional) Ajuste o controle deslizante de zoom ou clique em ![Exibir como Árvore Vertical](/help/creative/assets/tree-vertical.png "Exibir como Árvore Vertical") ou ![Exibir como árvore horizontal](/help/creative/assets/tree-horizontal.png "Exibir como árvore horizontal") para alterar a orientação.

   Suas configurações de exibição são salvas até que você faça logoff.

1. Altere os targets e os elementos criativos conforme necessário:

   * [Adicionar um destino de nível final](experience-target-node-add-final.md#manual-editor), [inserir um destino entre nós](experience-target-node-add-inner.md#manual-editor) ou [adicionar um destino irmão](experience-target-node-add-sibling.md#manual-editor).

   * [Copiar nós e criações filho](experience-target-node-copy.md#manual-editor) ou [excluir um nó](experience-target-node-delete.md#manual-editor).

   * [Atribuir ou cancelar atribuição de pacotes criativos](experience-assign-creative-bundles.md#manual-editor).

   * [Personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) ou [as URLs de rastreamento](experience-tracking-urls-targeting.md#manual-editor).

1. [Salve a experiência](#save).

## Alternar editores ou editar as configurações de experiência {#switch-editors}

>[!IMPORTANT]
>
>Antes de sair do editor orientado por IA, salve as alterações na árvore que deseja manter. Alternar para o editor manual ou o formulário de experiência não transfere as alterações não salvas.

* **Editor orientado por IA para o editor manual:** Clique em **[!UICONTROL Manual Decision Tree]**. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Yes]** para descartar as alterações não salvas e abrir o editor manual, ou em **[!UICONTROL No]** para permanecer.

* **Editor orientado por IA para configurações gerais:** Clique em **[!UICONTROL Experience Form]** e em **[!UICONTROL Yes]** para descartar as alterações de árvore não salvas e abrir o formulário. Edite as [configurações gerais de experiência](experience-settings-targeting.md) e clique em **[!UICONTROL Save]**.

* **Editor manual para configurações gerais:** salve as alterações na árvore que deseja manter e clique em **[!UICONTROL Experience Form]**. Edite as [configurações gerais de experiência](experience-settings-targeting.md) e clique em **[!UICONTROL Save]**.

* **Configurações gerais para o editor orientado por IA:** Clique em **[!UICONTROL Decision Tree]**. Salvar alterações nas configurações gerais de uma experiência direcionada também abre o editor orientado por IA.

* **Editor manual para o editor orientado por IA:** Salve as alterações na árvore, retorne à exibição [!UICONTROL Experiences] e selecione **[!UICONTROL Edit]** para a experiência.

Para sair do editor orientado por IA sem abrir outro editor, clique em **[!UICONTROL Cancel]**. Clique em **[!UICONTROL Yes]** para descartar as alterações de árvore não salvas ou em **[!UICONTROL No]** para continuar editando.

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
>* [Adicionar um nó de destino ao nível final](experience-target-node-add-final.md)
>* [Inserir um nó de destino entre nós](experience-target-node-add-inner.md)
>* [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Atribuir criações a um nó final](experience-assign-creative-bundles.md)
>* [Personalizar as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md)
>* [Personalizar otimização criativa e agendamento](experience-optimization-scheduling-targeting.md)
>* [Exportar e implementar uma marca de experiência de anúncio para uma experiência ao vivo](/help/creative/experiences/experience-tag-export.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Exibir o log de alterações para uma experiência](/help/creative/experiences/experience-view-change-log.md)
