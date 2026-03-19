---
title: Configurações de anúncio de TV conectado
description: Consulte descrições das configurações de anúncios disponíveis para anúncios de TV conectados.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: f58e478ea2c1397b15c667c1415a7038b6ea5e5b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Configurações de anúncio de TV conectado

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]**: A URL da marca VAST.

**[!UICONTROL Title]**: Um nome para o arquivo, que é usado no modo de exibição Anúncios e relatórios.

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a marca for válida, você verá um arquivo XML que inclui `<VAST>` perto da parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: CTV de 30 segundos).

**[!UICONTROL Width | Ad Unit Width]:** A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Height | Ad Unit Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

**[!UICONTROL Player X]:** A coordenada X da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Y]:** A coordenada Y da unidade de anúncio. Mantenha a configuração padrão.

**[!UICONTROL Player Width]:** A largura de toda a unidade de anúncio. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

É igual ao campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** A altura de toda a unidade de publicidade. Essa opção pode estar bloqueada dependendo do tipo de unidade de anúncio selecionada.

É igual ao campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Onde incluir controles de vídeo para o anúncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, ou *[!UICONTROL None]* (o padrão).

**[!UICONTROL Preserve Aspect Ratio]:** Se deseja manter as proporções de largura e altura do vídeo (*[!UICONTROL Yes]*) ou alongar o vídeo para preencher o espaço disponível (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como fonte do anúncio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente marcas VAST; somente leitura) A marca VAST de terceiros inserida como a origem do anúncio com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Clock Number]**: (usado somente no Reino Unido; disponível somente para usuários com permissão) um identificador exclusivo usado para garantir que o anúncio correto seja transmitido. Se esta configuração não for aplicável, deixe-a em branco.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de anúncios no Advertising DSP](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os posicionamentos associados a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
