---
title: Definir configurações de dados de feed
description: Saiba como definir as configurações que controlam como os dados de feed são processados.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Definir configurações de dados de feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Você pode configurar como lidar com grupos de anúncios, palavras-chave e anúncios em arquivos de dados de feed, e como processar os dados em arquivos FTP especificamente, por meio das configurações de feed.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Settings]**.

1. Especifique as [configurações de dados de feed](#feed-data-settings):

   1. Na seção [!UICONTROL Obsolete Item Auto-Processing], selecione as informações nos campos.

   1. (Anunciantes fazendo upload de dados via FTP ou por meio de um link direto para uma conta do centro do comerciante) Na seção [!UICONTROL FTP/GMC Account Auto-Processing], selecione as informações nos campos.

   1. Na seção [!UICONTROL Miscellaneous Auto-Processing], selecione as informações nos campos.

1. Clique em **[!UICONTROL Save]**.

## Configurações de dados do feed {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Aplica todas as configurações de [!UICONTROL Obsolete Item Auto-processing] a:

* *[!UICONTROL Ad Groups Only]:* Somente grupos de anúncios obsoletos.

* *[!UICONTROL Keywords Only]:* Somente palavras-chave e grupos de produtos obsoletos.

* *[!UICONTROL Ad Variations Only]* (o padrão): somente anúncios obsoletos.

* *[!UICONTROL Keywords and Ad Variations]:* Tanto palavras-chave obsoletas/destinos de produtos/grupos de produtos quanto anúncios obsoletos.

>[!NOTE]
>
>* Para [!DNL Google Ads] anúncios de compras, somente o grupo de produtos de nível mais baixo é afetado.
>* Para contas do [!DNL Yandex], as tarefas obsoletas de processamento automático de itens são sempre executadas em variações de anúncio, independentemente dessa configuração.

**[!UICONTROL When the Scheduled End Date is reached]:** (somente dados postados manualmente) O que fazer com itens de linha em um arquivo de feed postados com uma data e hora de término especificadas quando chegar a hora de término:

* *[!UICONTROL Delete]* (o padrão): exclua todos os componentes relevantes quando chegar a hora de término especificada. Você não pode reverter esta operação.

* *[!UICONTROL Pause]:* Pausar todos os componentes relevantes quando chegar a hora de término especificada. Você pode reativar os componentes posteriormente, se necessário.

* *[!UICONTROL None]:* Não altere o status dos componentes relevantes.

**[!UICONTROL Missing line items in a manually uploaded feed]:** O que fazer com os itens existentes quando eles não são incluídos em um novo arquivo de feed que foi carregado manualmente ou quando eles não mapeiam para campanhas ou grupos de anúncios existentes de acordo com as configurações Somente Mapa no modelo:

* *[!UICONTROL Delete]:* Excluir os componentes existentes.

* *[!UICONTROL Pause]:* Pausar os componentes existentes. Eles são reativados se um novo arquivo de feed contiver qualquer um dos mesmos itens de linha e mantêm suas pontuações de histórico e qualidade. **Observação:** se todos os grupos de produtos filho de um grupo de produtos pai estiverem ausentes, o grupo de produtos pai será excluído porque você não pode pausar grupos de produtos.

* *[!UICONTROL None]* (o padrão): não altere os componentes existentes.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** O que fazer com os itens existentes quando 1) eles não são incluídos a) em um novo arquivo de feed que foi carregado para um diretório FTP ou b) em uma conta de centro de comerciantes na próxima vez que o Search, Social e Commerce for sincronizado com ele ou 2) quando eles não são mapeados para campanhas ou grupos de anúncios existentes de acordo com as configurações [!UICONTROL Map Only] no modelo.

* *[!UICONTROL Delete]:* Excluir os componentes existentes.

* *[!UICONTROL Pause]:* Pausar os componentes existentes. Eles são reativados se novos dados contiverem qualquer um dos mesmos itens de linha e mantiverem seu histórico e pontuação de qualidade. **Observação:** se todos os grupos de produtos filho de um grupo de produtos pai estiverem ausentes, o grupo de produtos pai será excluído porque você não pode pausar grupos de produtos.

* *[!UICONTROL None]* (o padrão): não altere os componentes existentes.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** O que fazer com itens de linha que incluem um nível de estoque quando:

* (Para feeds com valores de estoque somente numérico na coluna especificada) O nível de estoque está em ou abaixo de uma quantidade especificada. A quantidade padrão é zero (0).

* (Para feeds com valores de texto na coluna especificada) O valor de [!UICONTROL Availability] é &quot;[!UICONTROL out of stock]&quot;; o valor não diferencia maiúsculas de minúsculas. **Observação:** **em modelos de feed, indique colunas de nível de estoque baseadas em texto usando a caixa de seleção para &quot;[!UICONTROL This column has non-numeric values]&quot;.

Selecione a ação para ambos os casos:

* *[!UICONTROL Delete]* (padrão) Excluir os componentes.

* *[!UICONTROL Pause]:* Pausar os componentes. Quando os dados forem atualizados, os componentes serão reativados se os valores numéricos de estoque forem maiores que a quantidade especificada ou se [!UICONTROL Availability] for &quot;[!UICONTROL in stock]&quot; ou &quot;[!UICONTROL preorder]&quot;. Os componentes mantêm seu histórico e pontuação de qualidade.

O nível de estoque para cada item de linha vem de uma coluna no arquivo de feed, conforme especificado no campo &quot;[!UICONTROL Stock Level]&quot; para cada modelo.

>[!TIP]
>
>* Para produtos ou serviços para os quais você espera reabastecer ou aumentar a disponibilidade, você deve pausar grupos de anúncios, palavras-chave e anúncios, em vez de excluí-los e recriá-los. Pausar permite que elas mantenham suas pontuações de qualidade.
>* Se você ativar o processamento automático obsoleto para grupos de anúncios e os novos dados incluírem um nível de estoque para o grupo de anúncios, será significativo excluir ou pausar o grupo de anúncios somente quando o nível de estoque especificado estiver no nível da categoria, em vez de no nível da marca/item. Por exemplo, se você tiver um grupo de anúncios &quot;convertíveis&quot;, o nível de estoque do grupo de anúncios deve ser o total de todos os modelos conversíveis individuais representados no grupo de anúncios.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Anunciantes carregando arquivos de dados via FTP ou uma conta do centro de comércio) Propaga automaticamente novos dados por meio dos modelos aplicáveis. A opção é selecionada por padrão. Se você desativar a opção, ainda será possível propagar dados manualmente para qualquer arquivo ou conta de feed ou para qualquer modelo.

>[!NOTE]
>
>* Para arquivos FTP, o serviço de feed verifica se há atualizações no diretório FTP a cada duas horas (horas pares no fuso horário PST). Essa opção processa todos os arquivos que foram carregados desde a última verificação.
>* Para contas do centro do comerciante, o Search, Social e Commerce sincroniza com a conta diariamente às 6:00, aproximadamente, no fuso horário do anunciante. Essa opção processa todos os dados atualizados desde a última sincronização.
>* Os dados propagados ficam disponíveis nas guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] até que os dados sejam postados na rede de publicidade ou na exibição [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (Anunciantes carregando arquivos de dados via FTP ou uma conta do centro de comércio) Cria automaticamente arquivos de bulksheet nos formatos corretos para as redes de anúncios relevantes depois que novos dados são propagados pelos modelos aplicáveis. Essa opção também remove os dados das guias [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads], a menos que qualquer subcomponente tenha erros.

Essa opção está desativada por padrão. Para ativar essa opção, marque a caixa de seleção e especifique se os arquivos de bulksheet devem ser publicados nas redes de anúncios:

* *[!UICONTROL Immediately]* (o padrão): Publica os arquivos de planilha em massa nas redes de anúncios relevantes depois que os dados são propagados pelos modelos. Os arquivos de bulksheet permanecem disponíveis no modo de exibição [!UICONTROL Bulksheets] por 30 dias.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Não postará os arquivos de bulksheet nas redes de anúncios relevantes, mas os listará na exibição [!UICONTROL Bulksheets], a partir da qual você poderá postá-los mais tarde. Os arquivos de bulksheet permanecem disponíveis no modo de exibição [!UICONTROL Bulksheets] por 30 dias. Quando o arquivo de bulksheet tem mais de 10 MB, mas tem menos de 2 GB, ele está no formato ZIP; não é necessário descompactar o arquivo para publicá-lo. **Dica:** se você ainda não validou suas páginas de aterrissagem, use esta opção para validá-las na exibição [!UICONTROL Bulksheets] antes de postar os dados na rede de publicidade.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Impede postar frases-chave com mais de um número especificado de palavras na rede de publicidade. Quando essa opção é selecionada, frases de palavras-chave com mais do que o número máximo de palavras são propagadas e listadas na guia [!UICONTROL Keywords], mas não são postadas quando você tenta postar os dados.

Essa opção está desativada por padrão para que todas as palavras-chave sejam postadas, independentemente de quantas palavras a frase inclua. Se você selecionar essa opção, selecione o número máximo de palavras a serem postadas (de 3 a 10).

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagar dados de feed por meio de modelos](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
