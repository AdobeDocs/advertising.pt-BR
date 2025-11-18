---
title: Gerenciar relatórios personalizados
description: Saiba como gerar e gerenciar a experiência cruzada [!UICONTROL Custom Creative Report].
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Você pode criar, duplicar, editar, executar, baixar e excluir relatórios personalizados.

## Criar um relatório personalizado {#report-create}

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. No canto superior direito, clique em **[!UICONTROL Create]**.

1. Especifique as [configurações do relatório](#report-settings).

1. Clique em **[!UICONTROL Create Custom Report]**.

## Duplicação de um relatório personalizado

Duplique um relatório personalizado para criar um novo relatório com configurações semelhantes.

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Ao lado do nome do relatório, clique em **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Opcional) Edite as [configurações do relatório](#report-settings.md) conforme necessário.

   O nome do relatório, por padrão, é &quot;\&lt;*nome do relatório existente*\> \#2&quot; (ou o próximo número na sequência).

## Editar um relatório personalizado {#report-edit}

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Ao lado do nome do relatório, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Edite as [configurações do relatório](#report-settings.md).

1. Clique em **[!UICONTROL Edit Custom Report]**.

## Executar um relatório personalizado {report-run-now}

Você pode executar qualquer relatório que não tenha expirado e não esteja em execução no momento.

>[!NOTE]
>
>Você também pode executar um relatório personalizado ao [criá-lo](#report-create) ou [editá-lo](#report-edit).

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Ao lado do nome do relatório, clique em **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   Quando o relatório é concluído, ele é enviado para os destinos especificados nas configurações do relatório.

## Baixar um relatório personalizado

É possível baixar qualquer instância de relatório concluída nos últimos quatro meses, com o status &quot;[!UICONTROL Ready to Download]&quot; ou &quot;[!UICONTROL Completed]&quot;.

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Na coluna [!UICONTROL Download Report] da linha do relatório, faça o seguinte:

   * Para baixar a instância mais recente do relatório, clique em **[!UICONTROL Download]**.

   * (Relatórios com várias instâncias) Clique em ![a seta para baixo](/help/dsp/assets/chevron-down.png "a seta para baixo") ao lado de [!UICONTROL Download] e, em seguida, clique na data de conclusão do relatório que deseja baixar. Instâncias de relatório baixáveis são indicadas com um ícone de download (![ícone de download](/help/dsp/assets/indicator-downloadable.png "ícone de download")).

     Quando muitas instâncias estiverem disponíveis, clique em **[!UICONTROL Load More]** na parte inferior da lista, se necessário.

     Quando um relatório é executado várias vezes no mesmo dia, as instâncias de relatório desse dia são listadas em ordem cronológica, com a instância mais recente no topo.

     Os trabalhos de relatório com falha são indicados com um ícone de erro (![indicador de erro](/help/dsp/assets/indicator-critical.png "indicador de erro")) e não podem ser baixados. Mantenha o cursor sobre o ícone de erro para obter uma descrição do erro.

## Excluir um relatório personalizado

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Ao lado do nome do relatório, clique em **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Configurações do relatório {#report-settings}

**[!UICONTROL Name]:** O nome do relatório. O comprimento máximo é de 180 caracteres.

**[!UICONTROL Report Type]:** O tipo de relatório.

### Seção [!UICONTROL Report Range]

Esta seção determina os dados incluídos no relatório. Para configurar datas para o agendamento do relatório, consulte a seção &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** O fuso horário para relatórios.

**[!UICONTROL Observe Daylight Savings Time]:** considera o horário de verão nos horários relatados.

**Intervalo:** o intervalo de datas para o qual gerar dados. O número de dias disponíveis varia de acordo com o relatório e as dimensões selecionadas. Escolha um:

* **[!UICONTROL Previous Calendar Week]:** Inclui dados da semana anterior.

* **[!UICONTROL Previous Calendar Month]:** Inclui dados do mês anterior.

* **[!UICONTROL Custom Range]:** Inclui dados entre datas de início e término específicas. Para relatar dados até o dia anterior, selecione **[!UICONTROL Present]**.

### Seção [!UICONTROL Report Run schedule]

Esta seção determina as datas em que o relatório é executado. Para configurar as datas nas quais incluir dados de relatório, consulte a seção &quot;[!UICONTROL Report range]&quot;.

**\[Agenda\]:** Quando gerar o relatório:

* *[!UICONTROL Immediately]*: Adiciona imediatamente o relatório à fila de relatórios.

  >[!NOTE]
  >
  >Você também pode [executar um relatório personalizado a qualquer momento](#report-run-now) na exibição [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Executa o relatório em uma data especificada para conclusão até 09:00 no fuso horário da conta.

* *[!UICONTROL Recurring]:* Executa o relatório de acordo com um agendamento durante um período de tempo especificado.

   * **\[Cronograma\]:** Com que frequência executar o relatório:

      * *Diariamente* para executar o relatório a cada N número de dias. Por exemplo, para executar o relatório a cada duas semanas (14 dias), selecione esta opção e digite **14**.

      * *Semanalmente* para executar o relatório em dias da semana especificados. Por exemplo, para executar o relatório toda segunda e sexta-feira, marque essa opção e marque as caixas de seleção ao lado de **segunda** e **sexta-feira**.

      * *Monthly* para executar o relatório em um dia numérico específico do mês, de 1 a 30. Por exemplo, para executar o relatório no primeiro dia de cada mês, selecione esta opção e digite **1**.

   * **De**: a primeira data em que o relatório pode ser executado. Dependendo do agendamento especificado, a primeira instância de relatório pode ocorrer após essa data.

   * **Até**: a data de expiração do relatório, que pode ser de até quatro meses. Antes de um relatório expirar, todos os destinos de email especificados recebem um alerta por email sete dias e um dia antes da data de expiração. Para manter o relatório por mais tempo, altere esta data.

### Seção [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Opcional) Dimensões adicionais pelas quais filtrar os dados, sejam as dimensões incluídas como colunas no relatório ou não. Os filtros disponíveis variam por tipo de relatório e podem incluir: *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* e *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Para aplicar um ou mais filtros, faça o seguinte:

* Selecione uma dimensão, o operador (*é igual a* ou *não é igual a*) e o valor aplicável. Por exemplo, para retornar dados apenas para anúncios precedentes, especifique &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Opcional) Adicione outros critérios ao filtro.
* (Opcional) Adicione filtros adicionais, cada um com um ou mais critérios.

### Seção [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** As colunas de dados, ou cabeçalhos, a serem incluídos no relatório. Para adicionar uma coluna, expanda a categoria e marque a caixa de seleção ao lado do nome da coluna. As colunas disponíveis variam de acordo com o relatório e todas as métricas indisponíveis estão desabilitadas.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** A ordem dos cabeçalhos de coluna. Você pode arrastar e soltar qualquer coluna para personalizar a ordem.

**[!UICONTROL Format]:** Define se um relatório deve ser gerado no formato *[!UICONTROL CSV]* (valores separados por vírgula) ou *[!UICONTROL Tab]* (valores separados por tabulação).

**[!UICONTROL Headers]:** Se deseja *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* cabeçalhos de coluna.

### Seção [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** As configurações variam de acordo com o tipo de relatório:

* **\[Tipo de regra\]:** (somente anunciantes com rastreamento de conversão do Adobe Advertising) No relatório, como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Você pode escolher mais de uma regra se quiser comparar diferenças entre as regras.

  >[!NOTE]
  >
  >Os caminhos de conversão incluem quaisquer impressões e cliques na impressão do anunciante ou nas janelas de retrospectiva de cliques, que estão configuradas em [!DNL Advertising Search, Social, & Commerce]. Os cliques recebem preferência por impressões durante a atribuição de conversão. Quaisquer cliques em um caminho de conversão receberão crédito total com base na regra de atribuição. As impressões recebem crédito somente quando nenhum clique é rastreado no caminho de conversão.

   * *[!UICONTROL Last Event]:* Atributos convertem para o último clique ou impressão no caminho de conversão.

   * *[!UICONTROL Weight Last More]:* Atribui conversões a todos os eventos no caminho de conversão, mas dá mais peso ao último evento e sucessivamente menos peso aos eventos anteriores.

   * *[!UICONTROL Even Distribution]:* Atributos convertem igualmente para cada evento no caminho de conversão.

   * *[!UICONTROL Weight First More]:* Atribui conversões a todos os eventos no caminho de conversão, mas concede mais peso ao primeiro evento e, sucessivamente, menos peso aos eventos a seguir.

   * *[!UICONTROL First Event]:* Conversões de atributos para o primeiro clique ou impressão no caminho de conversão.

   * *[!UICONTROL U-shaped]:* Atribui a conversão a todos os eventos no caminho de conversão, mas fornece mais peso ao primeiro e ao último eventos, com peso sucessivamente menor para os eventos no meio do caminho de conversão.

   * *[!UICONTROL Display Only]:* Conversões de atributos para o último clique ou impressão do DSP no caminho de conversão. Isso inclui vídeo e anúncios de TV conectados e exclui cliques em [!DNL Advertising Search, Social, & Commerce] anúncios.

   * *[!UICONTROL Social Only]:* Obsoleto

Consulte também &quot;[Como as regras de atribuição são calculadas para o Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)&quot;.

**[!UICONTROL Paths as Columns]:** Que tipos de conversões relatar quando eventos anteriores ocorreram no mesmo dispositivo. É possível incluir até três tipos. Para cada tipo selecionado, uma coluna separada é incluída para cada métrica de conversão e é anexada com o sufixo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)] ou [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inclui conversões atribuídas a cliques (CT para click-through) e a impressões (VT para view-through). As conversões atribuídas a impressões são multiplicadas pelo peso de viewthrough especificado. O peso de view-through padrão é de 100%, o que significa que as conversões atribuídas a impressões são contadas como 100% do valor das conversões atribuídas a cliques.

* *[!UICONTROL With Clicks (CT)]:* Inclui somente conversões atribuídas a cliques.

* *[!UICONTROL Impressions Only (VT)]:* Inclui somente conversões que foram atribuídas a impressões porque nenhum clique foi rastreado no caminho de conversão.

### Seção [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Onde entregar os relatórios concluídos e as notificações de erro. Não é possível alterar o tipo de destino depois de salvar o relatório.

>[!NOTE]
>
>Você sempre pode baixar relatórios concluídos da exibição [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Para não entregar nenhum relatório ou notificação.

* *[!UICONTROL S3]:* Para enviar o relatório concluído para um ou mais locais [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Para enviar o relatório concluído para um ou mais locais SFTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Para enviar o relatório concluído para um ou mais locais FTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL](Atualmente no Beta):* Para enviar o relatório concluído para um ou mais locais SSL FTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Para especificar endereços de email para os quais enviar relatórios concluídos ou notificações se o relatório for cancelado devido a erros.

**[!UICONTROL Email]:** (somente tipo de destino de email) Para cada endereço, insira o endereço e clique em **+**.

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP e somente tipos de destino SSL do FTP) Os nomes dos [destinos do relatório](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} para os quais o relatório personalizado é enviado.

* Para especificar um destino existente, selecione um nome de destino na lista. É possível selecionar vários nomes de destino separadamente.

* Para criar um novo destino:

   1. Clique em **Adicionar novo destino**.

   1. Insira as [configurações de destino do relatório](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} e clique em **Salvar**.

   1. De volta às configurações do relatório, clique em **Atualizar nomes de destino.**

      O novo destino agora está disponível na lista de destinos existentes, e você pode adicioná-lo ao relatório.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Relatórios de desempenho de nível de experiência](/help/creative/experiences/experience-performance-details.md)
>* [Sobre os relatórios personalizados do DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Sobre [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
