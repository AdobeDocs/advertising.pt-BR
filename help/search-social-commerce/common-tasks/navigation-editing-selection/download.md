---
title: Baixar dados de uma visualização de gerenciamento de campanha
description: Saiba como baixar dados da maioria das exibições de gerenciamento de campanha.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Baixar dados de uma visualização de gerenciamento de campanha

É possível baixar dados da [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] exibições, exceto para [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], e [!UICONTROL Extensions] exibições. Você pode baixar:

* Um relatório no [!DNL XLSM] (habilitado para macro [!DNL Microsoft® Excel] planilha). Se você selecionar linhas específicas na exibição, o relatório incluirá uma linha para cada linha selecionada. Se você não selecionar nenhuma linha, uma linha será criada para cada linha na exibição.

* Um arquivo de bulksheet no formato TXT que inclui todas as entidades secundárias relevantes. Se você selecionar linhas para entidades em várias redes de anúncios, um arquivo será criado para cada rede de anúncios relevante. Se você não selecionar nenhuma linha, um arquivo será criado para cada rede de publicidade representada na exibição. Os arquivos de bulksheet gerados para diferentes redes de anúncios incluem diferentes colunas de dados.

   Se você gerar dados para várias campanhas e os dados combinados consistirem em mais de 500.000 linhas, os dados serão divididos por campanha em dois ou mais arquivos, conforme necessário, denominados `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`e assim por diante.

   Cada arquivo de bulksheet no [!UICONTROL Downloads] também está listado no [!UICONTROL Bulksheets] exibição. Quando o arquivo for criado, você receberá uma notificação por email com um link do qual poderá baixar o arquivo; dependendo da quantidade de dados que estiver sendo compilada, a notificação poderá levar vários minutos ou mais. Se, no entanto, a geração do arquivo falhar, um arquivo de erro será listado na exibição Bulksheets e você receberá uma notificação por email com um link para o arquivo de erro. Excluir um arquivo de bulksheet de uma das opções [!UICONTROL Download] painel ou o [!UICONTROL Bulksheets] A guia a exclui de ambos os locais.

1. (Opcional) Selecione linhas individuais para incluir no arquivo.

   Caso contrário, todos os dados na visualização serão incluídos.

1. À direita da barra de ferramentas, clique em ![Download de Relatório](/help/search-social-commerce/assets/download.png "Download de Relatório").

1. Clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar") **[!UICONTROL Create]**, opcionalmente adicione o nome do arquivo e clique em **[!UICONTROL Report]** ou **[!UICONTROL Bulksheet]**.

1. (Opcional) Quando o trabalho de relatório estiver concluído, clique em ![Download de Relatório](/help/search-social-commerce/assets/download.png "Download de Relatório") para exibir o [!UICONTROL Available Reports] e, em seguida, baixe ou exclua o relatório:

   * Para abrir ou salvar o arquivo de acordo com o procedimento normal do navegador, clique em ![Baixar planilha](/help/search-social-commerce/assets/download-spreadsheet.png "Baixar planilha").

      Para obter mais informações sobre o procedimento do navegador, consulte a ajuda online do navegador.

   * Para excluir o arquivo, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

>[!MORELIKETHIS]
>
>[Exclua um relatório de dados de desempenho ou arquivo de bulksheet da [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
