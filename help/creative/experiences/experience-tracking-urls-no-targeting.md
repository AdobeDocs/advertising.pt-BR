---
title: Personalizar os URLs de rastreamento para uma experiência sem direcionamento
description: Saiba como personalizar os URLs de rastreamento para cada criativo em uma experiência sem definição de metas da árvore de decisão.
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
TQID: https://experienceleague.adobe.com/0NvlDveOyfCjAIIXJ-lgdOQbI56tLvvutOaXrUu9fCk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# Personalizar os URLs de rastreamento para uma experiência sem o direcionamento da árvore de decisão

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

1. Mantenha o cursor sobre a linha da tag de publicidade aplicável e clique em ![Editar URLs de rastreamento](/help/creative/assets/edit-gray.png "Editar URLs de rastreamento") **[!UICONTROL Tracking URLs]**. <!-- For targeted experiences, this is "EDIT Tracking URLs"  Tag Manager has only a list view, but no card view, as of 2/2. -->

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
