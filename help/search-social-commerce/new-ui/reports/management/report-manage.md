---
title: Gerenciar relatórios agendados
description: Saiba como gerenciar relatórios agendados.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Gerenciar relatórios agendados

Os relatórios de desempenho permitem rastrear e gerenciar o desempenho de portfólios, redes de anúncios e entidades de conta de rede de anúncios em um nível tão granular quanto você desejar. A maioria dos relatórios fornece visibilidade completa de como os anúncios em cada canal de marketing contribuem para a taxa de conversão geral.

Os dados de um relatório são compilados dinamicamente cada vez que você o executa. Opcionalmente, é possível gerar um novo relatório a partir de um relatório existente. Os parâmetros de relatório disponíveis variam de acordo com o tipo de relatório. Para a maioria dos relatórios, você tem a opção de visualizar as primeiras 50 linhas em vez de gerar o relatório inteiro. Ao gerar um relatório, você pode enviar uma notificação com links de download para um ou mais endereços de email quando um relatório for concluído, e os destinatários podem [gerenciar as notificações em [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Todos os relatórios concluídos estão disponíveis na seção [!UICONTROL Latest Reports] da exibição [!UICONTROL Reports], e você pode exibi-los em formato de tabela na janela do navegador ou abri-los ou baixá-los como arquivos.

## Categorias de relatório disponíveis

As seguintes categorias de relatório estão disponíveis na exibição [!UICONTROL Reports]. Talvez você não tenha acesso a todos eles; os relatórios disponíveis e os dados gerados por eles são determinados pela sua função e como a conta do cliente é configurada.

| Categoria do relatório | Descrição |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Relatórios básicos](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), que estão disponíveis para todos os usuários, mostram o custo real e dados de cliques de portfólios, contas de rede de anúncios, contas de rede de anúncios específicas, campanhas, grupos de anúncios, anúncios, palavras-chave, grupos de produtos, classificações de etiquetas e valores de etiquetas, restrições de unidade de oferta e restrições de rede. Elas se baseiam nos cliques faturados pelas redes de anúncios aplicáveis e, opcionalmente, podem incluir dados de conversão ou qualquer outra métrica criada. |
| [!UICONTROL Advanced Reports] | [Relatórios avançados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) fornecem insight adicionais para a sua configuração de publicidade, ajudando você a identificar onde se beneficiaria ao alterar a sua definição geográfica de metas ou as configurações de rede. Elas também podem ajudar a validar os dados de conversão nas visualizações e relatórios de gerenciamento de campanhas e portfólios em relação aos dados de rastreamento de conversão interna do anunciante. |
| [!UICONTROL Assist Reports] | [Relatórios de assistência](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) fornecem informações sobre os caminhos de conversão de todas as palavras-chave e anúncios de um anunciante. Eles usam dados capturados por meio do serviço de rastreamento de conversão da Adobe Advertising e podem ser gerados apenas para anunciantes com o serviço. |
| [!UICONTROL Specialty Reports] | [Os relatórios de especialidades](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) consistem em dados coletados pelas redes de publicidade (e não pelo rastreamento Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Os relatórios de precisão do modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indicam a precisão dos modelos de custo e receita usados para otimizar ofertas, orçamentos de campanha e metas de estratégia de oferta para um portfólio. |

## Automação de relatórios

Programe relatórios personalizados para serem gerados automaticamente de uma ou das duas formas a seguir:

* Gera relatórios automaticamente todos os dias ou em um dia específico da semana ou mês, usando [modelos de relatório](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Opcionalmente, é possível configurar a [entrega FTP de relatórios básicos e avançados](/help/search-social-commerce/new-ui/reports/ftp-reports.md) que usam um modelo.

* Continue atualizando seus modelos de planilha personalizados com dados de desempenho diário usando os [feeds de planilha](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## As [!UICONTROL Scheduled Reports] visualizações

As exibições [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] permitem criar e gerenciar relatórios e modelos de relatório:

* A guia **[!UICONTROL Latest Reports]** lista todos os relatórios disponíveis para você<!-- Doesn't seem to be true: that were requested in the last seven days -->, exceto aqueles que foram excluídos manualmente, com o relatório mais recente no topo por padrão. As informações mostradas para cada relatório incluem o agendamento pelo qual ele é executado (quando aplicável), as datas de início e término para as quais os dados foram ou serão gerados, quem criou o relatório e o status do relatório (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Os links ao lado de cada relatório permitem abri-lo ou salvá-lo como um arquivo de pasta de trabalho (XLS) do [!DNL Microsoft Excel], de valores separados por tabulação (TSV) ou CSV (valores separados por vírgula). Alguns tipos de relatório também podem ser salvos como [!UICONTROL Excel] pastas de trabalho com uma planilha separada para cada campanha aplicável.

  Nessa guia, também é possível criar um novo relatório (que, opcionalmente, pode ser usado como modelo), criar um novo relatório com base nas configurações de um relatório existente ou usar um modelo de relatório, cancelar os relatórios em andamento disponíveis para você ao excluí-los e excluir qualquer relatório concluído disponível para você.

* A guia **[!UICONTROL Templates]** lista todos os modelos de relatórios básicos e avançados disponíveis para você, incluindo informações sobre os cronogramas associados a eles. Por padrão, o modelo mais recente está na parte superior.

  Nessa guia, você cria um novo modelo, edita qualquer modelo criado (incluindo adição, alteração ou remoção de seu agendamento), gera um relatório a partir de um modelo e exclui qualquer modelo disponível.

## Como usar relatórios

| Finalidade | Relatório |
| ---- | ---- |
| Monitoramento de desempenho | <ul><li>[O [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[O [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[O [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[O [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[O [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[O [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Solução de problemas de desempenho e análise de tendências | <ul><li>[O [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[O [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[O [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[O [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[O [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) e [O [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualquer relatório básico que compara duas janelas de tempo usando o recurso &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificação das oportunidades de crescimento dos negócios | <ul><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Somente anunciantes com rastreamento de conversão do Adobe Advertising) [O [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Anunciantes com [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Relatórios personalizados dentro do Adobe Analytics Analysis Workspace</li></ul> |

## Gerar relatórios

### Gerar um novo relatório

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Clique em **[!UICONTROL Create Report]**, clique na categoria de relatório no painel esquerdo e selecione o tipo de relatório.<!-- Add link to list of report categories and report types --> Clique em **[!UICONTROL Proceed]**.

1. (Opcional) Na janela [!UICONTROL Create Report], altere as configurações padrão de relatório para [relatórios básicos e avançados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [relatórios de assistência](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [relatórios de precisão de modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) e [relatórios especializados](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md):

   1. (Opcional) Insira um nome personalizado para o relatório e para o modelo (se você salvar o relatório como um modelo).

   1. (Opcional) Para salvar as configurações do relatório como um modelo, habilite a configuração **[!UICONTROL Save as template]**.

   1. (Opcional) Selecione um relatório diferente **[!UICONTROL Type]** dentro da mesma categoria de relatório.

   1. (Opcional) Na guia **[!UICONTROL Basic Settings]**, selecione um modelo de relatório existente para usar ou alterar as configurações básicas padrão do relatório.

   1. (Opcional) Clique na guia **[!UICONTROL Columns]** e altere as colunas padrão no relatório, incluindo a ordem da coluna.

      Por padrão, todos os dados monetários nos relatórios são mostrados no formato para dólares americanos (como 1.000,00). Para exibir o valor no formato de moeda correto (mas sem símbolos de moeda nos formatos CSV e TSV), adicione a coluna &quot;[!UICONTROL Currency]&quot; ao relatório. Se o relatório incluir dados para contas com moedas diferentes, qualquer valor monetário &quot;[!UICONTROL Total]&quot; será a soma de todos os números na coluna, independentemente da moeda.

   1. (Alguns tipos de relatório, opcional) Clique na guia **[!UICONTROL Filters & Attribution]** ou **[!UICONTROL Filters]** e adicione filtros de dados, (alguns tipos de relatório) limite os resultados do relatório para incluir apenas classificações de rótulo específicas e altere as configurações padrão de regra de atribuição e atribuição de conversão.

   1. (Opcional) Clique na guia **[!UICONTROL Scheduling]** e altere as opções padrão de agendamento e entrega.

1. Clique em **[!UICONTROL Create]**.

Se você não tiver especificado um agendamento de relatório, o relatório será executado imediatamente; caso contrário, será executado de acordo com o agendamento especificado. O nome do relatório foi adicionado ao modo de exibição [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Se você tiver salvo o relatório como modelo, ele também será adicionado à exibição [[!UICONTROL Templates] &#x200B;](/help/search-social-commerce/reports/report-about.md). Quando o relatório é concluído, o arquivo é disponibilizado para abrir ou salvar; os modelos são disponibilizados imediatamente.

Se você tiver inserido endereços de email para notificação, cada destinatário receberá uma notificação quando o trabalho de relatório for concluído ou falhar, com base nas [configurações de notificação definidas pelo usuário](/help/search-social-commerce/notifications/notification-edit.md) para relatórios.

### Gerar um relatório a partir de um relatório existente

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que abrirá a guia **[!UICONTROL Latest Reports]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha do relatório e clique em **...** > **[!UICONTROL Duplicate]**.

   * Marque a caixa de seleção ao lado do relatório. Na barra de ferramentas de ações em massa, clique em [Duplicar](/help/search-social-commerce/assets/duplicate.png "Duplicar").

1. Edite as configurações do relatório, se necessário.

1. Clique em **[!UICONTROL Create]**.

### Gerar um relatório a partir de um modelo existente

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha de modelo e clique em **...** > **[!UICONTROL Duplicate]**.

   * Marque a caixa de seleção ao lado do modelo existente. Na barra de ferramentas de ações em massa, clique em [Duplicar](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.

1. (Opcional) Renomeie o modelo e edite as configurações do relatório, se necessário.

   Clique em **[!UICONTROL Next]** para mover entre as seções de configuração.

1. Habilite a configuração **[!UICONTROL Save as Template]**.

1. Clique em **[!UICONTROL Create]**.

## Visualizar ou salvar um relatório

Você pode visualizar um relatório no navegador da Web, abrir ou salvar os dados do relatório como uma pasta de trabalho [!DNL Microsoft Excel], um arquivo TSV (valores separados por tabulação), um arquivo CSV (valores separados por vírgula) ou (alguns tipos de relatório) uma pasta de trabalho com guias [!DNL Microsoft Excel].

>[!NOTE]
>
>Os membros da Equipe de conta da Adobe e alguns usuários administradores podem exibir relatórios criados por anunciantes e usuários de agências.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que abrirá a guia **[!UICONTROL Latest Reports]**.

1. Siga um destes procedimentos:

   * (Para exibir um relatório no navegador da Web) Siga um destes procedimentos:

      * Mantenha o cursor sobre a linha de modelo e clique em **...** > **[!UICONTROL Preview]**.

      * Marque a caixa de seleção ao lado do modelo existente. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Preview]**.

   * (Para abrir ou salvar os dados do relatório em um arquivo) Na coluna [!UICONTROL Export] ao lado do nome do relatório, clique no nome de um formato e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador:

      * **[!UICONTROL XLS]:** Para uma pasta de trabalho [!DNL Excel] com uma única planilha (formato XLSX). O relatório inclui uma planilha rotulada na parte superior com os parâmetros, com uma linha para cada componente relatado quando os dados do componente estiverem disponíveis. Linhas sem dados são omitidas.

        Os relatórios básicos incluem um total para cada coluna numérica.

      * **[!UICONTROL TSV]:** Para um arquivo TSV. O relatório inclui os parâmetros e uma linha para cada componente relatado.

      * **[!UICONTROL CSV]:** Para um arquivo CSV. O relatório inclui os parâmetros e uma linha para cada componente relatado.

## Excluir relatórios

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, que abrirá a guia **[!UICONTROL Latest Reports]**.

1. Siga um destes procedimentos:

   * (Para excluir um único relatório):

      1. Mantenha o cursor sobre a linha do relatório e clique em **...** > **[!UICONTROL Run]**.

      1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

   * (Para excluir um ou mais relatórios):

      1. Marque a caixa de seleção ao lado de cada relatório que você deseja excluir.

      1. Na barra de ferramentas de ações em massa, clique em [Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") **[!UICONTROL Delete]**.

      1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
