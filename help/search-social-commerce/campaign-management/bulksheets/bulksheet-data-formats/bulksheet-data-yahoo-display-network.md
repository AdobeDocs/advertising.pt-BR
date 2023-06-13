---
title: Dados de bulksheet para [!DNL Yahoo! Display Network] contas
description: Faça referência aos campos de cabeçalho e de dados em bulksheets baixados para [!DNL Yahoo! Display Network] contas.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Apêndice - Dados de bulksheet para [!DNL Yahoo! Display Network] contas

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

É possível baixar dados para [!DNL Yahoo! Display Network] contas em massa, mas não podem carregar ou publicar bulksheets na rede de publicidade.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Campos de dados disponíveis

| Campo | Campaign | Grupo de publicidade | Anúncio | Descrição |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/d | n/d | n/d | (Incluído nos bulksheets gerados para fins de informação) A plataforma de anúncios. |
| [!UICONTROL Acct  Name] | Se incluído | Se incluído | Se incluído | O nome exclusivo que identifica uma conta de rede de anúncios. |
| [!UICONTROL Campaign Name] | Se incluído | Se incluído | Se incluído | O nome exclusivo que identifica uma campanha para uma conta. |
| [!UICONTROL Ad Group Name] | n/d | Se incluído | Se incluído | O nome exclusivo que identifica um grupo de anúncios. |
| [!UICONTROL Ad Name] | n/d | n/d | Se incluído | O nome exclusivo que identifica o anúncio em um grupo de anúncios. O comprimento máximo é de 50 caracteres. |
| [!UICONTROL Ad Title] | n/d | n/d | Se incluído | O título de um anúncio. |
| [!UICONTROL Description Line 1] | n/d | n/d | Se incluído | A primeira linha do corpo de um anúncio. |
| [!UICONTROL Description Line 2] | n/d | n/d | Se incluído | A segunda linha do corpo de um anúncio. |
| [!UICONTROL Base URL/Final URL] | n/d | n/d | Se incluído | O URL da página de aterrissagem para o qual os usuários finais são levados quando clicam em seu anúncio, incluindo quaisquer parâmetros de acréscimo configurados para a campanha ou conta. URLs base/final no nível de palavra-chave substituem URLs no nível de anúncio e superior. |
| [!UICONTROL Destination URL] | n/d | n/d | n/d | (Incluído em bulksheets gerados para fins de informação; não publicado na rede de publicidade) Para contas com URLs de destino, esse valor é o URL que vincula um anúncio a um URL/página inicial base no site do anunciante (às vezes, por meio de outro site que rastreia o clique e redireciona o usuário para a página inicial). Inclui quaisquer parâmetros de acréscimo configurados para a campanha ou conta do Search, Social e &amp; Commerce. Se você gerou URLs de rastreamento, esse valor se baseia nos parâmetros de rastreamento nas configurações da conta e nas configurações da campanha. Se você anexou parâmetros específicos de rede de publicidade, eles podem ser substituídos pelos parâmetros equivalentes de Pesquisa, Social e Comércio. |
| \[Classificação de rótulo específica do anunciante\] | Se incluído | Se incluído | Se incluído | (Nomeado para uma classificação de rótulo específica do anunciante, como &quot;Cor&quot; para uma classificação de rótulo chamada Cor) Um valor para a classificação especificada associada à entidade. |
| [!UICONTROL Constraints] | Se incluído | Se incluído | n/d | Uma restrição atribuída à entidade. |
| [!UICONTROL Campaign Status] | Se incluído | n/d | n/d | O status de exibição da campanha: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/d | Se incluído | n/d | O status de exibição do grupo de anúncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/d | n/d | Se incluído | O status de exibição da palavra-chave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i> (somente palavras-chave existentes). |
| [!UICONTROL Campaign ID] | Se incluído | Se incluído | Se incluído | A ID exclusiva que identifica uma campanha existente. |
| [!UICONTROL Ad Group ID] | n/d | Se incluído | Se incluído | O identificador exclusivo que identifica um grupo de anúncios existente. |
| [!UICONTROL Keyword ID] | n/d | n/d | Se incluído | A ID exclusiva que identifica uma palavra-chave existente. |
| [!UICONTROL AMO ID] | n/d | n/d | n/d | (Em bulksheets gerados) Um identificador exclusivo gerado por Adobe para uma entidade sincronizada. |
| [!UICONTROL EF Error Message] | n/d | n/d | n/d | (Incluído em bulksheets gerados para fins de informação) Espaço reservado para exibir mensagens de erro do Search, Social e &amp; Commerce referentes aos dados na linha; as mensagens de erro estão incluídas em [!UICONTROL EF Errors] arquivos. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Baixar/criar um arquivo de bulksheet](../bulksheet-download.md)
