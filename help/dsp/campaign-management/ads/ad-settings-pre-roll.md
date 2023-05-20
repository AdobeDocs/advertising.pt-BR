---
title: Configurações do anúncio antes da exibição
description: Consulte descrições das configurações de anúncios disponíveis para anúncios precedentes.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Configurações do anúncio antes da exibição

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]:** O URL da tag VAST.

**[!UICONTROL Title]:** Um título para o arquivo, que está no campo [!UICONTROL Ads] e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e clique em **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a uma disposição, no campo [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: pré-rolagem de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Somente anúncios precedentes padrão e que podem ser ignorados) A largura da unidade de anúncio inteira. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Somente anúncios precedentes padrão e que podem ser ignorados) A altura de toda a unidade de anúncios. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y para a unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

Este campo é igual ao campo **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

Isso é o mesmo que o **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se as proporções de largura e altura do vídeo devem ser mantidas (*[!UICONTROL Yes]*) ou para alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios usando somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte do anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST; somente leitura) A tag VAST de terceiros inserida como fonte do anúncio com as tags necessárias [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) se for caso disso.

**[!UICONTROL Wmode]:** (Somente antes da exibição interativa) O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Somente antes da exibição interativa) O formato do player de anúncio para inventário potencial: *[!UICONTROL VPAID]* ou *[!UICONTROL VPAID & VAST]*. A visibilidade sempre é medida para VPAID, mas VPAID &amp; VAST inclui inventário que não permite a medição da visibilidade. Considere essa distinção se as métricas de visibilidade forem importantes para a campanha.

**[!UICONTROL Clock Number]**: (Somente antes da exibição interativa; usado somente no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se esta configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Pixel]

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser acionado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem com 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem do pixel, no formato apropriado para a imagem especificada [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios](ad-about.md)
>* [Crie um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações de publicidade](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)

