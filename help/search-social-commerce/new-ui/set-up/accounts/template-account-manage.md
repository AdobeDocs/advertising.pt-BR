---
title: (Nova interface do usuário) Gerenciar  [!DNL Naver] contas somente para rastreamento
description: Saiba como configurar e gerenciar detalhes da conta na nova interface do usuário para uma conta  [!DNL Naver] .
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar contas do [!DNL Naver] somente para rastreamento

*recurso do Beta*

Veja a seguir instruções para gerenciar [[!DNL Naver] contas](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) para acompanhar, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de publicidade. O Search, Social e Commerce não sincroniza dados com a rede de anúncios, fornece lances automatizados ou fornece qualquer tipo de otimização ou simulações.

Para obter detalhes sobre a funcionalidade disponível, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Criar detalhes da conta de rede de publicidade {#create-account}

Para habilitar o rastreamento de uma conta, você deve criar um registro de conta correspondente contendo as credenciais de acesso da conta e com o status *habilitado*.

>[!NOTE]
>
>Para criar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Clique em **[!UICONTROL Create Account]**.

1. Clique no nome da rede de publicidade e clique em **[!UICONTROL Next]**.

1. Especifique as [configurações da conta](#account-settings-naver):

   1. Na guia **[!UICONTROL Enter Account Details]**, especifique as configurações gerais da conta.

   1. (Anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e selecione todos os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

1. Clique em **[!UICONTROL Save]**.

## Editar detalhes da conta de rede de publicidade {#edit-account}

Para alterar o nome da conta, o status da conta ou os conjuntos de relatórios [!DNL Analytics] a serem usados para rastreamento e relatórios, edite os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

1. Edite as [configurações da conta](#account-settings-api):

   1. (Opcional) Na guia **[!UICONTROL Account Details]**, edite os detalhes da conta.

   1. (Opcional; anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e edite os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Clique em **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Adicionar configurações de conta de rede {#account-settings-api}

### Guia [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, peça à sua Equipe de conta da Adobe para atualizar o mapeamento.

**[!UICONTROL Network Account ID]:** A ID de conta atribuída pela rede de publicidade.

**[!UICONTROL Currency]:** A abreviação da moeda usada na conta.

**[!UICONTROL Time Zone]:** O fuso horário do anunciante.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** O Search, Social e Commerce sincroniza dados de campanha com a conta (quando há suporte) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.

## Guia [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes com [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md); opcional) Um ou mais conjuntos de relatórios do Analytics para os quais Search, Social e Commerce enviam dados carregados para a rede de publicidade, incluindo classificações de entidade e dados de cliques da conta.

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve ser habilitada. Além disso, a conta [!DNL Analytics] do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com a equipe de conta da Adobe.

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Sobre contas de rede de anúncios](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
