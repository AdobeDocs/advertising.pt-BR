---
title: '[!DNL Microsoft Advertising] dados de conversão'
description: Saiba mais sobre os tipos de dados de conversão rastreados por [!DNL Microsoft Advertising] disponíveis em Pesquisa, Social e Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
TQID: 'https://experienceleague.adobe.com/ZK-uDqw0sThnMzX6bdR-d33gh-AlLTaytJr1fS7pdgs'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] dados de conversão em Pesquisa, Social e Commerce

O Search, Social e Commerce sincroniza automaticamente todas as conversões rastreadas pelas suas [[!DNL Microsoft Advertising] tags de rastreamento universal de eventos (UET)](https://help.ads.microsoft.com/#apex/ads/en/53056) para conversões de site, incluindo conversões view-through, para relatórios e otimização.

Todas as métricas estão automaticamente disponíveis nas suas visualizações de gerenciamento de campanhas e relatórios básicos, e também estão disponíveis para uso nos objetivos do portfólio para otimização de campanhas do [!DNL Microsoft Advertising].

## Dados de conversão disponíveis

O Search, Social e Commerce sincroniza dados para conversões para as quais a opção &quot;[!DNL Include in 'Conversions']&quot; está habilitada, extraindo os dados dos últimos 35 dias e depois extraindo as alterações para os dados diariamente até 09:00-10:00 no fuso horário do anunciante. Os dados históricos podem mudar de dia para dia, à medida que novas conversões são rastreadas para cada clique.

Duas métricas para cada conversão [[!DNL Microsoft Advertising] rastreada](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que você configurou em [!DNL Microsoft Advertising]) estão automaticamente disponíveis em Pesquisa, Social e Commerce, usando os nomes de conversão configurados em [!DNL Microsoft Advertising]. As métricas para cada conversão incluem:

* `<conversion-name>` — O valor de conversão da palavra-chave (como Compra).

  >[!TIP]
  >
  >Use esse tipo de métrica de conversão no objetivo para portfólios que incluem [!DNL Microsoft Advertising] campanhas com o Valor máximo de conversão e estratégias de oferta de ROAS de destino.

* `CT_<conversion-name>` — O número (contagem) de conversões, começando com o prefixo &quot;CT_&quot; (como CT_Purchase).

  >[!TIP]
  >
  >Use esse tipo de métrica de conversão no objetivo para portfólios que incluem [!DNL Microsoft Advertising] campanhas com o número máximo de conversões e estratégias de oferta de CPA do Target.

Os dados são disponibilizados com base na hora do clique e no horário da conversão/transação a partir da data em que o recurso é ativado para a conta.

[!DNL Microsoft Advertising] registra cada conversão por [unidade de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data de clique (não a data de conversão). A atribuição é baseada na configuração de atribuição padrão para cada métrica em [!DNL Microsoft Advertising]. A atribuição do Adobe Advertising não é fatorada porque os dados no nível do evento de clique não estão disponíveis.

>[!NOTE]
>
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [altere o nome para exibição](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric) de uma das métricas duplicadas em [!UICONTROL Goals] > [!UICONTROL Conversions]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
>* Os dados no nível da unidade de oferta correspondem aos dados na rede de anúncios no mesmo nível. No entanto, os dados de conversão da própria rede de anúncios para níveis mais altos podem incluir conversões adicionais que não são atribuídas às unidades de oferta secundárias. Os dados em Pesquisa, Social e Commerce são sempre acumulados a partir do nível da unidade de oferta, portanto, por exemplo, um relatório de nível de campanha pode não ter os mesmos totais que um relatório de nível de campanha na rede de anúncios.
>* Normalmente, a variação de dados ocorre menos após a sincronização matinal do que no final do dia, quando as conversões adicionais ainda não foram sincronizadas. Recomendamos validar os dados pela manhã.
>* Os dados não estão disponíveis no nível de público ou localização geográfica e, portanto, não são usados para otimizar automaticamente os ajustes de oferta de RLSA e localização.

## Como comparar dados de conversão no [!DNL Microsoft Advertising] com dados no Search, Social e Commerce

Use as configurações de relatório a seguir para validar dados comparáveis.

### Configurações de relatório a serem usadas em [!DNL Microsoft Advertising]

Gere o relatório das ações de conversão selecionadas por dia e inclua dados para todos os status de anúncios.

### Configurações de relatórios a serem usadas no Search, Social e Commerce

Em Pesquisar, Social e Commerce, use a opção de exibição ou relatório para exibir conversões com base na data de clique (não na data da transação).

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique em **[!UICONTROL Create Report]**, clique em **[!UICONTROL Basic Reports]** no painel esquerdo e selecione **[!UICONTROL Search Engine Account Report]**. Clique em **[!UICONTROL Proceed]**.

1. Na janela [!UICONTROL Create Report], abra a guia **[!UICONTROL Basic Settings]** e especifique as [configurações de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md) a seguir:

   1. Defina **[!UICONTROL Data Aggregation]** como **[!UICONTROL Daily]**.

   1. Defina **[!UICONTROL Conversions Based on]** como **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para o relatório [!DNL Microsoft Advertising].

   1. Defina **[!UICONTROL Search/Content]** como **[!UICONTROL Search Only]**.

   1. Se **[!UICONTROL Filter By]** for exibido, selecione **[!UICONTROL Search engine]**.

   1. Em **[!UICONTROL Search Engine Hierarchy]**, expanda [!DNL Microsoft Advertising] e marque a caixa de seleção ao lado da conta que você deseja comparar. Clique em **[!UICONTROL Add selected items]** para mover a conta para **[!UICONTROL Selected Filters]**.

1. Abra a guia **[!UICONTROL Columns]** e adicione as métricas [!DNL Microsoft Advertising] que deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Configurar campanhas e contas de rede de publicidade](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Sobre o gerenciamento de campanhas e portfólios](/help/search-social-commerce/manage/manage-about.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
