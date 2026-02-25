---
title: Atribuir valores de classificação aos componentes da conta usando bulksheets
description: Saiba como usar bulksheets para atribuir valores de classificação a componentes de conta.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Atribuir valores de classificação aos componentes da conta usando bulksheets

Você pode associar classificações de etiquetas a valores das seguintes entidades de pesquisa usando bulksheets: campanha, grupo de anúncios, palavra-chave, anúncio, posicionamento, grupo de produtos no nível da unidade e público-alvo de pesquisa dinâmica. Cada classificação de etiqueta pode ter até 2000 valores.

Cada entidade pode ter um valor de rótulo por classificação. Por exemplo, Shoes_Campaign pode ter um valor de Cor de &quot;vermelho&quot; e um valor Geo de &quot;Los Angeles&quot;, mas não pode ter vários valores para Cor ou Geo.

Os valores de rótulo são herdados por entidades filhas, portanto, não insira valores para entidades filhas, a menos que deseje substituir os valores herdados.

>[!NOTE]
>
>Suas palavras-chave e cópia de anúncio para algumas redes de anúncios e tipos de campanha são [não mutáveis](/help/search-social-commerce/campaign-management/faqs-campaigns.md), o que significa que editá-las excluirá a entidade existente e criará uma nova. Quando uma entidade existente é excluída dessa maneira, a classificação de etiqueta não é atribuída à nova entidade.

1. [Baixe uma bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) que inclui as entidades às quais você deseja atribuir valores de classificação de etiquetas:

   * Na guia [!UICONTROL Rows and Columns], expanda a lista [!UICONTROL Campaign] no painel [!UICONTROL Bulksheet Columns].

   * Expanda a lista [!UICONTROL Label Classification].

   * Selecione cada classificação para a qual deseja incluir uma coluna no arquivo de bulksheet.

     Por exemplo, se você incluir as classificações de rótulo &quot;Cor&quot; e &quot;Geo&quot;, a planilha em massa incluirá as colunas &quot;Cor&quot; e &quot;Geo&quot;.

1. Abra o arquivo em um editor e adicione valores de etiquetas às colunas de classificação de etiquetas das entidades às quais elas serão associadas. O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

   Consulte os valores de exemplo na próxima seção.

   Além de adicionar valores, também é possível excluir valores existentes, removendo-os das linhas relevantes. Para remover valores de uma entidade pai e de suas entidades filho, a) inclua somente a linha de entidade pai e remova o valor de classificação existente ou b) inclua a entidade pai e suas entidades filho e remova o valor de classificação existente de todas as linhas pai e filho.

1. [Carregue o arquivo](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) para criar as associações.<!-- Update once the new bulksheet UI is GA -->

Os valores de etiqueta enviados estão visíveis nas visualizações de entidade relevantes.

## Exemplo de valores de classificação de etiquetas a serem carregados em bulksheets

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

>[!MORELIKETHIS]
>
>* [Sobre as classificações de rótulo](classification-about.md)
>* [Criar uma classificação de etiqueta](classification-create.md)
>* [Atribuir valores de classificação aos componentes da conta das exibições de gerenciamento de campanha](classification-values-assign-campaign-management.md)
>* [Remover os valores de classificação de etiquetas dos componentes da conta](classification-values-remove.md)
>* [Excluir valores de classificação de etiquetas](classification-values-delete.md)
>* [Excluir classificações de etiquetas](classification-delete.md)
