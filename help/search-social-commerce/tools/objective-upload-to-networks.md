---
title: Habilitar carregamento de objetivos para redes de anúncios
description: Saiba como fazer upload de objetivos para seus portfólios híbridos no [!DNL Google Ads] e [!DNL Microsoft® Advertising].
exl-id: 75a1a804-ad6a-4dbc-9cde-30fe54476162
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Habilitar carregamento de objetivos para redes de anúncios

*Anunciantes com [!DNL Google Ads] e [!DNL Microsoft® Advertising] somente contas*

*Anunciantes habilitados somente para otimização híbrida*

Se a conta do anunciante estiver configurada para usar otimização híbrida, o Adobe Advertising poderá, opcionalmente, fazer upload dos objetivos dos portfólios da conta para [!DNL Google Ads] e [!DNL Microsoft® Advertising] como conversões, para que você possa usá-las para otimização híbrida.

Habilitar essa opção aciona automaticamente um upload para portfólios que contêm campanhas com estratégias de lances inteligentes. O Search, Social e Commerce cria uma conversão na rede de anúncios para cada combinação aplicável de portfólio e objetivo. Cada conversão tem o nome `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, onde `<portfolio_id>` é a ID numérica do portfólio e `<se_acctid/conversion_manager_se_acctid>` é a ID numérica da conta da rede de publicidade ou da conta de gerente. A conversão representa todas as propriedades de transação ponderadas no objetivo.

Carrega para [!DNL Google Ads] ocorrem diariamente às 06:00 no fuso horário do anunciante. Carrega para [!DNL Microsoft® Advertising] ocorrem diariamente às 9h no fuso horário do anunciante.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao lado de **[!UICONTROL Enable Objective Upload]**.

   Essa opção só estará disponível se a conta do anunciante estiver configurada para usar otimização híbrida. Para ativar a otimização híbrida, entre em contato com a equipe de conta do Adobe.

1. Clique em **[!UICONTROL Save]**.

1. (Se suas conversões forem rastreadas no nível de uma conta de gerente) [Adicionar credenciais para sua conta de gerente](/help/search-social-commerce/admin/manager-accounts.md) em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento das propriedades de transação de um anunciante](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [Fazer upload de métricas de conversão para [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
