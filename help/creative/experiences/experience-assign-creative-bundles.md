---
title: Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência
description: Saiba como atribuir elementos de criação a cada público-alvo em suas experiências de anúncio.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência

*Experiências somente com direcionamento de árvore de decisão*

Você pode atribuir pacotes criativos a um nó de direcionamento no nível mais inferior em uma árvore de decisão de experiência. Para experiências para as quais você não configurou alvos, o nível mais baixo está em &quot;Todos&quot;.

Para experiências de anúncio padrão, é possível atribuir somente pacotes criativos padrão. Para experiências de anúncios dinâmicos, é possível atribuir somente pacotes criativos dinâmicos.

>[!NOTE]
>
>Se você não atribuir pelo menos um pacote criativo a cada nó final, poderá optar por usar os criativos padrão para cada nó não atribuído ao [salvar a experiência](experience-create-targeting.md). Para publicar uma experiência, você deve atribuir pacotes ou usar as criações padrão para cada nó final.

<!-- 1. [ways to get to the decision tree] -->

1. Siga um destes procedimentos:

   * (Nós finais sem criações) No nó, clique em **[!UICONTROL Assign Bundles]**.

   * (Nós com criações existentes) Mantenha o cursor sobre a caixa do pacote criativo abaixo do nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Marque a caixa de seleção ao lado de cada pacote a ser atribuído ao nó de destino e desmarque a caixa de seleção ao lado de cada pacote a ser desatribuído.

   Somente os pacotes do tipo de pacote relevante para a experiência (padrão ou dinâmica) são listados.

1. Clique em **[!UICONTROL Save]**.

1. (Opcional) [Personalizar a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) para os pacotes atribuídos.

1. (Opcional) [Personalizar as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md).

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

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
