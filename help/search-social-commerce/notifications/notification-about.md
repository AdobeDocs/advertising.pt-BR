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

*Recurso Beta*

Você pode definir suas configurações de notificação para assinar ou cancelar a assinatura de diferentes tipos de alertas. Você pode exibir as notificações de qualquer uma das seguintes maneiras:

* No [!UICONTROL Notifications] que está disponível no menu principal em ![Notificação](/help/search-social-commerce/assets/notifications-panel.png "Notificação").

* De [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* De um [!UICONTROL Notification Center] aplicativo web, que é aberto [!UICONTROL Notification Center] em uma janela separada fora do Search, Social e Commerce.

  O aplicativo é carregado mais rápido do que a versão normal do navegador e é atualizado automaticamente. Você pode instalar o aplicativo e gerenciá-lo usando o gerenciador de aplicativos do navegador.

* Das notificações por push para o navegador.

  Quando você ativa as notificações por push, elas são exibidas de acordo com as convenções de notificação do navegador.

Você pode exibir suas notificações, marcá-las como lidas ou não lidas e excluir notificações.

## Tipos de notificação

* **[!UICONTROL Notices]**: avisos de liberação, tempo de inatividade e outros avisos de gerenciamento de alterações.

* **[!UICONTROL Recommendations]**: oportunidades identificadas para melhorar o desempenho, implementar práticas recomendadas etc.

* **[!UICONTROL Warnings]**: problemas que exigem atenção, mas não são essenciais para a otimização ou o gerenciamento.

* **[!UICONTROL Issues]**: problemas críticos que exigem atenção imediata. As notificações de erro de autorização de conta estão incluídas.

## Categorias de notificação

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: notificações de que um [operação de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) foi concluído ou falhou.

   * **[!UICONTROL Manager Account Missing]**: as notificações de que os recursos de Pesquisa, Social e Comércio não têm as credenciais para uma [conta do gerenciador de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md), que são necessários para a configuração correta de funções críticas.

   * **[!UICONTROL UI Actions]**: notificações de que seus trabalhos executados em segundo plano foram concluídos ou falharam. Os tipos de trabalho incluem [tarefas de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), tarefas de edição em massa na tabela de dados ou usando a barra de ferramentas, tarefas de atribuição de entidade ou outras ações na interface do usuário (como sincronizar com redes de anúncios, colar linhas ou renomear entidades). As atribuições de entidade incluem atribuir ou desatribuir um [valor de classificação de etiqueta](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) a qualquer entidade, atribuindo uma campanha a um portfólio e atribuindo ou desatribuindo uma restrição a um portfólio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: usado para um beta fechado

      * **[!UICONTROL File Upload to Cloud Storage]**: usado para um beta fechado

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: notificações de que o Search, Social e Commerce não conseguiram acessar um [conta de rede de publicidade](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) devido a credenciais inválidas ou a um token de autorização inválido ou expirado.

      * **[!UICONTROL Account Missing]**: as notificações de que os recursos de Pesquisa, Social e Comércio não têm as credenciais para uma [conta de rede de publicidade](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**: notificações que o Search, Social e Commerce não conseguiram sincronizar com um [conta do gerenciador de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md) devido a credenciais inválidas ou a um token de autorização inválido ou expirado.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: notificações que [um [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) foi concluído ou falhou.

   * **[!UICONTROL Custom Alerts]**: notificações que [instâncias de alerta](/help/search-social-commerce/alerts/alert-about.md) foram acionados para um modelo de alerta.

   * **[!UICONTROL Reports]**: notificações de que um [relatório personalizado ou agendado](/help/search-social-commerce/reports/report-about.md) foi concluído ou falhou.

   * **[!UICONTROL Spreadsheet Feeds]**: notificações de que um [feed de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) foi concluído ou falhou.

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
>* [Ativar e desativar notificações por push de [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Instale e desinstale o [!UICONTROL Notification Center] aplicativo web](notification-app-install-uninstall.md)
