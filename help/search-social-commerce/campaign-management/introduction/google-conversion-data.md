---
title: '[!DNL Google Ads] dados de conversão'
description: Saiba mais sobre os tipos de dados de conversão  [!DNL Google Ads] rastreados disponíveis em Pesquisa, Social e Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
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
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [altere o nome para exibição](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) de uma das métricas duplicadas em [!UICONTROL Admin] > [!UICONTROL Conversions]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
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

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** e clique em **[!UICONTROL Search Engine Account Report]**.

1. Na janela [!UICONTROL Report Settings], especifique as seguintes configurações de relatório:

   1. Na seção **[!UICONTROL Conversions Based]** em, selecione **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para o relatório [!DNL Google Ads].

   1. Na seção **[!UICONTROL Search/Content]**, selecione **[!UICONTROL Search Only]**.

   1. Na seção **[!UICONTROL Search Engine Hierarchy]**, expanda a seção [!UICONTROL Google Adwords] e selecione a conta.

   1. Abra a guia [!UICONTROL Columns] e adicione as métricas [!DNL Google Ads] (começando com &quot;GL&quot;) que você deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação de contas e campanhas de rede de publicidade](campaign-implemention-overview.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Criar uma marca de conversão para [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
