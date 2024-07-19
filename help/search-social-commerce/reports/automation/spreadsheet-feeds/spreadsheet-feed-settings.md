---
title: Configurações do feed de relatório de planilha
description: Saiba mais sobre as configurações para feeds de planilha.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Configurações do feed de relatório de planilha

| Campo | Descrição |
|---|---|
| [!UICONTROL Feed Name] | Um nome para o feed da planilha. |
| [!UICONTROL Report Template] | O modelo de relatório que especifica os dados de relatório necessários; selecione aquele usado para criar o modelo [!DNL Excel]. Todos os modelos básicos de relatório são listados.<br><br><b>Observação:</b> se você alterar o modelo de relatório usado para o relatório ou atualizar as colunas no modelo, deverá criar e carregar um novo modelo [!DNL Excel]. |
| [!UICONTROL Excel Template] | O modelo [!DNL Excel] especialmente formatado que você criou no formato .XLSX, que é aplicado aos dados especificados no modelo de relatório. Especifique o arquivo a ser carregado inserindo o caminho completo e o nome do arquivo ou clicando em <b>[!UICONTROL Browse]</b> para localizar o arquivo no dispositivo ou na rede. |
| [!UICONTROL Back Fill From] | A data inicial para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. Insira um valor de até 90 dias; o padrão é sete (7) dias.<br><br>Por exemplo, se o valor for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] que começam com 1º de março serão atualizados (até a data final especificada pelo parâmetro [!UICONTROL Back Fill Until]). As linhas de dados existentes para datas anteriores a 1º de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Back Fill Until] | A data final para a qual os dados existentes na guia [!UICONTROL RAW] são atualizados, representada por um número de dias no passado. O valor padrão é um (1) dia.<br><br>Por exemplo, se esse valor for 1 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados até 6 de março (e começando com a data de início especificada pelo parâmetro [!UICONTROL Back Fill From]). Se esse valor for 1, o parâmetro [!UICONTROL Back Fill Until] for 7 e hoje for 7 de março, os dados existentes na guia [!UICONTROL RAW] serão atualizados de 1º de março a 6 de março. Em ambos os exemplos, as linhas de dados existentes para datas após 6 de março não são excluídas, mas não são atualizadas. |
| [!UICONTROL Email Recipients] | Endereços de email nos quais enviar notificações sempre que o relatório for atualizado ou sempre que o relatório for executado quando o modelo incluir um agendamento. Por padrão, o endereço da conta de usuário é inserido. Para especificar vários endereços, separe-os com vírgulas, espaços ou novas linhas. |
| [!UICONTROL Schedule Time] | A hora em que os feeds de planilha são atualizados: às 08:00 ou a qualquer hora entre 10:00 e 23:00 no fuso horário do anunciante. O padrão para novos feeds de planilha é 10h.<br><br><b>Observação:</b> por motivos de desempenho, você não pode atualizar os feeds de planilha às 9:00, quando outros relatórios forem gerados. |
| [!UICONTROL Email Notification] | (Quando Destinatários de email são especificados) O que incluir nas notificações por email para qualquer endereço especificado:<ul><li><i>Anexar feed</i> — Para enviar uma cópia do relatório concluído no formato XLSX. Se o arquivo tiver mais de 10 MB, a notificação não incluirá um anexo.</li><li><i>Somente notificação</i> (o padrão) — Para enviar apenas uma notificação da conclusão ou falha do relatório, com um link para o relatório.</li></ul> |

>[!MORELIKETHIS]
>
>* [Sobre feeds de relatório de planilha](spreadsheet-feed-about.md)
>* [Criar um feed de relatório de planilha](spreadsheet-feed-create.md)
>* [Criar um [!DNL Excel] modelo para um feed de relatório de planilha](spreadsheet-feed-create-excel-template.md)
>* [Editar configurações do feed de relatório da planilha](spreadsheet-feed-edit.md)
>* [Exibir ou salvar um arquivo de feed de relatório de planilha](spreadsheet-feed-view-or-save.md)
>* [Atualizar manualmente os feeds de relatório da planilha](spreadsheet-feed-refresh.md)
>* [Excluir feeds de relatório de planilha](spreadsheet-feed-delete.md)
