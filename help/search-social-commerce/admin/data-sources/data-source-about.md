---
title: Sobre sincronização [!DNL Google Analytics] métricas de conversão
description: Saiba mais sobre sincronização [!DNL Google Analytics] métricas de conversão para otimização e relatórios.
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Sobre sincronização [!DNL Google Analytics] métricas de conversão

As soluções de Pesquisa, Social e Comércio podem sincronizar métricas de conversão de uma [!DNL Google Analytics] combinação de conta, propriedade e exibição para otimização e relatórios. [Exibições de página](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessões](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Taxa de rejeição](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculado como rejeições/sessões) e [Duração da sessão](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) são incluídos automaticamente. É possível incluir até 16 métricas adicionais por fonte de dados.

>[!NOTE]
>
>Os usuários de DSP de publicidade podem usar as métricas de conversão como metas personalizadas e em relatórios.

Todo o uso da API para as transferências de dados é avaliado para um projeto na [!DNL Google Analytics] conta. Você pode exibir suas cotas para este projeto em [o [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulte [!DNL Google Analytics] para obter mais informações sobre [cotas e limites de chamada para solicitações de API de relatórios](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

As etapas a seguir descrevem o processo de sincronização de dados de conversão do [!DNL Google Analytics].

1. [Execute as tarefas de pré-requisito](data-source-prerequisites.md)

   * Implementar um token de Adobe Advertising (`ef_id` parâmetro da string de consulta) nos URLs da página inicial para todas as contas publicitárias aplicáveis.

   * Capture o token de Adobe Advertising (`ef_id` sequência de consulta (parâmetro) em uma [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Administrador de conta da agência, gerente de conta da agência, [!DNL Adobe] gerente de conta e administrador (somente usuários) [Criar uma fonte de dados por [!DNL Google Analytics] combinação de conta, propriedade e visualização](data-source-configure.md).

   Para integrar métricas de várias propriedades ou de várias exibições de uma única propriedade, configure uma fonte de dados separada para cada uma.

   Depois que uma fonte de dados é configurada, o Search, Social e Commerce extrai dados diariamente, começando às 05:00 no fuso horário do anunciante. Quando as métricas estiverem disponíveis, você poderá incluí-las nas exibições de gerenciamento de campanhas e portfólios e nos relatórios, e usá-las nos objetivos de otimização, conforme necessário.

>[!MORELIKETHIS]
>
>* [Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar um [!DNL Google Analytics] exibir como fonte de dados](data-source-configure.md)
>* [Editar um [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar um [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
