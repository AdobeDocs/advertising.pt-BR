---
title: Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação
description: Faça referência aos requisitos de dados para feeds de dados usando uma ID de transação.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação

A seguir estão os campos de cabeçalho e os campos de dados correspondentes necessários para cada tipo de arquivo de feed.

>[!NOTE]
>* Os cabeçalhos podem estar em qualquer ordem, desde que os dados nas linhas subsequentes sigam a mesma ordem. Se você não incluir um cabeçalho, a ordem das linhas de dados deverá ser consistente com cada arquivo de feed.
>* Cada linha do arquivo de feed deve conter dados para uma transação, e a transação deve ser identificada por uma ID de transação.

| Campo de cabeçalho/Nome da coluna | Tipo | Descrição |
| ---- | ---- | ---- |
| ID da transação (ev_transid) | String que diferencia maiúsculas de minúsculas | O identificador gerado pelo anunciante associado à transação. Como a tag de rastreamento de conversão de Adobe Advertising é usada para as partes online da transação, ela deve ser a mesma que a ID da transação (ev_transid) que o Adobe Advertising forneceu para a parte anterior da transação. Isso significa que a tag de conversão para a parte online da transação deve incluir uma métrica de conversão para uma ID de transação exclusiva.<br><br>**Observação:** o Adobe Advertising usa a ID para localizar os dados de transação antigos e atualizá-los de acordo com um modo de inserção acordado (por exemplo, para substituir os dados existentes ou aumentá-los com os novos dados). |
| Data da transação | DateTime | A data da transação. O formato deve ser consistente para cada transação. |
| Conversão específica do cliente | String | Uma conversão que está sendo rastreada (como tipo ou valor de transação). Discuta as conversões a serem incluídas com a equipe de implementação do Adobe Advertising antes de iniciar o feed. |

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
