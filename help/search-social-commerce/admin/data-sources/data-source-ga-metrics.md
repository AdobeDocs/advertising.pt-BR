---
title: Métricas [!DNL Google Analytics]  disponíveis
description: Referencie as  [!DNL Google Analytics]  métricas disponíveis para fontes de dados.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '131'
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
