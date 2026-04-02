---
title: Sobre a sincronização de  [!DNL Google Analytics] métricas de conversão
description: Saiba mais sobre como sincronizar  [!DNL Google Analytics] métricas de conversão para otimização e relatórios.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# Sobre a sincronização de [!DNL Google Analytics] métricas de conversão

A Search, o Social e o Commerce podem sincronizar métricas de conversão de uma conta, propriedade e combinação de exibição específica do [!DNL Google Analytics] para otimização e relatórios. [Exibições de página](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews), [Sessões](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions), [Taxa de Rejeição](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) (calculada como rejeições/sessões) e [Duração da Sessão](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration) são incluídas automaticamente. É possível incluir até 16 métricas adicionais por fonte de dados.

>[!NOTE]
>
>Os usuários do Advertising DSP podem usar as métricas de conversão como metas personalizadas e em relatórios.

Todo o uso da API para transferências de dados é avaliado para um projeto na conta [!DNL Google Analytics] aplicável. Você pode exibir suas cotas para este projeto em [the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulte [!DNL Google Analytics] documentação para obter mais informações sobre [cotas e limites de chamada para solicitações de API de relatórios](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

As etapas a seguir descrevem o processo de sincronização dos dados de conversão de [!DNL Google Analytics].

1. [Execute as tarefas de pré-requisito](data-source-prerequisites.md)

   * Implemente um token Adobe Advertising (parâmetro da sequência de consulta `ef_id`) nas URLs da página de aterrissagem para todas as contas de publicidade aplicáveis.

   * Capture o token do Adobe Advertising (`ef_id` parâmetro da cadeia de caracteres de consulta) em um [!DNL Custom Dimension] em [!DNL Google Analytics].

1. (Somente para usuários administradores de contas de agências, gerentes de contas de agências, [!DNL Adobe] gerentes de contas e administradores) [Crie uma fonte de dados por [!DNL Google Analytics] combinação de contas, propriedades e exibições](data-source-configure.md).

   Para integrar métricas de várias propriedades ou de várias exibições de uma única propriedade, configure uma fonte de dados separada para cada uma.

   Depois que uma fonte de dados é configurada, o Search, Social e Commerce extrai dados diariamente, a partir de 05:00 no fuso horário do anunciante. Quando as métricas estiverem disponíveis, você poderá incluí-las nas exibições de gerenciamento de campanhas e portfólios e nos relatórios, e usá-las nos objetivos de otimização, conforme necessário.

>[!MORELIKETHIS]
>
>* [Pré-requisitos para configurar uma [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar uma  [!DNL Google Analytics] exibição como fonte de dados](data-source-configure.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar uma [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
