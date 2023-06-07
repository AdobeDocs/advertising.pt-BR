---
title: Os dados usados para os relatórios
description: Saiba mais sobre os diferentes tipos de dados disponíveis em visualizações de dados e relatórios personalizados.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Os dados usados para os relatórios

O Search, Social e Commerce inclui um conjunto abrangente de relatórios de desempenho com base em dados de clique e conversão. Você pode exibir dados básicos de desempenho para os vários componentes de um portfólio ou conta de anúncio na [!UICONTROL Portfolios] e [!UICONTROL Campaigns] visualizações, bem como gerando vários relatórios básicos e avançados.

Os anunciantes que usam o serviço de rastreamento de conversão do Adobe Advertising também podem identificar o número de cliques para uma localização geográfica ou nome de domínio de um site de referência, como os anúncios em cada canal e os vários eventos que levam a uma conversão contribuem para o índice de conversão geral e a distribuição de conversões para um único site [propriedade de transação](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) por canal de marketing. Os relatórios disponíveis variam de acordo com o tipo de conta do usuário. A equipe da conta do Adobe tem acesso a todos os relatórios.

A maioria dos relatórios pode ser personalizada para exibir apenas as informações que você deseja ver. As seguintes métricas padrão estão disponíveis na maioria dos relatórios e são calculadas no nível do anúncio:

* **Métricas de desempenho padrão:**

   * **[!UICONTROL Impressions]:** O número total de vezes que o anúncio foi colocado.

   * **[!UICONTROL Clicks]:** O número total de vezes que um link foi clicado no anúncio.

   * **[!UICONTROL Cost]:** O custo total do anúncio. O custo da publicidade paga por clique (PPC) é sempre o número de cliques multiplicado pelo custo por clique.

   * **[!UICONTROL Cost per Click]:** O custo médio de um clique para um anúncio, que é o custo do anúncio dividido pelo número total de cliques do anúncio. Por exemplo, se você gastar US$ 100 para criar uma impressão de anúncio e o anúncio gerar 10 cliques, o custo por clique será de US$ 100/10=10 por clique.

   * **[!UICONTROL Average Position]:** (Quando aplicável) A posição média de um anúncio que foi colocado, ponderada pelo número de impressões.

   * **[!UICONTROL Estimated Clicks]:** (Incluído nos relatórios avançados para anunciantes somente com o serviço de rastreamento de conversão do Adobe Advertising) O número total de cliques estimados para uma cidade ou nome de domínio de um site de referência. Isso pode incluir dados para redes de anúncios para as quais um anunciante não tenha uma conta publicitária.

* **Métricas de conversão:** O número total de conversões de cada anúncio [propriedades da transação](/help/search-social-commerce/glossary.md#s-t)ou dados de transação rastreados para um tipo de conversão. Isso pode incluir métricas de conversão e envolvimento do site, mas não métricas calculadas e métricas calculadas avançadas, que são sincronizadas do Adobe Analytics.

   Isso também pode incluir [[!DNL Google Ads]Conversões rastreadas pelo](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) e [[!DNL Google Analytics]Conversões rastreadas pelo](/help/search-social-commerce/admin/data-sources/data-source-about.md) sincronizados para a conta do anunciante.

* **Métricas personalizadas:** Suas próprias métricas, que você obtém criando fórmulas com base em métricas existentes (como o custo por pedido).

## Disponibilidade de dados

Ao gerar relatórios, você pode escolher como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Por exemplo, você pode optar por atribuir toda a conversão ao último evento ou pesar mais o último evento do que os outros. Por padrão, as conversões são atribuídas ao último evento.

Dependendo da regra de atribuição especificada para o relatório, os dados para cada tipo de relatório estarão disponíveis para as datas a seguir.

| Grupo de relatório | Relatório | Datas para as quais os dados estão disponíveis |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | A partir de 15 de maio de 2021.<br><br><b>Exceção:</b> Os dados de métricas de destaque estarão disponíveis a partir de 8 de setembro de 2022. |
|  | Todos os outros [!UICONTROL Basic Reports] | Os 36 meses anteriores.<br><br><b>Exceção:</b> Os dados de métricas de destaque estarão disponíveis a partir de 8 de setembro de 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Os 45 dias anteriores. |
|  | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Os dois (2) meses anteriores mais o mês atual. |
| [!UICONTROL Assist Reports] | Todos | Os 18 meses anteriores. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | No ano anterior. |
|  | [!UICONTROL RSA Assets Report] | A partir de 10 de agosto de 2022. |
|  | Todos os outros [!UICONTROL Specialty Reports] | Os dois (2) meses anteriores. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Os 18 meses anteriores. |
| [!UICONTROL Change History Report] | — | Os 31 dias anteriores. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios](report-about.md)
>* [Tarefas de configuração inicial para relatórios](initial-setup.md)
