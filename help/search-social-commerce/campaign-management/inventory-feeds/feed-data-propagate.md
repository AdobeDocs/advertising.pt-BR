---
title: Propagar dados de feed de estoque por meio de modelos
description: Saiba mais sobre como propagar dados dos feeds de inventário por meio de modelos de anúncios para gerenciar a estrutura da conta e fornecer anúncios dinâmicos.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Propagar dados de feed de estoque por meio de modelos

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Depois de criar um modelo de feed específico para a rede de anúncios e associar um arquivo de feed ou um [!DNL Google] ou [!DNL Microsoft®] conta do centro de negócios com ela, você pode criar anúncios dinamicamente propagando os dados do feed por meio do modelo de acordo com a [configurações de dados de feed](feed-settings-manage.md). Durante a propagação, os nomes das colunas no modelo são substituídos por valores de dados no feed, e as campanhas geradas e seus componentes têm as configurações padrão, a menos que o modelo especifique o contrário. Dependendo das opções do modelo, o Search, Social e &amp; Commerce cria uma nova estrutura de conta (campanhas, grupos de anúncios, palavras-chave) para os anúncios ou mapeia os anúncios para a estrutura de conta existente.

Quando os novos dados de feed contêm novos valores de dados para um item ou o modelo foi alterado, os anúncios existentes são excluídos e os novos são criados. Se a única alteração for a designação de [!DNL Google Ads] Parâmetros 1 e 2, então apenas esses valores são atualizados. Anúncios duplicados (a mesma cópia de anúncio e página de aterrissagem) nunca são criados.

Ao propagar dados, você pode, opcionalmente, visualizar os dados gerados em uma exibição da hierarquia de campanha, gerar um arquivo de bulksheet para revisão ou gerar um arquivo de bulksheet para publicação imediata na rede de anúncios. Quando cada ação de propagação é concluída, um resumo de propagação é adicionado à guia Propagações, indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou deletado com base na propagação. Se você não publicar os dados imediatamente, poderá visualizá-los e publicá-los posteriormente.

## Propagar arquivos de feed do [!UICONTROL Templates] guia

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

1. Marque a caixa de seleção ao lado dos modelos a serem propagados.

1. Na barra de ferramentas, clique em **[!UICONTROL Propagate]** e selecione uma das seguintes opções:

   * **[!UICONTROL Propagate Only]:** Para mostrar os dados propagados no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias. Ainda é possível publicar os dados de qualquer componente e seus subcomponentes posteriormente na [!UICONTROL Templates] guia.

   * **[!UICONTROL Propagate and Preview]:** Para criar um arquivo de bulksheet (chamado de &quot;`<feed file name>_<template name>`&quot;), que está disponível no [!UICONTROL Bulksheets] exibir para revisão (mas não no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias). Posteriormente, você pode publicar o arquivo de bulksheet no [!UICONTROL Bulksheets] exibição.

      Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

   * **[!UICONTROL Propagate and Post to SE]:** Para criar um arquivo de bulksheet (chamado de &quot;`<feed file name>_<template name>`&quot;) que é imediatamente enfileirado para publicação na rede de publicidade. O arquivo de bulksheet está disponível no [!UICONTROL Bulksheets] exibição, mas não está disponível no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias.

      Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP.
   O &quot;Último Prop. A coluna &quot;Status&quot; mostra o status do job para os modelos aplicáveis.

   Quando cada ação de propagação é concluída, um sumário de propagação é adicionado ao [!UICONTROL Propagations] indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou excluído com base na propagação. A estimativa não inclui alterações feitas no próprio editor de anúncios da rede de anúncios.

## Propagar arquivos de feed do [!UICONTROL Feeds] lista

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]**.

1. Selecione a caixa ao lado do arquivo de feed.

1. Acima da tabela de dados, clique em **[!UICONTROL Propagate/Post Feed Data]** e selecione uma das seguintes opções:

   * **[!UICONTROL Propagate Only]:** Para mostrar os dados propagados no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias. Ainda é possível publicar os dados de qualquer componente e seus subcomponentes posteriormente na [!UICONTROL Templates] guia.

   * **[!UICONTROL Propagate and Preview]:** Para criar um arquivo de bulksheet (chamado de &quot;`<feed file name>_<template name>`&quot;), que está disponível no [!UICONTROL Bulksheets] exibir para revisão (mas não no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias). Posteriormente, você pode publicar o arquivo de bulksheet no [!UICONTROL Bulksheets] exibição.

      Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

   * **[!UICONTROL Propagate and Post to SE]:** Para criar um arquivo de bulksheet (chamado de &quot;`<feed file name>_<template name>`&quot;) que é imediatamente enfileirado para publicação na rede de publicidade. O arquivo de bulksheet está disponível no [!UICONTROL Bulksheets] exibição, mas não está disponível no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias.

      Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP.

1. Na janela pop-up, marque a caixa de seleção ao lado de cada modelo pelo qual deseja propagar dados do arquivo de feed e clique em **[!UICONTROL Propagate Feed]**.

   Todos os modelos associados ao arquivo são listados.

A variável [!UICONTROL Templates] será aberta e a caixa de diálogo &quot;[!UICONTROL Last Prop. Status]&quot;A coluna mostra o status do trabalho para os modelos aplicáveis.

Quando cada ação de propagação é concluída, um sumário de propagação é adicionado ao [!UICONTROL Propagations] indicando o número de cada tipo de entidade que foi ou seria criado, pausado ou excluído com base na propagação. A estimativa não inclui alterações feitas no próprio editor de anúncios da rede de anúncios.

## Exibir um resumo de propagação

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Clique em **[!UICONTROL Propagations]** guia.

1. Ao lado do nome do modelo, clique em ![Ícone Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Ícone Exibir/editar configurações") .

## Interromper um job de propagação

Você pode interromper um trabalho de propagação para dados de feed de inventário enquanto o trabalho ainda estiver na fila.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

1. No campo &quot;[!UICONTROL Last Prop. Status]&quot; ao lado do nome do modelo, clique em **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Gerenciar modelos de anúncio para feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Publicar dados de campanha gerados a partir de feeds para redes de anúncios](propagated-data-post.md)
>* [Interromper um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status dos dados gerados a partir dos feeds](propagated-data-status.md)

