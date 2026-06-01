---
title: (Nova interface do usuário) Os dados usados para relatórios
description: Saiba mais sobre os diferentes tipos de dados disponíveis em visualizações de dados e relatórios personalizados.
feature: Search Reports
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: ff99aaef-142d-4c93-a88c-011e979e3843id: c916feea-e212-4773-b673-4daed287b8a3id: adcb1be7-7ed0-464d-a8d4-c905c9d47742id: fa0141e5-dc99-4fbd-9c0e-40aff66de606id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: 18f4c5afafd63a6ae9421bf80b4e5b5fd424ed86
workflow-type: tm+mt
source-wordcount: 604
ht-degree: 0%

---

# (Nova interface do usuário) Os dados usados para relatórios

O Search, Social e Commerce inclui um conjunto abrangente de relatórios de desempenho com base em dados de cliques e conversão. Você pode ver dados básicos de desempenho para os vários componentes de um portfólio ou conta publicitária das visualizações [!UICONTROL Portfolios] e [!UICONTROL Campaigns], bem como gerar vários relatórios básicos e avançados.

Os anunciantes que usam o serviço de rastreamento de conversão da Adobe Advertising também podem identificar o número de cliques para uma localização geográfica ou nome de domínio de um site de referência, como os anúncios em cada canal e os vários eventos que levam a uma conversão contribuem para o índice geral de conversão e a distribuição de conversões para uma única [métrica de conversão](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) por canal de marketing. Os relatórios disponíveis variam de acordo com o tipo de conta do usuário. A equipe de conta da Adobe tem acesso a todos os relatórios.

A maioria dos relatórios pode ser personalizada para exibir apenas as informações que você deseja ver. As seguintes métricas padrão estão disponíveis na maioria dos relatórios e são calculadas no nível do anúncio:

* **Métricas de desempenho padrão:**

   * **[!UICONTROL Impressions]:** O número total de vezes que o anúncio foi colocado.

   * **[!UICONTROL Clicks]:** O número total de vezes que um link foi clicado no anúncio.

   * **[!UICONTROL Cost]:** O custo total do anúncio. O custo da publicidade paga por clique (PPC) é sempre o número de cliques multiplicado pelo custo por clique.

   * **[!UICONTROL Cost per Click]:** O custo médio de um clique para um anúncio, que é o custo do anúncio dividido pelo número total de cliques no anúncio. Por exemplo, se você gastar US$ 100 para criar uma impressão de anúncio e o anúncio gerar 10 cliques, o custo por clique será de US$ 100/10=10 por clique.

   * **[!UICONTROL Average Position]:** (quando aplicável) a posição média de um anúncio que foi colocado, ponderada pelo número de impressões.

   * **[!UICONTROL Estimated Clicks]:** (Incluído nos relatórios avançados de anunciantes somente com o serviço de rastreamento de conversão da Adobe Advertising) O número total de cliques estimados para uma cidade ou nome de domínio de um site de referência. Isso pode incluir dados para redes de anúncios para as quais um anunciante não tenha uma conta publicitária.

* **Métricas de conversão:** o número total de conversões de cada métrica de conversão do anunciante ou dados de transação rastreados em direção a uma métrica de conversão. Isso pode incluir métricas de conversão e envolvimento do site, mas não métricas calculadas e métricas calculadas avançadas, que são sincronizadas do Adobe Analytics.

  Isso também pode incluir [[!DNL Google Ads] conversões rastreadas](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) e [[!DNL Google Analytics] conversões rastreadas](/help/search-social-commerce/admin/data-sources/data-source-about.md) que são sincronizadas para a conta do anunciante.

* **Métricas personalizadas:** suas próprias métricas, que você obtém criando fórmulas com base em métricas existentes (como o custo por pedido).

## Disponibilidade de dados

Ao gerar relatórios, você pode escolher como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Por exemplo, você pode optar por atribuir toda a conversão ao último evento ou pesar mais o último evento do que os outros. Por padrão, as conversões são atribuídas ao último evento.

Dependendo da regra de atribuição especificada para o relatório, os dados para cada tipo de relatório estarão disponíveis para as datas a seguir.

| Grupo de relatório | Relatório | Datas para as quais os dados estão disponíveis |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | A partir de 15 de maio de 2021.<br><br><b>Exceção:</b> Os dados de métricas de destaque estarão disponíveis a partir de 8 de setembro de 2022. |
| | Todos os outros [!UICONTROL Basic Reports] | Os 36 meses anteriores.<br><br><b>Exceção:</b> Os dados de métricas de destaque estão disponíveis a partir de 8 de setembro de 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Os 45 dias anteriores. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Os dois (2) meses anteriores mais o mês atual. |
| [!UICONTROL Assist Reports] | Todos | Os 18 meses anteriores. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | No ano anterior. |
| | [!UICONTROL Google Asset Group Performance Report] | Sem limitações |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Os últimos 180 dias. |
| | [!UICONTROL RSA Assets Report] | A partir de 10 de agosto de 2022. |
| | Todos os outros [!UICONTROL Specialty Reports] | Os dois (2) meses anteriores. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Os 18 meses anteriores. |
| [!UICONTROL Change History Report] | — | Os 31 dias anteriores. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios](report-about.md)
>* [Tarefas de configuração iniciais para relatórios](initial-setup.md)
