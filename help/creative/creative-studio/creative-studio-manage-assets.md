---
title: Gerenciar ativos no Creative Studio
description: Saiba como fazer upload, navegar e gerenciar ativos na guia Creative Studio Assets no Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 0%

---

# Gerenciar ativos no [!UICONTROL Creative Studio]

*recurso do Beta*

Faça upload de ativos de imagens, vídeo, áudio e fontes para fazer referência nos modelos de anúncios e anexe às mensagens de bate-papo do agente de IA durante as sessões de geração de anúncios.

## A visualização [!UICONTROL Creative Studio] > [!UICONTROL Assets]

A guia **[!UICONTROL Assets]** lista seus ativos existentes em uma exibição de cartão.

### Ações disponíveis

<!--  * [Browse and search assets](#assets-search) -->

* [Fazer upload de ativos](#assets-upload)

* [Renomear um ativo](#assets-rename)

* [Baixar um ativo](#assets-download)

* [Excluir um ativo](#assets-delete)

<!--
Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.
-->

## Fazer upload de ativos {#assets-upload}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Assets]**.

1. Clique em **[!UICONTROL Upload Assets]**.

1. Selecione um ou mais arquivos do computador ou da rede.

   Os seguintes tipos de arquivos são compatíveis:

   | Tipo | Formatos compatíveis | Tamanho máximo do arquivo |
   | --- | --- | --- |
   | Imagens | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MB |
   | Vídeo | MP4, MOV, AVI, WebM | 512 MB |
   | Áudio | MP3, WAV, AAC, OGG | 50 MB |

   Arquivos vazios e tipos de arquivos não compatíveis são rejeitados com uma notificação de erro.

   O nome do ativo é salvo como o nome do arquivo carregado sem sua extensão. Espaços e caracteres não ASCII no nome do arquivo são substituídos por sublinhados (por exemplo, carregar `My Logo.png` cria um ativo chamado `My_Logo`). É possível renomear o ativo depois.

<!--
(from Bob) Moved from above step. Content in your repo failed to publish, and I'm testing several possible issues. Comment syntax between steps is sometimes problematic.

Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative.


maybe later:

   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |
   
-->

## Editar um nome de ativo {#asset-rename}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Assets]**.

1. Mantenha o cursor sobre o cartão de ativos e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Atualize o nome do ativo.

   Os nomes dos ativos podem ter até 512 caracteres.

1. Clique em **[!UICONTROL Update]**.

## Baixar um ativo {#asset-download}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Assets]**.

1. Mantenha o cursor sobre o cartão de ativos e clique em **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   O ativo é baixado de acordo com o procedimento normal do navegador.

## Excluir um ativo {#asset-delete}

>[!NOTE]
>
>Não é possível reativar um ativo excluído.

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Assets]**.

1. Mantenha o cursor sobre o cartão de ativos e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre o Creative Studio no Advertising Creative](creative-studio-about.md)
>* [Gerenciar modelos no Creative Studio](creative-studio-manage-templates.md)
>* [Gerar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)
