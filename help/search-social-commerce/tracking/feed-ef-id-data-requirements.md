---
title: Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF
description: Referência aos requisitos em matéria de dados para os feeds de dados que utilizam IDs EF.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF

A seguir estão os campos de cabeçalho e os campos de dados correspondentes necessários para cada tipo de arquivo de feed.

>[!NOTE]
>* Os cabeçalhos podem estar em qualquer ordem, desde que os dados nas linhas subsequentes sigam a mesma ordem. Se você não incluir um cabeçalho, a ordem das linhas de dados deverá ser consistente com cada arquivo de feed.
>* Cada linha do arquivo de feed deve conter dados para uma transação, e a transação deve ser identificada por um Adobe ef_id (token) gerado por publicidade.


| Campo de cabeçalho/Nome da coluna | Tipo | Descrição |
| ---- | ---- | ---- |
| ID EF | String que diferencia maiúsculas de minúsculas | O ef_id (token) que você capturou após o clique para a transação, que consiste na ID do surfer, o tempo de clique e o tipo de rede. Não altere o valor. |
| ID da transação | String que diferencia maiúsculas de minúsculas | (Opcional, mas recomendado) A ID de transação gerada pelo anunciante. A prática recomendada é incluir isso para cada transação, mesmo que ef_id seja usado para rastrear a transação no momento do redirecionamento. |
| Data da transação | DateTime | A data da transação. O formato deve ser consistente para cada transação. |
| Conversão específica do cliente | String | Uma conversão que está sendo rastreada (como tipo ou valor de transação). Discussões sobre as conversões a serem incluídas na equipe de implementação do Adobe Advertising antes de iniciar o feed. |

## Exemplo

O arquivo de exemplo a seguir inclui dados para duas propriedades de transação (Produto e Receita).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Rastreamento de conversão usando um feed de ID EF](/help/search-social-commerce/tracking/feed-efid.md)

