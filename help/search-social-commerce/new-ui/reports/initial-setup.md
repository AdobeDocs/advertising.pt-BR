---
title: (Nova interface) As tarefas de configuração iniciais para relatórios
description: Saiba como disponibilizar métricas em relatórios e como automatizar relatórios.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# (Nova interface) As tarefas de configuração iniciais para relatórios

Os novos usuários devem executar as seguintes tarefas de configuração inicial:

* Disponibilize as métricas de conversão que o Adobe Advertising está rastreando para um anunciante para relatórios e outras exibições e, opcionalmente, renomeie qualquer uma das métricas de conversão exibidas nos cabeçalhos da coluna para facilitar a leitura. Consulte &quot;[Gerenciar as métricas de conversão de um anunciante](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md).&quot;

  As propriedades de transações não estão disponíveis para relatórios, a menos que você as disponibilize especificamente.

  Posteriormente, se você começar a rastrear uma nova métrica de conversão, deverá repetir essa tarefa.

* (Opcional) Automatizar a geração de relatórios:

   * Se você quiser gerar dados de relatório regularmente para um incremento de tempo específico, como [!UICONTROL Campaign Report] para a semana passada ou os últimos 30 dias, poderá configurar [modelos de relatório](report-templates-manage.md) e agendá-los para serem executados diariamente ou em um dia específico da semana ou do mês. Cada vez que o relatório é agendado para execução, um novo relatório é gerado. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando o relatório é concluído, com base nas [configurações de notificação definidas em [!UICONTROL Notification Center]][Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md).

   * Se você deseja exibir dados atualizados do relatório diário em uma planilha formatada personalizada, com ou sem tabelas dinâmicas e quaisquer colunas adicionais que você precise para realizar outros cálculos, poderá configurar um [feed de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) diário. Os feeds de planilha são atualizados diariamente com os dados de desempenho mais recentes e continuam a reter os dados das datas anteriores. Para configurar os feeds de planilha, você deve primeiro criar um modelo de planilha personalizado em [!DNL Microsoft Excel]. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando um arquivo de feed estiver disponível, com base nas [configurações de notificação definidas no [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

   * Se quiser receber relatórios básicos e avançados em um local FTP, configure o [acesso FTP aos relatórios básicos e avançados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) solicitando uma conta FTP e configurando modelos de relatório com uma convenção de nomenclatura específica.

>[!MORELIKETHIS]
>
>* [Sobre relatórios](report-about.md)
>* [Dados usados para relatórios](data-used-for-reports.md)
