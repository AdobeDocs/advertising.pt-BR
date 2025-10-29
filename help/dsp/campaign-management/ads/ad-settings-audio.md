---
title: Configurações do anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios em áudio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Configurações do anúncio de áudio

## [!UICONTROL Insert Ad Tag]

*Somente novos anúncios*

**[!UICONTROL URL]**: A URL da marca VAST.

**[!UICONTROL Title]**: Um nome para o arquivo, que é usado na exibição e nos relatórios [!UICONTROL Ads].

>[!TIP]
>
> Para verificar a validade de uma tag VAST, cole-a em um navegador e pressione a tecla **[!UICONTROL Enter]**. Se a marca for válida, você verá um arquivo XML que inclui `<VAST>` perto da parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Somente leitura) O tipo de anúncio que você está criando, que corresponde ao tipo de posicionamento ao qual o anúncio pode ser anexado. O padrão é *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** O nome do anúncio. O título do ativo é usado por padrão, mas você pode alterar o nome.

>[!TIP]
>
> Use um nome fácil de encontrar ao anexar o anúncio a um posicionamento, no modo de exibição [!UICONTROL Ads] e em relatórios. Por exemplo, descreva o tipo de unidade e alguns atributos principais (como Visualização de produto de feriado: áudio de 30 segundos).

**[!UICONTROL Ad Duration]:** O comprimento do arquivo de áudio. É automaticamente definido como [!UICONTROL 15] ou [!UICONTROL 30], dependendo da unidade de anúncio selecionada.

Este campo pode ou não ser exibido, dependendo das permissões da conta.

**[!UICONTROL VAST Tag]:** (Anúncios usando somente marcas VAST) Uma URL para uma fonte de anúncio de terceiros. Verifique se a tag VAST inclui apenas arquivos de mídia de áudio.

**[!UICONTROL Final VAST Tag]:** (Anúncios usando somente marcas VAST) A URL da fonte de anúncio de terceiros com as [macros de rastreamento do Advertising DSP](/help/dsp/campaign-management/macros.md) necessárias inseridas, se aplicável.

**[!UICONTROL Select Rate]:** (Usuários com permissão apenas) Uma taxa pré-negociada cobrada pela Adobe, ou uma das taxas que você negociou e é cobrada pelo fornecedor. Para adicionar uma taxa, entre em contato com a equipe de conta da Adobe.

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
