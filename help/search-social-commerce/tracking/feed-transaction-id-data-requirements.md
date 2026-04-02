---
title: Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação
description: Faça referência aos requisitos de dados para feeds de dados usando uma ID de transação.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 0%

---

# Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação

A seguir estão os campos de cabeçalho e os campos de dados correspondentes necessários para cada tipo de arquivo de feed.

>[!NOTE]
>* Os cabeçalhos podem estar em qualquer ordem, desde que os dados nas linhas subsequentes sigam a mesma ordem. Se você não incluir um cabeçalho, a ordem das linhas de dados deverá ser consistente com cada arquivo de feed.
>* Cada linha do arquivo de feed deve conter dados para uma transação, e a transação deve ser identificada por uma ID de transação.

| Campo de cabeçalho/Nome da coluna | Tipo | Descrição |
| ---- | ---- | ---- |
| ID da transação (ev_transid) | String que diferencia maiúsculas de minúsculas | O identificador gerado pelo anunciante associado à transação. Como a tag de rastreamento de conversão do Adobe Advertising é usada para as partes online da transação, ela deve ser a mesma que a ID da transação (ev_transid) fornecida pela Adobe Advertising para a parte anterior da transação. Isso significa que a tag de conversão para a parte online da transação deve incluir uma métrica de conversão para uma ID de transação exclusiva.<br><br>**Observação:** o Adobe Advertising usa a ID para localizar os dados de transação antigos e atualizá-los de acordo com um modo de inserção acordado (por exemplo, para substituir os dados existentes ou aumentá-los com os novos dados). |
| Data da transação | DateTime | A data da transação. O formato deve ser consistente para cada transação. |
| Conversão específica do cliente | String | Uma conversão que está sendo rastreada (como tipo ou valor de transação). Discussões sobre as conversões a serem incluídas na equipe de implementação do Adobe Advertising antes de iniciar o feed. |

## Exemplo

O arquivo de exemplo a seguir inclui dados para duas métricas de conversão (Produto e Receita).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Rastreamento de conversão usando o feed de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md)
