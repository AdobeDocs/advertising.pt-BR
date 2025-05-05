---
title: Variações de dados esperadas entre  [!DNL Analytics]  e Adobe Advertising
description: Variações de dados esperadas entre  [!DNL Analytics]  e Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

Anunciantes com a integração do [!DNL Analytics for Advertising] <!-- (A4AdC) --> rastreiam anúncios pagos por meio do Adobe Advertising e do Adobe Analytics. Ao rastrear mídia, campanhas e canais por meio de vários sistemas, os mesmos conjuntos de dados de sistemas diferentes raramente correspondem completamente. Este documento explica como você deve esperar dados para a mídia que é traficada pelo Adobe Advertising para comparar com os dados nos diferentes sistemas nos quais a mídia é rastreada dentro do [!DNL Analytics].

>[!NOTE]
>
>Este documento se concentra no Adobe Advertising e no Analytics, mas muitos dos pontos principais também podem ser transferidos para outras soluções de rastreamento.

## Diferenças de atribuição em relatórios semelhantes

### Janelas de pesquisa e modelos de atribuição potencialmente diferentes

A integração [!DNL Analytics for Advertising] usa duas variáveis ([!DNL eVars] ou [!DNL rVars] \[reservado [!DNL eVars]]\) para capturar a [EF ID e a AMO ID](ids.md). Essas variáveis são configuradas com uma única janela de lookback (o tempo durante o qual click-throughs e view-throughs são atribuídos) e um modelo de atribuição. A menos que especificado de outra forma, as variáveis são configuradas para corresponder ao padrão, janela de retrospectiva de clique no nível do anunciante e modelo de atribuição no Adobe Advertising.

No entanto, as janelas de retrospectiva e os modelos de atribuição são configuráveis no Analytics (por meio do [!DNL eVars]) e no Adobe Advertising. Além disso, no Adobe Advertising, o modelo de atribuição é configurável não apenas no nível do anunciante (para otimização de lances), mas também em visualizações de dados e relatórios individuais (somente para fins de relatório). Por exemplo, uma organização pode preferir usar o modelo de atribuição de distribuição par para otimização, mas usar a atribuição de último contato para relatórios no Advertising DSP ou [!DNL Advertising Search, Social, & Commerce]. Alterar modelos de atribuição altera o número de conversões atribuídas.

Se uma janela de retrospectiva de relatório ou um modelo de atribuição for modificado em um produto e não no outro, os mesmos relatórios de cada sistema mostrarão dados distintos:

* **Exemplo de discrepâncias causadas por diferentes janelas de pesquisa:**

  Suponha que o Adobe Advertising tenha uma janela de retrospectiva de cliques de 60 dias e o [!DNL Analytics] tenha uma janela de retrospectiva de 30 dias. E suponha que um usuário chegue ao site através de um anúncio rastreado por Adobe Advertising, saia e retorne no dia 45 e converta. O Adobe Advertising atribui a conversão à visita inicial porque a conversão ocorreu dentro da janela de retrospectiva de 60 dias. [!DNL Analytics], no entanto, não pode atribuir a conversão à visita inicial porque a conversão ocorreu após a janela de retrospectiva de 30 dias expirar. Neste exemplo, o Adobe Advertising relata um número maior de conversões do que [!DNL Analytics].

  ![Exemplo de uma conversão atribuída ao Adobe Advertising, mas não ao [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exemplo de discrepâncias causadas por diferentes modelos de atribuição:**

  Suponha que um usuário interaja com três anúncios de Adobe Advertising diferentes antes da conversão, com a receita como o tipo de conversão. Se um relatório de Adobe Advertising usar um modelo de distribuição par para atribuição, ele atribuirá a receita uniformemente em todos os anúncios. No entanto, se [!DNL Analytics] usar o modelo de atribuição de último toque, ele atribuirá a receita ao último anúncio. No exemplo a seguir, o Adobe Advertising atribui um par de USD 10 dos 30 USD de receita capturados para cada um dos três anúncios, enquanto o [!DNL Analytics] atribui todos os 30 USD de receita ao último anúncio visto pelo usuário. Ao comparar relatórios de Adobe Advertising e [!DNL Analytics], você pode esperar ver o impacto da diferença na atribuição.

  ![Receita diferente atribuída ao Adobe Advertising e [!DNL Analytics] com base em diferentes modelos de atribuição](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>A prática recomendada é usar as mesmas janelas de retrospectiva e modelo de atribuição no Adobe Advertising e [!DNL Analytics]. Trabalhe com a equipe de conta do Adobe conforme necessário para identificar as configurações atuais e manter as configurações em sincronia.

Esses mesmos conceitos se aplicam a qualquer outro canal semelhante que use diferentes janelas de pesquisa ou modelos de atribuição.

#### Diferentes janelas de pesquisa para rastreamento de view-through {#impression-lookback}

No Adobe Advertising, a atribuição é baseada em cliques e impressões, e você pode configurar diferentes janelas de pesquisa para cliques e impressões. No [!DNL Analytics], no entanto, a atribuição é baseada em click-throughs e view-throughs, e você não tem a opção de definir diferentes janelas de atribuição para click-throughs e view-throughs; rastreamento para cada início na visita inicial ao site. Uma impressão pode ocorrer no mesmo dia ou vários dias antes de uma visualização ocorrer, e o tempo pode afetar o local em que a janela de atribuição começa em cada sistema.

Normalmente, a maioria das conversões view-through ocorre com rapidez suficiente para que ambos os sistemas atribuam crédito. No entanto, algumas conversões podem ocorrer fora da janela de retrospectiva de impressão de Adobe Advertising, mas dentro da janela de retrospectiva de [!DNL Analytics]; essas conversões são atribuídas ao view-through em [!DNL Analytics], mas não à impressão em Adobe Advertising.

No exemplo a seguir, suponha que um visitante recebeu um anúncio no Dia 1, realizou uma visita de view-through (ou seja, visitou a página de aterrissagem do anúncio sem clicar anteriormente no anúncio) no Dia 2 e converteu no Dia 45. Nesse caso, o Adobe Advertising rastrearia o usuário dos Dias 1 a 14 (usando uma retrospectiva de 14 dias), o [!DNL Analytics] rastrearia o usuário dos Dias 2 a 61 (usando uma retrospectiva de 60 dias) e a conversão no Dia 45 seria atribuída ao anúncio em [!DNL Analytics], mas não em Adobe Advertising.

![Exemplo de uma conversão de view-through atribuída em [!DNL Analytics], mas não em Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Uma outra causa de discrepâncias é que, no Adobe Advertising, você pode atribuir conversões view-through a um *peso view-through* personalizado relativo ao peso atribuído a uma conversão baseada em cliques. O peso de view-through padrão é de 40%, o que significa que uma conversão de view-through é contada como 40% do valor de uma conversão baseada em cliques. [!DNL Analytics] não fornece essa ponderação de conversões view-through. Assim, por exemplo, uma ordem de receita de US$ 100 capturada em [!DNL Analytics] é descontada em US$ 40 em Adobe Advertising se você estiver usando o peso view-through padrão — uma diferença de US$ 60.

Considere estas diferenças ao comparar conversões de view-through entre relatórios Adobe Advertising e [!DNL Analytics].

#### Modelos de atribuição disponíveis

| Atribuição de Adobe Advertising | Atribuição [!DNL Analytics] | Alocação de [!DNL eVar]/[!DNL rVar] |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/d | n/d |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Não usar* |
| [!UICONTROL Weight Last Event More] | n/d | n/d |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/d |
| n/d | [!UICONTROL J-Shaped] | n/d |
| n/d | [!UICONTROL Inverse-J] | n/d |
| n/d | [!UICONTROL Custom] | n/d |
| n/d | [!UICONTROL Participation] | n/d |
| n/d | [!UICONTROL Algorithmic] | n/d |

>[!NOTE]
>
>Para alocação linear, [!DNL Analytics] atribui eventos bem-sucedidos igualmente em todos os valores [!DNL eVar] em uma única visita. Portanto, use alocação linear com uma expiração [!DNL eVar] de &quot;Visita&quot;. No entanto, para anúncios, o uso da atribuição linear leva a uma alocação que não é realmente linear e a relatórios que não são ideais. Por exemplo, se um visitante interagir com três anúncios antes de converter em três visitas separadas, somente o anúncio visto na última visita será atribuído à conversão, não todos os três anúncios.
>
>Além disso, alternar a alocação de conversão de ou para &quot;Linear&quot; impede que os dados históricos sejam exibidos, o que pode levar a dados incorretos nos relatórios. Por exemplo, a alocação linear pode dividir a receita em vários valores [!DNL eVar] diferentes. Se você alterar a alocação para &quot;Mais recente&quot;, 100% dessa receita será associada ao valor único mais recente. Essa associação pode levar a conclusões incorretas.
>
>Para evitar confusão, [!DNL Analytics] torna os dados históricos indisponíveis na interface de relatórios. Você pode visualizar os dados históricos se alterar a [!DNL eVar] de volta para a configuração de alocação inicial, embora não deva alterar as configurações de alocação de [!DNL eVar] simplesmente para acessar os dados históricos. A Adobe recomenda usar um novo [!DNL eVar] quando você quiser aplicar uma nova configuração de alocação para dados que já estão sendo registrados, em vez de alterar as configurações de alocação para um [!DNL eVar] que já tem uma quantidade significativa de dados históricos.

Consulte uma lista de modelos de atribuição [!DNL Analytics] e suas definições em [https://experienceleague.adobe.com/pt-br/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/pt-br/docs/analytics/analyze/analysis-workspace/attribution/models).

Se você estiver conectado ao [!DNL Search, Social, & Commerce], poderá encontrar uma lista

* (Usuários na América do Norte) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Todos os outros usuários) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Atribuição de data de evento no Adobe Advertising

No Adobe Advertising, você pode relatar dados de conversão pela data de clique/data do evento associado (a data do evento de clique ou impressão) ou pela data da transação (data de conversão). O conceito de relatório de data de clique/evento não existe em [!DNL Analytics]; todas as conversões rastreadas em [!DNL Analytics] são relatadas por data da transação. Como resultado, a mesma conversão pode ser reportada com datas diferentes em Adobe Advertising e [!DNL Analytics]. Por exemplo, considere um usuário que clica em um anúncio em 1º de janeiro e converte em 5 de janeiro. Se você estiver visualizando os dados de conversão por data de evento no Adobe Advertising, a conversão será relatada em 1º de janeiro, quando o clique ocorreu. Em [!DNL Analytics], a mesma conversão é relatada em 5 de janeiro.

![Exemplo de uma conversão atribuída a datas diferentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Atribuição em [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] relatórios](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=pt-BR) permite configurar regras para identificar diferentes canais de marketing com base em aspectos distintos das informações de ocorrência. Você pode rastrear canais rastreados por Adobe Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] e [!UICONTROL Paid Search]) como [!DNL Marketing Channels] usando o parâmetro de cadeia de caracteres de consulta `ef_id` para identificar o canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> No entanto, mesmo que os relatórios do [!DNL Marketing Channels] possam rastrear canais de Adobe Advertising, os dados podem não corresponder aos relatórios de Adobe Advertising por vários motivos. Consulte as seções a seguir para obter mais informações.

>[!NOTE]
>
> Os conceitos principais a seguir também se aplicam a qualquer rastreamento de vários canais que envolva campanhas não rastreadas no Adobe Advertising, como a variável [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=pt-BR) (também conhecida como dimensão &quot;Código de rastreamento&quot; ou &quot;[!DNL eVar] 0&quot;) e rastreamento [!DNL eVar] personalizado.

### Modelos de Atribuição Possivelmente Diferentes em [!DNL Marketing Channels]

A maioria dos relatórios do [!DNL Marketing Channels] está configurada com a atribuição [!UICONTROL Last Touch], para a qual o último canal de marketing detectado recebe 100% do valor de conversão. O uso de modelos de atribuição diferentes para os relatórios do [!DNL Marketing Channels] e do Adobe Advertising gera discrepâncias nas conversões atribuídas.

### Uma Janela de Pesquisa Potencialmente Diferente em [!DNL Marketing Channels]

A janela de retrospectiva para [!DNL Marketing Channels] pode ser personalizada. No Adobe Advertising, a janela de retrospectiva de cliques é configurável, embora uma janela fixa de 60 dias seja comum. Se os dois produtos usarem janelas de pesquisa diferentes, você poderá esperar discrepâncias de dados.

### Atribuição de canal diferente em [!DNL Marketing Channels]

Os relatórios de Adobe Advertising capturam apenas mídia paga traficada pelo Adobe Advertising (pesquisa paga para [!DNL Advertising Search, Social, & Commerce] anúncios e exibição para anúncios do Advertising DSP), enquanto os relatórios de [!DNL Marketing Channels] podem rastrear todos os canais digitais. Isso pode levar a uma discrepância no canal para o qual uma conversão é atribuída.

Por exemplo, os canais de pesquisa paga e pesquisa natural muitas vezes têm uma relação simbiótica, em que cada canal auxilia o outro. O relatório [!DNL Marketing Channels] atribui algumas conversões à pesquisa natural que o Adobe Advertising não atribui porque ele não rastreia a pesquisa natural.

Considere também um cliente que visualiza um anúncio de exibição, clica em um anúncio de pesquisa pago, clica em uma mensagem de email e coloca um pedido de US$ 30. Mesmo se Adobe Advertising e [!DNL Marketing Channels] usarem o modelo de atribuição de último contato, a conversão ainda será atribuída de forma diferente a cada um. O Adobe Advertising não tem acesso ao canal [!UICONTROL Email], portanto, ele creditaria a pesquisa paga pela conversão. [!DNL Marketing Channels], no entanto, tem acesso aos três canais, portanto, creditaria [!UICONTROL Email] pela conversão.

![Exemplo de atribuição de conversão diferente no Adobe Advertising versus [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Para obter mais explicações sobre por que as métricas podem variar, consulte &quot;[Por que os dados de canal podem variar entre Adobe Advertising e  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;.

## Diferenças de Dados no Adobe Analytics [!DNL Paid Search Detection]

O recurso [legado [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=pt-BR) em [!DNL Analytics] permite que as empresas [definam regras para rastrear o tráfego de pesquisa orgânica e paga](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=pt-BR) de mecanismos de pesquisa especificados. As regras [!DNL Paid Search Detection] usam uma sequência de consulta e o domínio referenciador para identificar o tráfego de pesquisa natural e pago. Os relatórios [!DNL Paid Search Detection] fazem parte de um grupo maior de relatórios [Métodos de descoberta](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=pt-BR), que expiram quando ocorre um evento especificado (como uma Finalização de carrinho) ou quando a visita termina.

Esta é a interface para criar um conjunto de regras [!DNL Paid Search Detection]:

![Exemplo de uma regra de Detecção de Pesquisa Paga definida em [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Os relatórios [!DNL Paid Search Detection] resultantes incluem os relatórios [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] e [!UICONTROL Natural Search Keywords].

Observe as duas limitações a seguir com dados em [!DNL Paid Search Detection] relatórios:

* Os relatórios [!UICONTROL Paid Search Keywords] e [!UICONTROL Natural Search Keywords] mostram as consultas de pesquisa conforme identificadas pelas URLs de referência, não as palavras-chave nas quais os usuários fazem lances. Os relatórios Adobe Advertising e [!DNL Analytics] mostram as palavras-chave reais, portanto, não espere que elas se alinhem aos relatórios de palavra-chave [!DNL Paid Search Detection].

* Quando o recurso [!DNL Paid Search Detection] foi criado originalmente, a consulta de pesquisa de origem (a sequência de caracteres inserida pelo usuário na barra de pesquisa do mecanismo de pesquisa) estava mais prontamente disponível para anunciantes através da URL de referência. Atualmente, os mecanismos de pesquisa ofuscam amplamente a consulta de pesquisa, e os relatórios de palavra-chave [!DNL Paid Search Detection] têm valor limitado, pois a maioria dos dados de consulta se enquadra em &quot;não especificado&quot;.

  Com o [!DNL Analytics for Advertising], os anunciantes ainda poderão rastrear palavras-chave pagas no [!DNL Analytics]. O domínio referenciador informa aos relatórios do mecanismo qual mecanismo de pesquisa direcionou o tráfego. Como as informações de conta específicas do anunciante não estão vinculadas ao domínio referenciador, todo o tráfego é listado no mecanismo de pesquisa. Os anunciantes com várias contas no mesmo mecanismo de pesquisa devem consultar os relatórios do Adobe Advertising ou [!DNL Analytics] para obter relatórios específicos da conta.

### Por que configurar o [!DNL Paid Search Detection]?

Os relatórios [!DNL Paid Search Detection] permitem identificar o tráfego de pesquisa natural nos [[!DNL Analytics Marketing Channels] relatórios](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=pt-BR). Separar o tráfego de pesquisa paga do tráfego de pesquisa natural é uma ótima maneira de entender o valor que a pesquisa natural traz para o ecossistema de marketing completo.

## Validação de Dados de Click-Through para [!DNL Analytics for Advertising] {#data-validation}

Na sua integração, você deve validar os dados de click-through para garantir que todas as páginas do site estejam rastreando click-throughs corretamente.

No [!DNL Analytics], uma das maneiras mais fáceis de validar o rastreamento de [!DNL Analytics for Advertising] é comparar instâncias com cliques usando uma métrica calculada &quot;Instâncias de ID do AMO para cliques&quot;, que é calculada da seguinte forma:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] representa o número de vezes que [IDs AMO](ids.md) são rastreadas no site. Sempre que um anúncio é clicado, um parâmetro de ID do AMO (`s_kwcid`) é adicionado ao URL da página de aterrissagem. O número de [!UICONTROL AMO ID Instances], portanto, é análogo ao número de cliques e pode ser validado em relação aos cliques de anúncios reais. Geralmente vemos uma taxa de correspondência de 85% para [!DNL Search, Social, & Commerce] e uma taxa de correspondência de 30% para tráfego [!DNL DSP] (quando filtrados para incluir somente click-through [!UICONTROL AMO ID Instances]). A diferença nas expectativas entre pesquisa e exibição pode ser explicada pelo comportamento do tráfego esperado. A pesquisa captura a intenção e, como tal, os usuários geralmente pretendem clicar nos resultados da pesquisa de sua consulta. Os usuários que visualizam uma exibição ou anúncio de vídeo online, no entanto, têm mais probabilidade de clicar no anúncio involuntariamente e, em seguida, saltar do site ou abandonar a nova janela que é carregada antes que a atividade da página seja rastreada.

Nos relatórios de Adobe Advertising, você pode comparar instâncias a cliques de maneira semelhante usando a métrica &quot;[!UICONTROL EF ID Instances]&quot; em vez de [!UICONTROL AMO ID Instances]:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Embora você deva esperar uma alta taxa de correspondência entre a ID AMO e a ID EF, não espere 100% de paridade porque a ID AMO e a ID EF rastreiam basicamente dados diferentes, e essa diferença pode levar a pequenas diferenças no total [!UICONTROL AMO ID Instances] e [!UICONTROL EF ID Instances]. No entanto, se o total [!UICONTROL AMO ID Instances] em [!DNL Analytics] diferir de [!UICONTROL EF ID Instances] em Adobe Advertising em mais de 1%, entre em contato com a equipe de conta do Adobe para obter assistência.

Para obter mais informações sobre a ID AMO e a ID EF, consulte [IDs de Adobe Advertising usadas pelo Analytics](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Solução de problemas de disparidades entre cliques e instâncias

Se a relação [!UICONTROL EF ID Instances] para cliques estiver abaixo de 85%, verifique o seguinte:

* O rastreamento de cliques da conta ou de qualquer subnível está ausente, ou você tem um rastreamento de cliques duplicado (por exemplo, nos níveis da conta e da campanha)?

  Em Pesquisar, Social e Commerce, [baixe um bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) para a conta verificar as URLs de rastreamento.

  Além disso, em [!DNL Analytics], você pode ver se a ID do AMO e EF IF são anexados consistentemente usando uma métrica calculada de &quot;[!DNL AMO ID] a [!DNL EF ID]&quot;, que é calculada da seguinte maneira:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Um valor maior que 100% indica que estão faltando mais IDs EF do que IDs AMO.

* A página de aterrissagem tem um problema de carregamento para que a ID do AMO e a ID do EF não sejam capturadas?

* O URL da página de aterrissagem é redirecionado para que a ID AMO e a ID EF sejam perdidas?

* Todas as páginas de destino usam o conjunto de relatórios configurado?

>[!NOTE]
>
>Em teoria, é possível que uma instância tenha vários cliques. Verifique se há cliques em diferentes dispositivos (como desktop, dispositivo móvel e tablet).

## Comparando Conjuntos de Dados em [!DNL Analytics for Advertising] com o Adobe Advertising

A [ID do AMO](ids.md) (parâmetro de cadeia de caracteres de consulta s_kwcid) é usada para relatórios em [!DNL Analytics], e a [ID do EF](ids.md) (parâmetro de cadeia de caracteres de consulta ef_id) é usada para relatórios em Adobe Advertising. Como são valores distintos, é possível que um valor seja corrompido ou não seja adicionado à landing page.

Por exemplo, suponha que tenhamos a seguinte landing page:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

onde EF ID é &quot;`test_ef_id`&quot; e AMO ID é &quot;`test_amo_id`&quot;.

Se ocorrer um redirecionamento do lado do site, o URL poderá terminar assim:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

onde EF ID é &quot;`test_ef_id`&quot; e AMO ID é &quot;`test_amo_id#redirectAnchorTag`&quot;.

Neste exemplo, a adição da tag de âncora adiciona caracteres inesperados à ID do AMO, resultando em um valor que o Analytics não reconhece. Essa ID do AMO não seria classificada, e as conversões associadas a ela se enquadravam em &quot;[!UICONTROL unspecified]&quot; ou &quot;[!UICONTROL none]&quot; nos relatórios [!DNL Analytics].

Felizmente, embora problemas como esse sejam comuns, eles normalmente não resultam em uma alta porcentagem de discrepância. No entanto, se você notar uma grande discrepância entre as IDs AMO em [!DNL Analytics] e as IDs EF no Adobe Advertising, entre em contato com a equipe de conta do Adobe para obter assistência.

## Outras considerações de métrica

### A diferença entre cliques e visitas {#clicks-vs-visits}

Parecem análogos, mas os cliques e as visitas representam dados diferentes:

* **Clique em:** [!DNL DSP] ou o mecanismo de pesquisa registra um clique quando um visitante clica em um anúncio no site de um editor.

* **A Visita** [!DNL Analytics] define uma [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=pt-BR) como uma série de exibições de página por um usuário, terminando de acordo com um de vários critérios, como 30 minutos de inatividade.

Por definição, um clique pode levar a várias visitas.

Considere o exemplo a seguir: O usuário 1 e o usuário 2 acessam um site clicando em um anúncio de Adobe Advertising. O usuário 1 visualiza quatro páginas e depois sai para o dia, de modo que o clique inicial resulta em uma visita. O usuário 2 visualiza duas páginas, sai para um almoço de 45 minutos, retorna, visualiza mais duas páginas e depois sai; nesse caso, o clique inicial resulta em duas visitas.

![Exemplo da diferença entre cliques e visitas](/help/integrations/assets/a4adc-visits-example.png)

### A diferença entre cliques e click-throughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Cliques e click-throughs são duas métricas diferentes:

* **Clique em:** [!DNL DSP] ou o mecanismo de pesquisa registra um clique quando um visitante clica em um anúncio no site de um editor.

* **Click-throughs:** [!DNL Analytics] registra um click-through quando o visitante chega ao site de destino, a página de aterrissagem é carregada e a solicitação [!DNL Analytics] na parte inferior da página envia os dados para [!DNL Analytics].

Os cliques e click-throughs podem ser muito diferentes devido aos cliques acidentais do anúncio. Observamos que a maioria dos cliques nos anúncios de exibição são cliques acidentais, e esses visitantes acidentais clicam no botão Voltar antes que a página de aterrissagem seja carregada, portanto, o [!DNL Analytics] não pode registrar um click-through. Isso é especialmente verdadeiro para anúncios nos quais um clique acidental é mais provável, como anúncios móveis, anúncios de vídeo e anúncios que preenchem a tela e devem ser fechados antes que o usuário possa visualizar a página.

Os sites carregados em dispositivos móveis também têm menos probabilidade de resultar em click-throughs, devido às menores larguras de banda ou à potência de processamento disponível, fazendo com que as landing pages demorem mais para carregar. Não é incomum que 50 a 70% dos cliques não resultem em click-throughs. Em ambientes móveis, a diferença pode ser de até 90% devido à combinação de um navegador mais lento e à maior probabilidade de o usuário clicar acidentalmente no anúncio enquanto percorre a página ou tenta fechar o anúncio.

Os dados de cliques também podem ser registrados em ambientes que não podem gravar click-throughs com os mecanismos de rastreamento atuais (como cliques entrando, ou vindo, de um aplicativo móvel) ou para os quais o anunciante implantou apenas uma abordagem de rastreamento (por exemplo, com a abordagem de view-through do JavaScript, os navegadores que bloqueiam cookies de terceiros rastreiam cliques, mas não click-throughs). Um motivo importante pelo qual a Adobe recomenda a implantação das abordagens de rastreamento de URL de cliques e de rastreamento de view-through do JavaScript é maximizar a cobertura de click-throughs rastreáveis.

### Utilização de métricas de tráfego de Adobe Advertising para Dimension não-Adobe Advertising

O Adobe Advertising fornece ao Analytics [métricas de tráfego específicas de publicidade e as dimensões relacionadas de [!DNL DSP] and [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). As métricas fornecidas por Adobe Advertising são aplicáveis apenas às dimensões de Adobe Advertising especificadas e os dados não estão disponíveis para outras dimensões em [!DNL Analytics].

Por exemplo, se você exibir as métricas [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] por Conta, que é uma dimensão de Adobe Advertising, o total de [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] será mostrado por conta.

![Exemplo de métricas Adobe Advertising em um relatório usando uma dimensão Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

No entanto, se você exibir as métricas [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] por uma dimensão na página (como Página), para a qual o Adobe Advertising não fornece dados, as métricas [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] para cada página serão zero (0).

![Exemplo de métricas de Adobe Advertising em um relatório usando uma dimensão sem suporte](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Usando [!UICONTROL AMO ID Instances] como substituto para cliques com Dimension não Adobe Advertising

Como você não pode usar [!UICONTROL AMO Clicks] com dimensões no site, talvez queira encontrar um equivalente a cliques. Você pode ser tentado a usar as Visitas como substitutas, mas elas não são a melhor opção porque cada visitante pode ter várias visitas. (Consulte &quot;[A Diferença Entre Cliques e Visitas](#clicks-vs-visits)&quot;.) Em vez disso, recomendamos usar [!UICONTROL AMO ID Instances], que é o número de vezes que a ID do AMO é capturada. Embora [!UICONTROL AMO ID Instances] não corresponda exatamente a [!UICONTROL AMO Clicks], eles são a melhor opção para medir o tráfego de cliques no site. Para obter mais informações, consulte &quot;[Validação de Dados de Click-Through para [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Exemplo de [!UICONTROL AMO ID Instances] em vez de [!UICONTROL Adobe Advertising Clicks] para uma dimensão sem suporte](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [IDs de Adobe Advertising Usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Métricas de Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Por que os dados podem variar entre Adobe Advertising e  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
