---
title: '[!DNL Google Ads] dados de conversão'
description: Saiba mais sobre os tipos de dados de conversão rastreados por [!DNL Google Ads] disponíveis em Pesquisa, Social e Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
TQID: 'https://experienceleague.adobe.com/7qqQKfVhueHMc7hJDEac86la9dp36hwtrLF5ikxJzJM'
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
source-wordcount: '672'
ht-degree: 0%
---
# [!DNL Google Ads] dados de conversão em Pesquisa, Social e Commerce

O Search, Social e Commerce sincroniza automaticamente dados de conversão rastreados pelo [!DNL Google Ads] de todas as suas campanhas nas redes de pesquisa e compra do [!DNL Google Ads] no Search, Social e Commerce para relatórios e otimização.

Todas as métricas estão disponíveis automaticamente nas visualizações de gerenciamento de campanhas e relatórios básicos, além de estarem disponíveis para uso em objetivos de portfólio para otimização.

## Dados de conversão disponíveis

O Search, Social e Commerce sincroniza dados para conversões para as quais a opção &quot;[!DNL Include in 'Conversions']&quot; está habilitada, extraindo os dados dos últimos 35 dias e depois extraindo as alterações para os dados diariamente até 09:00-10:00 no fuso horário do anunciante. Os dados históricos podem mudar de dia para dia, à medida que novas conversões são rastreadas para cada clique.

Até três métricas para cada conversão [[!DNL Google Ads] rastreada](https://support.google.com/google-ads/answer/4677036) (que você configurou em [!DNL Google Ads]) estão automaticamente disponíveis em Pesquisa, Social e Commerce, usando os nomes de conversão configurados em [!DNL Google Ads]. As métricas para cada conversão incluem:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Ao rastrear) O valor de conversão da palavra-chave, começando com o prefixo &quot;GGL&quot; (como Compra GGL).

* `GGL_CT*` — O número (contagem) de conversões, começando com o prefixo &quot;GGL_CT&quot; (como GGL_CT_Purchase).

* `GGL_XD_CT*` — (Quando disponível para o tipo de conversão, ao rastreá-los) O número (contagem) de conversões entre dispositivos, conforme medido pelo Google, começando com o prefixo &quot;GGL_XD_CT_&quot; (como GGL_XD_CT_Purchase).

[!DNL Google Ads] registra cada conversão por [unidade de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data de clique (não a data de conversão). A atribuição é baseada na configuração de atribuição padrão para cada métrica em [!DNL Google Ads]. A atribuição do Adobe Advertising não é fatorada porque os dados no nível do evento de clique não estão disponíveis.

>[!NOTE]
>
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [altere o nome para exibição](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric) de uma das métricas duplicadas em [!UICONTROL Goals] > [!UICONTROL Conversions]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
>* Os dados no nível da unidade de oferta correspondem aos dados em [!DNL Google Ads] no mesmo nível. No entanto, os dados de conversão de [!DNL Google Ads] para níveis superiores podem incluir conversões adicionais que não são atribuídas às unidades de oferta secundárias. Os dados em Pesquisa, Social e Commerce são sempre acumulados a partir do nível da unidade de oferta, portanto, por exemplo, um relatório de nível de campanha pode não ter os mesmos totais que um relatório de nível de campanha no Google Ads.
>* Normalmente, a variação de dados ocorre menos após a sincronização matinal do que no final do dia, quando as conversões adicionais ainda não foram sincronizadas. Recomendamos validar os dados pela manhã.
>* Os dados de conversão não estão disponíveis para os anúncios [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] e [!DNL YouTube]. Filtre esses tipos de anúncios ao comparar os dados no [!DNL Google Ads] com os dados no Search, Social e Commerce.
>* Os dados para conversões de [!DNL Google Ads] não estão disponíveis no nível de público ou localização geográfica e, portanto, não são usados para otimizar automaticamente os ajustes de oferta de RLSA e localização.

## Como comparar dados de conversão no [!DNL Google Ads] com dados no Search, Social e Commerce

Se você comparar os dados em Search, Social e Commerce com os do [!DNL Google Ads], use a opção de exibição ou relatório para exibir conversões com base na data de clique (não na data da transação).

Use as configurações de relatório a seguir para validar dados comparáveis.

### Configurações de relatório a serem usadas em [!DNL Google Ads]

Gere o relatório das ações de conversão selecionadas por dia e inclua dados para todos os status de anúncios.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Configurações de relatórios a serem usadas no Search, Social e Commerce

Em Pesquisar, Social e Commerce, use a opção de exibição ou relatório para exibir conversões com base na data de clique (não na data da transação).

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique em **[!UICONTROL Create Report]**, clique em **[!UICONTROL Basic Reports]** no painel esquerdo e selecione **[!UICONTROL Search Engine Account Report]**. Clique em **[!UICONTROL Proceed]**.

1. Na janela [!UICONTROL Create Report], abra a guia **[!UICONTROL Basic Settings]** e especifique as [configurações de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md) a seguir:

   1. Defina **[!UICONTROL Data Aggregation]** como **[!UICONTROL Daily]**.

   1. Defina **[!UICONTROL Conversions Based on]** como **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para o relatório [!DNL Google Ads].

   1. Defina **[!UICONTROL Search/Content]** como **[!UICONTROL Search Only]**.

   1. Se **[!UICONTROL Filter By]** for exibido, selecione **[!UICONTROL Search engine]**.

   1. Em **[!UICONTROL Search Engine Hierarchy]**, expanda [!DNL Google Ads] e marque a caixa de seleção ao lado da conta que você deseja comparar. Clique em **[!UICONTROL Add selected items]** para mover a conta para **[!UICONTROL Selected Filters]**.

1. Abra a guia **[!UICONTROL Columns]** e adicione as métricas [!DNL Google Ads] (começando com &quot;GL&quot;) que você deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Configurar campanhas e contas de rede de publicidade](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Sobre o gerenciamento de campanhas e portfólios](/help/search-social-commerce/manage/manage-about.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/goals/conversions/conversions-upload-offline-enhanced-conversions.md)
