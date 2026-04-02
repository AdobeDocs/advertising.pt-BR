---
title: As tarefas de configuração iniciais para relatórios
description: Saiba como disponibilizar métricas em relatórios e como automatizar relatórios.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
TQID: https://experienceleague.adobe.com/N50b-O0oFBV6ZMXcFx8gRvLs3M1hN696d43VGlgkg44
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# As tarefas de configuração iniciais para relatórios

Os novos usuários devem executar as seguintes tarefas de configuração inicial:

* Disponibilize as métricas de conversão que o Adobe Advertising está rastreando para um anunciante [para relatórios e outras exibições](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) e, opcionalmente, [renomeie qualquer uma das métricas de conversão]&#x200B;(/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md que são exibidas nos títulos das colunas para facilitar a leitura.

  As propriedades de transações não estão disponíveis para relatórios, a menos que você as disponibilize especificamente.

  Posteriormente, se você começar a rastrear uma nova métrica de conversão, deverá repetir essa tarefa.

* (Opcional) Automatizar a geração de relatórios:

   * Se você quiser gerar dados de relatório regularmente para um incremento de tempo específico, como [!UICONTROL Campaign Report] para a semana passada ou os últimos 30 dias, poderá configurar [modelos de relatório](/help/search-social-commerce/reports/automation/templates/template-about.md) e agendá-los para serem executados diariamente ou em um dia específico da semana ou do mês. Cada vez que o relatório é agendado para execução, um novo relatório é gerado. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando o relatório é concluído, com base nas [configurações de notificação definidas no [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se você deseja exibir dados atualizados do relatório diário em uma planilha formatada personalizada, com ou sem tabelas dinâmicas e quaisquer colunas adicionais que você precise para realizar outros cálculos, poderá configurar um [feed de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) diário. Os feeds de planilha são atualizados diariamente com os dados de desempenho mais recentes e continuam a reter os dados das datas anteriores. Para configurar os feeds de planilha, você deve primeiro criar um modelo de planilha personalizado em [!DNL Microsoft Excel]. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando um arquivo de feed estiver disponível, com base nas [configurações de notificação definidas no [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se quiser receber relatórios básicos e avançados em um local FTP, configure o [acesso FTP aos relatórios básicos e avançados](/help/search-social-commerce/reports/automation/ftp-reports.md) solicitando uma conta FTP e configurando modelos de relatório com uma convenção de nomenclatura específica.

>[!MORELIKETHIS]
>
>* [Sobre relatórios](report-about.md)
>* [Dados usados para relatórios](data-used-for-reports.md)
