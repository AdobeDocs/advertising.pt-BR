---
title: Configurações do anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios em áudio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Configurações do anúncio de áudio

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]**: o URL da tag VAST.

**[!UICONTROL Title]**: Um nome para o arquivo, que será usado na variável [!UICONTROL Ads] e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e clique em **[!UICONTROL Enter]** chave. Se a tag for válida, você verá um arquivo XML que inclui `<VAST>` perto do topo.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a uma disposição, no campo [!UICONTROL Ads] e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: áudio de 30 segundos).

**[!UICONTROL Ad Duration]:** O comprimento do arquivo de áudio. É automaticamente definido como [!UICONTROL 15] ou [!UICONTROL 30], dependendo da unidade de anúncio selecionada.

Este campo pode ou não ser exibido, dependendo das permissões da conta.

**[!UICONTROL VAST Tag]:** (Anúncios usando somente tags VAST) Um URL para uma fonte de anúncios de terceiros. Verifique se a tag VAST inclui apenas arquivos de mídia de áudio.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente tags VAST) O URL da fonte de anúncios de terceiros com as tags necessárias [Macros de rastreamento de DSP de publicidade](/help/dsp/campaign-management/macros.md) se for caso disso.

**[!UICONTROL Select Rate]:** (Somente usuários com permissão) Uma taxa pré-negociada cobrada por meio do Adobe, ou uma das taxas que você negociou e pela qual será cobrada por meio do fornecedor. Para adicionar uma taxa, entre em contato com a equipe da conta Adobe.

### Pixel

Todos os pixels de rastreamento de evento existentes para o posicionamento são anexados automaticamente. Você pode desanexar pixels existentes e criar novos pixels conforme necessário, com base nas necessidades de rastreamento do anúncio individual.

As configurações a seguir se aplicam a cada pixel criado ou editado.

**[!UICONTROL Integration Event]:** O evento que aciona o pixel para ser acionado. Para esse tipo de anúncio, use pixels que são acionados no *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem com 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** A URL da imagem pixel, no formato apropriado para o Tipo de Pixel especificado.

**[!UICONTROL Pixel Name]:** O nome do pixel. Use um nome que ajude a identificar facilmente o pixel.

**[!UICONTROL Pixel Provider]:** O provedor de pixels:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*..

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios](ad-about.md)
>* [Crie um único anúncio](ad-create.md)
>* [Listar as disposições associadas a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações de publicidade](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
