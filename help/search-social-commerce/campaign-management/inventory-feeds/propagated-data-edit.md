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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Ao propagar dados do feed sem publicá-los simultaneamente na rede de anúncios, você pode editar os dados de uma das seguintes maneiras. É possível, opcionalmente, [publicar dados](propagated-data-post.md) de qualquer local para as redes de anúncios relevantes:

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview]&quot;, você poderá editar o arquivo de bulksheet gerado (chamado &quot;`<feed file name>_<template name>`&quot;) baixando-o do [!UICONTROL Bulksheets] exiba, edite o arquivo e faça upload dele novamente. Nenhum dado é incluído no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias.

* Se você usou a opção para &quot;[!UICONTROL Propagate only],&quot; é possível editar os dados gerados para componentes com a [[!UICONTROL New] status](propagated-data-status.md) em uma exibição de hierarquia de campanha no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias.

  As exibições de hierarquia de campanha mostram apenas os dados gerados a partir do arquivo de feed, não os componentes de conta existentes. Depois que os dados de um componente e todos os seus subcomponentes são publicados na rede de anúncios, ele não é mais listado na hierarquia da campanha.

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

   1. (Opcional) Para mostrar apenas componentes de campanha criados para um modelo específico:

      1. Clique no nome do template.

      1. No [!UICONTROL Accounts] no painel de navegação esquerdo, expanda o nó da rede de publicidade e o nó da conta da rede de publicidade e marque a caixa de seleção ao lado do nome do modelo.

   1. Clique em **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** dependendo dos componentes que deseja exibir.

      >[!NOTE]
      >
      >* A menos que você exiba dados para um modelo específico, a variável [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] As guias listam todos os grupos de anúncios, palavras-chave e anúncios criados a partir de todos os modelos e arquivos de feed. Grupos de produtos usados para [!DNL Google Ads] os anúncios de compras estão listados na [!UICONTROL Keywords] guia.
      >* Para exibir apenas os subcomponentes de uma campanha específica, comece exibindo o [!UICONTROL Campaigns] guia. Da mesma forma, para exibir somente os subcomponentes de um grupo de anúncios específico, comece exibindo o [!UICONTROL Ad Groups] guia.

   1. (Opcional; para editar grupos de anúncios, palavras-chave ou anúncios apenas) Filtre a lista para incluir apenas os subcomponentes de uma campanha ou grupo de anúncios específico:

      * Para listar todos os grupos de anúncios em uma campanha, clique no nome da campanha.

      * Para listar todas as palavras-chave em um grupo de anúncios, clique no nome do grupo de anúncios.

      * Para listar tudo como em um grupo de anúncios, clique no nome do grupo de anúncios e, em seguida, clique no [!UICONTROL Ads] guia.

   1. Clique em [Ícone Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações") ao lado da campanha, do grupo de publicidade, da palavra-chave ou do nome do anúncio.

   1. Edite as configurações e clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Publicar dados de campanha gerados a partir de feeds para redes de anúncios](propagated-data-post.md)
>* [Interromper um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status dos dados gerados a partir dos feeds](propagated-data-status.md)
