---
title: As tarefas de configuração iniciais para relatórios
description: Saiba como disponibilizar métricas em relatórios e como automatizar relatórios.
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# As tarefas de configuração iniciais para relatórios

Os novos usuários devem executar as seguintes tarefas de configuração inicial:

* Criar as métricas de conversão que o Adobe Advertising está rastreando para um anunciante [disponível para relatórios e outras visualizações](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)e, opcionalmente [renomear qualquer uma das métricas de conversão](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md que são exibidos nos cabeçalhos da coluna para facilitar a leitura.

  As propriedades de transações não estão disponíveis para relatórios, a menos que você as disponibilize especificamente.

  Posteriormente, se você começar a rastrear uma nova métrica de conversão, será necessário repetir essa tarefa.

* (Opcional) Automatizar a geração de relatórios:

   * Se você quiser gerar dados de relatório regularmente para um incremento de tempo específico, como um [!UICONTROL Campaign Report] para a última semana ou os últimos 30 dias, é possível configurar [modelos de relatório](/help/search-social-commerce/reports/automation/templates/template-about.md) e programe-as para serem executadas diariamente ou em um dia específico da semana ou do mês. Cada vez que o relatório é agendado para execução, um novo relatório é gerado. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando o relatório é concluído, com base na variável [configurações de notificação definidas em [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se quiser exibir dados atualizados do relatório diário em uma planilha formatada personalizada, com ou sem tabelas dinâmicas e quaisquer colunas adicionais necessárias para executar cálculos adicionais, você poderá configurar um relatório diário [feed de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Os feeds de planilha são atualizados diariamente com os dados de desempenho mais recentes e continuam a reter os dados das datas anteriores. Para configurar feeds de planilha, primeiro crie um modelo de planilha personalizado em [!DNL Microsoft Excel]. Você tem a opção de notificar os endereços de email de usuários específicos do Search, Social e Commerce quando um arquivo de feed estiver disponível, com base no [configurações de notificação definidas em [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Se quiser receber relatórios básicos e avançados em um local FTP, configure [Acesso FTP a relatórios básicos e avançados](/help/search-social-commerce/reports/automation/ftp-reports.md) solicitando uma conta FTP e configurando modelos de relatório usando uma convenção de nomenclatura específica.

>[!MORELIKETHIS]
>
>* [Sobre relatórios](report-about.md)
>* [Dados usados para relatórios](data-used-for-reports.md)
