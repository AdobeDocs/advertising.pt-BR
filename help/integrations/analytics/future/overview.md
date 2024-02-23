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

## Trocar Dados Entre [!DNL Analytics] e ADOBE ADVERTISING

### Puxar [!DNL Analytics] Dados no Adobe Advertising

Com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e o DSP puxa:

* **[!DNL Analytics]segmentos:**  Metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os segmentos de um anunciante ou agência criados no [!DNL Analytics] e publicado no Experience Cloud.

* **[!DNL Analytics]métricas de engajamento no site**

* **[!DNL Analytics]métricas padrão, personalizadas e reservadas**

### Enviar dados de Adobe Advertising para [!DNL Analytics]

* **Métricas de tráfego do Adobe Advertising**

* **Dimension do Adobe Advertising**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce], esse recurso é compatível com a maioria das redes de anúncios e tipos de campanha. Consulte &quot;Inventário suportado&quot; no [!DNL Search, Social, & Commerce] Guia para obter mais informações.<!-- add link when that's published in ExL -->

### Uso [!DNL Analytics] Segmentos a serem criados [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes aceitos com o [!DNL Advertising Search, Social, & Commerce] somente*

<!-- Verify all -->

Dentro de [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] Públicos-alvo de correspondência de clientes do Google provenientes de IDs de usuários que usam sua [!DNL Analytics] segmentos. Isso inclui segmentos do Adobe Analytics publicados no Adobe Experience Cloud e segmentos criados usando a Adobe Experience Cloud [!DNL Audience Library]. Para obter mais informações, consulte &quot;[Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Públicos-alvo de correspondência do cliente de IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo com base em tags do site, mas uma ID que não seja uma PII é atribuída a membros únicos do público-alvo para obter benefícios distintos em relação à correspondência padrão do cliente e aos públicos-alvo com base em tags do site.

Para criar as IDs de usuário necessárias, você deve usar uma tag JavaScript do Adobe Advertising <!-- with a user ID parameter -->em seus sites. Entre em contato com a equipe de conta do Adobe para obter mais informações.

![processo de criação de segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos-alvo, você pode usá-los no [!DNL Google Ads] campanhas como [metas ou exclusões no nível da campanha ou do grupo de anúncios](#audience-manager-targets).

### Uso [!DNL Analytics] Segmentos para direcionar ou excluir anúncios {#analytics-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) É possível usar qualquer [!DNL Google Ads] públicos-alvo que foram [criado usando [!DNL Analytics] segmentos](#audience-manager-google-audiences) como exclusões ou alvos no nível da campanha ou do grupo de anúncios no [!DNL Google Ads] campanhas.

* (Anunciantes com DSP) Você pode usar seu anúncio existente [!DNL Analytics] segmentos como destinos para seus posicionamentos de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que você pode usar como destinos ou exclusões para vários posicionamentos.

* (Anunciantes com Advertising Creative) Você pode usar seu anúncio existente [!DNL Analytics] segmentos como alvos para criações específicas em suas experiências de anúncio.
