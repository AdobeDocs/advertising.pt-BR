---
title: Configurações do anúncio antes da exibição
description: Consulte descrições das configurações de anúncios disponíveis para anúncios precedentes.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Configurações do anúncio antes da exibição

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
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos-chave (como Visualização de produto de feriado: pré-rolagem de 30 segundos).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Somente anúncios precedentes padrão e que podem ser ignorados) A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Somente anúncios precedentes padrão e que podem ser ignorados) A altura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

Este campo é igual ao campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

É igual ao campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se deseja manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como fonte do anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como a origem do anúncio com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Wmode]:** (Somente antes da exibição interativa) O modo de janela: *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Somente antes da exibição interativa) O formato do player de anúncio para inventário potencial: *[!UICONTROL VPAID]* ou *[!UICONTROL VPAID & VAST]*. A visibilidade sempre é medida para VPAID, mas VPAID &amp; VAST inclui inventário que não permite a medição da visibilidade. Considere essa distinção se as métricas de visibilidade forem importantes para a campanha.

**[!UICONTROL Clock Number]**: (Somente antes da exibição interativa; usado somente no Reino Unido; disponível somente para usuários com permissão) Um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se esta configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os Posicionamentos Associados a um Anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
