---
title: Pré-requisitos para integração do Adobe Advertising com o Customer Journey Analytics
description: Pré-requisitos para integração do Adobe Advertising com o Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 194675147b64af37de6373116f246f1e61388a23
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Pré-requisitos para integração do Adobe Advertising com o Customer Journey Analytics

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

* Anunciantes com [!DNL Analytics for Advertising] e Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [Todos os outros pré-requisitos para [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Anunciantes com Customer Journey Analytics, mas não [!DNL Analytics for Advertising]:

   * Biblioteca Adobe Experience Platform Web SDK: `alloy.js`

     O [!DNL Org ID] usado para o Web SDK e para a conta de anunciante do Adobe Advertising deve ser o mesmo. Você pode encontrar essa ID na [guia Resumo do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=pt-BR).

     ![Tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

     Você precisará do suporte do administrador do site do Experience Platform para criar um fluxo de dados do Experience Platform e um esquema XDM.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     Você precisará do suporte de seu analista da Web interno para configurar uma conexão com seu conjunto de dados e configurar os relatórios.

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente de cada biblioteca.

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* (Usuários do Adobe Analytics) [Coletar Dados Históricos para IDs AMO e IDs EF para Uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
