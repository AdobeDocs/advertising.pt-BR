---
title: Administração de usuários
description: Saiba como.
feature: Search Introduction
source-git-commit: ab6acc0ac777edb625b91a29464ca00a4407dcf1
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# (Nova interface de usuário) Administração de usuários para pesquisa, redes sociais e comércio

Alguns usuários podem gerenciar o acesso à nova interface do Search, Social e Commerce usando o Adobe Admin Console, que é o local central para gerenciar todos os direitos e o gerenciamento de usuários do Adobe. Os usuários são categorizados como usuários finais ou administradores. Sua equipe de conta da Adobe vai notificá-lo se você for um administrador. Se você for um administrador, consulte as seções a seguir para identificar suas permissões e fluxos de trabalho para gerenciar usuários.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Tipos de administradores relevantes

O Admin Console fornece vários tipos de administradores, mas somente os seguintes tipos de administradores e permissões são relevantes para o Search, Social e Commerce.

**Administrador do sistema:** Superusuário da organização. Um administrador do sistema pode executar todas as tarefas administrativas no Admin Console para a organização e pode delegar a funcionalidade administrativa a outros usuários (administradores de produto).&lt;!—, administradores de perfil de produto e administradores de grupo de usuários.  — Acho que é APENAS ADMINISTRADOR DE PRODUTOS PARA NÓS?  Verificar. —>

**Administrador de produto:** gerencia o acesso a um produto [!DNL Adobe] específico (como Search, Social e Commerce) e os direitos de seus usuários a esse produto. Os administradores de produtos podem criar perfis de produtos para o produto, criar (mas não remover) usuários e grupos de usuários, adicionar ou remover usuários e grupos de usuários dos perfis de produtos e adicionar ou remover outros administradores de produtos do produto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Perfis de produto padrão

Os perfis de produto, que são semelhantes a funções, habilitam os usuários com serviços específicos para um produto específico.

A nova interface de usuário do Search, Social &amp; Commerce tem os seguintes perfis de produto padrão, que fornecem diferentes subconjuntos de recursos e serviços. Não é possível editar ou excluir os perfis de produto padrão. No entanto, os administradores do sistema podem criar e gerenciar perfis de produtos adicionais com diferentes subconjuntos de permissões, conforme necessário.

* **Otimização Básica:** Este perfil fornece a seguinte funcionalidade:

   * Objetivos: acesso total

   * Simulações: acesso total

   * Grupos do Portfolio: acesso total

   * Portfólios: crie/edite acesso às configurações de portfólio para Objetivos, Campanhas e Gerenciamento de gastos; acesso somente leitura às configurações restantes do portfólio.

   * Campanhas: acesso somente leitura às configurações da campanha (nenhum recurso para criar, editar ou excluir está disponível); acesso total à restrição e atribuições do portfólio<!-- Is that the correct wording? -->

   * Grupos de Anúncios: acesso somente leitura às configurações do grupo de anúncios (nenhum recurso de criar, editar ou excluir está disponível); acesso total às atribuições de portfólio e restrição<!-- Is that the correct wording? -->

  Esse nível de acesso é preferido para usuários que ainda estão aprendendo a usar o Search, Social e Commerce.

* **Otimização de Especialistas:** Este perfil fornece a seguinte funcionalidade:

   * Objetivos: acesso total

   * Simulações: acesso total

   * Grupos do Portfolio: acesso total

   * Portfólios: acesso total

   * Campanhas: acesso somente leitura à lista de campanhas (nenhum recurso de criação, edição ou exclusão de campanha está disponível ainda); acesso total a restrições e atribuições de portfólio<!-- Is that the correct wording? -->

   * Grupos de anúncios: acesso somente leitura à lista de grupos de anúncios (nenhum recurso de criação, edição ou exclusão de campanha está disponível ainda); acesso total a restrições e atribuições de portfólio<!-- Is that the correct wording? -->

  Esse nível de acesso é recomendado para usuários especialistas de Search, Social e Commerce.

* **Somente Leitura:** Este perfil fornece a seguinte funcionalidade:

   * Objetivos: acesso somente leitura

   * Simulações: acesso somente leitura

   * Grupos Portfolio: acesso somente leitura

   * Portfólios: acesso somente leitura

   * Campanhas: acesso somente leitura

   * Grupos de publicidade: acesso somente leitura

* **Administrador:** este perfil concede acesso total a todas as funcionalidades disponíveis e permite que os usuários criem novas instâncias do cliente. Não atribua esse direito a ninguém a menos que você tenha uma justificativa de negócios apropriada.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Tarefas para administradores

### Faça logon no Adobe Admin Console e abra-o no Search, Social e Commerce

>[!PREREQUISITES]
>
>É necessário ter acesso de administrador&lt;!- Que tipo? Administrador do produto, administrador do sistema, mas tenho certeza de que também é administrador do perfil do produto ou administrador do grupo de usuários (que pode ser um grupo interno — marque) —> para Pesquisar, Social e Commerce.

1. Acesse https://adminconsole.adobe.com/enterprise/.

1. (Se você não estiver conectado ao Experience Cloud) Faça logon no Experience Cloud:

   1. Insira sua ID do [!DNL Adobe] e clique em **[!UICONTROL Continue]**.

   1. Selecione **[!UICONTROL Personal Account]&quot; ou &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Selecione a organização da Experience Cloud aplicável.

   1. Em Produtos e Serviços, clique em &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

   A página do produto é aberta por padrão na guia [!UICONTROL Product profiles] para Search, Social e Commerce. As guias adicionais incluem [!UICONTROL Users] e [!UICONTROL Product Admins].

### Fluxo de trabalho para administradores do sistema

1. [Entre no Adobe Admin Console e abra-o no Search, Social e Commerce](#open-admin-console).

1. Delegar gerenciamento de produtos e usuários [adicionando administradores de produtos](https://helpx.adobe.com/br/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Fluxo de trabalho para administradores de produtos

1. [Entre no Adobe Admin Console e abra-o no Search, Social e Commerce](#open-admin-console).

1. Conforme necessário, crie usuários finais [individualmente](https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html) ou [em massa](https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html).

1. (Opcional) Crie [grupos de usuários](https://helpx.adobe.com/br/enterprise/using/user-groups.html) para cada instância de produto e atribua usuários a cada grupo de usuários.

   Se a instância tiver muitos usuários, crie grupos de usuários para garantir que os usuários recebam os perfis certos com base em seu nível de conhecimento. (Consulte a Etapa 4 para atribuir grupos de usuários a perfis de produtos.) Você pode criar grupos de usuários com base na linha de negócios, nas necessidades de acesso do usuário, na data de admissão do usuário ou em outros critérios.

   >[!IMPORTANT]
   >
   >Os nomes dos grupos de usuários devem comunicar claramente os direitos que o grupo de usuários deve receber. Por exemplo, se você deseja criar um grupo de usuários com direitos &quot;Somente leitura&quot;, inclua &quot;Somente leitura&quot; no nome do grupo de usuários, como &quot;Acme_Uk_ReadOnly&quot; ou &quot;Acme_ReadOnly&quot;.

1. (Opcional) [Criar perfis de produto personalizados](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html) com conjuntos de permissões definidos.

   Os perfis personalizados estão além dos quatro perfis de produto padrão que já estão disponíveis.

   Cada perfil de produto de uma organização deve ter um nome exclusivo. Se sua organização usar várias instâncias de Pesquisa, Social e Commerce (por exemplo, Acme_US e Acme_JP), você não poderá duplicar um nome de perfil de produto em várias instâncias. **Prática recomendada:** Usar a convenção de nomenclatura &quot;&lt;Name>_&lt;Instance>,&quot; como &quot;Simulations_Only_JP&quot;.

1. [Atribua manualmente ou em massa cada usuário ou grupo de usuários ao perfil de produto relevante](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html).

## Guia completo de administração de usuários e links adicionais

* Para obter mais informações sobre a administração de usuários usando o Adobe Admin Console, consulte o &quot;[Guia de Administração do Adobe Enterprise &amp; Teams](https://helpx.adobe.com/br/enterprise/admin-guide.html)&quot;, incluindo a [visão geral do Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
