---
title: Rastreamento de conversão do Adobe Analytics
description: Saiba mais sobre como usar o rastreamento de conversão do Adobe Analytics para suas campanhas no Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
TQID: https://experienceleague.adobe.com/CM0S4RvR4RJ5Ylta5EJTdZh-VDDHYIfa7Qsd1Dm4D78
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# Rastreamento de conversão do Adobe Analytics

*Somente anunciantes com uma integração Adobe Advertising-Adobe Analytics*

Para anunciantes com integração Adobe Advertising-Adobe Analytics, a Advertising Cloud pode conectar seus cliques e impressões de anúncio com as métricas de conversão e engajamento do site rastreadas por [!DNL Analytics] quando você usa um redirecionamento com token (parâmetro `ef_id`) nas URLs de rastreamento de cliques para suas [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). Os dados do [!DNL Analytics] são enviados automaticamente para a Advertising Cloud por meio de um arquivo de feed diário.

Consulte &quot;[Visão Geral de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview){target="_blank"}&quot; para obter mais informações sobre a integração.

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

   Esta etapa anexa um redirecionamento ao servidor de rastreamento do Adobe Advertising (exceto para anúncios de [!DNL Google Ads] e [!DNL Microsoft Advertising] em navegadores com suporte para rastreamento paralelo) e adiciona um parâmetro &quot;ef_id&quot; preenchido dinamicamente à URL no momento do clique do anúncio. Quando o rastreamento paralelo é aplicado, os usuários finais são enviados diretamente do seu anúncio para o URL final, e o URL do modelo de rastreamento (com medição de cliques) é carregado em segundo plano.

Quando a integração for concluída, o Search, Social e Commerce receberá automaticamente todos os dados de eventos na página rastreados em [!DNL Analytics] para os conjuntos de relatórios que foram configurados.

>[!MORELIKETHIS]
>
>* [Opções de rastreamento de conversão](conversion-tracking-about.md)
