---
title: '[!UICONTROL Custom Creative Report]'
description: Saiba como gerar a experiência cruzada [!UICONTROL Custom Creative Report].
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: bf969c1b3cc57e2ef83087952a9bac530b276916
workflow-type: tm+mt
source-wordcount: '2021'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*recurso do Beta*

O [!UICONTROL Custom Creative Report] permite personalizar o conteúdo e a entrega de dados de relatório para todas as suas experiências de anúncio.

Você pode gerar relatórios uma vez ou pode agendá-los diariamente, semanalmente ou mensalmente às 03:00 no fuso horário especificado, de acordo com os critérios especificados (como a cada 15 dias ou no primeiro dia de cada mês). Depois que um relatório é gerado, você pode baixá-lo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou dos [destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados dos seguintes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL FTP <!-- (in beta) -->
* SFTP

## Criar um [!UICONTROL Custom Creative Report]

1. No menu principal, clique em **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. No canto superior direito, clique em **[!UICONTROL Create]**.

1. Especifique as [configurações do relatório](#report-settings).

1. Clique em **[!UICONTROL Create Custom Report]**.

## Configurações do relatório {#report-settings}

**[!UICONTROL Name]:** O nome do relatório. O comprimento máximo é de 180 caracteres.

**[!UICONTROL Report Type]:** O tipo de relatório: *[!UICONTROL Custom Creative Beta]*.

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
  >Você também pode [executar um relatório personalizado a qualquer momento](/help/dsp/reports/report-run-now.md) na exibição [!UICONTROL Reports].

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

**[!UICONTROL Select To Add As Report Headers]:** As colunas de dados, ou cabeçalhos, a serem incluídos no relatório. Para adicionar uma coluna, expanda a categoria e marque a caixa de seleção ao lado do nome da coluna. As colunas disponíveis variam de acordo com o relatório e todas as métricas indisponíveis são desativadas. Consulte &quot;[Colunas de Relatório Disponíveis](#report-custom-creative-columns)&quot; para obter descrições de todas as opções.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** A ordem dos cabeçalhos de coluna. Você pode arrastar e soltar qualquer coluna para personalizar a ordem.

**[!UICONTROL Format]:** Define se um relatório deve ser gerado no formato *[!UICONTROL CSV]* (valores separados por vírgula) ou *[!UICONTROL Tab]* (valores separados por tabulação).

**[!UICONTROL Headers]:** Se deseja *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* cabeçalhos de coluna.

### Seção [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** As configurações variam de acordo com o tipo de relatório:

* **\[Tipo de atribuição\]:** (somente anunciantes com rastreamento de conversão do Adobe Advertising) No relatório, como atribuir dados de conversão em uma série de eventos que levam a uma conversão:

   * *[!UICONTROL Unique]:* (padrão) Conta o número de vezes que um valor de dimensão (como um dispositivo ou posicionamento) estava no caminho para conversão.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* Distribui o crédito de cada conversão com base na frequência de ocorrência do valor da dimensão (como um dispositivo ou posicionamento) no caminho para conversão. Por exemplo, se houvesse um total de 10 impressões antes da conversão, com 8 no CTV e 2 no Mobile, então 80% do crédito (0,8) é dado para telas de CTV e 0,2 para o Mobile.

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

## Colunas de Relatório Disponíveis {#report-custom-creative-columns}

| Tipo de métrica | Subtipo | Nome da coluna | Descrição |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | As dimensões do anúncio publicado. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Se o anúncio fornecido foi um anúncio de imagem ou anúncio de vídeo padrão para a experiência. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Se os anúncios foram girados de acordo com pesos relativos (*Ponderados*) ou algorítmicos (*Algorítmicos*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | A ID que [!UICONTROL Creative] atribuiu ao criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | O nome do criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | O tipo de criativo (como [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | A ID que [!UICONTROL Creative] atribuiu ao criativo principal. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | O nome do criador principal. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | O tipo de criador pai (como [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | O URL da landing page. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | O tipo específico de interação do usuário. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | O fluxo direcional ou caminho de navegação da interação de cliques do usuário na experiência criativa. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | O navegador no qual o anúncio foi exibido (como [!UICONTROL Chrome] ou [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | O sistema operacional no qual o anúncio foi exibido (como [!UICONTROL Windows]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | O tipo de dispositivo no qual o anúncio foi exibido (como [!UICONTROL Desktop]). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | O nome da DSP em que os anúncios foram executados. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | A ID do posicionamento para o qual os anúncios foram executados. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | O nome do posicionamento para o qual os anúncios foram executados. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | A ID do site em que os anúncios foram executados. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | O nome do site em que os anúncios foram executados. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | A ID que [!UICONTROL Creative] atribuiu à marca de experiência de anúncio. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | O nome do anunciante. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | A data e a hora do evento. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | A ID que [!UICONTROL Creative] atribuiu à experiência. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | O nome da experiência. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | O caminho específico pela árvore decisória de direcionamento que determinou qual variante de experiência criativa foi disponibilizada para o usuário. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | O nome da tag do anúncio. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | A cidade à qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | Código do país ao qual são atribuídos os dados comunicados. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | A Área de mercado designada (DMA) à qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | O código do estado ao qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | O CEP ao qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Anúncios dinâmicos) A ID da categoria do produto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Anúncios dinâmicos) O nome da categoria do produto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Anúncios dinâmicos) O primeiro atributo criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Anúncios dinâmicos) O segundo atributo criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Anúncios dinâmicos) O terceiro atributo criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Anúncios dinâmicos) O quarto atributo criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Anúncios dinâmicos) O quinto atributo criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Anúncios dinâmicos) A ID do produto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Anúncios dinâmicos) O nome do produto de destino. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | As IDs para até cinco segmentos de usuário que corresponderam ao tema do anúncio. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | A ID de um pixel de redirecionamento ao qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | O nome de um pixel de redirecionamento ao qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Os atributos de um segmento de público-alvo ao qual os dados relatados são atribuídos. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | A soma de todos os cliques em um anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | A taxa de cliques, que é a porcentagem de cliques dividida por impressões de anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | A porcentagem de impressões veiculadas que resultaram em engajamentos do usuário. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | O número de interações em um anúncio veiculado. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | O número total de impressões de anúncios. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | A porcentagem de impressões com um cookie redirecionado. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | (Somente anúncios dinâmicos) A soma de todos os cliques nos anúncios de um produto. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | (Somente anúncios dinâmicos) A soma de todas as conversões em anúncios de um produto. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | (Somente anúncios dinâmicos) A porcentagem de anúncios de um produto que resultou em conversões. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | (Somente anúncios dinâmicos) A taxa de cliques para anúncios de um produto, que é a porcentagem de cliques dividida por impressões de anúncio. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | (Somente anúncios dinâmicos) O número total de impressões de um produto. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | (Somente anúncios dinâmicos) A receita total em anúncios veiculados para um produto. Quando o produto é nulo, esse valor é zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | A receita total dos anúncios veiculados. |
| [!UICONTROL Conversion Metrics] | [Agrupado pelo anunciante nas configurações do relatório] | [Conversão específica do anunciante] | O total de uma métrica de conversão específica do anunciante ou evento do Adobe Analytics. |
| [!UICONTROL Custom Goals] | [Agrupado pelo anunciante nas configurações do relatório] | [Meta personalizada específica do anunciante] | (Anunciantes com Advertising DSP) A soma ponderada de todas as conversões incluídas na [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md) especificada. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Relatórios de desempenho de nível de experiência](/help/creative/experiences/experience-performance-details.md)
>* [Sobre os relatórios personalizados do DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Sobre [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
