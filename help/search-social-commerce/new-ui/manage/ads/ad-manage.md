---
title: Gerenciar anúncios
description: Saiba como criar e gerenciar anúncios, incluindo os tipos de anúncios disponíveis.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6a479ae0bb30d609b16a343efcec296137b9ab43
workflow-type: tm+mt
source-wordcount: 1733
ht-degree: 0%

---

# Gerenciar anúncios

*recurso do Beta*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] e contas [!DNL Baidu] existentes apenas*

Um anúncio pertence a um grupo de anúncios e contém o conteúdo que é exibido aos usuários — como o título, a descrição, a imagem ou outros elementos criativos — dependendo da rede de anúncios e do tipo de anúncio.

Depois que você [tornar uma conta de rede de publicidade acessível por meio de uma conexão de API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e o Search, Social e Commerce tiver sincronizado os dados da conta com a rede de publicidade, você poderá criar anúncios para um [tipo de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md). Também é possível editar e alterar o status dos anúncios.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Sobre a exibição [!UICONTROL Ads] {#ad-view-about}

A exibição [!UICONTROL Manage] > [!UICONTROL Ads] lista todos os anúncios na exibição filtrada para a conta de anunciante selecionada.

### Ações disponíveis

* [Criar um anúncio](#ad-create)

* [Renomear um anúncio dentro da linha](#ad-rename)

* [Editar configurações de publicidade](#ad-edit)

* [Alterar o status ou excluir um anúncio](#ad-status)

* [Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Ads]](#ad-reports)

## Tipos de anúncios disponíveis {#ad-types}

Você pode criar e gerenciar os tipos de anúncios suportados para grupos de anúncios em uma conta de rede de anúncios sincronizada:

* **Anúncios de texto ou anúncios de texto expandidos** para um grupo de publicidade em uma campanha direcionada à rede de pesquisa. Os anúncios de texto podem incluir parâmetros de rastreamento opcionais que substituem os parâmetros de nível de grupo ou campanha do anúncio. Dependendo da rede de anúncios, talvez seja possível criar anúncios de texto expandidos/estendidos ou anúncios de texto padrão.

* Anúncios **de público-alvo** nativo entre dispositivos para campanhas [!DNL Microsoft Advertising] no [!DNL Microsoft Audience Network]. Você tem duas opções para anúncios de público-alvo, com base nas configurações da campanha:

  * Se a campanha estiver vinculada a uma loja central de comerciantes, permita que a rede de publicidade gere automaticamente anúncios baseados em feed para a campanha, usando as informações de produto da loja. Não é necessário criar anúncios baseados em feed para a campanha, mas você deve criar grupos de anúncios com direcionamento do usuário.

  * Se a campanha não estiver vinculada a uma conta do centro do comerciante, crie anúncios de público-alvo baseados em imagem usando o formato de anúncio responsivo, que inclui vários ativos de texto e imagem. A rede de anúncios reúne os anúncios usando as combinações mais eficazes de elementos de anúncios e os exibe em sites como [!DNL MSN], [!DNL Outlook.com] e [!DNL Microsoft Edge].

* **Anúncios somente de chamada** para [!DNL Google Ads] campanhas na rede de pesquisa. Anúncios somente para chamada são anúncios de texto que incluem um número de telefone. Você também pode usar um número de encaminhamento [!DNL Google Ads]-atribuído para relatórios de chamada avançados.

  >[!NOTE]
  >
  >No momento, não é possível criar ou editar anúncios somente para chamada. Você pode visualizar, alterar o status ou excluir um anúncio somente chamada existente.

* **Anúncios de pesquisa dinâmica expandidos** (agora chamados apenas de &quot;anúncios de pesquisa dinâmica&quot; nas redes de publicidade) para [!DNL Google Ads] e [!DNL Microsoft Advertising] grupos de anúncios de pesquisa dinâmica em campanhas de pesquisa. Os anúncios de pesquisa dinâmicos usam o conteúdo de seu site, em vez de palavras-chave, para decidir quando mostrar seus anúncios. A rede de publicidade gera dinamicamente o título, escolhe o URL da página de aterrissagem e o URL de exibição e gera automaticamente o URL final.

  Para obter mais informações sobre anúncios de pesquisa dinâmica, consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/2471185) e a [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Anúncios multimídia** para [!DNL Microsoft Advertising] campanhas de pesquisa. Anúncios multimídia são anúncios de imagens grandes, exibidos em posições proeminentes da linha principal e da barra lateral, e apenas um anúncio multimídia é exibido por página. Eles podem incluir vários ativos de texto e imagem, como anúncios responsivos, e a rede de anúncios monta os anúncios usando as combinações mais eficazes de elementos de anúncios. Os anúncios multimídia não substituem os posicionamentos de anúncios de texto.

* Linhas de promoção para **[!DNL Microsoft Advertising]anúncios de produtos (compras)** na rede de compras. Os anúncios de compras usam produtos no seu feed de produto existente do [!DNL Microsoft Merchant Center], em vez de palavras-chave, para decidir como e onde mostrar seus anúncios. Os URLs da cópia de anúncio e da página de aterrissagem são gerados automaticamente a partir das informações do produto no feed, mas você pode, opcionalmente, configurar linhas de promoção a serem incluídas no grupo de anúncios.

  Para obter mais informações sobre anúncios de produtos, consulte a [documentação do Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Anúncios de pesquisa responsivos** para campanhas [!DNL Google Ads] e [!DNL Microsoft Advertising] na rede de pesquisa. A rede de publicidade monta dinamicamente anúncios de pesquisa responsivos baseados em texto a partir de um conjunto de títulos e descrições de anúncios, favorecendo combinações com bom desempenho juntas. O anúncio inclui até três títulos, duas descrições e um URL personalizável do URL base e campos opcionais de caminho 1 e caminho 2. Opcionalmente, é possível fixar títulos e descrições de anúncios em posições específicas.

  >[!NOTE]
  >
  >[!DNL Google Ads] não fornece dados fora de seus editores nativos sobre as combinações de texto que foram exibidas como anúncios. Para obter mais informações sobre relatórios para cada combinação de texto, consulte a [documentação do Google Ads](https://support.google.com/google-ads/answer/7684791).

### Dados de desempenho no nível do anúncio

Os dados no nível do anúncio estão disponíveis para a maioria dos tipos de anúncios.

No entanto, não está disponível para [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA), desempenho máximo, compras inteligentes e [!DNL YouTube] campanhas. Espere discrepâncias entre o total de dados de nível de anúncio de uma campanha e o total de dados da campanha.

| Rede de publicidade/Campanha/Tipo de anúncio | Disponibilidade de dados |
|---|---|
| [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA) | Campanha, grupo de publicidade |
| [!DNL Google Ads] desempenho máximo | Campaign |
| [!DNL Google Ads] compras, compras inteligentes | Campanha, grupo de publicidade |
| [!DNL Google Ads] [!DNL YouTube] | Campanha, grupo de publicidade |

## Criar um anúncio {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* Não é necessário criar anúncios de produtos para campanhas de compras; a rede de anúncios os cria automaticamente. No entanto, para campanhas de compras de [!DNL Microsoft Advertising], é possível definir linhas de promoção a serem incluídas nos anúncios.
>* Você não pode criar [!DNL Google Ads] anúncios somente para chamada.

>[!TIP]
>
>Para criar um grande número de anúncios ao mesmo tempo, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Clique em **[!UICONTROL Create Ads]**.

1. Na etapa **[!UICONTROL Basic Settings]**, selecione a rede, a conta, a campanha, o grupo de anúncios e o tipo de anúncio.

   Para obter mais informações sobre os tipos de anúncios disponíveis, consulte &quot;[Tipos de anúncios disponíveis](#ad-types).&quot;

1. Especifique as configurações restantes para um [anúncio de texto do Baidu](ad-settings-baidu-text.md), [anúncio de pesquisa dinâmica expandido do Google Ads](ad-settings-google-dsa.md) (chamado apenas de &quot;anúncio de pesquisa dinâmica&quot; no Google Ads), [anúncio de pesquisa responsivo do Google Ads](ad-settings-google-rsa.md), [anúncio de pesquisa dinâmica expandido do Microsoft Advertising](ad-settings-microsoft-dsa.md), [anúncio multimídia do Microsoft Advertising](ad-settings-microsoft-multimedia.md), [anúncio de produto do Microsoft Advertising](ad-settings-microsoft-product.md), [anúncio responsivo (público-alvo) do Microsoft](ad-settings-microsoft-responsive.md), [anúncio de pesquisa responsivo do Advertising](ad-settings-microsoft-rsa.md) ou Configurações de [anúncio de texto Yandex](ad-settings-yandex-text.md).

   >[!NOTE]
   >
   >(Campanhas com rastreamento de conversão de Adobe Advertising) Se as configurações de conta ou campanha especificarem o rastreamento somente no nível da palavra-chave, o Search, Social e Commerce não gerará o rastreamento para anúncios.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere as configurações do anúncio.

1. Clique em **[!UICONTROL Create]**.

1. &#x200B;<!-- Add link to where to generate this once available to users-->(Anúncios de compras em campanhas com rastreamento de conversão do Adobe Advertising; opcional) Para rastrear cliques no anúncio, adicione manualmente um URL de rastreamento às configurações de conta, campanha ou grupo de produtos.

## Renomear um anúncio {#ad-rename}

Renomeie rapidamente um anúncio sem abrir as configurações completas do anúncio.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Mantenha o cursor sobre a linha de anúncio e clique em **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite o nome e clique em **[!UICONTROL Apply]**.

## Editar configurações de publicidade {#ad-edit}

>[!NOTE]
>
>* Os tipos de anúncios a seguir são *mutáveis*, o que significa que você pode alterar a cópia ou imagem do anúncio e manter a mesma ID de anúncio: todos os [!DNL Google Ads] tipos de anúncios, exceto anúncios de pesquisa dinâmica, e [!DNL Microsoft Advertising] anúncios de texto expandidos.
>* Todos os outros anúncios com suporte são *não mutáveis*, o que significa que alterar a cópia do anúncio ou a imagem excluirá o anúncio existente e criará um novo. O desempenho do novo anúncio pode ficar volátil por algumas semanas, enquanto o Search, Social e Commerce coleta dados suficientes para otimização.
>* Você não pode editar o conteúdo de um anúncio de produto, exceto para a linha de promoção para [!DNL Microsoft Advertising] anúncios de produto. No entanto, você pode pausar ou excluir um anúncio.
>* Você não pode editar [!DNL Google Ads] anúncios somente para chamada. No entanto, você pode pausar ou excluir um.
>* É possível editar apenas um anúncio por vez.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Marque a caixa de seleção ao lado do anúncio.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite as configurações restantes para um [anúncio de texto do Baidu](ad-settings-baidu-text.md), [anúncio de pesquisa dinâmica expandido do Google Ads](ad-settings-google-dsa.md) (agora chamado apenas de &quot;anúncio de pesquisa dinâmica&quot; no Google Ads), [anúncio de pesquisa responsivo do Google Ads](ad-settings-google-rsa.md), [anúncio de pesquisa dinâmica expandido do Microsoft Advertising](ad-settings-microsoft-dsa.md), [anúncio multimídia do Microsoft Advertising](ad-settings-microsoft-multimedia.md), [anúncio de produto do Microsoft Advertising](ad-settings-microsoft-product.md), [anúncio responsivo (público-alvo) do Microsoft](ad-settings-microsoft-responsive.md), [anúncio de pesquisa responsivo do Advertising](ad-settings-microsoft-rsa.md) ou Configurações de [anúncio de texto Yandex](ad-settings-yandex-text.md).

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere as configurações do anúncio.

1. Clique em **[!UICONTROL Update]**.

## Alterar o status de um anúncio {#ad-status}

Altere rapidamente o status de um anúncio sem abrir as configurações completas do anúncio.

Você pode pausar qualquer anúncio ativo em uma rede de anúncios compatível para desativar a licitação. Posteriormente, é possível retomar o lance alterando o status para ativo.

Você também pode excluir qualquer anúncio ativo ou pausado. Os anúncios excluídos são excluídos da rede de publicidade. Elas ainda estarão visíveis ao serem incluídas no filtro de dados, mas não poderão ser alteradas.

### Ativar ou pausar um anúncio

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Marque a caixa de seleção da linha de anúncio.

1. Na barra de ferramentas de ações em massa, altere o status:

   * Para ativar um anúncio pausado, clique em **[!UICONTROL Activate]**.

   * Para pausar um anúncio ativo, clique em **[!UICONTROL Pause]**.

### Excluir um anúncio

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Marque a caixa de seleção da linha de anúncio.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Ads] {#ad-reports}

Gere um relatório que inclua as linhas de dados de um ou mais anúncios na exibição [!UICONTROL Ads] e baixe o relatório como um arquivo de planilha do Microsoft Excel (formato XLXS). O relatório inclui todas as colunas visíveis na visualização.

É possível excluir qualquer relatório gerado.

Consulte também &quot;[(Interface herdada) Baixar dados de uma exibição de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interface herdada) Excluir um relatório de dados de desempenho ou arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Gerar um relatório com as linhas de dados filtradas

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Especifique os anúncios cujos dados você deseja baixar:

   * Para baixar dados de anúncios específicos, marque as caixas de seleção ao lado dos anúncios.

   * Para baixar dados para todos os anúncios, não é necessário marcar nenhuma caixa de seleção. Todos os anúncios são incluídos por padrão.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Nas configurações de [!UICONTROL Grid Reports], insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o arquivo é nomeado como &quot;ad_YYYMMDD_NNNN&quot;, onde &quot;NNNN&quot; é o número sequencial do trabalho (como &quot;ad_20250402_1326).

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] configurações de anúncio de texto](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] configurações expandidas de anúncios de pesquisa dinâmica](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] configurações responsivas de pesquisa e publicidade](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] configurações expandidas de anúncios de pesquisa dinâmica](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] configurações de anúncios multimídia](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] configurações de anúncio de produto](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] configurações de anúncios responsivos (público-alvo)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] configurações responsivas de pesquisa e publicidade](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] configurações de anúncio de texto](ad-settings-yandex-text.md)
