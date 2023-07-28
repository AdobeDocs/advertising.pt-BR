---
title: Sobre relatórios
description: Saiba mais sobre os relatórios de desempenho, incluindo os diferentes tipos de relatórios disponíveis e como automatizar relatórios.
exl-id: a945b255-a9b0-42f4-85ea-44416c837fc0
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Sobre relatórios

Os relatórios de desempenho permitem rastrear e gerenciar o desempenho de portfólios, redes de anúncios e entidades de conta de rede de anúncios em um nível tão granular quanto você desejar. A maioria dos relatórios fornece visibilidade completa de como os anúncios em cada canal de marketing contribuem para a taxa de conversão geral.

Os dados de um relatório são compilados dinamicamente cada vez que você o executa. Opcionalmente, é possível gerar um novo relatório a partir de um relatório existente. Os parâmetros de relatório disponíveis variam de acordo com o tipo de relatório. Para a maioria dos relatórios, você tem a opção de visualizar as primeiras 50 linhas em vez de gerar o relatório inteiro. Ao gerar um relatório, você pode enviar uma notificação com links de download para um ou mais endereços de email quando um relatório for concluído, e os recipients podem [gerenciar as notificações no [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Todos os relatórios concluídos estão disponíveis no [!UICONTROL Latest Reports] seção do [!UICONTROL Reports] e você pode exibi-los em formato de tabela na janela do navegador ou abri-los ou baixá-los como arquivos.

## Categorias de relatório disponíveis

As seguintes categorias de relatório estão disponíveis no [!UICONTROL Reports] exibição. Talvez você não tenha acesso a todos eles; os relatórios disponíveis e os dados gerados por eles são determinados pela sua função e como a conta do cliente é configurada.

| Categoria do relatório | Descrição |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Relatórios básicos](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), que estão disponíveis para todos os usuários, mostram o custo real e dados de cliques de portfólios, contas de rede de anúncios, contas específicas de rede de anúncios, campanhas, grupos de anúncios, anúncios, palavras-chave, grupos de produtos, classificações de etiquetas e valores de etiquetas, restrições de unidade de oferta e restrições de rede. Elas se baseiam nos cliques faturados pelas redes de anúncios aplicáveis e, opcionalmente, podem incluir dados de conversão ou qualquer outra métrica criada. |
| [!UICONTROL Advanced Reports] | [Relatórios avançados](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) forneça insights adicionais sobre a sua configuração de publicidade, ajudando você a identificar onde se beneficiaria ao alterar a segmentação geográfica ou as configurações de rede. Elas também podem ajudar a validar os dados de conversão nas visualizações e relatórios de gerenciamento de campanhas e portfólios em relação aos dados de rastreamento de conversão interna do anunciante. |
| [!UICONTROL Assist Reports] | [Relatórios de assistência](/help/search-social-commerce/reports/management/assist/assist-report-about.md) forneça insights sobre os caminhos de conversão para todas as palavras-chave e anúncios de um anunciante. Eles usam dados capturados por meio do serviço de rastreamento de conversão de Adobe Advertising e podem ser gerados apenas para anunciantes com o serviço. |
| [!UICONTROL Specialty Reports] | [Relatórios de especialidade](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) consistem em dados coletados pelas redes de anúncios (em vez de pelo rastreamento de Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Relatórios de precisão do modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indique a precisão dos modelos de custo e receita usados para otimizar ofertas. |

## Automação de relatórios

Programe relatórios personalizados para serem gerados automaticamente de uma ou das duas formas a seguir:

* Gerar relatórios automaticamente todos os dias ou em um dia específico da semana ou mês, usando [modelos de relatório](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Opcionalmente, é possível configurar [Entrega FTP de relatórios básicos e avançados](/help/search-social-commerce/reports/automation/ftp-reports.md) que usam um template.

* Continue atualizando seus modelos de planilha personalizados com dados de desempenho diário usando [feeds de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## As visualizações de Relatórios

A variável [!UICONTROL Reports] visualizações em [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] permite criar e gerenciar relatórios, modelos e feeds de planilha. A visualização inclui duas guias:

* A variável **[!UICONTROL Latest Reports]** A guia lista todos os relatórios disponíveis que foram solicitados nos últimos sete dias, exceto aqueles que foram excluídos manualmente, com o relatório mais recente no topo por padrão. As informações mostradas para cada relatório incluem o agendamento pelo qual ele é executado (quando aplicável), as datas inicial e final para as quais os dados foram ou serão gerados e o status do relatório (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Os links ao lado de cada relatório permitem exibi-lo no navegador da Web, abri-lo ou salvá-lo como um [!DNL Microsoft Excel] arquivo de pasta de trabalho (XLS) ou valores separados por tabulação (TSV); alguns tipos de relatório também podem ser salvos como [!UICONTROL Excel] pastas de trabalho com uma planilha separada para cada campanha aplicável.

  Nesta guia, você também pode criar um novo relatório (que, opcionalmente, pode ser usado como modelo), criar um novo relatório com base nas configurações de um relatório existente, cancelar os relatórios em andamento disponíveis para você ao excluí-los e excluir qualquer relatório concluído disponível para você. Os relatórios com mais de sete dias são excluídos automaticamente.

* A variável **[!UICONTROL Templates]** A guia lista todos os modelos de relatório básicos e avançados salvos disponíveis, incluindo informações sobre os cronogramas associados a eles. Por padrão, o modelo mais recente está na parte superior.

  Nessa guia, você cria um novo modelo, edita qualquer modelo criado (incluindo adição, alteração ou remoção de seu agendamento), gera um relatório a partir de um modelo e exclui qualquer modelo disponível.

## Como usar relatórios

| Finalidade | Relatório |
| ---- | ---- |
| Monitoramento de desempenho | <ul><li>[A variável [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[A variável [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[A variável [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[A variável [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[A variável [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[A variável [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solução de problemas de desempenho e análise de tendências | <ul><li>[A variável [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[A variável [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[A variável [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[A variável [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[A variável [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) e [A variável [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualquer relatório básico que compara duas janelas de tempo usando o &quot;[!UICONTROL Compare with]recurso &quot;</li></ul> |
| Identificação das oportunidades de crescimento dos negócios | <ul><li>(Anunciantes somente com rastreamento de conversão de Adobe Advertising) [A variável [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Anunciantes somente com rastreamento de conversão de Adobe Advertising) [A variável [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados no Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Anunciantes somente com rastreamento de conversão de Adobe Advertising) [A variável [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados no Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Dados usados para relatórios](data-used-for-reports.md)
>* [Tarefas de configuração inicial para relatórios](initial-setup.md)
>* [Gerar um relatório básico ou avançado](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Gerar um relatório de precisão de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Gerar um relatório de especialidade](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Gerar um relatório de assistência](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
