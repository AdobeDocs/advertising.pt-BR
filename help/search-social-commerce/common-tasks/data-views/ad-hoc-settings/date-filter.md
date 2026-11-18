---
title: Filtrar dados por intervalo de datas
description: Saiba como usar o filtro de intervalo de datas global.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 968023d95217d4d17b1441ae717f3e472b31f7c4
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%
---
# Filtrar dados por intervalo de datas

Use o filtro de intervalo de datas para especificar o período no qual mostrar dados de desempenho. Nas exibições que suportam comparação de datas, você também pode comparar o desempenho de dois períodos.

## (Nova interface do usuário) Alterar o intervalo de datas {#date-filter-new-ui}

1. No cabeçalho da página, clique no controle de intervalo de datas com o ícone de calendário.

1. Especifique o intervalo de datas:

   * Para usar um intervalo predefinido, selecione uma opção no menu acima do primeiro calendário, como **[!UICONTROL Yesterday]** ou **[!UICONTROL Last 7 Days]**.

   * Para usar um intervalo personalizado, selecione **[!UICONTROL Custom Date Range]** e selecione as datas de início e término no calendário. Use as setas do calendário para navegar entre meses.

1. Clique em **[!UICONTROL Apply]**.

## (Nova interface do usuário) Comparar dados de dois períodos {#compare-periods-new-ui}

*Exibições que oferecem suporte somente à comparação de datas*

1. No cabeçalho da página, clique no controle de intervalo de datas com o ícone de calendário.

1. Ligue o **[!UICONTROL Compare Periods]**.

   Dois painéis de calendário são mostrados lado a lado. O primeiro período tem um marcador azul-petróleo e o período de comparação tem um marcador roxo.

1. No primeiro painel, especifique o intervalo de datas:

   * Para usar um intervalo predefinido, selecione uma opção no menu acima do primeiro calendário, como **[!UICONTROL Yesterday]** ou **[!UICONTROL Last 7 Days]**.

   * Para usar um intervalo personalizado, selecione **[!UICONTROL Custom Date Range]** e selecione as datas de início e término no calendário. Use as setas do calendário para navegar entre meses.

1. No segundo painel, selecione uma predefinição de comparação ou clique em uma data de início no calendário.

   O período de comparação tem o mesmo número de dias que o primeiro período. Revise os intervalos de datas completos acima de ambos os calendários.

1. Em **[!UICONTROL Comparison Format]**, selecione como exibir a diferença:

   * **[!UICONTROL As percentage]:** Mostrar a diferença como uma porcentagem.

   * **[!UICONTROL As variance]:** Mostrar a diferença como um valor numérico.

1. Clique em **[!UICONTROL Apply]**.

   O controle de intervalo de datas mostra intervalos de datas completos com seus rótulos de período e marcadores de cor. Cada métrica comparável é agrupada em duas colunas de período e uma coluna **[!UICONTROL Change]**. Os campos que não são comparáveis permanecem como colunas únicas. Os marcadores de período nos cabeçalhos da coluna identificam os intervalos de datas correspondentes.

Para interromper a comparação de períodos, abra o controle de intervalo de datas, desative o **[!UICONTROL Compare Periods]** e clique em **[!UICONTROL Apply]**. Desativar a comparação limpa os filtros com base nos dados de comparação.

### Alterar o formato de comparação de um menu de colunas

1. Com a comparação de datas habilitada, abra o menu de cabeçalho de coluna para uma coluna **[!UICONTROL Change]** ou uma coluna de período para uma métrica comparável.

1. Selecione **[!UICONTROL As percentage]** ou **[!UICONTROL As variance]**.

   A seleção se aplica a todas as métricas de comparação na tabela de dados, não apenas à coluna selecionada. O controle de intervalo de datas é sincronizado com a seleção e o formato é compartilhado nas páginas aplicáveis do anunciante atual, incluindo exibições com intervalos de datas salvos.

   Uma mensagem de confirmação é exibida depois que a tabela de dados é atualizada com sucesso. Se a tabela de dados não puder ser atualizada com o formato selecionado, uma mensagem de erro será exibida; tente selecionar o formato novamente.

As opções de classificação e filtragem permanecem disponíveis nos menus de coluna, quando compatíveis.

## (Interface herdada) Configurações de intervalo de datas

O mesmo filtro de intervalo de datas global é aplicado à maioria das visualizações de dados, em todos os anunciantes, exceto para exibições padrão e personalizadas para as quais você salvou intervalos de datas específicos. O intervalo de datas padrão do sistema para exibições de gerenciamento de campanha é &quot;Ontem&quot;.

Suas configurações de intervalo de datas são salvas em um cookie específico do navegador, de modo que quaisquer alterações no filtro de intervalo de datas são usadas para todos os anunciantes sempre que você entrar usando o mesmo aplicativo do navegador, até alterar o filtro ou excluir o cookie. Cada aplicativo de navegador usado armazena configurações de filtro de intervalo de datas em um cookie diferente.

Quando você salva um intervalo de datas específico para uma exibição padrão ou personalizada, esse intervalo é aplicado sempre que a exibição é aplicada, independentemente do aplicativo do navegador usado.

>[!NOTE]
>
>* Você pode exibir dados dos 13 meses anteriores, mas qualquer exibição personalizada existente pode incluir dados apenas dos 180 dias anteriores.
>* Para exibir dados anteriores, vá para a [[!UICONTROL Reports] exibição](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) e execute um relatório básico.
>* Você também pode salvar um intervalo de datas para uma [exibição padrão ou personalizada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## (Interface herdada) Alterar o filtro de data global nas visualizações de campanha

1. Acima de qualquer tabela de dados em Pesquisar \> Campanhas \> Campanhas, clique no intervalo de datas atual.

1. No campo **[!UICONTROL Date Range]**, especifique o intervalo:

   * Para um intervalo predefinido: selecione na lista de incrementos de tempo comuns, variando de *[!UICONTROL Today]* a *[!UICONTROL Last 180 Days]*. O padrão é *[!UICONTROL Yesterday]*.

   * Para um intervalo específico: Selecione **[!UICONTROL Custom Date Range]** e especifique a data inicial e a data final.

     Insira as datas no formato MM/DD/AAAA ou MM-DD-AAAA ou clique em ![Ícone do calendário](/help/search-social-commerce/assets/calendar.png "Ícone do calendário") ao lado de cada campo para abrir o calendário e selecionar uma data.

1. (Opcional) Comparar dados para o intervalo de datas especificado com dados para um segundo intervalo de datas:

   1. Mova o controle deslizante **[!UICONTROL Comparison]** para a posição &quot;ligado&quot;.

      Ao selecionar essa opção, duas colunas adicionais são adicionadas para cada coluna de dados regular. Por exemplo, em vez de incluir apenas uma coluna para &quot;[!UICONTROL Impressions]&quot;, a tabela inclui colunas para &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; e &quot;[!UICONTROL Impressions Diff]&quot;.  Se exportar os dados, as mesmas colunas serão grafadas como &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; e &quot;[!UICONTROL Impressions Difference]&quot;.

   1. Especifique o segundo intervalo de datas.

   1. Escolha como expressar a diferença entre os dados nos dois intervalos de datas selecionados na coluna &quot;\[_Data field_\] Difference&quot;:

      * *[!UICONTROL Variance]* (padrão): mostra a diferença como um valor numérico.

      * *[!UICONTROL % Change]:* Mostra a diferença como uma porcentagem.

1. Clique em **[!UICONTROL Apply]**.
