---
title: Editar uma experiência com direcionamento de árvore de decisão
description: Saiba como editar as configurações de uma experiência de anúncio direcionada usando uma árvore de decisão.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: 115b769c2880936c422747b44f43b4be7281916d
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Editar uma experiência com direcionamento de árvore de decisão

*Beta fechado*

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir experiências específicas.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Edit]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Edit]**.

1. Edite as [configurações gerais de experiência](experience-settings-targeting.md).

1. (Opcional) Para editar a árvore decisória, clique em **[!UICONTROL Decision Tree]** no canto superior direito e siga qualquer um destes procedimentos:

   * ([Processando](experience-about.md#experience-statuses) experiências) Siga um destes procedimentos:

      * Para descartar as alterações não postadas existentes na experiência online, clique em **[!UICONTROL Discard and start again]**.

      * Para manter as alterações não postadas existentes, clique em **[!UICONTROL Continue editing draft]**.

      * Para editar os detalhes da experiência, clique em **[!UICONTROL Edit Experience Details]**.

   * (Opcional) Altere as configurações de exibição da árvore de decisão.

     Suas configurações são salvas até que você faça logoff.

   * Aumente ou diminua o zoom movendo o controle deslizante.

   * Alternar entre a exibição de uma lista vertical e uma lista horizontal clicando em ![Exibir como Árvore Vertical](/help/creative/assets/tree-vertical.png "Exibir como Árvore Vertical") ou ![Exibir como árvore horizontal](/help/creative/assets/tree-horizontal.png "Exibir como árvore horizontal"), respectivamente.

   * (Opcional) Altere os públicos-alvo de publicidade e as criações correspondentes de qualquer uma das seguintes maneiras:

      * Metas:

        *[Adicione um nó de destino ao nível final](experience-target-node-add-final.md) em uma experiência.

         * [Insira um nó de destino entre os nós](experience-target-node-add-inner.md).

         * [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md).

         * [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md).

      * Pacotes do Creative:

         * [Atribuir e cancelar atribuição de criações a um nó final](experience-assign-creative-bundles.md).

           Se não atribuir pelo menos um pacote a cada nó final, você poderá optar por usar os criativos padrão para cada nó não atribuído ao salvar a experiência. Para publicar uma experiência, você deve atribuir pacotes ou usar as criações padrão para cada nó final.

         * [Personalize as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md).

         * [Personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) para os pacotes atribuídos.

1. Clique em **[!UICONTROL Save]** e faça o seguinte.

   * (Se cada nó no nível mais inferior incluir pelo menos um pacote criativo) Clique em **[!UICONTROL OK]**.

   * (Se cada nó no nível mais inferior não incluir pelo menos um pacote criativo), siga um destes procedimentos:

      * Para salvar a experiência sem todos os pacotes criativos necessários, clique em **[!UICONTROL Save as Draft]**.

        Você não pode criar uma marca de anúncio para uma experiência de [rascunho](experience-about.md#experience-statuses).

      * Para atribuir o criativo padrão a cada destino que ainda não recebeu um pacote criativo, clique em **[!UICONTROL Assign Default Creatives]**. Depois de revisar a árvore atualizada com os criativos padrão atribuídos, clique em **[!UICONTROL Save]** e **[!UICONTROL OK]**.

      * Para continuar editando a árvore decisória, clique em **[!UICONTROL Continue Edit]**.

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
