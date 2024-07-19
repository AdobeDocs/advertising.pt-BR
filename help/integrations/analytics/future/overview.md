---
title: Integrações de Adobe Advertising com o Adobe Analytics
description: Saiba mais sobre como o Adobe Advertising pode trocar dados com o Adobe Analytics e como você pode usar os dados no Search, Social e Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integrações de Adobe Advertising com o Adobe Analytics

É possível integrar o Adobe Advertising com o Analytics das seguintes maneiras.

## Trocar Dados entre [!DNL Analytics] e Adobe Advertising

### Transferir dados do [!DNL Analytics] para o Adobe Advertising

Com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP:

* **[!DNL Analytics]segmentos:** Metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os segmentos de um anunciante ou de uma agência criados em [!DNL Analytics] e publicados no Experience Cloud.

* **[!DNL Analytics]métricas de envolvimento do site**

* **[!DNL Analytics]métricas padrão, personalizadas e reservadas**

### Enviar dados de Adobe Advertising para [!DNL Analytics]

* **Métricas de tráfego do Adobe Advertising**

* **Dimension do Adobe Advertising**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce], esse recurso tem suporte para a maioria das redes de anúncios e tipos de campanha. Consulte &quot;Inventário com Suporte&quot; no Guia do [!DNL Search, Social, & Commerce] para obter mais informações.<!-- add link when that's published in ExL -->

### Usar [!DNL Analytics] segmentos para criar [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes aceitos com [!DNL Advertising Search, Social, & Commerce] somente*

<!-- Verify all -->

No [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] públicos-alvo de correspondência do cliente do Google a partir de IDs de usuário usando seus [!DNL Analytics] segmentos existentes. Isso inclui segmentos do Adobe Analytics publicados no Adobe Experience Cloud e segmentos criados com o Adobe Experience Cloud [!DNL Audience Library]. Para obter mais informações, consulte &quot;[Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Os públicos-alvo de correspondência do cliente das IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo baseados em marcas de site, mas uma ID que não seja uma PII é atribuída a membros de público-alvo exclusivos para benefícios distintos em relação aos públicos-alvo padrão baseados em marcas de site e correspondência do cliente.

Para criar as IDs de usuário necessárias, você deve usar uma tag Adobe Advertising JavaScript <!-- with a user ID parameter -->nos sites. Entre em contato com a equipe de conta do Adobe para obter mais informações.

![processo de criação de segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos, você pode usá-los em [!DNL Google Ads] campanhas como [exclusões ou destinos de nível de campanha ou de grupo de anúncios](#audience-manager-targets).

### Usar [!DNL Analytics] segmentos para direcionar ou excluir anúncios {#analytics-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) Você pode usar qualquer [!DNL Google Ads] público-alvo que tenha sido [criado usando [!DNL Analytics] segmentos](#audience-manager-google-audiences) como metas ou exclusões no nível da campanha ou do grupo de anúncios em suas [!DNL Google Ads] campanhas.

* (Anunciantes com DSP) Você pode usar seus segmentos existentes do [!DNL Analytics] como destinos de seus posicionamentos de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que você pode usar como destinos ou exclusões para vários posicionamentos.

* (Anunciantes com Advertising Creative) Você pode usar seus segmentos existentes do [!DNL Analytics] como destinos de criações específicas em suas experiências de anúncio.
