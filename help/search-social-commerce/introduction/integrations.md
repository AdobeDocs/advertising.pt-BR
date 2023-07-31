---
title: Integração com soluções e serviços da Adobe Experience Cloud
description: Saiba mais sobre as integrações de pesquisa, social e comércio com as soluções e os serviços da Adobe Experience Cloud.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integração com soluções e serviços da Adobe Experience Cloud

A Advertising Search, Social e Commerce está integrada ao seguinte [!DNL Adobe] produtos.

* [Tags do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Você pode usar o [Extensão do Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) para que a Adobe Experience Platform crie tags de rastreamento de conversão Adobe Advertising, bem como tags de rastreamento de terceiros, para suas páginas de aterrissagem de anúncios. (Também é possível [crie tags de rastreamento de conversão diretamente no Search, Social e Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Entre em contato com a equipe de conta do Adobe ou com a equipe de implementação para obter informações a serem incluídas nas tags.

* Adobe Analytics — (recurso de Opt-in) Adobe Advertising e [!DNL Analytics] são integrados das seguintes formas:

   * ADOBE ADVERTISING e [!DNL Analytics] compartilhe dados perfeitamente. [!DNL Analytics] O pode enviar dados de conversão e engajamento do site diariamente para o Search, Social e Commerce, em que os dados estão disponíveis para otimização de anúncios e relatórios. Além disso, o Adobe Advertising pode enviar dados de tráfego de anúncios — incluindo impressões, cliques e custos — de suas redes de anúncios diariamente para [!DNL Analytics], em que os dados estão disponíveis em todas as ferramentas de relatório.

     Consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md)&quot; para obter mais informações sobre [!DNL Analytics] suporte para cada rede de publicidade e tipo de publicidade. Consulte também &quot;[Visão geral do [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; para obter mais informações sobre a troca de dados.

     Para trocar dados, tanto o Adobe Advertising como o [!DNL Analytics] deve ser configurado inicialmente. Entre em contato com a equipe de conta do Adobe para obter mais informações sobre a configuração inicial.

     >[!NOTE]
     >
     >Por padrão, a variável [!DNL Analytics] As métricas do não estão visíveis nas telas Pesquisa, Social e Comércio. Você deve [disponibilizar as métricas em exibições de gerenciamento de campanhas, portfólios e relatórios](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) depois que a variável [!DNL Adobe] a equipe de implementação configurou os eventos padrão ou personalizados selecionados para serem transmitidos para o Adobe Advertising. Opcionalmente, é possível alterar os nomes das métricas exibidas (sem alterá-los em [!DNL Analytics]). É possível tornar as métricas visíveis na interface do usuário e renomeá-las a partir de [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * Anunciantes com [!DNL Analytics] mas não o Audience Manager pode [criar [!DNL Google Ads] públicos-alvo de correspondência do cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) de [!DNL Analytics] segmentos que são compartilhados com a Adobe Experience Cloud. Para ser elegível, um anunciante deve implementar o [Serviço de identidade da Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) e implantar uma tag em seus sites. Você pode usar os públicos-alvo no [!DNL Google Ads] campanhas como nível de campanha ou nível de grupo de anúncios [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusões](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Segmentos do Adobe Audience Manager — (recurso de Opt-in) é possível [criar [!DNL Google Ads] públicos-alvo de correspondência do cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) em segmentos de Audience Manager que têm Pesquisa, Redes sociais e Comércio como destino. Isso pode incluir [!DNL Analytics] segmentos publicados na Adobe Experience Cloud e segmentos criados usando a Biblioteca de público-alvo da Adobe Experience Cloud. Você pode usar os públicos-alvo no [!DNL Google Ads] campanhas como nível de campanha ou nível de grupo de anúncios [targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusões](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Consulte &quot;[Integrações de Adobe Advertising com o Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; para obter mais informações.

* Adobe Target — Você pode implementar o compartilhamento de sinal de click-through entre o Search, Social, &amp; Commerce e [!DNL Target], configurar uma atividade de teste A/B no [!DNL Target] para seus anúncios e, em seguida, use [!DNL Analytics] Analysis Workspace para visualizar os dados de teste.

* Adobe Campaign — Você pode [criar e atualizar um [!DNL Google Ads] público-alvo de correspondência do cliente usando uma lista de email no [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notificações do Adobe Experience Cloud — (Quando você está conectado por meio do Adobe Experience Cloud) No link de notificações ([Notificações de alerta](/help/search-social-commerce/assets/notifications-panel.png "Notificações de alerta")na parte superior de cada página, é possível visualizar todas as atualizações de sistema, publicações, menções e ativos compartilhados da Adobe Experience Cloud. Entre em contato com a equipe de conta do Adobe para obter informações sobre como acessar o Adobe Experience Cloud.
