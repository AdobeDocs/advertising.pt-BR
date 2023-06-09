---
title: Como as regras de atribuição são calculadas
description: Saiba como o Adobe Advertising calcula cada tipo de regra de atribuição.
source-git-commit: d4237253af7110a3ed02595c466c01359f5601d4
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Como as regras de atribuição são calculadas para o Adobe Advertising

*Anunciantes com rastreamento de conversão de anúncio Adobe somente*

<!-- Verify statements about cross-device events -->

A regra de atribuição no nível do anunciante é usada para atribuir dados de conversão — possivelmente em vários canais de anúncios — em uma série de eventos que levam a uma conversão.

Em relatórios, exibições padrão e personalizadas para Pesquisa de publicidade, Social, &amp; Commerce (Pesquisa, Social e Comércio) e (algumas funções de usuário) simulações em nível de portfólio para Pesquisa, Social e Comércio, a regra selecionada é usada somente para a exibição, relatório ou dados de simulação. As várias regras de atribuição são aplicadas da seguinte maneira:

>[!NOTE]
>
>* As regras de atribuição se aplicam a cliques em anúncios pagos em qualquer canal e a impressões em exibições e anúncios sociais. Elas não se aplicam a impressões para anúncios de pesquisa paga, que não podem ser rastreados no nível do evento.
>* A Adobe Advertising sempre armazena os seguintes eventos para cada surfer na Web antes de uma conversão: a) o primeiro clique pago; b) até 10 cliques para cada canal (pesquisa, social ou exibição), incluindo o primeiro clique; e c) até 10 impressões de exibição. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* No Advertising DSP e no Advertising Creative, as definições entre dispositivos consideram somente o caminho do evento da regra de atribuição selecionada.<!-- cross-device attribution via LiveRamp only -->
* Nas exibições de relatórios e gerenciamento, o número de casas decimais exibidas para um valor depende da moeda, mas o Adobe Advertising armazena valores mais precisos.

## Último evento (o padrão)

Atribui a conversão ao último clique pago da série no do anunciante [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) ou, se nenhum clique pago ocorreu, para a última impressão no [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j).

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

![Porcentagens de atribuição do último evento](/help/search-social-commerce/assets/attribution-percent-last-event.png "Porcentagens de atribuição do último evento")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Click1, Click2, Click3, Conversão de US$ 120

A conversão é atribuída ao Click 3 na quantidade de US$ 120.

### Exemplo com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Conversion of 120 USD

A conversão é atribuída ao Click 1 na quantidade de US$ 120.

### Exemplo com todas as impressões

**Nota:** Somente impressões para exibição e anúncios sociais são aplicáveis.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3, Conversão de 120 USD

A conversão é atribuída à Impressão 3. Como a conversão é um view-through, o método de avaliação view-through selecionado na seção &quot;Atribuição de conversão&quot; das configurações do relatório é aplicado:

* Se o parâmetro de relatório especificar um peso de view-through ponderado, esse peso será aplicado à view-through. Por exemplo, se o peso de view-through do anunciante for 40%, então 120 USD x 40% = 48 USD, então 48 USD é atribuído à Impressão 3.

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, nenhum peso de view-through será aplicado à view-through, e os 120 USD completos serão atribuídos à Impressão 3.

+++

<!-- end examples as collapsible content -->

## Primeiro evento

Atribui a conversão ao primeiro clique pago na série dentro do [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) ou, caso não tenham ocorrido cliques pagos, à primeira impressão no [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j). Essa regra está disponível somente para eventos em dispositivos únicos.

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

![Porcentagens da primeira atribuição de evento](/help/search-social-commerce/assets/attribution-percent-first-event.png "Porcentagens da primeira atribuição de evento")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Clique em 1, Clique em 2, Clique em 3, Conversão de US$ 120

A conversão é atribuída ao Click 1 na quantidade de US$ 120.

### Exemplo com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Conversion of 120 USD

A conversão é atribuída ao Click 1 na quantidade de US$ 120.

### Exemplo com todas as impressões

**Nota:** Somente impressões para exibição e anúncios sociais são aplicáveis.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3, Conversão de 120 USD

A conversão é atribuída à Impressão 1. Como a conversão é um view-through, o método de avaliação view-through selecionado na seção &quot;(Exibir campanhas) Atribuição de conversão&quot; das configurações do relatório é aplicado:

* Se o parâmetro de relatório especificar um peso de view-through ponderado, esse peso será aplicado à view-through. Por exemplo, se o peso de view-through do anunciante for 40%, então 120 x 40% = 48 USD, então 48 USD são atribuídos à Impressão 1.

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, nenhum peso de view-through será aplicado à view-through, e os 120 USD completos serão atribuídos à Impressão 1.

+++

<!-- end examples as collapsible content -->

## Peso Primeiro Evento Mais

Atribui a conversão a todos os eventos na série que ocorreram dentro do [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j), mas atribui mais peso ao primeiro evento e, sucessivamente, menos peso aos seguintes eventos. Essa regra está disponível somente para eventos em dispositivos únicos.

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

Quando o caminho de conversão inclui cliques pagos e impressões, as impressões são tratadas de forma diferente por diferentes produtos da Adobe Advertising:

* Em Pesquisa, Social e Comércio, a variável [peso de substituição de impressão](/help/search-social-commerce/glossary.md#i-j) — que é especificado na configuração de peso de substituição de impressão do anunciante e nos parâmetros de relatório, exibição ou simulação personalizada — é aplicado pela primeira vez às impressões.

* No DSP, as impressões são ignoradas e somente os cliques são ponderados. O DSP não leva os pesos de substituição de impressão em consideração para atribuição.

![Porcentagens de atribuição de mais peso do primeiro evento](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Porcentagens de atribuição de mais peso do primeiro evento")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Clique em 1, Clique em 2, Clique em 3, Conversão de US$ 120

Atribuição: Clique em 1 = 60 USD, Clique em 2 = 40 USD, Clique em 3 = 20 USD (total de 120 USD)

### Exemplos com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Somente Pesquisa, Social e Comércio) Uso do padrão &quot;Peso de substituição de impressão&quot; de 10%

Como a série de eventos incluía impressões e cliques, o peso de substituição de impressão se aplica às impressões.

Atribuição: Impressão 1 = 8 USD, Clique 1 = 72 USD, Impressão 2 = 4 USD, Clique 2 = 36 USD (total de 120 USD)

#### Uso de (somente DSP) sem Peso de substituição de impressão ou (somente Pesquisa, Social e Comércio) com &quot;Peso de substituição de impressão&quot; de 0%

Como a série de eventos inclui impressões e cliques, as impressões são ignoradas.

Atribuição: Impressão 1 = 0 USD, Clique 1 = 80 USD, Impressão 2 = 0 USD, Clique 2 = 40 USD (total de 120 USD)

### Exemplo com todas as impressões

**Nota:** Somente impressões para anúncios de exibição são aplicáveis.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3, Conversão de 120 USD

Como a conversão é um view-through, o método de avaliação view-through — em vez do peso de substituição de impressão — é aplicado para determinar o valor de cada impressão:

* Se o parâmetro de relatório tiver especificado um peso de view-through ponderado, esse peso será aplicado aos valores de impressão. Por exemplo, se o peso de view-through for 40%, então, Impressão 1 = 24 USD, Impressão 2 = 16 USD, Impressão 3 = 8 USD (total de 48 USD)

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, nenhum peso de view-through será aplicado à impressão, e o total de US$ 120 será dividido entre as três impressões: Impressão 1 = 60 US$, Impressão 2 = 40 US$, Impressão 3 = 20 US$ (total de 120 US$)

+++

<!-- end examples as collapsible content -->

## Distribuição par

>[!NOTE]
>
>Essa regra está disponível somente para eventos em dispositivos únicos.

Atribui a conversão igualmente a cada evento na série que ocorreu dentro do [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j).

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

Quando o caminho de conversão inclui cliques pagos e impressões, as impressões são tratadas de forma diferente por diferentes produtos da Adobe Advertising:

* Em Pesquisa, Social e Comércio, a variável [peso de substituição de impressão](/help/search-social-commerce/glossary.md#i-j) — que é especificado na configuração de peso de substituição de impressão do anunciante e nos parâmetros de relatório, exibição ou simulação personalizada — é aplicado pela primeira vez às impressões.

* No DSP, as impressões são ignoradas e somente os cliques são ponderados. O DSP não leva os pesos de substituição de impressão em consideração para atribuição.

![Porcentagens de atribuição uniformes](/help/search-social-commerce/assets/attribution-percent-even.png "Porcentagens de atribuição uniformes")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Clique em 1, Clique em 2, Clique em 3, conversão de 120 USD

Nenhuma impressão levou à conversão, portanto, o peso de substituição de impressão não é aplicável e a conversão é dividida igualmente entre os três cliques:

Atribuição: Clique em 1 = 40 USD, Clique em 2 = 40 USD, Clique em 3 = 40 USD (total de 120 USD)

### Exemplos com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Somente Pesquisa, Social e Comércio) Uso do padrão &quot;Peso de substituição de impressão&quot; de 10%

Como a série de eventos incluía impressões e cliques, o peso de substituição de impressão se aplica às impressões.

Atribuição: Impressão 1 = 6 USD, Clique 1 = 54 USD, Impressão 2 = 6 USD, Clique 2 = 54 USD (total de 120 USD)

#### Uso de (somente Adobe Advertising DSP) sem Peso de substituição de impressão ou (somente Pesquisa, Social e Comércio) com &quot;Peso de substituição de impressão&quot; de 0%

Como a série de eventos inclui impressões e cliques, as impressões são ignoradas.

Atribuição: Impressão 1 = 0 USD, Clique 1 = 60 USD, Impressão 2 = 0 USD, Clique 2 = 60 USD (total de 120 USD)

## Exemplo com todas as impressões

**Nota:** Somente impressões para anúncios de exibição são aplicáveis.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3, Conversão de 120 USD

Como a conversão é um view-through, o método de avaliação view-through — em vez do peso de substituição de impressão — é aplicado para determinar o valor de cada impressão:

* Se o parâmetro de relatório tiver especificado um peso de view-through ponderado, esse peso será aplicado aos valores de impressão. Por exemplo, se o peso de view-through for 40%, então, Impressão 1 = 16 USD, Impressão 2 = 16 USD, Impressão 3 = 16 USD (total de 48 USD)

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, nenhum peso de view-through será aplicado à impressão, e o total de US$ 120 será dividido entre as três impressões: Impressão 1 = US$ 40, Impressão 2 = US$ 40, Impressão 3 = US$ 40 (total de US$ 120)

+++

<!-- end examples as collapsible content -->

## Peso Último Evento Mais

Atribui a conversão a todos os eventos na série que ocorreram dentro do [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j), mas atribui mais peso ao último evento e, sucessivamente, menos peso aos eventos anteriores.

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

Quando o caminho de conversão inclui cliques pagos e impressões, as impressões são tratadas de forma diferente por produtos Adobe Advertising diferentes:

* Em Pesquisa, Social e Comércio, a variável [peso de substituição de impressão](/help/search-social-commerce/glossary.md#i-j) — que é especificado na configuração de peso de substituição de impressão do anunciante e nos parâmetros de relatório, exibição ou simulação personalizada — é aplicado pela primeira vez às impressões.

* No DSP, as impressões são ignoradas e somente os cliques são ponderados. O DSP não leva os pesos de substituição de impressão em consideração para atribuição.

![Porcentagens de atribuição de mais pesos do último evento](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Porcentagens de atribuição de mais pesos do último evento")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Clique em 1, Clique em 2, Clique em 3, Conversão de US$ 120

Atribuição: Clique em 3 = 60 USD, Clique em 2 = 40 USD, Clique em 1 = 20 USD (total de 120 USD)

### Exemplos com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Somente Pesquisa, Social e Comércio) Uso do padrão &quot;Peso de substituição de impressão&quot; de 10%

Como a série de eventos incluía impressões e cliques, o peso de substituição de impressão se aplica às impressões.

Atribuição: Impressão 1 = 4 USD, Clique 1 = 36 USD, Impressão 2 = 8 USD, Clique 2 = 72 USD (total de 120 USD)

#### Uso de (somente DSP) sem Peso de substituição de impressão ou (somente Pesquisa, Social e Comércio) com &quot;Peso de substituição de impressão&quot; de 0%

Como a série de eventos inclui impressões e cliques, as impressões são ignoradas.

Atribuição: Impressão 1 = 0 USD, Clique 1 = 40 USD, Impressão 2 = 0 USD, Clique 2 = 80 USD (total de 120 USD)

### Exemplo com todas as impressões

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3,Conversão de 120 USD

Como a conversão é um view-through, o método de avaliação view-through — em vez do peso de substituição de impressão — é aplicado para determinar o valor de cada impressão:

* Se o parâmetro de relatório tiver especificado um peso de view-through ponderado, esse peso será aplicado aos valores de impressão. Por exemplo, se o peso do view-through for 40%, multiplique cada valor em &quot;Exemplo com todos os cliques&quot; por 40%: Impressão 3 = 24 USD, Impressão 2 = 16 USD, Impressão 1 = 8 USD (total de 48 USD)

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, os 120 USD completos serão divididos entre as impressões: Impressão 3 = 60 USD, Impressão 2 = 40 USD, Impressão 1 = 20 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->

## Em forma de U

Atribui a conversão a todos os eventos na série que ocorreram dentro do [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j), mas atribui mais peso ao primeiro evento e aos últimos eventos, com peso sucessivamente menor para os eventos no meio do caminho de conversão.

Quando a conversão é precedida apenas por impressões, a conversão é considerada uma *view-through*, que é ponderado de acordo com o do anunciante [definição de intensidade de viewthrough](/help/search-social-commerce/glossary.md#uv) ou — conforme especificado — de acordo com o método de avaliação view-through especificado nos parâmetros relatório, view ou simulação personalizada.

Quando o caminho de conversão inclui cliques pagos e impressões, as impressões são tratadas de forma diferente por diferentes produtos da Adobe Advertising:

* Em Pesquisa, Social e Comércio, a variável [peso de substituição de impressão](/help/search-social-commerce/glossary.md#i-j) — que é especificado na configuração de peso de substituição de impressão do anunciante e nos parâmetros de relatório, exibição ou simulação personalizada — é aplicado pela primeira vez às impressões.

* No DSP, as impressões são ignoradas e somente os cliques são ponderados. O DSP não leva os pesos de substituição de impressão em consideração para atribuição.

![Porcentagens de atribuição em forma de U](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "Porcentagens de atribuição em forma de U")

<!-- start examples as collapsible content -->

+++Exemplos de cálculos de evento

### Exemplo com todos os cliques

Caminho do evento: Clique 1, Clique 2, Clique 3, Clique 4, Conversão de 120 USD

Atribuição: Clique em 1 = 36 USD, Clique em 2 = 24 USD, Clique em 3 = 24 USD, Clique em 4 = 36 USD (total de 120 USD)

### Exemplos com impressões e cliques

**Nota:** As impressões são aplicáveis somente a partir de anúncios de exibição e sociais.

Caminho do evento: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Somente Pesquisa, Social e Comércio) Uso do padrão &quot;Peso de substituição de impressão&quot; de 10%

Como a série de eventos incluía impressões e cliques, o peso de substituição de impressão se aplica às impressões.

Atribuição: Impressão 1 = 6 USD, Clique 1 = 54 USD, Impressão 2 = 6 USD, Clique 2 = 54 USD (total de 120 USD)

#### Usar (somente DSP) sem sobreposição de peso de impressão ou (somente Pesquisa, Social e Comércio) um &quot;Peso de sobreposição de impressão&quot; de 0%

Como a série de eventos inclui impressões e cliques, as impressões são ignoradas.

Atribuição: Impressão 1 = 0 USD, Clique 1 = 60 USD, Impressão 2 = 0 USD, Clique 2 = 60 USD (total de 120 USD)

### Exemplo com todas as impressões

**Nota:** Somente impressões para anúncios de exibição são aplicáveis.

Caminho do evento: Impressão 1, Impressão 2, Impressão 3, Impressão 4, Conversão de US$ 120

Como a conversão é um view-through, o método de avaliação view-through — em vez do peso de substituição de impressão — é aplicado para determinar o valor de cada impressão:

* Se o parâmetro de relatório tiver especificado um peso de view-through ponderado, esse peso será aplicado aos valores de impressão. Por exemplo, se o peso do view-through for 40%, clique em 1 = 14,40 USD, clique em 2 = 9,60 USD, clique em 3 = 9,60 USD, clique em 4 = 14,40 USD (total de 48 USD)

* Se o parâmetro de relatório especificar o uso de valores brutos para view-throughs, os 120 USD completos serão divididos entre as impressões: Clique em 1 = 36 USD, Clique em 2 = 24 USD, Clique em 3 = 24 USD, Clique em 4 = 36 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->
