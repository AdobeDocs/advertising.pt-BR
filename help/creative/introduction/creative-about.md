---
title: Sobre o Adobe Advertising Creative
description: Saiba mais sobre  [!DNL Creative].
feature: Creative Introduction
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Sobre o Adobe Advertising Creative 2.0

*Beta fechado*

<!-- verify all and rewrite to include new stuff -->

Como parte do Adobe Advertising, o Advertising Creative é uma plataforma de autoatendimento para automatizar experiências de anúncios personalizados em tempo real e, opcionalmente, otimizar seus anúncios no nível do elemento criativo.

## Bibliotecas criativas personalizadas de criativos reutilizáveis

Suas bibliotecas Creative permitem gerenciar os elementos de criação que você usará em suas experiências de anúncio. Você pode criar várias bibliotecas, cada uma com criações e grupos criativos individuais (chamados de *pacotes*). Você adicionará pacotes criativos às suas experiências de anúncio.

## Experiências baseadas em regras

Com o [!DNL Creative], você pode criar histórias usando um modelo de árvore decisória baseado em regras — desdobrando uma cadeia coreografada de anúncios que são personalizados em tempo real com base no que você conhece sobre o seu público-alvo e que seguem seus clientes mesmo quando eles mudam para sites diferentes<!-- verify if that's true without Adobe CDP -->. Por exemplo, as histórias podem mudar com base no comportamento do cliente, geografia, demografia, redirecionamento, posição na jornada do cliente e muito mais.

### Implementação de experiências como anúncios

Depois de criar uma experiência, você pode gerar uma tag JavaScript ou iframe para a experiência e implementar a tag como um anúncio de terceiros na Advertising DSP ou em qualquer outro DSP.<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level REtargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### Otimização dos elementos de publicidade

Opcionalmente, você pode permitir que o [!DNL Creative] otimize os elementos de anúncios para qualquer experiência com base no desempenho, independentemente de você definir metas específicas de público-alvo, usando a rotação de anúncios ponderada e otimizada, viabilizada pelo Adobe Sensei.

## Redirecionamento de pixels

Você pode criar pixels de redirecionamento para usar como targets para criações em uma experiência de anúncio. Os destinos mostram anúncios somente para usuários com atributos especificados que visitaram anteriormente páginas da Web específicas.

## Rastreamento de impressão, clique e conversão

O [!DNL Creative] rastreia automaticamente todas as impressões e cliques de anúncios veiculados por uma experiência. Opcionalmente, também é possível adicionar URLs de rastreamento de impressões e de rastreamento de cliques de terceiros a criações em bibliotecas do Creative, bem como URLs de rastreamento personalizados em uma experiência.

[!DNL Creative] também rastreia conversões de anúncios veiculados a partir de suas experiências de anúncio.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optoinal?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Relatórios de desempenho

Você pode visualizar relatórios de desempenho detalhados no nível de experiência em Criativos > Experiências.

Você também pode criar relatórios personalizados do Creative em Relatórios > Relatórios personalizados para monitorar o desempenho no nível de experiência em suas experiências. Se você usar suas experiências do [!DNL Creative] como anúncios nas campanhas do DSP, os dados de desempenho para esses anúncios estarão disponíveis em relatórios personalizados adicionais, da mesma forma que os dados para seus outros anúncios do DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

Você pode, opcionalmente, enviar seus relatórios personalizados para [destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md) especificados.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Sobre suas bibliotecas criativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Sobre experiências no Advertising Creative](/help/creative/experiences/experience-about.md)
