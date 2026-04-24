---
title: Integrações do Adobe Advertising com o Adobe Audience Manager
description: Saiba mais sobre as diferentes maneiras pelas quais o Adobe Advertising pode trocar dados com o Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2: id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 0%

---

# Integrações do Adobe Advertising com o Adobe Audience Manager

Você pode integrar o Adobe Advertising com o Audience Manager das seguintes maneiras.

## Sincronizar Audience Manager e outros segmentos do [!DNL Adobe] para direcionamento de anúncios

O [!DNL Search, Social, & Commerce] e a DSP podem obter metadados, dados de hierarquia e dados de público-alvo exclusivos para todos os públicos-alvo da Audience Manager de um anunciante ou agência e de outros [!DNL Adobe]. Essa conexão exclusiva está disponível somente para profissionais de marketing que usam o Adobe Advertising. Consulte &quot;[Importar segmentos do Adobe Audience Manager para direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Use o Audience Manager e outros segmentos do [!DNL Adobe] para criar [!DNL Google Ads] públicos-alvo {#audience-manager-google-audiences}

*Anunciantes aceitos com [!DNL Advertising Search, Social, & Commerce] somente*

No [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] públicos-alvo de correspondência do cliente a partir de IDs de usuário usando seus segmentos existentes do Audience Manager que têm [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] é um nome antigo para [!DNL Search, Social, & Commerce].) Isso inclui segmentos do Adobe Analytics publicados no Adobe CX Enterprise e segmentos criados com o Adobe CX Enterprise [!DNL Audience Library]. Para obter mais informações, consulte &quot;[Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Os públicos-alvo de correspondência do cliente das IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo baseados em marcas de site, mas uma ID que não seja uma PII é atribuída a membros de público-alvo exclusivos para benefícios distintos em relação aos públicos-alvo padrão baseados em marcas de site e correspondência do cliente.

Para criar as IDs de usuário necessárias, você deve usar uma tag do Adobe Advertising JavaScript <!-- with a user ID parameter -->nos sites. Entre em contato com a equipe de conta da Adobe para obter mais informações.

![processo de criação de segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos, você pode usá-los em [!DNL Google Ads] campanhas como [exclusões ou destinos de nível de campanha ou de grupo de anúncios](#audience-manager-targets).

### Usar o Audience Manager e outros segmentos do [!DNL Adobe] para direcionar ou excluir anúncios {#audience-manager-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) Você pode usar qualquer [!DNL Google Ads] público-alvo que tenha sido [criado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como metas ou exclusões no nível da campanha ou do grupo de anúncios em suas [!DNL Google Ads] campanhas.

* (Anunciantes com o DSP) Você pode usar seus segmentos existentes do [!DNL Adobe] como destinos de seus posicionamentos de anúncios. You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Adobe] segments as targets for specific creatives in your ad experiences.

>[!NOTE]
>
>For more information about how to create audiences in the Audience Manager and Adobe CX Enterprise [!DNL Audience Library] interfaces, and common use cases for different audience types, see &quot;[Audience creation options](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Send DSP media exposure data to Audience Manager

*Advertisers with DSP only*

DSP customers with Adobe Audience Manager can capture data from ad campaigns using pixel calls to Audience Manager. You can then use the campaign data to build rule-based traits, which you can use to define new segments to enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

See &quot;[Overview of sending DSP media exposure data to Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; for more information.

## Get richer insights into site activity with Audience Analytics

Adobe Advertising customers with [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) can send both Adobe Advertising-tracked data and Audience Manager segments to [!DNL Analytics] for enriched insights about site activity.

For more information, see &quot;[[!DNL Adobe Audience Analytics] for Adobe Advertising customers](/help/integrations/audience-manager/audience-analytics.md).&quot;
