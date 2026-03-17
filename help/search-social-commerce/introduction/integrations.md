---
title: Integração com soluções e serviços da Adobe Experience Cloud
description: Saiba mais sobre as integrações de Pesquisa, Social e Commerce com as soluções e os serviços da Adobe Experience Cloud.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Integração com soluções e serviços da Adobe Experience Cloud

O Advertising Search, Social e Commerce está integrado aos seguintes produtos do [!DNL Adobe].

* [Marcas da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Você pode usar a [Extensão do Adobe Advertising Cloud](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) para o Adobe Experience Platform para [criar marcas de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md), bem como marcas de rastreamento de terceiros, para suas páginas de aterrissagem de anúncios. Se sua organização não tiver uma conta do Experience Platform, ainda será possível instalar a extensão diretamente na [interface do usuário da Coleção de dados da Adobe Experience Platform](https://experience.adobe.com/#/data-collection/), que está disponível gratuitamente para os clientes da Adobe Experience Cloud.

  Para instalar a extensão necessária, contate o administrador da organização para obter acesso aos recursos de Coleção de Dados na interface do usuário e solicite a concessão da permissão `manage_properties`.

  **Observação:** você também pode [criar marcas de rastreamento de conversão diretamente no Search, Social e Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (recurso de Opt-in) Adobe Advertising e [!DNL Analytics] estão integrados das seguintes maneiras:

   * O Adobe Advertising e o [!DNL Analytics] compartilham dados facilmente. O [!DNL Analytics] pode enviar dados de conversão e participação do site diariamente para o Search, Social e Commerce, em que os dados estão disponíveis para otimização de anúncios e relatórios. Além disso, o Adobe Advertising pode enviar dados de tráfego de anúncios — incluindo impressões, cliques e custos — de suas redes de anúncios diariamente para o [!DNL Analytics], em que os dados estão disponíveis em todas as ferramentas de relatório.

     Consulte &quot;[Inventário suportado](/help/search-social-commerce/introduction/supported-inventory.md)&quot; para obter mais informações sobre o suporte de [!DNL Analytics] para cada rede de publicidade e tipo de publicidade. Consulte também &quot;[Visão geral de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; para obter mais informações sobre a troca de dados.

     Para trocar dados, o Adobe Advertising e o [!DNL Analytics] devem estar configurados inicialmente. Entre em contato com a equipe de conta da Adobe para obter mais informações sobre a configuração inicial.

     >[!NOTE]
     >
     >Por padrão, as métricas [!DNL Analytics] não estão visíveis nas telas Search, Social e Commerce. Você deve [disponibilizar explicitamente as métricas em modos de exibição de gerenciamento de campanhas, portfólios e relatórios](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) depois que a equipe de implementação do [!DNL Adobe] configurar eventos padrão ou personalizados selecionados para serem transmitidos para o Adobe Advertising. Opcionalmente, é possível alterar os nomes de métrica exibidos (sem alterá-los em [!DNL Analytics]). Você pode tornar as métricas visíveis na interface e renomeá-las de [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Anunciantes com [!DNL Analytics], mas não com o Audience Manager, podem [criar [!DNL Google Ads] públicos-alvo de correspondência do cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) de [!DNL Analytics] segmentos que são compartilhados com o Adobe Experience Cloud. Para ser qualificado, um anunciante deve implementar o [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) e implantar uma tag em seus sites. Você pode então usar os públicos em [!DNL Google Ads] campanhas como [alvos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusões](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) de nível de campanha ou de grupo de anúncios.

* Segmentos do Adobe Audience Manager — (recurso de aceitação) Você pode [criar [!DNL Google Ads] públicos-alvo de correspondência do cliente](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) de segmentos do Audience Manager que têm o Search, o Social e o Commerce como destino. Isso pode incluir [!DNL Analytics] segmentos publicados na Adobe Experience Cloud e segmentos criados usando a Biblioteca de público-alvo da Adobe Experience Cloud. Você pode então usar os públicos em [!DNL Google Ads] campanhas como [alvos](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusões](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) de nível de campanha ou de grupo de anúncios.

  Consulte &quot;[Integrações do Adobe Advertising com o Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; para obter mais informações.

* Adobe Target — Você pode implementar o compartilhamento de sinal de click-through entre o Search, Social, &amp; Commerce e [!DNL Target], configurar uma atividade de teste A/B no [!DNL Target] para seus anúncios e usar o Analysis Workspace [!DNL Analytics] para exibir os dados de teste.

* Adobe Campaign — Você pode [criar e atualizar um público-alvo de correspondência do cliente [!DNL Google Ads] usando uma lista de email [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notificações do Adobe Experience Cloud — (Quando você está conectado por meio do Adobe Experience Cloud) No link de notificações ([Notificações de Alerta](/help/search-social-commerce/assets/notifications-panel.png "Notificações de alerta")), na parte superior de cada página, é possível exibir todas as atualizações de sistema, publicações, menções e ativos compartilhados do Adobe Experience Cloud. Entre em contato com a equipe de conta da Adobe para obter mais informações sobre como acessar o Adobe Experience Cloud.
