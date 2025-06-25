---
title: Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha
description: Saiba como atribuir valores de classificação a componentes de conta.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha

Você pode atribuir e remover valores de classificação para as seguintes entidades de pesquisa das exibições de gerenciamento de campanhas: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo da pesquisa dinâmica. Se necessário, é possível criar classificações e valores de classificação durante o processo de atribuição. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncio para algumas redes de anúncios e tipos de campanha são [não mutáveis](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que editá-las excluirá a entidade existente e criará uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. Clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** e selecione a exibição de componente de conta.

1. Siga um destes procedimentos:

   * (Para atribuir valores a uma única entidade) Mantenha o cursor sobre o nome da entidade, clique em ![Botão Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Botão Menu") e selecione **[!UICONTROL Classification]**.

   * (Para atribuir valores a uma ou mais entidades) Faça o seguinte:

      * Marque a caixa de seleção ao lado de cada linha relevante.

        Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * Na barra de ferramentas acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e em **[!UICONTROL Classification]**.

1. Em [!UICONTROL Assignment Details], execute um dos procedimentos a seguir:

   * Para alterar quaisquer valores de classificações existentes para novos valores, selecione **[!UICONTROL Set To]**.

     O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

   * Para atribuir valores de classificação especificados sem remover valores existentes, selecione **[!UICONTROL Assign]**.

   * Para remover valores de classificação específicos atribuídos no momento, selecione **[!UICONTROL Remove]**.

     Ao remover um valor de classificação, os dados do relatório referentes ao valor não estarão mais disponíveis para os componentes de conta especificados.

   * Para excluir os valores de classificação especificados, selecione **[!UICONTROL Delete]**.

     A exclusão de um valor de classificação o torna indisponível para uso futuro e os dados de relatório não estão mais disponíveis para o valor. Todas as atribuições entre os valores e componentes de conta específicos são removidas, mas os componentes de conta não são excluídos.

1. Para cada valor de classificação aplicável, faça o seguinte:

   1. Na coluna **[!UICONTROL Classification]**, especifique o nome da classificação:

      * Para usar uma classificação existente, clique no nome da classificação para expandi-la.

      * Para criar uma classificação, clique em [!UICONTROL +]. No campo de entrada, insira o nome da classificação e clique em ![Salvar](/help/search-social-commerce/assets/select.png "Salvar") para salvar imediatamente a classificação.

        O nome deve consistir em [caracteres ASCII 32-126](https://www.asciitable.com/), e o comprimento máximo é de 27 caracteres de byte único.

   1. Na coluna **[!UICONTROL Value Name]**, especifique o nome do valor:

      * Para usar um valor existente, clique no nome do valor para selecioná-lo.

      * Para criar um valor, clique em [!UICONTROL +]. No campo de entrada, insira o valor e clique em ![Salvar](/help/search-social-commerce/assets/select.png "Salvar") para salvar imediatamente o valor.

        O comprimento máximo é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

1. (Opcional) Insira detalhes adicionais:

   1. Ao lado de **[!UICONTROL Additional Details]**, clique em ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para expandir os detalhes.

   1. Digite um **[!UICONTROL Project Name]** opcional e/ou **[!UICONTROL Description]** opcional.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre as classificações de rótulo](classification-about.md)
>* [Criar uma classificação de etiqueta](classification-create.md)
>* [Atribuir valores de classificação aos componentes da conta usando bulksheets](classification-values-assign-bulksheets.md)
>* [Remover os valores de classificação de etiquetas dos componentes da conta](classification-values-remove.md)
>* [Excluir valores de classificação de etiquetas](classification-values-delete.md)
>* [Excluir classificações de etiquetas](classification-delete.md)
