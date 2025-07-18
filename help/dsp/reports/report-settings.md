---
title: Configurações do relatório personalizado
description: Consulte descrições das configurações de relatório personalizadas.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 0%

---

# Configurações do relatório personalizado

**[!UICONTROL Name]:** O nome do relatório. O comprimento máximo é de 180 caracteres.

**[!UICONTROL Report Type]:** O tipo de relatório: *[!UICONTROL Custom]* (que inclui a maioria das opções disponíveis), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, **, *[!UICONTROL Path Length]* ou *[!UICONTROL Time to Conversion]*.

## Seção [!UICONTROL Report Range]

Esta seção determina os dados incluídos no relatório. Para configurar datas para o agendamento do relatório, consulte a seção &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** O fuso horário para relatórios.

**[!UICONTROL Observe Daylight Savings Time]:** considera o horário de verão nos horários relatados.

**Intervalo:** o intervalo de datas para o qual gerar dados. O número de dias disponíveis varia de acordo com o relatório e as dimensões selecionadas. Escolha um:

* **[!UICONTROL Previous Calendar Week]:** Inclui dados da semana anterior.

* **[!UICONTROL Previous Calendar Month]:** Inclui dados do mês anterior.

* **[!UICONTROL Custom Range]:** Inclui dados entre datas de início e término específicas. Para relatar dados até o dia anterior, selecione **[!UICONTROL Present]**.

## Seção [!UICONTROL Report Run schedule]

Esta seção determina as datas em que o relatório é executado. Para configurar as datas nas quais incluir dados de relatório, consulte a seção &quot;[!UICONTROL Report range]&quot;.

**\[Agenda\]:** Quando gerar o relatório:

* *[!UICONTROL Immediately]*: Adiciona imediatamente o relatório à fila de relatórios.

  >[!NOTE]
  >
  >Você também pode [executar um relatório personalizado a qualquer momento](report-run-now.md) na exibição [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* Executa o relatório em uma data especificada para conclusão às 09:00 no fuso horário da conta.

* *[!UICONTROL Recurring]:* Executa o relatório de acordo com um agendamento durante um período de tempo especificado.

   * **\[Cronograma\]:** Com que frequência executar o relatório:

      * *Diariamente* para executar o relatório a cada N número de dias. Por exemplo, para executar o relatório a cada duas semanas (14 dias), selecione esta opção e digite **14**.

      * *Semanalmente* para executar o relatório em dias da semana especificados. Por exemplo, para executar o relatório toda segunda e sexta-feira, marque essa opção e marque as caixas de seleção ao lado de **segunda** e **sexta-feira**.

      * *Monthly* para executar o relatório em um dia numérico específico do mês, de 1 a 30. Por exemplo, para executar o relatório no primeiro dia de cada mês, selecione esta opção e digite **1**.

   * **De**: a primeira data em que o relatório pode ser executado. Dependendo do agendamento especificado, a primeira instância de relatório pode ocorrer após essa data.

   * **Até**: a data de expiração do relatório, que pode ser de até quatro meses. Antes de um relatório expirar, todos os destinos de email especificados recebem um alerta por email sete dias e um dia antes da data de expiração. Para manter o relatório por mais tempo, altere esta data.

## Seção [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (Opcional) Dimensões adicionais pelas quais filtrar os dados, sejam as dimensões incluídas como colunas no relatório ou não. Os filtros disponíveis variam por tipo de relatório e podem incluir: *[!UICONTROL Account]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* e *[!UICONTROL Video Duration]*.

<!-- Add when available:
*[!UICONTROL Deal ID]*, *[!UICONTROL Deal List]*, 
-->

Para aplicar um ou mais filtros, faça o seguinte:

* Selecione uma dimensão, o operador (*é igual a* ou *não é igual a*) e o valor aplicável. Por exemplo, para retornar dados apenas para anúncios precedentes, especifique &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Opcional) Adicione outros critérios ao filtro.
* (Opcional) Adicione filtros adicionais, cada um com um ou mais critérios.

\* *[!UICONTROL Account]* está disponível somente para os seguintes tipos de relatório quando sua organização está configurada para [relatórios entre contas](report-about.md#cross-account-reporting): [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] e [!UICONTROL Conversion]. Entre em contato com a equipe de conta da Adobe para obter mais informações sobre relatórios entre contas.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (Caminho para Conversão, Extensão do Caminho e Tempo para Conversão somente) Inclui dados para cliques em anúncios de pesquisa de campanhas Advertising Search, Social e Commerce especificadas. Ao selecionar essa opção:

1. Selecione a conta de Pesquisa, Social e Commerce usando o filtro **Filtrar por[!UICONTROL SSC Account]**.

1. Selecione as campanhas usando o filtro **Filtrar por[!UICONTROL SSC Campaign]**.

   Para selecionar várias campanhas, clique em **[!UICONTROL Add Criteria]** para a segunda campanha e as campanhas subsequentes.

## Seção [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** As colunas de dados, ou cabeçalhos, a serem incluídos no relatório. Para adicionar uma coluna, expanda a categoria e marque a caixa de seleção ao lado do nome da coluna. As colunas disponíveis variam de acordo com o relatório e todas as métricas indisponíveis são desativadas. As categorias de dados disponíveis podem incluir:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Os relatórios [!UICONTROL Household Reach & Frequency] e [!UICONTROL Path to Conversion] podem incluir apenas uma dimensão.
  > Os relatórios [!UICONTROL Path Length] e [!UICONTROL Time to Conversion] não incluem dimensões.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >O relatório [!UICONTROL Household Reach & Frequency] pode incluir métricas de sobreposição ou não sobreposição, mas não ambas.

* [!UICONTROL Conversion Metrics] (classificado pelo anunciante)

* [!UICONTROL Custom Goals] (classificado pelo anunciante)

Consulte &quot;[Colunas de Relatório Disponíveis](report-columns.md)&quot; para obter descrições de todas as opções.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** A ordem dos cabeçalhos de coluna. Você pode arrastar e soltar qualquer coluna para personalizar a ordem.

**[!UICONTROL Format]:** Define se um relatório deve ser gerado no formato *[!UICONTROL CSV]* (valores separados por vírgula) ou *[!UICONTROL Tab]* (valores separados por tabulação).

**[!UICONTROL Headers]:** Se deseja *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* cabeçalhos de coluna.

## Seção [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** As configurações variam de acordo com o tipo de relatório:

* **\[Tipo de atribuição\]:** ([!UICONTROL Household Conversion] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas) No relatório, como atribuir dados de conversão em uma série de eventos que levam a uma conversão:

   * *[!UICONTROL Unique]:* (padrão) Conta o número de vezes que um valor de dimensão (como um dispositivo ou posicionamento) estava no caminho para conversão.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribui o crédito de cada conversão com base na frequência de ocorrência do valor da dimensão (como um dispositivo ou posicionamento) no caminho para conversão. Por exemplo, se houvesse um total de 10 impressões antes da conversão, com 8 no CTV e 2 no Mobile, então 80% do crédito (0,8) é dado para telas de CTV e 0,2 para o Mobile.

* **\[Tipo de Regra\]:** (Todos os relatórios [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] e [!UICONTROL Site] com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas; anunciantes somente com rastreamento de conversão do Adobe Advertising) No relatório, como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Você pode escolher mais de uma regra se quiser comparar diferenças entre as regras.

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

* **Pesquisa:** ([!UICONTROL Household Conversion] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas e [!UICONTROL Path to Conversion], [!UICONTROL Path Length] ou [!UICONTROL Time to Conversion] relatórios somente com [!UICONTROL Conversion Metrics] colunas; anunciantes somente com rastreamento de conversão do Adobe Advertising) No relatório, o número máximo de dias após um evento de impressão ou um evento de clique (para relatórios [!UICONTROL Path to Conversion], [!UICONTROL Path Length] ou [!UICONTROL Time to Conversion]) em que um evento de conversão pode ser atribuído a ele. O padrão é *[!UICONTROL 30 days]*, e o máximo é de 92 dias.

  >[!TIP]
  >
  >Se você usar [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), use a mesma janela de pesquisa que você usa em [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (Todos os relatórios [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] e [!UICONTROL Site] com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas) Quais tipos de conversões relatar quando eventos anteriores ocorreram no mesmo dispositivo. É possível incluir até três tipos. Para cada tipo selecionado, uma coluna separada é incluída para cada métrica de conversão e é anexada com o sufixo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)] ou [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inclui conversões atribuídas a cliques (CT para click-through) e a impressões (VT para view-through). As conversões atribuídas a impressões são multiplicadas pelo peso de viewthrough especificado. O peso de view-through padrão é de 100%, o que significa que as conversões atribuídas a impressões são contadas como 100% do valor das conversões atribuídas a cliques.

* *[!UICONTROL With Clicks (CT)]:* Inclui somente conversões atribuídas a cliques.

* *[!UICONTROL Impressions Only (VT)]:* Inclui somente conversões que foram atribuídas a impressões porque nenhum clique foi rastreado no caminho de conversão.

**[!UICONTROL Conversion Reporting Based On]:** Como relatar dados de conversão:

* *[!UICONTROL Conversion Timestamp]:* (padrão) Conversões estão associadas à data de conversão.

* *[!UICONTROL Event Timestamp]:* As conversões são relatadas com base na data da impressão ou clique que causou a conversão, conforme determinado pelo [!UICONTROL Attribution Rule Settings] especificado.

## Seção [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Onde entregar os relatórios concluídos e as notificações de erro. Não é possível alterar o tipo de destino depois de salvar o relatório.

>[!NOTE]
>
>Você sempre pode baixar relatórios concluídos da exibição [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Para não entregar nenhum relatório ou notificação.

* *[!UICONTROL S3]:* Para enviar o relatório concluído para um ou mais locais [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Para enviar o relatório concluído para um ou mais locais SFTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Para enviar o relatório concluído para um ou mais locais FTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL] (Atualmente no Beta):* Para enviar o relatório concluído para um ou mais locais SSL FTP, que você deve selecionar no campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Para especificar endereços de email para os quais enviar relatórios concluídos ou notificações se o relatório for cancelado devido a erros.

**[!UICONTROL Email]:** (somente tipo de destino de email) Para cada endereço, insira o endereço e clique em **+**.

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP e FTP somente tipos de destino SSL) Os nomes dos destinos de relatório para os quais o relatório personalizado é enviado.

* Para especificar um destino existente, selecione um nome de destino na lista. É possível selecionar vários nomes de destino separadamente.

* Para criar um novo destino:

   1. Clique em **Adicionar novo destino**.

   1. Insira as [configurações de destino do relatório](/help/dsp/reports/report-destinations/report-destination-settings.md) e clique em **Salvar**.

   1. De volta às configurações do relatório, clique em **Atualizar nomes de destino.**

      O novo destino agora está disponível na lista de destinos existentes, e você pode adicioná-lo ao relatório.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar um Relatório Personalizado](/help/dsp/reports/report-copy.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Baixar um Relatório Personalizado](/help/dsp/reports/report-download.md)
>* [Executar um Relatório Personalizado](/help/dsp/reports/report-run-now.md)
>* [Configurações de Relatório Personalizado](/help/dsp/reports/report-settings.md)
>* [Sobre Destinos de Relatórios](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
