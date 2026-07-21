---
title: Gerenciar grupos de produtos de compras
description: Saiba mais sobre como criar, editar e excluir grupos de produtos de compras e consulte as configurações de grupo de produtos para Google Ads e Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# Gerenciar grupos de produtos de compras

*[!DNL Google Ads]e [!DNL Microsoft Advertising] campanhas de compras somente*

Você pode criar e gerenciar grupos de produtos na exibição [!UICONTROL Product Groups] em [!UICONTROL Assets] > [!UICONTROL Shopping].

Você pode exibir dados sobre grupos de produtos em [o [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md).

## O que são grupos de produtos?

Nas campanhas de compras, os grupos de produtos (e não as palavras-chave) determinam os produtos na conta da central de compras para os quais os anúncios de compras são exibidos. Cada grupo de produtos é baseado em um único atributo de produto (como categoria, tipo de produto, marca, condição, ID de produto ou rótulos personalizados) e usa a mesma oferta para todos os produtos correspondentes. É possível incluir ou excluir ofertas para os produtos em cada grupo.

Os grupos de produtos são configurados no nível do grupo de anúncios para determinar quais produtos nas contas do centro de comércio aparecem nos anúncios de compras do grupo de anúncios. Mesmo que o grupo de publicidade não inclua entidades de publicidade, a rede de publicidade ainda exibirá anúncios dos produtos.

Quando o mesmo produto é incluído em mais de uma campanha, a rede de publicidade usa primeiro a prioridade de campanha para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

Para obter mais informações sobre [!DNL Google] campanhas de compras e anúncios, consulte &quot;[Implementar [!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; e a [documentação do Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Para obter mais informações sobre [!DNL Microsoft] campanhas de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; e a [[!DNL Microsoft Advertising] documentação](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Suporte indisponível para [!DNL Google Ads] grupos de listagem em campanhas de desempenho máximo. Para gerenciar e exibir dados de grupos de listagem, use o editor [!DNL Google Ads].

### Hierarquia de grupo de produtos

Antes de criar grupos de produtos com atributos específicos para um grupo de anúncios, você deve primeiro criar um grupo de produtos com tudo incluído chamado &quot;[!UICONTROL All Products]&quot;. A partir desse grupo de produtos principal, você pode criar grupos de produtos secundários para subconjuntos de produtos e criar netos a partir dos grupos de produtos secundários. Depois de criar o primeiro grupo de produtos filho para um grupo de anúncios, outro grupo de produtos chamado &quot;[!UICONTROL Everything Else]&quot; será criado automaticamente usando a oferta padrão de grupo de anúncios. À medida que você adiciona mais grupos de produtos, o grupo &quot;[!UICONTROL Everything Else]&quot; é ajustado de acordo para constituir todos os produtos que não estão em outro grupo de produtos.

Em um grupo de anúncios, é possível criar até sete níveis de grupos de produtos (sem incluir &quot;[!UICONTROL All Products]&quot;) para incluir ou excluir de ofertas, com um ou mais grupos de produtos direcionados ao mesmo atributo em cada nível (por exemplo, [!UICONTROL Brand]=Acme para um grupo de produtos e [!UICONTROL Brand]=AcmePlus para outro no mesmo nível). Os grupos de produtos principais são chamados de subdivisões, e o nível mais baixo de subdivisão é conhecido como uma unidade. Você pode definir lances e modelos de rastreamento ou excluir completamente lances no nível da unidade. O conjunto inteiro de grupos de produtos ativos de um grupo de publicidade é aplicado hierarquicamente para determinar os produtos elegíveis. Por exemplo, se você subdividir o [!UICONTROL All Products] em [!UICONTROL Brand]=AcmeBasic e [!UICONTROL Brand]=AcmePlus e subdividir cada um desses grupos de produtos em [!UICONTROL Condition]=Novos e definir ofertas, apenas os novos produtos com as marcas AcmeBasic e AcmePlus poderão ser anunciados ou excluídos dos anúncios.

![Exemplo de um conjunto de grupos de produtos](/help/search-social-commerce/assets/product-group-list-new.png "Exemplo de um conjunto de grupos de produtos")

![Exemplo de hierarquia de grupo de produtos](/help/search-social-commerce/assets/product-group-tree-new.png "Exemplo de hierarquia de grupo de produtos")

### Filtros de produto {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

Consulte também a ajuda do [!DNL Google Ads] &quot;[Gerenciar uma campanha de compras com grupos de produtos](https://support.google.com/google-ads/answer/6275317)&quot; e a ajuda do [!DNL Microsoft Advertising] &quot;[Entender e usar grupos de produtos](https://help.ads.microsoft.com/#apex/bae/en/56782).&quot;

| Rede de compras | Dimension do produto | Atributos | Notas |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] to [!UICONTROL Category 5=] | \[A ID da categoria\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[A marca\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[A ID do item\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] a [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[O tipo de produto\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] a [!UICONTROL Custom Label 4=] | \[O atributo para o rótulo personalizado\] | — |
| [!DNL Google Ads] | Canal= | [!UICONTROL Local], [!UICONTROL Online] | Para mostrar anúncios somente para produtos locais ou online.<br><br><b>Observação:</b> Para criar anúncios para produtos locais, a opção &quot;Anúncios de Inventário Local&quot; deve estar habilitada e você deve participar do programa de compras local com [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Mostrar anúncios de produtos que estão disponíveis apenas para um único canal (local ou online apenas) ou que estão disponíveis para vários canais (local e online). |

## A visualização [!UICONTROL Product Groups]

A exibição [!UICONTROL Product Groups] em [!UICONTROL Assets] > [!UICONTROL Shopping] lista todos os grupos de produtos na exibição filtrada para a conta de anunciante selecionada. Você também pode criar e gerenciar grupos de produtos.

### Ações disponíveis <!-- Go through all -->

* [Criar um grupo de produtos [!UICONTROL All Products]](#product-group-create-all-products)

* [Criar um nó filho de grupo de produtos em um grupo de produtos existente](#node-add)

* Editar configurações de um nó de grupo de produtos:

  * [Editar quaisquer configurações](#node-edit)

  * [Editar somente o [!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [Editar somente o [!UICONTROL Max CPC]](#node-edit-maxcpc)

* [Excluir um nó do grupo de produtos](#node-delete)

* [Atribuir restrições](#constraint-assign) a grupos de produtos e [remover restrições](#constraint-unassign) de grupos de produtos

* [Atribuir classificações de etiquetas](#classification-values-assign) a grupos de produtos e [remover classificações de etiquetas](#classification-values-remove) de grupos de produtos

>[!NOTE]
>
>Você pode criar e editar grandes quantidades de dados de grupos de produtos (incluindo rótulos e atribuições de restrições) ao mesmo tempo, carregando [arquivos de bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e postando-os na rede de publicidade.

## Criar um grupo de produtos [!UICONTROL All Products] {#product-group-create-all-products}

Antes de criar grupos de produtos com atributos específicos, primeiro você deve criar um grupo de produtos com tudo incluído chamado &quot;[!UICONTROL All Products]&quot;. Cada grupo de anúncios pode ter somente um grupo &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Para criar muitos componentes da conta de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Product Group]**.

1. Selecione a rede de publicidade, a conta, a campanha e o grupo de publicidade e clique em **[!UICONTROL Continue]**.

1. Especifique as [configurações do grupo de produtos do Google Ads](#google-ads-product-group-settings) ou as [configurações do grupo de produtos do Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Clique em **[!UICONTROL Review and Save]**.

1. Se necessário, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") e altere as [configurações de grupo de produtos do Google Ads](#google-ads-product-group-settings) ou as [configurações de grupo de produtos do Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Clique em **[!UICONTROL Create]**.

## Criar um nó filho de grupo de produtos em um grupo de produtos existente {#product-group-create-child}

Depois de criar pelo menos um grupo &quot;[!UICONTROL All Products]&quot; completo para um grupo de anúncios, você poderá criar nós de grupos de produtos secundários para subconjuntos de produtos a serem incluídos ou excluídos de ofertas, com um ou mais grupos de produtos direcionados ao mesmo atributo em cada nível (por exemplo, [!UICONTROL Brand]=Acme para um grupo de produtos e [!UICONTROL Brand]=AcmePlus para outro no mesmo nível). Você pode criar até sete níveis de nós de grupos de produtos secundários, sem incluir &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Você não pode criar um grupo de produtos filho para um grupo de produtos &quot;[!UICONTROL Everything Else]&quot;.

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Opcional) Para exibir um grupo de produtos e seus nós filhos do grupo de produtos no Modo de exibição em árvore, mantenha o cursor sobre o nome do grupo de produtos, clique em **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Mantenha o cursor sobre o nome do grupo de produtos e clique em **[!UICONTROL ...]>[!UICONTROL + Add Node]**.

1. Especifique as [configurações do grupo de produtos do Google Ads](#google-ads-product-group-settings) ou as [configurações do grupo de produtos do Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Clique em **[!UICONTROL Center]**.

## Editar configurações de um nó de grupo de produtos {#node-edit}

É possível editar o modelo de oferta e rastreamento para nós de grupo de produtos de unidade (grupos de produtos sem nós de grupo de produtos filho) incluídos em um grupo de publicidade. Você não pode editar nenhuma informação para grupos de produtos de unidade excluídos ou para nós de subdivisão incluídos ou excluídos, que são grupos de produtos com nós de grupo de produtos secundários.

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Opcional) Para exibir um grupo de produtos e seus nós filhos do grupo de produtos no Modo de exibição em árvore, mantenha o cursor sobre o nome do grupo de produtos, clique em **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Mantenha o cursor sobre o nome do grupo de produtos e clique em **[!UICONTROL ...]>[!UICONTROL + Edit Node]**.

1. Edite as [configurações do grupo de produtos do Google Ads](#google-ads-product-group-settings) ou as [configurações do grupo de produtos do Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Clique em **[!UICONTROL Update]**.

## Editar somente o [!UICONTROL Tracking Template] de um nó de grupo de produtos {#node-edit-tracking-template}

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenha o cursor sobre o nome do grupo de produtos e clique em **[!UICONTROL ...]>[!UICONTROL Tree View]** para exibir o grupo de produtos e seus nós filhos do grupo de produtos no Modo de Exibição de Árvore.

1. Na coluna **[!UICONTROL Tracking Template]**, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Altere o valor **[!UICONTROL Tracking Template]** e clique em **[!UICONTROL Save]**.

## Editar somente o [!UICONTROL Max CPC] de um nó de grupo de produtos {#node-edit-maxcpc}

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenha o cursor sobre o nome do grupo de produtos e clique em **[!UICONTROL ...]>[!UICONTROL Tree View]** para exibir o grupo de produtos e seus nós filhos do grupo de produtos no Modo de Exibição de Árvore.

1. Na coluna **[!UICONTROL Max CPC]**, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Altere o valor **[!UICONTROL Max CPC]** e clique em **[!UICONTROL Save]**.

## Excluir um nó do grupo de produtos {#node-delete}

Você pode excluir qualquer grupo de produtos, exceto um grupo &quot;Tudo mais&quot; quando outros grupos de produtos existem no mesmo nível, usado para determinar quais produtos na conta da central de atendimento são incluídos nos anúncios de compras do grupo de anúncios. A exclusão de um grupo de produtos exclui todos os grupos de produtos secundários.

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Mantenha o cursor sobre o nome do grupo de produtos e clique em **[!UICONTROL ...]>[!UICONTROL Tree View]** para exibir o grupo de produtos e seus nós filhos do grupo de produtos no Modo de Exibição de Árvore.

1. Clique na coluna **[!UICONTROL Status]** e selecione **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Atribuir uma restrição aos grupos de produtos selecionados {#constraint-assign}

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Marque a caixa de seleção ao lado de cada grupo de produtos ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

## Remover restrições dos grupos de produtos selecionados {#constraint-unassign}

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Marque a caixa de seleção ao lado de cada grupo de produtos do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Atribuir valores de classificação a grupos de produtos {#classification-values-assign}

>[!NOTE]
>
>Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Marque a caixa de seleção ao lado de cada grupo de produtos ao qual você atribuirá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Para cada valor de classificação aplicável, faça o seguinte:

   1. Na coluna **[!UICONTROL Classifications]**, especifique a classificação:

      * Para usar uma classificação existente, clique no nome da classificação para expandi-la.

      * Para criar uma classificação, clique em [!UICONTROL +] no cabeçalho da coluna. No campo de entrada, insira o nome da classificação e clique em ![Salvar](/help/search-social-commerce/assets/save-checkmark.png "Salvar") para salvar imediatamente a classificação. Para usar a nova classificação, clique no nome da classificação para expandi-la.

        O nome deve consistir em [caracteres ASCII 32-126](https://www.asciitable.com/), e o comprimento máximo é de 27 caracteres de byte único.

   1. Na coluna **[!UICONTROL Value Name]**, especifique o valor da classificação selecionada:

      * Para usar um valor existente, selecione o valor.

      * Para criar um valor, clique em [!UICONTROL +] no cabeçalho da coluna. No campo de entrada, insira o valor e clique em ![Salvar](/help/search-social-commerce/assets/save-checkmark.png "Salvar") para salvar imediatamente o valor e selecioná-lo por padrão.

        O comprimento máximo é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

1. Clique em **+[!UICONTROL Assign Now]**.

## Remover valores de classificação de etiquetas de grupos de produtos {#classification-values-remove}

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

1. No menu principal, clique em **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Marque a caixa de seleção ao lado de cada grupo de produtos do qual você removerá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## Configurações do grupo de produtos [!DNL Google Ads] {#google-ads-product-group-settings}

### Grupos de produtos &quot;Todos os produtos&quot;

**[!UICONTROL Network]:** (Somente novos grupos de produtos) A rede de anúncios.

**[!UICONTROL Account]:** (Somente novos grupos de produtos) O nome da conta da rede de publicidade.

**[!UICONTROL Campaign]:** (Somente novos grupos de produtos) A campanha.

**[!UICONTROL Ad Group]:** (Somente novos grupos de produtos) O grupo de anúncios.

**[!UICONTROL Condition]** ou **[!UICONTROL Condition Type]:** (Somente leitura) Todos os Produtos

**[!UICONTROL Condition Value]:** (Somente grupos de produtos existentes)  

**[!UICONTROL Bid]** ou **[!UICONTROL Max CPC]:** (Somente grupos de produtos incluídos) O CPC (custo máximo por clique), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

{{$include /help/_includes/tracking-template-google.md}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários. Nenhum parâmetro de acréscimo especificado para a conta ou campanha foi incluído. Nenhum parâmetro de acréscimo especificado para a conta ou campanha foi incluído.

### Todos os outros grupos de produtos

**[!UICONTROL Condition Type]** e **[!UICONTROL Condition Value]:** (Somente leitura para grupos de produtos existentes) As dimensões de produto a serem direcionadas. Para novos grupos de produtos, insira a dimensão pela qual direcionar produtos e o atributo de qualificação para a categoria de informações selecionada (como &quot;Acme&quot; quando você está direcionando por marca ou &quot;New&quot; quando você está direcionando por condição).

Depois de criar um grupo de produtos para dimensões de produto específicas (ou seja, não &quot;Todos os produtos&quot;), o Search, Social e Commerce cria automaticamente um grupo de produtos para &quot;Tudo mais&quot;.

Para obter uma lista de dimensões de produto disponíveis, consulte &quot;[Filtros de produto](#product-filters)&quot;. Sua lista de dimensões pode ser limitada com base na configuração [!UICONTROL Inventory Filter] da campanha.

**[!UICONTROL Excluded]:** (Opcional para novos grupos de produtos; somente leitura para grupos de produtos existentes) Exclui ofertas em anúncios para produtos correspondentes.

**[!UICONTROL Max CPC]:** (Somente grupos de produtos incluídos) O custo máximo por clique (CPC), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários.

## Configurações do grupo de produtos [!DNL Microsoft Advertising] {#microsoft-advertising-product-group-settings}

### Grupos de produtos &quot;Todos os produtos&quot;

**[!UICONTROL Network]:** (Somente novos grupos de produtos) A rede de anúncios.

**[!UICONTROL Account]:** (Somente novos grupos de produtos) O nome da conta da rede de publicidade.

**[!UICONTROL Campaign]:** (Somente novos grupos de produtos) A campanha.

**[!UICONTROL Ad Group]:** (Somente novos grupos de produtos) O grupo de anúncios.

**[!UICONTROL Condition]** ou **[!UICONTROL Condition Type]:** (Somente leitura) Todos os Produtos

**[!UICONTROL Condition Value]:** (Somente grupos de produtos existentes)  

**[!UICONTROL Bid]** ou **[!UICONTROL Max CPC]:** (Somente grupos de produtos incluídos) O CPC (custo máximo por clique), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

**[!UICONTROL Base URL]:** (Somente novos grupos de produtos) Não usado<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários.

### Todos os outros grupos de produtos

**[!UICONTROL Condition Type]** e **[!UICONTROL Condition Value]:** (Somente leitura para grupos de produtos existentes) As dimensões de produto a serem direcionadas. Para novos grupos de produtos, insira a dimensão pela qual direcionar produtos e o atributo de qualificação para a categoria de informações selecionada (como &quot;Acme&quot; quando você está direcionando por marca ou &quot;New&quot; quando você está direcionando por condição).

Depois de criar um grupo de produtos para dimensões de produto específicas (ou seja, não &quot;Todos os produtos&quot;), o Search, Social e Commerce cria automaticamente um grupo de produtos para &quot;Tudo mais&quot;.

Para obter uma lista de dimensões de produto disponíveis, consulte &quot;[Filtros de produto](#product-filters)&quot;. Sua lista de dimensões pode ser limitada com base na configuração [!UICONTROL Inventory Filter] da campanha.

**[!UICONTROL Excluded]:** (Opcional para novos grupos de produtos; somente leitura para grupos de produtos existentes) Exclui ofertas em anúncios para produtos correspondentes.

**[!UICONTROL Max CPC]:** (Somente grupos de produtos incluídos) O custo máximo por clique (CPC), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários.

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implementar [!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [O [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
