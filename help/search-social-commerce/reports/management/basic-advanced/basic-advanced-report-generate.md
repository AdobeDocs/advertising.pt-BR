---
title: Gerar um relatório básico ou avançado
description: Saiba como gerar um relatório básico ou avançado personalizado.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Gerar um relatório básico ou avançado

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** ou **[!UICONTROL Advanced Reports]** e clique no [tipo de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Opcional) Na janela [!UICONTROL Report Settings], altere as [configurações de relatório](basic-advanced-report-settings.md) padrão:

   1. (Opcional) Insira um nome personalizado para o relatório e para o modelo (se você salvar o relatório como um modelo).

   1. (Opcional) Para salvar as configurações do relatório como um modelo, marque a caixa de seleção ao lado de **[!UICONTROL Save as template]**.

   1. (Opcional) Na guia **[!UICONTROL Basic Settings]**, selecione um modelo de relatório existente para usar ou alterar as configurações básicas padrão do relatório.

   1. (Opcional) Clique em **[!UICONTROL Columns tab]** e altere as colunas padrão no relatório.

      Por padrão, todos os dados monetários nos relatórios são mostrados no formato para dólares americanos (como 1.000,00). Para exibir o valor no formato de moeda correto (mas sem símbolos de moeda nos formatos CSV e TSV), adicione a coluna &quot;[!UICONTROL Currency]&quot; ao relatório. Se o relatório incluir dados para contas com moedas diferentes, qualquer valor monetário &quot;[!UICONTROL Total]&quot; será a soma de todos os números na coluna, independentemente da moeda.

   1. (Opcional; somente [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] e [!UICONTROL Label Classification Report]) Clique na guia **[!UICONTROL Classifications]** e limite os resultados do relatório para incluir apenas classificações de rótulo específicas.

   1. (Opcional) Clique na guia **[!UICONTROL Advanced Filters]** e altere as opções avançadas padrão.

   1. (Opcional) Clique na guia **[!UICONTROL Attribution]** e altere a regra de atribuição padrão.

   1. (Opcional) Clique na guia **[!UICONTROL Scheduling and Delivery]** e altere as opções padrão de agendamento e entrega.

1. (Opcional quando disponível) Para visualizar as primeiras 50 linhas do relatório, clique em **[!UICONTROL Preview]**. Quando terminar, clique em **[!UICONTROL Back]** para retornar à página de configurações do relatório.

   >[!NOTE]
   >
   >O botão Visualizar está disponível para todos os relatórios básicos e avançados, exceto para os [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] e [!UICONTROL Transaction Report].

1. Clique em **[!UICONTROL Create]**.

Se você não tiver especificado um agendamento de relatório, o relatório será executado imediatamente; caso contrário, será executado de acordo com o agendamento especificado. O nome do relatório foi adicionado ao modo de exibição [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Se você tiver salvo o relatório como modelo, ele também será adicionado à exibição [[!UICONTROL Templates] ](/help/search-social-commerce/reports/report-about.md). Quando o relatório é concluído, o arquivo é disponibilizado para abrir ou salvar; os modelos são disponibilizados imediatamente.

Se você tiver inserido endereços de email para notificação, cada destinatário receberá uma notificação quando o trabalho de relatório for concluído ou falhar, com base nas [configurações de notificação definidas pelo usuário](/help/search-social-commerce/notifications/notification-edit.md) para relatórios.

>[!MORELIKETHIS]
>
>* [Sobre relatórios básicos e avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Configurações básicas e avançadas de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Colunas de relatório para relatórios básicos e avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Excluir relatórios](/help/search-social-commerce/reports/management/report-delete.md)
