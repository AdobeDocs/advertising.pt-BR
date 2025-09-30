---
title: Fluxos de trabalho para anúncios dinâmicos
description: Saiba mais sobre os fluxos de trabalho para gerenciar anúncios dinâmicos.
feature: Creative Dynamic Creatives
source-git-commit: f25b0edea0f264f8ebd7c487112a7cbfca32c9e0
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Fluxos de trabalho para anúncios dinâmicos

*Usuários com permissões para criar anúncios dinâmicos*

Você pode configurar anúncios dinâmicos de duas maneiras:

* Fluxo de trabalho 1: faça upload de um modelo de anúncio e catálogo de variação de anúncios diretamente nas configurações de anúncios dinâmicos ao adicionar anúncios dinâmicos a uma biblioteca criativa. Você pode baixar um modelo de feed existente para criar o catálogo.

  Use esse fluxo de trabalho quando a mesma pessoa puder fornecer todas as informações (exceto o modelo de feed) para criar os anúncios. Os arquivos carregados permanecem disponíveis para uso futuro.

* Fluxo de trabalho 2: configure um modelo de anúncio e catálogos de variação de anúncio em exibições separadas e adicione separadamente anúncios dinâmicos a um criativo usando o modelo de anúncio e os catálogos já disponíveis.

  Use este fluxo de trabalho quando pessoas diferentes concluirão tarefas diferentes ou quando quiser concluir apenas uma tarefa por vez.

## Fluxo de trabalho 1

>[!PREREQUISITES]
>
>* Modelos de anúncios no formato HTML5
>* Catálogos de produtos no formato CSV, TSV ou planilha do Microsoft Excel (XLSX)

1. [Criar criações dinâmicas](/help/creative/creative-libraries/creative-add-dynamic.md) para uma biblioteca criativa. Para anúncios dinâmicos do HTML5, carregue um modelo de anúncio e catálogos.

1. Use os recursos de criação dinâmicos para experiências de anúncio:

   1. [Crie conjuntos de anúncios dinâmicos](/help/creative/creative-libraries/bundle-manage.md) que você possa anexar todos de uma só vez a uma experiência de anúncio.

   1. Crie experiências de anúncio dinâmicas [com direcionamento](/help/creative/experiences/experience-create-targeting.md) ou [sem direcionamento](/help/creative/experiences/experience-create-no-targeting.md) e [atribua os pacotes criativos às experiências](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Gerar e implementar marcas de experiência de anúncio](/help/creative/experiences/experience-tag-export.md) para executá-las como anúncios em sua DSP.

      Para usar uma experiência de anúncio como um anúncio no Adobe Advertising DSP, faça upload da tag de experiência de anúncio para uma campanha do Advertising DSP. Para usar uma experiência de anúncio como um anúncio em uma DSP diferente, implemente a tag de experiência de anúncio nessa DSP.

## Fluxo de trabalho 2

1. [Crie um modelo de anúncio](/help/creative/ad-templates/ad-template-manage.md) para seus anúncios dinâmicos com base nos ativos disponíveis.

1. Configure os elementos de publicidade:

   * (Para anúncios estáticos únicos do HTML5) Colete e [carregue os ativos de imagem](/help/creative/feeds/asset-manage.md) para seus anúncios.

   * (Para anúncios dinâmicos do HTML5) Crie catálogos dos elementos de anúncio:

      1. Crie um arquivo de feed no formato de planilha do Microsoft Excel (XLSX), com uma linha para cada variação de anúncio. Inclua um nome de imagem em cada linha. Colete separadamente os ativos de imagem associados.

      1. [Carregar o arquivo de feed e os ativos de imagem](/help/creative/feeds/asset-manage.md).

      1. [Crie um modelo de feed](/help/creative/feeds/feed-template-manage.md) para mapear os campos no arquivo de feed (planilha) para campos no back-end do Advertising Creative.

      1. [Crie um catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-create) de um arquivo de feed especificado e um modelo de feed especificado e [processe o catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-process) para ver as variações de anúncios que podem ser criadas a partir dele.

         Você pode usar cada arquivo de feed somente para um catálogo.

         Você pode [acompanhar o status dos trabalhos de processamento de catálogo](/help/creative/feeds/job-status-track.md) na guia [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Criar criações dinâmicas](/help/creative/creative-libraries/creative-add-dynamic.md) para uma biblioteca criativa. Para anúncios dinâmicos do HTML5, use um modelo de anúncio especificado e catálogos especificados.

1. Use os recursos de criação dinâmicos para experiências de anúncio:

   1. [Crie conjuntos de anúncios dinâmicos](/help/creative/creative-libraries/bundle-manage.md) que você possa anexar todos de uma só vez a uma experiência de anúncio.

   1. Crie experiências de anúncio dinâmicas [com direcionamento](/help/creative/experiences/experience-create-targeting.md) ou [sem direcionamento](/help/creative/experiences/experience-create-no-targeting.md) e [atribua os pacotes criativos às experiências](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Gerar e implementar marcas de experiência de anúncio](/help/creative/experiences/experience-tag-export.md) para executá-las como anúncios em sua DSP.

      Para usar uma experiência de anúncio como um anúncio no Adobe Advertising DSP, faça upload da tag de experiência de anúncio para uma campanha do Advertising DSP. Para usar uma experiência de anúncio como um anúncio em uma DSP diferente, implemente a tag de experiência de anúncio nessa DSP.
