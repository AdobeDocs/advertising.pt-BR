---
title: Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica
description: Saiba como criar e gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%
---
# Gerenciar [!DNL Google Ads] destinos de pesquisa dinâmica

*[!DNL Google Ads]somente contas*

Você pode criar, editar e alterar o status de destinos de pesquisa dinâmica para [!DNL Google Ads] campanhas que usam a rede de pesquisa.

## O que são destinos de pesquisa dinâmica?

Os destinos de pesquisa dinâmica definem se a rede de anúncios usa todas as páginas do site ou um subconjunto delas para direcionar seus anúncios de pesquisa dinâmica. Configure alvos de pesquisa dinâmica no nível do grupo de publicidade; eles se aplicam a todos os anúncios de pesquisa dinâmica no mesmo grupo de publicidade.

Dependendo das configurações da campanha, os destinos de pesquisa dinâmica podem ser obrigatórios ou opcionais:

* Você deve criar destinos de pesquisa dinâmica quando não especificar um domínio de site e idioma na seção &quot;[!UICONTROL DSA Options]&quot; da campanha.

* Opcionalmente, é possível criar destinos de pesquisa dinâmica ao especificar um domínio de site e idioma na seção &quot;[!UICONTROL DSA Options]&quot; da campanha.

  O [!DNL Google Ads] mostra automaticamente seus anúncios de pesquisa dinâmica com base no conteúdo de um site especificado com essas configurações.

Para melhor rastrear o desempenho, configure sua campanha com um grupo de anúncios por público alvo de pesquisa dinâmica e inclua um grupo de anúncios que segmente todos os critérios.

Para obter mais informações sobre [!DNL Google Ads] anúncios de pesquisa dinâmica, consulte https://support.google.com/google-ads/answer/2471185.

## A visualização [!UICONTROL Auto Targets] {#auto-target-view-about}

A exibição [!UICONTROL Targeting] > [!UICONTROL Auto Targets] lista todos os destinos de pesquisa dinâmica na exibição filtrada para a conta de anunciante selecionada. Você também pode gerenciar seus destinos de pesquisa dinâmica.

A visualização dos dados requer a permissão [!UICONTROL View Auto Targets]. Criar destinos e editar seus lances ou status requer a permissão [!UICONTROL Edit Auto Targets].

### Ações disponíveis

* [Criar um público alvo de pesquisa dinâmica](#auto-target-create)

* [Editar as configurações de destinos de pesquisa dinâmica](#auto-target-edit)

* [Alterar o status ou excluir alvos de pesquisa dinâmica](#auto-target-status)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

* [Atribuir restrições](#constraint-assign) aos destinos de pesquisa dinâmica e [remover restrições](#constraint-unassign) dos destinos de pesquisa dinâmica

* [Atribuir classificações de rótulo](#classification-values-assign) aos destinos de pesquisa dinâmica e [remover classificações de rótulo](#classification-values-remove) dos destinos de pesquisa dinâmica

>[!NOTE]
>
>Você pode criar e editar grandes quantidades de dados de destino (incluindo rótulos e atribuições de restrições) ao mesmo tempo, carregando [arquivos de bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e postando-os na rede de publicidade.

## Criar um destino de pesquisa dinâmica [!DNL Google Ads] {#auto-target-create}

Você pode criar destinos de pesquisa dinâmica para definir páginas em seus sites (ou seja, os domínios usados nos URLs de exibição de seus anúncios) cujo conteúdo é usado para direcionar seus anúncios de pesquisa dinâmica no mesmo grupo de anúncios.

É possível direcionar todas as páginas indexadas ou especificar até três critérios.

>[!NOTE]
>
>Para melhor monitorar o desempenho, crie um target com a opção [!UICONTROL All] para apenas um grupo de anúncios por campanha.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create Auto Target]**.

1. Em **[!UICONTROL Basic Settings]**, selecione a rede de publicidade, a conta, a campanha e o grupo de publicidade.

1. Especifique as [configurações de destino de pesquisa dinâmica](#auto-target-create-settings) restantes.

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as configurações. Para alterar qualquer configuração, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** na seção aplicável e altere as configurações.

1. Clique em **[!UICONTROL Create]**.

## Editar configurações de destino de pesquisa dinâmica [!DNL Google Ads] {#auto-target-edit}

É possível editar o status ou o lance máximo para um ou mais targets de pesquisa dinâmica. Você não pode alterar os critérios de destino.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada linha a ser editada.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. No painel **[!UICONTROL Edit Auto Targets]**, edite as [configurações de status e oferta](#auto-target-edit-settings).

   Suas alterações são aplicadas a todos os alvos selecionados. As configurações que você não alterar manterão seus valores existentes.

   Quando os destinos selecionados usam várias moedas, a edição de lances é desabilitada. Você ainda pode alterar o status deles.

1. Clique em **[!UICONTROL Save]**.

Você também pode editar a oferta de um único público alvo diretamente na tabela de dados clicando no valor da oferta.

## Alterar ou excluir o status de [!DNL Google Ads] destinos de pesquisa dinâmica {#auto-target-status}

Você pode pausar um público alvo de pesquisa dinâmica para parar de usá-lo em anúncios de pesquisa dinâmica no mesmo grupo de publicidade. Posteriormente, você poderá retomar o uso do target alterando seu status para ativo. Você também pode excluir destinos de pesquisa dinâmica.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. (Opcional) Filtre a lista para incluir destinos de pesquisa dinâmica específicos.

1. Siga um destes procedimentos:

   * Para alterar o status de um destino, clique em seu valor na coluna **[!UICONTROL Status]** e selecione **[!UICONTROL Active]** ou **[!UICONTROL Paused]**.

   * Para alterar o status de vários destinos, marque a caixa de seleção ao lado de cada destino, clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa, selecione **[!UICONTROL Status]** no painel **[!UICONTROL Edit Auto Targets]** e clique em **[!UICONTROL Save]**.

   * Para excluir um ou mais destinos, marque a caixa de seleção ao lado de cada destino, clique em **[!UICONTROL ...]>[!UICONTROL Delete]** na barra de ferramentas de ações em massa e, em seguida, clique em **[!UICONTROL Confirm]** na mensagem de confirmação.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Gerenciar atribuições de restrição para alvos de pesquisa dinâmica {#constraints}

### Atribuir uma restrição aos destinos de pesquisa dinâmica {#constraint-assign}

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica ao qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

### Remover restrições dos destinos de pesquisa dinâmica selecionados {#constraint-unassign}

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica do qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

## Gerenciar valores de classificação para destinos de pesquisa dinâmica {#classification-values}

### Atribuir valores de classificação aos destinos de pesquisa dinâmica {#classification-values-assign}

>[!NOTE]
>
>Os valores de rótulo são herdados por entidades secundárias, portanto, não insira valores para destinos de pesquisa dinâmica, a menos que você queira substituir os valores herdados.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica ao qual você atribuirá um valor de rótulo.

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

### Remover valores de classificação de etiquetas dos destinos de pesquisa dinâmica {#classification-values-remove}

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

1. No menu principal, clique em **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Marque a caixa de seleção ao lado de cada destino de pesquisa dinâmica do qual você removerá um valor de rótulo.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] configurações de destino de pesquisa dinâmica {#dynamic-search-target-settings}

### Configurações disponíveis durante a criação {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Direcionamentos automáticos:** as páginas indexadas cujo conteúdo é usado para direcionar os anúncios de pesquisa dinâmica no grupo de publicidade:

* *[!UICONTROL All]* (o padrão): segmenta todas as páginas indexadas.

* *[!UICONTROL Specific]:* Direciona páginas que correspondem a até três critérios. Selecione um critério e insira seu valor. Para adicionar outro critério, clique em **[!UICONTROL And]**. Os critérios são combinados com AND, portanto, uma página deve corresponder a todos os critérios especificados. Clique em **[!UICONTROL Reset]** para limpar os critérios.

  * *[!UICONTROL Category]:* A categoria de conteúdo [!DNL Google Ads] da página é igual ao valor especificado. Insira um valor.

  * *[!UICONTROL URL]:* A URL da página contém o valor especificado, como `shoes.example.com`. Insira um URL válido.

  * *[!UICONTROL Page Title]:* O título da página contém o texto especificado. Insira um valor.

  * *[!UICONTROL Page Content]:* O conteúdo da página contém o texto especificado. Insira um valor.

Você não pode alterar os critérios de destino após criar o destino.

**[!UICONTROL Status]:** O status do destino:

* *[!UICONTROL Active]* (padrão): habilita lances.

* *[!UICONTROL Paused]:* Desabilita a licitação.

**[!UICONTROL Bid]:** O CPC (custo máximo por clique) do destino. Esse valor substitui a oferta de nível de grupo de anúncios. O campo é opcional; quando você insere um lance, o valor mínimo é 0,01 na moeda da conta.

>[!NOTE]
>
>Se o target estiver em um portfólio otimizado, a oferta de CPC especificada será aplicada por um dia. Posteriormente, o recurso de otimização coloca ofertas de acordo com seus próprios cálculos.

### Configurações disponíveis durante a edição {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** Selecione **[!UICONTROL Active]** ou **[!UICONTROL Paused]**.

#### [!UICONTROL Bid details]

A edição de lances é desabilitada quando os alvos selecionados usam várias moedas.

**[!UICONTROL Bid adjustment]:** Como alterar o número máximo de lances:

* *[!UICONTROL Set to]:* Substitua cada oferta pelo valor em [!UICONTROL Set value].

* *[!UICONTROL Increase]:* Aumente cada oferta pelo valor ou porcentagem em [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* Diminua cada oferta pelo valor ou porcentagem em [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (Para [!UICONTROL Increase] e [!UICONTROL Decrease]) Selecione **[!UICONTROL Currency]** ou **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** O novo lance ou a quantidade ou porcentagem pela qual alterar cada lance. O valor mínimo é 0,01.

**[!UICONTROL Max limit]:** (Opcional; para [!UICONTROL Increase] e [!UICONTROL Decrease]) Um limite na moeda da conta. Para um aumento, este é o lance máximo resultante. Para uma diminuição, este é o lance mínimo resultante. Ao inserir um limite, o valor mínimo é 0,01.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Gerenciar restrições para unidades de oferta de pesquisa](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nova interface do usuário) Gerenciar classificações de rótulos](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
