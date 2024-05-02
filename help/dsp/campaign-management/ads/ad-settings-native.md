---
title: Configurações do anúncio de exibição nativo
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de exibição nativos.
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Configurações do anúncio de exibição nativo

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O tipo de anúncio é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a uma disposição, no campo [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 15 segundos nativo).

**[!UICONTROL Native Creative]:** Uma imagem de 1200 x 627 para maximizar a entrega no inventário móvel. Clique em **[!UICONTROL Browse]** e localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Um título atraente para envolver os visualizadores.

**[!UICONTROL Description]:** O corpo do anúncio. O comprimento máximo é de 100 caracteres.

**[!UICONTROL Landing Page]:** O URL no qual o visualizador chega ao clicar no anúncio.

**[!UICONTROL Final Landing Page]:** A variável [!UICONTROL Landing Page] URL com o necessário [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) se for caso disso.

**[!UICONTROL Sponsored By (Advertiser Name)]:** O anunciante do anúncio.

**[!UICONTROL Call to Action]:** (Opcional) A etapa que os visualizadores devem realizar quando visualizarem este anúncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Um logotipo na proporção de 1:1 a ser incluído no anúncio para obter maior reconhecimento da marca. Clique em **[!UICONTROL Browse]** e localize o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser acionado. Para esse tipo de anúncio, a única opção é *[!UICONTROL Impression]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem com 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem do pixel, no formato apropriado para a imagem especificada [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios](ad-about.md)
>* [Crie um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações de publicidade](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
