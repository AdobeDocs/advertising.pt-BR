---
title: Gerenciar as métricas de conversão de um anunciante
description: Saiba como você pode usar as métricas de conversão que o Adobe Advertising rastreia para um anunciante.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 932
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar as métricas de conversão de um anunciante

*recurso do Beta*

As métricas de [conversão](/help/search-social-commerce/glossary.md#c-d) de um anunciante são usadas em todo o Adobe Advertising:

* Em Pesquisa, Social e Commerce, os dados para as métricas de conversão podem ser exibidos em colunas nas visualizações de gerenciamento de campanha, portfólio e objetivo e nos relatórios. Os usuários com privilégios de acesso suficientes também podem usar métricas de conversão para criar objetivos, que são usados para otimizar portfólios.

* (Anunciantes com o Advertising DSP) No DSP, você pode incluir métricas de conversão em exibições de gerenciamento de campanha, objetivos personalizados e relatórios personalizados. Você também pode usar as métricas de conversão para criar [objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md), que são usados para otimizar pacotes.

As métricas disponíveis incluem:

* Métricas de conversão que o Adobe Advertising rastreia para um anunciante.

* [Métricas de conversão e envolvimento do site sincronizadas do Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventos do site sincronizados do Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversões rastreadas por [!DNL Google Ads] e conversões rastreadas por [!DNL Microsoft Advertising] marcas de rastreamento de evento universal.

* (Quando [você configurou uma  [!DNL Google Analytics] combinação específica de conta, propriedade e exibição](/help/search-social-commerce/admin/data-sources/data-source-about.md) para Pesquisa, Social e Commerce) Conversões rastreadas por [!DNL Google Analytics].

* Conversões de feeds personalizados.

A partir da lista de métricas de conversão disponíveis, cada usuário com acesso aos dados do anunciante pode personalizar as métricas que vê disponíveis para exibições de gerenciamento e relatórios, incluindo ou omitindo métricas específicas à sua escolha. Você pode usar um nome de métrica exatamente como está escrito nos dados recuperados ou alterar o nome mostrado nos cabeçalhos da coluna para facilitar a leitura.

>[!IMPORTANT]
>
>Por padrão, nenhuma das métricas de conversão de um anunciante — exceto as conversões rastreadas pelas tags de rastreamento de evento universal [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] — está disponível para inclusão em exibições de gerenciamento de campanhas e portfólios, objetivos e relatórios. Para disponibilizar uma métrica de conversão, você deve disponibilizá-la explicitamente.
>
>Novas conversões controladas por [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] marcas de rastreamento de eventos universais estão sempre disponíveis automaticamente.

>[!TIP]
>
>Quando o anunciante (ou a rede de anúncios) parar de coletar uma métrica de conversão, [oculte-a dos modos de exibição e relatórios de gerenciamento](#conversion-metrics-change-available), a menos que você queira usá-la para exibir dados históricos.

## Exibir as métricas de conversão rastreadas para um anunciante

* No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

Todas as métricas de conversão coletadas para o anunciante e todos os nomes de exibição diferentes atribuídos a ele são listados. Cada linha de métrica inclui a origem da métrica.

## Alterar o nome de exibição de uma métrica de conversão

Por exemplo, se você coletar dados de registro usando uma métrica de conversão chamada *reg*, poderá alterar o nome de exibição para vê-los exibidos como &quot;Registros&quot;.

Não é possível excluir um nome para exibição existente.

>[!NOTE]
>
>Para [métricas de [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md), todas as alterações manuais no nome para exibição serão substituídas se você atualizar ou reautenticar a integração. Da mesma forma, qualquer alteração de nome em [!DNL Google Analytics] é ignorada a menos que você [atualize](/help/search-social-commerce/admin/data-sources/data-source-edit.md) ou [reautentique](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) a integração.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Filtre a lista [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de um cabeçalho de [coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Na coluna **[!UICONTROL Conversion Display Name]** da métrica, mantenha o cursor sobre o nome da métrica e clique em **...** > **[!UICONTROL Rename]**.

1. Insira o nome que deve ser exibido e clique em **[!UICONTROL Apply]**.

   Os nomes para exibição devem ser exclusivos e não podem incluir os seguintes caracteres especiais: `\"<'>&`

## Alterar as métricas de conversão disponíveis em exibições de gerenciamento, objetivos e relatórios {#conversion-metrics-change-available}

>[!NOTE]
>
>Quando você oculta uma métrica de conversão que estava disponível anteriormente, ela é removida de qualquer métrica derivada que contenha a métrica de conversão.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

   Todas as métricas de conversão coletadas para o anunciante e todos os nomes diferentes especificados para exibição são listados.

1. (Opcional) Filtre a lista [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de um [cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Altere as métricas de conversão disponíveis para exibições de gerenciamento e relatórios:

   * Para mostrar ou ocultar uma única métrica, clique na opção na coluna **[!UICONTROL Visibility]** para alterar a configuração.

   * Para mostrar ou ocultar várias métricas, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada métrica de conversão.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Na barra de ferramentas de ações em massa, clique em ![Visibilidade](/help/search-social-commerce/assets/visible.png "Visibilidade") para mostrar as métricas ou ![Visibilidade desativada](/help/search-social-commerce/assets/visibility-off.png "Visibilidade desativada") para ocultar as métricas.

      1. (Para ocultar métricas) Na mensagem de confirmação, clique em **[!UICONTROL Confirm]** para ocultar as métricas, incluindo a remoção delas de qualquer métrica derivada que contenha as métricas.

## Gerenciar visibilidade de conversão e relatórios de origem

Você pode baixar as seguintes informações sobre suas conversões rastreadas: o nome da métrica sincronizada, o nome de exibição da métrica nas exibições e relatórios de gerenciamento de Pesquisa, Social e Commerce, se a métrica está visível nas exibições e relatórios de gerenciamento, a ID de conversão e a origem da métrica. Baixe os dados para um arquivo no formato da pasta de trabalho [!DNL Microsoft Excel] (arquivo XLSX).

### Gerar um relatório com as linhas de dados filtradas

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Especifique as conversões cujos dados você deseja baixar:

   * Para baixar dados de linhas específicas, marque as caixas de seleção ao lado das linhas.

   * Para baixar dados para todas as linhas, não é necessário marcar nenhuma caixa de seleção. Todas as linhas são incluídas por padrão.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Nas configurações de [!UICONTROL Grid Reports], insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o arquivo é nomeado como &quot;converssionsReport_YYYMMDD_NNNN&quot;, onde &quot;NNNN&quot; é o número sequencial do trabalho (como &quot;converssionsReport_20260402_1326).

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório concluído

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") **[!UICONTROL Reports]**.

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

<!--
>[!MORELIKETHIS]
>
>* 
-->
