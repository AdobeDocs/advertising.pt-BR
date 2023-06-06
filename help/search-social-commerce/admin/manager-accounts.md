---
title: Gerenciar credenciais para contas do gerenciador de rede de anúncios
description: Saiba como fornecer credenciais para o [!DNL Google Ads] contas de gerente.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Gerenciar credenciais para contas do gerenciador de rede de anúncios

*Recurso Beta*

*[!DNL Google Ads]somente contas*

Forneça as credenciais para o [!DNL Google Ads] As contas de gerente para as quais você deseja que o Search, Social e Commerce carregue conversões entre contas. Use este recurso se desejar a) fazer upload [!DNL Adobe]Métricas de conversão entre contas rastreadas para um [!DNL Google Ads] conta do gerente ou b) fazer upload de objetivos de portfólio que incluem conversões entre contas para [!DNL Google Ads] para otimização híbrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Você pode adicionar credenciais para novos registros de conta de gerente ou reautenticar uma conta de gerente existente.

Depois de adicionar credenciais para uma conta de gerente, as configurações da conta mostram a ID da conta de gerente associada como somente leitura. Além disso, um &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; na [!UICONTROL Campaigns] > [!UICONTROL Accounts] a exibição mostra a ID da conta do gerente para cada conta filho e indica um erro quando a conta do gerente não está autenticada. [!UICONTROL Notification Center] inclui notificações quando as credenciais de uma conta de gerente estão ausentes ([o [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou quando um token de autenticação de conta de gerente expira ([o [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Para adicionar credenciais de uma nova conta de gerente

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecionar **[!UICONTROL Create new manager account]**.

1. Insira as credenciais de logon da conta de gerente.

   A variável **[!UICONTROL Manager Account ID]** e **[!UICONTROL Login Email]** são obrigatórios. Search, Social e Commerce captura e armazena automaticamente o token de conta a ser usado para autenticação.

   Opcionalmente, é possível incluir uma **[!UICONTROL MCC Account Name]** para identificação no Search, Social, &amp; Commerce e na conta **[!UICONTROL Password]**. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

1. Clique em **[!UICONTROL Authenticate]**.

1. Clique em **[!UICONTROL Save]**.

## Para autenticar novamente uma conta de gerente existente

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecionar **[!UICONTROL Reauthenticate existing manager account]**.

1. Selecione a conta do gerente.

1. Insira as credenciais de logon da conta de gerente.

   A variável **[!UICONTROL Manager Account ID]** e **E-mail de login** são obrigatórios. Search, Social e Commerce captura e armazena automaticamente o token de conta a ser usado para autenticação.

   Opcionalmente, é possível incluir uma **[!UICONTROL MCC Account Name]** para identificação no Search, Social, &amp; Commerce e na conta **[!UICONTROL Password]**. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

1. Clique em **[!UICONTROL Authenticate]**.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Habilitar carregamento de objetivos para redes de anúncios](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Fazer upload de métricas de conversão para [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Editar suas configurações de notificação](/help/search-social-commerce/notifications/notification-edit.md)

