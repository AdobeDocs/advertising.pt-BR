---
title: Criar uma experiência com direcionamento de árvore de decisão
description: Saiba como criar uma experiência de anúncio direcionada usando uma árvore de decisão.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Criar uma experiência com direcionamento de árvore de decisão

*Beta fechado*

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Clique em **[!UICONTROL Create New Experience]**.

1. Insira as [configurações gerais de experiência](experience-settings-targeting.md).

1. Clique em **[!UICONTROL Create]**.

1. Na árvore decisória, faça o seguinte:

   1. (Opcional) Altere as configurações de exibição da árvore de decisão.

      Suas configurações são salvas até que você faça logoff.

      * Aumente ou diminua o zoom movendo o controle deslizante.

      * Alternar entre a exibição de uma lista vertical e uma lista horizontal clicando em ![Exibir como Árvore Vertical](/help/creative/assets/tree-vertical.png "Exibir como Árvore Vertical") ou ![Exibir como árvore horizontal](/help/creative/assets/tree-horizontal.png "Exibir como árvore horizontal"), respectivamente.

   1. (Opcional) Defina as metas de publicidade e os elementos de criação correspondentes de qualquer uma das seguintes maneiras:

      * Metas:

        *[Adicione um nó de destino ao nível final](experience-target-node-add-final.md) em uma experiência.

         * [Insira um nó de destino entre os nós](experience-target-node-add-inner.md).

         * [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md).

         * [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md).

      * Pacotes de criação:

         * [Atribuir e cancelar atribuição de criações a um nó final](experience-assign-creative-bundles.md).

           Se não atribuir pelo menos um pacote a cada nó final, você poderá optar por usar os criativos padrão para cada nó não atribuído ao salvar a experiência. Para ser publicada, a experiência deve ser atribuída a pacotes ou usar os criativos padrão para todos os anúncios criados a partir dela.

         * [Personalize as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md).

         * [Personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) para os pacotes atribuídos.

1. Clique em **[!UICONTROL Save]** e faça o seguinte.

   * (Se cada nó no nível mais inferior incluir pelo menos um pacote criativo) Clique em **[!UICONTROL OK]**.

   * (Se cada nó no nível mais inferior não incluir pelo menos um pacote criativo), siga um destes procedimentos:

      * Para salvar a experiência sem todos os pacotes criativos necessários, clique em **[!UICONTROL Save as Draft]**.

        Você não pode criar uma marca de anúncio para uma experiência de [rascunho](experience-about.md#experience-statuses).

      * Para atribuir o criativo padrão a cada destino que ainda não recebeu um pacote criativo, clique em **[!UICONTROL Assign Default Creatives]**. Depois de revisar a árvore atualizada com os criativos padrão atribuídos, clique em **[!UICONTROL Save]** e **[!UICONTROL OK]**.

      * Para continuar editando a árvore decisória, clique em **[!UICONTROL Continue Edit]**.

Quando a experiência é em tempo real, o [!DNL Creative] cria automaticamente uma tag de anúncio para cada tamanho criativo aplicável.

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
