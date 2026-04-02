---
title: Gerenciar credenciais para contas do gerenciador de rede de anúncios
description: Saiba como fornecer credenciais para suas  [!DNL Google Ads] contas de gerente.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
TQID: https://experienceleague.adobe.com/NHgpx-F19gX8jsOIPijPzNlGVhBje-CVsj4jjlV1OR0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 0%

---

# Gerenciar credenciais para contas do gerenciador de rede de anúncios

*[!DNL Google Ads]somente contas*

Forneça as credenciais das suas contas de gerente do [!DNL Google Ads] para as quais você deseja que o Search, Social e Commerce carregue conversões entre contas. Use este recurso se desejar a) carregar [!DNL Adobe] métricas de conversão entre contas rastreadas para uma conta de gerente [!DNL Google Ads] ou b) carregar objetivos de portfólio que incluem conversões entre contas para [!DNL Google Ads] para otimização híbrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Você pode adicionar credenciais para novos registros de conta de gerente ou reautenticar uma conta de gerente existente.

Depois de adicionar credenciais para uma conta de gerente, as configurações da conta mostram a ID da conta de gerente associada como somente leitura. Além disso, uma coluna opcional &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; na exibição [!UICONTROL Campaigns] > [!UICONTROL Accounts] mostra a ID da conta de gerente para cada conta filho e indica um erro quando a conta de gerente não está autenticada. [!UICONTROL Notification Center] inclui notificações quando as credenciais de uma conta de gerente estão ausentes ([o [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou quando um token de autenticação de conta de gerente expira ([o [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Para adicionar credenciais de uma nova conta de gerente

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecione **[!UICONTROL Create new manager account]**.

1. Insira as credenciais de logon da conta de gerente.

   O **[!UICONTROL Manager Account ID]** e **[!UICONTROL Login Email]** são obrigatórios. O Search, Social e Commerce captura e armazena automaticamente o token de conta a ser usado para autenticação.

   Opcionalmente, você pode incluir um **[!UICONTROL MCC Account Name]** para identificação no Search, Social, &amp; Commerce e na conta **[!UICONTROL Password]**. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

1. Clique em **[!UICONTROL Authenticate]**.

1. Clique em **[!UICONTROL Save]**.

## Para autenticar novamente uma conta de gerente existente

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecione **[!UICONTROL Reauthenticate existing manager account]**.

1. Selecione a conta do gerente.

1. Insira as credenciais de logon da conta de gerente.

   O **[!UICONTROL Manager Account ID]** e o **Email de Logon** são obrigatórios. O Search, Social e Commerce captura e armazena automaticamente o token de conta a ser usado para autenticação.

   Opcionalmente, você pode incluir um **[!UICONTROL MCC Account Name]** para identificação no Search, Social, &amp; Commerce e na conta **[!UICONTROL Password]**. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

1. Clique em **[!UICONTROL Authenticate]**.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Habilitar carregamento de objetivos em redes de anúncios](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Carregar métricas de conversão rastreadas por Pesquisa, Social e Commerce para [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Editar suas configurações de notificação](/help/search-social-commerce/notifications/notification-edit.md)
