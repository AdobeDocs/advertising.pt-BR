---
title: Sobre a sincronização de  [!DNL Google Analytics] métricas de conversão
description: Saiba mais sobre como sincronizar  [!DNL Google Analytics] métricas de conversão para otimização e relatórios.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Sobre a sincronização de [!DNL Google Analytics] métricas de conversão

A Search, o Social e o Commerce podem sincronizar métricas de conversão de uma conta, propriedade e combinação de exibição específica do [!DNL Google Analytics] para otimização e relatórios. [Exibições de página](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessões](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Taxa de Rejeição](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculada como rejeições/sessões) e [Duração da Sessão](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) são incluídas automaticamente. É possível incluir até 16 métricas adicionais por fonte de dados.

>[!NOTE]
>
>Os usuários do Advertising DSP podem usar as métricas de conversão como metas personalizadas e em relatórios.

Todo o uso da API para transferências de dados é avaliado para um projeto na conta [!DNL Google Analytics] aplicável. Você pode exibir suas cotas para este projeto em [the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulte [!DNL Google Analytics] documentação para obter mais informações sobre [cotas e limites de chamada para solicitações de API de relatórios](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

As etapas a seguir descrevem o processo de sincronização dos dados de conversão de [!DNL Google Analytics].

1. [Execute as tarefas de pré-requisito](data-source-prerequisites.md)

   * Implemente um token Adobe Advertising (`ef_id` parâmetro da sequência de consulta) nas URLs da página de aterrissagem para todas as contas de publicidade aplicáveis.

   * Capture o token Adobe Advertising (`ef_id` parâmetro da cadeia de caracteres de consulta) em um [!DNL Custom Dimension] em [!DNL Google Analytics].

1. (Somente para usuários administradores de contas de agências, gerentes de contas de agências, [!DNL Adobe] gerentes de contas e administradores) [Crie uma fonte de dados por [!DNL Google Analytics] combinação de contas, propriedades e exibições](data-source-configure.md).

   Para integrar métricas de várias propriedades ou de várias exibições de uma única propriedade, configure uma fonte de dados separada para cada uma.

   Depois que uma fonte de dados é configurada, o Search, Social e Commerce extrai dados diariamente, começando às 05:00 no fuso horário do anunciante. Quando as métricas estiverem disponíveis, você poderá incluí-las nas exibições de gerenciamento de campanhas e portfólios e nos relatórios, e usá-las nos objetivos de otimização, conforme necessário.

>[!MORELIKETHIS]
>
>* [Pré-requisitos para configurar uma [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar uma  [!DNL Google Analytics] exibição como fonte de dados](data-source-configure.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar uma [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
