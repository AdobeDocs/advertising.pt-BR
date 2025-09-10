---
title: Glossário
description: Consulte as definições de termos principais.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '2308'
ht-degree: 0%

---

# Glossário {#glossary}

## A-B {#a-b}

**grupo de anúncios:** um conjunto de anúncios e suas palavras-chave, posicionamentos e grupos de produtos relacionados para uma campanha.

**Variação de anúncio:** qualquer anúncio dentro de um grupo de anúncios ou estratégia de publicidade.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id):** Um código de rastreamento que permite à Adobe Advertising compartilhar dados sobre campanhas com a Adobe Analytics e a Adobe Customer Journey Analytics. Começa com `s_kwcid=`.

**unidade de oferta:** um termo de Pesquisa, Social e Commerce para uma unidade na qual são feitas ofertas.

* Para campanhas CPC, esta é uma palavra-chave e seu tipo de correspondência para uma campanha de pesquisa ou conteúdo, um grupo de produtos no nível da unidade (o nível mais baixo de subdivisão) para uma campanha de compras ou um destino de pesquisa dinâmica para uma campanha de publicidade de pesquisa dinâmica. Quando a mesma combinação de palavra-chave e tipo de correspondência, o mesmo grupo de produtos ou o mesmo público-alvo de pesquisa dinâmica ocorre em vários grupos de anúncios em uma única campanha, todas as instâncias são consideradas a mesma unidade de oferta e, portanto, têm a mesma oferta.

* Para campanhas com as estratégias de gastos [!DNL Maximize Clicks], [!DNL Maximize Conversion Value], [!DNL Maximize Conversions], [!DNL Target Cost Per Acquisition] ou [!DNL Target Return on Ad Spend], cada campanha é uma unidade de oferta.

* Para campanhas em [!DNL Yahoo! Display Network], que não usa palavras-chave, todos os anúncios em um grupo de anúncios têm a mesma oferta e são considerados a mesma unidade de oferta.

**restrição de unidade de oferta:** Consulte &quot;restrição&quot;.

## C-D {#c-d}

**campanha:** um conjunto de grupos de anúncios em uma única conta de anúncio que compartilham um orçamento, intervalo de tempo, direcionamento e outras configurações. **Observação:** [!DNL Baidu] não tem o conceito de campanhas, mas o Search, Social e Commerce cria pseudo-campanhas para cada conjunto de grupos de anúncios relacionados em contas do [!DNL Baidu] existentes que são sincronizadas no Search, Social e Commerce.

**campo com diferenciação de maiúsculas e minúsculas:** um campo ou consulta com diferenciação de maiúsculas e minúsculas trata as letras maiúsculas (como C) de forma diferente das letras minúsculas (como c). Por exemplo, Carro é tratado como um valor diferente de carro.

**clique:** Um clique único do usuário em um anúncio online ou dentro dele.

**janela de retrospectiva de cliques:** Uma configuração no nível do anunciante que especifica o número de dias após a ocorrência de um clique pago em uma série de eventos em que o clique pode ser atribuído a uma conversão.

**hora do clique:** a hora em que um usuário final com um endereço IP exclusivo clica pela primeira vez em um anúncio na rede de anúncios.

**taxa de click-through:** (CTR) O número de cliques dividido pelo número de impressões em um anúncio. Os anúncios mais relevantes para a consulta de pesquisa têm as taxas de click-through mais altas.

**URL de rastreamento de cliques:** Um modelo de rastreamento ou uma URL de destino com código incorporado para rastrear cliques em uma palavra-chave, variação de anúncio ou posicionamento.

**restrição:** (anunciantes com portfólios; aplicável somente para unidades de oferta em portfólios padrão) uma regra para licitação em uma palavra-chave ou anúncio específico. Ele substitui todos os limites no nível do portfólio e a estratégia de lances recomendada.

**conversão:** a conclusão de uma ação depois que um usuário final clica em um anúncio, geralmente capturado como uma métrica. Os exemplos incluem registros e compras e podem representar contagens ou valores monetários. Uma conversão pode consistir em um ou mais eventos de transação, mas os termos &quot;conversão&quot; e &quot;transação&quot; são frequentemente usados alternadamente.

**rastreamento de conversão:** o rastreamento de conversão usa cookies para rastrear a) cliques nos anúncios de um anunciante nas redes de anúncios e b) as transações resultantes no site do anunciante.

**precisão de custo:** (Anunciantes com portfólios) O gasto real de um portfólio dividido pelo gasto previsto. [Relatórios de precisão de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicam a precisão dos modelos de custo que são usados para otimização e o [[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) inclui mais detalhes, além de recomendações para melhorar a precisão do modelo.

**modelo de custo:** (anunciantes com portfólios) Tecnologia de pesquisa, social e Commerce que prevê o volume de custo, a oferta necessária para ganhar cada posição ou posicionamento e o CPC (pesquisa) ou o CPM (exibição) para cada unidade de oferta usando dados históricos e técnicas de previsão matemática.

**cobertura de modelo de custo:** (anunciantes com portfólios) o número e/ou a porcentagem de unidades de oferta em campanhas CPC ou eCPC que receberam pelo menos uma impressão nos últimos sete dias para que o recurso de otimização possa criar modelos de custo. Nem todas as unidades de oferta têm modelos de custo; as unidades de oferta com modelos de custo contam para a cobertura do modelo de custo.

**meia-vida do modelo de custo:** (Anunciantes com portfólios) O número de dias antes da data atual para a qual os dados de custo são considerados mais recentes e, portanto, mais relevantes para modelos de custo.

**custo por 1000 impressões:** (CPM) o custo de um anúncio para cada mil impressões. Os anunciantes que usam um modelo de preços do CPM pagam por impressões em vez de cliques.

**custo por aquisição:** (CPA) O custo de um anúncio dividido pelo número de conversões. Também chamado de custo por transação (CPT) ou custo por ordem (CPO).

**custo por clique:** (CPC) 1) O custo de um anúncio dividido pelo número total de cliques no anúncio. Por exemplo, se você gastar US$ 100 para criar uma impressão de anúncio e o anúncio gerar 10 cliques, o custo por clique será de US$ 100/10=10 por clique. 2) Um modelo de preços no qual os anunciantes são cobrados por cada clique de anúncio.

**custo por pedido:** (CPO) o custo de um anúncio dividido pelo número de pedidos. Também chamado de custo por aquisição (CPA) ou custo por transação (CPT).

**custo por transação:** (CPT) O custo de um anúncio dividido pelo número de transações. Também chamado de custo por aquisição (CPA).

**CPA:** Consulte &quot;custo por aquisição&quot;.

**CPC:** Consulte &quot;custo por clique&quot;.

**CPM:** Consulte &quot;custo por 1000 impressões&quot;.

**CPO:** Consulte &quot;custo por pedido&quot;.

**CPT:** Consulte &quot;custo por transação&quot;.

**CSV:** um formato de arquivo que consiste em valores separados por vírgula (CSV).

**CTR:** Consulte &quot;taxa de cliques&quot;.

## E-F {#e-f}

**eCPM:** o CPM efetivo ou o custo médio pago por 1000 impressões durante um intervalo de datas especificado. Os valores de eCPM podem ser calculados para campanhas do CPM ou CPC.

## G-H {#g-h}

**meia-vida:** o tempo necessário para que uma quantidade diminua para metade de seu valor inicial. Para cada portfólio, é possível especificar meia-vida para indicar por quanto tempo os dados são relevantes para modelos de custo e de receita.
Consulte &quot;meia-vida do modelo de custo&quot; e &quot;meia-vida do modelo de receita&quot;.

## I-J {#i-j}

**impressão:** uma única exibição de um anúncio em uma página da Web, aplicativo móvel ou outra mídia de entrega. Um usuário não precisa visualizar ou clicar no anúncio para que ele conte como uma impressão.

**janela de retrospectiva de impressão:** (Somente campanhas sociais e de exibição) uma configuração no nível do anunciante que especifica o número de dias após a ocorrência de uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão.

**peso de substituição de impressão:** uma porcentagem especificada de um valor de conversão para atribuir a impressões que ocorrem na janela de retrospectiva de impressão do cliente quando a conversão é precedida por cliques pagos e impressões. Quando uma conversão é precedida apenas por impressões, o peso de view-through do anunciante, em vez do peso de substituição de impressão, é aplicado às impressões.

## K-L {#k-l}

**palavra-chave:** uma palavra ou frase associada a um anúncio.

**restrição de palavra-chave:** Consulte &quot;restrição&quot;.

**classificação de rótulo:** uma maneira de agrupar os componentes da conta em conjuntos significativos. Uma classificação de etiqueta pode conter vários valores de etiqueta, que indicam atributos. Por exemplo, uma classificação de rótulo &quot;Geográfico&quot; pode incluir valores para diferentes regiões geográficas.

**valor do rótulo:** um elemento de uma classificação de rótulo. Ele pode ser atribuído como uma tag a campanhas de publicidade e entidades de campanha para que você possa filtrar dados e relatórios de desempenho por rótulo ou configurar restrições opcionais em unidades de oferta associadas ao rótulo.

**URL da página de aterrissagem:** o URL da página da Web do anunciante que abre quando o usuário final clica em um anúncio.

## M-N {#m-n}

**custo marginal:** a alteração no custo total quando a quantidade é alterada por uma unidade.

**valor de custo marginal para objetivo:** a alteração no custo necessária para aumentar o valor do objetivo em um (1). Ela tem o mesmo valor da coluna herdada &quot;Custo-para-Receita Marginal&quot;.

**tipo de correspondência:** uma opção que especifica como os termos de pesquisa são correspondidos aos anúncios. As opções variam de acordo com a rede de anúncios.

**lance mínimo:** 1) O valor mínimo a ser pago por impressão ou por 1000 impressões. 2) Para palavras-chave de pesquisa, o lance mínimo necessário para uma determinada palavra-chave com base em sua pontuação de qualidade. O lance mínimo é geralmente o menor valor que você pode pagar por clique para que sua palavra-chave mostre anúncios.

**precisão do modelo:** (anunciantes com portfólios) a porcentagem de precisão dos modelos de custo e de receita usados para otimizar ofertas, orçamentos de campanha e metas de estratégia de oferta para um portfólio. Consulte &quot;modelo de custo&quot;, &quot;precisão de custo&quot;, &quot;modelo de receita&quot; e &quot;precisão da receita&quot;.

## O-P {#o-p}

**objetivo:** (anunciantes com portfólios) uma meta que um cliente define para atender ao seu objetivo comercial para um portfólio específico ou uma campanha de exibição, como maximizar lucros ou atingir uma meta de vendas específica. Um objetivo consiste nas métricas de conversão a serem rastreadas e otimizadas para o portfólio e nos pesos relativos dessas métricas. O total das conversões ponderadas da carteira é calculado como &quot;valor objetivo&quot;.

**valor do objetivo:** (anunciantes com portfólios) o total de conversões ponderadas, conforme calculado de acordo com o objetivo atual do portfólio, incluindo:

* todas as conversões, tendo em conta a) os pesos atribuídos a cada conversão no objetivo do portfólio e, quando aplicável, b) o peso de view-through para view-throughs.

* todos os cliques, que o recurso de otimização considera uma única conversão e é ponderado de acordo com o valor de clique do objetivo.

Ela tem o mesmo valor da coluna herdada &quot;Receita ponderada&quot;.

**recurso de otimização:** (anunciantes com portfólios) Tecnologia de lance por palavras-chave de Pesquisa, Social e Commerce, que determina a estratégia ideal de lance e gerenciamento de orçamento para um portfólio com base em seu objetivo comercial.

**transação órfã:** um evento de transação que não pode ser associado a uma palavra-chave ou anúncio específico.

**pixel:** Uma imagem transparente, de um pixel por um pixel, inserida em uma página da Web para fins de rastreamento. As tags de rastreamento de conversão do Adobe Advertising incluem um pixel de imagem do HTML ou o JavaScript para rastrear cliques e suas transações resultantes.

**posicionamento:** um local em uma rede de exibição no qual seus anúncios podem aparecer. Pode ser um site inteiro, um subconjunto de um site ou uma posição de anúncio em uma página específica.

**portfólio:** um conjunto de campanhas de publicidade e suas unidades de oferta associadas, que são otimizadas para um único objetivo comercial e um destino de desempenho.

**PDV:** porcentagem do gasto

**PPC:** Consulte &quot;pagamento por clique&quot;.

**propriedade:** Consulte &quot;métrica de conversão&quot;.

**hora da propriedade:** a hora em que um evento de conversão individual ocorre. Quando um evento inclui eventos de acompanhamento relacionados (como um cliente que se registra primeiro em uma avaliação gratuita e depois se inscreve em um serviço pago), cada evento tem seu próprio tempo de propriedade.

## Q-R {#q-r}

**pontuação de qualidade:** uma pontuação que uma rede de publicidade atribui a uma de suas palavras-chave para determinar o preço de oferta e a posição do anúncio. Ela é calculada de acordo com a relevância da palavra-chave para seu anúncio associado e para a consulta de pesquisa do usuário, a taxa de cliques da palavra-chave e outros fatores.

**URL de redirecionamento:** Parte de uma URL de destino que envia o usuário para outro servidor antes, ou em vez, da página de aterrissagem do anunciante.

**retorno do investimento:** (ROI) Receita menos custos.

**precisão da receita:** (anunciantes com portfólios) a receita real de um portfólio dividida pela receita prevista. [Os relatórios de precisão do modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicam a precisão dos modelos de receita usados para otimização e o [[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) inclui mais detalhes, além de recomendações para melhorar a precisão do modelo.

**modelo de receita:** (anunciantes com portfólios) Tecnologia de pesquisa, social e Commerce que prevê a taxa de conversão e o retorno estimado para cada unidade de oferta, com base nos dados de clique (pesquisa e social) ou nos dados de impressão (exibição) e nos dados de conversão do anunciante.

**cobertura do modelo de receita:** (Anunciantes com portfólios) O número e/ou porcentagem de unidades de oferta em um portfólio com modelos de receita. As unidades de oferta podem ter modelos de receita, mesmo que não tenham recebido receita, mas tenham recebido impressões.

**meia-vida do modelo de receita:** (Anunciantes com portfólios) O número de dias antes da data atual para a qual os dados de receita são considerados mais recentes e, portanto, mais relevantes para modelos de receita.

**ROI:** Consulte &quot;retorno sobre o investimento&quot;.

## S-T {#s-t}

**simulação:** (anunciantes com portfólios) modelagem de Portfolio que estima o número de cliques e conversões que um portfólio pode esperar para diferentes níveis de gastos e orçamentos diários correspondentes, usando dados históricos.

**Estratégia de gastos:** (anunciantes com portfólios) a estratégia selecionada para otimizar ofertas de palavras-chave/anúncios para um portfólio.

**`s_kwcid`:** Consulte &quot;ID do AMO&quot;.

**modelo de rastreamento:** (contas somente com URLs finais) O modelo de rastreamento ou a URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora a URL final/avançada em um parâmetro. Para o rastreamento de conversão do Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce prefixa automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.

**URL de rastreamento:** Um modelo de rastreamento ou uma URL de destino com parâmetros extras adicionados para rastrear informações sobre cliques no anúncio. Ele pode incluir um URL de redirecionamento para enviar os usuários inicialmente para um servidor de rastreamento antes de redirecioná-los para a página de aterrissagem do anunciante.

**transação:** Qualquer evento rastreável que ocorra online ou offline. Vários eventos de transação podem ser rastreados juntos como parte da mesma transação ou conversão; por exemplo, uma solicitação on-line de informações, além de um pedido resultante por telefone, pode ser considerada componentes de uma compra. Os termos &quot;transação&quot; e &quot;conversão&quot; são frequentemente usados alternadamente. Uma transação é representada por uma ID de transação e tem uma ou mais propriedades associadas a ela.

**ID da transação:** Uma ID especificada pelo anunciante que identifica uma transação. Quando uma transação inclui vários eventos, todos têm a mesma ID de transação.

**propriedade de transação:** Consulte &quot;conversão&quot;.

**hora da transação:** a hora em que um clique ou uma impressão é convertida em uma transação. Quando uma transação consiste em vários eventos de transação (como quando um cliente se registra pela primeira vez em uma avaliação gratuita e depois se inscreve em um serviço pago), o tempo da transação vem do primeiro evento na cadeia (registro na avaliação gratuita).

**TSV:** um formato de arquivo que consiste em valores separados por tabulação (CSV).

## U-V {#u-v}

**viewthrough:** (Exibição e anúncios sociais) uma impressão de anúncio (ou sequência de impressões) que resulta em uma conversão sem que o usuário clique em um anúncio.

**peso de view-through:** (somente campanhas sociais e de exibição) uma configuração no nível do anunciante que especifica o peso a ser atribuído a uma conversão de view-through relativa ao peso atribuído a uma conversão baseada em cliques, como uma porcentagem.

## W-X {#w-x}

**objetivo ponderado:** Consulte &quot;objetivo&quot;.

**receita ponderada:** Consulte &quot;valor do objetivo&quot;.

**XLS** ou **XLSX**: um formato de arquivo binário para pastas de trabalho [!DNL Microsoft Office Excel].

## Y-Z {#y-z}
