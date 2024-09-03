---
title: Implementar [!DNL Google Ads] campanhas de compras
description: Saiba mais sobre o fluxo de trabalho para configurar  [!DNL Google Ads] campanhas de compras.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementar campanhas de compras de [!DNL Google Ads]

Os anúncios em campanhas de compras usam dados sobre produtos no feed de produto existente do [!DNL Google Merchant Center], em vez de palavras-chave, para decidir como e onde mostrar seus anúncios.

[!DNL Google Ads] campanhas podem direcionar [!DNL Google Shopping Network] usando [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; As configurações das campanhas [!DNL Google Shopping] incluem uma prioridade ([!UICONTROL High], [!UICONTROL Medium] ou [!UICONTROL Low]). Como opção, você pode mostrar as informações do inventário local nos anúncios de compra usando uma configuração de nível de campanha.

Você pode controlar quais produtos são mostrados com seus anúncios de compras configurando *[grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* de vários níveis no nível do grupo de anúncios. Os grupos de produtos são baseados em quaisquer atributos de produto (categoria, tipo de produto, marca, condição, ID de produto e rótulos personalizados) e você pode criar até sete níveis de grupos de produtos para incluir ou excluir dos lances. Você pode definir ofertas no nível mais baixo de grupos de produtos, usando a mesma oferta para todos os produtos correspondentes. Quando o mesmo produto é incluído em mais de uma campanha, o [!DNL Google Ads] usa a prioridade de nível de campanha primeiro para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

## Etapas para configurar campanhas de compras do [!DNL Google Ads]

Você pode configurar campanhas de compras usando [modelos de feed de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Google Shopping], usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individualmente. As instruções a seguir incluem links para a criação de entidades individuais.

1. Configure sua conta do [!DNL Google Merchant Center] e preencha-a com dados do produto.

1. [Permitir que o Search, Social e Commerce baixem dados da [!DNL Google Merchant Center] conta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crie uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) na rede de compras.

1. [Crie um grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) na campanha e defina a oferta padrão para todos os anúncios.

   Você pode substituir a oferta padrão para grupos de produtos individuais.

1. Criar grupos de produtos para o grupo de publicidade:

   1. [Crie um grupo de produtos &quot;Todos os Produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Criar grupos de produtos derivados](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Você não precisa criar anúncios de compras. Mesmo que o grupo de anúncios não inclua entidades de anúncio, [!DNL Google Ads] ainda exibirá anúncios para os produtos.

1. (Opcional) Para rastrear cliques no anúncio, [gere uma URL de rastreamento usando a ferramenta de URLs de rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md) e depois adicione-a às configurações de conta, campanha ou grupo de produtos.

1. Monitore o desempenho [gerando o [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) e [o [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Conforme necessário:

   1. [Edite as configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar o orçamento da campanha.

      Se a campanha fizer parte de um portfólio, a configuração de portfólio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permitirá que o Search, Social e Commerce otimize os orçamentos para todas as campanhas no portfólio.

   1. [Ajuste a oferta máxima para grupos de produtos existentes](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [exclua grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para os quais não deseja mais criar anúncios, ou adicione um [novo grupo de produtos &quot;todos os produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) ou [novos grupos de produtos filhos](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para criar anúncios para produtos adicionais.

>[!NOTE]
>
>* Consulte os campos obrigatórios para gerenciar campanhas e grupos de produtos do [!DNL Google Shopping] usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) e [modelos de feed de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Para obter mais informações sobre [!DNL Google Shopping] campanhas, consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/2454022).
