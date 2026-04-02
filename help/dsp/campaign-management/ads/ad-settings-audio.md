---
title: Configurações de anúncio de áudio
description: Consulte descrições das configurações de anúncios disponíveis para anúncios em áudio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
TQID: https://experienceleague.adobe.com/rP0SJspXvqzivctnNqe7b35mbL-ARZlGzC3cLAS-uwA
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
source-wordcount: 277
ht-degree: 0%

---

# Configurações de anúncio de áudio

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
>* [Sobre o gerenciamento de anúncios no Advertising DSP](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Listar os posicionamentos associados a um anúncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
