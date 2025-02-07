---
title: Glossário
description: Consulte as definições de termos principais.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Glossário {#glossary}

*Beta fechado*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**click-through:** Um clique de anúncio que resulta em uma conversão.

**destino da transmissão de dados:** os destinos da transmissão de dados permitem que os elementos de anúncio sejam selecionados com base nos dados fornecidos em tempo real pelo DSP, editor ou parceiro. Isso pode incluir dados de terceiros.

<!-- verify this -->Em uma experiência de anúncio, cada destino de transmissão de dados pode incluir até cinco pares de valores chave; você especifica as chaves e pelo menos um valor no primeiro nó de destino nesse nível e as mesmas chaves estão disponíveis para nós de destino irmãos. Cada um dos pares de valor-chave é anexado como uma macro à tag de publicidade dessa experiência. No momento da impressão do anúncio, o DSP, editor ou parceiro é responsável pela substituição dos valores por dados específicos para essa impressão. As informações são passadas de volta para [!DNL Creative] para que ele possa mostrar uma experiência de anúncio apropriada com base nas regras definidas na experiência.

Por exemplo, para direcionar um ou mais possíveis criadores para visualizadores que são do sexo feminino e estão no Segmento 1234, você configuraria os destinos da transmissão de dados `gender=female` e `segment=1234` para o nó de destino. O DSP que veicula a impressão preenche a tag com as informações de gênero e segmento, e os visitantes que atendem aos requisitos especificados recebem uma das criações associadas.

**engagement-through:** um envolvimento de anúncio (como assistir a um vídeo ou expandir um anúncio) que resulta em uma conversão.

<!-- or flexible html5 creative variation? -->
**variação de um criativo HTML5 flexível:** uma derivação de um ativo criativo HTML5 flexível em seu [!UICONTROL Creative Libraries], que é gerado ao atribuir o criativo a uma experiência e alterar qualquer um dos atributos padrão na experiência.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**viewthrough:** uma impressão de anúncio, ou sequência de impressões, que resulta em uma conversão sem que o usuário clique em um anúncio.
