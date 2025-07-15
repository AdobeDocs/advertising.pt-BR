---
title: Baixar dados de uma visualização de gerenciamento de campanha
description: Saiba como baixar dados da maioria das exibições de gerenciamento de campanha.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# (Interface herdada) Baixar dados de uma visualização de gerenciamento de campanha

*Interface do usuário herdada*

Você pode baixar dados das visualizações [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] exceto para as visualizações [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] e [!UICONTROL Extensions]. Você pode baixar:

* Um relatório no formato [!DNL XLSM] (planilha habilitada para macro [!DNL Microsoft Excel]). Se você selecionar linhas específicas na exibição, o relatório incluirá uma linha para cada linha selecionada. Se você não selecionar nenhuma linha, uma linha será criada para cada linha na exibição.

* Um arquivo de bulksheet no formato TXT que inclui todas as entidades secundárias relevantes. Se você selecionar linhas para entidades em várias redes de anúncios, um arquivo será criado para cada rede de anúncios relevante. Se você não selecionar nenhuma linha, um arquivo será criado para cada rede de publicidade representada na exibição. Os arquivos de bulksheet gerados para diferentes redes de anúncios incluem diferentes colunas de dados.

  Se você gerar dados para várias campanhas e os dados combinados consistirem em mais de 500.000 linhas, os dados serão divididos ainda mais por campanha em dois ou mais arquivos, conforme necessário, chamados `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt` e assim por diante.

  Cada arquivo de bulksheet no painel [!UICONTROL Downloads] também está listado na exibição [!UICONTROL Bulksheets]. Quando o arquivo for criado, você receberá uma notificação por email com um link do qual poderá baixar o arquivo; dependendo da quantidade de dados que estiver sendo compilada, a notificação poderá levar vários minutos ou mais. Se, no entanto, a geração do arquivo falhar, um arquivo de erro será listado na exibição Bulksheets e você receberá uma notificação por email com um link para o arquivo de erro. Excluir um arquivo de bulksheet do painel [!UICONTROL Download] ou da guia [!UICONTROL Bulksheets] o exclui de ambos os locais.

>[!NOTE]
>
>Consulte também a ajuda para baixar dados na nova interface de usuário do &quot;[[!UICONTROL Portfolios] modo de exibição](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)&quot;, &quot;[[!UICONTROL Campaigns] modo de exibição](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)&quot; e &quot;[[!UICONTROL Ad Groups] modo de exibição](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md).&quot;

1. (Opcional) Selecione linhas individuais para incluir no arquivo.

   Caso contrário, todos os dados na visualização serão incluídos.

1. À direita da barra de ferramentas, clique em ![Download de Relatório](/help/search-social-commerce/assets/download.png "Download de Relatório").

1. Clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar") **[!UICONTROL Create]**, opcionalmente adicione o nome do arquivo, e clique em **[!UICONTROL Report]** ou **[!UICONTROL Bulksheet]**.

1. (Opcional) Depois que o trabalho de relatório for concluído, clique em ![Download de Relatório](/help/search-social-commerce/assets/download.png "Download de Relatório") para exibir o painel [!UICONTROL Available Reports] e, em seguida, baixe ou exclua o relatório:

   * Para abrir ou salvar o arquivo de acordo com o procedimento normal do seu navegador, clique em ![Baixar planilha](/help/search-social-commerce/assets/download-spreadsheet.png "Baixar planilha").

     Para obter mais informações sobre o procedimento do navegador, consulte a ajuda online do navegador.

   * Para excluir o arquivo, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

>[!MORELIKETHIS]
>
>* [(Interface herdada) Excluir um relatório de dados de desempenho ou um arquivo de bulksheet do menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [(Nova interface do usuário) Gerenciar relatórios de exibição de dados da [!UICONTROL Portfolios] exibição](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)
>* [(Nova interface do usuário) Gerenciar relatórios de exibição de dados da [!UICONTROL Campaigns] exibição](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)
>* [(Nova interface do usuário) Gerenciar relatórios de exibição de dados da [!UICONTROL Ad Groups] exibição](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)
