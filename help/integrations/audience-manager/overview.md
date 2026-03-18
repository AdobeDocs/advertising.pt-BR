---
title: Integrações do Adobe Advertising com o Adobe Audience Manager
description: Saiba mais sobre as diferentes maneiras pelas quais o Adobe Advertising pode trocar dados com o Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Integrações do Adobe Advertising com o Adobe Audience Manager

Você pode integrar o Adobe Advertising com o Audience Manager das seguintes maneiras.

## Sincronizar Audience Manager e outros segmentos do [!DNL Adobe] para direcionamento de anúncios

O [!DNL Search, Social, & Commerce] e a DSP podem obter metadados, dados de hierarquia e dados de público-alvo exclusivos para todos os públicos-alvo da Audience Manager de um anunciante ou agência e de outros [!DNL Adobe]. Essa conexão exclusiva está disponível somente para profissionais de marketing que usam o Adobe Advertising. Consulte &quot;[Importar segmentos do Adobe Audience Manager para direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Use o Audience Manager e outros segmentos do [!DNL Adobe] para criar [!DNL Google Ads] públicos-alvo {#audience-manager-google-audiences}

*Anunciantes aceitos com [!DNL Advertising Search, Social, & Commerce] somente*

No [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] públicos-alvo de correspondência do cliente a partir de IDs de usuário usando seus segmentos existentes do Audience Manager que têm [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] é um nome antigo de [!DNL Search, Social, & Commerce].) Isso inclui segmentos do Adobe Analytics publicados no Adobe Experience Cloud e segmentos criados com o Adobe Experience Cloud [!DNL Audience Library]. Para obter mais informações, consulte &quot;[Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Os públicos-alvo de correspondência do cliente das IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo baseados em marcas de site, mas uma ID que não seja uma PII é atribuída a membros de público-alvo exclusivos para benefícios distintos em relação aos públicos-alvo padrão baseados em marcas de site e correspondência do cliente.

Para criar as IDs de usuário necessárias, você deve usar uma tag do Adobe Advertising JavaScript <!-- with a user ID parameter -->nos sites. Entre em contato com a equipe de conta da Adobe para obter mais informações.

![processo de criação de segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos, você pode usá-los em [!DNL Google Ads] campanhas como [exclusões ou destinos de nível de campanha ou de grupo de anúncios](#audience-manager-targets).

### Usar o Audience Manager e outros segmentos do [!DNL Adobe] para direcionar ou excluir anúncios {#audience-manager-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) Você pode usar qualquer [!DNL Google Ads] público-alvo que tenha sido [criado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como metas ou exclusões no nível da campanha ou do grupo de anúncios em suas [!DNL Google Ads] campanhas.

* (Anunciantes com o DSP) Você pode usar seus segmentos existentes do [!DNL Adobe] como destinos de seus posicionamentos de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que você pode usar como destinos ou exclusões para vários posicionamentos.

* (Anunciantes com o Advertising Creative) Você pode usar seus segmentos existentes do [!DNL Adobe] como destinos de criações específicas em suas experiências de anúncio.

>[!NOTE]
>
>Para obter mais informações sobre como criar públicos-alvo nas interfaces do [!DNL Audience Library] do Audience Manager e do Experience Cloud, e casos de uso comuns para diferentes tipos de público-alvo, consulte &quot;[Opções de criação de público-alvo](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Enviar dados de exposição da mídia do DSP para o Audience Manager

*Somente anunciantes com o DSP*

Os clientes do DSP com o Adobe Audience Manager podem capturar dados de campanhas de anúncios usando chamadas de pixel para o Audience Manager. Em seguida, você pode usar os dados da campanha para criar características com base em regras, que podem ser usadas para definir novos segmentos para habilitar vários casos de uso do DSP, como segmentação mais avançada, gerenciamento de frequência, análise de marketing e insights de relatórios.

Consulte &quot;[Visão geral do envio de dados de exposição de mídia do DSP para o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

## Obtenha insights mais avançados sobre a atividade do site com o Audience Analytics

Os clientes do Adobe Advertising com [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) podem enviar dados rastreados pela Adobe Advertising e segmentos do Audience Manager para o [!DNL Analytics] para obter insights enriquecidos sobre a atividade do site.

Para obter mais informações, consulte &quot;[[!DNL Adobe Audience Analytics] para clientes do Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md)&quot;.
