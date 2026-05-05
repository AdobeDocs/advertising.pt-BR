---
title: Gerencie as métricas de conversão de um anunciante no DSP.
description: Saiba como você pode usar as métricas de conversão que o Adobe Advertising rastreia para um anunciante do DSP.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Gerenciar as métricas de conversão de um anunciante

As métricas de conversão de um anunciante são usadas em todo o Adobe Advertising:

* No Advertising DSP, você pode incluir métricas de conversão em exibições de gerenciamento de campanha, objetivos personalizados e relatórios personalizados. Você também pode usar as métricas de conversão de um anunciante para criar [objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md), que são usados para otimizar pacotes.

* (Anunciantes com Advertising Search, Social e Commerce) Em Search, Social e Commerce, os dados das métricas de conversão podem ser exibidos em colunas nas exibições de campanha, portfólio e gerenciamento de objetivos e nos relatórios. Os usuários com privilégios de acesso suficientes também podem usar métricas de conversão para criar objetivos, que são usados para otimizar portfólios.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

Os tipos de métricas rastreadas para usuários do DSP incluem:

* Métricas de conversão que o Adobe Advertising rastreia para um anunciante.

* [Métricas de conversão e envolvimento do site sincronizadas do Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventos do site sincronizados do Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversões de feeds personalizados.

A partir da lista de métricas de conversão disponíveis, cada usuário com acesso aos dados do anunciante pode personalizar as métricas que vê disponíveis para exibições de gerenciamento e relatórios, incluindo ou omitindo métricas específicas à sua escolha. Você pode usar um nome de métrica exatamente como está escrito nos dados recuperados ou alterar o nome mostrado nos cabeçalhos da coluna para facilitar a leitura.

>[!IMPORTANT]
>
>Por padrão, nenhuma das métricas de conversão de um anunciante está disponível para inclusão em exibições de gerenciamento de campanha, objetivos personalizados e relatórios personalizados. Para disponibilizar uma métrica de conversão, você deve disponibilizá-la explicitamente.

>[!TIP]
>
>Quando o anunciante (ou a rede de anúncios) parar de coletar uma métrica de conversão, [oculte-a dos modos de exibição e relatórios de gerenciamento](#conversion-metrics-change-available), a menos que você queira usá-la para exibir dados históricos.

## Exibir as métricas de conversão rastreadas para um anunciante

* No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

Todas as métricas de conversão coletadas para o anunciante e todos os nomes de exibição diferentes atribuídos a ele são listados. Cada linha de métrica inclui a origem da métrica.

## Alterar o nome de exibição de uma métrica de conversão

Por exemplo, se você coletar dados de registro usando uma métrica de conversão chamada *reg*, poderá alterar o nome de exibição para vê-los exibidos como &quot;Registros&quot;.

Não é possível excluir um nome para exibição existente.

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

1. Mantenha o cursor sobre a linha e clique em **[!UICONTROL Edit Display Name]**.

1. Insira o nome que deve ser exibido e clique em **[!UICONTROL Save]**.

   Os nomes para exibição devem ser exclusivos e não podem incluir os seguintes caracteres especiais: `\"<'>&`

## Alterar as métricas de conversão disponíveis nas exibições de gerenciamento de campanhas, objetivos personalizados e relatórios personalizados {#change-the-conversion-metrics-available-in-ui}

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Conversions]**.

   Todas as métricas de conversão coletadas para o anunciante e todos os nomes diferentes especificados para exibição são listados.

1. (Opcional) Filtre a lista:

   1. Acima da lista, clique em ![Filtro](/help/dsp/assets/filter.png "Filtro").

   1. Especifique os filtros e clique em **[!DNL Apply]**.

      Você pode filtrar as métricas pela ID do cliente AMO, se as métricas estão visíveis ou ocultas na interface e por fonte de dados.

1. Altere as métricas de conversão disponíveis para exibições de gerenciamento e relatórios:

   * Para mostrar uma métrica, mantenha o cursor sobre a linha e clique em **[!UICONTROL Show in UI and Reports]**.

   * Para ocultar uma métrica, mantenha o cursor sobre a linha e clique em **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Gerenciar suas visualizações de dados de campanha](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Gerenciar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)
