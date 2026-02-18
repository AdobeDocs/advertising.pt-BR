---
title: Configurações de criação dinâmicas
description: Referencie as configurações de criações dinâmicas.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Configurações de criação dinâmicas

<!-- add a description -->

## Configurações de anúncios dinâmicos<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Detalhes básicos

**[!UICONTROL Creative Type]:** Se o criativo é um anúncio *[!UICONTROL Display]* (HTML5) ou um anúncio *[!UICONTROL Video]*.

**[!UICONTROL Dynamic Display Ad Name]** ou **[!UICONTROL Dynamic Video Ad Name]:** Um nome exclusivo para o criativo.

**[!UICONTROL Advertiser]:** O anunciante para o qual criar os anúncios. Se você estiver criando os anúncios de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], o anunciante já está selecionado e é somente leitura.

**[!UICONTROL Library]:** A biblioteca criativa na qual criar os anúncios. Se você estiver criando os anúncios de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], o nome da biblioteca já está selecionado como somente leitura.

**[!UICONTROL Ad Template Size]:** (somente anúncios de exibição dinâmicos) as [dimensões de anúncio](/help/creative/creative-libraries/creative-sizes.md) do modelo de anúncio a partir do qual o anúncio será criado. Se você selecionar um [!UICONTROL Ad Template] específico pela primeira vez, esse valor será selecionado automaticamente.

## Modelo de publicidade

**[!UICONTROL Ad Template]:** O modelo de anúncio a partir do qual criar os anúncios. Selecione um modelo de anúncio existente ou carregue um novo modelo de anúncio e selecione o tipo de modelo (*Estático* ou *Dinâmico*). O modelo deve estar em formato ZIP e conter:<!-- Need to add more specs for templates -->

* Exibir criativos: arquivos HTML5 com o formato de anúncio desejado e (somente anúncios dinâmicos HTML5) um arquivo com os atributos de anúncio (.tdf)

* Criação de vídeo: um arquivo .scene com o formato de anúncio desejado. O arquivo ZIP pode ter no máximo 512 MB.

Para continuar, clique em **[!UICONTROL Select Ad Template]**.

**[!UICONTROL Card Count (Max 50)]:** (Exibir somente anúncios) O número de produtos a serem exibidos em um carrossel.

**[!UICONTROL Duration]:** (Somente anúncios de vídeo; somente leitura) A duração do vídeo derivada do modelo de anúncio selecionado. A duração de cada vídeo deve ser de 1 a 90 segundos.

## Catálogos

**[!UICONTROL Template]:** O modelo de feed a ser usado para criar os anúncios.

**\[Catálogos\]**: um ou mais catálogos a partir dos quais os anúncios serão gerados. Selecione um catálogo existente ou crie um novo catálogo baixando um modelo de feed existente e criando e carregando o novo catálogo. Clique em **[!UICONTROL Select Catalog]**.

Os catálogos carregados devem estar em formato ZIP e conter o seguinte:

* (Exibição dinâmica e anúncios de vídeo) Um ou mais arquivos de feed no formato CSV, TSV ou planilha do Microsoft Excel (XLSX). O tamanho máximo do arquivo é 512 MB.<!-- Need to add more specs for the feed files -->

* (Exibir anúncios) Ativos de imagem no formato GIF, JPEG, JPG ou PNG

* (Anúncios de vídeo) Ativos de vídeo nos formatos MP4, MOV ou WEBM. Os modelos de anúncios suportados incluem o cartão de início, o cartão de fim, a sobreposição superior, a sobreposição inferior ou em forma de L. A duração de cada vídeo deve ser de 1 a 90 segundos.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Os tipos de colunas no arquivo de feed para os quais os valores devem estar presentes para criar anúncios: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Observação:** essas configurações funcionam independentemente das configurações avançadas nas configurações de experiência do anúncio.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mapeie cada atributo (campo de anúncio dinâmico) no modelo de anúncio especificado para uma coluna no catálogo especificado (rótulo do catálogo) ou insira um valor estático.

>[!MORELIKETHIS]
>
>* [Adicionar criações dinâmicas a uma biblioteca criativa](creative-add-dynamic.md)
>* [Editar criações dinâmicas em uma biblioteca criativa](creative-edit-dynamic.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
