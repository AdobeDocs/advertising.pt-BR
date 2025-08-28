---
title: Visão geral da integração entre o Adobe Advertising e o Adobe Customer Journey Analytics
description: Saiba mais sobre as opções para integrar o Adobe Advertising ao Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: b60834569c795013d989fca81c3799165250094b
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Visão geral da integração entre o Adobe Advertising e o Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O Adobe Advertising é integrado ao Adobe Customer Journey Analytics para compartilhamento e emissão de relatórios de dados bidirecionais. Há duas opções para configurar a integração:

* Anunciantes com [!DNL Analytics for Advertising] e Customer Journey Analytics têm a mesma funcionalidade que têm até [!DNL Analytics for Advertising], com a adição de visualizações no Customer Journey Analytics.

  Você ainda rastreará eventos de click-through usando o Adobe Experience Platform Web SDK (`alloy.js`) ou o Adobe Experience Cloud Identity Service (`visitorAPI.js`). Os anunciantes com o Advertising DSP ainda usarão um trecho do JavaScript para rastrear eventos de view-through. Os dados disponíveis no Customer Journey Analytics incluem:

   * Dados de desempenho da campanha do Adobe Advertising no Customer Journey Analytics

   * Atividade do site e conversões controladas por [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] no Customer Journey Analytics

   * Dados de atribuição de [!DNL Analytics] no Adobe Advertising, onde podem ser usados para otimização e relatórios

  Nesse caso de uso, não é necessário executar nenhuma etapa extra, exceto para [coletar opcionalmente dados históricos para IDs AMO e IDs EF para uso no Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

* (Recurso beta futuro) Anunciantes com o Customer Journey Analytics, mas não com o [!DNL Analytics for Advertising], podem trocar dados nativamente entre o Adobe Advertising e o Customer Journey Analytics usando a biblioteca [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`). Você pode rastrear eventos do site usando cookies, IP com hash e IDs universais ([!DNL LiveRamp RampIDs] e ID5 IDs) e atribuir eventos do site à atividade de mídia paga. Os seguintes dados estão disponíveis nos níveis de campanha, grupo de publicidade, pacote, disposição e palavra-chave:

   * Dados de desempenho da campanha do Adobe Advertising no Customer Journey Analytics

     **Observação:** dados de [!DNL Apple] e [!DNL Tiktok] não estão disponíveis.

   * Atividade do site e conversões controladas por [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] no Customer Journey Analytics

   * Dados de atribuição do Customer Journey Analytics no Adobe Advertising, onde podem ser usados para otimização e relatórios

  **Observação:** ainda não há dados orgânicos disponíveis.

  Nesse caso de uso, use o Web SDK para rastrear eventos do site (usando cookies, endereços IP com hash ou IDs universais) e atribuir os eventos do site à atividade de mídia paga em [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] e Adobe DSP. Você também usará o Adobe Experience Platform para a coleta de dados.

## Como iniciar uma integração nativa entre o Adobe Advertising e o Customer Journey Analytics

Entre em contato com a equipe de conta da Adobe, que concluirá a configuração inicial necessária para começar e ajudará você a planejar a implementação e o uso de dados com base nas necessidades da organização.

>[!MORELIKETHIS]
>
>* [Pré-requisitos](prerequisites.md)
>* (Usuários do Adobe Analytics) [Coletar Dados Históricos para IDs AMO e IDs EF para Uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
