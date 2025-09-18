---
title: Configurações do anúncio de exibição
description: Consulte descrições das configurações de anúncios disponíveis para exibir anúncios.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Configurações do anúncio de exibição

As configurações a seguir são para anúncios de exibição padrão.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: Jogador 300x250&quot;).

**\[Ad Source\]**: (Somente leitura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (somente anúncios de terceiros) Indica que o anúncio é um anúncio de banner expansível. As configurações de expansão relacionadas determinam qual inventário comprar, portanto, reflita o comportamento do anúncio.

**[!UICONTROL Expansion Method]:** (somente para anúncios de banner expansíveis de terceiros) Se o banner se expande em *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (somente anúncios de banner expansíveis de terceiros) A direção na qual o anúncio se expande: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (somente anúncios de banner expansíveis de terceiros) O fornecedor certificado para o qual o anúncio está disponível: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (somente anúncios de terceiros) A URL do ativo criativo de terceiros. Qualquer parâmetro de [carimbo de data/hora] e [[carimbo de data/hora]] é substituído por valores reais.

**[!UICONTROL Final Display Code]:** (somente anúncios de terceiros) A URL do ativo criativo de terceiros, com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Ad Size]:** A largura e a altura do anúncio. Deve ser um [tamanho de anúncio de exibição padrão com suporte](ad-specs.md). Você pode inserir manualmente o tamanho do anúncio antes de carregar o anúncio ou inserir um [!UICONTROL Display Code]. Se você não inserir o tamanho do anúncio, as dimensões do anúncio carregado ou da tag do anúncio serão inseridas automaticamente como somente leitura.

>[!IMPORTANT]
>
> O tamanho do anúncio declarado nos campos largura e altura corresponde às solicitações de oferta recebidas. Você pode enfrentar problemas na entrega se as dimensões do anúncio não corresponderem ao tamanho declarado do anúncio.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual. **Dica:** para editar os pixels de rastreamento de terceiros para vários anúncios em um posicionamento de uma só vez usando a exibição [!UICONTROL Ad Tools], consulte &quot;[Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads).&quot;

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel. Para este tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem de pixel, no formato apropriado para o [!UICONTROL Pixel Type] especificado.

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os Posicionamentos Associados a um Anúncio](ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
