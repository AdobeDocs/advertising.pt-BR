---
title: especificação criativa do HTML5
description: Consulte a especificação criativa de HTML para Advertising Creative.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# especificação criativa do HTML para o Advertising Creative

Este documento descreve os requisitos e o suporte de API para criações de HTML5 no [!DNL Creative]. A API permite o desenvolvimento de criativos HTML5 cujos atributos podem ser configurados no momento da entrega criativa.

## Escopo

O [!DNL Creative] oferece suporte a banners HTML5 com criações de mídia não-avançada que aparecem dentro de bordas definidas em uma página. Você pode usar os seguintes tipos de criações de HTML5:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** oferece suporte a até 5 URLs de página de aterrissagem que podem ser configuradas durante a criação criativa e o tráfico.

* **HTML flexível5:** oferece suporte a até 5 URLs de página de aterrissagem que podem ser configuradas durante a criação criativa e o tráfico, além de permitir que atributos criativos sejam modificados durante a criação criativa e o tráfico.

## Requisitos

### Requisitos de pasta e compactação

* O criativo deve ser empacotado em um arquivo ZIP (formato .ZIP). Arquivos ZIP aninhados não são suportados, portanto, não inclua uma pasta compactada dentro da pasta compactada externa.

* O arquivo ZIP deve conter pelo menos um arquivo HTML — o arquivo de exibição do HTML principal — que inclui uma referência à biblioteca JavaScript [!DNL Creative]. O arquivo HTML principal pode estar na pasta raiz ou em uma subpasta.

* O arquivo HTML principal pode ser nomeado como qualquer coisa, desde que não inclua caracteres especiais, embora `index.html` seja recomendado.

* Todos os ativos de suporte necessários para renderizar o criativo final devem estar na mesma pasta que o arquivo de exibição do HTML ou em subpastas na pasta principal.

* Não inclua nenhum arquivo no criativo que não esteja referenciado para esse criativo.

### Inclusão do arquivo Advertising Creative JavaScript

O arquivo HTML principal — e nenhum outro arquivo — deve conter uma referência ao arquivo JavaScript `AMOLibrary.js`. Chame o arquivo na primeira linha da seção `<head>` usando este endereço:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Esse arquivo contém funções para garantir que o teste local de eventos de saída ocorra sem problemas.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### requisitos de criação do HTML5

#### Suporte para URLs click-through no HTML estático 5

##### `amo.registerClick(clkVar, clkUrl)`

Registra as URLs de click-through e o parâmetro associado usado para fazer referência a cada URL (conhecido como `clickTag`). Isso informa o servidor de publicidade [!DNL Creative] onde adicionar o rastreamento de cliques. Você pode usar essa API para registrar até cinco variáveis de tag de clique, cada uma com um URL de página inicial correspondente.

>[!NOTE]
>
>Os URLs estáticos incluídos no criativo do HTML5 são usados apenas para fins de teste local e serão substituídos. Ao carregar um criativo HTML5, você definirá a página de aterrissagem padrão para cada variável `clickTag`. Ao atribuir um criativo HTML5 carregado a uma experiência de anúncio, você pode, opcionalmente, substituir a página de aterrissagem padrão para cada variável `clickTag` e o [!DNL Creative] adiciona o rastreamento de cliques às URLs ao salvar a experiência.

###### Parâmetros

* `clkVar` — O nome da variável click (geralmente &quot;clickTag&quot;), entre aspas duplas.

* `clkUrl` — O URL da página de aterrissagem para esta variável de clique, entre aspas duplas.

###### Uso

Chame `amo.registerClick()` na seção `<head>` do arquivo HTML principal.

###### Exemplo

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Aciona o evento de saída, que redireciona o usuário para a página de aterrissagem configurada para `clickTag`. Durante os testes locais, essa função alerta os desenvolvedores se o URL que está sendo passado para a função foi registrado.

###### Parâmetros

* `clkTag` — O nome da variável de clique usada para atribuir o URL da página de aterrissagem usando a função `amo.registerClick()`, entre aspas simples.

* `event` — (Opcional) O objeto de evento &quot;click&quot; do JavaScript. Isso registra as coordenadas de cliques, que podem ser usadas para analisar ainda mais o desempenho criativo.

###### Uso

Chame `amo.onAdClick()` na seção `<body>` do arquivo HTML principal.

###### Exemplos

`amo.onAdClick('clickTag')` OU `amo.onAdClick('clickTag',clickEvt)`

### Requisitos criativos flexíveis do HTML5

#### Suporte para URLs click-through no HTML flexível5

##### `amo.registerClick(clkVar, clkUrl)`

Registra as URLs de click-through e o parâmetro associado usado para fazer referência a cada URL (conhecido como `clickTag`). Isso informa o servidor de publicidade [!DNL Creative] onde adicionar o rastreamento de cliques. Você pode usar essa API para registrar até cinco variáveis de tag de clique, cada uma com um URL de página inicial correspondente.

>[!NOTE]
>
>Os URLs estáticos incluídos no criativo do HTML5 são usados apenas para fins de teste local e serão substituídos. Ao carregar um criativo HTML5, você definirá a página de aterrissagem padrão para cada variável `clickTag`. Ao atribuir um criativo HTML5 carregado a uma experiência de anúncio, você pode, opcionalmente, substituir a página de aterrissagem padrão para cada variável `clickTag` e o [!DNL Creative] adiciona o rastreamento de cliques às URLs ao salvar a experiência.

###### Parâmetros

* `clkVar` — O nome da variável click (geralmente &quot;clickTag&quot;), entre aspas duplas.

* `clkUrl` — O URL da página de aterrissagem para esta variável de clique, entre aspas duplas.

###### Uso

Chame `amo.registerClick()` na seção `<head>` do arquivo HTML principal.

###### Exemplo

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Aciona o evento de saída, que redireciona o usuário para a página de aterrissagem configurada para `clickTag`. Durante os testes locais, essa função alerta os desenvolvedores se o URL que está sendo passado para a função foi registrado.

###### Parâmetros

* `clkTag` — O nome da variável de clique usada para atribuir o URL da página de aterrissagem usando a função `amo.registerClick()`, entre aspas simples.

* `event` — (Opcional) O objeto de evento &quot;click&quot; do JavaScript. Isso registra as coordenadas de cliques, que podem ser usadas para analisar ainda mais o desempenho criativo.

###### Uso

Chame `amo.onAdClick()` na seção `<body>` do arquivo HTML principal.

###### Exemplos

`amo.onAdClick('clickTag')` OU `amo.onAdClick('clickTag',clickEvt)`

#### Suporte para atributos criativos no HTML flexível5

##### `amo.registerAttribute(key, type, value)`

Define os atributos das criações que podem ser alteradas no momento da criação ou criação da experiência. É possível definir até 20 atributos criativos que podem ser configurados no momento da criação ou da criação da experiência.

>[!NOTE]
>
>Os valores definidos neste método são usados apenas para desenvolvimento local e não são usados em veiculação de anúncios ao vivo.

###### Parâmetros

* `key` — O nome alfanumérico do atributo. Deve começar com um caractere alfabético.

* `type` — O tipo de atributo (`TEXT` ou `IMAGE`).

* `value` — O valor do atributo para teste. Para atributos do tipo `IMAGE`, o valor deve ser o caminho relativo para o arquivo de imagem.

###### Uso

Chame `amo.registerAttribute()` para registrar um atributo criativo, tipo e valor durante o teste no modo local. Todos os arquivos de imagem usados como valores de amostra devem ser empacotados no arquivo ZIP juntamente com o pacote carregado.

##### `amo.attributes`

Um objeto JSON para consultar os nomes e valores da variável do atributo criativo. As chaves do objeto serão os nomes dos atributos e os valores serão os valores desses atributos.

No modo de teste local, os pares de valores chave são os pares registrados pela API `amo.registerAttribute`. Para produção, os nomes e valores das variáveis do atributo criativo devem ser configurados no momento da criação criativa e do tráfico.

### Requisitos de conteúdo criativo

A maioria das trocas de exibição disponíveis no Advertising DSP tem os seguintes requisitos criativos:

* Todas as imagens de anúncios devem ter uma borda sólida.

* Não são permitidos anúncios em expansão.

* A landing page deve abrir em uma nova janela.

* O domínio da página de aterrissagem e seus subdomínios não podem ter mais de 35 caracteres. **Observação:** as URLs da página de aterrissagem final são definidas no DSP e não nos ativos HTML5 propriamente ditos.

* Qualquer isenção de responsabilidade da oferta de um anúncio deve ser incluída no próprio anúncio e não apenas na landing page.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Exemplo de conteúdo como um objeto e uma matriz JSON

### Exemplo de conteúdo como um objeto JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Exemplo de conteúdo como uma matriz JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Exemplo de criação de HTML5

### Exemplo de estrutura de pasta (após a descompactação)

* index.html

* /assets (pasta)

   * bg.jpg (JPG,, PNG, SVG ou imagem GIF)

### Exemplo de arquivo HTML (index.html) para criações de HTML5 simples

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Exemplo de arquivo HTML (index.html) para criações de HTML 5 estáticas

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Adicionar criações padrão a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-standard.md)
