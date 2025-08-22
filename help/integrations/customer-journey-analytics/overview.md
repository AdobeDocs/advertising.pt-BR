---
title: Visão geral da integração entre o Adobe Advertising e o Adobe Customer Journey Analytics
description: Saiba mais sobre as opções para integrar o Adobe Advertising ao Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 1e8305031b175f9bb1c52b82b6ed4913e6108349
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Visão geral da integração entre o Adobe Advertising e o Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O Adobe Advertising é integrado ao Adobe Customer Journey Analytics para estender e aprimorar os recursos de cada produto. Há duas opções para configurar a integração:

* Anunciantes com [!DNL Analytics for Advertising] e Customer Journey Analytics têm a mesma funcionalidade que têm até [!DNL Analytics for Advertising], com a adição de visualizações no Customer Journey Analytics.

  Você ainda rastreará eventos de click-through usando o Adobe Experience Platform Web SDK (`alloy.js`) ou o Adobe Experience Cloud Identity Service (`visitorAPI.js`). Os anunciantes com o Advertising DSP ainda usarão um trecho do JavaScript para rastrear eventos de view-through. Os dados disponíveis no Customer Journey Analytics incluem:

   * Dados de desempenho da campanha do Adobe Advertising

   * Atividade do site e conversões controladas por [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta]

   * Dados de atribuição de [!DNL Analytics], que podem ser usados para otimização e relatórios no Adobe Advertising

  Nesse caso de uso, não é necessário executar nenhuma etapa extra, exceto para [coletar opcionalmente dados históricos para IDs AMO e IDs EF para uso no Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

* (Recurso beta futuro) Os anunciantes com o Customer Journey Analytics, mas não com o [!DNL Analytics for Advertising], podem trocar nativamente os dados a seguir entre o Adobe Advertising e o Customer Journey Analytics rastreando eventos de click-through e view-through com o Adobe Experience Platform Web SDK (`alloy.js`). Os dados estão disponíveis nos níveis de campanha, grupo de publicidade, pacote, disposição e palavra-chave.

   * Dados de desempenho da campanha do Adobe Advertising

     **Observação:** dados de [!DNL Apple] e [!DNL Tiktok] não estão disponíveis.

   * Atividade do site e conversões controladas por [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta]

   * Dados de atribuição do Customer Journey Analytics, que podem ser usados para otimização e relatórios no Adobe Advertising

  **Observação:** ainda não há dados orgânicos disponíveis.<!-- Does that belong somewhere up above? -->

  Nesse caso de uso, use o Web SDK para rastrear eventos do site (usando cookies, endereços IP com hash ou IDs universais) e atribuir os eventos do site à atividade de mídia paga em [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] e Adobe DSP. Você também usará o Adobe Experience Platform para a coleta de dados.

## Como iniciar uma integração nativa entre o Adobe Advertising e o Customer Journey Analytics

Entre em contato com a equipe de conta da Adobe, que concluirá a configuração inicial necessária para começar e ajudará você a planejar a implementação e o uso de dados com base nas necessidades da organização.

>[!MORELIKETHIS]
>
>* [Pré-requisitos](prerequisites.md)
>* (Usuários do Adobe Analytics) [Coletar Dados Históricos para IDs AMO e IDs EF para Uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
