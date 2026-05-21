---
title: Exibir o relatório [!UICONTROL Change History]
description: Saiba como visualizar alterações recentes na conta do anunciante.
exl-id: f8744da7-cc7a-49c1-aeac-1e601768f992
feature: Search Reports
TQID: https://experienceleague.adobe.com/nRlvKpVQf3wbMd83plf3CQp1pPYpHVJzMVJN54lryYM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 0%

---

# Exibir o relatório [!UICONTROL Change History]

O relatório [!UICONTROL Change History] de (nova interface) [!UICONTROL History Logs] e (interface herdada) inclui um log de alterações feitas na conta do anunciante nos últimos 31 dias. O relatório pode incluir alterações nos seguintes tipos de objetos: usuários (anunciantes), portfólios, campanhas, grupos de anúncios, anúncios, palavras-chave, inserções e públicos-alvo de produtos. Você pode classificar e filtrar os dados por qualquer coluna.

Você pode baixar informações adicionais sobre os logs de histórico do anunciante para um arquivo no formato de pasta de trabalho [!DNL Microsoft Excel] (arquivo XLSX). O relatório inclui os valores antigo e novo e a hora em que a alteração ocorreu.

>[!NOTE]
>
>Para ver as alterações nos portfólios, consulte também o [histórico de alterações do portfólio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-change-history.md).

## (Nova interface do usuário) Exibir o relatório [!UICONTROL History Logs] {#history-logs-open}

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL History Logs]**.

1. (Opcional) [Alterar os dados incluídos na exibição](/help/search-social-commerce/common-tasks/data-views/data-views-about.md).

### Gerenciar downloads de relatórios para [!UICONTROL History Logs]

#### Gerar um relatório com as linhas de dados filtradas

1. [Abrir os logs do histórico](#history-logs-open).

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Nas configurações de [!UICONTROL Grid Reports], insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o arquivo é nomeado como &quot;allChangeHistory_YYYYMMDD_NNNN&quot;, onde &quot;NNNN&quot; é o número sequencial do trabalho (como &quot;allChangeHistory_20260402_1326).

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

#### Baixar um relatório concluído

1. [Abrir os logs do histórico](#history-logs-open).

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

#### Excluir um relatório concluído

1. [Abrir os logs do histórico](#history-logs-open).

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Na lista [!UICONTROL Recently Generated] da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

## (Interface herdada) Exibir o relatório [!UICONTROL Change History]

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Change History]**.

1. (Opcional) Altere os dados incluídos no relatório de qualquer uma das seguintes maneiras:

   * (Para mostrar ou ocultar colunas) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") no lado direito de qualquer cabeçalho de coluna, destaque **[!UICONTROL Columns]** e marque a caixa de seleção ao lado de cada coluna a ser incluída e desmarque a caixa de seleção ao lado de cada coluna a ser excluída.

     A configuração da coluna é aplicada à visualização em todos os anunciantes.

   * (Para filtrar os dados por valor de coluna) Siga um destes procedimentos:

      * [Aplique um filtro usando o link **[!UICONTROL Add Filter]**](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

      * [Aplicar um filtro a partir de um menu de cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

   * (Para alterar o intervalo de datas do relatório) Faça o seguinte:

      1. Acima da tabela de dados, clique no intervalo de datas atual.

      1. Especifique o intervalo:

         * (Para um intervalo predefinido) — Selecione na lista de incrementos de tempo comuns. O padrão é *[!UICONTROL 2 Days Ago]*.

         * (Para um intervalo específico) — Selecione **[!UICONTROL Custom Date Range]** e especifique a data inicial e a data final.

           Insira as datas no formato MM/DD/AAAA ou MM-DD-AAAA ou clique em ![Calendário](/help/search-social-commerce/assets/calendar.png "Calendário") ao lado de cada campo para abrir o calendário e selecionar uma data. Você pode incluir dados somente dos últimos 31 dias.

      1. Clique em **[!UICONTROL Apply]**.

1. (Opcional) Baixe uma cópia do relatório:

   1. Acima da tabela de dados, clique em **[!UICONTROL Download]**.

      Quando o relatório for concluído, ele será listado no menu [!UICONTROL Download].

   1. (Para abrir ou salvar os dados do relatório em um arquivo) Clique em ![Baixar Relatório como XLS](/help/search-social-commerce/assets/download-spreadsheet2.png "Baixar Relatório como XLS") ao lado do nome do arquivo e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

      Para obter mais informações, consulte a ajuda online do navegador.
