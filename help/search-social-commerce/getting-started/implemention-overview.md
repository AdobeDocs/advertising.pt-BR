---
title: Visão geral da implementação do Search, Social e Commerce
description: Saiba mais sobre o fluxo de trabalho geral para iniciar e manter um portfólio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# Visão geral da implementação do Search, Social e Commerce

[!DNL Adobe] ou uma de suas agências afiliadas trabalha com cada anunciante para iniciar seus portfólios de publicidade online e rastrear quaisquer campanhas de publicidade adicionais. Após o lançamento inicial, as tarefas contínuas adicionais garantem que as metas do anunciante continuem a ser atingidas.

Este é o fluxo de trabalho geral para implementar e usar o Search, Social e Commerce.

## Lançamento inicial

[!DNL Adobe] e/ou sua agência trabalham com você e fazem o seguinte:

1. Avalie suas metas comerciais de alto nível e elabore estratégias para atingi-las:

   1. Identifique seu modelo de negócios e objetivos de marketing.

   1. Identifique os requisitos de rastreamento de conversão

   1. Analise suas estruturas de conta de anúncios online existentes.

   1. Identifique métricas para otimização e relatórios de portfólio.

1. (Usuários administradores ou gerentes de contas) Configurar contas administrativas:

   1. Configure a conta do anunciante. Se uma agência gerencia os dados do anunciante, a conta dele deve ser associada à conta da agência.

   1. (Se necessário) Crie contas de usuário para o anunciante exibir e gerenciar seus dados de campanha e gerar relatórios.

   Trabalhe com o administrador para configurar o acesso usando o Adobe Admin Console e os perfis de produto apropriados. Consulte &quot;[Administração de usuários para Pesquisa, Social e Commerce](/help/search-social-commerce/user-administration.md).&quot;

1. Sincronize com ou crie campanhas para cada uma das contas da rede de anúncios:

   * Para contas conectadas à API, [crie os detalhes da conta](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account) em [!UICONTROL Manage] > [!UICONTROL Accounts], conclua a autenticação específica da rede, configure as opções de rastreamento e habilite a conta.

   * Para contas sem suporte à API, siga o fluxo de trabalho [carregamento de dados](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md) ou [conta somente de rastreamento](/help/search-social-commerce/manage/accounts/template-account-manage.md), conforme aplicável. Essas contas não são sincronizadas com a rede de anúncios ou com a otimização do portfólio de suporte.

   * Se as contas ainda não tiverem dados de campanha, adicione campanhas, grupos de anúncios, palavras-chave, anúncios e posicionamentos no Search, Social e Commerce ou na rede de anúncios.

     Para obter a lista de verificação de configuração detalhada, consulte &quot;[Configurar contas e campanhas de rede de publicidade](campaign-implementation-overview.md)&quot;. Para os tipos de campanha com suporte, use [!UICONTROL Manage] > [!UICONTROL Campaigns] para [criar e gerenciar campanhas](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Configure o rastreamento de todos os anúncios para os quais você deseja que o Adobe Advertising rastreie conversões:

   1. (Se necessário) [Configure o rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) para anúncios e, opcionalmente, para palavras-chave, [!DNL Google Ads] inserções e [!DNL Google Ads] extensões, gerando e carregando URLs de rastreamento de cliques.

      As URLs de rastreamento de cliques para anunciantes com o serviço de rastreamento de conversão baseado em pixel da Adobe Advertising incluem um redirecionamento para os servidores [!DNL Adobe].

   1. [Configurar o controle de conversão](/help/search-social-commerce/tracking/conversion-tracking-about.md). Dependendo da implementação, pode envolver a adição de tags de rastreamento de conversão às páginas da Web apropriadas e/ou a configuração de uma queda diária de feed para os dados de conversão coletados usando seu próprio método. Você pode [gerar tags de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) de [!UICONTROL Goals] > [!UICONTROL Conversions].

      Para obter mais informações, consulte &quot;[Sobre rastreamento para Pesquisa, Social e Commerce](/help/search-social-commerce/tracking/tracking-about.md)&quot;.

1. Configurar integrações com produtos adicionais:

   1. (Anunciantes com o Adobe Analytics e/ou Adobe Audience Manager) Configure integrações entre as várias contas para que o Adobe Advertising possa trocar dados com elas.

      Consulte o guia em &quot;[Integrações com o CX Enterprise](/help/integrations/home.md)&quot;.

   1. (Anunciantes com [!DNL Google Analytics]) Sincronizam métricas de conversão para uma conta, propriedade e combinação de exibição [!DNL Google Analytics] para otimização e relatórios.

      Essa configuração usa a interface do usuário herdada. Consulte &quot;[Sobre sincronização [!DNL Google Analytics] métricas de conversão](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)&quot; e, quando necessário, [alternar para a interface herdada](ui-switch.md).

1. (Opcional) Configure e inicie portfólios:

   1. Em [!UICONTROL Goals] > [!UICONTROL Conversions], [revise as métricas de conversão e torne visíveis as métricas necessárias](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). Em [!UICONTROL Goals] > [!UICONTROL Objectives], [crie ou selecione um objetivo](/help/search-social-commerce/goals/objectives/objective-about.md) para otimização.

   1. Em [!UICONTROL Manage] > [!UICONTROL Portfolios], [crie portfólios](/help/search-social-commerce/manage/portfolios/portfolio-create.md) configurados para atingir seu objetivo e suas metas comerciais, com as [campanhas qualificadas](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) apropriadas. [Ative os portfólios](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para coletar e modelar dados. A equipe de implementação reúne e valida os dados de cliques e receita por pelo menos 14 dias e valida as configurações do portfólio.

      >[!NOTE]
      >
      >Search, Social e Commerce ainda rastreia e relata dados de campanhas que não são atribuídas a portfólios, mas não fornece otimização para eles.

   1. Depois que dados suficientes estiverem disponíveis para criar uma linha de base, a equipe poderá [alterar o status do portfólio para otimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), permitindo que o Search, Social e Commerce otimize ofertas, orçamentos e/ou metas de estratégia de oferta para o portfólio, com base no tipo de portfólio e nas estratégias de oferta de campanha.

   Consulte &quot;[Sobre portfólios](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot; para obter suporte à otimização e status do portfólio.

1. Monitore o desempenho de seus portfólios:

   1. Use [!UICONTROL Dashboard] > [!UICONTROL Overview] para [analisar tendências do portfólio](/help/search-social-commerce/dashboard/dashboard-overview.md) e [exibir detalhes de desempenho do portfólio](/help/search-social-commerce/manage/portfolios/portfolio-details.md) para investigar os resultados e a precisão do modelo.

   1. [Configurar alertas personalizados](/help/search-social-commerce/common-tasks/alerts-manage.md) e [gerar relatórios personalizados](/help/search-social-commerce/reports/management/report-manage.md) para monitoramento de desempenho. Quando necessário, automatize os relatórios usando os [modelos de relatório](/help/search-social-commerce/reports/report-templates-manage.md) e os [feeds de planilha](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Para obter mais informações, consulte &quot;[Monitorar o desempenho da campanha e do portfólio](/help/search-social-commerce/manage/manage-about.md#monitor-performance)&quot;.

1. (Opcional) Configure suas [visualizações de dados de desempenho](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) para mostrar os dados que você deseja ver.

## Tarefas em andamento

Após a primeira inicialização, as seguintes tarefas contínuas serão necessárias. Dependendo das suas condições de contrato, [!DNL Adobe], uma agência afiliada ou o anunciante realiza estas tarefas:

* Continue a monitorar e analisar o desempenho de cada portfólio visualizando alertas, dados de desempenho de cada portfólio e suas campanhas de componentes, relatórios personalizáveis e simulações (algumas funções).

* Ajuste as várias estratégias e configurações que você usa para gerenciar o conjunto de portfólios, conforme necessário, com base no desempenho real e previsto do portfólio e nas oportunidades de crescimento:

  * Ajuste orçamentos, objetivos e outras configurações do portfólio.

  * Ajuste as estruturas de conta/campanha para acomodar as alterações na estratégia de marketing.

  * Adicionar/pausar/excluir componentes da campanha. Isso pode incluir a expansão de conjuntos de palavras-chave com base na análise de termos de pesquisa e testes de páginas de aterrissagem e cópia de anúncios.

  * Atualizar estratégias de direcionamento geográfico e de site com base em relatórios de desempenho avançados.

  * (Opcional) Adicione restrições de licitação a palavras-chave de pesquisa individuais ou a todas as palavras-chave em um grupo de publicidade, campanha ou portfólio.

  * Adicione novos portfólios.

Para obter instruções sobre como monitorar campanhas e portfólios e ajustar suas configurações, consulte &quot;[Sobre o gerenciamento de campanhas e portfólios](/help/search-social-commerce/manage/manage-about.md)&quot; e &quot;[Editar detalhes do portfólio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md).&quot;
