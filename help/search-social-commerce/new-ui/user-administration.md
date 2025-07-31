---
title: (Nova interface do usuário) Administração de usuários
description: Saiba como gerenciar o acesso de usuários.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Nova interface de usuário) Administração de usuários para pesquisa, redes sociais e comércio

Alguns usuários podem gerenciar o acesso à nova interface do Search, Social e Commerce usando a [Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html), que é o local central para gerenciar todos os direitos e o gerenciamento de usuários da Adobe. Os usuários são categorizados como usuários finais ou administradores. Sua equipe de conta da Adobe vai notificá-lo se você for um administrador. Se você for um administrador, consulte as seguintes seções para identificar suas permissões e fluxos de trabalho para gerenciar usuários.

## Tipos de administradores

O Admin Console fornece vários tipos de administradores. Os seguintes tipos de administradores e permissões são necessários para o Search, Social e Commerce. Você pode adicionar outros tipos se desejar delegar tarefas de gerenciamento de usuários.

**Administrador do sistema:** Superusuário que gerencia todos os produtos da organização, incluindo todas as instâncias de clientes da organização. (As instâncias do cliente são as mesmas que as contas de anunciante herdadas, com uma ou mais instâncias por ID de organização). Um administrador do sistema pode executar todas as tarefas administrativas no Admin Console para a organização e pode delegar a funcionalidade administrativa a outros usuários para qualquer produto da organização.

**Administrador de produto:** gerencia o acesso a um produto [!DNL Adobe] específico (como Search, Social e Commerce) e aos direitos de usuário desse produto. Os administradores de produtos podem criar perfis de produtos para o produto, criar (mas não remover) usuários e grupos de usuários para o produto, adicionar ou remover usuários e grupos de usuários dos perfis de produtos e adicionar ou remover outros administradores de produtos do produto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Perfis de produto padrão

Os perfis de produto, que são semelhantes a funções, habilitam os usuários com serviços específicos para um produto específico.

A nova interface de usuário do Search, Social &amp; Commerce tem os seguintes perfis de produto padrão, que fornecem diferentes subconjuntos de recursos e serviços. Não é possível editar as permissões de produto para os perfis de produto padrão ou excluir os perfis de produto padrão. No entanto, administradores de produtos, administradores de perfis de produtos e administradores de sistemas podem criar e gerenciar perfis de produtos adicionais com diferentes subconjuntos de permissões disponíveis, conforme necessário.

* **[!UICONTROL Basic Optimization]:** Este perfil fornece a seguinte funcionalidade:

   * [!UICONTROL Objectives]: Acesso total

   * [!UICONTROL Simulations]: Acesso total

   * [!UICONTROL Portfolio Groups]: Acesso total

   * [!UICONTROL Portfolios]: Criar/editar acesso às configurações do portfólio para [!UICONTROL Objectives], [!UICONTROL Campaigns] e Gastos [!UICONTROL Management]; acesso somente leitura às configurações restantes do portfólio.

   * [!UICONTROL Campaigns]: Acesso somente leitura às configurações da campanha (nenhum recurso criar, editar ou excluir está disponível); acesso total à restrição e atribuições do portfólio

   * [!UICONTROL Ad Groups]: Acesso somente leitura às configurações do grupo de anúncios (nenhum recurso para criar, editar ou excluir está disponível); acesso total à restrição e atribuições do portfólio

  Esse nível de acesso é preferido para usuários que ainda estão aprendendo a usar o Search, Social e Commerce.

* **[!UICONTROL Expert Optimization]:** Este perfil fornece a seguinte funcionalidade:

   * [!UICONTROL Objectives]: Acesso total

   * [!UICONTROL Simulations]: Acesso total

   * [!UICONTROL Portfolio Groups]: Acesso total

   * [!UICONTROL Portfolios]: Acesso total

   * [!UICONTROL Campaigns]: Acesso somente leitura à lista de campanhas (nenhum recurso de criação, edição ou exclusão de campanha está disponível); acesso total a atribuições de portfólio e restrições

   * [!UICONTROL Ad Groups]: Acesso somente leitura à lista de grupos de anúncios (nenhum recurso de criação, edição ou exclusão de campanha está disponível ainda); acesso total a atribuições de restrição e portfólio

  Esse nível de acesso é recomendado para usuários especialistas de Search, Social e Commerce.

* **[!UICONTROL Read-Only]:** Este perfil fornece a seguinte funcionalidade:

   * [!UICONTROL Objectives]: Acesso somente leitura

   * [!UICONTROL Simulations]: Acesso somente leitura

   * [!UICONTROL Portfolio Groups]: Acesso somente leitura

   * [!UICONTROL Portfolios]: Acesso somente leitura

   * [!UICONTROL Campaigns]: Acesso somente leitura

   * [!UICONTROL Ad Groups]: Acesso somente leitura

* **[!UICONTROL Admin]:** Este perfil concede acesso total a todas as funcionalidades disponíveis e permite que os usuários criem novas instâncias do cliente (o mesmo que contas de anunciante herdadas, com uma ou mais instâncias por ID de organização). Não atribua esse direito a ninguém a menos que você tenha uma justificativa de negócios apropriada.

## Tarefas para administradores

### Faça logon no Adobe Admin Console e abra-o no Search, Social e Commerce

>[!PREREQUISITES]
>
>Você deve ter algum tipo de acesso de administrador ao Search, Social e Commerce para fazer logon no Admin Console.

1. Acesse https://adminconsole.adobe.com/enterprise/.

1. (Se você não estiver conectado ao Experience Cloud) Faça logon no Experience Cloud:

   1. Insira sua ID do [!DNL Adobe] e clique em **[!UICONTROL Continue]**.

   1. Selecione **[!UICONTROL Personal Account]&quot; ou **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Selecione a organização da Experience Cloud aplicável.

      O Admin Console abre na guia [!UICONTROL Overview].

   1. Em [!UICONTROL Product & services], clique em &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name].&quot;

      A página do produto abre na guia [!UICONTROL Product profiles] para Search, Social e Commerce. As guias adicionais incluem [!UICONTROL Users] e [!UICONTROL Product Admins].

### Fluxo de trabalho para administradores do sistema

Siga este fluxo de trabalho para cada instância de cliente do Search, Social e Commerce.

1. [Entre no Adobe Admin Console e abra-o no Search, Social e Commerce](#open-admin-console).

1. (Opcional) [Adicionar outro administrador do sistema](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) como backup.

1. Delegar gerenciamento de produtos e usuários [adicionando administradores de produtos](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Fluxo de trabalho para administradores de produtos

Siga este fluxo de trabalho para cada instância de cliente do Search, Social e Commerce.

1. [Entre no Adobe Admin Console e abra-o no Search, Social e Commerce](#open-admin-console).

1. Conforme necessário, crie usuários finais [individualmente](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) ou [em massa](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Opcional) Crie [grupos de usuários](https://helpx.adobe.com/enterprise/using/user-groups.html) para a instância e atribua usuários a cada grupo de usuários.

   Se a instância tiver muitos usuários, crie grupos de usuários para garantir que os usuários recebam os perfis certos com base em seu nível de conhecimento. (Consulte a Etapa 4 para atribuir grupos de usuários a perfis de produtos.) Você pode criar grupos de usuários com base na linha de negócios, nas necessidades de acesso do usuário, na data de admissão do usuário ou em outros critérios.

   >[!IMPORTANT]
   >
   >Os nomes dos grupos de usuários devem comunicar claramente os direitos que o grupo de usuários deve receber. Por exemplo, se você deseja criar um grupo de usuários com direitos &quot;Somente leitura&quot;, inclua &quot;Somente leitura&quot; no nome do grupo de usuários, como &quot;Acme_Uk_ReadOnly&quot; ou &quot;Acme_ReadOnly&quot;.

1. (Opcional) [Criar perfis de produto personalizados](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) com conjuntos de permissões definidos.

   Os perfis personalizados estão além dos quatro perfis de produto padrão que já estão disponíveis.

   Cada perfil de produto de uma organização deve ter um nome exclusivo. Se sua organização usar várias instâncias de Pesquisa, Social e Commerce (por exemplo, Acme_US e Acme_JP), você não poderá duplicar um nome de perfil de produto em várias instâncias. **Prática recomendada:** Use a convenção de nomenclatura `<Name>_<Instance>,`, como &quot;Simulations_Only_JP&quot;.

   **Cuidado:** as permissões do produto são muito granulares. Tenha cuidado ao configurar perfis de produto personalizados ou ao omitir funcionalidades que deseja incluir.

1. [Atribua manualmente ou em massa cada usuário ou grupo de usuários ao perfil de produto relevante](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html).

## Guia completo de administração de usuários e links adicionais

* Para obter mais informações sobre a administração de usuários usando o Adobe Admin Console, consulte o &quot;[Guia de Administração do Adobe Enterprise &amp; Teams](https://helpx.adobe.com/enterprise/admin-guide.html)&quot;, incluindo a [visão geral do Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
