---
title: Criar uma experiência com direcionamento de árvore de decisão
description: Saiba como criar uma experiência de anúncio direcionada usando uma árvore de decisão.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 95e17af996cb3171667ef3cd5ac662f08112691b
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Criar uma experiência com direcionamento de árvore de decisão

*Beta fechado*

Crie uma experiência de anúncio direcionada usando uma árvore de decisão. Cada experiência usa anúncios de uma única biblioteca criativa.

>[!NOTE]
>
>* Depois de criar uma experiência direcionada, você não pode alterá-la para uma experiência não direcionada, que usa um fluxo de trabalho diferente.
>* Certifique-se de que suas experiências de anúncio incluam direcionamento compatível com as campanhas em que você o implementará. O comportamento hierárquico do direcionamento pode variar de acordo com a DSP. Ao fazer upload de uma tag de experiência de anúncio para o Advertising DSP e anexá-la a uma disposição, o direcionamento no nível do anúncio é aplicado sobre o direcionamento no nível do posicionamento (e não em vez dele). Por exemplo, se uma disposição for direcionada a usuários na Austrália e um anúncio for direcionado a usuários no Japão, o anúncio será direcionado à ramificação &quot;Todos os outros&quot;.

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

         * [Adicione um nó de destino ao nível final](experience-target-node-add-final.md).

         * [Insira um nó de destino entre os nós](experience-target-node-add-inner.md).

         * [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md).

         * [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md).

      * Pacotes do Creative:

         * [Atribuir e cancelar atribuição de criações a um nó final](experience-assign-creative-bundles.md).

           Se não atribuir pelo menos um pacote a cada nó final, você poderá optar por usar os criativos padrão para cada nó não atribuído ao salvar a experiência. Para publicar uma experiência, você deve atribuir pacotes ou usar as criações padrão para cada nó final.

         * [Personalize as URLs de rastreamento para criações nos pacotes atribuídos](experience-tracking-urls-targeting.md).

         * [Personalize a otimização criativa e o agendamento](experience-optimization-scheduling-targeting.md) para os pacotes atribuídos.

1. (Opcional) Alterne entre a árvore de decisão e as configurações gerais:

   * Para abrir as configurações gerais na árvore decisória, clique em **[!UICONTROL Experience Form]** no canto superior direito.

   * Para abrir a árvore decisória nas configurações gerais, clique em **[!UICONTROL Decision Tree]** no canto superior direito.

1. Clique em **[!UICONTROL Save]** e faça o seguinte.

   * (Se cada nó no nível mais inferior incluir pelo menos um pacote criativo) Clique em **[!UICONTROL OK]**.

   * (Se cada nó no nível mais inferior não incluir pelo menos um pacote criativo), siga um destes procedimentos:

      * Para salvar a experiência sem todos os pacotes criativos necessários, clique em **[!UICONTROL Save as Draft]**.

        Você não pode criar uma marca de anúncio para uma experiência de [rascunho](experience-about.md#experience-statuses).

      * Para atribuir o criativo padrão a cada destino que ainda não recebeu um pacote criativo, clique em **[!UICONTROL Assign Default Creatives]**. Depois de revisar a árvore atualizada com os criativos padrão atribuídos, clique em **[!UICONTROL Save]** e **[!UICONTROL OK]**.

      * Para continuar editando a árvore decisória, clique em **[!UICONTROL Continue Edit]**.

Quando a experiência é em tempo real, o [!DNL Creative] cria automaticamente uma tag de anúncio para cada tamanho de criação ou duração de vídeo aplicável. Em seguida, você pode [exportar uma marca de anúncio e implementá-la em uma DSP](/help/creative/experiences/experience-tag-export.md).

Para experiências de anúncio de vídeo, os recursos de criação de vídeo são transcodificados automaticamente pelo DSP como tags VAST 2.0 para que você possa visualizá-los. Opcionalmente, [aplique a transcodificação específica do editor](experience-tag-video-transcoding.md) a qualquer marca de experiência de anúncio de vídeo.

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
