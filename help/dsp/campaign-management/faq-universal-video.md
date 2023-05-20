---
title: Perguntas frequentes sobre o Universal Video
description: Saiba mais sobre anúncios de vídeo universais.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Perguntas frequentes sobre o Universal Video

[Anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-about.md#ad-types) O permite direcionar o inventário de vídeo de ambientes de desktop, móveis e de TV conectada para o inventário VPAID e VAST usando uma única inserção de vídeo.

## Como criar anúncios e disposições universais de vídeo?

Inserções de vídeo universais podem conter somente anúncios de vídeo universais e anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

Crie inserções e anúncios de vídeo universais de forma semelhante à criação de outros tipos de inserções e vídeos:

1. Dentro da campanha desejada, [criar uma inserção de vídeo universal](/help/dsp/campaign-management/placements/placement-create.md), selecionando o [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Você deve especificar pelo menos um ambiente (desktop, móvel, TV conectada) para o target.

1. Na mesma campanha que a inserção de vídeo universal, [criar um único anúncio de vídeo universal](/help/dsp/campaign-management/ads/ad-create.md) ou [criar vários anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Se você criar vários anúncios, certifique-se de especificar &quot;[!UICONTROL Universal Video]&quot; como o [!UICONTROL Ad Type]:

   * Para [!DNL Google] ou [!DNL Flashtalking] anúncios: na guia &quot;[!UICONTROL Review ad types]&quot; depois de fazer upload do arquivo, clique na guia **[!UICONTROL Ad Type]** e selecione **[!UICONTROL Universal Video]**.

   * Para outros tipos de tags de anúncio: no arquivo de planilha que você fizer upload, especifique o campo Ad Type para cada anúncio como **[!UICONTROL Universal Video]**.

1. [Abra as configurações do anúncio](/help/dsp/campaign-management/ads/ad-edit.md) para cada novo anúncio e selecione o formato de vídeo aplicável:

   * **[!UICONTROL VPAID]:** A visibilidade é sempre medida.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inclui inventário que não permite a medição da visibilidade.
   * **[!UICONTROL VAST]** - Adequado para inventário de TV conectada.

   Consulte &quot;[Configurações de Anúncio de Vídeo Universal](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; para obter mais informações.

1. [Anexe os novos anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) para a inserção de vídeo universal.

## Por que algumas metas e pacotes de otimização ficam indisponíveis quando o ambiente de TV conectada é selecionado para uma inserção universal de vídeo?

Metas incompatíveis com disposições padrão de TV conectada, como Menor custo por clique, não são compatíveis com o ambiente de TV conectada em disposições de vídeo universal. Da mesma forma, pacotes com metas de otimização incompatíveis também não estão disponíveis para seleção.

## Quando a variável **[!UICONTROL VAST]** formato de vídeo a ser usado para anúncios de vídeo universais?

Uso **[!UICONTROL VAST]** em qualquer um dos seguintes cenários:

* O posicionamento é direcionado ao inventário de TV conectado.
* O posicionamento é direcionado ao inventário de vídeo do Google Ad Manager, Appnexus, SpotX ou Freewheel. Esses SSPs não oferecem suporte ao formato de vídeo VPAID &amp; VAST.

## É possível anexar vários anúncios de vídeo universal à mesma disposição de vídeo universal?

Sim.
