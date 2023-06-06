---
title: Exibir dados gerados de feeds
description: Saiba como visualizar dados gerados de feeds de dados de inventário.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Exibir dados gerados de feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Ao propagar dados do feed sem publicá-los simultaneamente na rede de anúncios, é possível visualizar os dados de uma das seguintes maneiras. É possível, opcionalmente, [publicar dados](propagated-data-post.md) de qualquer local para as redes de anúncios relevantes.

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview],&quot; em seguida, visualize o bulksheet gerado (chamado de &quot;`<feed file name>_<template name>`&quot;) no [!UICONTROL Bulksheets] exibição. Nenhum dado é incluído no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias. Essa opção permite [validar as landing pages](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associado aos anúncios e palavras-chave antes de publicar os dados.

* Se você usou a opção para &quot;[!UICONTROL Propagate only],&quot; em seguida, visualize os dados gerados em uma exibição de hierarquia de campanha do [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias.

   As exibições de hierarquia de campanha mostram apenas os dados gerados a partir do arquivo de feed, não os componentes de conta existentes. Depois que os dados de um componente e todos os seus subcomponentes são publicados na rede de anúncios, ele não é mais listado na exibição da hierarquia da campanha.

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

   1. (Opcional) Para mostrar apenas componentes de campanha criados para um modelo específico:

      1. Clique no nome do template.

      1. No [!UICONTROL Accounts] no painel de navegação esquerdo, expanda o nó da rede de publicidade e o nó da conta da rede de publicidade e marque a caixa de seleção ao lado do nome do modelo.
   1. Clique em **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** dependendo dos componentes que deseja exibir.

      >[!NOTE]
      >
      >* A menos que você exiba dados para um modelo específico, a variável [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] As guias listam todos os grupos de anúncios, palavras-chave e anúncios criados a partir de todos os modelos e arquivos de feed. Grupos de produtos usados para [!DNL Google Ads] os anúncios de compras estão listados na [!UICONTROL Keywords] guia.
      >* Para exibir apenas os subcomponentes de uma campanha específica, comece exibindo o [!UICONTROL Campaigns] guia. Da mesma forma, para exibir somente os subcomponentes de um grupo de anúncios específico, comece exibindo o [!UICONTROL Ad Groups] guia.


   1. (Opcional) Para exibir mais informações, siga um destes procedimentos:

      * Para exibir as configurações de qualquer campanha, grupo de publicidade, palavra-chave ou anúncio, clique em [Ícone Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações") ao lado do nome.

      * Para exibir os subcomponentes de uma campanha ou grupo de anúncios, faça o seguinte:

         * Para listar todos os grupos de anúncios em uma campanha, clique no nome da campanha.

         * Para listar todas as palavras-chave ou destinos de produtos em um grupo de anúncios, clique no nome do grupo de anúncios.

         * Para listar todos os anúncios em um grupo de anúncios, clique no nome do grupo de anúncios e, em seguida, clique no [!UICONTROL Ads] guia.


>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Publicar dados de campanha gerados a partir de feeds para redes de anúncios](propagated-data-post.md)
>* [Interromper um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status dos dados gerados a partir dos feeds](propagated-data-status.md)

