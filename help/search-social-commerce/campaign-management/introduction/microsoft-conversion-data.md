---
title: '[!DNL Microsoft Advertising] dados de conversão'
description: Saiba mais sobre os tipos de dados de conversão  [!DNL Microsoft Advertising] rastreados disponíveis em Pesquisa, Social e Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '629'
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
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [altere o nome para exibição](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) de uma das métricas duplicadas em [!UICONTROL Admin] > [!UICONTROL Conversions]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
>* Os dados no nível da unidade de oferta correspondem aos dados na rede de anúncios no mesmo nível. No entanto, os dados de conversão da própria rede de anúncios para níveis mais altos podem incluir conversões adicionais que não são atribuídas às unidades de oferta secundárias. Os dados em Pesquisa, Social e Commerce são sempre acumulados a partir do nível da unidade de oferta, portanto, por exemplo, um relatório de nível de campanha pode não ter os mesmos totais que um relatório de nível de campanha na rede de anúncios.
>* Normalmente, a variação de dados ocorre menos após a sincronização matinal do que no final do dia, quando as conversões adicionais ainda não foram sincronizadas. Recomendamos validar os dados pela manhã.
>* Os dados não estão disponíveis no nível de público ou localização geográfica e, portanto, não são usados para otimizar automaticamente os ajustes de oferta de RLSA e localização.

## Como comparar dados de conversão no [!DNL Microsoft Advertising] com dados no Search, Social e Commerce

Use as configurações de relatório a seguir para validar dados comparáveis.

### Configurações de relatório a serem usadas em [!DNL Microsoft Advertising]

Gere o relatório das ações de conversão selecionadas por dia e inclua dados para todos os status de anúncios.

### Configurações de relatórios a serem usadas no Search, Social e Commerce

Em Pesquisar, Social e Commerce, use a opção de exibição ou relatório para exibir conversões com base na data de clique (não na data da transação).

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** e clique em **[!UICONTROL Search Engine Account Report]**.

1. Na janela [!UICONTROL Report Settings], especifique as seguintes configurações de relatório:

   1. Na seção **[!UICONTROL Conversions Based]** em, selecione **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para o relatório [!DNL Microsoft Advertising].

   1. Na seção **[!UICONTROL Search/Content]**, selecione **[!UICONTROL Search Only]**.

   1. Na seção **[!UICONTROL Search Engine Hierarchy]**, expanda a seção [!UICONTROL Microsoft Advertising] e selecione a conta.

   1. Abra a guia [!UICONTROL Columns] e adicione as métricas [!DNL Microsoft Advertising] que deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação de contas e campanhas de rede de publicidade](campaign-implemention-overview.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
