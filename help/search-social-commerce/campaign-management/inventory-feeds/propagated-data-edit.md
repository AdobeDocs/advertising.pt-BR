---
title: Editar dados gerados a partir dos feeds
description: Saiba como editar dados gerados a partir de feeds de dados de inventário.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Editar dados gerados a partir dos feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Ao propagar dados do feed sem publicá-los simultaneamente na rede de anúncios, você pode editar os dados de uma das seguintes maneiras. Posteriormente, você poderá [postar dados](propagated-data-post.md) de qualquer local para as redes de anúncios relevantes:

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview]&quot;, poderá editar o arquivo de bulksheet gerado (chamado &quot;`<feed file name>_<template name>`&quot;) baixando-o da exibição [!UICONTROL Bulksheets], editando o arquivo e fazendo o upload novamente. Nenhum dado está incluído nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

* Se você usou a opção para &quot;[!UICONTROL Propagate only]&quot;, poderá editar os dados gerados para componentes com o [[!UICONTROL New] status](propagated-data-status.md) em uma exibição de hierarquia de campanha das guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

  As exibições de hierarquia de campanha mostram apenas os dados gerados a partir do arquivo de feed, não os componentes de conta existentes. Depois que os dados de um componente e todos os seus subcomponentes são publicados na rede de anúncios, ele não é mais listado na hierarquia da campanha.

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

   1. (Opcional) Para mostrar apenas componentes de campanha criados para um modelo específico:

      1. Clique no nome do template.

      1. No menu [!UICONTROL Accounts], no painel de navegação esquerdo, expanda o nó de rede de publicidade e o nó de conta de rede de publicidade e marque a caixa de seleção ao lado do nome do modelo.

   1. Clique na guia **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]**, dependendo dos componentes que deseja exibir.

      >[!NOTE]
      >
      >* A menos que você exiba dados para um modelo específico, as guias [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] listam todos os grupos de anúncios, palavras-chave e anúncios criados a partir de todos os modelos e arquivos de feed. Os grupos de produtos usados para [!DNL Google Ads] anúncios de compras estão listados na guia [!UICONTROL Keywords].
      >* Para exibir apenas os subcomponentes de uma campanha específica, comece pela guia [!UICONTROL Campaigns]. Da mesma forma, para exibir somente os subcomponentes de um grupo de anúncios específico, comece pela exibição da guia [!UICONTROL Ad Groups].

   1. (Opcional; para editar grupos de anúncios, palavras-chave ou anúncios apenas) Filtre a lista para incluir apenas os subcomponentes de uma campanha ou grupo de anúncios específico:

      * Para listar todos os grupos de anúncios em uma campanha, clique no nome da campanha.

      * Para listar todas as palavras-chave em um grupo de anúncios, clique no nome do grupo de anúncios.

      * Para listar tudo como em um grupo de anúncios, clique no nome do grupo de anúncios e clique na guia [!UICONTROL Ads].

   1. Clique em [Exibir/editar ícone de configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações") ao lado da campanha, do grupo de publicidade, da palavra-chave ou do nome do anúncio.

   1. Edite as configurações e clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status de dados gerados a partir de feeds](propagated-data-status.md)
