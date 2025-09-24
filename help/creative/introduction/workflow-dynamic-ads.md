---
title: Fluxo de trabalho para anúncios dinâmicos
description: Saiba mais sobre o fluxo de trabalho para gerenciar anúncios dinâmicos.
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Fluxo de trabalho para anúncios dinâmicos

1. [Crie um modelo de anúncio](/help/creative/ad-templates/ad-template-manage.md) para seus anúncios dinâmicos com base nos ativos disponíveis

1. Configure os elementos de publicidade:

   * (Para anúncios estáticos únicos do HTML5) Colete e [carregue os ativos de imagem](/help/creative/feeds/asset-manage.md) para seus anúncios.

   * (Para anúncios dinâmicos do HTML5) Crie catálogos dos elementos de anúncio:

      1. Crie um arquivo de feed no formato de planilha do Microsoft Excel (XLSX), com uma linha para cada variação de anúncio. Inclua um nome de imagem ou uma referência a uma Adobe Experience Manager em cada linha. Colete separadamente os ativos de imagem associados.

      1. [Carregar o arquivo de feed e os ativos de imagem](/help/creative/feeds/asset-manage.md).

      1. [Crie um modelo de feed](/help/creative/feeds/feed-template-manage.md) para mapear os campos no arquivo de feed (planilha) para campos no back-end do Advertising Creative.

      1. [Crie um catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-create) de um arquivo de feed especificado e um modelo de feed especificado e [processe o catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-process) para ver as variações de anúncios que podem ser criadas a partir dele.

         Você pode usar cada arquivo de feed somente para um catálogo.

         Você pode [acompanhar o status dos trabalhos de processamento de catálogo](/help/creative/feeds/job-status-track.md) na guia [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Criar criações dinâmicas](/help/creative/creative-libraries/creative-add-dynamic.md) para uma biblioteca criativa. Para anúncios dinâmicos do HTML5, use um modelo de anúncio especificado e catálogos especificados.

1. [Crie conjuntos de anúncios dinâmicos](/help/creative/creative-libraries/bundle-manage.md) que você possa anexar todos de uma só vez a uma experiência de anúncio.

1. Crie experiências de anúncio dinâmicas com [com direcionamento](/help/creative/experiences/experience-create-targeting.md) ou [sem direcionamento](/help/creative/experiences/experience-create-no-targeting.md) e [atribua-as agrupadas às suas experiências de anúncio dinâmicas](/help/creative/experiences/experience-assign-creative-bundles.md).

1. [Gerar e implementar marcas de experiência de anúncio](/help/creative/experiences/experience-tag-export.md) para executá-las como anúncios em sua DSP.

   Para usar uma experiência de anúncio como um anúncio no Adobe Advertising DSP, faça upload da tag de experiência de anúncio para uma campanha do Advertising DSP. Para usar uma experiência de anúncio como um anúncio em uma DSP diferente, implemente a tag de experiência de anúncio nessa DSP.
