---
title: Visão geral do envio de dados de exposição de mídia do DSP para o Adobe Audience Manager
description: Saiba como usar pixels de evento do Audience Manager para capturar dados em nível de impressão e de clique de campanhas do Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Visão geral do envio de dados de exposição de mídia do DSP para o Adobe Audience Manager

*Somente anunciantes com o Advertising DSP*

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Audience Manager*

Os clientes do Advertising DSP com o Adobe Audience Manager podem usar os pixels de evento do Audience Manager para capturar dados de nível de impressão e dados de nível de clique de campanhas do DSP. Os pixels do evento enviam os dados como sinais acionáveis para a Audience Manager. Esses sinais permitem vários casos de uso do DSP, como segmentação mais avançada, gerenciamento de frequência, análises de marketing e insights de relatórios.

A DSP não cobra para enviar esses sinais para a Audience Manager. No entanto, você paga custos de assimilação padrão do Audience Manager com base em chamadas de servidor, de acordo com o contrato do Audience Manager. O Audience Manager remove eventos duplicados que são rastreados de duas maneiras diferentes, para que cada evento seja cobrado apenas uma vez.

>[!NOTE]
>
> O Audience Manager também oferece suporte à captura de dados de arquivos de log do servidor de anúncios, o que fornece menos flexibilidade. Esse processo não é abordado nesta documentação.

## Benefícios principais

* Os dados de campanha do DSP fluem para o Audience Manager em tempo real e você pode usá-los para criar características baseadas em regras que você usa para definir segmentos.

* Os segmentos estão disponíveis para direcionamento imediatamente após a característica do usuário e a qualificação de segmento, reforçando os esforços de direcionamento em tempo real.

* Você pode aproveitar os dados da campanha para casos de uso, como limite de frequência em criações, redirecionamento de usuários que foram expostos a campanhas anteriores e análise do comportamento downstream do site e dos pontos de entrada.

* Os dados agregados fornecem uma exibição unificada do desempenho da campanha, ajudam a identificar caminhos de conversão personalizados e podem ser usados para melhorar a sequência de eventos que levam a conversões por meio do Audience Manager [!DNL Audience Optimization Reports] ou por meio de uma [[!DNL Audience Analytics] integração com o Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Como os dados são rastreados

Os pixels do evento de impressão e clique do Audience Manager são baseados em cookies. Os pixels não capturam eventos que ocorrem em ambientes sem cookies, como aplicativos móveis e CTV (TV conectada).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Pixels de rastreamento de impressão

O Audience Manager rastreia dados de impressão de um anúncio quando você anexa um pixel de rastreamento de evento transparente de 1xl ao anúncio. O pixel do evento é carregado sempre que o anúncio é exibido a um usuário e carregado pelo navegador da Web. O pixel é carregado de um subdomínio específico do cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=pt-BR), que é um domínio herdado do Audience Manager e contém parâmetros como pares de valores chave. A chamada de evento coleta dados de impressão e conversão e os envia para os servidores de coleta de dados da Audience Manager.

### Rastreamento de cliques em pixels

O Audience Manager rastreia cliques de forma semelhante às impressões, exceto que não carrega o pixel do evento transparente sempre que o anúncio é veiculado. Em vez disso, os dados de cliques são rastreados no URL de click-through do anúncio. O anúncio aponta para um subdomínio específico do cliente do [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=pt-BR), que é um domínio herdado do Audience Manager, para processamento pelos servidores de coleta de dados da Audience Manager. O servidor então redireciona o usuário para a página inicial desejada. O URL contém parâmetros como pares de valor chave.

>[!NOTE]
>
>Se sua organização usar o rastreamento de [!DNL Analytics], talvez você não precise do rastreamento de cliques do Audience Manager. O Adobe Analytics captura sinais de cliques e pode enviá-los para o Audience Manager por meio do [encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=pt-BR).

>[!MORELIKETHIS]
>
>* [Coletar dados de clique e impressão de campanhas do Advertising DSP](collect.md)
>* [Casos de uso](use-cases.md)
