---
title: Gerenciar modificadores
description: Saiba como configurar e gerenciar modificadores para seus modelos de anúncio para feeds de dados de inventário.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Gerenciar modificadores

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Modificadores são adjetivos ou advérbios que podem ser adicionados ou removidos de uma sentença sem alterar a estrutura básica da sentença. Você pode criar grupos de modificadores para usar como variáveis em vários campos de dados em modelos de dados de feed. Ao incluir modificadores nos campos de estrutura de conta (campanha e grupo de anúncios), palavras-chave, URLs de base e anúncios, você cria um valor para cada valor de modificador associado. Por exemplo, se você usar uma variável do grupo de modificadores em um título de anúncio e o grupo de modificadores incluir três modificadores (&quot;barato&quot;, &quot;desconto&quot; e &quot;acessível&quot;), três anúncios separados serão criados para cada linha de dados no feed de dados — um para cada modificador. Da mesma forma, se você incluir um grupo de modificadores com vários valores no URL base de um grupo de anúncios, um conjunto de palavras-chave será criado para cada um dos URLs base resultantes.

Cada grupo de modificadores pode incluir quantos modificadores desejar. Cada modelo pode usar apenas um grupo de modificadores.

## Criar um grupo de modificadores

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Modifiers]**.

1. Acima da lista de grupos de modificadores, clique em **[!UICONTROL Create]**.

1. Especifique as configurações do grupo de modificadores:

   **[!UICONTROL Name]:** O nome do grupo de modificadores.

   **[!UICONTROL Modifiers]:** Os valores do modificador para o grupo (um por linha).

1. Clique em **[!UICONTROL Save]**.

## Editar um Grupo de Modificadores

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Modifiers]**.

1. Na lista de grupos de modificadores, clique no nome do grupo de modificadores.

1. Edite as configurações do grupo de modificadores:

   **[!UICONTROL Name]:** O nome do grupo de modificadores.

   **[!UICONTROL Modifiers]:** Os valores do modificador para o grupo (um por linha).

1. Clique em **[!UICONTROL Save]**.

## Excluir Grupos de Modificadores

>[!IMPORTANT]
>
>Quando você deleta um grupo de modificadores, remove todas as variáveis desse grupo de modificadores (denotado como `<modifier_group_name>`) nos campos dos modelos existentes. Se você tentar propagar dados por meio de um modelo usando variáveis para modificadores que não existem, o job falhará1.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Modifiers]**.

1. Marque a caixa de seleção ao lado de cada grupo de modificadores que você deseja deletar.

1. Acima da lista de grupos de modificadores, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Yes]**.

1. (Se necessário) [Remover referências ao modificador](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) de todos os modelos aplicáveis.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Gerenciar modelos de anúncios](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)

