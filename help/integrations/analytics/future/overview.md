---
title: Integrações de publicidade do Adobe com o Adobe Analytics
description: Saiba mais sobre como a Adobe Advertising pode trocar dados com o Adobe Analytics e como você pode usar os dados em Pesquisar, Social e Comércio.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Integrações de publicidade do Adobe com o Adobe Analytics

É possível integrar a publicidade do Adobe com o Analytics das seguintes maneiras.

## Trocar dados entre [!DNL Analytics] e publicidade Adobe

### Puxar [!DNL Analytics] Dados na publicidade Adobe

Com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP:

* **[!DNL Analytics]segmentos:**  Metadados, dados de hierarquia e dados de público-alvo exclusivos para todos os segmentos de anunciantes ou agências criados no [!DNL Analytics] e publicados no Experience Cloud.

* **[!DNL Analytics]métricas de envolvimento do site**

* **[!DNL Analytics]métricas padrão, personalizadas e reservadas**

### Enviar dados de publicidade do Adobe para [!DNL Analytics]

* **Métricas de tráfego da publicidade Adobe**

* **Dimension da publicidade Adobe**

>[!NOTE]
>
>Para [!DNL Search, Social, & Commerce], esse recurso é compatível com a maioria das redes de anúncios e tipos de campanha. Consulte &quot;Inventário suportado&quot; na seção [!DNL Search, Social, & Commerce] Guia para obter mais informações.<!-- add link when that's published in ExL -->

### Use [!DNL Analytics] Segmentos a serem criados [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes aceitos com [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] Os públicos-alvo da correspondência do cliente do Google com as IDs de usuário existentes [!DNL Analytics] segmentos. Isso inclui segmentos do Adobe Analytics publicados na Adobe Experience Cloud e segmentos que são criados usando a Adobe Experience Cloud [!DNL Audience Library]. Para obter mais informações, consulte a ajuda do produto em [!DNL Search, Social, & Commerce].

[Correspondência de clientes de IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo baseados em tags de site, mas uma ID que não seja de PII é atribuída a membros exclusivos do público-alvo para benefícios distintos em relação à correspondência de clientes padrão e públicos baseados em tags de site.

Para criar as IDs de usuário necessárias, você deve usar uma tag JavaScript Adobe Advertising <!-- with a user ID parameter -->em seus sites. Entre em contato com a equipe de conta do Adobe para obter mais informações.

![processo de criação de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos-alvo, você pode usá-los em [!DNL Google Ads] campanhas como [metas ou exclusões a nível de campanha ou de grupo de anúncios](#audience-manager-targets).

### Use [!DNL Analytics] Segmentos para segmentar ou excluir anúncios {#analytics-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) Você pode usar qualquer [!DNL Google Ads] públicos-alvo que foram [criado usando [!DNL Analytics] segmentos](#audience-manager-google-audiences) como metas ou exclusões a nível de campanha ou de grupo de anúncios em seu [!DNL Google Ads] campanhas.

* (Anunciantes com DSP) Você pode usar seu [!DNL Analytics] segmentos como alvos de disposições de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que podem ser usados como alvos ou exclusões para várias disposições.

* (Anunciantes com Advertising Creative) Você pode usar seus [!DNL Analytics] segmentos como alvos para criações específicas em suas experiências de publicidade.
