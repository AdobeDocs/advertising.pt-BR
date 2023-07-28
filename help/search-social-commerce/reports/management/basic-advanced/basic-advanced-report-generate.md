---
title: Gerar um relatório básico ou avançado
description: Saiba como gerar um relatório básico ou avançado personalizado.
exl-id: cad5183c-cd21-439a-ab3e-033b2bb187ec
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Gerar um relatório básico ou avançado

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Report]**, mantenha o cursor sobre **[!UICONTROL Basic Reports]** ou **[!UICONTROL Advanced Reports]** e, em seguida, clique na guia [tipo de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Opcional) Na [!UICONTROL Report Settings] , altere o padrão [configurações de relatório](basic-advanced-report-settings.md):

   1. (Opcional) Insira um nome personalizado para o relatório e para o modelo (se você salvar o relatório como um modelo).

   1. (Opcional) Para salvar as configurações do relatório como um modelo, marque a caixa de seleção ao lado de **[!UICONTROL Save as template]**.

   1. (Opcional) No **[!UICONTROL Basic Settings]** selecione um template de relatório existente para usar ou alterar as configurações básicas padrão do relatório.

   1. (Opcional) Clique no link **[!UICONTROL Columns tab]** e altere as colunas padrão no relatório.

      Por padrão, todos os dados monetários nos relatórios são mostrados no formato para dólares americanos (como 1.000,00). Para exibir o valor no formato de moeda correto (mas sem símbolos de moeda nos formatos CSV e TSV), adicione o &quot;[!UICONTROL Currency]&quot; ao relatório. Se o relatório incluir dados de contas com moedas diferentes, qualquer &quot;[!UICONTROL Total]&quot;os valores monetários são a soma de todos os números na coluna, independentemente da moeda.

   1. (Opcional; [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], e [!UICONTROL Label Classification Report] somente) Clique no botão **[!UICONTROL Classifications]** e limite os resultados do relatório para incluir apenas classificações de rótulo específicas.

   1. (Opcional) Clique no link **[!UICONTROL Advanced Filters]** e altere as opções avançadas padrão.

   1. (Opcional) Clique no link **[!UICONTROL Attribution]** e altere a regra de atribuição padrão.

   1. (Opcional) Clique no link **[!UICONTROL Scheduling and Delivery]** e altere as opções padrão de agendamento e delivery.

1. (Opcional quando disponível) Para visualizar as primeiras 50 linhas do relatório, clique em **[!UICONTROL Preview]**. Quando terminar, clique em **[!UICONTROL Back]** para retornar à página de configurações do relatório.

   >[!NOTE]
   >
   >O botão Visualizar está disponível para todos os relatórios básicos e avançados, exceto para [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report], e [!UICONTROL Transaction Report].

1. Clique em **[!UICONTROL Create]**.

Se você não tiver especificado um agendamento de relatório, o relatório será executado imediatamente; caso contrário, será executado de acordo com o agendamento especificado. O nome do relatório é adicionado à variável [[!UICONTROL Latest Reports] exibir](/help/search-social-commerce/reports/report-about.md). Se você tiver salvo o relatório como um modelo, ele também será adicionado à variável [[!UICONTROL Templates] exibir](/help/search-social-commerce/reports/report-about.md). Quando o relatório é concluído, o arquivo é disponibilizado para abrir ou salvar; os modelos são disponibilizados imediatamente.

Se você tiver inserido algum endereço de email para notificação, cada destinatário receberá uma notificação quando o trabalho de relatório for concluído ou falhar, com base no [configurações de notificação definidas](/help/search-social-commerce/notifications/notification-edit.md) para relatórios.

>[!MORELIKETHIS]
>
>* [Sobre relatórios básicos e avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Configurações básicas e avançadas de relatório](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Colunas de relatório para relatórios básicos e avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Excluir relatórios](/help/search-social-commerce/reports/management/report-delete.md)
