---
title: Glossário
description: Consulte as definições de termos principais.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Glossário {#glossary}

*Beta fechado*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** Um clique de anúncio que resulta em uma conversão.

**destino da transmissão de dados:** os destinos da transmissão de dados permitem que os elementos de anúncio sejam selecionados com base nos dados fornecidos em tempo real pela DSP, pelo editor ou pelo parceiro. Isso pode incluir dados de terceiros.

<!-- verify this -->Em uma experiência de anúncio, cada destino de transmissão de dados pode incluir até cinco pares de valores chave; você especifica as chaves e pelo menos um valor no primeiro nó de destino nesse nível e as mesmas chaves estão disponíveis para nós de destino irmãos. Cada um dos pares de valor-chave é anexado como uma macro à tag de publicidade dessa experiência. No momento da impressão do anúncio, o DSP, editor ou parceiro é responsável pela substituição dos valores por dados específicos para essa impressão. As informações são passadas de volta para [!DNL Creative] para que ele possa mostrar uma experiência de anúncio apropriada com base nas regras definidas na experiência.

Por exemplo, para direcionar um ou mais possíveis criadores para visualizadores que são do sexo feminino e estão no Segmento 1234, você configuraria os destinos da transmissão de dados `gender=female` e `segment=1234` para o nó de destino. A DSP que produz a impressão preenche a tag com as informações de gênero e segmento, e os visitantes que atendem aos requisitos especificados recebem uma das criações associadas.

**engagement-through:** Um envolvimento de anúncio (como rolar por um anúncio do carrossel ou expandir um anúncio) que resulta em uma conversão. Esse tipo de evento é separado do clique no anúncio para acessar uma página de aterrissagem ou um evento na página de aterrissagem.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**viewthrough:** uma impressão de anúncio, ou sequência de impressões, que resulta em uma conversão sem que o usuário clique em um anúncio.
