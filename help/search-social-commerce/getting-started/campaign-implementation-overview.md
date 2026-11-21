---
title: Configurar campanhas e contas de rede de publicidade
description: Siga o fluxo de trabalho de configuração para conexões de rede de anúncios, campanhas, rastreamento, métricas de conversão e otimização opcional do portfólio.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# Configurar campanhas e contas de rede de publicidade

*recurso do Beta*

O [!DNL Adobe] e sua agência trabalham com você para conectar suas contas de rede de publicidade, preparar campanhas, configurar o rastreamento e validar os dados de desempenho. Se você quiser que o Search, Social e Commerce otimizem campanhas qualificadas, o fluxo de trabalho também incluirá a configuração do portfólio.

Esta lista de verificação fornece os detalhes da conta e da campanha para o [fluxo de trabalho de implementação](implemention-overview.md) mais amplo. As tarefas que você pode executar dependem das suas permissões e da [funcionalidade com suporte para cada rede de publicidade e tipo de campanha](/help/search-social-commerce/introduction/supported-inventory.md).

## Configurar fluxo de trabalho

1. **Confirmar requisitos de acesso e conta.**

   Trabalhe com o administrador para confirmar o acesso ao anunciante apropriado e as permissões necessárias para suas tarefas. Consulte &quot;[Administração de usuários para Pesquisa, Social e Commerce](/help/search-social-commerce/user-administration.md).&quot;

   Se necessário, crie a conta real da rede de publicidade no site da rede de publicidade. Criar um registro de conta no Search, Social e Commerce não cria uma conta na rede de anúncios.

1. **Conecte ou registre cada conta de rede de publicidade.**

   Em [!UICONTROL Manage] > [!UICONTROL Accounts], use o fluxo de trabalho para o [tipo de conta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md):

   * **Conexão de API:** [Crie os detalhes da conta](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), conclua a autenticação específica da rede, configure as opções de rastreamento e habilite a conta. Verifique sua [autenticação e status de acesso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status); uma autenticação bem-sucedida não significa necessariamente que todas as permissões necessárias foram concedidas.

   * **Carregamento de dados:** [Crie os detalhes da conta e carregue dados de campanha e desempenho](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). Essas contas não são sincronizadas com a rede de anúncios ou com a otimização do portfólio de suporte.

   * **[!DNL Naver]somente rastreamento:** Siga o [fluxo de trabalho de conta somente rastreamento](/help/search-social-commerce/manage/accounts/template-account-manage.md). Use bulksheets para gerar URLs de rastreamento e aplicá-los no editor da rede de anúncios; a conta não sincroniza ou não oferece suporte à otimização do portfólio.

1. **Revisar ou criar estrutura de campanha.**

   Para contas conectadas à API, analise as campanhas sincronizadas e seus componentes. [Solicitar uma sincronização manual](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) quando necessário.

   Para os tipos de campanha com suporte, use [!UICONTROL Manage] > [!UICONTROL Campaigns] para [criar ou editar campanhas](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Crie os [grupos de anúncios](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [anúncios](/help/search-social-commerce/manage/ads/ad-manage.md) necessários e outros componentes com suporte. Você também pode usar [bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) para operações em massa com suporte.

   Conclua qualquer configuração específica da rede necessária antes de ativar as campanhas. Gerencie componentes não compatíveis na própria interface da rede de anúncios.

1. **Configure e valide o rastreamento antes de iniciar.**

   Selecione o [método de rastreamento de conversão](/help/search-social-commerce/tracking/conversion-tracking-about.md) que corresponde à sua implementação. Quando necessário, [gerar e aplicar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) e [gerar tags de rastreamento de conversão](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Configure todos os [integrações](/help/integrations/home.md) ou [feeds de conversão](/help/search-social-commerce/tracking/tracking-about.md) necessários e valide se as conversões podem ser atribuídas conforme esperado. Para campanhas somente de rastreamento, aplique os URLs de rastreamento gerados no editor da rede de publicidade.

1. **Revisar métricas de conversão.**

   Em [!UICONTROL Goals] > [!UICONTROL Conversions], [revise as métricas rastreadas e torne as métricas necessárias visíveis](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) para exibições de gerenciamento, relatórios e objetivos. Altere os nomes de exibição quando necessário para distinguir métricas.

1. **(Opcional) Preparar otimização de portfólio.**

   Confirme se as campanhas e suas estratégias de lance estão [qualificadas para otimização de portfólio](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Crie ou selecione um objetivo](/help/search-social-commerce/goals/objectives/objective-about.md) que use as métricas de conversão apropriadas. Em [!UICONTROL Manage] > [!UICONTROL Portfolios], [crie um portfólio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) ou [edite um portfólio existente](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) com o objetivo, a estratégia de gastos e as configurações de otimização necessárias.

   [Atribua as campanhas ao portfólio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Cada campanha pode pertencer a apenas um portfólio e todas as campanhas em um portfólio devem usar a mesma moeda.

1. **Valide os dados da campanha e estabeleça uma linha de base de desempenho.**

   Confirme se os dados de custo, clique e conversão estão disponíveis para cada campanha. Compare os dados de conversão com a origem apropriada, incluindo [!DNL Google Ads] e [!DNL Microsoft Advertising] quando aplicável. Use intervalos de datas consistentes e configurações de atribuição ao comparar relatórios.

   Para um novo portfólio, [ative-o](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para coletar e modelar dados. Valide as configurações de dados e portfólio antes de habilitar a otimização.

1. **(Opcional) Inicia a otimização do portfólio.**

   Quando o portfólio estiver pronto, [altere seu status para otimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), revisando os pré-requisitos e as mensagens de confirmação. O Search, Social e Commerce otimiza o portfólio de acordo com suas configurações e com as estratégias de oferta de campanha compatíveis.

1. **Configurar monitoramento e relatórios contínuos.**

   [Personalizar suas visualizações de dados](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [configurar alertas personalizados](/help/search-social-commerce/common-tasks/alerts-manage.md) e [gerar relatórios agendados](/help/search-social-commerce/reports/management/report-manage.md). Quando necessário, automatize os relatórios usando os [modelos de relatório](/help/search-social-commerce/reports/report-templates-manage.md) e os [feeds de planilha](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Continue a [monitorar e ajustar campanhas e portfólios](/help/search-social-commerce/manage/manage-about.md#monitor-performance) após a inicialização.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação do Search, Social e Commerce](implemention-overview.md)
>* [Sobre o gerenciamento de campanhas e portfólios](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
