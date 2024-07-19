---
title: Gerenciar contas de comerciante
description: Saiba como configurar e gerenciar detalhes de uma conta da central de comércio.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Gerenciar contas de comerciante

*Somente funções de gerente de conta de agência, gerente de conta de Adobe e administrador de usuário*

O Search, Social e Commerce pode baixar e exibir dados de produtos todos os dias para qualquer uma das contas do Google Merchant Center ou do Microsoft Merchant Center de um anunciante. Além disso, o Search, Social e Commerce pode automatizar a criação de anúncios com base no conteúdo da conta de comerciante.Para trabalhar diretamente com os dados do produto no Search, Social e Commerce, você deve criar um registro de conta correspondente contendo as credenciais de acesso da conta e com o acesso *habilitado*.

>[!NOTE]
>
>Você não pode remover um registro de conta de comerciante. Você pode desabilitar o acesso a uma conta alterando o tipo de conta para *desabilitado*.

## Criar detalhes da conta de comerciante {#create-merchant-account}

*Somente funções de gerente de conta de agência, gerente de conta de Adobe e administrador de usuário*

Para exibir dados do produto e gerar modelos de rastreamento para uma conta de comerciante, e para criar anúncios com base nos dados, você deve criar um registro de conta correspondente contendo as credenciais de acesso da conta e com acesso à conta *habilitada*.

>[!NOTE]
>
>Para criar uma conta real na rede do comerciante, vá para o site da rede.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, que abrirá a guia [!UICONTROL Accounts].

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Account]**.

1. Especifique as [configurações da conta do comerciante](#merchant-account-settings):

   1. No menu [!UICONTROL Product Source], selecione o centro de comércio.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Obrigatório para contas do [!DNL Google Ads]; opcional para contas do [!DNL Microsoft Advertising]) Permitir que o Search, Social e &amp; Commerce acessem a conta usando o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/):

      1. (somente contas do [!DNL Microsoft Advertising]) Selecione **[!UICONTROL oAuth]**.

      1. Clique em **[!UICONTROL Enable Connection]**.

      1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta do anunciante. A prática recomendada é usar as credenciais para o acesso da API de conteúdo à conta da central do comerciante.

      1. Na tela de solicitação de acesso/permissão, clique no botão para confirmar a permissão.

      1. Copie a cadeia de caracteres de autenticação na janela pop-up que é aberta e cole-a no campo **[!UICONTROL oAuth Token]**.

      1. Especifique as outras configurações da conta.

1. Clique em **[!UICONTROL Save]**.

   Os dados de atributo de todos os produtos na conta do ficam disponíveis no Search, Social e Commerce após o próximo processo diário de sincronização (cerca de 06:00 no fuso horário local do usuário). Você pode usar os dados do produto para automatizar a criação de anúncios usando feeds de inventário.

## Editar detalhes da conta de comerciante {#edit-merchant-account}

*Somente funções de gerente de conta de agência, gerente de conta de Adobe e administrador de usuário*

Se as credenciais da conta forem alteradas ou se você quiser parar de recuperar e usar dados de uma conta de comerciante, edite os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede do comerciante, vá para o site da rede.

1. No menu principal, clique em **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, que abrirá a guia [!UICONTROL Accounts].

1. Ao lado do nome da conta, clique em ![Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Exibir/editar configurações").

1. Edite as [configurações da conta do comerciante](#merchant-account-settings).

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social e Commerce devem sincronizar os novos dados da conta com os da rede de estabelecimentos comerciais. Isso acontece automaticamente uma vez por dia, por volta das 06:00 no fuso horário local do usuário.

## Desabilitar acesso a uma conta de comerciante {#disable-merchant-account}

*Somente funções de gerente de conta de agência, gerente de conta de Adobe e administrador de usuário*

Ao desativar uma conta de comerciante, o Search, o Social e o Commerce não fazem logon na conta e, portanto, não recuperam os dados atualizados do produto. Os dados coletados enquanto a conta estava habilitada ainda são armazenados e os anúncios existentes criados usando os dados do produto não são atualizados, pausados ou excluídos de acordo com o modelo de feed e as configurações de dados do feed.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , que abrirá a guia [!UICONTROL Accounts].

1. Ao lado do nome da conta, clique em ![Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Exibir/editar configurações").

1. Altere o [!UICONTROL EF Account Type] para **[!UICONTROL Disabled]**.

1. Clique em **[!UICONTROL Save]**.

## Configurações da conta de comerciante {#merchant-account-settings}

>[!NOTE]
>
>Somente as funções de gerente de conta de agência, gerente de conta [!DNL Adobe] e administrador podem definir configurações de conta de comerciante.

**[!UICONTROL Product Source]:** A rede de comerciante. Você não pode alterar o valor de uma conta existente.

**[!UICONTROL OAuth Token]:** (somente contas [!DNL Google Merchant Center]) O token da conta para autorizar logons usando o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] somente) Se autorizar logons na conta usando:

* *[!UICONTROL Client login]:* Para usar o logon do cliente.

* *[!UICONTROL oAuth]* (o padrão): Para usar o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] somente) A chave de acesso da conta de desenvolvedor a ser usada.

**[!UICONTROL Account Name]:** O nome exibido para a conta no Search, Social e Commerce.

**[!UICONTROL Login]:** O nome ou ID de logon da conta.

**[!UICONTROL Password]:** A senha da conta.

**[!UICONTROL Confirm Password]:** A senha da conta.

**[!UICONTROL EF Account Type]:** Se o Search, Social e Commerce acessam a conta:

* *[!UICONTROL Enabled]* (padrão): Search, Social e Commerce podem fazer logon na conta para recuperar dados do produto.

* *[!UICONTROL Disabled]:* O Search, Social e Commerce não faz logon na conta e, portanto, não recupera dados atualizados do produto. Os dados coletados enquanto a conta estava habilitada ainda são armazenados e os anúncios existentes criados usando os dados do produto não são atualizados, pausados ou excluídos de acordo com o modelo de feed e as configurações de dados do feed.

**[!UICONTROL Account ID]:** A ID da conta do comerciante. Se você tiver apenas uma conta com as informações de logon especificadas, esse valor será opcional.

**[!UICONTROL Time Zone]:** O fuso horário do anunciante. Use o mesmo fuso horário configurado para as informações de conta de Pesquisa, Social e Commerce do anunciante (que é definido quando a conta é criada). Você não pode alterar o valor de uma conta existente.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de anúncios](ad-network-account-about.md)
>* [Gerenciar contas de rede de publicidade](ad-network-account-manage.md)
