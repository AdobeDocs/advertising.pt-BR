---
title: Anexar e remover pixels dos anúncios
description: Saiba como anexar e remover pixels de rastreamento de terceiros dos anúncios.
feature: DSP Ads
exl-id: 7b386a58-5300-49cf-9de8-4ce982a5181d
source-git-commit: 3538c1d881a3032863c5a6f8c7361ac1c0bc35f9
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Anexar e remover pixels dos anúncios

Você pode anexar e desanexar pixels de rastreamento de terceiros dos anúncios.

## Abrir a visualização [!UICONTROL Ad Tools] {#ad-tools-open}

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. Abra a exibição [!UICONTROL Ad Tools] de qualquer uma das seguintes maneiras:

   * (Na exibição [!UICONTROL Campaigns]) Ao lado do nome da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (No modo de exibição [!UICONTROL Packages], [!UICONTROL Placements] ou [!UICONTROL Ads]) No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

## Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento {#attach-pixels-ads}

1. [Abra a exibição [!UICONTROL Ad Tools] de &#x200B;](#ad-tools-open).

   A guia **[!UICONTROL Attach Pixels]** é aberta.

1. Na subexibição [!UICONTROL Edit]:

   1. (Opcional) Localize anúncios e pixels de terceiros de qualquer uma das seguintes maneiras:

      * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por status do anúncio, tipo de anúncio, evento de integração de pixels ou tipo de pixel.

      * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes dos anúncios e nos nomes dos pixels.

   1. (Se não houver pixels de rastreamento de terceiros para a campanha) Crie um pixel:

      1. Na tabela à direita, clique em **[!UICONTROL Create pixel]**.

      1. Especifique as configurações:

         **[!UICONTROL Integration Event]:** O evento que dispara o pixel a ser acionado, como *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** A URL da imagem de pixel, no formato apropriado para o Tipo de Pixel especificado.

         **[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

         **[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

      1. Clique em **[!UICONTROL Save]**.

   1. Na tabela à esquerda, marque a caixa de seleção ao lado de cada anúncio para o qual deseja anexar pixels de rastreamento de terceiros.

   1. Na tabela à direita, marque a caixa de seleção ao lado de cada pixel de rastreamento de terceiros que você deseja anexar aos anúncios selecionados.

      Somente os pixels que ainda não estão anexados aos anúncios selecionados podem ser selecionados.

   1. Na parte inferior direita, clique em **[!UICONTROL Attach]**.

1. (Opcional) Para retornar às exibições de detalhes da campanha, clique em ![Retornar à pasta](/help/dsp/assets/breadcrumb-return.png "Retornar à pasta") à esquerda de [!UICONTROL Ad Tools] e selecione o nome da campanha.

## Desanexar pixels de rastreamento de terceiros de anúncios em um posicionamento {#detach-pixels-ads}

1. [Abra a exibição [!UICONTROL Ad Tools] de &#x200B;](#ad-tools-open).

   A guia **[!UICONTROL Attach Pixels]** é aberta.

1. Na subexibição [!UICONTROL Edit]:

   1. (Opcional) Localize anúncios e pixels de terceiros de qualquer uma das seguintes maneiras:

      * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por status do anúncio, tipo de anúncio, evento de integração de pixels ou tipo de pixel.

      * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes dos anúncios e nos nomes dos pixels.

   1. Na tabela à esquerda, marque a caixa de seleção ao lado de cada anúncio do qual deseja desanexar pixels de rastreamento de terceiros.

   1. Na tabela à direita, marque a caixa de seleção ao lado de cada pixel de rastreamento de terceiros que você deseja desanexar dos anúncios selecionados.

      Somente os pixels anexados a todos os anúncios selecionados são selecionáveis.

   1. Na parte inferior direita, clique em **[!UICONTROL Detach]**.

1. (Opcional) Para retornar às exibições de detalhes da campanha, clique em ![Retornar à pasta](/help/dsp/assets/breadcrumb-return.png "Retornar à pasta") à esquerda de [!UICONTROL Ad Tools] e selecione o nome da campanha.

## Exibir pixels anexados a anúncios {#view-pixels-ads}

1. [Abra a exibição [!UICONTROL Ad Tools] de &#x200B;](#ad-tools-open).

   A guia **[!UICONTROL Attach Pixels]** é aberta.

1. Alterne para a opção **[!UICONTROL View]** no canto superior direito.

1. (Opcional) Localize anúncios e pixels de terceiros conforme necessário:

   * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por status do anúncio, tipo de anúncio, evento de integração de pixels ou tipo de pixel.

   * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes dos anúncios e nos nomes dos pixels.

1. Clique em qualquer linha de anúncio na tabela à esquerda para ver os pixels anexados na tabela à direita.

1. (Opcional) Para anexar mais pixels aos anúncios, alterne para a exibição **[!UICONTROL Edit]** no canto superior direito. Consulte a Etapa 3 do procedimento anterior, &quot;[Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento](#attach-pixels-ads)&quot; para obter instruções.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Anexar anúncios a inserções](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Criar um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Editar um anúncio](ad-edit.md)
>* [Listar os Posicionamentos Associados a um Anúncio](ad-list-placements.md)
>* [Editar os Cronogramas de Anúncios para Posicionamentos](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Perguntas Frequentes sobre Vídeo Universal](/help/dsp/campaign-management/faq-universal-video.md)
