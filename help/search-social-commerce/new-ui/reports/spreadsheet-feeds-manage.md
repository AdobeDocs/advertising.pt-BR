---
title: (Nova interface do usuário) Gerenciar feeds de relatório de planilha
description: Saiba como criar, configurar, atualizar, visualizar e excluir feeds de relatório de planilha que fornecem dados diários de desempenho em uma planilha formatada personalizada.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: b0691683d8b9a02169920645c4220c3737cb9bd9
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%
---
# (Nova interface do usuário) Gerenciar feeds de relatório de planilha

*Somente para relatórios básicos e relatórios de precisão de modelo*

<!-- Update link to notifications once available -->

Os feeds de planilha fornecem dados de desempenho diário para todos os relatórios básicos e relatórios de precisão de modelo em um formato de planilha personalizado em [!DNL Microsoft Excel] XLSX. Você pode configurar feeds de planilha usando [!DNL Excel] modelos de planilha especialmente formatados que você cria a partir de modelos de relatório comuns. A cada dia, a planilha é atualizada automaticamente em um horário especificado com dados novos e brutos agregados diariamente. Os dados brutos preenchem quaisquer colunas e gráficos incluídos no modelo da planilha. Quando um arquivo de feed de planilha estiver disponível, ou se a geração do arquivo falhar, cada destinatário de email especificado nas configurações do feed de planilha receberá uma notificação, com base nas [configurações de notificação para relatórios](/help/search-social-commerce/notifications/notification-about.md) definidas pelo usuário.

Você pode configurar o feed para atualizar até os últimos 90 dias de dados, e todos os dados existentes anteriores permanecem, continuando a acumular.

A exibição [!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds] lista todos os feeds de planilha que você criou. Nesta exibição, você pode criar, editar, atualizar manualmente ou excluir feeds de planilha, exibir as configurações do modelo de relatório associado e copiar dados de linha selecionados.

## Ações disponíveis

* [Criar um modelo  [!DNL Excel]  para um feed de relatório de planilha](#spreadsheet-feed-create-excel-template)

* [Criar um feed de relatório de planilha](#spreadsheet-feed-create)

* [Editar configurações do feed de relatório de planilha](#spreadsheet-feed-edit)

* [Exibir as configurações do modelo de relatório associado](#spreadsheet-feed-view-template)

* [Exibir ou salvar um arquivo de feed de relatório de planilha](#spreadsheet-feed-view-or-save)

* [Atualizar manualmente os feeds de relatório da planilha](#spreadsheet-feed-refresh)

* [Excluir feeds de relatório de planilha](#spreadsheet-feed-delete)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

## Criar um modelo [!DNL Excel] para um feed de relatório de planilha {#spreadsheet-feed-create-excel-template}

Para criar feeds de planilha, você deve primeiro criar modelos de planilha do [!DNL Microsoft Excel] especialmente formatados usando os [modelos de relatório](report-templates-manage.md) comuns. Como opção, você pode personalizar a planilha [!DNL Excel] para incluir colunas e gráficos adicionais.

1. Em **[!UICONTROL Reports]>[!UICONTROL Reports]**, gere o tipo de relatório desejado usando uma unidade [!UICONTROL Date Aggregation] de &quot;[!UICONTROL Daily]&quot; e com todos os outros parâmetros de dados desejados, salvando o relatório como modelo.

   >[!NOTE]
   >
   > * Você pode criar feeds de planilha para os relatórios [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] e [!UICONTROL Forecast Accuracy]. Se você usa o [!UICONTROL Ad Group Report], limite o número de grupos de anúncios incluídos para obter resultados mais rápidos.
   > * A unidade [!UICONTROL Date Range] definida no modelo não é usada. Você definirá as datas para as quais atualizará os dados ao configurar o feed de planilha posteriormente.

1. Depois que o relatório for gerado, vá para **[!UICONTROL Reports]>[!UICONTROL Reports]** e exporte uma versão TSV ou XLS da saída do relatório para um arquivo.

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

      Os feeds de planilha são atualizados automaticamente todos os dias no [!UICONTROL Schedule Time] configurado. Os endereços especificados na configuração [!UICONTROL Email Recipients] do feed recebem notificações quando a planilha é atualizada.

## Editar configurações do feed de relatório de planilha {#spreadsheet-feed-edit}

>[!NOTE]
>
> Se você editar as colunas no modelo de relatório ou usar um modelo de relatório novo ou atualizado, será necessário atualizar o modelo [!DNL Excel] de acordo e carregá-lo novamente.

1. (Opcional) Para atualizar o modelo de relatório ou o modelo [!DNL Excel] usado para o feed de planilhas:

   * (Opcional) Para usar um modelo de relatório diferente ou atualizado para o feed, [crie um novo [!DNL Excel] modelo para o modelo de relatório](#spreadsheet-feed-create-excel-template).

     Você selecionará o modelo de relatório e carregará o novo arquivo [!DNL Excel] nas próximas etapas.

   * (Opcional) Para simplesmente adicionar colunas personalizadas ao modelo [!DNL Excel], insira as colunas à direita das colunas do modelo de relatório e salve o arquivo como uma planilha [!DNL Excel] no formato .XLSX. Você precisará carregar o novo arquivo [!DNL Excel] na próxima etapa.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Altere as configurações do feed de planilha:

   1. Marque a caixa de seleção ao lado do nome do feed da planilha.

   1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

   1. Na caixa de diálogo **[!UICONTROL Edit Spreadsheet Feed]**, altere as [configurações do feed de planilha](#spreadsheet-feed-settings).

   1. Clique em **[!UICONTROL Submit]**.

   1. (Opcional) Assim que o [!UICONTROL Update Status] do feed for *[!UICONTROL Finished]*, clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

   >[!NOTE]
   >
   > Se o modelo de relatório associado ao feed for excluído posteriormente, o feed também será excluído.

   Os feeds de planilha são atualizados automaticamente todos os dias no [!UICONTROL Schedule Time] configurado no fuso horário do anunciante. Os endereços especificados na configuração [!UICONTROL Email Recipients] do feed recebem notificações quando a planilha é atualizada.

## Configurações do feed de relatório de planilha {#spreadsheet-feed-settings}

| Campo | Descrição |
|---|---|
| [!UICONTROL Feed Name] | Um nome para o feed de planilhas, com no máximo 120 caracteres. |
| [!UICONTROL Report Template] | O modelo de relatório que especifica os dados de relatório necessários; selecione aquele usado para criar o modelo [!DNL Excel]. Todos os modelos de relatório básicos estão listados.<br><br><b>Observação:</b> se você alterar o modelo de relatório usado para o relatório ou atualizar as colunas no modelo, deverá criar e carregar um novo modelo [!DNL Excel]. |
| [!UICONTROL Excel Template] | O modelo [!DNL Excel] especialmente formatado que você criou no formato .XLSX, que é aplicado aos dados especificados no modelo de relatório. Clique em <b>[!UICONTROL Choose file]</b> para localizar o arquivo a ser carregado. |
| [!UICONTROL Back Fill From] | A data inicial para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. Insira um valor de 1 a 90 que seja maior que [!UICONTROL Back Fill Until]; o padrão é sete (7) dias.<br><br>Por exemplo, se o valor for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] que começam com 1º de março serão atualizados (até a data final especificada pelo parâmetro [!UICONTROL Back Fill Until]). As linhas de dados existentes para datas anteriores a 1º de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Back Fill Until] | A data final para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. Insira um valor de 1 a 90 que seja menor que [!UICONTROL Back Fill From]. O valor padrão é um (1) dia.<br><br>Por exemplo, se esse valor for 1 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados até 6 de março (e começando com a data de início especificada pelo parâmetro [!UICONTROL Back Fill From]). Se esse valor for 1, o parâmetro [!UICONTROL Back Fill From] for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados de 1º de março a 6 de março. Em ambos os exemplos, as linhas de dados existentes para datas após 6 de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Email Recipients] | Endereços de email para enviar notificações sempre que o feed de planilha for atualizado. Por padrão, o endereço da conta de usuário é inserido. Para especificar vários endereços, separe-os com vírgulas, espaços ou novas linhas. |
| [!UICONTROL Schedule Time] | A hora em que o feed da planilha é atualizado todos os dias no fuso horário do anunciante. Selecione um horário nas opções disponíveis. O padrão para novos feeds de planilha é 10h. |
| [!UICONTROL Email Notification] | O que incluir nas notificações por email para os endereços especificados:<ul><li><i>[!UICONTROL Attach Feed (Max 10MB)]</i> — Para enviar uma cópia do relatório concluído no formato XLSX. Se o arquivo tiver mais de 10 MB, a notificação não incluirá um anexo.</li><li><i>[!UICONTROL Notification Only]</i> (o padrão) — Para enviar apenas uma notificação da conclusão ou falha do relatório, com um link para o relatório.</li></ul> |

## Exibir as configurações do modelo de relatório associado {#spreadsheet-feed-view-template}

O ícone de engrenagem **[!UICONTROL Template Settings]** abre uma duplicata do modelo de relatório associado ao feed. Abrir a duplicata não salva um novo modelo ou altera o modelo associado do feed.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Clique no ícone de engrenagem **[!UICONTROL Template Settings]** ao lado do nome do modelo de relatório associado.

1. Revise as configurações do relatório.

1. Clique em **[!UICONTROL Cancel]** quando terminar. Se for solicitado que você descarte a instalação, clique em **[!UICONTROL Discard]**.

Para alterar o modelo de relatório original, siga o [procedimento de edição do modelo de relatório](report-templates-manage.md#template-edit). Para usar um modelo diferente para o feed, [edite as configurações do feed de planilha](#spreadsheet-feed-edit) e selecione o modelo.

## Exibir ou salvar um arquivo de feed de relatório de planilha {#spreadsheet-feed-view-or-save}

Você pode visualizar qualquer feed de planilha gerado ou salvá-lo em um arquivo. Os arquivos de feed de planilha estão no formato XLSX [!DNL Microsoft Excel].

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

## Atualizar manualmente os feeds de relatório da planilha {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Os feeds de planilha são atualizados automaticamente todos os dias no [!UICONTROL Schedule Time] configurado no fuso horário do anunciante.

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

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.
