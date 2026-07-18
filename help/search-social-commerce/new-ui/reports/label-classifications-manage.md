---
title: Gerenciar classificações de etiquetas
description: Saiba mais sobre como usar as classificações de etiquetas para agrupar os componentes da conta.
feature: Search Label Classifications
source-git-commit: 44f83bcf32d671ad96a420827d16d8f1ec39049e
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 0%

---

# Gerenciar classificações de etiquetas

As classificações de etiquetas ajudam a agrupar os componentes da conta em conjuntos significativos. Por exemplo, você pode criar uma classificação de etiqueta principal chamada &quot;Geo&quot;, criar um valor de etiqueta diferente para cada região geográfica (como &quot;Reino Unido&quot; e &quot;Japão&quot;) dentro da classificação e, em seguida, atribuir os valores da etiqueta às suas [unidades de oferta](/help/search-social-commerce/glossary.md#a-b) ou campanhas principais. Em seguida, você pode incluir qualquer valor de rótulo como uma coluna separada em suas exibições e relatórios e criar uma tabela dinâmica de seus relatórios sobre diferentes grupos de classificação e valores.

## Componentes das classificações de etiquetas

### Classificações de rótulo

Cada anunciante pode ter até 30 classificações de rótulo, que são categorias de nível superior. Depois de criar uma classificação de rótulo, você pode criar valores de rótulo específicos para a classificação.

### Valores do rótulo

Cada classificação de etiqueta pode ter até 2000 valores. Depois de criar valores de rótulo específicos para uma classificação, você pode atribuí-los a campanhas, grupos de anúncios, palavras-chave, anúncios, posicionamentos e grupos de produtos [nas exibições de gerenciamento de campanhas](#classification-values-assign-campaign-management) ou [usando bulksheets](#classification-values-assign-bulksheets).

Cada entidade elegível pode ter valores de etiqueta para várias classificações, mas apenas um valor de etiqueta por classificação. Os valores de rótulo são herdados por entidades filhas, mas podem ser substituídos. O valor atribuído no nível mais baixo sempre substitui os valores atribuídos nos níveis pai.

## A exibição Classificações de etiquetas

A exibição [!UICONTROL Reports] > [!UICONTROL Labels Classifications] inclui subexibições [!UICONTROL Classifications] e [!UICONTROL Label Values]. Por padrão, são exibidos dados para suas classificações e valores de etiqueta em nível de palavra-chave, mas é possível exibir dados para classificações e valores em nível de anúncio.

## Ações disponíveis

* Exibir dados para suas classificações de etiquetas.

* Visualize os dados dos valores de classificação de etiqueta.

* [Criar uma classificação de etiqueta](#classification-create).

* Atribua valores de classificação aos componentes da conta [das exibições de gerenciamento de campanha](#classification-values-assign-campaign-management) ou [usando bulksheets](#classification-values-assign-bulksheets).

* [Remover os valores de classificação de etiquetas dos componentes da conta](#classification-values-remove).

* [Excluir valores de classificação de etiquetas](#classification-values-delete).

* [Excluir classificações de rótulo](#classification-delete).

## Criar uma classificação de etiqueta {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Clique em **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. No canto superior direito, clique em **[!UICONTROL Create Classification]**.

1. Insira um nome exclusivo para a classificação de etiquetas e clique em **[!UICONTROL Create]**.

   O nome deve ser exclusivo para a conta do anunciante e consiste em [caracteres ASCII 32-126](https://www.asciitable.com/), e o comprimento máximo é de 27 caracteres de byte único. O nome não pode ser idêntico ao nome de uma coluna de relatório existente ou de uma coluna de bulksheet existente. Veja os nomes das colunas de bulksheet para [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [LY Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Rede de exibição](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md) e [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha {#classification-values-assign-campaign-management}

Você pode atribuir e remover valores de classificação para as seguintes entidades de pesquisa das exibições de gerenciamento de campanhas: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo da pesquisa dinâmica. Se necessário, é possível criar classificações e valores de classificação durante o processo de atribuição. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncio para algumas redes de anúncios e tipos de campanha são [não mutáveis](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que editá-las excluirá a entidade existente e criará uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. Abra a exibição de entidade no menu **[!UICONTROL Manage]** ou **[!UICONTROL Target]**.

1. Marque a caixa de seleção ao lado de cada linha relevante.

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

## Atribuir valores de classificação aos componentes da conta usando bulksheets {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

Você pode associar classificações de etiquetas a valores das seguintes entidades de pesquisa usando bulksheets: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo de pesquisa dinâmica. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncio para algumas redes de anúncios e tipos de campanha são [não mutáveis](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que editá-las excluirá a entidade existente e criará uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. [Baixe uma bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md) que inclui as entidades às quais você deseja atribuir valores de classificação de etiquetas:

   * Na guia [!UICONTROL Rows and Columns], expanda a lista [!UICONTROL Campaign] no painel [!UICONTROL Bulksheet Columns].

   * Expanda a lista [!UICONTROL Label Classification].

   * Selecione cada classificação para a qual deseja incluir uma coluna no arquivo de bulksheet.

     Por exemplo, se você incluir as classificações de rótulo &quot;Cor&quot; e &quot;Geo&quot;, a planilha em massa incluirá as colunas &quot;Cor&quot; e &quot;Geo&quot;.

1. Abra o arquivo em um editor e adicione valores de etiquetas às colunas de classificação de etiquetas das entidades às quais elas serão associadas. O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

   Consulte os valores de exemplo na próxima seção.

   Além de adicionar valores, também é possível excluir valores existentes, removendo-os das linhas relevantes. Para remover valores de uma entidade pai e de suas entidades filho, a) inclua somente a linha de entidade pai e remova o valor de classificação existente ou b) inclua a entidade pai e suas entidades filho e remova o valor de classificação existente de todas as linhas pai e filho.

1. [Carregue o arquivo](/help/search-social-commerce/new-ui/set-up/bulksheets/upload.md) para criar as associações.

Os valores de etiqueta enviados estão visíveis nas visualizações de entidade relevantes.

### Exemplo de valores de classificação de etiquetas a serem carregados em bulksheets

Este exemplo inclui colunas para classificações de rótulo &quot;Cor&quot; e &quot;Geo&quot;. Para seus próprios bulksheets, substitua colunas por seus próprios nomes de classificação de etiqueta.

| Conta | Campaign | Grupo de publicidade | Palavra-chave | Anúncio | Posicionamento | Rótulos | Cor | Geo |
|---|---|---|---|---|---|---|---|---|
| Conta1 | C1 | | | | | | Verde | |
| Conta1 | C1 | AG1 | | | | | | |
| Conta1 | C1 | AG1 | K1 | | | | | Reino Unido |
| Conta1 | C1 | AG1 | K2 | | | | Vermelho | AU |
| Conta1 | C1 | AG1 | K3 | | | | Azul | DE |
| Conta1 | C1 | AG1 | | A1 | | | | |
| Conta1 | C1 | AG1 | | A1 | | | Vermelho | |
| Conta1 | C1 | AG1 | | | P1 | | Vermelho | AU |
| Conta1 | C1 | AG1 | | | P2 | | Azul | DE |

## Remover dos componentes da conta os valores de classificação de etiquetas {#classification-values-remove}

Remover um valor de classificação remove a associação com o componente de conta e todos os seus componentes secundários. Os dados do relatório para o valor de classificação não estão mais disponíveis para esses componentes. A remoção de um valor de classificação não exclui o valor nem os componentes da conta.

>[!NOTE]
>
>Para excluir um valor de uma classificação de etiqueta, consulte &quot;[Excluir valores de classificação de etiquetas](#classification-values-delete)&quot;.

1. Abra a exibição de entidade no menu **[!UICONTROL Manage]** ou **[!UICONTROL Target]**.

1. Marque a caixa de seleção ao lado de cada linha relevante.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Marque a caixa de seleção ao lado de cada valor de classificação a ser removido das entidades selecionadas.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Para selecionar todos os valores atribuídos, clique em **[!UICONTROL Select All]**. Para desmarcar todos os valores atribuídos, clique em **[!UICONTROL Deselect All]**.

1. Clique em **[!UICONTROL Unassign Selected]**.

## Excluir valores de classificação de etiqueta {#classification-values-delete}

A exclusão dos valores de classificação de etiqueta os torna indisponíveis para uso futuro e os dados de relatório não estão mais disponíveis para os valores. Todas as atribuições entre os valores e suas classificações de etiquetas principais e componentes de conta específicos são removidas, mas as classificações de etiquetas principais e os componentes da campanha não são excluídos.

>[!NOTE]
>
>Para simplesmente desassociar um valor de classificação de um componente da conta, consulte &quot;[Remover valores de classificação de etiquetas dos componentes da conta](#classification-values-remove)&quot;.

1. Clique em **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Clique na guia **[!UICONTROL Label Values]**.

1. (Opcional) Filtre a lista para incluir valores de rótulo específicos.

1. Marque a caixa de seleção ao lado de cada valor de rótulo a ser excluído.

   É possível excluir até 200 linhas por vez.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Excluir classificações de etiquetas

Excluir uma classificação remove todas as associações entre seus valores secundários e componentes de conta. Uma classificação excluída e seus valores não estarão disponíveis para uso futuro. Os dados do relatório para os valores de classificação estão mais disponíveis.

>[!NOTE]
>
>Para simplesmente desassociar um valor de classificação de um componente da conta, consulte &quot;[Remover valores de classificação de etiquetas dos componentes da conta](#classification-values-remove)&quot;.

1. Clique em **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. (Opcional) Filtre a lista para incluir classificações de rótulo específicas.

1. Marque a caixa de seleção ao lado de cada classificação de rótulo a ser excluída.

   É possível excluir até 200 linhas por vez.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.
