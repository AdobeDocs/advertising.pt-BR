---
title: Gerenciar modelos de feed
description: Saiba como gerenciar modelos de feed.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Gerenciar modelos de feed

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Os modelos de feed mapeiam campos em seus arquivos/catálogos de feed com campos no back-end do Advertising Creative. Os anúncios dinâmicos do HTML5, mas não os anúncios estáticos do HTML5, exigem um modelo de feed para criar anúncios dinâmicos.

Você pode usar um modelo de feed com vários modelos de anúncio.

## Criar um modelo de feed

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. No canto superior direito, clique em **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Especifique as [configurações do modelo de feed](#feed-template-settings).

1. Clique em **[!UICONTROL Save]**.

## Editar um modelo de feed

**Observação:** só é possível editar modelos de feed criados por você.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Duplicate]**.

1. Edite as [configurações do modelo de feed](#feed-template-settings) conforme necessário.

1. Clique em **[!UICONTROL Save]**.

## Exibir um modelo de feed

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL View]**.

## Duplicação de um modelo de feed

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Duplicate]**.

1. Na tela [!UICONTROL Duplicate Template], digite um **[!UICONTROL Template Name]** exclusivo. Se você estiver duplicando um modelo criado por outra pessoa, selecione o **[!UICONTROL Advertiser]**. Opcionalmente, edite outras [configurações do modelo de feed](#feed-template-settings), conforme necessário.

1. Clique em **[!UICONTROL Save]**.

## Baixar um modelo de feed

Os modelos de feed baixados estão no formato de planilha compactada do Microsoft Excel (XLSX).

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha de modelo e clique em **[!UICONTROL Download]**.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

## Configurações do modelo de feed {#feed-template-settings}

### Configurações de [!UICONTROL General]

**[!UICONTROL Template Name]:** Um nome de modelo exclusivo para o anunciante especificado.

**[!UICONTROL Advertiser]:** O anunciante que pode usar o modelo.

**[!UICONTROL Description]:** (Opcional) Informações que são úteis para qualquer pessoa que use o modelo de feed.

### Configurações de [!UICONTROL Field Mapping]

Mapeie cada campo no arquivo de feed para um campo no back-end do Advertising Creative. Consulte &quot;[Campos disponíveis para arquivos de feed de anúncios dinâmicos](/help/creative/appendix-available-feed-fields.md)&quot; para obter uma lista dos campos de back-end e seus atributos obrigatórios.<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

Pelo menos um campo de arquivo de feed deve ser marcado como &quot;[!UICONTROL Is Unique]&quot;. Para adicionar um mapeamento de campo, clique em **[!UICONTROL +]**. Para remover o último mapeamento de campo, clique em **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** O campo no arquivo de feed.

**[!UICONTROL Description]:** (Opcional) Informações que são úteis para qualquer pessoa que use o modelo de feed.

**[!UICONTROL Is Unique]:** Indica que o campo é uma ID exclusiva (chave). Pelo menos um campo por modelo de feed deve ser exclusivo. Para selecionar esta opção, clique no botão para movê-la para a direita.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** O campo [no back-end do Advertising Creative](/help/creative/appendix-available-feed-fields.md) que mapeia para o [!UICONTROL Field Name] especificado no arquivo de feed.

>[!MORELIKETHIS]
>
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gerenciar arquivos de ativos](/help/creative/feeds/asset-manage.md)
>* [Gerenciar catálogos](/help/creative/feeds/catalog-manage.md)
>* [Rastrear o status dos trabalhos de processamento do catálogo](/help/creative/feeds/job-status-track.md)
>* [Gerenciar modelos de anúncios dinâmicos](/help/creative/ad-templates/ad-template-manage.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-dynamic.md)
