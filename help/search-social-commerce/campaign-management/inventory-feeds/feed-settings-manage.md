---
title: Definir configurações de dados de feed
description: Saiba como definir as configurações que controlam como os dados de feed são processados.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Definir configurações de dados de feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Você pode configurar como lidar com grupos de anúncios, palavras-chave e anúncios em arquivos de dados de feed, e como processar os dados em arquivos FTP especificamente, por meio das configurações de feed.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Settings]**.

1. Especifique a [configurações de dados de feed](#feed-data-settings):

   1. No [!UICONTROL Obsolete Item Auto-Processing] selecione as informações nos campos.

   1. (Anunciantes que fazem upload de dados via FTP ou via link direto para uma conta do centro do comerciante) Na [!UICONTROL FTP/GMC Account Auto-Processing] selecione as informações nos campos.

   1. No [!UICONTROL Miscellaneous Auto-Processing] selecione as informações nos campos.

1. Clique em **[!UICONTROL Save]**.

## Configurações de dados do feed {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Aplica todas as [!UICONTROL Obsolete Item Auto-processing] configurações para:

* *[!UICONTROL Ad Groups Only]:* Somente grupos de anúncios obsoletos.

* *[!UICONTROL Keywords Only]:* Somente palavras-chave e grupos de produtos obsoletos.

* *[!UICONTROL Ad Variations Only]* (o padrão): somente anúncios obsoletos.

* *[!UICONTROL Keywords and Ad Variations]:* Palavras-chave/alvos de produto/grupos de produto obsoletos e anúncios obsoletos.

>[!NOTE]
>
>* Para [!DNL Google Ads] anúncios de compras, somente o grupo de produtos de nível mais baixo é afetado.
>* Para [!DNL Yandex] contas, tarefas de processamento automático de item obsoletas são sempre executadas em variações de anúncio, independentemente dessa configuração.

**[!UICONTROL When the Scheduled End Date is reached]:** (Somente dados publicados manualmente) O que fazer com os itens de linha em um arquivo de feed publicado com uma data e hora de término especificadas assim que a hora de término chegar:

* *[!UICONTROL Delete]* (o padrão): exclua todos os componentes relevantes quando chegar a hora de término especificada. Você não pode reverter esta operação.

* *[!UICONTROL Pause]:* Pausar todos os componentes relevantes quando chegar a hora de término especificada. Você pode reativar os componentes posteriormente, se necessário.

* *[!UICONTROL None]:* Não altere o status dos componentes relevantes.

**[!UICONTROL Missing line items in a manually uploaded feed]:** O que fazer com os itens existentes quando não são incluídos em um novo arquivo de feed que foi carregado manualmente ou quando não mapeiam para campanhas ou grupos de anúncios existentes de acordo com as configurações Somente mapa no modelo:

* *[!UICONTROL Delete]:* Excluir os componentes existentes.

* *[!UICONTROL Pause]:* Pausar os componentes existentes. Eles são reativados se um novo arquivo de feed contiver qualquer um dos mesmos itens de linha e mantêm suas pontuações de histórico e qualidade. **Nota:** Se todos os grupos de produtos secundários de um grupo de produtos principal estiverem ausentes, o grupo de produtos principal será excluído, pois você não pode pausar grupos de produtos.

* *[!UICONTROL None]* (o padrão): não altere os componentes existentes.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** O que fazer com os itens existentes quando 1) eles não são incluídos a) em um novo arquivo de feed que foi carregado para um diretório FTP ou b) em uma conta do centro de comércio na próxima vez que o Search, Social e Commerce for sincronizado com ele ou 2) quando eles não são mapeados para campanhas ou grupos de anúncios existentes de acordo com o [!UICONTROL Map Only] configurações no modelo.

* *[!UICONTROL Delete]:* Excluir os componentes existentes.

* *[!UICONTROL Pause]:* Pausar os componentes existentes. Eles são reativados se novos dados contiverem qualquer um dos mesmos itens de linha e mantiverem seu histórico e pontuação de qualidade. **Nota:** Se todos os grupos de produtos secundários de um grupo de produtos principal estiverem ausentes, o grupo de produtos principal será excluído, pois você não pode pausar grupos de produtos.

* *[!UICONTROL None]* (o padrão): não altere os componentes existentes.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** O que fazer com itens de linha que incluem um nível de estoque quando:

* (Para feeds com valores de estoque somente numérico na coluna especificada) O nível de estoque está em ou abaixo de uma quantidade especificada. A quantidade padrão é zero (0).

* (Para feeds com valores de texto na coluna especificada) O valor de [!UICONTROL Availability] é &quot;[!UICONTROL out of stock]&quot;; o valor não diferencia maiúsculas de minúsculas. **Nota:** **Em modelos de feed, indique as colunas de nível de estoque com base em texto usando a caixa de seleção &quot;[!UICONTROL This column has non-numeric values].&quot;

Selecione a ação para ambos os casos:

* *[!UICONTROL Delete]* (o padrão) Excluir os componentes.

* *[!UICONTROL Pause]:* Pausar os componentes. Quando os dados forem atualizados, os componentes serão reativados se os valores numéricos de estoque forem maiores que a quantidade especificada ou se a variável [!UICONTROL Availability] é &quot;[!UICONTROL in stock]&quot; ou &quot;[!UICONTROL preorder]&quot;. Os componentes mantêm seu histórico e pontuação de qualidade.

O nível de estoque para cada item de linha vem de uma coluna no arquivo de feed, conforme especificado na &quot;[!UICONTROL Stock Level]&quot; para cada modelo.

>[!TIP]
>
>* Para produtos ou serviços para os quais você espera reabastecer ou aumentar a disponibilidade, você deve pausar grupos de anúncios, palavras-chave e anúncios, em vez de excluí-los e recriá-los. Pausar permite que elas mantenham suas pontuações de qualidade.
>* Se você ativar o processamento automático obsoleto para grupos de anúncios e os novos dados incluírem um nível de estoque para o grupo de anúncios, será significativo excluir ou pausar o grupo de anúncios somente quando o nível de estoque especificado estiver no nível da categoria, em vez de no nível da marca/item. Por exemplo, se você tiver um grupo de anúncios &quot;convertíveis&quot;, o nível de estoque do grupo de anúncios deve ser o total de todos os modelos conversíveis individuais representados no grupo de anúncios.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Anunciantes fazendo upload de arquivos de dados via FTP ou uma conta do centro de comércio) Propaga automaticamente novos dados por meio dos modelos aplicáveis. A opção é selecionada por padrão. Se você desativar a opção, ainda será possível propagar dados manualmente para qualquer arquivo ou conta de feed ou para qualquer modelo.

>[!NOTE]
>
>* Para arquivos FTP, o serviço de feed verifica se há atualizações no diretório FTP a cada duas horas (horas pares no fuso horário PST). Essa opção processa todos os arquivos que foram carregados desde a última verificação.
>* Para contas do centro do comerciante, o Search, Social e Commerce sincroniza com a conta diariamente às 6:00, aproximadamente, no fuso horário do anunciante. Essa opção processa todos os dados atualizados desde a última sincronização.
>* Os dados propagados estão disponíveis no [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] até que os dados sejam publicados na rede de publicidade ou na [!UICONTROL Bulksheets] exibição.

**[!UICONTROL Post to the SE]:** (Anunciantes fazendo upload de arquivos de dados via FTP ou uma conta do centro do comerciante) Cria automaticamente arquivos de bulksheet nos formatos corretos para as redes de anúncios relevantes depois que novos dados são propagados pelos modelos aplicáveis. Essa opção também remove os dados do [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] guias, a menos que quaisquer subcomponentes tenham erros.

Essa opção está desativada por padrão. Para ativar essa opção, marque a caixa de seleção e especifique se os arquivos de bulksheet devem ser publicados nas redes de anúncios:

* *[!UICONTROL Immediately]* (o padrão): Publica os arquivos de planilha em massa nas redes de anúncios relevantes depois que os dados são propagados pelos modelos. Os arquivos de bulksheet permanecem disponíveis no [!UICONTROL Bulksheets] exibir por 30 dias.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Não publica os arquivos de bulksheet nas redes de anúncios relevantes, mas os lista em [!UICONTROL Bulksheets] , na qual você pode publicá-los posteriormente. Os arquivos de bulksheet permanecem disponíveis no [!UICONTROL Bulksheets] exibir por 30 dias. Quando o arquivo de bulksheet tem mais de 10 MB, mas tem menos de 2 GB, ele está no formato ZIP; não é necessário descompactar o arquivo para publicá-lo. **Dica:** Se você não tiver validado as landing pages anteriormente, use essa opção para validá-las no [!UICONTROL Bulksheets] antes de publicar os dados na rede de publicidade.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Impede a publicação de frases-chave com mais do que um número especificado de palavras na rede de publicidade. Quando essa opção é selecionada, frases de palavras-chave com mais do que o número máximo de palavras são propagadas e listadas no [!UICONTROL Keywords] mas não são publicados quando você tenta publicar os dados.

Essa opção está desativada por padrão para que todas as palavras-chave sejam postadas, independentemente de quantas palavras a frase inclua. Se você selecionar essa opção, selecione o número máximo de palavras a serem postadas (de 3 a 10).

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagar dados do feed por meio de modelos](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Publicar dados de campanha gerados a partir de feeds para redes de anúncios](propagated-data-post.md)
