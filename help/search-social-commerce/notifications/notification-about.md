---
title: Sobre notificações
description: Saiba mais sobre notificações, incluindo os diferentes tipos e categorias.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Sobre notificações

*Recurso do Beta*

Você pode definir suas configurações de notificação para assinar ou cancelar a assinatura de diferentes tipos de alertas. Você pode exibir as notificações de qualquer uma das seguintes maneiras:

* No painel [!UICONTROL Notifications], que está disponível no menu principal em ![Notificações](/help/search-social-commerce/assets/notifications-panel.png "Notificações").

* De [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Em um aplicativo Web [!UICONTROL Notification Center], que abre [!UICONTROL Notification Center] em uma janela separada fora do Search, Social e Commerce.

  O aplicativo é carregado mais rápido do que a versão normal do navegador e é atualizado automaticamente. Você pode instalar o aplicativo e gerenciá-lo usando o gerenciador de aplicativos do navegador.

* Das notificações por push para o navegador.

  Quando você ativa as notificações por push, elas são exibidas de acordo com as convenções de notificação do navegador.

Você pode exibir suas notificações, marcá-las como lidas ou não lidas e excluir notificações.

## Tipos de notificação

* **[!UICONTROL Notices]**: avisos de liberação, tempo de inatividade e outros avisos de gerenciamento de alterações.

* **[!UICONTROL Recommendations]**: Oportunidades identificadas para melhorar o desempenho, implementar práticas recomendadas etc.

* **[!UICONTROL Warnings]**: problemas que requerem atenção, mas não são críticos para otimização ou gerenciamento.

* **[!UICONTROL Issues]**: Problemas críticos que exigem atenção imediata. As notificações de erro de autorização de conta estão incluídas.

## Categorias de notificação

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: Notificações de que uma [operação de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) foi concluída ou falhou.

   * **[!UICONTROL Manager Account Missing]**: as notificações de que Search, Social e Commerce não têm as credenciais de uma [conta de gerente de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md), que são necessárias para a configuração correta de funções críticas.

   * **[!UICONTROL UI Actions]**: Notificações de que seus trabalhos executados em segundo plano foram concluídos ou falharam. Os tipos de trabalho incluem [trabalhos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), trabalhos de edição em massa na tabela de dados ou usando a barra de ferramentas, trabalhos de atribuição de entidade ou outras ações na interface do usuário (como sincronizar com redes de anúncios, colar linhas ou renomear entidades). As atribuições de entidade incluem atribuir ou desatribuir um [valor de classificação de etiqueta](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) para qualquer entidade, atribuir uma campanha a um portfólio e atribuir ou desatribuir uma restrição a um portfólio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: usado para um beta fechado

      * **[!UICONTROL File Upload to Cloud Storage]**: usado para um beta fechado

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: as notificações de que a Pesquisa, o Social e a Commerce não conseguiram acessar uma [conta de rede de anúncios](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) devido a credenciais inválidas ou um token de autorização inválido ou expirado.

      * **[!UICONTROL Account Missing]**: as credenciais de uma [conta de rede de anúncios](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) estão ausentes nas notificações de que Search, Social e Commerce.

      * **[!UICONTROL Manager Account Auth Error]**: Notificações de que a Pesquisa, o Social e o Commerce não puderam ser sincronizados com uma [conta de gerente de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md) devido a credenciais inválidas ou um token de autorização inválido ou expirado.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Notificações de que [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) foi concluído ou falhou.

   * **[!UICONTROL Custom Alerts]**: Notificações de que [instâncias de alerta](/help/search-social-commerce/alerts/alert-about.md) foram acionadas para um modelo de alerta.

   * **[!UICONTROL Reports]**: Notificações de que um [relatório personalizado ou agendado](/help/search-social-commerce/reports/report-about.md) foi concluído ou falhou.

   * **[!UICONTROL Spreadsheet Feeds]**: Notificações de que um [feed de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) foi concluído ou falhou.

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [Exibir suas notificações](notification-view.md)
>* [Marcar uma notificação como lida ou não lida](notification-mark-read-unread.md)
>* [Excluir uma notificação](notification-delete.md)
>* [Editar suas configurações de notificação](notification-edit.md)
>* [Habilitar e desabilitar notificações por push de [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Instalar e desinstalar o [!UICONTROL Notification Center] aplicativo Web](notification-app-install-uninstall.md)
