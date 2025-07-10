---
title: Personalizar os URLs de rastreamento para uma experiência sem direcionamento
description: Saiba como personalizar os URLs de rastreamento para cada criativo em uma experiência sem definição de metas da árvore de decisão.
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Personalizar os URLs de rastreamento para uma experiência sem o direcionamento da árvore de decisão

*Beta fechado*

Para experiências sem direcionamento de árvore de decisão, é possível criar até cinco URLs de rastreamento de impressão personalizados, cinco URLs de rastreamento de cliques personalizados e um URL de página de aterrissagem personalizado para cada criativo individual usado para a tag de experiência de anúncio. Você pode personalizar as URLs de rastreamento no [!UICONTROL Tag Manager].

As URLs personalizadas são usadas apenas para anúncios criados a partir da tag de experiência de anúncio e não são salvas nas configurações básicas de criação no [!UICONTROL Creative Libraries].

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**.

1. (Se não houver uma tag para o tamanho do anúncio) Crie uma tag para o tamanho criativo aplicável.

   É possível criar uma ou mais tags para cada tamanho criativo usado para a experiência.

   1. No canto superior direito, clique em **[!UICONTROL Create Tag]**.

   1. Insira um **[!UICONTROL Tag name]** exclusivo e selecione o **[!UICONTROL Tag size]**.

      Os tamanhos dos elementos de criação padrão da experiência determinam os tamanhos disponíveis.

   1. Clique em **[!UICONTROL Create]**.

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Editar URLs de rastreamento](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Tracking URLs]**. <!-- For targeted experiences, this is "EDIT Tracking URLs" -->&lt;!— O Tag Manager tem apenas uma visualização de lista, mas nenhuma visualização de cartão, a partir de 2/2. >

   As guias [!UICONTROL Click Tracking URLs], [!UICONTROL Impression Tracking URLs] e [!UICONTROL Landing URLs] listam os nomes de todos os criadores nos tamanhos aplicáveis nos conjuntos atribuídos. Os tamanhos dos criativos padrão da experiência determinam os tamanhos disponíveis.<!-- There's no distinct "Creative Sizes" setting. -->

1. Nas guias **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** e **[!UICONTROL Landing URLs]**, faça o seguinte para cada criativo, conforme necessário:

   1. Expanda a linha para o criativo.

   1. Siga um destes procedimentos:

      * Para adicionar ou editar um URL personalizado, insira o URL no campo de entrada.

      * Para adicionar outra URL personalizada, clique em **[!UICONTROL +]** e insira a URL no campo de entrada.

      * Para remover uma URL personalizada, mantenha o cursor sobre a linha criativa e clique em ![Excluir](/help/creative/assets/delete.png "Excluir").

      É possível incluir até cinco URLs de rastreamento de impressão personalizados, cinco URLs de rastreamento de cliques personalizados e um URL de página de aterrissagem personalizado.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Atribuir criações a uma marca de anúncio para experiências sem direcionamento](experience-tag-assign-creatives.md)
>* [Personalizar as URLs de rastreamento para uma experiência com direcionamento de árvore de decisão](experience-tracking-urls-targeting.md)
