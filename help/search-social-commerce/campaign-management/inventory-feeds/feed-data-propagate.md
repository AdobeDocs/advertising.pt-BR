---
title: Propagar dados de feed de estoque por meio de modelos
description: Saiba mais sobre como propagar dados dos feeds de inventário por meio de modelos de anúncios para gerenciar a estrutura da conta e fornecer anúncios dinâmicos.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propagar dados de feed de estoque por meio de modelos

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Depois de criar um modelo de feed específico da rede de anúncios e associar um arquivo de feed ou uma conta de centro de comerciantes [!DNL Google] ou [!DNL Microsoft] a ele, você pode criar anúncios dinamicamente propagando os dados de feed por meio do modelo de acordo com as [configurações de dados de feed](feed-settings-manage.md). Durante a propagação, os nomes das colunas no modelo são substituídos por valores de dados no feed, e as campanhas geradas e seus componentes têm as configurações padrão, a menos que o modelo especifique o contrário. Dependendo das opções do modelo, o Search, Social e Commerce cria uma nova estrutura de conta (campanhas, grupos de anúncios, palavras-chave) para os anúncios ou mapeia os anúncios para a estrutura de conta existente.

Quando os novos dados de feed contêm novos valores de dados para um item ou o modelo foi alterado, os anúncios existentes são excluídos e os novos são criados. Se a única alteração for a designação do Parâmetro [!DNL Google Ads] 1 e do Parâmetro 2, apenas esses valores serão atualizados. Anúncios duplicados (a mesma cópia de anúncio e página de aterrissagem) nunca são criados.

Ao propagar dados, você pode, opcionalmente, visualizar os dados gerados em uma exibição da hierarquia de campanha, gerar um arquivo de bulksheet para revisão ou gerar um arquivo de bulksheet para publicação imediata na rede de anúncios. Quando cada ação de propagação é concluída, um resumo de propagação é adicionado à guia Propagações, indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou deletado com base na propagação. Se você não publicar os dados imediatamente, poderá visualizá-los e publicá-los posteriormente.

## Propagar arquivos de feed da guia [!UICONTROL Templates]

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Marque a caixa de seleção ao lado dos modelos a serem propagados.

1. Na barra de ferramentas, clique em **[!UICONTROL Propagate]** e selecione uma das seguintes opções:

   * **[!UICONTROL Propagate Only]:** Para mostrar os dados propagados nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. Você ainda pode postar os dados de qualquer componente e seus subcomponentes posteriormente na guia [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Para criar um arquivo de bulksheet (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponível no modo de exibição [!UICONTROL Bulksheets] para revisão (mas não nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]). Posteriormente, você pode postar o arquivo de bulksheet da exibição [!UICONTROL Bulksheets].

     Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

   * **[!UICONTROL Propagate and Post to SE]:** Para criar um arquivo de bulksheet (chamado &quot;`<feed file name>_<template name>`&quot;) que é imediatamente enfileirado para postagem na rede de anúncios. O arquivo de bulksheet está disponível na exibição [!UICONTROL Bulksheets], mas não está disponível nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

     Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP.

   O &quot;Último Prop. A coluna &quot;Status&quot; mostra o status do job para os modelos aplicáveis.

   Quando cada ação de propagação é concluída, um resumo de propagação é adicionado à guia [!UICONTROL Propagations], indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou excluído com base na propagação. A estimativa não inclui alterações feitas no próprio editor de anúncios da rede de anúncios.

## Propagar arquivos de feed da lista [!UICONTROL Feeds]

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]**.

1. Selecione a caixa ao lado do arquivo de feed.

1. Acima da tabela de dados, clique em **[!UICONTROL Propagate/Post Feed Data]** e selecione uma das seguintes opções:

   * **[!UICONTROL Propagate Only]:** Para mostrar os dados propagados nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. Você ainda pode postar os dados de qualquer componente e seus subcomponentes posteriormente na guia [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Para criar um arquivo de bulksheet (denominado &quot;`<feed file name>_<template name>`&quot;), que está disponível no modo de exibição [!UICONTROL Bulksheets] para revisão (mas não nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]). Posteriormente, você pode postar o arquivo de bulksheet da exibição [!UICONTROL Bulksheets].

     Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

   * **[!UICONTROL Propagate and Post to SE]:** Para criar um arquivo de bulksheet (chamado &quot;`<feed file name>_<template name>`&quot;) que é imediatamente enfileirado para postagem na rede de anúncios. O arquivo de bulksheet está disponível na exibição [!UICONTROL Bulksheets], mas não está disponível nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

     Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP.

1. Na janela pop-up, marque a caixa de seleção ao lado de cada modelo pelo qual deseja propagar dados do arquivo de feed e clique em **[!UICONTROL Propagate Feed]**.

   Todos os modelos associados ao arquivo são listados.

A guia [!UICONTROL Templates] é aberta e a coluna &quot;[!UICONTROL Last Prop. Status]&quot; mostra o status do trabalho para os modelos aplicáveis.

Quando cada ação de propagação é concluída, um resumo de propagação é adicionado à guia [!UICONTROL Propagations], indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou excluído com base na propagação. A estimativa não inclui alterações feitas no próprio editor de anúncios da rede de anúncios.

## Exibir um resumo de propagação

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Clique na guia **[!UICONTROL Propagations]**.

1. Ao lado do nome do modelo, clique em ![Ícone Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações").

## Interromper um job de propagação

Você pode interromper um trabalho de propagação para dados de feed de inventário enquanto o trabalho ainda estiver na fila.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Na coluna &quot;[!UICONTROL Last Prop. Status]&quot; ao lado do nome do modelo, clique em **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Gerenciar modelos de anúncios para feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status de dados gerados a partir de feeds](propagated-data-status.md)
