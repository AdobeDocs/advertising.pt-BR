---
title: Gerenciar arquivos de ativos
description: Saiba como fazer upload e gerenciar arquivos de ativos para um anunciante.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Gerenciar arquivos de ativos

Os anúncios dinâmicos do HTML5 exigem um arquivo de feed no formato de planilha do Microsoft Excel (XLSX) e os ativos de imagem referenciados na planilha (exceto para referências de ativos do Adobe Experience Manager). Os anúncios estáticos HTML5 exigem apenas um único ativo de imagem por anúncio.


>[!NOTE]
>
> Você pode usar cada arquivo de feed somente para um catálogo.

## Requisitos de arquivo

* Anúncios dinâmicos do HTML5:

   * Um arquivo de feed no formato CSV, TSV ou planilha do Microsoft Excel (XLSX), com uma linha de cabeçalho e uma linha de dados para cada variação de anúncio. Inclua um nome de imagem em cada linha usando o formato `images/image_name` (como `images/300x250_acme_logo.png`).

     Os nomes de campo específicos do anunciante devem mapear para os [campos disponíveis para arquivos de feed de anúncios dinâmicos](/help/creative/appendix-available-feed-fields.md).

   * Os ativos de imagem associados nos formatos GIF, JPEG, JPG ou PNG.<!-- Is this true: The maximum file size is two (2) MB. --> Consulte os [tamanhos de criação suportados](/help/creative/creative-libraries/creative-sizes.md).

   * (Opcional) Ativos de vídeo no formato MP4 ou WEBM

  Você pode carregar um único arquivo XLSX, uma única imagem ou arquivo de vídeo ou um único arquivo ZIP contendo qualquer combinação de XLSX, imagem e arquivos de vídeo.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Anúncios estáticos do HTML5:

   * Um ativo de imagem por anúncio em formato GIF, JPG, JPEG ou PNG.

     Você pode carregar uma única imagem ou várias imagens em um arquivo ZIP.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Fazer upload de um arquivo de ativo

>[!NOTE]
>
>Em vez de carregar arquivos de ativos, você também pode carregar um catálogo diretamente ao [adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md). Todos os catálogos que você criar lá ficarão disponíveis no modo de exibição [!UICONTROL Catalogs] para uso futuro.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Assets]**.

1. No canto superior direito, clique em **[!UICONTROL Create]** > **[!UICONTROL Asset]**.

1. Configure o arquivo de ativo:

   1. Selecione o anunciante que pode acessar o arquivo de ativo.

   1. Especifique o arquivo de ativo de uma das seguintes maneiras:

      * Arraste e solte um arquivo em seu dispositivo ou rede na caixa.

      * Clique em **[!UICONTROL Select a file]** para localizar o arquivo no dispositivo ou na rede.

   1. Clique em **[!UICONTROL Upload]**.

Todos os arquivos ZIP são descompactados automaticamente. Ao carregar um arquivo de planilha, o arquivo é listado na subguia [!UICONTROL Feeds]. Ao carregar um arquivo de imagem, ele é listado na subguia [!UICONTROL Images].

## Baixar um arquivo de ativo

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Assets]**.

1. Mantenha o cursor sobre a linha do ativo e clique em **[!UICONTROL Download]**.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

## Excluir um arquivo de ativo

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Assets]**.

1. Mantenha o cursor sobre a linha do ativo e clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Campos disponíveis para arquivos de feed de anúncios dinâmicos](/help/creative/appendix-available-feed-fields.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gerenciar modelos de feed](/help/creative/feeds/feed-template-manage.md)
>* [Gerenciar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Gerenciar modelos de anúncios dinâmicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md)
