---
title: Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF
description: Referência aos requisitos em matéria de dados para os feeds de dados que utilizam IDs EF.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
TQID: https://experienceleague.adobe.com/p66X8xVlx-JwKjGgXxonJRRu78Q8F4109VkaIVtUbwU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 0%

---

# Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF

A seguir estão os campos de cabeçalho e os campos de dados correspondentes necessários para cada tipo de arquivo de feed.

>[!NOTE]
>* Os cabeçalhos podem estar em qualquer ordem, desde que os dados nas linhas subsequentes sigam a mesma ordem. Se você não incluir um cabeçalho, a ordem das linhas de dados deverá ser consistente com cada arquivo de feed.
>* Cada linha do arquivo de feed deve conter dados para uma transação, e a transação deve ser identificada por uma ef_id (token) gerada pela Adobe Advertising.

| Campo de cabeçalho/Nome da coluna | Tipo | Descrição |
| ---- | ---- | ---- |
| ID EF | String que diferencia maiúsculas de minúsculas | O ef_id (token) que você capturou após o clique para a transação, que consiste na ID do surfer, o tempo de clique e o tipo de rede. Não altere o valor. |
| ID da transação | String que diferencia maiúsculas de minúsculas | (Opcional, mas recomendado) A ID de transação gerada pelo anunciante. A prática recomendada é incluir isso para cada transação, mesmo que ef_id seja usado para rastrear a transação no momento do redirecionamento. |
| Data da transação | DateTime | A data da transação. O formato deve ser consistente para cada transação. |
| Conversão específica do cliente | String | Uma conversão que está sendo rastreada (como tipo ou valor de transação). Discussões sobre as conversões a serem incluídas na equipe de implementação do Adobe Advertising antes de iniciar o feed. |

## Exemplo

O arquivo de exemplo a seguir inclui dados para duas métricas de conversão (Produto e Receita).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Rastreamento de conversão usando um feed EF ID](/help/search-social-commerce/tracking/feed-efid.md)
