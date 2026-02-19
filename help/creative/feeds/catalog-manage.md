---
title: Gerenciar catálogos de feed
description: Saiba como gerenciar catálogos de feed.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Gerenciar catálogos de feed

Os catálogos de feed processados são conjuntos de variações de anúncios potenciais criados a partir de um arquivo de feed especificado e um template de feed especificado. O Dynamic HTML5 e os anúncios de vídeo, mas não os anúncios estáticos do HTML5, exigem um catálogo para criar anúncios dinâmicos.

Antes de criar variações de anúncios e [adicionar anúncios dinâmicos a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md), processe o catálogo. Posteriormente, você pode atualizar o arquivo de feed e reprocessar o catálogo para criar um novo conjunto de variações de anúncios.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Cada arquivo de feed pode processar até 500 linhas com ativos de vídeo.

>[!TIP]
>
>Para todas as contas com vídeos dinâmicos, a prática recomendada é [baixar o modelo de feed universal [!UICONTROL Adobe Creative Template]](feed-template-manage.md), mapear cada campo no arquivo de ativo para um campo no back-end do Advertising Creative e, em seguida, renomear e carregar o modelo de feed. Use o novo modelo de feed, juntamente com o arquivo de ativo, para criar um catálogo.

## Criar um catálogo {#feed-catalog-create}

>[!NOTE]
>
>Você também pode carregar um catálogo diretamente ao [adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md). Todos os catálogos que você criar lá ficarão disponíveis no modo de exibição [!UICONTROL Catalogs] para uso futuro.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Catalog]**.

1. No canto superior direito, clique em **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Especifique as [configurações do catálogo](#catalog-settings) conforme necessário.

1. Clique em **[!UICONTROL Next]**.

1. Revise as variações de anúncios potenciais que podem ser criadas para o catálogo.

1. Clique em **[!UICONTROL Save]**.

## Editar um catálogo

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Catalog]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Edit]**.

1. Edite as [configurações do catálogo](#catalog-settings) conforme necessário.

1. Revise as variações de anúncios potenciais que podem ser criadas para o catálogo.

1. Clique em **[!UICONTROL Save]**.

## Processar um catálogo {#feed-catalog-process}

O processamento de um catálogo disponibiliza as variações de anúncios para criar anúncios dinâmicos do HTML5.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Catalog]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Run Now]**.

## Pausar um catálogo ativo

Pausar um catálogo para torná-lo inativo.<!-- Can you Activate it again? -->

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Ativar um catálogo pausado

<!-- Verify if this is available. -->

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Activate]**.

## Arquivar um catálogo

Arquive um catálogo para excluí-lo.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Archive]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Archive]**.

## Configurações do catálogo {#catalog-settings}

**[!UICONTROL Advertiser]:** O anunciante que pode usar o catálogo.

**[!UICONTROL Asset]:** O arquivo de feed a ser usado como entrada para o catálogo.

**[!UICONTROL Catalog Name]:** Um nome de catálogo exclusivo para o anunciante especificado. Por padrão, o nome do arquivo de feed é usado, incluindo a extensão do arquivo, que é a prática recomendada para identificação.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** O modelo de feed a ser usado para mapear campos no arquivo de ativo/feed especificado para campos no back-end do Advertising Creative.

>[!MORELIKETHIS]
>
>* [Rastrear o status dos trabalhos de processamento do catálogo](/help/creative/feeds/job-status-track.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gerenciar arquivos de ativos](/help/creative/feeds/asset-manage.md)
>* [Gerenciar modelos de feed](/help/creative/feeds/feed-template-manage.md)
>* [Gerenciar modelos de anúncios dinâmicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md)
