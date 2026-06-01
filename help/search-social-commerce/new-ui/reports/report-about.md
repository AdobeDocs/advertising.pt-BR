---
title: (Nova interface do usuário) Sobre relatórios agendados
description: Saiba mais sobre os relatórios de desempenho agendados, incluindo os diferentes tipos de relatórios disponíveis e como automatizar relatórios.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
  - id: c916feea-e212-4773-b673-4daed287b8a3
  - id: adcb1be7-7ed0-464d-a8d4-c905c9d47742
  - id: ff99aaef-142d-4c93-a88c-011e979e3843
  - id: fa0141e5-dc99-4fbd-9c0e-40aff66de606
  - id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
source-git-commit: bd4246ec79684167254a153d2f3d0b917a493096
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 0%

---

# (Nova interface do usuário) Sobre relatórios agendados

Os relatórios de desempenho agendados permitem rastrear e gerenciar o desempenho de portfólios, redes de anúncios e entidades de conta de rede de anúncios em um nível tão granular quanto você deseja. A maioria dos relatórios fornece visibilidade completa de como os anúncios em cada canal de marketing contribuem para a taxa de conversão geral.

Os dados de um relatório são compilados dinamicamente cada vez que você o executa. Opcionalmente, é possível gerar um novo relatório a partir de um relatório existente. Os parâmetros de relatório disponíveis variam de acordo com o tipo de relatório. Para a maioria dos relatórios, você tem a opção de visualizar as primeiras 50 linhas em vez de gerar o relatório inteiro. Ao gerar um relatório, você pode enviar uma notificação com links de download para um ou mais endereços de email quando um relatório for concluído, e os destinatários podem [gerenciar as notificações em [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

Todos os relatórios concluídos estão disponíveis na seção [!UICONTROL Latest Reports] da exibição [!UICONTROL Reports], e você pode exibi-los em formato de tabela na janela do navegador ou abri-los ou baixá-los como arquivos.

## Categorias de relatório disponíveis

As seguintes categorias de relatório estão disponíveis na exibição [!UICONTROL Scheduled Reports]. Talvez você não tenha acesso a todos eles; os relatórios disponíveis e os dados gerados por eles são determinados pela sua função e como a conta do cliente é configurada.

| Categoria do relatório | Descrição |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Relatórios básicos](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), que estão disponíveis para todos os usuários, mostram o custo real e dados de cliques de portfólios, contas de rede de anúncios, contas de rede de anúncios específicas, campanhas, grupos de anúncios, anúncios, palavras-chave, grupos de produtos, classificações de etiquetas e valores de etiquetas, restrições de unidade de oferta e restrições de rede. Elas se baseiam nos cliques faturados pelas redes de anúncios aplicáveis e, opcionalmente, podem incluir dados de conversão ou qualquer outra métrica criada. |
| [!UICONTROL Advanced Reports] | [Relatórios avançados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) fornecem insight adicionais para a sua configuração de publicidade, ajudando você a identificar onde se beneficiaria ao alterar a sua definição geográfica de metas ou as configurações de rede. Elas também podem ajudar a validar os dados de conversão nas visualizações e relatórios de gerenciamento de campanhas e portfólios em relação aos dados de rastreamento de conversão interna do anunciante. |
| [!UICONTROL Assist Reports] | [Relatórios de assistência](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) fornecem informações sobre os caminhos de conversão de todas as palavras-chave e anúncios de um anunciante. Eles usam dados capturados por meio do serviço de rastreamento de conversão da Adobe Advertising e podem ser gerados apenas para anunciantes com o serviço. |
| [!UICONTROL Specialty Reports] | [Os relatórios de especialidades](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) consistem em dados coletados pelas redes de publicidade (e não pelo rastreamento Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Os relatórios de precisão do modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indicam a precisão dos modelos de custo e receita usados para otimizar ofertas, orçamentos de campanha e metas de estratégia de oferta para um portfólio. |

## Automação de relatórios

Programe relatórios personalizados para serem gerados automaticamente de uma ou das duas formas a seguir:

* Gera relatórios automaticamente todos os dias ou em um dia específico da semana ou mês, usando [modelos de relatório](/help/search-social-commerce/new-ui/reports/report-templates-manage.md).

  Opcionalmente, é possível configurar a [entrega FTP de relatórios básicos e avançados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) que usam um modelo.

* Continue atualizando seus modelos de planilha personalizados com dados de desempenho diário usando os [feeds de planilha](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## A visualização [!UICONTROL Scheduled Reports]

A exibição [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] permite criar e gerenciar relatórios, modelos e feeds de planilha. A visualização inclui duas guias:

* A guia **[!UICONTROL Latest Reports]** lista todos os relatórios disponíveis que foram solicitados nos últimos sete dias, exceto aqueles que foram excluídos manualmente, com o relatório mais recente no topo por padrão. As informações mostradas para cada relatório incluem o agendamento pelo qual ele é executado (quando aplicável), as datas de início e término para as quais os dados foram ou serão gerados e o status do relatório (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Os links ao lado de cada relatório permitem exibi-lo no navegador da Web, abri-lo ou salvá-lo como um arquivo de [!DNL Microsoft Excel] pasta de trabalho (XLS) ou valores separados por tabulação (TSV). Alguns tipos de relatório também podem ser salvos como [!UICONTROL Excel] pastas de trabalho com uma planilha separada para cada campanha aplicável.

  Nesta guia, você também pode criar um novo relatório (que, opcionalmente, pode ser usado como modelo), criar um novo relatório com base nas configurações de um relatório existente, cancelar os relatórios em andamento disponíveis para você ao excluí-los e excluir qualquer relatório concluído disponível para você. Os relatórios com mais de sete dias são excluídos automaticamente.

* A guia **[!UICONTROL Templates]** lista todos os modelos de relatórios básicos e avançados disponíveis para você, incluindo informações sobre os cronogramas associados a eles. Por padrão, o modelo mais recente está na parte superior.

  Nessa guia, você cria um novo modelo, edita qualquer modelo criado (incluindo adição, alteração ou remoção de seu agendamento), gera um relatório a partir de um modelo e exclui qualquer modelo disponível.

## Como usar relatórios

| Finalidade | Relatório |
| ---- | ---- |
| Monitoramento de desempenho | <ul><li>[O [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[O [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[O [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[O [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[O [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[O [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solução de problemas de desempenho e análise de tendências | <ul><li>[O [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[O [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[O [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[O [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[O [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) e [O [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualquer relatório básico que compara duas janelas de tempo usando o recurso &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificação das oportunidades de crescimento dos negócios | <ul><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [As tarefas de configuração iniciais para relatórios](initial-setup.md)
>* [Os dados usados para os relatórios](data-used-for-reports.md)
>* [Gerenciar relatórios agendados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
