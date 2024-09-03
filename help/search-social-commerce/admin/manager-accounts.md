---
title: Gerenciar credenciais para contas do gerenciador de rede de anúncios
description: Saiba como fornecer credenciais para suas  [!DNL Google Ads] contas de gerente.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Gerenciar credenciais para contas do gerenciador de rede de anúncios

*[!DNL Google Ads]somente contas*

Forneça as credenciais das suas contas de gerente do [!DNL Google Ads] para as quais você deseja que o Search, Social e Commerce carregue conversões entre contas. Use este recurso se desejar a) carregar [!DNL Adobe] métricas de conversão entre contas rastreadas para uma conta de gerente [!DNL Google Ads] ou b) carregar objetivos de portfólio que incluem conversões entre contas para [!DNL Google Ads] para otimização híbrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Você pode adicionar credenciais para novos registros de conta de gerente ou reautenticar uma conta de gerente existente.

Depois de adicionar credenciais para uma conta de gerente, as configurações da conta mostram a ID da conta de gerente associada como somente leitura. Além disso, uma coluna opcional &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; na exibição [!UICONTROL Campaigns] > [!UICONTROL Accounts] mostra a ID da conta de gerente para cada conta filho e indica um erro quando a conta de gerente não está autenticada. [!UICONTROL Notification Center] inclui notificações quando as credenciais de uma conta de gerente estão ausentes ([o [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou quando um token de autenticação de conta de gerente expira ([o [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Para adicionar credenciais de uma nova conta de gerente

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecione **[!UICONTROL Create new manager account]**.

1. Insira as credenciais de logon da conta de gerente.

   O **[!UICONTROL Manager Account ID]** e **[!UICONTROL Login Email]** são obrigatórios. O Search, Social e Commerce captura e armazena automaticamente o token de conta a ser usado para autenticação.

   Opcionalmente, você pode incluir um **[!UICONTROL MCC Account Name]** para identificação no Search, Social, &amp; Commerce e na conta **[!UICONTROL Password]**. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

1. Clique em **[!UICONTROL Authenticate]**.

1. Clique em **[!UICONTROL Save]**.

## Para autenticar novamente uma conta de gerente existente

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

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
