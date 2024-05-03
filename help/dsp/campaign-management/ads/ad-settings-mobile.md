---
title: Configurações do anúncio móvel
description: Consulte descrições das configurações de anúncios disponíveis para anúncios móveis.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Configurações do anúncio móvel

## [!UICONTROL Insert Ad Tag]

*Somente novos formatos de anúncios de vídeo para dispositivos móveis*

**[!UICONTROL URL]** ou **[!UICONTROL Ad Tag]**: uma tag de anúncio VAST ou de anúncio de terceiros que contém ativos criativos e pixels de rastreamento

**[!UICONTROL Ad Title]** ou **[!UICONTROL Title]**: Um nome para o anúncio usado no [!UICONTROL Ads] e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e clique em **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anúncios De Exibição Para Dispositivos Móveis

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: Jogador 300x250&quot;).

**\[Origem do anúncio\]**: (Somente leitura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** O URL do ativo criativo de terceiros. Qualquer [carimbo de data e hora] e [[carimbo de data e hora]] parâmetros serão substituídos por valores reais.

**[!UICONTROL Final Display Code]:** O URL do ativo criativo de terceiros, com as informações necessárias [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) se for caso disso.

### [!UICONTROL Basic]: Anúncios De Vídeo

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: pré-rolagem de telefone de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** A largura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

Isso é o mesmo que o **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

Isso é o mesmo que o **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se as proporções de largura e altura do vídeo devem ser mantidas (*[!UICONTROL Yes]*) ou para alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alguns tipos de anúncio) O número de segundos para atrasar a aparência do botão Fechar.

**[!UICONTROL VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como o ativo criativo.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como o ativo criativo com o [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) se for caso disso.

**[!UICONTROL Wmode]:** (Alguns tipos de anúncios) O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual. **Dica:** Para editar os pixels de rastreamento de terceiros para vários anúncios em uma disposição de uma só vez usando o [!UICONTROL Ad Tools] exibir, consulte &quot;[Anexar pixels de rastreamento de terceiros a anúncios em um posicionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser acionado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem com 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem do pixel, no formato apropriado para a imagem especificada [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios](ad-about.md)
>* [Crie um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações de publicidade](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
