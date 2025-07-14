---
title: Perguntas frequentes Sobre relatórios personalizados
description: Saiba mais sobre respostas a perguntas comuns sobre relatórios de desempenho, incluindo solução de problemas de dados.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 01fe9264fee43ed29f6cee022dadeb29fbd26f45
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Perguntas frequentes Sobre relatórios personalizados

## Perguntas gerais

+++E se o intervalo de datas do relatório começar antes dos dados do relatório estarem disponíveis?
O relatório é gerado, mas inclui apenas dados para as datas em que os dados estão disponíveis. Para obter mais informações sobre quando os dados estão disponíveis para cada tipo de relatório, consulte &quot;[Os dados usados para os relatórios](data-used-for-reports.md)&quot;.
+++

+++Qual é a diferença entre relatórios baseados em data de clique e data de transação?
Quando você relata conversões por data da transação, os dados incluem transações cuja data da transação ocorreu durante o período especificado. Essa opção é a configuração padrão nos relatórios básicos e avançados e mostra quanta receita foi auferida dentro do período especificado.

Quando você relata conversões por data de clique, os dados incluem transações que resultaram de um clique que ocorreu durante o período especificado. Quando um portfólio tem atrasos significativos entre cliques e transações, esse tipo de relatório mostra o histórico de receita por clique do portfólio, o que dá uma ideia de quais comportamentos de receita esperar ao longo do tempo.

![Relatório por data de clique versus relatório por data de transação](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Relatório por data de clique versus relatório por data de transação")
+++

+++O que acontece se eu alterar a janela de retrospectiva de clique ou a janela de retrospectiva de impressão?
(Somente anunciantes com o serviço de rastreamento de conversão baseado em pixel do Advertising) Os dados para eventos resultantes do clique inicial são coletados por um período mais longo ou mais curto.

A [janela de retrospectiva de cliques](/help/search-social-commerce/glossary.md#c-d) e a [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j) de um anunciante determinam o número de dias após a ocorrência de um clique pago ou de uma impressão de exibição (respectivamente) em que o evento pode ser atribuído a uma conversão. Alterar um valor para um período mais longo ou mais curto pode ser importante para anunciantes com períodos especialmente curtos ou longos de clique para receita ou de exibição de impressão para receita.

**Prática recomendada:** verifique se as janelas de retrospectiva são mais longas do que os tempos de clique para receita e exibição de impressão para receita para a maioria de suas palavras-chave ou anúncios. Quando são mais curtas, algumas conversões não são associadas ao clique ou impressão inicial.
+++

+++Como sei quais conversões resultaram de uma extensão de anúncio [!DNL Google Ads] ou lista de produtos?
Você pode ver quais conversões resultaram de um clique em uma extensão de anúncio [!DNL Google Ads] (em vez do anúncio propriamente dito) ou em uma lista de produtos gerando um [!UICONTROL Transaction Report]. O valor da coluna [!UICONTROL Link Type] mostra o tipo e o título de um link que foi clicado:

* As listas de produtos estão listadas como `pla:<product ID>`, como `pla:8525822`.

* Os sitelinks estão listados como `sl:<Sitelink text>`, como `sl:See Current Offers`.

  Você também pode identificar um sitelink se incluir a coluna [!UICONTROL Tracking URL] no relatório. O [!UICONTROL Tracking URL] para um sitelink inclui o atributo `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Conversões de [!DNL Google Ads] locais e ramais telefônicos são incluídas nos dados dos anúncios que elas acompanham. Eles não são relatados separadamente.

+++

+++A coluna &quot;[!UICONTROL Keyword]&quot; no meu relatório inclui um valor &quot;(conteúdo adgroup) &lt;*nome do grupo de anúncios*>.&quot;
Quando a linha inclui dados para campanhas de pesquisa habilitadas para conteúdo, campanhas de exibição ou campanhas sociais — que não incluem palavras-chave — a coluna [!UICONTROL Keyword] mostra o nome do grupo de anúncios aplicável.
+++

+++Devido a alterações sazonais ou de mercado, meus relatórios mostram dados atípicos. Isso afeta os lances depois que as condições são alteradas?
O recurso de otimização cria seus modelos de receita para cada unidade de oferta diariamente para garantir que ele identifique e responda imediatamente às tendências, e os modelos incorporam dados históricos de longo prazo para ajudar a prever o desempenho sazonal. A configuração de meia-vida do modelo de receita do portfólio <!-- add link to glossary? --> também determina o peso dos dados de receita recentes. A prática recomendada é reduzir a meia-vida durante um período de desempenho atípico, mas aumentá-la depois que o modelo de receita for ajustado. Em caso de dúvidas sobre a necessidade de ajustar a meia-vida, entre em contato com a equipe de conta da Adobe.

Se você não quiser que os dados do período afetem lances futuros, poderá optar por excluir essas datas do modelo. Entre em contato com a equipe de conta da Adobe para excluir as datas.
+++

+++É possível criar um relatório sobre uma métrica de propriedade de conta específica, como [!UICONTROL Device] ou [!UICONTROL Objective Name]?
Para relatórios de entidade de campanha ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] e [!UICONTROL Product Group Report]), os dados de métrica são agregados dinamicamente pelas colunas de propriedade incluídas no relatório. Opcionalmente, é possível remover a coluna principal do relatório e incluir apenas as colunas de propriedade para as quais deseja agregar dados.

Por exemplo, se você gerar uma [!UICONTROL Keyword Report] que inclua as colunas Dispositivo [!UICONTROL Ad Group] e , então, por padrão, o relatório agrega métricas para cada palavra-chave por grupo de anúncios e tipo de dispositivo. No entanto, se você remover a coluna [!UICONTROL Keyword] antes de gerar o relatório, ele gera dinamicamente métricas para os grupos de anúncios especificados por tipo de dispositivo.

>[!NOTE]
>
>Você não pode usar esse recurso para agregar dados por classificações de rótulo. Quaisquer colunas de classificação de etiqueta no relatório são omitidas. Em vez disso, use o [Relatório de Classificação de Rótulo](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Problemas gerais de dados

+++Relatórios gerados usando diferentes regras de atribuição mostram totais diferentes.
Se você gerar um relatório várias vezes usando os mesmos parâmetros de relatório, mas com regras de atribuição diferentes, os dados poderão ser diferentes por um dos seguintes motivos:

* Os dados baseados em data de clique podem estar fora do intervalo de datas especificado.

  Se você usar o parâmetro de relatório &quot;[!UICONTROL Conversions based on click date]&quot;, o intervalo de datas especificado será aplicado à data do clique em vez da data da transação. Se o relatório também usar a regra de atribuição &quot;Primeiro evento&quot; ou &quot;Último evento&quot;, o primeiro ou o último evento que levou à conversão pode estar fora do intervalo de datas especificado. Por exemplo, suponha que um usuário tenha clicado em Keyword_1 em 30 de abril, em Keyword_2 em 20 de maio e convertido em 21 de maio. Se o relatório usar a regra de atribuição &quot;[!UICONTROL First Event]&quot; e um intervalo de datas de 1 a 21 de maio, o primeiro evento (um clique em Keyword_1 em 30 de abril) não será incluído no relatório. Se você executar o relatório com o mesmo intervalo de datas, mas usando a regra de atribuição &quot;[!UICONTROL Last Event]&quot;, a conversão será incluída no relatório porque o último clique ocorreu dentro do intervalo de datas especificado.

* A seleção de filtro de portfólio exclui alguns dos eventos que levam à conversão.

  Se você relatar em um subconjunto de portfólios, talvez não esteja incluindo as campanhas que incluíram o evento ao qual a conversão foi atribuída em uma das regras de atribuição. Por exemplo, suponha que um usuário clique em Palavra-chave_1 de Portfolio_1, clique em Palavra-chave_2 de Portfolio_2 e, em seguida, converta. Se o relatório usar a regra de atribuição &quot;[!UICONTROL First Event]&quot;, Portfolio_1 deverá ser incluído para que a conversão seja incluída no relatório. No entanto, se o relatório usar a regra de atribuição &quot;Último evento&quot;, Portfolio_2 deverá ser incluído.

>[!TIP]
>
>Se você deseja comparar os totais de conversão de acordo com diferentes regras de atribuição, execute os relatórios usando o parâmetro de relatório &quot;[!UICONTROL Conversions based on transaction date]&quot; e selecione todas as redes de anúncios ou todos os portfólios. Se você não definir outros filtros, os totais de conversão deverão corresponder.

+++

+++Os campos de dados individuais estão incorretos, embora os totais estejam corretos.
Essa situação pode ocorrer quando os formatos de métrica usam números inteiros:

* Se você criar uma [métrica personalizada](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) com o formato *Número com/sem Pontos Decimais* (que mostra dados como números inteiros) e incluí-los em um modo de exibição ou relatório que usa uma regra de atribuição de conversão ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), a saída será mostrada em números inteiros, não em decimais. Nesse caso, campos de dados individuais podem estar incorretos, embora os totais estejam corretos. Por exemplo, se uma ordem é dividida uniformemente entre três eventos, uma ordem (em vez de 0,33) é atribuída a cada um dos três eventos. Para resolver o problema, [altere o formato da métrica](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) para *Número para 2 Pontos Decimais*.

* Da mesma forma, se você tiver uma métrica de receita enviada como um número inteiro, ocorrerá o mesmo problema. (O formato de receita é controlado pela tag de conversão que envia os dados.) Para resolver o problema, [crie uma métrica personalizada](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) que consista exclusivamente na métrica de receita e com o formato *Número para 2 Pontos Decimais*, e inclua-a em exibições e relatórios em vez da métrica original.
+++

+++Quando os dados de clique ou receita estão ausentes, como evitar que afetem lances futuros?
Problemas de dados de cliques ocorrem quando o Search, o Social e o Commerce estão fora de sincronia com a rede de anúncios. Entre em contato com a equipe de conta da Adobe para sincronizar manualmente a conta. Se os dados de cliques estiverem ausentes por um dia inteiro, peça à sua equipe de conta da Adobe para excluir esse dia dos modelos de custo.

Problemas de dados de receita podem ocorrer devido a um problema de arquivo de rastreamento ou feed. Entre em contato com a equipe de conta da Adobe para investigar o problema. Se os dados de receita estiverem ausentes por um dia inteiro, peça à sua equipe de conta da Adobe para excluir esse dia dos modelos de receita.
+++

+++Os dados monetários são mostrados no formato incorreto.
Por padrão, todos os dados monetários nos relatórios são mostrados no formato para dólares americanos (como 1.000,00). Para exibir o valor no formato de moeda correto (mas sem símbolos de moeda nos formatos CSV e TSV), adicione a coluna &quot;[!UICONTROL Currency]&quot; ao relatório. Se o relatório incluir dados para contas com moedas diferentes, qualquer valor monetário &quot;[!UICONTROL Total]&quot; será simplesmente a soma de todos os números na coluna, independentemente da moeda.
+++

+++Por que vejo valores decimais para uma métrica de conversão que deve ser um número natural (1, 2 e assim por diante)?
Você pode ver valores decimais nos seguintes casos:

* Se você executou o relatório usando qualquer parâmetro de regra de atribuição de conversão diferente de [!UICONTROL Last Event] ou [!UICONTROL First Event], a receita pode ser dividida entre vários eventos no caminho de conversão.

* Na [!UICONTROL Transaction Report], se várias [unidades de oferta](/help/search-social-commerce/glossary.md#a-b) com diferentes tipos de correspondência tiverem a mesma ID de transação, a receita da ID de rastreamento será dividida de acordo com o número de cliques na data de clique especificada.
+++

## Métricas de desempenho padrão

+++Os dados de clique estão ausentes dos relatórios.
Veja a seguir os motivos comuns para a falta de dados de cliques.

| Causa | Detecção/análise | Resolução |
|---|---|---|
| O processo que recupera os dados de cliques da conta de anúncio falhou. | Não há uma maneira sistemática de detectar esse problema, mas você pode notar que uma campanha não mostra informações de custo ou clique, mesmo que a conta publicitária tenha gasto dinheiro. | Entre em contato com a equipe de conta da Adobe.<br><br>Se os dados estiverem ausentes por mais de 24 horas, exclua essas datas das previsões de custo até que os dados sejam recuperados. A equipe de conta da Adobe pode excluir as datas. |
| Um problema de faturamento entre o anunciante e a rede de anúncios impede que a conta de anúncios seja gasta. | Não há uma maneira sistemática de detectar esse problema, mas você pode notar que uma campanha não mostra informações de custos ou cliques. | Se você souber que uma conta publicitária não pôde gastar devido a um problema de faturamento, exclua essas datas das previsões de custo. A equipe de conta da Adobe pode excluir as datas. |

+++

+++Os dados de desempenho são diferentes dos dados no editor de rede de anúncios.
Quando a rede de anúncios envia atualizações para dados anteriores (geralmente porque atribuíram fraude de cliques a alguns cliques), o Search, Social e Commerce não atualiza os dados, a menos que haja mais de 5% de discrepância e a Equipe de conta da Adobe registre uma solicitação.

Além disso, ao comparar dados de compartilhamento de impressão agregados em um intervalo de datas, os dados que os relatórios de Pesquisa, Social e Commerce podem ser diferentes dos dados que a rede de publicidade relata. Essa diferença se deve à maneira como os dados são relatados pela API da rede de anúncios, que a Search, o Social e o Commerce usam para obter dados. Por exemplo, para dados [!DNL Google Ads]:

* Para a maioria das métricas de compartilhamento de impressão, [!DNL Google Ads] limita a extremidade inferior ou superior dos valores relatados para valores menores que 10% ou maiores que 90%. Os dados são reportados como 0,0999 para &lt;10% e 0,9001 para >90%

* Quando há uma combinação de dados limitados e não limitados no intervalo de datas, a impressão dos agregados do Search, Social e Commerce compartilha dados usando os valores enviados na API como estão, usando 0,0999 para linhas com &lt;10% e 0,9001 para linhas com >90%. Esta agregação pode resultar em uma variação dos dados pré-agregados de [!DNL Google Ads], pois [!DNL Google Ads] pode usar valores percentuais reais, como 7% ou 97%.
+++

+++Os dados de desempenho em relatórios são diferentes dos dados em [!DNL Google Analytics].
Os dois sistemas medem dados diferentes, portanto, você deve esperar ver dados diferentes. Por exemplo:

* Pesquisa, Social e Commerce (e Google Ads) monitoram cliques, enquanto [!DNL Google Analytics] monitoram visitas por sessão de navegador de 30 minutos. Por exemplo, se um usuário clicar em seu anúncio uma vez, clicar no botão Voltar e clicar no anúncio novamente, então Pesquisar, Social e Commerce registrará dois cliques, mas [!DNL Google Analytics] registrará uma visita.

* O [!DNL Google Analytics] mostra todos os dados de tráfego, enquanto o Search, Social, &amp; Commerce (e o [!DNL Google Ads]) filtra cliques inválidos (como cliques repetidos em excesso).

* [!DNL Google Analytics] inclui dados de cliques e receita para todos os cliques. Search, Social e Commerce não podem rastrear dados de cliques e receita de anúncios e palavras-chave com URLs de rastreamento incorretos ou ausentes.
+++

## Métricas de conversão

+++Meu relatório não mostra dados de conversão.
O relatório pode não incluir métricas de conversão para as quais ocorreram conversões.
+++

+++A receita está ausente dos relatórios.

**Anunciantes usando marcas de conversão do Adobe Advertising**

*Causas possíveis:*

* Palavras-chave ou anúncios foram adicionados sem prefixar o prefixo de rastreamento de cliques em Search, Social e Commerce aos modelos de rastreamento ou URLs de destino, ou o prefixo de rastreamento está incorreto.

* A tag de rastreamento de conversão não está implementada corretamente em todas as páginas da Web aplicáveis ou foi editada.

* As métricas de conversão que Search, Social e Commerce estão rastreando são excluídas dos relatórios e, portanto, não estão visíveis.

* O analisador de receita do cliente não foi implementado.

*Possível solução ou solução alternativa:*

1. Verifique se as colunas corretas estão incluídas nos relatórios ou nas visualizações de dados. Se as colunas corretas não estiverem disponíveis para adição, você ou sua equipe de conta da Adobe devem [disponibilizar as métricas de conversão para os relatórios](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Verifique se as tags de rastreamento de conversão corretas estão implementadas em todas as páginas da Web aplicáveis. Se necessário, peça à sua equipe de conta da Adobe para criar uma transação de teste para cada tag de rastreamento de conversão aplicável e capturar os detalhes da transação, como `transactionid` e detalhes do cookie (como `trackingid`, `clickid` e assim por diante).

1. Se a opção [!UICONTROL Auto Upload] estiver desabilitada para a campanha e você tiver adicionado palavras-chave ou anúncios, verifique se você gerou um modelo de rastreamento ou URL de destino que inclui o rastreamento de redirecionamento de cliques de Pesquisa, Social e Commerce para cada um. Sua equipe de conta da Adobe pode executar um relatório interno para ver se algum URL de rastreamento de cliques (modelos de rastreamento ou URLs de destino) está ausente ou malformado.

   Se necessário, gere o rastreamento criando um arquivo de bulksheet com as URLs corretas e publique o arquivo na conta apropriada usando a opção **Gerar URLs de rastreamento**.

   O URL de destino deve começar com &quot;http://pixel.everesttech.net&quot; ou &quot;https://pixel.everesttech.net&quot;.

1. Se nenhuma dessas etapas resolver o problema, [entre em contato com o Atendimento ao Cliente](/help/search-social-commerce/get-help.md).

   Se o cliente não tiver sido iniciado ou se for iniciado recentemente, o Atendimento ao cliente verificará se um analisador de receita foi configurado. Se o analisador estiver configurado, eles verificarão se o Search, Social e Commerce está recebendo conversões de pixels e solucionarão o problema.

**Anunciantes enviando feeds de dados de conversão**

*Causas possíveis:*

* O arquivo de feed não foi entregue, não foi completamente analisado ou o feed continha transações órfãs.

* As métricas de conversão relevantes são excluídas dos relatórios e, portanto, não estão visíveis.

>[!NOTE]
>
>Os dados geralmente não aparecem na interface até 2 a 4 horas após o recebimento do feed.

*Possível solução ou solução alternativa:*

1. Verifique se as colunas corretas estão incluídas nos relatórios ou nas visualizações de dados. Se as colunas corretas não estiverem disponíveis para adição, você ou sua equipe de conta da Adobe devem [disponibilizar as métricas de conversão para os relatórios](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Execute o [!UICONTROL Portfolio Report]. Se estiver vazio, execute o [!UICONTROL Campaign Report] e o [!UICONTROL Search Engine Report] para ver se a receita aparece nesses relatórios. Se isso acontecer, as campanhas não poderão ser atribuídas ao portfólio apropriado.

1. Verifique se o arquivo foi enviado ao servidor de receita e se o arquivo seguiu o mesmo formato e a mesma convenção de nomenclatura de arquivos que os arquivos anteriores.

   Se a convenção de nomenclatura de formato ou arquivo foi alterada, corrija o arquivo e reenvie-o.

1. Se o arquivo foi enviado, [entre em contato com o Atendimento ao Cliente](/help/search-social-commerce/get-help.md).

   O Atendimento ao cliente verificará se o arquivo foi recebido e analisado. Se o arquivo foi processado sem erros, eles verificam transações órfãs.
+++

+++Alguns relatórios avançados não incluem dados de conversão fornecidos por um feed de anunciante.
O [!UICONTROL Geo Distribution Report] e o [!UICONTROL Domain Referral Report] usam dados capturados pelo serviço de rastreamento de conversão da Adobe Advertising e só podem ser gerados para anunciantes com o serviço. Os relatórios não incluem dados de conversão que são rastreados fora do sistema de rastreamento de conversão do Adobe Advertising.
+++

+++Os dados de receita são diferentes dos dados de receita do próprio anunciante.

**Anunciantes usando marcas de conversão do Adobe Advertising**

*Causas possíveis:*

* Search, Social e Commerce ignora a receita quando o cookie expira ou é excluído, mas o anunciante pode considerá-la receita válida.

* O tráfego para a página do anunciante veio de um marcador ou pesquisa orgânica em vez de um anúncio.

* A tag de rastreamento de conversão não está implementada corretamente em todas as páginas da Web aplicáveis ou foi editada.

*Possível solução ou solução alternativa:*

1. Vá para **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** e gere um [!UICONTROL Transaction Report]. Compare as transações que o Search, Social e Commerce recebeu com os dados do anunciante.

1. Se algumas transações estiverem incorretas ou ausentes, verifique se a tag de rastreamento de conversão relevante está implementada em todas as páginas da Web aplicáveis e não foi editada, a menos que a Equipe de conta da Adobe o aconselhe a fazê-lo. Uma tag pode estar ausente ou ter sido alterada se o site tiver sido atualizado recentemente.

   O Search, Social e Commerce espera URLs bem formadas (com parâmetros em pares nome-valor) dentro da variável `ef_transaction_properties` e dentro do elemento `src` da tag `img`.

1. Se você não puder determinar e resolver o problema, [contate o Atendimento ao Cliente](/help/search-social-commerce/get-help.md).

   O Atendimento ao cliente tentará identificar as transações ausentes e, em seguida, verificar se há transações órfãs e transações que não vieram de um anúncio (&quot;conversões não correlacionadas&quot;).

**Anunciantes com feeds de dados de conversão usando `ef_id` valores**

Veja as possíveis causas e soluções para implementações de pixel acima.

**Anunciantes com feeds de dados de conversão usando IDs de transação**

*Causas possíveis:*

* O Search, Social e Commerce ignora a receita quando o cookie expira ou é excluído, mas o anunciante pode considerá-la válida.

* O tráfego para a página do anunciante veio de um marcador ou pesquisa orgânica em vez de um anúncio.

* Uma conversão offline foi relatada antes de uma transação online ocorrer com a mesma ID de transação. A transação online deve ocorrer primeiro.

*Possível solução ou solução alternativa:*

1. Vá para **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** e gere um [!UICONTROL Transaction Report]. Compare as transações que o Search, Social e Commerce recebeu com os dados de feed do anunciante.

1. Se uma transação no arquivo de feed estiver ausente no relatório, verifique se uma transação online com a mesma ID de transação (rastreada pelo pixel) ocorreu antes da conversão offline.

1. Se você não puder determinar e resolver o problema, [contate o Atendimento ao Cliente](/help/search-social-commerce/get-help.md).

   O Atendimento ao cliente verificará se há erros de análise de dados e [transações órfãs](/help/search-social-commerce/glossary.md#o-p).

**Anunciantes com outros tipos de feeds de dados de conversão**

*Causas possíveis:*

* Search, Social e Commerce ignora a receita quando o cookie expira ou é excluído, mas o anunciante pode considerá-la receita válida.

* O tráfego para a página do anunciante veio de um marcador ou pesquisa orgânica em vez de um anúncio.

* Há [transações órfãs](/help/search-social-commerce/glossary.md#o-p), portanto, o Search, Social e Commerce não está contando toda a receita que deveria.

* O anunciante validou um relatório de Pesquisa, Social e Commerce em relação a um conjunto de dados diferente daquele enviado no feed.

* As IDs de transação (`ev_transid` valores) não foram enviadas, não são exclusivas ou estão incorretas.

* O arquivo de feed contém IDs de rastreamento duplicadas.

* Ocorreram erros quando o arquivo foi analisado.

* A lógica de desduplicação do anunciante é diferente da lógica de Pesquisa, Social e Commerce.

*Possível solução ou solução alternativa:*

1. Vá para **[!UICONTROL Insights]e[!UICONTROL Reports > Reports]** e gere um [!UICONTROL Transaction Report]. Compare as transações que o Search, Social e Commerce recebeu com os dados do anunciante.

1. Se algumas transações estiverem incorretas ou ausentes, verifique se a) o arquivo de feed contém todas as IDs de transação necessárias e nenhuma ID de rastreamento duplicada e b) as IDs de transação são exclusivas e corretas.

1. Se você não puder determinar e resolver o problema, [contate o Atendimento ao Cliente](/help/search-social-commerce/get-help.md).

   O Atendimento ao cliente verificará se há erros de análise de dados e transações órfãs.
+++

+++Os dados de receita são diferentes dos dados no Adobe Analytics
Consulte [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Relatórios específicos

+++O [!UICONTROL Portfolio Report] deve mostrar os mesmos números que a exibição [!UICONTROL Portfolios]?
A exibição [!UICONTROL Portfolio Report] e [!UICONTROL Portfolios] mostram os mesmos dados quando todos os filtros da exibição, os parâmetros do relatório e as colunas de dados da exibição e do relatório são os mesmos. Por exemplo, se a exibição [!UICONTROL Portfolios] mostrar portfólios que são &quot;[!UICONTROL All but inactive]&quot; para o intervalo de datas &quot;[!UICONTROL Last 7 days]&quot; e com apenas as colunas de dados padrão exibidas, uma [!UICONTROL Portfolio Report] usando os parâmetros padrão mostrará dados idênticos. Se você alterar qualquer um dos parâmetros do relatório ou usar filtros diferentes na exibição [!UICONTROL Portfolios], os valores de dados poderão ser diferentes.
+++

+++Os dados em meu [!UICONTROL Portfolio Report] não correspondem aos dados em meu [!UICONTROL Search Engine Report] ou [!UICONTROL Search Engine Account Report].
O [!UICONTROL Portfolio Report] mostra dados apenas para as campanhas atribuídas aos portfólios especificados, mas o [!UICONTROL Search Engine Report] e o [!UICONTROL Search Engine Account Report] também podem incluir dados para campanhas que não estão atribuídas a um portfólio.
+++

+++Qual a diferença entre o [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] e o [!UICONTROL Model Accuracy Report] no nível de portfólio?
(Somente para usuários de gerente de conta de agência, gerente de conta da Adobe e administrador) O [!UICONTROL Forecast Accuracy Report] disponível em [!UICONTROL Reports] > [!UICONTROL Model Accuracy] fornece os mesmos dados que o [!UICONTROL Model Accuracy Report] de nível de portfólio, exceto que você pode executá-lo em vários portfólios e alterar a regra de atribuição. Você também pode executar e agendar o relatório usando parâmetros personalizados e pode usá-lo para criar feeds de planilha. Além disso, o [!UICONTROL Forecast Accuracy Report] é mais preciso que o relatório de nível de portfólio herdado, pois avalia a precisão da receita usando os objetivos históricos do portfólio, em vez do objetivo atual, e representa com mais precisão os dados do fuso horário aplicável.
+++

+++Os dados no nível do anúncio não estão disponíveis para [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA), desempenho máximo, compras inteligentes e [!DNL YouTube] campanhas.
As redes de anúncios não fornecem o identificador necessário para atribuir receita a um anúncio individual dessas campanhas. Consequentemente, os dados de desempenho no nível do anúncio não estão disponíveis para esses tipos de campanha na visualização [!UICONTROL Ads] ou em [!UICONTROL Ad Variation Report]. Espere discrepâncias entre o total de dados de nível de anúncio de uma campanha e o total de dados da campanha.
+++

+++No [!UICONTROL Transaction Report], como sei qual métrica de conversão é de um feed de dados ou é rastreada pelo pixel de rastreamento do Adobe Advertising?
Em um relatório de transações, é possível saber se uma métrica de conversão incluída foi rastreada pelo pixel de rastreamento do Adobe Advertising ao incluir a coluna personalizada &quot;[!UICONTROL Tracking URL]&quot;. As URLs de rastreamento com o pixel de rastreamento Adobe Advertising começam com &quot;`http://pixel.everesttech.net`&quot;.
+++

+++Os dados em meu [!UICONTROL Transaction Report] não correspondem aos dados em meu [!UICONTROL Keyword Report].
Ao gerar ambos os relatórios por portfólio, os dados serão diferentes se você gerar o [!UICONTROL Keyword Report] usando dados históricos (isto é, com base na configuração do portfólio durante as datas especificadas) em vez de usar dados para as campanhas atuais. Quando você gera o [!UICONTROL Transaction Report] por portfólio, ele inclui dados para as campanhas atuais no portfólio.
+++

## Feeds de planilhas

+++A saída do relatório inclui uma combinação de intervalos de datas.
Você poderá ver intervalos de datas diferentes se o feed agregar dados usando qualquer nível de agregação de dados diferente de &quot;[!UICONTROL Daily]&quot;.

Para resolver o problema, atualize o feed da planilha para incluir dados agregados diariamente. Esta tarefa inclui a atualização do modelo de relatório, a geração de um relatório usando o modelo, a criação de um modelo [!DNL Microsoft Excel] personalizado usando o relatório e a atualização das configurações do feed para incluir o novo modelo do Excel. Para obter mais informações, consulte &quot;[Editar configurações do feed de relatório da planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

+++O feed de planilha resulta em um Erro interno.
Este erro poderá ocorrer se você alterar as colunas no modelo de relatório, mas não atualizar o modelo [!DNL Microsoft Excel] adequadamente.

Para resolver o problema, atualize o feed da planilha para incluir as novas colunas. Esta tarefa inclui a atualização do modelo de relatório, a geração de um relatório usando o modelo, a criação de um modelo [!DNL Excel] personalizado usando o relatório e a atualização das configurações do feed para incluir o novo modelo do Excel. Para obter mais informações, consulte &quot;[Editar configurações do feed de relatório da planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++

+++Quando tento abrir um feed de planilha no [!DNL Excel], o [!DNL Excel] relata um erro de &quot;conteúdo ilegível&quot; e os dados são removidos do conteúdo recuperado.
Quando o modelo [!DNL Microsoft Excel] não classifica os dados por data de início em ordem crescente, o feed da planilha pode incluir linhas em branco. Especificamente, [!DNL Excel] relata o erro &quot;O Excel encontrou conteúdo ilegível no &#39;&lt;*nome do relatório*>.xlsx.&#39; Deseja recuperar o conteúdo da pasta de trabalho? Se você confiar na origem desta pasta de trabalho, clique em sim.&quot; Se você clicar em &quot;Sim&quot;, receberá a seguinte mensagem: &quot;Registros removidos: informações da célula da parte /xl/worksheets/sheet1.xml&quot;, e o feed da planilha terá linhas em branco.

Para resolver o problema, edite o modelo [!DNL Excel] associado ao feed para classificar os dados por [!DNL Start date in Ascending (Oldest to Newest) order] e, em seguida, carregue o modelo atualizado por meio das configurações do feed de planilhas. Para obter mais informações, consulte &quot;[Editar feeds de relatório de planilha](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)&quot;.
+++
