---
title: Rastreamento de conversão do Adobe Analytics
description: Saiba mais sobre como usar o rastreamento de conversão do Adobe Analytics para suas campanhas no Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: 8deabf2c98901d706acdd035221e8c24e4a1d20d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Rastreamento de conversão do Adobe Analytics

*Somente anunciantes com integração Adobe Advertising-Adobe Analytics*

Para anunciantes com integração Adobe Advertising-Adobe Analytics, o Advertising Cloud pode conectar seus cliques e impressões de anúncios com as métricas de conversão e engajamento do site rastreadas por [!DNL Analytics] quando você usa um redirecionamento com token (parâmetro `ef_id`) nas URLs de rastreamento de cliques para suas [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). Os dados do [!DNL Analytics] são enviados automaticamente para a Advertising Cloud por meio de um arquivo de feed diário.

Consulte &quot;[Visão Geral de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/dsp/integrations/analytics/overview.html){target="_blank"}&quot; para obter mais informações sobre a integração.

>[!PREREQUISITES]
>
> Os fusos horários na conta do anunciante do Search, Social e Commerce, nos conjuntos de relatórios do [!DNL Analytics] e nas contas da rede de anúncios devem coincidir. Se não corresponderem, ocorrem variações de dados entre os sistemas.

## Visão geral da implementação

1. No [!DNL Analytics], sua equipe de implementação do Search, Social e Commerce modifica as seguintes configurações para cada conjunto de relatórios:

   * A expiração de `ef_id` [!DNL eVar] foi alterada para corresponder à janela de retrospectiva de cliques do anunciante para o Adobe Advertising.

   * A ID de usuário do Adobe Advertising.

   * Eventos padrão e personalizados para usar na otimização.

1. Em Search, Social e Commerce, sua equipe de implementação:

   1. Sincroniza a hierarquia de contas de rede de anúncios existente em Pesquisa, Social e Commerce.

   1. Adiciona redirecionamentos com o token &quot;`ef_id`&quot; passando para as URLs de rastreamento e os publica na rede de anúncios.

   Esta etapa anexa um redirecionamento ao servidor de rastreamento de Adobe Advertising (exceto para anúncios [!DNL Google Ads] e [!DNL Microsoft Advertising] em navegadores que oferecem suporte ao rastreamento paralelo) e adiciona um parâmetro &quot;ef_id&quot; preenchido dinamicamente à URL no momento do clique do anúncio. Quando o rastreamento paralelo é aplicado, os usuários finais são enviados diretamente do seu anúncio para o URL final, e o URL do modelo de rastreamento (com medição de cliques) é carregado em segundo plano.

Quando a integração for concluída, o Search, Social e Commerce receberá automaticamente todos os dados de eventos na página rastreados em [!DNL Analytics] para os conjuntos de relatórios que foram configurados.

>[!MORELIKETHIS]
>
>* [Opções de rastreamento de conversão](conversion-tracking-about.md)
