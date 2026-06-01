---
title: (Nova interface do usuário) Gerenciar credenciais para contas de gerente do Google Ads
description: Saiba como configurar e gerenciar credenciais para contas de gerente do Google Ads na nova interface do usuário.
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar credenciais para contas de gerente do [!DNL Google Ads]

*recurso do Beta*

*[!DNL Google Ads]somente contas*

Forneça credenciais para suas contas de gerente do [!DNL Google Ads] para as quais você deseja que o Search, Social e Commerce carregue conversões entre contas. Use este recurso se desejar a) carregar [!DNL Adobe] métricas de conversão entre contas rastreadas para uma conta de gerente [!DNL Google Ads] ou b) carregar objetivos de portfólio que incluem conversões entre contas para [!DNL Google Ads] para otimização híbrida.

Você pode adicionar credenciais para novos registros de conta de gerente ou reautenticar uma conta de gerente existente.

Depois de adicionar credenciais para uma conta de gerente, as configurações da conta mostram a ID da conta de gerente associada como somente leitura. [!UICONTROL Notification Center] inclui [notificações](/help/search-social-commerce/new-ui/notifications-manage.md) quando as credenciais de uma conta de gerente estão ausentes (o [!UICONTROL Manager Account Missing Error]) ou quando um token de autenticação de conta de gerente expira (o [!UICONTROL Manager Account Auth Error]).

## Adicionar credenciais para uma nova conta de gerente {#create-manager-account}

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Clique em **[!UICONTROL +]**.

1. Selecione a rede de publicidade e clique em **[!UICONTROL Next]**.

1. Especifique as [configurações da conta de gerente](#manager-account-settings).

1. Clique em **[!UICONTROL Authenticate]** e faça logon usando as credenciais da conta de gerente.

   Search, Social e Commerce capturam e armazenam automaticamente o token de autenticação.

1. Em Pesquisar, Social e Commerce, clique em **[!UICONTROL Save]**.

## Editar detalhes da conta do gerente {#edit-manager-account}

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em  (/help/search-social-commerce/assets/edit-new.png &quot;Editar).

1. Edite as [configurações da conta de gerente](#manager-account-settings).

1. Clique em **[!UICONTROL Re-Authenticate]** e faça logon usando as credenciais da conta de gerente.

   Search, Social e Commerce capturam e armazenam automaticamente o token de autenticação.

1. Em Pesquisar, Social e Commerce, clique em **[!UICONTROL Save]**.

## Reautenticar uma conta de gerente {#reauthenticate-manager-account}

Reautentique uma conta de gerente quando o token OAuth expirar ou se tornar inválido.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Reauthenticate]**.

1. Faça logon usando as credenciais da conta de gerente.

   Search, Social e Commerce capturam e armazenam automaticamente o novo token de autenticação.

## Configurações da conta do gerente {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** A identificação de conta exclusiva para a conta de gerente na rede de publicidade.

**[!UICONTROL Mnaager Account Name]:** O nome a ser exibido para a conta de gerente em Pesquisa, Social e Commerce.

**[!UICONTROL Login Email]:** O endereço de email associado ao logon da conta de gerente. Necessário para autenticação.

**[!UICONTROL Password]:** (Opcional) A senha da conta. Digite a senha quando quiser criptografá-la e salvá-la para que o gerente de conta possa atualizar os tokens conforme necessário.

>[!MORELIKETHIS]
>
>* [Habilitar carregamento de objetivos em redes de anúncios](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Gerenciar notificações](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
