---
title: Configurações de anúncios móveis
description: Consulte descrições das configurações de anúncios disponíveis para anúncios móveis.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
TQID: https://experienceleague.adobe.com/1e3HmwtXzDUQ60rGhnJ5n-feky0rYlqwt7ZQZ6YXNCQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 516
ht-degree: 0%

---

# Configurações de anúncios móveis

## [!UICONTROL Insert Ad Tag]

*Somente novos formatos de anúncios de vídeo móveis*

**[!UICONTROL URL]** ou **[!UICONTROL Ad Tag]**: uma marca de anúncio VAST ou uma marca de anúncio de terceiros que contém ativos criativos e pixels de rastreamento

**[!UICONTROL Ad Title]** ou **[!UICONTROL Title]**: Um nome para o anúncio que é usado na exibição e nos relatórios [!UICONTROL Ads].

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a marca for válida, você verá um arquivo XML que inclui `<VAST>` perto da parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Anúncios De Exibição Para Dispositivos Móveis

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: Jogador 300x250&quot;).

**\[Ad Source\]**: (Somente leitura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** A URL do ativo criativo de terceiros. Qualquer parâmetro de [carimbo de data/hora] e [[carimbo de data/hora]] é substituído por valores reais.

**[!UICONTROL Final Display Code]:** A URL do ativo criativo de terceiros, com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

### [!UICONTROL Basic]: Anúncios de vídeo

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, na exibição Anúncios e nos relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: pré-rolagem de telefone de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

É igual ao campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

É igual ao campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se deseja manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alguns tipos de anúncios) O número de segundos para atrasar a aparência do botão Fechar.

**[!UICONTROL VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como ativo criativo.

**[!UICONTROL Final VAST Tag]:** (Anúncios que usam somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como ativo criativo com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Wmode]:** (Alguns tipos de anúncios) O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios no Advertising DSP](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os posicionamentos associados a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
