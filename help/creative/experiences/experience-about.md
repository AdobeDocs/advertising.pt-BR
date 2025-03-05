---
title: Sobre experiências no Advertising Creative
description: Saiba como configurar experiências de anúncio personalizadas e otimizar elementos de anúncio com base no desempenho.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Sobre as experiências no Advertising Creative 2.0

*Beta fechado*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] fornece duas estruturas de experiência de anúncio diferentes para os anúncios em uma biblioteca criativa<!-- can use a single library only -->:

* **Experiências com direcionamento de árvore de decisão:** [!DNL Creative] permite configurar experiências de anúncio personalizadas em toda a jornada do cliente usando um modelo de árvore de decisão. Você pode personalizar todos os elementos de anúncios — imagens, títulos, ofertas e páginas de aterrissagem — com base no público-alvo.

  Por exemplo, você pode especificar o mesmo pacote criativo para as pessoas em Chicago e Nova York que estão em um segmento específico de público-alvo do Adobe Analytics, mas enviar as pessoas em Chicago que estão no mesmo segmento para páginas de aterrissagem diferentes de Nova York. Você também pode especificar um pacote diferente para as pessoas no segmento que vivem em qualquer lugar, exceto Chicago e Nova York, e um terceiro pacote para outras pessoas que não estão no segmento.

  As opções de direcionamento incluem visualizadores em seus segmentos de público-alvo primários da Adobe Audience Manager, Adobe Analytics e Advertising Cloud DSP; visualizadores em localizações geográficas específicas, incluindo países, estados, DMAs nos Estados Unidos, cidades e CEPs; visualizadores para os quais pares de valores-chave específicos (alvos de transmissão de dados) são transmitidos pela DSP, publicador ou parceiro; visualizadores com [!DNL Creative] pixels de redirecionamento e valores de atributo especificados; e visualizadores com tipos de dispositivo, sistemas operacionais e navegadores específicos.

  Você pode atribuir pacotes criativos a cada experiência, opcionalmente personalizando a otimização e o agendamento dos pacotes criativos e alterando as páginas de aterrissagem padrão e as URLs de rastreamento<!-- and any flexible attributes --> para criações individuais em cada pacote.

* **Experiências sem direcionamento de árvore de decisão:** [!DNL Creative] otimiza os elementos de anúncio para a experiência de anúncio sem restringir o público.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Você especificará datas de início e término e algumas configurações padrão para cada experiência, mas grande parte do fluxo de trabalho não está diretamente dentro da experiência. Em vez de adicionar criações diretamente à experiência, você cria uma tag de anúncio para cada tamanho de anúncio da experiência e adiciona criações a ela, configura a otimização criativa e o agendamento e personaliza as páginas de aterrissagem e URLs de rastreamento de dentro do [!UICONTROL Tag Manager].

## Otimização de anúncios

<!-- MORE -->
O [!DNL Creative] otimiza os elementos de anúncio para qualquer experiência com base no desempenho. Para experiências direcionadas a públicos-alvo específicos, os anúncios podem ser otimizados com base no desempenho dos elementos de anúncios individuais para os conjuntos de públicos-alvo. Para experiências sem metas de público-alvo específicas, os elementos de anúncio são otimizados com base apenas no desempenho dos elementos de anúncio individuais.

## Implementação e gerenciamento de experiências

Depois de criar uma experiência ao vivo (com todos os elementos de anúncio necessários), você pode [gerar uma tag de JavaScript ou iframe para toda a experiência](experience-tag-export.md), que você pode, opcionalmente, carregar como um anúncio para uma campanha no Adobe Advertising DSP ou implementar como um anúncio em uma DSP de terceiros. [!DNL Creative] veicula anúncios para a experiência com base nas opções de direcionamento e rotação de anúncios, bem como no inventário de anúncios disponível.

## Dados de desempenho para suas experiências

Ao habilitar a opção [!UICONTROL Metrics] na exibição [!UICONTROL Experiences], cada cartão ou linha de experiência indica o número de impressões e cliques recebidos pela experiência.

![Opção de métricas](/help/creative/assets/metrics-option.png "Opção de métricas")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Você pode ver dados detalhados do desempenho de qualquer experiência da visualização [!UICONTROL Creative] > [!UICONTROL Experiences]. Para monitorar o desempenho em suas experiências, crie um [!UICONTROL Custom Creative Report].

<!--
You can [view detailed performance data for any experience](experience-performance-details.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## Status da experiência {#experience-statuses}

<!-- verify that these are all still the same -->

O status de uma experiência é definido automaticamente, exceto por *excluído*, que você definiu manualmente.

*Ao vivo:* a experiência inclui todos os elementos necessários, de modo que você possa gerar uma marca de experiência para implementar como um anúncio em uma DSP. <!-- A live experience may be scheduled to start in the future -->

*Rascunho:* Todas as ramificações da experiência não recebem criações, portanto, a experiência está incompleta e você não pode gerar uma marca de experiência.

*Processando:* uma experiência online anterior foi editada, mas agora está incompleta. Não é possível gerar uma tag de experiência para ela. **Observação:** se você já implementou uma marca de experiência para a experiência, a versão ativa anterior ainda será disponibilizada. Se posteriormente você concluir a experiência, tornando-a ativa novamente, a nova versão será disponibilizada usando a implementação de tag existente.

*Excluída:* a experiência foi excluída de [!DNL Creative] e não está mais visível nos modos de exibição [!UICONTROL Experiences].

>[!NOTE]
>
>Você pode alterar o status de um anúncio em uma DSP sem afetar o status da experiência em [!DNL Creative].

## A visualização [!UICONTROL Experiences]

A exibição [!UICONTROL Experiences] mostra todas as suas experiências de direcionamento e de não direcionamento. Você pode ver os nomes da experiência, o status, as datas de início e término, o número e as dimensões dos pacotes criativos ou criativos atribuídos e se a experiência inclui anúncios dinâmicos. Ao habilitar a opção [!UICONTROL Metrics] na exibição [!UICONTROL Experiences], cada cartão ou linha de experiência indica o número de impressões e cliques recebidos pela experiência.

Você pode criar e gerenciar suas experiências, incluindo otimização e atribuição de criativos e pacotes criativos às suas experiências. Você também pode criar e renomear tags de experiência de anúncio e exportar as tags nos formatos JavaScript e iframe para implementação em seus DSPs. Como opção, os anunciantes com o Advertising DSP podem fazer upload de tags diretamente em uma campanha do Advertising DSP como anúncios.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Criar uma experiência sem direcionamento](experience-create-no-targeting.md)
