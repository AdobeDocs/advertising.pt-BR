---
title: Sincronizar [!DNL Adobe] públicos-alvo
description: Saiba como sincronizar metadados, dados de hierarquia e dados de público-alvo exclusivos para seus  [!DNL Adobe]  públicos-alvo.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Sincronizar [!DNL Adobe] públicos-alvo

Somente *[!DNL Direct Access]gerentes e administradores de clientes*

*Anunciantes somente com integração Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics*

Você pode permitir que o Search, Social e Commerce obtenha metadados, dados de hierarquia e dados exclusivos de público-alvo para todos os públicos-alvo [!DNL Adobe] de um anunciante ou agência nas visualizações [!UICONTROL Campaigns] > [!UICONTROL Audiences]. Essas informações incluem dados para:

* Segmentos do Adobe Audience Manager

* Segmentos do Adobe Analytics publicados no Adobe Experience Cloud

* Segmentos criados usando o Adobe Experience Cloud [!DNL Audience Library]

Para ser elegível, o anunciante ou a agência devem implementar o [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=pt-BR) e fornecer sua ID da organização (anteriormente chamada de [!DNL IMS Org ID]).

A sincronização inicial leva cerca de 24 horas. Depois disso, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Insira o identificador exclusivo da organização para a conta da Adobe Experience Cloud do anunciante e clique em **[!UICONTROL Submit]**.

   Se você não souber a ID da organização do anunciante, procure-a no campo **[!UICONTROL IMS Org ID]** nas configurações do anunciante em [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integração com soluções e serviços da Adobe Experience Cloud](/help/search-social-commerce/introduction/integrations.md)
