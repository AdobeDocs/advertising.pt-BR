---
title: Gerenciar palavras-chave
description: Saiba como criar e gerenciar palavras-chave licitáveis e negativas e atribuir restrições a palavras-chave.
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
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%
---
# Gerenciar palavras-chave

*recurso do Beta*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] e contas [!DNL Baidu] existentes apenas*

Uma palavra-chave é uma palavra ou frase associada a um anúncio. As configurações de palavra-chave incluem o tipo de correspondência de palavra-chave, os lances máximos a serem usados quando seu anúncio é acionado pela palavra-chave e (para algumas redes de anúncios) parâmetros de rastreamento opcionais. As configurações de nível de palavra-chave substituem as configurações de campanha ou do grupo de anúncios. Palavras-chave negativas impedem que anúncios sejam exibidos para pesquisas correspondentes.

Depois que você [tornar uma conta de rede de publicidade acessível por meio de uma conexão de API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) e o Search, Social e Commerce tiver sincronizado os dados da conta com a rede de publicidade, você poderá criar palavras-chave para grupos de anúncios de pesquisa em [tipos de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md). Você também pode editar e alterar o status de palavras-chave, além de criar e excluir palavras-chave negativas.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Sobre a exibição [!UICONTROL Keywords] {#keyword-view-about}

A exibição [!UICONTROL Manage] > [!UICONTROL Keywords] inclui duas guias para a conta de anunciante selecionada:

* A guia [!UICONTROL Keywords] lista todas as palavras-chave licitáveis na exibição filtrada.

* A guia [!UICONTROL Negatives] lista todas as palavras-chave negativas na exibição filtrada.

### Ações disponíveis

* [Criar palavras-chave](#keyword-create)

* [Criar palavras-chave negativas](#keyword-negative-create)

* [Editar configurações de palavra-chave](#keyword-edit)

* [Alterar o status ou excluir palavras-chave e palavras-chave negativas](#keyword-status)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

* [Atribuir restrições a palavras-chave e cancelar atribuição de restrições a palavras-chave](#keyword-constraints)

* [Atribuir classificações de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) a palavras-chave

## Criar palavras-chave {#keyword-create}

>[!TIP]
>
>Para criar um grande número de palavras-chave de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]**, clique em **[!UICONTROL Create Keywords]**.

1. Na etapa **[!UICONTROL Basic Settings]**, selecione a rede, a conta, a campanha e o grupo de anúncios.

1. Insira as [[!DNL Baidu] configurações de palavra-chave](keyword-settings-baidu.md), [[!DNL Google Ads] configurações de palavra-chave](keyword-settings-google.md), [[!DNL LY Ads] configurações de palavra-chave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] configurações de palavra-chave](keyword-settings-microsoft.md) ou [[!DNL Yandex] configurações de palavra-chave](keyword-settings-yandex.md).

   Você pode inserir ou colar até 2000 palavras-chave em uma operação. Separe várias palavras-chave com vírgulas ou insira-as em linhas separadas.

   >[!NOTE]
   >
   >Se as configurações de conta ou campanha especificarem o rastreamento somente no nível do anúncio, o Search, Social e Commerce não gerará o rastreamento para palavras-chave.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere as configurações de entidade e/ou palavra-chave.

1. Clique em **[!UICONTROL Create]**.

## Editar configurações de palavra-chave {#keyword-edit}

Alterar o texto da palavra-chave ou o tipo de correspondência pode excluir a palavra-chave existente e criar uma nova, dependendo da rede de anúncios. Consulte as configurações de palavras-chave da sua rede de publicidade para obter detalhes.

>[!TIP]
>
>Para editar uma grande quantidade de dados de palavras-chave de uma só vez, incluindo palavras-chave em diferentes redes de anúncios, use os [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]**, marque a caixa de seleção ao lado de cada palavra-chave a ser editada.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite as [[!DNL Baidu] configurações de palavra-chave](keyword-settings-baidu.md), [[!DNL Google Ads] configurações de palavra-chave](keyword-settings-google.md), [[!DNL LY Ads] configurações de palavra-chave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] configurações de palavra-chave](keyword-settings-microsoft.md) ou [[!DNL Yandex] configurações de palavra-chave](keyword-settings-yandex.md).

   Para várias palavras-chave, você pode editar apenas os campos que são comuns a todas as palavras-chave selecionadas e suas alterações serão aplicadas a todas as palavras-chave selecionadas. Para alguns campos alfanuméricos, é possível alterar os valores existentes para um valor especificado, substituir uma string existente por uma string especificada, adicionar um prefixo ou anexar um sufixo. Para alguns campos monetários, você pode alterar valores existentes para um valor especificado ou aumentar ou diminuir o valor em uma porcentagem ou quantia monetária especificada, com um limite.

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere as configurações de palavra-chave.

1. Clique em **[!UICONTROL Update]**.

## Criar palavras-chave negativas {#keyword-negative-create}

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] e contas [!DNL Baidu] existentes apenas*

Você pode criar palavras-chave negativas para um grupo de anúncios de pesquisa ou campanha direcionada à pesquisa ou exibição/rede nativa.

>[!NOTE]
>
>Você também pode criar e editar palavras-chave negativas nas [configurações do grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) e [configurações da campanha](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Para criar um grande número de palavras-chave negativas de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Negatives]**, clique em **[!UICONTROL Create Negatives]** e depois em **[!UICONTROL Campaign Negative Keyword]** ou **[!UICONTROL Ad Group Negative Keyword]**.

1. Selecione a rede, a conta, a campanha e (para palavras-chave negativas no nível do grupo de anúncios) o grupo de anúncios.

1. Insira as palavras-chave negativas. Use a sintaxe a seguir, sem um sinal de menos (`-`):

   * Correspondência ampla negativa: `keyword` (sem suporte de [!DNL Microsoft Advertising])

   * Correspondência de frase negativa: `"keyword"`

   * Correspondência exata negativa: `[keyword]`

   Separe vários valores com vírgulas ou insira-os em linhas separadas. Você pode inserir ou colar até 2.000 palavras-chave negativas em uma operação. Os seguintes requisitos e restrições se aplicam:

   * Tamanho máximo de caracteres: [!DNL Baidu]: 30 byte único ou 15 bytes duplos; [!DNL Microsoft Advertising]: 100 byte único ou 50 byte duplo; [!DNL Google Ads] e [!DNL LY Ads]: 80 byte único ou 40 byte duplo.

   * [!DNL Baidu] permite somente um tipo de correspondência por palavra-chave por grupo de publicidade. Por exemplo, o Grupo de Anúncios 1 não pode incluir `"keyword"` e `[keyword]`.

   * [!DNL Google Ads]: Cada palavra-chave não pode consistir em mais de 10 palavras e pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [ ] ' + . / :`

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** e altere a entidade e/ou as palavras-chave negativas.

1. Clique em **[!UICONTROL Create]**.

## Alterar o status de palavras-chave e palavras-chave negativas {#keyword-status}

Você pode pausar uma palavra-chave de pesquisa ativa e licitável para desativar a licitação nela. Posteriormente, é possível retomar o lance alterando o status para ativo.

Você também pode excluir palavras-chave de pesquisa ativas ou pausadas, ou palavras-chave negativas. As palavras-chave excluídas são excluídas da rede de publicidade. Elas ainda estarão visíveis ao serem incluídas no filtro de dados, mas não poderão ser alteradas.

### Ativar ou pausar palavras-chave

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]**, você pode filtrar a lista e marcar a caixa de seleção ao lado de cada palavra-chave cujo status deseja alterar.

1. Na barra de ferramentas de ações em massa, altere o status:

   * Para ativar palavras-chave pausadas, clique em **[!UICONTROL Activate]**.

   * Para pausar palavras-chave ativas, clique em **[!UICONTROL Pause]**.

### Excluir palavras-chave ou palavras-chave negativas

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]** ou **[!UICONTROL Negatives]**, filtre opcionalmente a lista e marque a caixa de seleção ao lado de cada palavra-chave ou palavra-chave negativa a ser excluída.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Gerenciar atribuições de restrição para palavras-chave {#keyword-constraints}

Você pode atribuir e remover restrições de licitação para campanhas, grupos de anúncios, palavras-chave, disposições, grupos de produtos no nível da unidade e alvos de pesquisa dinâmica. Cada entidade pode ter apenas uma restrição.

As restrições são herdadas por entidades filhas, portanto, não é necessário atribuir restrições a entidades filhas, a menos que você deseje substituir os valores herdados.

Desfazer a atribuição de uma restrição remove a associação com os componentes da conta e todos os seus componentes filhos, e os dados do relatório para a restrição não estão mais disponíveis para esses componentes. Cancelar a atribuição de uma restrição não exclui a restrição nem os próprios componentes da conta.

>[!NOTE]
>
>* Posteriormente, se você editar uma palavra-chave ou a cópia de anúncio para um anúncio não mutável, criando assim uma nova palavra-chave ou anúncio, a restrição não será atribuída à nova entidade.
>* As restrições ativas restringem os lances somente para unidades de lance atribuídas em portfólios de nível de palavra-chave herdada otimizados. Elas são ignoradas para unidades de oferta que estão em portfólios ativos, estão em portfólios híbridos ou não estão em portfólios.

### Atribuir uma restrição a palavras-chave {#keyword-constraint-assign}

Você pode atribuir uma única restrição a uma ou mais palavras-chave.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]**, marque a caixa de seleção ao lado de cada palavra-chave à qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

### Cancelar atribuição de restrições a palavras-chave {#keyword-constraint-unassign}

O cancelamento da atribuição de uma restrição não a exclui. Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;Excluir restrições para unidades de oferta de pesquisa&quot; no capítulo do Guia de Otimização em &quot;Restrições de oferta&quot;, que está disponível no Search, Social e Commerce.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Na guia **[!UICONTROL Keywords]**, marque a caixa de seleção ao lado de cada palavra-chave da qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] configurações de palavra-chave](keyword-settings-baidu.md)
>* [[!DNL Google Ads] configurações de palavra-chave](keyword-settings-google.md)
>* [[!DNL LY Ads] configurações de palavra-chave](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] configurações de palavra-chave](keyword-settings-microsoft.md)
>* [[!DNL Yandex] configurações de palavra-chave](keyword-settings-yandex.md)
>* [Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gerenciar classificações de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
