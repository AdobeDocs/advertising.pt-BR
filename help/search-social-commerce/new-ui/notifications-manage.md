---
title: (Nova interface do usuário) Gerenciar notificações
description: Saiba como visualizar, configurar e gerenciar notificações de Pesquisa, Redes sociais e Commerce, incluindo notificações por push e o aplicativo web da Central de notificações.
feature: Search Notifications
source-git-commit: 2d218abb121a750ea3d75a68ebaf6d0b0b306a09
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar notificações

*recurso do Beta*

Você pode definir suas configurações de notificação para assinar ou cancelar a assinatura de diferentes tipos de alertas. Você pode exibir as notificações de qualquer uma das seguintes maneiras:

* No painel [!UICONTROL Notifications], que está disponível no canto superior direito em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações"). No painel, você pode filtrar a lista, editar suas configurações de notificação ou abrir [!UICONTROL Notification Center].

* De [!UICONTROL Notification Center], que abre em uma janela separada fora do Search, Social e Commerce. Para abrir [!UICONTROL Notification Center] no painel [!UICONTROL Notifications], clique em **[!UICONTROL View All]**.

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

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: Notificações de que uma [operação de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) foi concluída ou falhou.<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**: as notificações de que a Pesquisa, o Social e o Commerce não têm as credenciais de uma [conta de gerente de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md), que são necessárias para a configuração correta de funções críticas.<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**: Notificações de que seus trabalhos executados em segundo plano foram concluídos ou falharam. Os tipos de trabalho incluem [trabalhos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->, trabalhos de edição em massa na tabela de dados ou usando a barra de ferramentas, trabalhos de atribuição de entidade ou outras ações na interface do usuário (como sincronizar com redes de anúncios, colar linhas ou renomear entidades). As atribuições de entidade incluem atribuir ou desatribuir um [valor de classificação de etiqueta](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md) a qualquer entidade, atribuir uma campanha a um portfólio e [atribuir ou desatribuir uma restrição de oferta a uma entidade](/help/search-social-commerce/new-ui/goals/constraints-manage.md).

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: Notificações de que um arquivo de dados da conta foi carregado, ou de falha no carregamento de dados da conta, via [carregamento manual de dados da conta](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**: Notificações de que um arquivo de dados da conta foi carregado, ou de falha no carregamento de dados da conta, via [carregamento de dados da conta para um  [!DNL Amazon] [!DNL S3] bucket](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: as notificações de que a Pesquisa, o Social e a Commerce não conseguiram acessar uma [conta de rede de anúncios](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) devido a credenciais inválidas ou um token de autorização inválido ou expirado.

      * **[!UICONTROL Account Missing]**: as credenciais de uma [conta de rede de anúncios](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) estão ausentes nas notificações de que Search, Social e Commerce.

      * **[!UICONTROL Manager Account Auth Error]**: Notificações de que a Pesquisa, o Social e o Commerce não puderam ser sincronizados com uma [conta de gerente de rede de publicidade](/help/search-social-commerce/admin/manager-accounts.md) devido a credenciais inválidas ou um token de autorização inválido ou expirado.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Notificações de que [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) foi concluído ou falhou.

   * **[!UICONTROL Custom Alerts]**: Notificações de que [instâncias de alerta](/help/search-social-commerce/new-ui/alerts-manage.md) foram acionadas para um modelo de alerta.

   * **[!UICONTROL Spreadsheet Feeds]**: Notificações de que um [feed de planilha](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md) foi concluído ou falhou.

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**: Notificações de que um relatório de exibição de dados de uma exibição específica (como o conteúdo da tabela de dados na exibição [!UICONTROL Camapigns]) foi concluído ou falhou.

      * **[!UICONTROL Reports]**: Notificações de que um [relatório personalizado ou agendado](/help/search-social-commerce/new-ui/reports/management/report-manage.md) foi concluído ou falhou.

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**: notificações quando a otimização intradiária está desabilitada.

      * **[!UICONTROL Simulation Report]**: Notificações sobre [trabalhos de simulação](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: notificações no nível do anunciante sobre atribuição automática bem-sucedida e com falha de metas de conversão de campanha.

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: notificações no nível de portfólio sobre atribuição automática bem-sucedida e com falha de metas de conversão de campanha.

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: Notificações sobre [trabalhos de edição de portfólio em massa via bulksheets](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

         * **[!UICONTROL Portfolio Settings]**: Notificações sobre [alterações nas configurações do portfólio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Ações disponíveis

* [Exibir suas notificações](#notification-view)

* [Editar suas configurações de notificação](#notification-edit)

* [Marcar uma notificação como lida ou não lida](#notification-mark-read-unread)

* [Excluir uma notificação](#notification-delete)

* [Ativar e desativar notificações por push](#notification-push-enable-disable)

* [Instalar e desinstalar o aplicativo Web [!UICONTROL Notification Center]](#notification-app-install-uninstall)

## Exibir suas notificações {#notification-view}

Quando você é [inscrito nas notificações](#notification-edit) sobre erros de autenticação de conta, alertas personalizados disparados e [!UICONTROL Advertising Insights] gerados, é possível exibir suas notificações no painel [!UICONTROL Notifications] ou [!UICONTROL Notification Center].

### Exibir notificações no painel [!UICONTROL Notifications]

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. (Opcional) Siga qualquer um destes procedimentos:

   * Para exibir os detalhes de qualquer notificação, clique no nome da notificação.

     Em algumas notificações, a seção [!UICONTROL Action Recommended] pode incluir um link que abre uma exibição filtrada das entidades afetadas ou responsáveis.

   * Para marcar uma notificação como *lida* ou *não lida*, mantenha o cursor sobre o nome do alerta e clique em ![Marcar como Lida ou Não Lida](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como Lida ou Não Lida").

     As notificações marcadas como *lido* estão em um texto de cor mais clara, mas permanecem disponíveis até que você as exclua.

     ![Notificações Lidas e Não Lidas](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notificações Lidas e Não Lidas")

   * Para alterar as preferências de assinatura para o tipo de notificação, clique em ![Configurações](/help/search-social-commerce/assets/settings-nc.png "Configurações") ao lado da notificação, altere as configurações e clique em **[!UICONTROL Save]**.

   * Para excluir uma notificação, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da notificação.

   * Para abrir [!UICONTROL Notification Center], clique em **[!UICONTROL View All]**.

### Exibir notificações em [!UICONTROL Notification Center]

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. Clique em **[!UICONTROL View All]**.

1. (Opcional) Para filtrar suas notificações por tipo, clique em *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings] ou[!UICONTROL Issues]*.

1. (Opcional) Siga qualquer um destes procedimentos:

   * Para exibir os detalhes de qualquer notificação, clique no nome da notificação.

     Em algumas notificações, a seção [!UICONTROL Action Recommended] pode incluir um link que abre uma exibição filtrada das entidades afetadas ou responsáveis.

   * Para marcar uma notificação como *lida* ou *não lida*, mantenha o cursor sobre o nome do alerta e clique em ![Marcar como Lida ou Não Lida](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como Lida ou Não Lida").

     As notificações marcadas como *lido* estão em um texto de cor mais clara, mas permanecem disponíveis até que você as exclua.

   * Para alterar as preferências de assinatura para o tipo de notificação, clique em ![Configurações](/help/search-social-commerce/assets/settings-nc.png "Configurações") ao lado da notificação, altere as configurações e clique em **[!UICONTROL Save]**.

   * Para excluir uma notificação, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da notificação.

## Editar suas configurações de notificação {#notification-edit}

Opcionalmente, você pode assinar ou cancelar a assinatura de notificações da Web e por email sobre erros de autenticação de conta, todos os alertas personalizados acionados e a conclusão do [!UICONTROL Advertising Insights] gerado.

1. Abra as configurações de notificação de uma das seguintes maneiras:

   * Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações") para abrir o painel [!UICONTROL Notifications]. No canto superior direito, clique em ![Configurações](/help/search-social-commerce/assets/settings-nc.png "Configurações").

   * Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações"), clique em **[!UICONTROL View All]** para abrir o [!UICONTROL Notification Center] e, no menu esquerdo, clique em ![Configurações](/help/search-social-commerce/assets/settings-nc.png "Configurações").

1. Altere suas configurações para qualquer categoria de notificação listada acima:

   * Para assinar ou cancelar a assinatura de notificações, mova o controle deslizante na coluna [!UICONTROL Subscribe]:

      * Para cancelar a inscrição de todos os tipos de notificação, mova o controle deslizante para a esquerda (desativado).

      * Para assinar um ou mais tipos de notificação, mova o controle deslizante para a direita (ativado).

   * (Quando [!UICONTROL Subscribe] estiver habilitado) Para assinar notificações por email, marque a caixa de seleção na coluna **[!UICONTROL Email]**.

   * (Quando [!UICONTROL Subscribe] estiver desabilitado) Para assinar notificações da Web nas notificações do Search, Social, &amp; Commerce e por push se elas estiverem habilitadas para o navegador, marque a caixa de seleção na coluna **[!UICONTROL Web]**.

     As notificações da Web são entregues somente quando você [habilita notificações por push](#notification-push-enable-disable) para o navegador.

1. Clique em **[!UICONTROL Save]**.

## Marcar uma notificação como lida ou não lida {#notification-mark-read-unread}

Marcar uma notificação como *lida* ou *não lida* altera o número de notificações não lidas indicadas no link [!UICONTROL Notifications] na parte superior de cada página (como o ícone ![Notificações com contador de notificações não lidas](/help/search-social-commerce/assets/notifications-unread.png "Ícone Notificações com contador de notificações não lidas")).

As notificações marcadas como *lido* estão em um texto de cor mais clara, mas permanecem disponíveis até que você as exclua.

![Notificações Lidas e Não Lidas](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notificações Lidas e Não Lidas")

1. [Abra o painel Notificações ou a Central de Notificações](#notification-view).

1. Mantenha o cursor sobre o nome do alerta e clique em ![Marcar como Lido ou Não Lido](/help/search-social-commerce/assets/notifications-read-unread.png "Marcar como Lido ou Não Lido").

## Excluir uma notificação {#notification-delete}

### Excluir uma notificação no painel [!UICONTROL Notifications]

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. Clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da notificação.

### Excluir uma notificação em [!UICONTROL Notification Center]

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. Clique em **[!UICONTROL View All]**.

1. (Opcional) Para filtrar suas notificações por tipo, clique em *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]* ou *[!UICONTROL Issues]*.

1. Clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da notificação.

## Ativar e desativar notificações por push {#notification-push-enable-disable}

Você pode ativar notificações em Pesquisa, Social e Commerce, onde elas são exibidas de acordo com as convenções de notificação do navegador. Em dispositivos que usam o [!DNL Microsoft Windows], as notificações são exibidas na parte inferior direita da tela (bandeja do sistema). Em [!DNL Apple Mac] dispositivos, as notificações são exibidas no menu direito.

As notificações por push estão disponíveis nos seguintes navegadores:

* [!DNL Google Chrome] 40 e superior

* [!DNL Microsoft Edge] 17 e superior

* [!DNL Mozilla Firefox] 44 e superior

Você pode desativar as notificações por push de acordo com o procedimento padrão do navegador.

### Ativar notificações por push

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. Clique em **[!UICONTROL View All]**.

1. Na parte inferior direita, clique em ![Habilitar notificações por push](/help/search-social-commerce/assets/notifications-push.png "Habilitar notificações por push").

1. Na mensagem de confirmação, clique em **[!UICONTROL Enable]**.

1. Configure o navegador para permitir notificações de [!UICONTROL Notification Center] em `https://alert-center-ui-na.efrontier.com`.

   As configurações padrão de notificação variam de acordo com o navegador e você pode a) ser automaticamente apresentado à opção para permitir notificações de [!UICONTROL Notification Center] ou b) precisar gerenciar manualmente as configurações de notificação. Por exemplo, em [!DNL Microsoft Edge], você pode permitir notificações de [!UICONTROL Notification Center] na barra de ferramentas do navegador. Consulte as instruções na ajuda do navegador.

   ![Onde gerenciar configurações de notificação no Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Onde gerenciar configurações de notificação no Microsoft Edge")

1. Nas [configurações de notificação](#notification-edit), habilite as [!UICONTROL Web] notificações para os tipos de alertas que você deseja enviar.

### Desativar notificações por push

Remover notificações de `https://alert-center-ui-na.efrontier.com` no gerenciador de notificações do navegador. Por exemplo, em [!DNL Google Chrome], você pode remover ou bloquear notificações de sites especificados em `chrome://settings/content/notifications`.

Consulte as instruções na ajuda do navegador.

## Instalar e desinstalar o aplicativo Web [!UICONTROL Notification Center] {#notification-app-install-uninstall}

Você pode receber e gerenciar notificações fora do navegador instalando um aplicativo Web do [!UICONTROL Notification Center]. O aplicativo tem a mesma aparência e funcionalidade que [!UICONTROL Notification Center] no Search, Social e Commerce. O aplicativo está disponível para [!DNL Google Chrome] 40 e superior ou [!DNL Microsoft Edge] 17 e superior.

Depois de instalar o aplicativo [!UICONTROL Notification Center], ele é habilitado automaticamente no gerenciador de aplicativos do navegador e carregado como uma janela separada cujo layout é organizado dinamicamente com base no tamanho da janela. Você pode abrir e fechar o aplicativo a partir do gerenciador de aplicativos do navegador ou fixá-lo na barra de tarefas ou docking station do sistema operacional. O aplicativo é atualizado automaticamente.

![Ícone do Centro de notificações na barra de tarefas do Microsoft Windows](/help/search-social-commerce/assets/windows-taskbar.png "Ícone do Centro de notificações na barra de tarefas do Microsoft Windows")

Você pode desabilitar ou desinstalar o aplicativo no gerenciador de aplicativos do navegador. Para obter informações adicionais sobre como gerenciar aplicações web, consulte a ajuda do navegador.

### Instalar o aplicativo Web [!UICONTROL Notification Center] para [!DNL Google Chrome]

1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

1. Clique em **[!UICONTROL View All]**.

1. Na parte inferior direita, clique em ![Instalar aplicativo Web da Central de Notificações](/help/search-social-commerce/assets/notifications-install-app.png "Instalar aplicativo Web da Central de Notificações").

1. Na mensagem de confirmação, clique em **[!UICONTROL Add]**.

1. No aplicativo de instalação? clique em **[!UICONTROL Install]**.

### Instalar o aplicativo Web [!UICONTROL Notification Center] para [!DNL Microsoft Edge]

* A partir do Search, Social e Commerce:

   1. Na parte superior direita de qualquer página, clique em ![Notificações](/help/search-social-commerce/assets/notifications.png "Notificações").

   1. Clique em **[!UICONTROL View All]**.

   1. Na parte inferior direita, clique em ![Instalar aplicativo Web da Central de Notificações](/help/search-social-commerce/assets/notifications-install-app.png "Instalar aplicativo Web da Central de Notificações").

   1. Na mensagem de confirmação, clique em **[!UICONTROL Add]**.

   1. Na mensagem do aplicativo [!UICONTROL Install Notification Center], clique em **[!UICONTROL Install]**.

* No menu principal [!DNL Edge]:

   1. Na barra de ferramentas do navegador, clique em **...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. Na mensagem do aplicativo [!UICONTROL Install Notification Center], clique em **[!UICONTROL Install]**.

### Desinstalar o aplicativo Web [!UICONTROL Notification Center] para [!DNL Google Chrome]

* Em [!DNL Chrome], vá para `chrome://apps`, clique com o botão direito do mouse em **[!UICONTROL notification-center]** e clique em **[!UICONTROL Remove from Chrome]**.

### Desinstalar o aplicativo Web [!UICONTROL Notification Center] para [!DNL Microsoft Edge]

1. Na barra de ferramentas do navegador [!DNL Edge], clique em **...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. Alternativamente, vá para `edge://apps`.

1. Clique com o botão direito do mouse em **[!UICONTROL Notification Center]** e em **[!UICONTROL Uninstall]**.
