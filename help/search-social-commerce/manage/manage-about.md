---
title: Sobre o gerenciamento de campanhas e portfólios
description: Saiba como as contas de publicidade, campanhas, rastreamento e otimização de portfólio funcionam juntas e como monitorar e melhorar o desempenho.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# Sobre o gerenciamento de campanhas e portfólios

*recurso do Beta*

O Search, Social e Commerce reúne gerenciamento de campanhas, relatórios de desempenho e otimização de portfólio em uma interface. Dependendo da rede de publicidade e do tipo de campanha, você pode sincronizar dados de campanha, criar e editar componentes da campanha, rastrear conversões e otimizar ofertas, orçamentos ou metas de estratégia de oferta. Consulte o [inventário com suporte](/help/search-social-commerce/introduction/supported-inventory.md) para obter a funcionalidade disponível para cada rede de publicidade.

O menu [!UICONTROL Manage] fornece acesso a suas contas, campanhas, grupos de anúncios, anúncios, palavras-chave, grupos de produtos e portfólios. Suas permissões determinam quais exibições e ações estão disponíveis. Para obter a organização completa do menu, consulte &quot;[Como a interface do usuário está organizada](/help/search-social-commerce/getting-started/user-interface.md)&quot;.

## Como contas, campanhas e portfólios se encaixam

* **Adicionar contas de rede** conecte os dados do anunciante à Pesquisa, ao Social e à Commerce. [Os tipos de conta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) incluem contas sincronizadas por meio de uma conexão de API, contas para as quais você carrega dados e contas somente de rastreamento baseadas em modelo. O tipo de conta determina se você pode sincronizar dados, gerenciar campanhas ou usar otimização de portfólio.

* **Campanhas** contêm os anúncios e outros componentes usados para entregar seus anúncios. Para os tipos de campanha com suporte, você pode [criar e gerenciar campanhas](/help/search-social-commerce/manage/campaigns/campaign-manage.md) e seus componentes nas [!UICONTROL Manage] exibições. Você também pode usar [bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) para operações em massa com suporte.

* **Portfólios** agrupam campanhas qualificadas para otimizá-las em direção a um objetivo comercial comum e a um objetivo de orçamento ou desempenho. Uma campanha pode pertencer a apenas um portfólio e todas as campanhas em um portfólio devem usar a mesma moeda. Consulte &quot;[Sobre portfólios](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot;.

A atribuição do Portfolio é opcional. Você pode rastrear e criar relatórios sobre campanhas sem atribuí-las a um portfólio. Nem todas as redes de anúncios, tipos de campanha ou estratégias de ofertas oferecem suporte à otimização do portfólio.

## Sincronizar dados da campanha

Para contas conectadas por meio de uma API, o Search, o Social e o Commerce recupera a estrutura de campanha e os dados de desempenho compatíveis da rede de anúncios. As alterações feitas nos componentes de campanha compatíveis do Search, Social e Commerce são enviadas para a rede de anúncios.

Quando necessário, você pode [solicitar uma sincronização manual](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). Se uma conta parar de sincronizar, revise seu [status de autenticação e acesso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Contas de upload de dados e contas somente de rastreamento não são sincronizadas com a rede de anúncios. Siga o fluxo de trabalho para o [tipo de conta](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) para fornecer dados de campanha e desempenho.

## Configurar rastreamento e otimização

[O rastreamento](/help/search-social-commerce/tracking/tracking-about.md) conecta a atividade de campanha às conversões que são importantes para sua empresa. Dependendo da sua implementação, os dados de conversão podem vir de tags da Adobe Advertising, de uma integração do Adobe Analytics, de rastreamento de rede de anúncios ou de feeds de dados. Configure o rastreamento de cliques e o rastreamento de conversão conforme necessário para a implementação do e valide os dados antes de usá-los para otimização.

Em [!UICONTROL Goals] > [!UICONTROL Conversions], você pode [revisar as métricas de conversão rastreadas para o anunciante e controlar sua visibilidade](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Use as métricas apropriadas em seus [objetivos](/help/search-social-commerce/goals/objectives/objective-about.md).

Para habilitar a otimização de portfólio, [crie um portfólio](/help/search-social-commerce/manage/portfolios/portfolio-create.md), atribua um objetivo e campanhas qualificadas e defina suas configurações de gastos e otimização. Um portfólio ativo coleta e modela os dados de desempenho. Quando os dados e as configurações estiverem prontos, [altere o status do portfólio para otimizado](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) para iniciar a otimização. As ações executadas dependem do tipo de portfólio e das [estratégias de oferta de campanha](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

Para obter a sequência de configuração detalhada, consulte &quot;[Configurar contas e campanhas de rede de publicidade](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)&quot;.

## Monitorar o desempenho da campanha e do portfólio {#monitor-performance}

A equipe da conta, a agência ou o anunciante é responsável por monitorar o desempenho e fazer ajustes, de acordo com os termos do contrato de serviço. Rotineiramente:

* Revise o desempenho da campanha e da conta nas [!UICONTROL Manage] exibições. [Personalize colunas, filtros e intervalos de datas](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) para se concentrar nas métricas e entidades importantes.

* Use [!UICONTROL Dashboard] > [!UICONTROL Overview] para [monitorar tendências de portfólio e alterações de desempenho](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Revise [alertas personalizados](/help/search-social-commerce/common-tasks/alerts-manage.md) para condições que exigem investigação.

* [Gerar relatórios](/help/search-social-commerce/reports/management/report-manage.md) para desempenho de campanha, palavra-chave, anúncio e portfólio. Para portfólios, [analise os detalhes de desempenho](/help/search-social-commerce/manage/portfolios/portfolio-details.md), incluindo o desempenho real e a precisão do modelo.

* Use [simulações](/help/search-social-commerce/plan/simulations/simulation-about.md), quando disponíveis, para avaliar os efeitos previstos de diferentes níveis de gastos.

* Investigue as diferenças entre as conversões e os dados de origem relatados. Consulte as orientações para [!DNL Google Ads] e [!DNL Microsoft Advertising] dados de conversão nos links relacionados.

## Ajustar campanhas e portfólios

Com base no desempenho e nas alterações em suas metas comerciais, talvez seja necessário:

* Edite configurações da campanha, crie ou pause componentes da campanha, refine conjuntos de palavras-chave ou teste anúncios diferentes. As ações disponíveis dependem da rede de anúncios e do tipo de campanha.

* Analise o direcionamento geográfico, de público-alvo e de posicionamento usando as exibições e os relatórios de gerenciamento relevantes.

* [Altere as atribuições de campanha](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) quando uma campanha precisar ser otimizada com um portfólio diferente. Atribuir uma campanha a outro portfólio a remove de seu portfólio anterior.

* [Edite as configurações do portfólio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md), incluindo o objetivo, a estratégia de gastos, as restrições ou os controles de otimização, conforme permitido pelo perfil do produto.

* Revise o [histórico de alterações](/help/search-social-commerce/reports/history-logs.md) ao investigar as alterações de desempenho.

>[!MORELIKETHIS]
>
>* [Configurar campanhas e contas de rede de publicidade](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Estoque com suporte](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
