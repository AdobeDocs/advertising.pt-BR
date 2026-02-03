---
title: Gerenciar modelos de anúncios dinâmicos
description: Saiba como gerenciar modelos de anúncios dinâmicos e criar anúncios com base neles.
feature: Creative Templates
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Gerenciar modelos de anúncios dinâmicos

Crie um modelo de anúncio separado para cada combinação de tipo de anúncio (HTML5 estático ou HTML5 dinâmico) e tamanho de anúncio ao fazer upload de um arquivo compactado HTML5 com o formato de anúncio desejado. Para anúncios HTML5 dinâmicos, você também carrega um arquivo contendo os atributos do anúncio<!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Criar um modelo de anúncio dinâmico

>[!NOTE]
>
>Você também pode carregar um modelo de anúncio dinâmico ao [adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md). Todos os modelos de anúncios criados lá ficam disponíveis no modo de exibição [!UICONTROL Ad Templates] para uso futuro.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. No canto superior direito, clique em **[!UICONTROL Create Ad Template]**

1. Especifique as [configurações do modelo de anúncio](#ad-template-settings)

1. Clique em **[!UICONTROL Create]**.

## Editar um modelo de anúncio dinâmico

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenha o cursor sobre a linha do modelo de anúncio e clique em **[!UICONTROL Edit]**.

1. Edite as [configurações do modelo de anúncio](#ad-template-settings).

1. Clique em **[!UICONTROL Save]**.

## Baixar um modelo de anúncio dinâmico

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenha o cursor sobre a linha do modelo de anúncio e clique em **[!UICONTROL Download]**.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

## Excluir um modelo de anúncio dinâmico

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenha o cursor sobre a linha do modelo de anúncio e clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.<!-- Confirm -->

## Criar anúncios dinâmicos a partir de um modelo de anúncio

>[!NOTE]
>
>Você também pode [adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md) de dentro de uma biblioteca criativa.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Mantenha o cursor sobre a linha do modelo de anúncio e clique em **[!UICONTROL Create Dynamic Ad]**.

   Na tela [!UICONTROL New Dynamic Ad], os campos [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type] e [!UICONTROL Ad Template] são automaticamente selecionados e somente leitura.

1. Especifique as configurações de anúncio dinâmico para [criar os anúncios dinâmicos](/help/creative/creative-libraries/creative-add-dynamic.md).

## Configurações do modelo de publicidade {#ad-template-settings}

### Detalhes do modelo de publicidade

**[!UICONTROL Advertiser]**: (Somente leitura para modelos existentes) O anunciante para o qual os anúncios serão gerados.

**[!UICONTROL Ad Template Name]**: um nome de modelo de anúncio exclusivo para o anunciante.

**[!UICONTROL Ad Template Type]**: (Somente leitura para modelos existentes) O formato do modelo de anúncio: *HTML5 estático* ou *HTML5 dinâmico*.

**[!UICONTROL Ad Template Size]**: (Somente leitura para modelos existentes) as dimensões dos anúncios criados pelo modelo.

**[!UICONTROL Description]**: (Opcional) Informações que são úteis para qualquer pessoa que use o modelo de anúncio.

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### zip HTML5

Um arquivo HTML5 compactado com o formato de anúncio desejado. Se você já tiver carregado um arquivo, o nome do arquivo será listado.

Consulte a [especificação criativa do HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

Para carregar um arquivo:

1. Clique em **[!UICONTROL Upload HTML5 zip]**.

1. Localize o arquivo no dispositivo ou na rede.

### (Modelos de anúncios dinâmicos do HTML5) Arquivo de atributos

<!-- EXPLAIN -->Um arquivo que contém atributos para o modelo de anúncio. Se você já tiver carregado um arquivo, o nome do arquivo será listado.

<!-- Add specs for this file type -->

Para carregar um arquivo:

1. Clique em **[!UICONTROL Upload Attributes File]**.

1. Localize o arquivo no dispositivo ou na rede.

>[!MORELIKETHIS]
>
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gerenciar arquivos de ativos](/help/creative/feeds/asset-manage.md)
>* [Gerenciar modelos de feed](/help/creative/feeds/feed-template-manage.md)
>* [Gerenciar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md)

