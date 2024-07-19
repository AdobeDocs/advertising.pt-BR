---
title: Anexar anúncios a inserções
description: Saiba como anexar anúncios a inserções.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Anexar anúncios a inserções

Use a exibição [!UICONTROL Ad Tools] para anexar anúncios a posicionamentos, anexar pixels de rastreamento de terceiros aos anúncios e desanexar pixels de rastreamento de terceiros existentes dos anúncios.

>[!NOTE]
>
>Anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

## Abrir a Exibição [!UICONTROL Ad Tools] {#ad-tools-open}

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. Abra a exibição [!UICONTROL Ad Tools] de qualquer uma das seguintes maneiras:

   * (No modo de exibição [!UICONTROL Packages], [!UICONTROL Placements] ou [!UICONTROL Ads]) No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Na exibição [!UICONTROL Placements]) Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Na exibição [!UICONTROL Ads]) Ao lado do nome do anúncio, clique em **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   A guia [!UICONTROL Attach Ads] é selecionada por padrão.

## Anexar anúncios a inserções {#attach-ads-campaign}

1. [Abra a exibição ](#ad-tools-open) de [!UICONTROL Ad Tools].

1. Na subexibição [!UICONTROL Edit], faça o seguinte para cada grupo de anúncios que deseja anexar aos posicionamentos:

   1. (Opcional) Localize inserções e anúncios específicos de qualquer uma das seguintes maneiras:

      * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por pacote, tipo de posicionamento, status de posicionamento, tipo de anúncio ou status de anúncio.

      * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes de posicionamento e anúncios.

   1. Na tabela à esquerda, marque a caixa de seleção ao lado de cada posicionamento ao qual os anúncios serão anexados.

   1. Na tabela à direita, marque a caixa de seleção ao lado de cada anúncio que deseja anexar aos posicionamentos selecionados.

      Somente os anúncios aplicáveis ao tipo de posicionamento e que ainda não estejam anexados aos posicionamentos selecionados podem ser selecionados.

   1. Na parte inferior direita, clique em **[!UICONTROL Attach]**.

1. (Opcional) Para retornar às exibições de detalhes da campanha, clique em ![Retornar à pasta](/help/dsp/assets/breadcrumb-return.png "Retornar à pasta") à esquerda de [!UICONTROL Ad Tools] e selecione o nome da campanha.

## Exibir anúncios anexados a inserções {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Abra a exibição ](#ad-tools-open) de [!UICONTROL Ad Tools].

1. Alterne para a opção **[!UICONTROL View]** no canto superior direito.

1. (Opcional) Localize inserções e anúncios específicos conforme necessário:

   * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por pacote, tipo de posicionamento, status de posicionamento, tipo de anúncio ou status de anúncio.

   * Nas tabelas direita e esquerda, procure sequências de texto específicas no posicionamento ou nome do anúncio.

1. Clique em qualquer linha de posicionamento na tabela à esquerda para ver os anúncios anexados na tabela à direita.

1. (Opcional) Para anexar mais anúncios aos posicionamentos da campanha, alterne para a exibição **[!UICONTROL Edit]** no canto superior direito. Consulte a Etapa 2 do procedimento anterior, &quot;[Anexar anúncios a inserções](#attach-ads-campaign)&quot; para obter instruções.

## Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento {#attach-pixels-ads}

1. [Abra a exibição ](#ad-tools-open) de [!UICONTROL Ad Tools].

1. Clique na guia **[!UICONTROL Attach Pixels]**.

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

1. [Abra a exibição ](#ad-tools-open) de [!UICONTROL Ad Tools].

1. Clique na guia **[!UICONTROL Attach Pixels]**.

1. Na subexibição [!UICONTROL Edit]:

   1. (Opcional) Localize anúncios e pixels de terceiros de qualquer uma das seguintes maneiras:

      * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por status do anúncio, tipo de anúncio, evento de integração de pixels ou tipo de pixel.

      * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes dos anúncios e nos nomes dos pixels.

   1. Na tabela à esquerda, marque a caixa de seleção ao lado de cada anúncio do qual deseja desanexar pixels de rastreamento de terceiros.

   1. Na tabela à direita, marque a caixa de seleção ao lado de cada pixel de rastreamento de terceiros que você deseja desanexar dos anúncios selecionados.

      Somente os pixels anexados a todos os anúncios selecionados são selecionáveis.

   1. Na parte inferior direita, clique em **[!UICONTROL Detach]**.

1. (Opcional) Para retornar às exibições de detalhes da campanha, clique em ![Retornar à pasta](/help/dsp/assets/breadcrumb-return.png "Retornar à pasta") à esquerda de [!UICONTROL Ad Tools] e selecione o nome da campanha.

## Visualizar pixels anexados a anúncios {#view-pixels-ads}

1. [Abra a exibição ](#ad-tools-open) de [!UICONTROL Ad Tools].

1. Clique na guia **[!UICONTROL Attach Pixels]**.

1. Alterne para a opção **[!UICONTROL View]** no canto superior direito.

1. (Opcional) Localize anúncios e pixels de terceiros conforme necessário:

   * Acima da tabela à esquerda, clique em ![Filtrar](/help/dsp/assets/filter.png) e filtre as listas por status do anúncio, tipo de anúncio, evento de integração de pixels ou tipo de pixel.

   * Acima das tabelas direita e esquerda, procure sequências de texto específicas nos nomes dos anúncios e nos nomes dos pixels.

1. Clique em qualquer linha de anúncio na tabela à esquerda para ver os pixels anexados na tabela à direita.

1. (Opcional) Para anexar mais pixels aos anúncios, alterne para a exibição **[!UICONTROL Edit]** no canto superior direito. Consulte a Etapa 3 do procedimento anterior, &quot;[Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento](#attach-pixels-ads)&quot; para obter instruções.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Editar um anúncio](ad-edit.md)
>* [Listar os Posicionamentos Associados a um Anúncio](ad-list-placements.md)
>* [Editar os Cronogramas de Anúncios para Posicionamentos](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Perguntas Frequentes sobre Vídeo Universal](/help/dsp/campaign-management/faq-universal-video.md)
