---
title: Gerenciar disposições
description: Saiba como criar e gerenciar inserções e inserções negativas de Google Ads e atribuir restrições a inserções.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 0%
---
# Gerenciar disposições

*recurso do Beta*

*[!DNL Google Ads]somente contas*

Posicionamentos são locais na rede de exibição nos quais seus anúncios podem aparecer. As configurações de posicionamento incluem o lance máximo e os parâmetros de rastreamento opcionais. As configurações de nível de posicionamento substituem as configurações de campanha ou do grupo de anúncios. Posicionamentos negativos impedem que os anúncios sejam exibidos em sites especificados.

Depois que você [tornar uma conta de rede de publicidade acessível por meio de uma conexão de API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) e o Search, Social e Commerce tiver sincronizado os dados da conta com a rede de publicidade, você poderá criar posicionamentos para grupos de anúncios em [tipos de campanha compatíveis](/help/search-social-commerce/introduction/supported-inventory.md) que direcionem a rede de exibição. Também é possível editar e alterar o status de disposições, além de criar e excluir disposições negativas.

>[!NOTE]
>
>[!DNL Google Ads] não fornece dados de desempenho no nível de anúncio para posicionamentos.

## Sobre a exibição [!UICONTROL Placements] {#placement-view-about}

A exibição [!UICONTROL Targeting] > [!UICONTROL Placements] inclui duas guias para a conta de anunciante selecionada:

* A guia [!UICONTROL Placements] lista todos os posicionamentos licitáveis na exibição filtrada.

* A guia [!UICONTROL Negatives] lista todos os posicionamentos negativos na exibição filtrada.

A exibição da página requer a permissão [!UICONTROL View Placements]. Criar posicionamentos ou posicionamentos negativos, editar posicionamentos, alterar o status do posicionamento e excluir posicionamentos ou posicionamentos negativos requer a permissão [!UICONTROL Edit Placements].

### Ações disponíveis

* [Criar inserções](#placement-create)

* [Criar posicionamentos negativos](#placement-negative-create)

* [Editar configurações de posicionamento](#placement-edit)

* [Alterar o status ou excluir disposições e disposições negativas](#placement-status)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

* [Atribuir restrições a disposições e cancelar atribuição de restrições a disposições](#placement-constraints)

* [Atribuir classificações de rótulo a posicionamentos](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Criar inserções {#placement-create}

>[!TIP]
>
>Para criar um grande número de posicionamentos de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, clique em **[!UICONTROL Create Placement]**.

1. Na etapa **[!UICONTROL Basic Settings]**, selecione a rede, a conta, a campanha e o grupo de anúncios.

1. Insira as [configurações de posicionamento](#placement-create-settings).

   Para criar vários posicionamentos, separe os URLs do site com vírgulas.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere a entidade e/ou as configurações de posicionamento.

1. Clique em **[!UICONTROL Create]**.

## Criar posicionamentos negativos {#placement-negative-create}

Você pode criar posicionamentos negativos para uma campanha ou grupo de anúncios [!DNL Google Ads] direcionado à rede de exibição.

>[!NOTE]
>
>Você também pode criar e editar posicionamentos negativos nas [configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) e [configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Para criar um grande número de posicionamentos negativos de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Negatives]**, clique em **[!UICONTROL Create Negative]** e depois em **[!UICONTROL Campaign Negative]** ou **[!UICONTROL Ad Group Negative]**.

1. Na etapa **[!UICONTROL Basic Settings]**, selecione a rede, a conta, a campanha e (para posicionamentos negativos no nível do grupo de anúncios) o grupo de anúncios.

1. Na etapa **[!UICONTROL Manage Websites]**, insira as URLs de site negativas, como `www.example.com` ou `example.com/shoes`.

   Separe vários URLs com vírgulas. Este formulário aceita URLs de site, não sequências de caracteres de tópico ou categoria.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere a entidade e/ou as URLs negativas do site.

1. Clique em **[!UICONTROL Create]**.

## Editar configurações de posicionamento {#placement-edit}

É possível editar o status, a oferta, o URL base e o modelo de rastreamento de um ou mais posicionamentos. Não é possível alterar o URL do site de destino ou editar disposições excluídas.

>[!TIP]
>
>Para editar uma grande quantidade de dados de posicionamento de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, marque a caixa de seleção ao lado de cada posicionamento a ser editado.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. No painel **[!UICONTROL Edit Placements]**, edite as [configurações de posicionamento](#placement-edit-settings).

   Para várias disposições, as alterações são aplicadas a todas as disposições selecionadas. Você pode definir lances para um valor especificado ou aumentá-los ou diminuí-los em uma porcentagem ou quantia monetária especificada, com um limite. Para URLs, você pode substituir o valor existente, localizar e substituir texto, adicionar um prefixo ou anexar um sufixo.

   A edição de lances é desativada quando as disposições selecionadas usam várias moedas.

1. Clique em **[!UICONTROL Save]**.

## Alterar o status de disposições e disposições negativas {#placement-status}

Você pode pausar uma disposição ativa e licitável para desativar a licitação nela. Posteriormente, é possível retomar o lance alterando o status para ativo.

Também é possível excluir disposições ativas ou pausadas ou disposições negativas. Os posicionamentos excluídos são excluídos da rede de anúncios. Elas ainda estarão visíveis ao serem incluídas no filtro de dados, mas não poderão ser alteradas.

### Ativar ou pausar inserções

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, você pode filtrar a lista e marcar a caixa de seleção ao lado de cada posicionamento cujo status deseja alterar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Na seção **[!UICONTROL Placement Details]**, altere o **[!UICONTROL Status]**:

   * Para ativar os posicionamentos pausados, selecione **[!UICONTROL Active]**.

   * Para pausar disposições ativas, selecione **[!UICONTROL Paused]**.

1. Clique em **[!UICONTROL Save]**.

### Excluir disposições ou disposições negativas

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]** ou **[!UICONTROL Negatives]**, filtre opcionalmente a lista e marque a caixa de seleção ao lado de cada posicionamento ou posicionamento negativo a ser excluído.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Gerenciar atribuições de restrição para disposições {#placement-constraints}

Você pode atribuir e remover restrições de licitação para campanhas, grupos de anúncios, palavras-chave, disposições, grupos de produtos no nível da unidade e alvos de pesquisa dinâmica. Cada entidade pode ter apenas uma restrição.

As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Cancelar a atribuição de uma restrição não exclui a restrição nem os próprios componentes da conta.

>[!NOTE]
>
>* Posteriormente, se você editar uma palavra-chave ou a cópia de anúncio para um anúncio não mutável, criando assim uma nova palavra-chave ou anúncio, a restrição não será atribuída à nova entidade.
>* As restrições ativas restringem os lances somente para unidades de lance atribuídas em portfólios de nível de palavra-chave herdada otimizados. Elas são ignoradas para unidades de oferta que estão em portfólios ativos, estão em portfólios híbridos ou não estão em portfólios.

### Atribuir uma restrição aos posicionamentos {#placement-constraint-assign}

Você pode atribuir uma única restrição a uma ou mais disposições.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, marque a caixa de seleção ao lado de cada posicionamento ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

### Cancelar atribuição de restrições de posicionamentos {#placement-constraint-unassign}

O cancelamento da atribuição de uma restrição não a exclui. Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;[Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status).&quot;

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Na guia **[!UICONTROL Placements]**, marque a caixa de seleção ao lado de cada posicionamento do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Configurações de posicionamento {#placement-settings}

### Configurações ao criar inserções {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** A rede de anúncios. Somente [!DNL Google Ads] é suportado.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites na rede de exibição na qual seu anúncio pode aparecer. Insira uma URL de site válida, como `www.example.com`, `example.com` ou `example.com/shoes`. Separe vários URLs com vírgulas. A URL não pode incluir um ponto de interrogação (`?`).

Para excluir sites, [crie posicionamentos negativos](#placement-negative-create) da guia [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] ou use as configurações de campanha e do grupo de anúncios.

**[!UICONTROL Status]:** O status de exibição do posicionamento: *[!UICONTROL Active]* (para habilitar lances) ou *[!UICONTROL Paused]* (para desabilitar lances).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (opcional) o custo máximo por clique (CPC) ou o custo por mil impressões visualizáveis (vCPM) para o anúncio baseado em posicionamento, dependendo da estratégia de oferta da campanha. Esse valor substitui a oferta de nível de grupo de anúncios.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>O formulário de criação de new-UI requer a URL base e o modelo de rastreamento, quando especificado, para começar com `http://` ou `https://`.

### Configurações ao editar disposições {#placement-edit-settings}

O painel [!UICONTROL Edit Placements] oferece suporte às seguintes configurações para um ou mais posicionamentos selecionados. Você não pode alterar a URL do site de destino.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** Como alterar a oferta:

* *[!UICONTROL Set to]:* Substitua o lance existente por um valor especificado.

* *[!UICONTROL Increase]:* Aumente o lance existente em um valor ou porcentagem especificada.

* *[!UICONTROL Decrease]:* Diminua o lance existente em uma quantidade ou porcentagem especificada.

**[!UICONTROL Modifier type]:** (Para aumentos ou diminuições) Se o ajuste usa *[!UICONTROL Currency]* ou *[!UICONTROL Percentage]*.

**[!UICONTROL Set value]:** O novo lance ou o valor de ajuste. O valor mínimo é 0,01.

**[!UICONTROL Max limit]:** (Para aumentos ou reduções; opcional) O limite para a oferta ajustada. Para um aumento, este é o lance máximo; para uma diminuição, este é o lance mínimo. O valor limite mínimo é 0,01.

A edição de lances é desativada quando as disposições selecionadas usam várias moedas.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** Para cada campo, selecione como modificar o valor:

* *[!UICONTROL Set To]:* Substitua o valor. Insira uma URL de site válida que comece com `http://` ou `https://`.

* *[!UICONTROL Find/Replace]:* Substituir texto especificado dentro do valor. Insira o texto a ser localizado e o texto de substituição.

* *[!UICONTROL Add Suffix]:* Anexar texto ao valor. Insira o texto do sufixo.

* *[!UICONTROL Add Prefix]:* Adicione texto ao início do valor. Insira o texto do prefixo.

>[!NOTE]
>
>Todas as novas URLs de base devem ser URLs válidas que comecem com `http://` ou `https://`.

>[!MORELIKETHIS]
>
>* [Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gerenciar classificações de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
