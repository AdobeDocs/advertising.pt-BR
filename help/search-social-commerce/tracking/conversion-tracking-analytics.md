---
title: Rastreamento de conversão do Adobe Analytics
description: Saiba mais sobre como usar o rastreamento de conversão do Adobe Analytics para suas campanhas no Adobe Advertising.
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Rastreamento de conversão do Adobe Analytics

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Para anunciantes com uma integração Adobe Advertising-Adobe Analytics, o Advertising Cloud pode conectar seus cliques em anúncios e impressões com as métricas de conversão e engajamento do site rastreadas pelo [!DNL Analytics] quando você usa um redirecionamento com um token (`ef_id` parâmetro) nos URLs de rastreamento de cliques do [unidades de oferta](/help/search-social-commerce/glossary.md#a-b). A variável [!DNL Analytics] Os dados do são enviados automaticamente para a Advertising Cloud por meio de um arquivo de feed diário.

Consulte &quot;[Visão geral do [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; para obter mais informações sobre a integração.

>[!PREREQUISITES]
>
> Fusos horários na conta do anunciante do Search, Social, &amp; Commerce, o [!DNL Analytics] conjuntos de relatórios e as contas da rede de publicidade devem corresponder. Se não corresponderem, haverá variações de dados entre os sistemas.

## Visão geral da implementação

1. Entrada [!DNL Analytics], sua equipe de implementação do Search, Social e Commerce modifica as seguintes configurações para cada conjunto de relatórios:

   * A expiração da variável `ef_id` [!DNL eVar] foi alterado para corresponder à janela de retrospectiva de cliques do anunciante para Adobe Advertising.

   * A ID de usuário do Adobe Advertising.

   * Eventos padrão e personalizados para usar na otimização.

1. Em Pesquisa, Social e Comércio, sua equipe de implementação:

   1. Sincroniza a hierarquia de contas de rede de anúncios existente em Pesquisa, Social e Comércio.

   1. Adiciona redirecionamentos com &quot;`ef_id`&quot;token de envio para os URLs de rastreamento do e os publica na rede de anúncios.

   Esta etapa anexa um redirecionamento ao servidor de rastreamento do Adobe Advertising (exceto para [!DNL Google Ads] e [!DNL Microsoft Advertising] anúncios em navegadores compatíveis com rastreamento paralelo) e adiciona um parâmetro &quot;ef_id&quot; preenchido dinamicamente ao URL no momento do clique no anúncio. Quando o rastreamento paralelo é aplicado, os usuários finais são enviados diretamente do seu anúncio para o URL final, e o URL do modelo de rastreamento (com medição de cliques) é carregado em segundo plano.

Quando a integração for concluída, o Search, Social e Commerce receberá automaticamente todos os dados de eventos na página rastreados no [!DNL Analytics] para os conjuntos de relatórios que foram configurados.

>[!MORELIKETHIS]
>
>* [Opções de rastreamento de conversão](conversion-tracking-about.md)
