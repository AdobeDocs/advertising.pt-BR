---
title: Criar um [!DNL Excel] modelo para um feed de relatório de planilha
description: Saiba como criar modelos de planilha especialmente formatados.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Criar um [!DNL Excel] modelo para um feed de relatório de planilha

*Somente para relatórios básicos e relatórios de precisão de modelo*

Para criar feeds de planilha, você deve primeiro criar feeds especialmente formatados [!DNL Microsoft® Excel] modelos de planilhas usando modelos de relatório regulares. Opcionalmente, é possível personalizar a variável [!DNL Excel] planilha para incluir colunas e gráficos adicionais.

1. Entrada **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, gere o tipo de relatório desejado usando um [!UICONTROL Date Aggregation] unidade de &quot;[!UICONTROL Daily]&quot; e com todos os outros parâmetros de dados desejados, salve o relatório como um template.

   >[!NOTE]
   >
   > * Você pode criar feeds de planilha para [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], e [!UICONTROL Forecast Accuracy] relatórios. Se você usar o [!UICONTROL Ad Group Report], limite o número de grupos de anúncios incluídos para obter resultados mais rápidos.
   > * A variável [!UICONTROL Date Range] a unidade definida no modelo não é usada. Você definirá as datas para as quais atualizará os dados ao configurar o feed de planilha posteriormente.


1. Depois que o relatório for gerado, acesse **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** e exporte uma versão TSV ou XLS da saída do relatório para um arquivo.

1. Entrada [!DNL Excel], crie um modelo personalizado para o relatório:

   1. Abra o arquivo de relatório em [!DNL Excel].

   1. Prepare a pasta de trabalho:

      1. Exclua as linhas principais que mostram os parâmetros do relatório. Para arquivos XLS, exclua também o &quot;[!UICONTROL Total]linha &quot;. Opcionalmente, é possível excluir algumas linhas de dados, mas manter a) a linha de cabeçalho de dados com todas as colunas na ordem original e b) pelo menos uma linha de dados. Não adicione dados manualmente.

         >[!NOTE]
         >
         > A coluna final deve incluir valores diferentes de zero.

      2. Classifique os dados pela data de início em ordem crescente (da mais antiga para a mais recente).

      3. Altere o nome da guia da planilha de &quot;[!UICONTROL Sheet1]&quot; para &quot;[!UICONTROL RAW].&quot;

         Esse nome de guia específico permite que os dados sejam atualizados.

      4. (Opcional) Adicione colunas personalizadas à direita das colunas do modelo de relatório, conforme necessário.
   1. (Opcional) Em uma planilha separada, crie uma tabela dinâmica. Depois de concluir, clique com o botão direito do mouse em qualquer célula da tabela dinâmica e selecione **[!UICONTROL Pivot Table Options]**, clique no link **[!UICONTROL Data]** e selecione **[!UICONTROL Refresh data when opening the file]**.

   1. Salvar o arquivo como um [!DNL Excel] planilha em formato .XLSX.


>[!MORELIKETHIS]
>
>* [Sobre feeds de relatório de planilhas](spreadsheet-feed-about.md)
>* [Criar um feed de relatório de planilha](spreadsheet-feed-create.md)
>* [Editar configurações do feed de relatório de planilha](spreadsheet-feed-edit.md)
>* [Configurações do feed de relatório de planilha](spreadsheet-feed-settings.md)
>* [Exibir ou salvar um arquivo de feed de relatório de planilha](spreadsheet-feed-view-or-save.md)
>* [Atualizar manualmente os feeds de relatório da planilha](spreadsheet-feed-refresh.md)
>* [Excluir feeds de relatório de planilha](spreadsheet-feed-delete.md)

