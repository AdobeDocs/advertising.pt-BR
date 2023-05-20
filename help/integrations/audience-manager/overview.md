---
title: Integrações de publicidade do Adobe com o Adobe Audience Manager
description: Saiba mais sobre as diferentes maneiras pelas quais a Adobe Advertising pode trocar dados com a Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Integrações de publicidade do Adobe com o Adobe Audience Manager

Você pode integrar o anúncio de Adobe com o Audience Manager das seguintes maneiras.

## Sincronizar Audience Manager e outros [!DNL Adobe] Segmentos para direcionamento de anúncios

[!DNL Search, Social, & Commerce] e o DSP podem obter metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os Audience Manager e outros [!DNL Adobe] públicos-alvo. Essa conexão exclusiva está disponível somente para profissionais de marketing que usam o Adobe Advertising. Consulte &quot;[Importar segmentos do Adobe Audience Manager para direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usar Audience Manager e outros [!DNL Adobe] Segmentos a serem criados [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes aceitos com o [!DNL Advertising Search, Social, & Commerce] somente*

Dentro de [!DNL Search, Social, & Commerce], você pode criar [!DNL Google Ads] Públicos-alvo de correspondência de clientes do Google provenientes de IDs de usuários utilizando seus segmentos de Audience Manager existentes que [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] é um nome antigo de [!DNL Search, Social, & Commerce].) Isso inclui segmentos do Adobe Analytics publicados no Adobe Experience Cloud e segmentos criados usando a Adobe Experience Cloud [!DNL Audience Library]. Para obter mais informações, consulte a ajuda no produto em [!DNL Search, Social, & Commerce].

[Públicos-alvo de correspondência do cliente de IDs de usuário](https://support.google.com/google-ads/answer/9199250) funcionam como públicos-alvo com base em tags do site, mas uma ID que não seja uma PII é atribuída a membros únicos do público-alvo para obter benefícios distintos em relação à correspondência padrão do cliente e aos públicos-alvo com base em tags do site.

Para criar as IDs de usuário necessárias, você deve usar uma tag JavaScript do Adobe Advertising <!-- with a user ID parameter -->em seus sites. Entre em contato com a equipe de conta do Adobe para obter mais informações.

![processo de criação de segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Depois de criar os públicos-alvo, você pode usá-los no [!DNL Google Ads] campanhas como [metas ou exclusões no nível da campanha ou do grupo de anúncios](#audience-manager-targets).

### Usar Audience Manager e outros [!DNL Adobe] Segmentos para direcionar ou excluir anúncios {#audience-manager-targets}

* (Anunciantes aceitos com [!DNL Search, Social, & Commerce]) É possível usar qualquer [!DNL Google Ads] públicos-alvo que foram [criado usando [!DNL Adobe] segmentos](#audience-manager-google-audiences) como exclusões ou alvos no nível da campanha ou do grupo de anúncios no [!DNL Google Ads] campanhas.

* (Anunciantes com DSP) Você pode usar seu anúncio existente [!DNL Adobe] segmentos como destinos para seus posicionamentos de anúncios. Opcionalmente, é possível incluir os segmentos em públicos-alvo reutilizáveis, que você pode usar como destinos ou exclusões para vários posicionamentos.

* (Anunciantes com Advertising Creative) Você pode usar sua [!DNL Adobe] segmentos como alvos para criações específicas em suas experiências de anúncio.

>[!NOTE]
>
>Para obter mais informações sobre como criar públicos-alvo no Audience Manager e no Experience Cloud [!DNL Audience Library] e casos de uso comuns para diferentes tipos de público, consulte &quot;[Opções de criação de público-alvo](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Enviar dados de exposição da mídia DSP para o Audience Manager

*Anunciantes somente com DSP*

Clientes DSP com Adobe Audience Manager podem capturar dados de campanhas de publicidade usando chamadas de pixel para Audience Manager. Em seguida, você pode usar os dados da campanha para criar características com base em regras, que podem ser usadas para definir novos segmentos para habilitar vários casos de uso do DSP, como segmentação mais avançada, gerenciamento de frequência, análise de marketing e insights de relatórios.

Consulte &quot;[Visão geral do envio de dados de exposição da mídia DSP para o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

## Obtenha insights mais avançados sobre a atividade do site com o Audience Analytics

Clientes da Adobe Advertising com [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) pode enviar dados de Adobe rastreados por publicidade e segmentos de Audience Manager para [!DNL Analytics] para obter insights enriquecidos sobre a atividade do site.

Para obter mais informações, consulte &quot;[[!DNL Adobe Audience Analytics] para clientes da Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md).&quot;
