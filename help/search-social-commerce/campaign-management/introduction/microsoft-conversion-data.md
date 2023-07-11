---
title: '[!DNL Microsoft Advertising] dados de conversão'
description: Saiba mais sobre os tipos de [!DNL Microsoft Advertising]Dados de conversão rastreados pelo disponíveis no Search, Social e Commerce.
source-git-commit: 0d7a7b63b31f85b3befb3217fc43bcb229b370f0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] dados de conversão no Search, Social e Commerce

O Search, Social e Commerce sincroniza automaticamente todas as conversões rastreadas pelo seu [Tags de rastreamento de evento universal (UET) da Microsoft Advertising](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) para conversões de site do para o, incluindo conversões de view-through, para relatórios e otimização.

Todas as métricas estão disponíveis automaticamente em suas visualizações de gerenciamento de campanhas e relatórios básicos, e também estão disponíveis para uso em objetivos de portfólio para otimização de campanhas do Microsoft Advertising.

## Dados de conversão disponíveis

Pesquisar, Social e Comércio sincroniza dados para conversões para as quais &quot;[!DNL Include in 'Conversions']&quot; for ativada, extraindo os dados dos últimos 35 dias e depois extraindo as alterações nos dados diariamente até 09:00-10:00 no fuso horário do anunciante. Os dados históricos podem mudar de dia para dia, à medida que novas conversões são rastreadas para cada clique.

Duas propriedades de transação para cada [[!DNL Microsoft Advertising]Conversão rastreada](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que você configurou em [!DNL Microsoft Advertising]) ficam disponíveis automaticamente no Search, Social e Commerce, usando os nomes de conversão configurados em [!DNL Microsoft Advertising]. As propriedades de transação para cada conversão incluem:

* `<conversion-name>` — O valor de conversão da palavra-chave (como Compra).

  >[!TIP]
  >
  >Use esse tipo de propriedade no objetivo para portfólios que incluem [!DNL Microsoft Advertising] campanhas com o Valor máximo de conversão e estratégias de oferta de ROAS do Target.

* `CT_<conversion-name>` — O número (contagem) de conversões, começando com o prefixo &quot;CT_&quot; (como CT_Purchase).

  >[!TIP]
  >
  >Use esse tipo de propriedade no objetivo para portfólios que incluem [!DNL Microsoft Advertising] campanhas com as estratégias de oferta Máximo de conversões e CPA do Target.

Os dados são disponibilizados com base na hora do clique e no horário da conversão/transação a partir da data em que o recurso é ativado para a conta.

[!DNL Microsoft Advertising] registra cada conversão por [unidade de oferta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data de clique (não a data de conversão). A atribuição se baseia na configuração padrão de atribuição de cada métrica em [!DNL Microsoft Advertising]; a atribuição Adobe Advertising não é considerada porque os dados no nível do evento de clique não estão disponíveis.

>[!NOTE]
>
>* Se você tiver várias contas com os mesmos nomes de conversão, poderá ver nomes de conversão duplicados no Adobe Advertising. Se isso ocorrer, [alterar o nome de exibição](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) para uma das métricas duplicadas no [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Os relatórios não são precisos quando duas métricas diferentes têm o mesmo nome.
>* Os dados no nível da unidade de oferta correspondem aos dados na rede de anúncios no mesmo nível. No entanto, os dados de conversão da própria rede de anúncios para níveis mais altos podem incluir conversões adicionais que não são atribuídas às unidades de oferta secundárias. Os dados em Pesquisa, Social e Comércio são sempre acumulados a partir do nível da unidade de oferta, portanto, por exemplo, um relatório de nível de campanha pode não ter os mesmos totais que um relatório de nível de campanha na rede de anúncios.
>* Normalmente, a variação de dados ocorre menos após a sincronização matinal do que no final do dia, quando as conversões adicionais ainda não foram sincronizadas. Recomendamos validar os dados pela manhã.
>* Os dados não estão disponíveis no nível de público ou localização geográfica e, portanto, não são usados para otimizar automaticamente os ajustes de oferta de RLSA e localização.

## Como comparar dados de conversão no [!DNL Microsoft Advertising] com dados em Pesquisa, Social e Comércio

Use as configurações de relatório a seguir para validar dados comparáveis.

### Configurações de relatório a serem usadas no [!DNL Microsoft Advertising]

Gere o relatório das ações de conversão selecionadas por dia e inclua dados para todos os status de anúncios.

### Configurações de relatórios a serem usadas em pesquisa, redes sociais e comércio

Em Pesquisar, Social e Comércio, use a opção de exibição ou relatório para exibir conversões com base na data de clique (não a data da transação).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** e clique em **[!UICONTROL Search Engine Account Report]**.

1. No [!UICONTROL Report Settings] especifique as seguintes configurações de relatório:

   1. No **[!UICONTROL Conversions Based]** em seção, selecione **[!UICONTROL Click date]**.

   1. Especifique o mesmo intervalo de datas usado para a variável [!DNL Microsoft Advertising] relatório.

   1. No **[!UICONTROL Search/Content]** , selecione **[!UICONTROL Search Only]**.

   1. No **[!UICONTROL Search Engine Hierarchy]** , expanda a [!UICONTROL Microsoft Advertising] e selecione a conta.

   1. Abra o [!UICONTROL Columns] e adicione a guia [!DNL Microsoft Advertising] métricas que você deseja comparar.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação de contas e campanhas de rede de anúncios](campaign-implemention-overview.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Exibir as propriedades de transação rastreadas para um anunciante](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
