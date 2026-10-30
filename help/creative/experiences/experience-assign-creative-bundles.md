---
title: Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência
description: Saiba como atribuir elementos de criação a cada público-alvo em suas experiências de anúncio.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: 'https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M'
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
source-wordcount: '453'
ht-degree: 0%
---
# Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência

*Experiências somente com direcionamento de árvore de decisão*

Você pode atribuir pacotes criativos a um nó de direcionamento no nível mais inferior em uma árvore de decisão de experiência. Para experiências para as quais você não configurou alvos, o nível mais baixo está em &quot;Todos&quot;.

Para experiências de anúncio padrão, é possível atribuir somente pacotes criativos padrão. Para experiências de anúncios dinâmicos, é possível atribuir somente pacotes criativos dinâmicos.

>[!NOTE]
>
>Se você não atribuir pelo menos um pacote criativo a cada nó final, poderá optar por usar os criativos padrão para cada nó não atribuído ao [salvar a experiência](experience-create-targeting.md). Para publicar uma experiência, você deve atribuir pacotes ou usar as criações padrão para cada nó final.

## Uso do editor orientado por IA (Beta) {#ai-editor}

Enquanto você está [criando](experience-create-targeting.md#ai-editor) ou [editando](experience-edit-targeting.md#ai-editor) a experiência, use os controles da tela:

1. Siga um destes procedimentos:

   * Para um nó final sem pacotes, clique em **[!UICONTROL Assign Bundles]**.

   * Para um nó com pacotes existentes, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** em seu nó de folha criativa.

1. Na guia **[!UICONTROL Assign Bundles]**, marque a caixa de seleção ao lado de cada pacote a ser atribuído e desmarque a caixa de seleção ao lado de cada pacote a ser desatribuído.

   Somente pacotes do tipo relevante para a experiência (padrão ou dinâmica) são listados.

1. (Opcional) Abra a guia **[!UICONTROL Creative optimisation]** para [personalizar rotação e agendamento](experience-optimization-scheduling-targeting.md).

1. Clique em **[!UICONTROL Save]** na caixa de diálogo para atualizar a árvore de trabalho.

1. (Opcional) [Personalizar as URLs de rastreamento](experience-tracking-urls-targeting.md#ai-editor).

1. [Salve a experiência](#save) do cabeçalho da árvore para manter suas alterações.

## Usar o editor manual {#manual-editor}

[Abra o editor manual](experience-edit-targeting.md#experience-open) antes de seguir essas etapas.

1. Siga um destes procedimentos:

   * (Nós finais sem criações) No nó, clique em **[!UICONTROL Assign Bundles]**.

   * (Nós com criações existentes) Mantenha o cursor sobre a caixa do pacote criativo abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Marque a caixa de seleção ao lado de cada pacote a ser atribuído ao nó de destino e desmarque a caixa de seleção ao lado de cada pacote a ser desatribuído.

   Somente os pacotes do tipo de pacote relevante para a experiência (padrão ou dinâmica) são listados.

1. Clique em **[!UICONTROL Save]**.

1. (Opcional) [Personalizar a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) para os pacotes atribuídos.

1. (Opcional) [Personalizar as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md).

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores. Salvar a caixa de diálogo do pacote sozinho não salva ou publica a experiência.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Adicionar um nó de destino ao nível final](experience-target-node-add-final.md)
>* [Inserir um nó de destino entre nós](experience-target-node-add-inner.md)
>* [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
>* [Exportar e implementar uma marca de experiência de anúncio para uma experiência ao vivo](experience-tag-export.md)
>* [Exibir o log de alterações para uma experiência](/help/creative/experiences/experience-view-change-log.md)
