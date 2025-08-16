---
title: O layout da árvore de decisão
description: Saiba mais sobre o layout da árvore de decisão para obter experiências com direcionamento.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# O layout da árvore de decisão para [!DNL Creative] experiências

Ao habilitar a opção &quot;[!UICONTROL Targeting]&quot; para uma experiência, você configura a experiência usando uma árvore de decisão.

Inicialmente, cada árvore decisória começa com o nível raiz, &quot;Tudo&quot;. Você pode adicionar um ou mais nós de destino e, em seguida, atribuir pacotes criativos aos nós finais em cada ramificação da árvore de decisão. Por padrão, a árvore de decisão é exibida verticalmente, mas você pode, opcionalmente, visualizá-la horizontalmente.

![Exemplo de uma árvore de decisão vertical sem destinos](/help/creative/assets/experience-decision-tree-no-targets.png "Exemplo de uma árvore de decisão vertical sem destinos")

![Exemplo de uma árvore de decisão horizontal sem destinos](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Exemplo de uma árvore de decisão horizontal sem destinos")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>-->

## Termos

**Árvore:** A estrutura de decisão geral como uma árvore com ramificações.

**Nó de Destino:** Um destino dentro de uma ramificação.

**Nó Folha:** um conjunto de criações atribuídas a um nó de destino final.

## Metas em uma árvore de decisão

Cada árvore decisória pode ter até cinco níveis de metas. Cada nível de destino pode incluir várias ramificações, cada uma com um ou mais nós com o mesmo tipo de destino (segmento de público-alvo, tipo de localização geográfica, valores para chaves de transmissão de dados especificadas, atributos para um pixel de redirecionamento especificado ou categoria de dispositivo). Você pode atribuir pacotes criativos em cada tamanho de anúncio para o qual especificou uma criação de imagem ou vídeo padrão para os nós de destino de nível mais baixo.

![Exemplo de uma árvore de decisão com destinos](/help/creative/assets/experience-decision-tree.png "Exemplo de uma árvore de decisão com destinos")

Ao adicionar um nó de destino ao nível final, você especifica o destino do novo nó. Um nó irmão adicional, &quot;Tudo mais&quot;, é criado automaticamente para todos que não correspondem ao público-alvo especificado. Em seguida, você pode adicionar outros nós irmãos com diferentes alvos do mesmo tipo.

No entanto, quando você insere um nó de destino entre níveis existentes, o primeiro nó do novo nível é atribuído inicialmente a &quot;Todos&quot;. Para identificar um destino específico, crie um nó de destino irmão no mesmo nível, para o qual especifique o destino real. Essa ação cria o nó de destino e substitui o nó &quot;All&quot; pelo nó &quot;Everything Else&quot; (que inclui todos os pacotes criativos atribuídos anteriormente a All). Em seguida, você pode adicionar outros nós irmãos com diferentes alvos do mesmo tipo.

Para todos os nós principais, você pode, opcionalmente, copiar todos os nós de destino secundários e pacotes criativos e colá-los em outro nó no mesmo nível. Você pode adicionar os nós colados à estrutura existente ou substituir a estrutura existente por eles.

## Criação em uma árvore de decisão

Atribua pacotes criativos a cada nó final de direcionamento na experiência.

Em cada nó com pacotes criativos, você pode, opcionalmente, girar as criações incluídas a) de acordo com pesos especificados ou b) de forma algorítmica para otimizar a taxa de cliques ou um objetivo personalizado. Opcionalmente, também é possível girar as criações em uma sequência de tempo especificada usando as mesmas opções.

Opcionalmente, é possível personalizar os URLs da página inicial, os URLs de rastreamento de impressão e os URLs de rastreamento de cliques, conforme necessário para criações individuais. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Sobre experiências no Advertising Creative 2.0](experience-about.md)
>* [Criar uma experiência com direcionamento](/help/creative/experiences/experience-create-targeting.md)
>* [Configurações de experiência direcionadas](/help/creative/experiences/experience-settings-targeting.md)
