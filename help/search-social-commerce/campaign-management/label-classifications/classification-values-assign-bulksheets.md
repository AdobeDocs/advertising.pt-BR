---
title: Atribuir valores de classificação aos componentes da conta usando bulksheets
description: Saiba como usar bulksheets para atribuir valores de classificação a componentes de conta.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# Atribuir valores de classificação aos componentes da conta usando bulksheets

Você pode associar classificações de etiquetas a valores das seguintes entidades de pesquisa usando bulksheets: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo de pesquisa dinâmica. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncios para algumas redes de anúncios e tipos de campanha são [não mutável](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que a edição exclui a entidade existente e cria uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. [Baixar uma bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) que inclui as entidades às quais você deseja atribuir valores de classificação de label:

   * No [!UICONTROL Rows and Columns] , expanda a [!UICONTROL Campaign] na lista [!UICONTROL Bulksheet Columns] painel.

   * Expanda a [!UICONTROL Label Classification] lista.

   * Selecione cada classificação para a qual deseja incluir uma coluna no arquivo de bulksheet.

      Por exemplo, se você incluir as classificações de rótulo &quot;Cor&quot; e &quot;Geo&quot;, a planilha em massa incluirá as colunas &quot;Cor&quot; e &quot;Geo&quot;.

1. Abra o arquivo em um editor e adicione valores de etiquetas às colunas de classificação de etiquetas das entidades às quais elas serão associadas. O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

   Consulte os valores de exemplo na próxima seção.

   Além de adicionar valores, também é possível excluir valores existentes, removendo-os das linhas relevantes. Para remover valores de uma entidade pai e de suas entidades filho, a) inclua somente a linha de entidade pai e remova o valor de classificação existente ou b) inclua a entidade pai e suas entidades filho e remova o valor de classificação existente de todas as linhas pai e filho.

1. [Fazer upload do arquivo](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) para criar as associações.

Os valores de etiqueta enviados estão visíveis nas visualizações de entidade relevantes.

## Exemplo de valores de classificação de etiquetas a serem carregados em bulksheets

Este exemplo inclui colunas para classificações de rótulo &quot;Cor&quot; e &quot;Geo&quot;. Para seus próprios bulksheets, substitua colunas por seus próprios nomes de classificação de etiqueta.

| Conta | Campaign | Grupo de publicidade | Palavra-chave | Anúncio | Posicionamento | Rótulos | Cor | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | Verde |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | Reino Unido |
| Acct1 | C1 | AG1 | K2 |  |  |  | Vermelho | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | Azul | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | Vermelho |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | Vermelho | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | Azul | DE |

>[!MORELIKETHIS]
>
>* [Sobre as classificações de rótulo](classification-about.md)
>* [Criar uma classificação de etiqueta](classification-create.md)
>* [Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha](classification-values-assign-campaign-management.md)
>* [Remover dos componentes da conta os valores de classificação de etiquetas](classification-values-remove.md)
>* [Excluir valores de classificação de etiqueta](classification-values-delete.md)
>* [Excluir classificações de etiquetas](classification-delete.md)

