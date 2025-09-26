---
title: Configurações de criação dinâmicas
description: Referencie as configurações de criações dinâmicas.
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Configurações de criação dinâmicas

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Configurações de anúncios dinâmicos<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Detalhes básicos

**[!UICONTROL Dynamic Ad Name]:** Um nome exclusivo para o criativo.

**[!UICONTROL Advertiser]:** O anunciante para o qual criar os anúncios.

**[!UICONTROL Library]:** A biblioteca criativa na qual criar os anúncios. Se você estiver criando os anúncios de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], o nome da biblioteca já está selecionado como somente leitura.

**[!UICONTROL Ad Template Size]:** As [dimensões de anúncios](/help/creative/creative-libraries/creative-sizes.md) do modelo de anúncio a partir do qual o anúncio será criado. Se você selecionar um [!UICONTROL Ad Template] específico pela primeira vez, esse valor será selecionado automaticamente.

## Modelo de publicidade

**[!UICONTROL Ad Template]:** O modelo de anúncio a partir do qual criar os anúncios. Selecione um modelo de anúncio existente ou carregue um novo modelo de anúncio e selecione o tipo de modelo (*Estático* ou *Dinâmico*). Um modelo carregado deve estar em formato ZIP e conter arquivos HTML5 e o arquivo de definição de modelo (template.TDF). <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** O número de produtos a serem exibidos em um carrossel.

## Catálogos

**[!UICONTROL Template]:** O modelo de feed a ser usado para criar os anúncios.

**\[Catálogos\]**: um ou mais catálogos a partir dos quais os anúncios serão gerados. Selecione um catálogo existente ou crie um novo catálogo baixando um modelo de feed existente e criando e carregando o novo catálogo.

Os catálogos carregados devem estar em formato ZIP e conter o seguinte:

* Um ou mais arquivos de feed no formato CSV, TSV ou planilha do Microsoft Excel (XLSX).<!-- Need to add more specs for that -->

* Ativos de imagem no formato GIF, JPEG, JPG ou PNG

* (Opcional) Ativos de vídeo no formato MP4 ou WEBM

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Os tipos de colunas no arquivo de feed para os quais os valores devem estar presentes para criar anúncios: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Observação:** essas configurações funcionam independentemente das configurações avançadas nas configurações de experiência do anúncio.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mapeie cada atributo (campo de anúncio dinâmico) no modelo de anúncio especificado para uma coluna no catálogo especificado (rótulo do catálogo) ou insira um valor estático.

>[!MORELIKETHIS]
>
>* [Adicionar criações dinâmicas a uma biblioteca criativa](creative-add-dynamic.md)
>* [Editar criações dinâmicas em uma biblioteca criativa](creative-edit-dynamic.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
