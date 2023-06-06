---
title: Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica
description: Saiba como criar e gerenciar [!DNL Google Ads] alvos de pesquisa dinâmica.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica

*[!DNL Google Ads]somente contas*

Você pode criar, editar e alterar o status de alvos de pesquisa dinâmica para campanhas que usam a rede de pesquisa.

>[!NOTE]
>
>Você pode criar e editar grandes quantidades de dados de destino de uma só vez fazendo upload [arquivos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) e publicá-los na rede de publicidade.

## Criar um [!DNL Google Ads] destino de pesquisa dinâmica

Você pode criar destinos de pesquisa dinâmica para definir páginas em seus sites (ou seja, os domínios usados nos URLs de exibição de seus anúncios) cujo conteúdo é usado para direcionar seus anúncios de pesquisa dinâmica no mesmo grupo de anúncios.

Você pode direcionar todos os critérios ou até três critérios individuais.

>[!NOTE]
>
>Para melhor monitorar o desempenho, crie um &quot;[!UICONTROL All Targets]&quot; para apenas um grupo de anúncios por campanha.

>[!TIP]
>
>Para criar muitos componentes da conta de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade, a conta, a campanha e o grupo de publicidade e clique em **[!UICONTROL Continue]**.

1. Especifique a [configurações do dynamic search target](#dynamic-search-target-settings).

1. Clique em **[!UICONTROL Post]**.

## Editar [!DNL Google Ads] configurações do dynamic search target

É possível editar o status ou o lance máximo de um [!DNL Google Ads] destino de pesquisa dinâmica. Você não pode alterar os critérios de destino.

>[!TIP]
>
>Para editar grandes quantidades de dados de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada linha a ser editada.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Especifique a [configurações do dynamic search target](#dynamic-search-target-settings).

   Para vários alvos, as alterações são aplicadas a todos os alvos selecionados. Para o [!UICONTROL Bid field], você tem opções para alterar os valores existentes para um valor especificado ou para aumentar ou diminuir o valor em uma porcentagem especificada ou valor monetário, com um limite.

1. Salve os dados:

   * (Alvos únicos) Clique em **[!UICONTROL Post]**.

   * (Vários grupos de anúncios) Clique **[!UICONTROL Post Now]**.

## Alterar o status de [!DNL Google Ads] destinos de pesquisa dinâmica

Você pode pausar qualquer público alvo de pesquisa dinâmica ativo em um tipo de campanha compatível para não usá-los mais em anúncios de pesquisa dinâmica no mesmo grupo de anúncios. Posteriormente, você pode usá-los como alvos alterando o status do anúncio de volta para ativo.

Também é possível excluir qualquer destino dinâmico.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Opcional) Filtre a lista para incluir destinos dinâmicos específicos.

1. Siga um destes procedimentos:

   * Para alterar o status de um target dinâmico, clique no **[!UICONTROL Status]** e altere o status.

   * Para excluir um ou mais destinos dinâmicos, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada destino dinâmico que você deseja excluir.
      Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Na barra de ferramentas, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e selecione **[!UICONTROL Delete]**.

      1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.


## [!DNL Google Ads] configurações do dynamic search target {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Obrigatório quando você não especifica um domínio de site e idioma no [!UICONTROL DSA Options] seção; somente leitura para destinos existentes) Alvos de pesquisa dinâmica para o grupo de publicidade:

* *[!UICONTROL All Targets]* (o padrão): segmenta todas as páginas indexadas.

* *\[Destinos específicos\]:* Direciona até três critérios para as páginas indexadas. Ao selecionar essa opção, você deve especificar os critérios especificando categorias de informações e valores específicos para os quais os anúncios devem ser direcionados (por exemplo, &quot;URL contém shoes.example.com&quot;). Para especificar mais de um critério, clique em **[!UICONTROL + And]**. Os critérios de direcionamento incluem:

   * *[!UICONTROL Category]:* Para mostrar anúncios de páginas indexadas com um [!DNL Google Ads] categoria de conteúdo.

   * *[!UICONTROL URL]:* Para mostrar anúncios de páginas indexadas com um URL específico, onde o valor pode ser incluído em qualquer lugar no URL.

   * *[!UICONTROL Page Title]:* Para mostrar anúncios de páginas indexadas com texto específico no título da página.

   * *[!UICONTROL Page Content]:* Para mostrar anúncios de páginas indexadas com conteúdo específico.

**Status:** O status das configurações do target:

* *[!UICONTROL Active]* (o padrão): Permite lances.

* *[!UICONTROL Paused]:* Desabilita lances.

* *[!UICONTROL Deleted]* (somente destinos existentes): exclui as definições de destino.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** O CPC (custo máximo por clique) de um anúncio ou o CPM (custo por 1000 impressões) de um anúncio, conforme aplicável à rede de anúncios e ao modelo de preços da campanha. Esse valor substitui o valor no nível do grupo de anúncios.

>[!NOTE]
>
>Se o target estiver em um portfólio otimizado, a oferta de CPC especificada será aplicada por um dia. Posteriormente, o recurso de otimização coloca ofertas de acordo com seus próprios cálculos.

>[!MORELIKETHIS]
>
>* [Sobre [!DNL Google Ads] destinos de pesquisa dinâmica](dynamic-search-target-about.md)

