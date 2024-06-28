---
title: Visão geral do envio de dados de exposição da mídia DSP para o Adobe Audience Manager
description: Saiba como usar pixels de evento Audience Manager para capturar dados de nível de impressão e nível de clique de campanhas do Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Visão geral do envio de dados de exposição da mídia DSP para o Adobe Audience Manager

*Anunciantes somente com o Advertising DSP*

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Audience Manager*

Os clientes do Advertising DSP com Adobe Audience Manager podem usar pixels de evento Audience Manager para capturar dados de nível de impressão e dados de nível de clique de campanhas do DSP. Os pixels do evento enviam os dados como sinais acionáveis para o Audience Manager. Esses sinais permitem vários casos de uso do DSP, como segmentação mais avançada, gerenciamento de frequência, análise de marketing e insights de relatórios.

A DSP não cobra para enviar esses sinais para o Audience Manager. No entanto, você paga custos de assimilação de Audience Manager padrão com base em chamadas de servidor, de acordo com o contrato de Audience Manager. O Audience Manager remove eventos duplicados que são rastreados de duas maneiras diferentes, para que cada evento seja cobrado apenas uma vez.

>[!NOTE]
>
> O Audience Manager também é compatível com a captura de dados de arquivos de log do servidor de anúncios, o que fornece menos flexibilidade. Esse processo não é abordado nesta documentação.

## Principais benefícios

* Os dados de campanha do DSP fluem para o Audience Manager em tempo real, e você pode usá-los para criar características baseadas em regras que você usa para definir segmentos.

* Os segmentos estão disponíveis para direcionamento imediatamente após a característica do usuário e a qualificação de segmento, reforçando os esforços de direcionamento em tempo real.

* Você pode aproveitar os dados da campanha para casos de uso, como limite de frequência em criações, redirecionamento de usuários que foram expostos a campanhas anteriores e análise do comportamento downstream do site e dos pontos de entrada.

* Os dados agregados fornecem uma visualização unificada do desempenho da campanha, ajuda a identificar caminhos de conversão personalizados e podem ser usados para melhorar a sequência de eventos que levam a conversões por meio do Audience Manager [!DNL Audience Optimization Reports] ou por meio de um [[!DNL Audience Analytics] integração com o Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Como os dados são rastreados

Os pixels do evento de impressão de Audience Manager e clique são baseados em cookies. Os pixels não capturam eventos que ocorrem em ambientes sem cookies, como aplicativos móveis e TV conectada (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Pixels de rastreamento de impressão

o Audience Manager rastreia dados de impressão de um anúncio quando você anexa um pixel transparente de rastreamento de eventos de 1xl ao anúncio. O pixel do evento é carregado sempre que o anúncio é exibido a um usuário e carregado pelo navegador da Web. O pixel é carregado de um subdomínio específico do cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que é um domínio herdado do Audience Manager e contém parâmetros como pares de valores chave. A chamada de evento coleta dados de impressão e conversão e os envia para os servidores de coleta de dados do Audience Manager.

### Pixels de rastreamento de cliques

O Audience Manager rastreia cliques de forma semelhante às impressões, exceto que não carrega o pixel de evento transparente sempre que o anúncio é veiculado. Em vez disso, os dados de cliques são rastreados no URL de click-through do anúncio. O anúncio aponta para um subdomínio específico do cliente do [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que é um domínio herdado do Audience Manager, para processamento pelos servidores de coleta de dados do Audience Manager. O servidor então redireciona o usuário para a página inicial desejada. O URL contém parâmetros como pares de valor chave.

>[!NOTE]
>
>Se sua organização usar [!DNL Analytics] , talvez você não precise do rastreamento de cliques do Audience Manager. O Adobe Analytics captura sinais de cliques e pode enviá-los para o Audience Manager por meio de [encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Coletar dados de cliques e impressões de campanhas do Advertising DSP](collect.md)
>* [Casos de uso](use-cases.md)
