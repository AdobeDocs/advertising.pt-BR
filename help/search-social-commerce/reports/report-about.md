---
title: Sobre relatórios
description: Saiba mais sobre os relatórios de desempenho, incluindo os diferentes tipos de relatórios disponíveis e como automatizar relatórios.
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Sobre relatórios

Os relatórios de desempenho permitem rastrear e gerenciar o desempenho de portfólios, redes de anúncios e entidades de conta de rede de anúncios em um nível tão granular quanto você desejar. A maioria dos relatórios fornece visibilidade completa de como os anúncios em cada canal de marketing contribuem para a taxa de conversão geral.

Os dados de um relatório são compilados dinamicamente cada vez que você o executa. Opcionalmente, é possível gerar um novo relatório a partir de um relatório existente. Os parâmetros de relatório disponíveis variam de acordo com o tipo de relatório. Para a maioria dos relatórios, você tem a opção de visualizar as primeiras 50 linhas em vez de gerar o relatório inteiro. Ao gerar um relatório, você pode enviar uma notificação com links de download para um ou mais endereços de email quando um relatório for concluído, e os destinatários podem [gerenciar as notificações em [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Todos os relatórios concluídos estão disponíveis na seção [!UICONTROL Latest Reports] da exibição [!UICONTROL Reports], e você pode exibi-los em formato de tabela na janela do navegador ou abri-los ou baixá-los como arquivos.

## Categorias de relatório disponíveis

As seguintes categorias de relatório estão disponíveis na exibição [!UICONTROL Reports]. Talvez você não tenha acesso a todos eles; os relatórios disponíveis e os dados gerados por eles são determinados pela sua função e como a conta do cliente é configurada.

| Categoria do relatório | Descrição |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Relatórios básicos](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), que estão disponíveis para todos os usuários, mostram o custo real e dados de cliques de portfólios, contas de rede de anúncios, contas de rede de anúncios específicas, campanhas, grupos de anúncios, anúncios, palavras-chave, grupos de produtos, classificações de etiquetas e valores de etiquetas, restrições de unidade de oferta e restrições de rede. Elas se baseiam nos cliques faturados pelas redes de anúncios aplicáveis e, opcionalmente, podem incluir dados de conversão ou qualquer outra métrica criada. |
| [!UICONTROL Advanced Reports] | [Relatórios avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) fornecem informações adicionais sobre a configuração de seus anúncios, ajudando você a identificar onde se beneficiaria com a alteração do seu direcionamento geográfico ou das configurações de rede. Elas também podem ajudar a validar os dados de conversão nas visualizações e relatórios de gerenciamento de campanhas e portfólios em relação aos dados de rastreamento de conversão interna do anunciante. |
| [!UICONTROL Assist Reports] | [Relatórios de assistência](/help/search-social-commerce/reports/management/assist/assist-report-about.md) fornecem informações sobre os caminhos de conversão de todas as palavras-chave e anúncios de um anunciante. Eles usam dados capturados por meio do serviço de rastreamento de conversão de Adobe Advertising e podem ser gerados apenas para anunciantes com o serviço. |
| [!UICONTROL Specialty Reports] | [Os relatórios de especialidades](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) consistem em dados coletados pelas redes de publicidade (e não pelo rastreamento de Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Os relatórios de precisão do modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicam a precisão dos modelos de custo e receita usados para otimizar ofertas, orçamentos de campanha e metas de estratégia de oferta para um portfólio. |

## Automação de relatórios

Programe relatórios personalizados para serem gerados automaticamente de uma ou das duas formas a seguir:

* Gera relatórios automaticamente todos os dias ou em um dia específico da semana ou mês, usando [modelos de relatório](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Opcionalmente, é possível configurar a [entrega FTP de relatórios básicos e avançados](/help/search-social-commerce/reports/automation/ftp-reports.md) que usam um modelo.

* Continue atualizando seus modelos de planilha personalizados com dados de desempenho diário usando os [feeds de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## As visualizações de Relatórios

O modo de exibição [!UICONTROL Reports] em [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] permite criar e gerenciar relatórios, modelos e feeds de planilha. A visualização inclui duas guias:

* A guia **[!UICONTROL Latest Reports]** lista todos os relatórios disponíveis que foram solicitados nos últimos sete dias, exceto aqueles que foram excluídos manualmente, com o relatório mais recente no topo por padrão. As informações mostradas para cada relatório incluem o agendamento pelo qual ele é executado (quando aplicável), as datas de início e término para as quais os dados foram ou serão gerados e o status do relatório (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Os links ao lado de cada relatório permitem exibi-lo no navegador da Web, abri-lo ou salvá-lo como um arquivo de [!DNL Microsoft Excel] pasta de trabalho (XLS) ou valores separados por tabulação (TSV). Alguns tipos de relatório também podem ser salvos como [!UICONTROL Excel] pastas de trabalho com uma planilha separada para cada campanha aplicável.

  Nesta guia, você também pode criar um novo relatório (que, opcionalmente, pode ser usado como modelo), criar um novo relatório com base nas configurações de um relatório existente, cancelar os relatórios em andamento disponíveis para você ao excluí-los e excluir qualquer relatório concluído disponível para você. Os relatórios com mais de sete dias são excluídos automaticamente.

* A guia **[!UICONTROL Templates]** lista todos os modelos de relatórios básicos e avançados disponíveis para você, incluindo informações sobre os cronogramas associados a eles. Por padrão, o modelo mais recente está na parte superior.

  Nessa guia, você cria um novo modelo, edita qualquer modelo criado (incluindo adição, alteração ou remoção de seu agendamento), gera um relatório a partir de um modelo e exclui qualquer modelo disponível.

## Como usar relatórios

| Finalidade | Relatório |
| ---- | ---- |
| Monitoramento de desempenho | <ul><li>[O [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[O [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[O [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[O [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[O [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[O [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solução de problemas de desempenho e análise de tendências | <ul><li>[O [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[O [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[O [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[O [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[O [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) e [O [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualquer relatório básico que compara duas janelas de tempo usando o recurso &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificação das oportunidades de crescimento dos negócios | <ul><li>(Somente anunciantes com rastreamento de conversão de Adobe Advertising) [O [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Somente anunciantes com rastreamento de conversão de Adobe Advertising) [O [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Somente anunciantes com rastreamento de conversão de Adobe Advertising) [O [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Dados usados para relatórios](data-used-for-reports.md)
>* [Tarefas de configuração iniciais para relatórios](initial-setup.md)
>* [Gerar um relatório básico ou avançado](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Gerar um relatório de precisão de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Gerar um relatório de especialidade](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Gerar um relatório de assistência](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
