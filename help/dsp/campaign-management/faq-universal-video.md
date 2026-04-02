---
title: Perguntas frequentes sobre vídeo universal
description: Saiba mais sobre anúncios de vídeo universais.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
TQID: https://experienceleague.adobe.com/LAzSivup-EVuDgtWN1T58lfRjzgrchIiFF9-lMJAVlw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 348
ht-degree: 0%

---

# Perguntas frequentes sobre vídeo universal

[Anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-about.md#ad-types) permitem direcionar o inventário de vídeo de ambientes de desktop, dispositivos móveis e TV conectada para o inventário VPAID e VAST usando um único posicionamento de vídeo.

## Como criar anúncios e disposições universais de vídeo?

Inserções de vídeo universais podem conter somente anúncios de vídeo universais e anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

Crie inserções e anúncios de vídeo universais de forma semelhante à criação de outros tipos de inserções e vídeos:

1. Na campanha desejada, [crie um posicionamento de vídeo universal](/help/dsp/campaign-management/placements/placement-create.md), selecionando o [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Você deve especificar pelo menos um ambiente (desktop, móvel, TV conectada) para o target.

1. Na mesma campanha que o posicionamento de vídeo universal, [crie um único anúncio de vídeo universal](/help/dsp/campaign-management/ads/ad-create.md) ou [crie vários anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Se você criar vários anúncios, certifique-se de especificar &quot;[!UICONTROL Universal Video]&quot; como [!UICONTROL Ad Type]:

   * Para [!DNL Google] ou [!DNL Flashtalking] anúncios: na etapa &quot;[!UICONTROL Review ad types]&quot;, depois de carregar o arquivo, clique no campo **[!UICONTROL Ad Type]** e selecione **[!UICONTROL Universal Video]**.

   * Para outros tipos de marcas de anúncio: no arquivo de planilha que você carrega, especifique o campo Tipo de anúncio para cada anúncio como **[!UICONTROL Universal Video]**.

1. [Abra as configurações de anúncio](/help/dsp/campaign-management/ads/ad-edit.md) para cada novo anúncio e selecione o formato de vídeo aplicável:

   * **[!UICONTROL VPAID]:** A visibilidade é sempre medida.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inclui inventário que não permite a medição de visibilidade.
   * **[!UICONTROL VAST]** - Adequado para inventário de TV conectada.

   Consulte &quot;[Configurações de anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; para obter mais informações.

1. [Anexe os novos anúncios de vídeo universal](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) ao posicionamento de vídeo universal.

## Por que algumas metas e pacotes de otimização ficam indisponíveis quando o ambiente de TV conectado é selecionado para uma inserção de vídeo universal?

Metas incompatíveis com disposições padrão de TV conectada, como Menor custo por clique, não são compatíveis com o ambiente de TV conectada em disposições de vídeo universal. Da mesma forma, pacotes com metas de otimização incompatíveis também não estão disponíveis para seleção.

## Quando o formato de vídeo **[!UICONTROL VAST]** deve ser usado para anúncios de vídeo universais?

Use **[!UICONTROL VAST]** em qualquer um dos cenários a seguir:

* O posicionamento é direcionado ao inventário de TV conectado.
* O posicionamento é direcionado ao inventário de vídeo do Google Ad Manager, Appnexus, SpotX ou FreeWheel. Esses SSPs não oferecem suporte ao formato de vídeo VPAID &amp; VAST.

## É possível anexar vários anúncios de vídeo universal à mesma disposição de vídeo universal?

Sim.
