---
title: Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha
description: Saiba como atribuir valores de classificação a componentes de conta.
exl-id: 7e55d7d8-5e12-409b-ad5d-c53cbf24c7c9
feature: Search Label Classifications
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha

Você pode atribuir e remover valores de classificação para as seguintes entidades de pesquisa das exibições de gerenciamento de campanhas: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo da pesquisa dinâmica. Se necessário, é possível criar classificações e valores de classificação durante o processo de atribuição. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncios para algumas redes de anúncios e tipos de campanha são [não mutável](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que a edição exclui a entidade existente e cria uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. Clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** e selecione a exibição de componente da conta.

1. Siga um destes procedimentos:

   * (Para atribuir valores a uma única entidade) Mantenha o cursor sobre o nome da entidade, clique em ![Botão Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Botão Menu")e selecione **[!UICONTROL Classification]**.

   * (Para atribuir valores a uma ou mais entidades) Faça o seguinte:

      * Marque a caixa de seleção ao lado de cada linha relevante.

        Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Na barra de ferramentas acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais")e clique em **[!UICONTROL Classification]**.

1. No [!UICONTROL Assignment Details], execute um dos procedimentos a seguir:

   * Para alterar quaisquer valores de classificações existentes para novos valores, selecione **[!UICONTROL Set To]**.

     O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

   * Para atribuir valores de classificação especificados sem remover valores existentes, selecione **[!UICONTROL Assign]**.

   * Para remover valores de classificação específicos atribuídos no momento, selecione **[!UICONTROL Remove]**.

     Ao remover um valor de classificação, os dados do relatório referentes ao valor não estarão mais disponíveis para os componentes de conta especificados.

   * Para excluir os valores de classificação especificados, selecione **[!UICONTROL Delete]**.

     A exclusão de um valor de classificação o torna indisponível para uso futuro e os dados de relatório não estão mais disponíveis para o valor. Todas as atribuições entre os valores e componentes de conta específicos são removidas, mas os componentes de conta não são excluídos.

1. Para cada valor de classificação aplicável, faça o seguinte:

   1. No **[!UICONTROL Classification]** especifique o nome da classificação:

      * Para usar uma classificação existente, clique no nome da classificação para expandi-la.

      * Para criar uma classificação, clique em [!UICONTROL +]. No campo de entrada, digite o nome da classificação e clique em ![Salvar](/help/search-social-commerce/assets/select.png "Salvar") para salvar imediatamente a classificação.

        O nome deve consistir em [Caracteres ASCII 32-126](https://www.asciitable.com/)e o comprimento máximo é de 27 caracteres de byte único.

   1. No **[!UICONTROL Value Name]** especifique o nome do valor:

      * Para usar um valor existente, clique no nome do valor para selecioná-lo.

      * Para criar um valor, clique em [!UICONTROL +]. No campo de entrada, insira o valor e clique em ![Salvar](/help/search-social-commerce/assets/select.png "Salvar") para salvar imediatamente o valor.

        O comprimento máximo é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

1. (Opcional) Insira detalhes adicionais:

   1. Ao lado de **[!UICONTROL Additional Details]**, clique em ![Abertura](/help/search-social-commerce/assets/chevron-up.png "Abertura") para expandir os detalhes.

   1. Insira um opcional **[!UICONTROL Project Name]** e/ou opcional **[!UICONTROL Description]**.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre as classificações de rótulo](classification-about.md)
>* [Criar uma classificação de etiqueta](classification-create.md)
>* [Atribuir valores de classificação aos componentes da conta usando bulksheets](classification-values-assign-bulksheets.md)
>* [Remover dos componentes da conta os valores de classificação de etiquetas](classification-values-remove.md)
>* [Excluir valores de classificação de etiqueta](classification-values-delete.md)
>* [Excluir classificações de etiquetas](classification-delete.md)
