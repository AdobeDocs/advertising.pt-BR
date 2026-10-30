---
title: Criar uma experiência com direcionamento de árvore de decisão
description: Saiba como criar uma experiência de anúncio direcionada usando o editor de árvore decisória manual ou orientado por IA.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
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
source-wordcount: '715'
ht-degree: 0%
---
# Criar uma experiência com direcionamento de árvore de decisão

Crie uma experiência de anúncio direcionada usando uma árvore de decisão. Cada experiência usa anúncios de uma única biblioteca criativa.

O editor orientado por IA (Beta) é aberto por padrão. Você pode configurar a árvore por meio do agente de IA ou editar a tela diretamente. Você também pode alternar para o editor manual existente.

>[!NOTE]
>
>* Depois de criar uma experiência direcionada, você não pode alterá-la para uma experiência não direcionada, que usa um fluxo de trabalho diferente.
>* Certifique-se de que suas experiências de anúncio incluam direcionamento compatível com as campanhas em que você o implementará. O comportamento hierárquico do direcionamento pode variar de acordo com a DSP. Ao fazer upload de uma tag de experiência de anúncio para o Advertising DSP e anexá-la a uma disposição, o direcionamento no nível do anúncio é aplicado sobre o direcionamento no nível do posicionamento (e não em vez dele). Por exemplo, se uma disposição for direcionada a usuários na Austrália e um anúncio for direcionado a usuários no Japão, o anúncio será direcionado à ramificação &quot;Todos os outros&quot;.

## Criar a experiência

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Clique em **[!UICONTROL Create New Experience]**.

1. Insira as [configurações gerais de experiência](experience-settings-targeting.md), com **[!UICONTROL Targeting]** habilitado.

1. Clique em **[!UICONTROL Create]**.

   O editor de árvore decisória orientado por IA é aberto para a nova experiência.

1. Configure a árvore usando um dos procedimentos a seguir.

## Configure a árvore usando o editor orientado por IA (Beta) {#ai-editor}

1. Na conversa, descreva a estrutura de direcionamento desejada, incluindo os critérios para cada ramificação e como lidar com visualizadores que não correspondem a um destino especificado.

1. Revise a árvore na tela. Para solicitar alterações, descreva-as na conversa. Aguarde o assistente concluir o processamento antes de interagir com a tela.

1. (Opcional) Refine a árvore diretamente na tela de desenho:

   * [Adicionar um destino de nível final](experience-target-node-add-final.md#ai-editor), [inserir um nível de destino](experience-target-node-add-inner.md#ai-editor) ou [adicionar um destino irmão](experience-target-node-add-sibling.md#ai-editor).

   * [Copiar nós e criações filho](experience-target-node-copy.md#ai-editor) ou [excluir um nó](experience-target-node-delete.md#ai-editor).

1. [Atribua pacotes criativos aos nós finais](experience-assign-creative-bundles.md#ai-editor) e, opcionalmente, [personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) e as [URLs de rastreamento](experience-tracking-urls-targeting.md#ai-editor).

   Para publicar a experiência, você deve atribuir pacotes a cada nó final ou usar as criações padrão da experiência. Você pode atribuir padrões a nós não atribuídos ao salvar.

1. (Opcional) Edite as configurações gerais de experiência:

   1. Para salvar as alterações na árvore que deseja manter, clique em **[!UICONTROL Save]**.

   1. Clique em **[!UICONTROL Experience Form]** e em **[!UICONTROL Yes]** para descartar as alterações de árvore não salvas e abrir o formulário.

   1. Edite as [configurações gerais de experiência](experience-settings-targeting.md) e clique em **[!UICONTROL Save]**.

      O editor orientado por IA é aberto.

1. [Salve a experiência](#save).

## Configurar a árvore usando o editor manual {#manual-editor}

1. No editor orientado por IA, clique em **[!UICONTROL Manual Decision Tree]** e em **[!UICONTROL Yes]** para sair do editor orientado por IA.

   Salve todas as alterações do editor de IA que você deseja manter antes de alternar. A confirmação do switch descarta as alterações de árvore não salvas.

1. (Opcional) Altere as configurações de exibição:

   * Aumente ou diminua o zoom movendo o controle deslizante.

   * Alternar entre as exibições vertical e horizontal clicando em ![Exibir como Árvore Vertical](/help/creative/assets/tree-vertical.png "Exibir como Árvore Vertical") ou ![Exibir como árvore horizontal](/help/creative/assets/tree-horizontal.png "Exibir como árvore horizontal").

   Suas configurações de exibição são salvas até que você faça logoff.

1. Configure os públicos-alvo de anúncios e as criações correspondentes:

   * [Adicionar um destino de nível final](experience-target-node-add-final.md#manual-editor), [inserir um destino entre nós](experience-target-node-add-inner.md#manual-editor) ou [adicionar um destino irmão](experience-target-node-add-sibling.md#manual-editor).

   * [Copiar nós e criações filho](experience-target-node-copy.md#manual-editor) ou [excluir um nó](experience-target-node-delete.md#manual-editor).

   * [Atribuir pacotes criativos](experience-assign-creative-bundles.md#manual-editor) e, opcionalmente, [personalizar a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) e [rastrear URLs](experience-tracking-urls-targeting.md#manual-editor).

1. (Opcional) Para editar as configurações gerais de experiência, clique em **[!UICONTROL Experience Form]** e edite as [configurações gerais de experiência](experience-settings-targeting.md).

1. [Salve a experiência](#save).

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores.

{{$include /help/_includes/experience-save.md}}

## Tags de anúncio e transcodificação de vídeo para experiências salvas

Quando a experiência é em tempo real, o [!DNL Creative] cria automaticamente uma tag de anúncio para cada tamanho de criação ou duração de vídeo aplicável. Em seguida, você pode [exportar uma marca de anúncio e implementá-la em uma DSP](/help/creative/experiences/experience-tag-export.md).

Para experiências de anúncio de vídeo, os recursos de criação de vídeo são transcodificados automaticamente pelo Adobe Advertising DSP como tags VAST 2.0 para que você possa visualizá-los. Opcionalmente, [aplique a transcodificação de uma DSP](experience-tag-video-transcoding.md) diferente a qualquer marca de experiência de vídeo e anúncios.

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
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Exibir o log de alterações para uma experiência](/help/creative/experiences/experience-view-change-log.md)
