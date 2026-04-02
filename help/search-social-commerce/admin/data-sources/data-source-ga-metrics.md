---
title: Métricas [!DNL Google Analytics]  disponíveis
description: Referencie as  [!DNL Google Analytics]  métricas disponíveis para fontes de dados.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2: id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# Apêndice - Métricas [!DNL Google Analytics] disponíveis

As seguintes métricas, com exceção das exclusões anotadas, estão disponíveis quando são habilitadas na implementação do cliente em [!DNL Google Analytics].

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categoria | Excluído | Comentários |
| ---- | ---- | ---- |
| \[Todos\] | Métricas com um tipo de dados de &quot;PERCENTUAL&quot; | As métricas apresentadas como uma porcentagem são sempre excluídas. |
| Usuário | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Session | ga:uniqueDimensionCombinations | — |
| Conversões de metas | — | — |
| Rastreamento de página | ga:entrances, ga:timeOnPage, ga:exits | — |
| Pesquisa interna | — | Os nomes amigáveis de todas as métricas da Pesquisa interna são anexados ao valor &quot;Pesquisa interna: &quot; |
| Rastreamento de eventos | — | — |
| Comércio eletrônico | — | — |
| Interações sociais | — | — |
| Exceções | — | — |
| Variáveis ou colunas personalizadas | ga :calcMetric_* | As métricas calculadas são sempre excluídas. |

>[!MORELIKETHIS]
>
>* [Sobre a sincronização [!DNL Google Analytics] de métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar uma [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar uma  [!DNL Google Analytics] exibição como fonte de dados](data-source-configure.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar uma [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
