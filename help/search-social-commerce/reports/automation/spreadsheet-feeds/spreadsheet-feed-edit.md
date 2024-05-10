---
title: Editar configurações do feed de relatório de planilha
description: Saiba como editar as configurações para feeds de planilha.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Editar configurações do feed de relatório de planilha

*Somente para relatórios básicos e relatórios de precisão de modelo*

É possível alterar qual modelo de relatório, [!DNL Microsoft Excel] e outros parâmetros são usados para um feed de planilha.

>[!NOTE]
>
> Se você editar as colunas no modelo de relatório ou usar um modelo de relatório novo ou atualizado, será necessário atualizar o [!DNL Excel] modelo de acordo e carregue-o novamente.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Opcional) Para atualizar o modelo de relatório ou a variável [!DNL Excel] modelo usado para o feed de planilha:

   * (Opcional) Para usar um modelo de relatório diferente ou atualizado para o feed, [criar um novo [!DNL Excel] modelo para o modelo de relatório](spreadsheet-feed-create-excel-template.md).

     Será necessário fazer upload do modelo de relatório e do novo [!DNL Excel] arquivo na próxima etapa.

   * (Opcional) Para simplesmente adicionar colunas personalizadas à [!DNL Excel] insira as colunas à direita das colunas do modelo de relatório e salve o arquivo como um [!DNL Excel] planilha em formato .XLSX. Será necessário fazer upload do novo [!DNL Excel] arquivo na próxima etapa.

1. Altere as configurações do feed de planilha:

   * No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Ao lado do nome do feed da planilha, clique em ![Botão Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Botão Exibir/editar configurações").

   * No [!UICONTROL Edit Spreadsheet Feed] , altere o [configurações do feed de planilha](spreadsheet-feed-settings.md).

   * Clique em **[!UICONTROL Submit]**.

   * (Opcional) Depois que o feed for [!UICONTROL Update Status] é *[!UICONTROL Finished]*, clique em **[!UICONTROL XLSX]** ao lado do feed e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

     >[!NOTE]
     >
     > Se o modelo de relatório associado ao feed for excluído posteriormente, o feed também será excluído.

     Os feeds de planilha são atualizados automaticamente às 08:00 cada dia no fuso horário do anunciante. Se o modelo de relatório incluir endereços para qualquer destinatário de email, esses endereços receberão notificações quando a planilha for atualizada.

>[!MORELIKETHIS]
>
>* [Sobre feeds de relatório de planilha](spreadsheet-feed-about.md)
>* [Criar um feed de relatório de planilha](spreadsheet-feed-create.md)
>* [Criar um [!DNL Excel] modelo para um feed de relatório de planilha](spreadsheet-feed-create-excel-template.md)
>* [Editar configurações do feed de relatório de planilha](spreadsheet-feed-edit.md)
>* [Configurações do feed de relatório de planilha](spreadsheet-feed-settings.md)
>* [Exibir ou salvar um arquivo de feed de relatório de planilha](spreadsheet-feed-view-or-save.md)
>* [Atualizar manualmente os feeds de relatório da planilha](spreadsheet-feed-refresh.md)
