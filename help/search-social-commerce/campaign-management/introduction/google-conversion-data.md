---
title: '[!DNL Google Ads] dados de conversão'
description: Saiba mais sobre os tipos de [!DNL Google Ads]Dados de conversão rastreados pelo disponíveis no Search, Social e Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# [!DNL Google Ads] dados de conversão no Search, Social e Commerce

O Search, Social e Commerce sincroniza automaticamente [!DNL Google Ads]Dados de conversão rastreados pelo para todas as campanhas no [!DNL Google Ads] redes de pesquisa e compras em Pesquisa, Social e Comércio para geração de relatórios e otimização.

Todas as métricas estão disponíveis automaticamente nas visualizações de gerenciamento de campanhas e relatórios básicos, além de estarem disponíveis para uso em objetivos de portfólio para otimização.

## Dados de conversão disponíveis

Pesquisar, Social e Comércio sincroniza dados para conversões para as quais &quot;[!DNL Include in 'Conversions']&quot; for ativada, extraindo os dados dos últimos 35 dias e depois extraindo as alterações nos dados diariamente até 09:00-10:00 no fuso horário do anunciante. Os dados históricos podem mudar de dia para dia, à medida que novas conversões são rastreadas para cada clique.

Até três propriedades de transação para cada [[!DNL Google Ads]Conversão rastreada](https://support.google.com/google-ads/answer/4677036) (que você configurou em [!DNL Google Ads]) ficam disponíveis automaticamente no Search, Social e Commerce, usando os nomes de conversão configurados em [!DNL Google Ads]. As propriedades de transação para cada conversão incluem:

* `GGL*` — (Ao rastrear) O valor de conversão da palavra-chave, começando com o prefixo &quot;GGL&quot; (como Compra GGL).

* `GGL_CT*` — O número (contagem) de conversões, começando com o prefixo &quot;GGL_CT&quot; (como GGL_CT_Purchase).

* `GGL_XD_CT*` — (Quando disponível para o tipo de conversão, ao rastreá-los) O número (contagem) de conversões entre dispositivos, conforme medido pelo Google, começando com o prefixo &quot;GGL_XD_CT_&quot; (como GGL_XD_CT_Purchase).

[!DNL Google Ads] registra cada conversão por [unidade de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data de clique (não a data de conversão). A atribuição se baseia na configuração padrão de atribuição de cada métrica em [!DNL Google Ads]; a atribuição Adobe Advertising não é considerada porque os dados no nível do evento de clique não estão disponíveis.

>[!NOTE]
>
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [alterar o nome de exibição](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) para uma das métricas duplicadas no [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
>* Os dados no nível de unidade de oferta correspondem aos dados em [!DNL Google Ads] no mesmo nível. No entanto, [!DNL Google Ads]Os dados de conversão próprios do para níveis superiores podem incluir conversões adicionais que não são atribuídas às unidades de oferta secundárias. Os dados em Pesquisa, Social e Comércio são sempre acumulados a partir do nível da unidade de oferta, portanto, por exemplo, um relatório de nível de campanha pode não ter os mesmos totais que um relatório de nível de campanha no Google Ads.
>* Normalmente, a variação de dados ocorre menos após a sincronização matinal do que no final do dia, quando as conversões adicionais ainda não foram sincronizadas. Recomendamos validar os dados pela manhã.
>* Os dados de conversão não estão disponíveis para [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], e [!DNL YouTube] anúncios. Filtre esses tipos de anúncios ao comparar dados no [!DNL Google Ads] com dados em Pesquisa, Social e Comércio.
>* Dados para [!DNL Google Ads] as conversões não estão disponíveis no nível de público ou localização geográfica e, portanto, não são usadas para otimizar automaticamente os ajustes de oferta de RLSA e localização.

## Como comparar dados de conversão no [!DNL Google Ads] com dados em Pesquisa, Social e Comércio

Se você comparar os dados no Search, Social e Commerce com os do [!DNL Google Ads], use a opção de exibição ou de relatório para exibir conversões com base na data de clique (não na data da transação).

Use as configurações de relatório a seguir para validar dados comparáveis.

### Configurações de relatório a serem usadas no [!DNL Google Ads]

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

### Configurações de relatórios a serem usadas em pesquisa, redes sociais e comércio

Em Pesquisar, Social e Comércio, use a opção de exibição ou relatório para exibir conversões com base na data de clique (não a data da transação).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** e clique em **[!UICONTROL Search Engine Account Report]**.

1. No [!UICONTROL Report Settings] especifique as seguintes configurações de relatório:

   1. No **[!UICONTROL Conversions Based]** em seção, selecione **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para a variável [!DNL Google Ads] relatório.

   1. No **[!UICONTROL Search/Content]** , selecione **[!UICONTROL Search Only]**.

   1. No **[!UICONTROL Search Engine Hierarchy]** , expanda a [!UICONTROL Google Adwords] e selecione a conta.

   1. Abra o [!UICONTROL Columns] e adicione a guia [!DNL Google Ads] métricas (começando com &quot;GL&quot;) que você deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação de contas e campanhas de rede de anúncios](campaign-implemention-overview.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Exibir as propriedades de transação rastreadas para um anunciante](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
