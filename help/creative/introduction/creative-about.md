---
title: Sobre o Adobe Advertising Creative
description: Saiba mais sobre  [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
TQID: https://experienceleague.adobe.com/UfaLj12BFBAxCDvtb6cUtVxlcuOSYgnZPTAn7494APk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 493
ht-degree: 0%

---

# Sobre o Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Como parte do Adobe Advertising, o Advertising Creative é uma plataforma de autoatendimento para automatizar experiências de anúncios personalizados em tempo real e, opcionalmente, otimizar seus anúncios no nível do elemento criativo.<!-- Verify --> Você pode implementar as experiências de anúncio como anúncios em qualquer DSP, incluindo o Adobe Advertising DSP.

## Bibliotecas criativas personalizadas de criativos reutilizáveis

Suas bibliotecas Creative permitem gerenciar os elementos de criação que você usará em suas experiências de anúncio. Você pode criar várias bibliotecas, cada uma com criações e grupos criativos individuais (chamados de *pacotes*, que você anexará às experiências).

### [!DNL Adobe] integrações de ativos

O [!DNL Creative] está diretamente integrado aos seguintes produtos do [!DNL Adobe], permitindo que você importe ativos para suas bibliotecas criativas:

* **Adobe Experience Manager:** carregue os [!DNL Adobe] ativos de imagem que sua equipe de design cria e aprova para anúncios de imagem padrão.

* **Adobe GenStudio for Performance Marketing:** importe todas as variantes de anúncios das suas experiências de anúncio de exibição como criações do HTML5.

## Experiências baseadas em regras e não direcionadas

* **Experiências direcionadas e baseadas em regras:** Crie histórias usando um modelo de árvore decisória baseado em regras — desdobrando uma cadeia coreografada de anúncios que são personalizados em tempo real com base no que você sabe sobre o seu público-alvo. Por exemplo, as histórias podem mudar com base no comportamento do cliente, geografia, demografia, redirecionamento, posição na jornada do cliente e muito mais.

* **Experiências não direcionadas:** agende e otimize os elementos de anúncio sem restringir o público.

### [!DNL Adobe] integrações de dados

Use os segmentos de público-alvo primários da Adobe Audience Manager e da Adobe Analytics, bem como os segmentos de público-alvo personalizados criados no Advertising DSP e os pixels de redirecionamento criados com o [!DNL Creative], como alvos para criações específicas em uma experiência de anúncio. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementação de experiências como anúncios

Depois de criar uma experiência, você pode gerar uma tag JavaScript ou iframe para a experiência e implementar a tag como um anúncio de terceiros em uma campanha do Advertising DSP ou em qualquer outra DSP.

### Otimização dos elementos de publicidade

Opcionalmente, você pode permitir que o [!DNL Creative] otimize os elementos de anúncios para qualquer experiência com base no desempenho, independentemente de você definir metas específicas de público-alvo, usando a rotação de anúncios ponderada e otimizada, viabilizada pelo [!DNL Adobe AI].

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Redirecionamento de pixels

Você pode criar pixels de redirecionamento para usar como targets para criações em uma experiência de anúncio. Os destinos mostram anúncios somente para usuários com atributos especificados que visitaram anteriormente páginas da Web específicas.

## Rastreamento de impressão, clique e conversão

O [!DNL Creative] rastreia automaticamente todas as impressões e cliques de anúncios veiculados por uma experiência. Opcionalmente, também é possível adicionar URLs de rastreamento de impressões e de rastreamento de cliques de terceiros a criações em bibliotecas do Creative, bem como URLs de rastreamento personalizados em uma experiência.

[!DNL Creative] também rastreia conversões de anúncios veiculados a partir de suas experiências de anúncio.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Relatórios de desempenho

Você pode visualizar relatórios de desempenho detalhados no nível de experiência em Criativos > Experiências.

Você também pode criar relatórios personalizados do Creative em Relatórios > Relatórios personalizados para monitorar o desempenho no nível de experiência em suas experiências. Se você usar suas experiências do [!DNL Creative] como anúncios nas campanhas do DSP, os dados de desempenho para esses anúncios estarão disponíveis em relatórios personalizados adicionais, da mesma forma que os dados para seus outros anúncios do DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Você pode, opcionalmente, enviar seus relatórios personalizados para [destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md) especificados.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Sobre suas bibliotecas criativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Sobre experiências no Advertising Creative](/help/creative/experiences/experience-about.md)
