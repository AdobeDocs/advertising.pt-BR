---
title: Configurações de anúncio de vídeo universal
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de vídeo universais.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
TQID: https://experienceleague.adobe.com/el77W69kVO-3vFRPR5pT62NCm35IHlABo-sUvEcVnRI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 384
ht-degree: 0%

---

# Configurações de anúncio de vídeo universal

>[!NOTE]
>
>Anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]:** A URL da marca VAST.

**[!UICONTROL Title]:** Um título para o arquivo, que está na exibição e nos relatórios [!UICONTROL Ads].

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a marca for válida, você verá um arquivo XML que inclui `<VAST>` perto da parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: vídeo universal de 30 segundos).

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se deseja manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como fonte do anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como a origem do anúncio com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Wmode]:** O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Se esta configuração não for aplicável, deixe-a em branco.

**[!UICONTROL Video Format]:** O formato do player de anúncio para inventário potencial: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. A visibilidade sempre é medida para [!UICONTROL VPAID], mas [!UICONTROL VPAID & VAST] inclui inventário que não permite a medição de visibilidade. Considere essa distinção se as métricas de visibilidade forem importantes para a campanha.

Use o [!UICONTROL VAST], que não permite a medição da visibilidade, quando você direciona uma TV conectada ou um inventário que exige estritamente apenas o formato VAST (geralmente de fontes de fornecimento como Google Ad Manager, Appnexus, SpotX e FreeWheel). Use essa opção também para inventário anteriormente compatível com inserções/anúncios VAST (Standard Pre-roll) ou VAST (Phone + Tablet Standard Pre-roll).

**[!UICONTROL Clock Number]**: (usado somente no Reino Unido; disponível somente para usuários com permissão) um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se esta configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Perguntas frequentes sobre vídeo universal](/help/dsp/campaign-management/faq-universal-video.md)
>* [Sobre o gerenciamento de anúncios no Advertising DSP](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os posicionamentos associados a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
