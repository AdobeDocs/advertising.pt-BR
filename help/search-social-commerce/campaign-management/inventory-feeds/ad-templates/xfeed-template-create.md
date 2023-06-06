---
title: Gerenciamento de modelos de feed
description: Saiba como criar um modelo de anúncio para feeds de dados de inventário.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Criar, clonar ou editar um modelo de feed

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Você pode criar modelos de anúncio específicos do mecanismo de pesquisa através dos quais os dados do inventário podem ser processados. Criar modelos separados para texto e anúncios de texto expandidos/estendidos, anúncios de pesquisa responsivos, [!DNL Google Ads] anúncios de compras e [!DNL Microsoft Advertising] anúncios de compras.

Além de criar modelos do zero, você pode criar novos modelos clonando os existentes.

Depois de criar ou clonar um modelo e associá-lo a um arquivo de feed de dados, você pode propagar os dados no arquivo por meio do modelo para criar dados da campanha e estrutura de conta.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

1. Siga um destes procedimentos:

   * Para criar um modelo do zero, clique em **[!UICONTROL Create/Clone]** na barra de ferramentas acima da tabela de dados e, em seguida, selecione a rede de anúncios aplicável.

   * Para clonar um template existente:

      1. Marque a caixa de seleção ao lado do modelo que você deseja copiar.

      1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create/Clone]** e selecione a rede de anúncios aplicável.
   * (Para editar um modelo existente) Ao lado do nome do modelo, clique em ![Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Exibir/editar configurações").


1. Especifique as configurações para o [modelo de anúncio de texto](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] modelo de anúncio de compras](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)ou [[!DNL Microsoft Advertising] modelo de anúncio de compras](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Na parte superior da janela de configurações do modelo, especifique o nome do modelo e a conta aplicável.

      Ao clonar um modelo existente, renomeie o novo modelo para que os anúncios criados a partir do novo modelo não sejam associados aos anúncios criados a partir do modelo de origem.

   1. (Opcional) Na coluna à esquerda, especifique o arquivo de feed de produto ou a conta do centro de comércio cujos dados serão propagados por meio do modelo:

      * (Para arquivos de feed de produto) Para selecionar um arquivo carregado anteriormente, clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Seta para baixo") e selecione um arquivo na lista de arquivos de feed disponíveis. Para fazer upload de um novo arquivo, especifique o arquivo inserindo o caminho e o nome completos ou clicando em **[!UICONTROL Browse]** para localizar o arquivo no dispositivo ou na rede e clique em **[!UICONTROL Upload]**.

      * (Para uma conta do centro do comerciante sincronizada) Selecione o nome da conta.

      As colunas do arquivo ou conta selecionada são exibidas.

   1. No **[!UICONTROL Account Structure]** especifique as configurações da estrutura de conta.

   1. (Somente anúncios de texto) Clique no link **[!UICONTROL Keywords]** e especifique as configurações de palavra-chave.

   1. (Texto e anúncios de pesquisa responsivos somente) Clique no link **[!UICONTROL Ads]** e execute um dos procedimentos a seguir:

      >[!NOTE]
      >
      >* É possível incluir até quatro modelos de variação de anúncios por modelo de anúncio de texto padrão, cinco modelos de variação de anúncios por modelo de anúncio de texto expandido/estendido e três modelos de variação de anúncios por modelo de anúncio de pesquisa responsivo.
      >* Cada grupo de publicidade pode incluir até três anúncios de pesquisa responsivos ativados.
      >* Não é possível editar variações de anúncios de texto padrão existentes, e os modelos existentes não geram mais anúncios de texto padrão.
      >* Se você alterar um modelo de variação de anúncios, os anúncios existentes poderão ser excluídos e novos poderão ser criados quando você propagar dados por meio do modelo, [dependendo do tipo de anúncio e da rede de anúncios](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).


      * Para adicionar uma variação de anúncio, faça o seguinte:

         1. Clique em **[!UICONTROL Add Ad Variation]** para criar um anúncio de texto, **[!UICONTROL Add ETA Variation]** para criar um anúncio de texto expandido/estendido, ou **[!UICONTROL Add RSA Variation]** para criar um anúncio de texto responsivo.

            Depois de especificar o tipo de anúncio, você pode criar somente esse tipo de anúncio com o modelo.

         1. Especifique as configurações do anúncio.

            Para anúncios de pesquisa responsivos, você pode incluir de 3 a 15 títulos e 2 a 4 descrições.

         1. (Opcional) Para preencher previamente todos os campos de texto alternativo do anúncio com texto dos campos de texto do anúncio original, marque a caixa de seleção ao lado de **[!UICONTROL Prefill]**.

         1. (Opcional) Para adicionar outro conjunto de cópias de anúncio a um anúncio, que pode ser usado se qualquer uma das linhas do anúncio original exceder o tamanho máximo depois que quaisquer parâmetros dinâmicos forem substituídos por dados durante a propagação, clique em **[!UICONTROL Add Alternate]** e, em seguida, adicione os valores alternativos.

            >[!NOTE]
            >
            >* Se a variável [!UICONTROL Prefill] for selecionada, os campos alternativos serão pré-preenchidos com os campos originais e você poderá editá-los conforme necessário.
            >* Somente os campos de cópia de anúncio que excedem o comprimento máximo são substituídos pelo valor alternativo. Por exemplo, se apenas um título ou título original for muito longo, a variação de anúncio gerada usará o título ou título alternativo e as descrições originais. Portanto, certifique-se de que o texto alternativo faça sentido quando combinado com o texto original do anúncio.
            >* Se a cópia do anúncio original atender aos requisitos de comprimento do mecanismo de pesquisa, a cópia alternativa do anúncio será descartada.
            >* É possível especificar até quatro alternativas para cada campo de texto publicitário.

         * Para editar uma variação de anúncio, faça o seguinte:

            1. Edite as configurações do anúncio.

               Para anúncios de pesquisa responsivos, você pode incluir de 3 a 15 títulos e 2 a 4 descrições.

            1. (Opcional) Para preencher previamente todos os campos de texto alternativo do anúncio com texto dos campos de texto do anúncio original, marque a caixa de seleção ao lado de **[!UICONTROL Prefill]**.

            1. (Opcional) Para adicionar outro conjunto de cópias de anúncio a um anúncio, que pode ser usado se qualquer uma das linhas do anúncio original exceder o tamanho máximo depois que quaisquer parâmetros dinâmicos forem substituídos por dados durante a propagação, clique em **[!UICONTROL Add Alternate]** e, em seguida, adicione os valores alternativos.

               >[!NOTE]
               >
               >* Se a variável [!UICONTROL Prefill] for selecionada, os campos alternativos serão pré-preenchidos com os campos originais e você poderá editá-los conforme necessário.
               >* Somente os campos de cópia de anúncio que excedem o comprimento máximo são substituídos pelo valor alternativo. Por exemplo, se apenas um título ou título original for muito longo, a variação de anúncio gerada usará o título ou título alternativo e as descrições originais. Portanto, certifique-se de que o texto alternativo faça sentido quando combinado com o texto original do anúncio.
               >* Se a cópia do anúncio original atender aos requisitos de comprimento do mecanismo de pesquisa, a cópia alternativa do anúncio será descartada.
               >* É possível especificar até quatro alternativas para cada campo de texto publicitário.

         * Para remover uma variação de anúncio, clique em **[!UICONTROL Remove ETA Variation]** (para anúncios de texto expandidos/estendidos) ou **[!UICONTROL Remove RSA Variation]** (para anúncios de pesquisa responsivos) ao lado dele, conforme aplicável.
   1. (Somente modelos de compras) Clique no link **[!UICONTROL Product Groups]** e especifique as informações sobre os grupos de produtos que deseja direcionar.

   1. (Opcional) Clique no link **[!UICONTROL Feed Filters]** e especifique quais linhas serão propagadas no arquivo de feed.

   1. (Opcional) Clique no link **[!UICONTROL Label Classifications tab]** e especifique os valores de classificação de rótulo para atribuir aos diferentes componentes de campanha que são criados:

      1. Clique na caixa de seleção ao lado de **[!DNL \[Component\] Label Classifications]**.

      1. Para cada classificação de rótulo a ser atribuída ao componente, faça o seguinte:

         1. Clique em **[!UICONTROL Add Label Classification]**.

         1. Selecione a classificação de etiqueta e selecione um valor existente ou insira um novo valor.





1. Salve o template:

   * Para simplesmente salvar o modelo, clique em **[!UICONTROL Save]** e clique em **[!UICONTROL Save]** novamente.

   * Para salvar o modelo e propagar o arquivo de dados especificado através dele, clique em **[!UICONTROL Save]** e clique em **[!UICONTROL Save & Propagate]**.

<!-- add more entries below -->

## Alterar o status dos modelos de feed

Você pode ativar qualquer modelo de feed de dados pausado ou pausar qualquer modelo de feed de dados ativo.

>[!NOTE]
>
>Você pode propagar dados manualmente por meio de um modelo pausado, mas os dados não são propagados automaticamente por meio dele.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

1. Marque a caixa de seleção ao lado de cada modelo cujo status você deseja alterar.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Change Status]** e clique em **[!UICONTROL Activate]** ou **[!UICONTROL Pause]**.

## Excluir modelos de feed

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

1. Marque a caixa de seleção ao lado de cada modelo que deseja excluir.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Sobre a automatização do gerenciamento de anúncios usando feeds de inventário](inventory-feeds-about.md)
>* [Fluxo de trabalho para gerenciar dados da campanha usando feeds de inventário](inventory-feeds-workflow.md)

