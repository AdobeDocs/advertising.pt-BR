---
title: Perguntas frequentes sobre vídeo universal
description: Saiba mais sobre anúncios de vídeo universais.
feature: DSP Placements, DSP Ads
source-git-commit: fe5340cbf495eb9498d89c18080307464d4067d9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Perguntas frequentes sobre o Universal Video

## Como criar disposições e anúncios de vídeo universais?

As disposições de vídeo universal podem conter somente anúncios de vídeo universais, e os anúncios de vídeo universais podem ser anexados apenas a disposições de vídeo universais.

Crie-os de forma semelhante à criação de outros tipos de disposições e vídeos:

1. Dentro da campanha desejada, [criar uma inserção de vídeo universal](/help/dsp/campaign-management/placements/placement-create.md), selecionando o [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Você precisará especificar pelo menos um ambiente (desktop, celular, TV conectada) para o público-alvo.

1. Na mesma campanha da disposição de vídeo universal, [criar um único anúncio de vídeo universal](/help/dsp/campaign-management/ads/ad-create.md) ou [criar vários anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Se você criar várias publicidades, especifique &quot;[!UICONTROL Universal Video]&quot; como a [!UICONTROL Ad Type]:

   * Para [!DNL Google] ou [!DNL Flashtalking] anúncios: No &quot;[!UICONTROL Review ad types]&quot; depois de fazer upload do arquivo, clique no botão **[!UICONTROL Ad Type]** e selecione **[!UICONTROL Universal Video]**.

   * Para outros tipos de tags de anúncio: No arquivo de planilha que você faz upload, especifique o campo Tipo de anúncio para cada anúncio como **[!UICONTROL Universal Video]**.

1. [Abra as configurações de anúncio](/help/dsp/campaign-management/ads/ad-edit.md) para cada novo anúncio e selecione o formato de vídeo aplicável:

   * **[!UICONTROL VPAID]:** A capacidade de visualização é sempre medida.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inclui inventário que não permite a avaliação da capacidade de visualização.
   * **[!UICONTROL VAST]** - Adequado para o inventário da TV ligada.

   Consulte &quot;[Configurações universais de anúncio de vídeo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; para obter mais informações.

1. [Anexe os novos anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) à disposição de vídeo universal.

## Por que algumas metas e pacotes de otimização estão indisponíveis quando o ambiente Connected TV é selecionado para uma disposição de vídeo universal?

Metas incompatíveis com posicionamentos de TV conectados padrão, como Menor custo por clique, não são compatíveis com o ambiente de TV conectado em posicionamentos de vídeo universais. Da mesma forma, os pacotes com metas de otimização incompatíveis também não estão disponíveis para seleção.

## Quando a função **[!UICONTROL VAST]** o formato de vídeo pode ser usado para anúncios de vídeo universais?

Use **[!UICONTROL VAST]** em qualquer um dos seguintes cenários:

* A disposição será direcionada ao inventário da TV conectada.
* O posicionamento direcionará o inventário de vídeo do Google Ad Manager, Appnexus, SpotX ou Freewheel. Esses SSPs não são compatíveis com o formato de vídeo VPAID e VAST.

## É possível anexar vários anúncios de vídeo universais à mesma disposição de vídeo universal?

Sim.
