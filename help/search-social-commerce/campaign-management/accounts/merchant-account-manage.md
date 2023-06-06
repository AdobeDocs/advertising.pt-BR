---
title: Gerenciar contas de comerciante
description: Saiba como configurar e gerenciar detalhes de uma conta da central de comércio.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Gerenciar contas de comerciante

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

A Search, Social e Commerce pode baixar e exibir dados de produtos todos os dias para qualquer uma das contas do Google Merchant Center ou do Microsoft Merchant Center de um anunciante. Além disso, o Search, Social e Commerce pode automatizar a criação de anúncios com base no conteúdo da conta do comerciante.Para trabalhar diretamente com os dados do produto no Search, Social e Commerce, você deve criar um registro de conta correspondente contendo as credenciais de acesso da conta e com acesso *habilitado*.

>[!NOTE]
>
>Você não pode remover um registro de conta de comerciante. Você pode desativar o acesso a uma conta alterando o tipo de conta para *desabilitado*.

## Criar detalhes da conta de comerciante {#create-merchant-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Para exibir dados do produto e gerar modelos de rastreamento para uma conta de comerciante, e para criar anúncios com base nos dados, você deve criar um registro de conta correspondente contendo as credenciais de acesso da conta e com acesso à conta *habilitado*.

>[!NOTE]
>
>Para criar uma conta real na rede do comerciante, vá para o site da rede.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, que abre para o [!UICONTROL Accounts] guia.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Create Account]**.

1. Especifique a [configurações da conta de comerciante](#merchant-account-settings):

   1. No [!UICONTROL Product Source] selecione o centro de comércio.

   1. (Obrigatório para [!DNL Google Ads] contas; opcional para [!DNL Microsoft Advertising] contas) Permitir que o Search, Social e Commerce acesse a conta usando o [[!DNL OAuth] protocolo de autorização](http://tools.ietf.org/html/draft-ietf-oauth-v2-22):

      1. ([!DNL Microsoft Advertising] somente contas) Selecionar **[!UICONTROL oAuth]**.

      1. Clique em **[!UICONTROL Enable Connection]**.

      1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta do anunciante. A prática recomendada é usar as credenciais para o acesso da API de conteúdo à conta da central do comerciante.

      1. Na tela de solicitação de acesso/permissão, clique no botão para confirmar a permissão.

      1. Copie a string de autenticação na janela pop-up que é aberta e cole a string na **[!UICONTROL oAuth Token]** campo.

      1. Especifique as outras configurações da conta.

1. Clique em **[!UICONTROL Save]**.

   Os dados de atributo de todos os produtos na conta do estão disponíveis em Pesquisa, Social e Comércio após o próximo processo diário de sincronização (cerca de 06:00 no fuso horário local do usuário). Você pode usar os dados do produto para automatizar a criação de anúncios usando feeds de inventário.

## Editar detalhes da conta de comerciante {#edit-merchant-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Se as credenciais da conta forem alteradas ou se você quiser parar de recuperar e usar dados de uma conta de comerciante, edite os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede do comerciante, vá para o site da rede.

1. No menu principal, clique em **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, que abre para o [!UICONTROL Accounts] guia.

1. Ao lado do nome da conta, clique em ![Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Exibir/editar configurações").

1. Edite o [configurações da conta de comerciante](#merchant-account-settings).

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>A Search, Social e Commerce deve sincronizar os novos dados da conta com os da rede de comerciantes. Isso acontece automaticamente uma vez por dia, por volta das 06:00 no fuso horário local do usuário.

## Desabilitar acesso a uma conta de comerciante {#disable-merchant-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Quando você desativa uma conta de comerciante, o Search, Social e Commerce não faz logon na conta e, portanto, não recupera os dados atualizados do produto. Os dados coletados enquanto a conta estava habilitada ainda são armazenados e os anúncios existentes criados usando os dados do produto não são atualizados, pausados ou excluídos de acordo com o modelo de feed e as configurações de dados do feed.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , que abre para o [!UICONTROL Accounts] guia.

1. Ao lado do nome da conta, clique em ![Exibir/editar configurações](/help/search-social-commerce/assets/settings.png "Exibir/editar configurações").

1. Altere o [!UICONTROL EF Account Type] para **[!UICONTROL Disabled]**.

1. Clique em **[!UICONTROL Save]**.

## Configurações da conta de comerciante {#merchant-account-settings}

>[!NOTE]
>
>Somente gerente de conta da agência, [!DNL Adobe] as funções de gerente de conta e administrador de usuário podem definir configurações de conta de comerciante.

**[!UICONTROL Product Source]:** A rede mercantil. Você não pode alterar o valor de uma conta existente.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] contas somente) O token da conta para autorizar logons usando o [[!DNL OAuth] protocolo de autorização](http://tools.ietf.org/html/draft-ietf-oauth-v2-22).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] somente) Se autorizar logons na conta usando:

* *[!UICONTROL Client login]:* Para usar o login do cliente.

* *[!UICONTROL oAuth]* (o padrão): Para usar a variável [[!DNL OAuth] protocolo de autorização](http://tools.ietf.org/html/draft-ietf-oauth-v2-22).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] somente) A chave de acesso para a conta de desenvolvedor usar.

**[!UICONTROL Account Name]:** O nome exibido para a conta no Search, Social e Commerce.

**[!UICONTROL Login]:** O nome ou ID de logon da conta.

**[!UICONTROL Password]:** A senha da conta.

**[!UICONTROL Confirm Password]:** A senha da conta.

**[!UICONTROL EF Account Type]:** Se o Search, Social e Commerce acessará a conta:

* *[!UICONTROL Enabled]* (o padrão): Search, Social e Commerce podem fazer logon na conta para recuperar dados do produto.

* *[!UICONTROL Disabled]:* O Search, Social e Commerce não faz logon na conta e, portanto, não recupera os dados atualizados do produto. Os dados coletados enquanto a conta estava habilitada ainda são armazenados e os anúncios existentes criados usando os dados do produto não são atualizados, pausados ou excluídos de acordo com o modelo de feed e as configurações de dados do feed.

**[!UICONTROL Account ID]:** A ID da conta do comerciante. Se você tiver apenas uma conta com as informações de logon especificadas, esse valor será opcional.

**[!UICONTROL Time Zone]:** O fuso horário do anunciante. Use o mesmo fuso horário configurado para as informações da conta de Pesquisa, Social e Comércio do anunciante (que é definido quando a conta é criada). Você não pode alterar o valor de uma conta existente.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de publicidade](ad-network-account-about.md)
>* [Gerenciar contas de rede de publicidade](ad-network-account-manage.md)

