---
title: Disponível [!DNL Google Analytics] métricas
description: Referencie a [!DNL Google Analytics] métricas disponíveis para fontes de dados.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Apêndice - Disponível [!DNL Google Analytics] métricas

As seguintes métricas, exceto as exclusões anotadas, estão disponíveis quando são ativadas na implementação do cliente no [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categoria | Excluído | Comentários |
| ---- | ---- | ---- |
| \[Todos\] | Métricas com um tipo de dados de &quot;PERCENTUAL&quot; | As métricas apresentadas como uma porcentagem são sempre excluídas. |
| Usuário | ga:1diaUsuários, ga:7diaUsuários, ga:14diaUsuários, ga:28diaUsuários, ga:sessõesPorUsuário | — |
| Session | ga:uniqueDimensionCombinations | — |
| Conversões de metas | — | — |
| Rastreamento de página | ga:entradas, ga:horaNaPágina, ga:saídas | — |
| Pesquisa interna | — | Os nomes amigáveis de todas as métricas da Pesquisa interna são anexados ao valor &quot;Pesquisa interna: &quot; |
| Rastreamento de eventos | — | — |
| Comércio eletrônico | — | — |
| Interações sociais | — | — |
| Exceções | — | — |
| Variáveis ou colunas personalizadas | ga:calcMetric_* | As métricas calculadas são sempre excluídas. |

>[!MORELIKETHIS]
>
>* [Sobre sincronização [!DNL Google Analytics] métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar um [!DNL Google Analytics] exibir como fonte de dados](data-source-configure.md)
>* [Editar um [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar um [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
