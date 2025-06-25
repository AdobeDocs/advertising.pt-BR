---
title: Gerenciar arquivos de feed de dados de inventário
description: Saiba como definir as configurações que controlam como os dados de feed são processados.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Gerenciar arquivos de feed de dados de inventário

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Se você enviar seus próprios dados de feed, precisará carregar arquivos contendo os dados do produto para criar dinamicamente a estrutura da campanha, os anúncios e as palavras-chave, com base nos dados do produto. Em seguida, você pode associá-los a modelos de anúncios específicos da rede de anúncios e processar os dados por meio dos modelos, eventualmente postando os dados nas redes de anúncios relevantes. É possível associar vários modelos a um arquivo de feed, mas cada modelo pode ser associado a apenas um arquivo de feed.

>[!NOTE]
>
>Não carregue arquivos se estiver usando dados diretamente de uma conta da central de comércio.

Você pode fazer upload e processar arquivos de feed de dados de uma das seguintes maneiras:

* **Usando o FTP automaticamente:** Você pode carregar arquivos diretamente em um diretório FTP; o serviço de feed verifica novos arquivos a cada duas horas. Depois de fazer upload de um arquivo pela primeira vez, você pode associá-lo a um modelo específico de rede de anúncios. Posteriormente, todos os arquivos carregados com o mesmo nome serão associados automaticamente ao mesmo modelo. Dependendo de como você [define as configurações dos dados de feed](feed-settings-manage.md), o Search, Social e Commerce poderá propagar automaticamente os dados de feed por meio de todos os modelos aplicáveis e, opcionalmente, postar os dados de campanha e anúncios resultantes nas redes de anúncios relevantes.

  Para configurar um diretório FTP para depositar e processar automaticamente arquivos de dados, entre em contato com a equipe de conta da Adobe.

* **Processamento Manual:** Você pode [carregar arquivos de feed](#feed-file-upload) manualmente da exibição [!UICONTROL Advanced] (ACM). Depois de associar um arquivo de feed a um ou mais [modelos](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) específicos da rede de anúncios, você pode gerar dados de campanha e anúncios [propagando os dados de feed por meio dos modelos](feed-data-propagate.md) de acordo com as [configurações de dados de feed](feed-settings-manage.md). Opcionalmente, é possível pré-visualizar os dados gerados nas exibições de hierarquia de campanha, gerar um arquivo de bulksheet para revisão ou gerar um arquivo de bulksheet para publicação imediata na rede de anúncios. Se você não postar os dados imediatamente, poderá [pré-visualizá-los](propagated-data-view.md) e [postá-los](propagated-data-post.md) mais tarde. Você pode [substituir o arquivo de feed existente por um novo arquivo](#feed-file-replace) sem perder nenhuma associação de modelo existente.

## Requisitos do arquivo de feed

Nenhum campo de dados específico é necessário em um arquivo individual, mas o seguinte é necessário para cada arquivo:

* A primeira linha do arquivo deve conter nomes de coluna (também chamados de *cabeçalhos*), que correspondem aos parâmetros dinâmicos nos modelos associados. As linhas restantes devem incluir dados que correspondam aos nomes das colunas. Cada linha de dados (linha) deve pertencer a apenas um componente da conta, como uma campanha ou um anúncio. Os valores em todas as linhas devem ser separados por guias ou vírgulas. Consulte o [arquivo de exemplo CSV](#example-csv-feed-file) e o [arquivo de exemplo TSV](#example-tsv-feed-file) abaixo.

* O arquivo pode ser de qualquer tamanho, mas deve ter uma das seguintes extensões: `.tsv` (para valores separados por tabulação), `.txt` (para texto ASCII compatível com [!DNL Unicode]), `.csv` (para valores separados por vírgula) ou `.zip` (para um único arquivo no formato ZIP compactado, que é descompactado em um arquivo TSV).

* O nome do arquivo diferencia maiúsculas de minúsculas e não pode incluir os seguintes caracteres: `# % & * | \ : " < > . ? /`

* Se você depositar arquivos em um diretório FTP, deverá usar o mesmo nome de arquivo para cada versão do arquivo.

* (Somente modelos do [!DNL Google Ads]) Se o modelo usar o parâmetro de anúncio Param2 ou Param2 em anúncios de texto, os campos de dados correspondentes no arquivo de feed deverão incluir dados numéricos, sem símbolos monetários.

* Para atualizar componentes de conta existentes, inclua o nome da campanha existente (e seus componentes, se relevante). Se a estrutura existente não for especificada, novos componentes serão criados.

### Exemplo de um arquivo de feed separado por vírgulas {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Exemplo de um arquivo de feed separado por tabulação {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Práticas recomendadas

* Para dados que incluem caracteres internacionais, use arquivos no formato TSV ou TXT.

* Para obter um processo repetível com revisão ou edição manual limitada, configure arquivos de feed e seus dados de estrutura de conta da seguinte maneira:

   * Inclua colunas e linhas que contenham dados suficientes para criar uma estrutura de conta ou mapear para a estrutura de conta existente. Idealmente, use uma estrutura de conta existente que esteja intimamente ligada à taxonomia do produto e para a qual os dados do feed sejam facilmente mapeados.

   * Inclua descrições curtas o suficiente para usar em uma cópia de anúncio.

   * Use padrões de dados e convenções de nomenclatura consistentes em todas as linhas de produto.

   * Remova todos os espaços anteriores e os espaços à direita.

   * Remova todos os caracteres ilegíveis.

## Exibir ou baixar um arquivo de feed

Você pode abrir ou baixar qualquer arquivo de feed que tenha sido carregado manualmente ou por FTP.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Localize o arquivo de feed:

1. Na lista de modelos, localize um modelo que use o arquivo de feed.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]** para abrir uma lista de todos os arquivos de feed.

1. Clique no nome do arquivo de feed.

1. Abra ou salve o arquivo de acordo com o procedimento normal do navegador.

Para obter mais informações, consulte a ajuda online do navegador.

## Carregar manualmente um arquivo de feed {#feed-file-upload}

>[!NOTE]
> Se você associar um modelo a um arquivo carregado manualmente, mas fizer upload via FTP de outro arquivo com o mesmo nome, extensão de arquivo e uso de letras maiúsculas e minúsculas, o arquivo FTP será usado ao propagar os dados pelo modelo. Por exemplo, myfile.csv substitui myfile.csv, mas Myfile.CSV não substitui.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Upload]**.

1. Especifique o arquivo a ser carregado inserindo o caminho completo e o nome do arquivo ou clicando em **[!UICONTROL Browse]** para localizar o arquivo no dispositivo ou na rede.

1. Clique em **[!UICONTROL Upload].

Todos os campos no arquivo são validados. Não é possível postar itens com comprimentos de campo inválidos posteriormente até que você corrija os valores. Todos os nomes de colunas no arquivo ficam disponíveis em modelos como parâmetros dinâmicos.

## Substituir um arquivo de feed {#feed-file-replace}

Ao substituir um arquivo de feed — mesmo que o novo arquivo tenha um nome de arquivo ou extensão diferente — todas as associações de modelo existentes permanecem. O novo arquivo é usado quando você propaga dados por todos os modelos que foram originalmente associados ao arquivo anterior.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Siga um destes procedimentos:

   * Na coluna [!UICONTROL Feed] de qualquer modelo aplicável, clique em ![Mais opções](/help/search-social-commerce/assets/options.png "Mais opções") e selecione **[!UICONTROL Re-upload]**.

   * Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]**. Na lista de arquivos de feed, marque a caixa de seleção ao lado do nome do arquivo existente. Acima da tabela de dados, clique em **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >A origem do arquivo de feed (&quot;[!UICONTROL FTP]&quot; ou &quot;&amp;mdash&quot; para arquivos carregados manualmente) está incluída na coluna [!UICONTROL Source].

1. Especifique o arquivo a ser carregado inserindo o caminho completo e o nome do arquivo ou clicando em **[!UICONTROL Browse]** para localizar o arquivo no dispositivo ou na rede.

Mesmo que o novo arquivo tenha um nome ou extensão diferente, o arquivo existente será substituído pelo novo arquivo.

1. Clique em **[!UICONTROL Re-Upload]**.

Todos os campos no arquivo são validados. Não é possível postar itens com comprimentos de campo inválidos posteriormente até que você corrija os valores. Todos os nomes de colunas no arquivo ficam disponíveis em modelos como parâmetros dinâmicos.

## Excluir arquivos de feed

Você pode excluir qualquer arquivo de feed que tenha sido carregado manualmente ou via FTP. Ao excluir um arquivo de feed, ele não é mais associado a nenhum modelo.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Feeds]**.

1. Marque a caixa de seleção ao lado de cada arquivo que você deseja excluir.

1. Acima da tabela de dados, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagar dados de feed por meio de modelos](feed-data-propagate.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status de dados gerados a partir de feeds](propagated-data-status.md)
