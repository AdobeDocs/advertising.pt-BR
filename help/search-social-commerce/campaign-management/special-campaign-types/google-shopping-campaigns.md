---
title: Implementar [!DNL Google Ads] campanhas de compras
description: Saiba mais sobre o fluxo de trabalho para configuração [!DNL Google Ads] campanhas de compras.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] campanhas de compras

Anúncios em campanhas de compras usam dados sobre produtos em suas campanhas existentes [!DNL Google Merchant Center] feed do produto, em vez de palavras-chave, para decidir como e onde mostrar seus anúncios.

[!DNL Google Ads] as campanhas podem direcionar o [!DNL Google Shopping Network] usando o [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; As configurações para [!DNL Google Shopping] As campanhas incluem uma prioridade ([!UICONTROL High], [!UICONTROL Medium]ou [!UICONTROL Low]). Como opção, você pode mostrar as informações do inventário local nos anúncios de compra usando uma configuração de nível de campanha.

Você pode controlar quais produtos são mostrados com seus anúncios de compras configurando níveis múltiplos *[grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* no nível do grupo de publicidade. Os grupos de produtos são baseados em quaisquer atributos de produto (categoria, tipo de produto, marca, condição, ID de produto e rótulos personalizados) e você pode criar até sete níveis de grupos de produtos para incluir ou excluir dos lances. Você pode definir ofertas no nível mais baixo de grupos de produtos, usando a mesma oferta para todos os produtos correspondentes. Quando o mesmo produto estiver incluído em mais de uma campanha, [!DNL Google Ads] usa a prioridade no nível da campanha primeiro para determinar qual campanha (e lances associados) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

## Etapas para configurar [!DNL Google Ads] campanhas de compras

Você pode configurar campanhas de compras usando [modelos de feed de estoque](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Google Shopping], usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)ou individualmente. As instruções a seguir incluem links para a criação de entidades individuais.

1. Configure seu [!DNL Google Merchant Center] conta e preencha-a com dados do produto.

1. [Permitir que o Search, Social e Commerce baixem dados da [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Criar uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) na rede de compras.

1. [Criar um grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) na campanha e defina a oferta padrão para todos os anúncios.

Você pode substituir a oferta padrão para grupos de produtos individuais.

1. Criar grupos de produtos para o grupo de publicidade:

   1. [Criar um grupo de produtos &quot;Todos os produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Criar grupos de produtos secundários](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).
   >[!NOTE]
   >Você não precisa criar anúncios de compras. Mesmo que o grupo de anúncios não inclua entidades de anúncio, [!DNL Google Ads] O ainda exibe anúncios para os produtos.

1. (Opcional) Para rastrear cliques no anúncio, [gerar um URL de rastreamento usando a ferramenta URLs de rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md)e, em seguida, adicione-o às configurações de conta, campanha ou grupo de produtos.

1. Monitorar o desempenho por [gerando o [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) e [o [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Conforme necessário:

   1. [Editar as configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar o orçamento da campanha.

      Se a campanha fizer parte de um portfólio, a configuração do portfólio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permite que o Search, Social e Commerce otimizem os orçamentos para todas as campanhas no portfólio.

   1. [Ajustar o lance máximo para grupos de produtos existentes](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [excluir grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para o qual você não deseja mais criar anúncios ou adicionar um [novo grupo de produtos &quot;todos os produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)ou [novos grupos de produtos secundários](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) para criar anúncios para produtos adicionais.

>[!NOTE]
>
>* Consulte os campos obrigatórios para gerenciar [!DNL Google Shopping] campanhas e grupos de produtos usando o [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) e [modelos de feed de estoque](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Para obter mais informações sobre [!DNL Google Shopping] campanhas, consulte o [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/2454022).

