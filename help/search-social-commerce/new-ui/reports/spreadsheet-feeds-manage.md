---
title: (Nova interface do usuário) Gerenciar feeds de relatório de planilha
description: Saiba como criar, configurar, atualizar, visualizar e excluir feeds de relatório de planilha que fornecem dados diários de desempenho em uma planilha formatada personalizada.
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar feeds de relatório de planilha

*Somente para relatórios básicos e relatórios de precisão de modelo*

<!-- Update link to notifications once available -->

Os feeds de planilha fornecem dados de desempenho diário para todos os relatórios básicos e relatórios de precisão de modelo em um formato de planilha personalizado em [!DNL Microsoft Excel] XLSX. Você pode configurar feeds de planilha usando [!DNL Excel] modelos de planilha especialmente formatados que você cria a partir de modelos de relatório comuns. A cada dia, a planilha é atualizada automaticamente em um horário especificado com dados novos e brutos agregados diariamente. Os dados brutos preenchem quaisquer colunas e gráficos incluídos no modelo da planilha. Quando um arquivo de feed de planilha estiver disponível, ou se a geração do arquivo falhar, cada destinatário de email no modelo de relatório receberá uma notificação, com base nas [configurações de notificação para relatórios](/help/search-social-commerce/notifications/notification-about.md) definidas pelo usuário.

Você pode configurar o feed para atualizar até os últimos 90 dias de dados, e todos os dados existentes anteriores permanecem, continuando a acumular.

A exibição [!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds] lista todos os feeds de planilha que você criou. Nesta exibição, você pode criar feeds de planilha, atualizar manualmente um feed ou excluir um feed.

## Ações disponíveis

* [Criar um modelo  [!DNL Excel]  para um feed de relatório de planilha](#spreadsheet-feed-create-excel-template)

* [Criar um feed de relatório de planilha](#spreadsheet-feed-create)

* [Editar configurações do feed de relatório de planilha](#spreadsheet-feed-edit)

* [Exibir ou salvar um arquivo de feed de relatório de planilha](#spreadsheet-feed-view-or-save)

* [Atualizar manualmente os feeds de relatório da planilha](#spreadsheet-feed-refresh)

* [Excluir feeds de relatório de planilha](#spreadsheet-feed-delete)

## Criar um modelo [!DNL Excel] para um feed de relatório de planilha {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

Para criar feeds de planilha, você deve primeiro criar modelos de planilha do [!DNL Microsoft Excel] especialmente formatados usando modelos de relatório comuns. Como opção, você pode personalizar a planilha [!DNL Excel] para incluir colunas e gráficos adicionais.

1. Em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, gere o tipo de relatório desejado usando uma unidade [!UICONTROL Date Aggregation] de &quot;[!UICONTROL Daily]&quot; e com todos os outros parâmetros de dados desejados, salvando o relatório como modelo.

   >[!NOTE]
   >
   > * Você pode criar feeds de planilha para os relatórios [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] e [!UICONTROL Forecast Accuracy]. Se você usa o [!UICONTROL Ad Group Report], limite o número de grupos de anúncios incluídos para obter resultados mais rápidos.
   > * A unidade [!UICONTROL Date Range] definida no modelo não é usada. Você definirá as datas para as quais atualizará os dados ao configurar o feed de planilha posteriormente.

1. Depois que o relatório for gerado, vá para **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** e exporte uma versão TSV ou XLS da saída do relatório para um arquivo.

1. Em [!DNL Excel], crie um modelo personalizado para o relatório:

   1. Abra o arquivo de relatório em [!DNL Excel].

   1. Prepare a pasta de trabalho:

      1. Exclua as linhas principais que mostram os parâmetros do relatório. Para arquivos XLS, exclua também a linha &quot;[!UICONTROL Total]&quot;. Opcionalmente, é possível excluir algumas linhas de dados, mas manter a) a linha de cabeçalho de dados com todas as colunas na ordem original e b) pelo menos uma linha de dados. Não adicione dados manualmente.

         >[!NOTE]
         >
         > A coluna final deve incluir valores diferentes de zero.

      1. Classifique os dados pela data de início em ordem crescente (da mais antiga para a mais recente).

      1. Altere o nome da guia da planilha de &quot;[!UICONTROL Sheet1]&quot; para &quot;[!UICONTROL RAW].&quot;

         Esse nome de guia específico permite que os dados sejam atualizados.

      1. (Opcional) Adicione colunas personalizadas à direita das colunas do modelo de relatório, conforme necessário.

   1. (Opcional) Em uma planilha separada, crie uma tabela dinâmica. Quando terminar, clique com o botão direito do mouse em qualquer célula da tabela dinâmica e selecione **[!UICONTROL Pivot Table Options]**, clique na guia **[!UICONTROL Data]** e selecione **[!UICONTROL Refresh data when opening the file]**.

   1. Salve o arquivo como uma planilha [!DNL Excel] no formato .XLSX.

## Criar um feed de relatório de planilha {#spreadsheet-feed-create}

1. [Crie o  [!DNL Excel] modelo para popular com os dados do relatório](#spreadsheet-feed-create-excel-template).

1. Crie o feed de planilha:

   1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   1. No canto superior direito, clique em **[!UICONTROL Create Spreadsheet]**.

   1. Na caixa de diálogo **[!UICONTROL Create Spreadsheet Feed]**, especifique as [configurações do feed de planilha](#spreadsheet-feed-settings).

   1. Clique em **[!UICONTROL Submit]**.

   1. (Opcional) Assim que o [!UICONTROL Update Status] do feed for *[!UICONTROL Finished]*, clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

      >[!NOTE]
      >
      >Se o modelo de relatório associado ao feed for excluído posteriormente, o feed também será excluído.

      Os feeds de planilha são atualizados automaticamente todos os dias no [!UICONTROL Schedule Time] configurado. Se o modelo de relatório incluir endereços para qualquer destinatário de email, esses endereços receberão notificações quando a planilha for atualizada.

## Editar configurações do feed de relatório de planilha {#spreadsheet-feed-edit}

>[!NOTE]
>
> Se você editar as colunas no modelo de relatório ou usar um modelo de relatório novo ou atualizado, será necessário atualizar o modelo [!DNL Excel] de acordo e carregá-lo novamente.

1. (Opcional) Para atualizar o modelo de relatório ou o modelo [!DNL Excel] usado para o feed de planilhas:

   * (Opcional) Para usar um modelo de relatório diferente ou atualizado para o feed, [crie um novo [!DNL Excel] modelo para o modelo de relatório](#spreadsheet-feed-create-excel-template).

     Você fará o upload do modelo de relatório e do novo arquivo [!DNL Excel] nas próximas etapas.

   * (Opcional) Para simplesmente adicionar colunas personalizadas ao modelo [!DNL Excel], insira as colunas à direita das colunas do modelo de relatório e salve o arquivo como uma planilha [!DNL Excel] no formato .XLSX. Você precisará carregar o novo arquivo [!DNL Excel] na próxima etapa.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Altere as configurações do feed de planilha:

   1. Marque a caixa de seleção ao lado do nome do feed da planilha.

   1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

   1. Na caixa de diálogo [!UICONTROL Create Spreadsheet Feed]<!-- sic -->, altere as [configurações do feed de planilha](#spreadsheet-feed-settings).

   1. Clique em **[!UICONTROL Submit]**.

   1. (Opcional) Assim que o [!UICONTROL Update Status] do feed for *[!UICONTROL Finished]*, clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

   >[!NOTE]
   >
   > Se o modelo de relatório associado ao feed for excluído posteriormente, o feed também será excluído.

   Os feeds de planilha são atualizados automaticamente às 08:00, todos os dias, no fuso horário do anunciante. Se o modelo de relatório incluir endereços para qualquer destinatário de email, esses endereços receberão notificações quando a planilha for atualizada.

## Configurações do feed de relatório de planilha {#spreadsheet-feed-settings}

| Campo | Descrição |
|---|---|
| [!UICONTROL Feed Name] | Um nome para o feed da planilha. |
| [!UICONTROL Report Template] | O modelo de relatório que especifica os dados de relatório necessários; selecione aquele usado para criar o modelo [!DNL Excel]. Todos os modelos de relatório básicos estão listados.<br><br><b>Observação:</b> se você alterar o modelo de relatório usado para o relatório ou atualizar as colunas no modelo, deverá criar e carregar um novo modelo [!DNL Excel]. |
| [!UICONTROL Excel Template] | O modelo [!DNL Excel] especialmente formatado que você criou no formato .XLSX, que é aplicado aos dados especificados no modelo de relatório. Especifique o arquivo a ser carregado inserindo o caminho completo e o nome do arquivo ou clicando em <b>[!UICONTROL Browse]</b> para localizar o arquivo no dispositivo ou na rede. |
| [!UICONTROL Back Fill From] | A data inicial para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. Insira um valor de até 90 dias; o padrão é sete (7) dias.<br><br>Por exemplo, se o valor for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] que começam com 1º de março serão atualizados (até a data final especificada pelo parâmetro [!UICONTROL Back Fill Until]). As linhas de dados existentes para datas anteriores a 1º de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Back Fill Until] | A data final para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. O valor padrão é um (1) dia.<br><br>Por exemplo, se esse valor for 1 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados até 6 de março (e começando com a data de início especificada pelo parâmetro [!UICONTROL Back Fill From]). Se esse valor for 1, o parâmetro [!UICONTROL Back Fill Until] for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados de 1º de março a 6 de março. Em ambos os exemplos, as linhas de dados existentes para datas após 6 de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Email Recipients] | Endereços de email nos quais enviar notificações sempre que o relatório for atualizado ou sempre que o relatório for executado quando o modelo incluir um agendamento. Por padrão, o endereço da conta de usuário é inserido. Para especificar vários endereços, separe-os com vírgulas, espaços ou novas linhas. |
| [!UICONTROL Schedule Time] | A hora em que os feeds de planilha são atualizados: às 08:00 ou a qualquer hora entre 10:00 e 23:00 no fuso horário do anunciante. O padrão para novos feeds de planilha é 10:00.<br><br><b>Observação:</b> por motivos de desempenho, não é possível atualizar os feeds de planilha em 09:00, quando outros relatórios são gerados. |
| [!UICONTROL Email Notification] | (Quando Destinatários de email são especificados) O que incluir nas notificações por email para qualquer endereço especificado:<ul><li><i>[!UICONTROL Attach feed]</i> — Para enviar uma cópia do relatório concluído no formato XLSX. Se o arquivo tiver mais de 10 MB, a notificação não incluirá um anexo.</li><li><i>[!UICONTROL Notification Only]</i> (o padrão) — Para enviar apenas uma notificação da conclusão ou falha do relatório, com um link para o relatório.</li></ul> |

## Exibir ou salvar um arquivo de feed de relatório de planilha {#spreadsheet-feed-view-or-save}

Você pode visualizar qualquer feed de planilha gerado ou salvá-lo em um arquivo. Os arquivos de feed de planilha estão no formato XLSX [!DNL Microsoft Excel].

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

## Atualizar manualmente os feeds de relatório da planilha {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Os feeds de planilhas são atualizados automaticamente às 08:00, todos os dias, no fuso horário local.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Marque a caixa de seleção ao lado de cada feed que deseja atualizar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Run Spreadsheet]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

1. (Opcional) Assim que o [!UICONTROL Update Status] de um feed for *[!UICONTROL Finished]*, clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

## Excluir feeds de relatório de planilha {#spreadsheet-feed-delete}

>[!NOTE]
>
>Se o modelo de relatório associado a um feed for excluído, o feed será excluído automaticamente.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Marque a caixa de seleção ao lado de cada feed que deseja excluir.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.
