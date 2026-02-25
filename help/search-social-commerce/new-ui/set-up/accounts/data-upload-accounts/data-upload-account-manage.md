---
title: Configurar contas de rede de publicidade para upload de dados
description: Saiba como configurar e gerenciar detalhes de uma conta de rede de anúncios.
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Gerenciar contas de rede de publicidade para uploads de dados

<!-- Edit all, including title and metadata -->

A seguir estão instruções para gerenciar detalhes de contas de redes de anúncios para as quais você fará upload dos dados da conta.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Para obter instruções sobre como gerenciar detalhes de uma conta de rede de anúncios que o Search, Social e Commerce sincroniza usando a API da rede de anúncios, consulte &quot;[Gerenciar contas de rede de anúncios por meio da conexão de API](../api-accounts/api-account-manage.md)&quot;.

## Criar detalhes da conta {#create-account}

1. Clique em **[!UICONTROL Create Account]**.

1. Clique no nome da rede de publicidade e clique em **[!UICONTROL Next]**.

1. Especifique as [configurações da conta](#account-settings):

   1. Na guia **[!UICONTROL Account Details]**, edite os detalhes da conta.

   1. (Anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e edite os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

   1. (Opcional) Na guia **[!UICONTROL Upload File]**, carregue arquivos de dados da conta.

1. Clique em **[!UICONTROL Save]**.

## Editar detalhes da conta {#edit-account}

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

1. Edite as [configurações da conta](#account-settings-upload):

   1. (Opcional) Na guia **[!UICONTROL Account Details]**, edite os detalhes da conta.

   1. (Opcional; anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e edite os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

   1. (Opcional) Na guia **[!UICONTROL Upload File]**, carregue arquivos de dados da conta.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Clique em **[!UICONTROL Save]**.

## Ativar ou desativar contas de rede de publicidade {#enable-disable-account}

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Da exibição [!UICONTROL Accounts]):

      * (Para habilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Activate]** na barra de ferramentas de ações em massa.

      * (Para desabilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Pause]** na barra de ferramentas de ações em massa.

   * (Nas configurações da conta):

      1. Selecione a conta de uma das seguintes maneiras:

         * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

         * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

      1. Na guia **[!UICONTROL Account Details]**, desative o **[!UICONTROL Account enabled]**.

      1. Clique em **[!UICONTROL Save]**.

## Configurações da conta {#account-settings-upload}

### Guia [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, notifique a Equipe de conta da Adobe para que ela possa atualizar o mapeamento.

**[!UICONTROL Network Account ID]:** A ID de conta atribuída pela rede de publicidade. Essa ID é usada somente para relatórios. Search, Social e Commerce não se conectam diretamente à conta da rede de publicidade.

**[!UICONTROL Currency]:** (Somente leitura para contas existentes) A abreviação da moeda usada para a conta.

**[!UICONTROL Time Zone]:** (Somente leitura para contas existentes) O fuso horário do anunciante.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** O Search, Social e Commerce permite a busca automatizada de dados para um bucket do S3 especificado.

## Guia [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes com [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md); opcional) Um ou mais conjuntos de relatórios do Analytics para os quais Search, Social e Commerce enviam dados carregados para a rede de publicidade, incluindo classificações de entidade e dados de cliques da conta.

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve ser habilitada. Além disso, a conta [!DNL Analytics] do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com a equipe de conta da Adobe.

### Guia [!UICONTROL Upload File]

(Opcional) Carregar arquivos de dados para a conta.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
