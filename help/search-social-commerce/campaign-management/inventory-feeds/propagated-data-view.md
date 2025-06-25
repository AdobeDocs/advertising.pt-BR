---
title: Exibir dados gerados de feeds
description: Saiba como visualizar dados gerados de feeds de dados de inventário.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Exibir dados gerados de feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Ao propagar dados do feed sem publicá-los simultaneamente na rede de anúncios, é possível visualizar os dados de uma das seguintes maneiras. Posteriormente, você poderá [postar dados](propagated-data-post.md) de qualquer local para as redes de anúncios relevantes.

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview]&quot;, exiba a planilha gerada (chamada &quot;`<feed file name>_<template name>`&quot;) da exibição [!UICONTROL Bulksheets]. Nenhum dado está incluído nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. Essa opção permite [validar as páginas de aterrissagem](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associadas aos anúncios e palavras-chave antes de postar os dados.

* Se você usou a opção para &quot;[!UICONTROL Propagate only]&quot;, visualize os dados gerados em uma exibição de hierarquia de campanha das guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

  As exibições de hierarquia de campanha mostram apenas os dados gerados a partir do arquivo de feed, não os componentes de conta existentes. Depois que os dados de um componente e todos os seus subcomponentes são publicados na rede de anúncios, ele não é mais listado na exibição da hierarquia da campanha.

   1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

   1. (Opcional) Para mostrar apenas componentes de campanha criados para um modelo específico:

      1. Clique no nome do template.

      1. No menu [!UICONTROL Accounts], no painel de navegação esquerdo, expanda o nó de rede de publicidade e o nó de conta de rede de publicidade e marque a caixa de seleção ao lado do nome do modelo.

   1. Clique na guia **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]**, dependendo dos componentes que deseja exibir.

      >[!NOTE]
      >
      >* A menos que você exiba dados para um modelo específico, as guias [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] listam todos os grupos de anúncios, palavras-chave e anúncios criados a partir de todos os modelos e arquivos de feed. Os grupos de produtos usados para [!DNL Google Ads] anúncios de compras estão listados na guia [!UICONTROL Keywords].
      >* Para exibir apenas os subcomponentes de uma campanha específica, comece pela guia [!UICONTROL Campaigns]. Da mesma forma, para exibir somente os subcomponentes de um grupo de anúncios específico, comece pela exibição da guia [!UICONTROL Ad Groups].

   1. (Opcional) Para exibir mais informações, siga um destes procedimentos:

      * Para exibir as configurações de qualquer campanha, grupo de publicidade, palavra-chave ou anúncio, clique em [Ícone Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações") ao lado do nome.

      * Para exibir os subcomponentes de uma campanha ou grupo de anúncios, faça o seguinte:

         * Para listar todos os grupos de anúncios em uma campanha, clique no nome da campanha.

         * Para listar todas as palavras-chave ou destinos de produtos em um grupo de anúncios, clique no nome do grupo de anúncios.

         * Para listar todos os anúncios em um grupo de anúncios, clique no nome do grupo de anúncios e clique na guia [!UICONTROL Ads].

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status de dados gerados a partir de feeds](propagated-data-status.md)
