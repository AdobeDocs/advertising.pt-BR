---
title: Configurações do anúncio de exibição
description: Consulte descrições das configurações de anúncios disponíveis para exibir anúncios.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
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

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os Posicionamentos Associados a um Anúncio](ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
