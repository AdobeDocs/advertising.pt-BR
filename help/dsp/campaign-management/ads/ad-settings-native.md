---
title: Configurações do anúncio de exibição nativo
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de exibição nativos.
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 152ba89baa17264a74a1a2498e0140972a0470eb
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Configurações do anúncio de exibição nativo

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O tipo de anúncio é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: 15 segundos nativo).

**[!UICONTROL Native Creative]:** Uma imagem de 1200x627 para maximizar a entrega no inventário móvel. Clique em **[!UICONTROL Browse]**, localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Um título atraente para engajar os visualizadores.

**[!UICONTROL Description]:** O corpo do anúncio. O comprimento máximo é de 100 caracteres.

**[!UICONTROL Landing Page]:** A URL na qual o visualizador chega ao clicar no anúncio.

**[!UICONTROL Final Landing Page]:** A URL [!UICONTROL Landing Page] com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Sponsored By (Advertiser Name)]:** O anunciante do anúncio.

**[!UICONTROL Call to Action]:** (opcional) a etapa que os visualizadores devem realizar quando visualizarem este anúncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Um logotipo de proporção 1:1 a ser incluído no anúncio para obter mais reconhecimento da marca. Clique em **[!UICONTROL Browse]**, localize o arquivo em seu dispositivo ou rede e clique em **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual. **Dica:** para editar os pixels de rastreamento de terceiros para vários anúncios em um posicionamento de uma só vez usando a exibição [!UICONTROL Ad Tools], consulte &quot;[Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem de pixel, no formato apropriado para o [!UICONTROL Pixel Type] especificado.

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os Posicionamentos Associados a um Anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
