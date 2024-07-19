---
title: Implementar [!DNL Microsoft Advertising] campanhas de compras
description: Saiba mais sobre o fluxo de trabalho para configurar  [!DNL Microsoft Advertising] campanhas de compras.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementar campanhas de compras de [!DNL Microsoft Advertising]

Os anúncios em campanhas de compras usam dados sobre produtos no feed de produto existente do [!DNL Microsoft Merchant Center], em vez de palavras-chave, para decidir como e onde mostrar seus anúncios.

[!DNL Microsoft] campanhas de compras têm como alvo o [!DNL Microsoft Advertising Shopping Network]. As configurações das campanhas de compras incluem um país especificado no qual os produtos são vendidos e uma prioridade ([!DNL High], [!DNL Medium] ou [!DNL Low]). Opcionalmente, você pode filtrar seu inventário para anunciar produtos com atributos específicos e direcionar ou excluir locais e tipos de dispositivos específicos.

Você pode controlar quais produtos são mostrados com seus anúncios de compras configurando *[grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* de vários níveis no nível do grupo de anúncios. Os grupos de produtos são baseados em quaisquer atributos de produto (categoria, tipo de produto, marca, condição, ID de produto e rótulos personalizados), e você pode criar até sete níveis de grupos de produtos para incluir ou excluir de lances, sem incluir &quot;[!DNL Add Products]&quot;. Você pode definir ofertas no nível mais baixo de grupos de produtos, usando a mesma oferta para todos os produtos correspondentes. Quando o mesmo produto é incluído em mais de uma campanha, o [!DNL Microsoft Advertising] usa a prioridade de nível de campanha primeiro para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

## Etapas para configurar campanhas de compras do [!DNL Microsoft Advertising]

Você pode configurar campanhas de compras usando [modelos de feed de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Microsoft Advertising], usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individualmente. As instruções a seguir incluem links para a criação de entidades individuais.

1. Configure sua conta do [!DNL Microsoft Merchant Center] e preencha-a com dados do produto.

1. [Permitir que o Search, Social e Commerce baixem dados da [!DNL Microsoft Merchant Center] conta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crie uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) na rede de compras.

1. [Crie um grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) na campanha e defina a oferta padrão para todos os anúncios.

   Você pode substituir a oferta padrão para grupos de produtos individuais.

1. Criar grupos de produtos para o grupo de publicidade:

   1. [Crie um grupo de produtos &quot;Todos os Produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Criar grupos de produtos derivados](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Crie [anúncios de produtos](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) com [linhas promocionais para incluir potencialmente em cada anúncio de compras](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) no grupo de anúncios.

      O Microsoft Advertising gera dinamicamente a cópia do anúncio e o URL da página de aterrissagem para cada anúncio.

      >[!NOTE]
      >
      >Mesmo que o grupo de anúncios não inclua entidades de anúncio, [!DNL Microsoft Advertising] ainda exibirá anúncios para os produtos.

1. (Opcional) Para rastrear cliques no anúncio, [gere uma URL de rastreamento usando a ferramenta de URLs de rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md). A prática recomendada é adicionar a URL de rastreamento ao campo [!UICONTROL Tracking Template] nas configurações de conta, campanha ou grupo de produtos. Para facilitar a manutenção, adicione-a no mais alto nível possível.

   Como alternativa, você pode adicionar a URL de rastreamento aos dados do produto na conta [!DNL Microsoft Merchant Center]. Para fazer isso, inclua a URL de rastreamento junto com o valor no campo &quot;link&quot; ou &quot;mobile_link&quot;, conforme apropriado, em uma coluna personalizada &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; no feed do produto. O valor no campo &quot;bingads_redirect&quot; substitui os valores nos campos &quot;link&quot; e &quot;mobile_link&quot;. Os URLs gerados usando esse método não incluem nenhum parâmetro de rastreamento especificado nas configurações de pesquisa, social e conta da Commerce ou da campanha.

1. Monitore o desempenho [gerando o [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Conforme necessário:

   1. [Edite as configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar o orçamento da campanha.

      Se a campanha fizer parte de um portfólio, a configuração de portfólio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permitirá que o Search, Social e Commerce otimize os orçamentos para todas as campanhas no portfólio.

   1. Ajuste o lance máximo para grupos de produtos existentes, exclua grupos de produtos para os quais não deseja mais criar anúncios ou adicione um novo grupo de produtos &quot;todos os produtos&quot; ou novos grupos de produtos secundários para criar anúncios para produtos adicionais.

>[!NOTE]
>
>* Consulte os campos obrigatórios para gerenciar campanhas e grupos de produtos do [!DNL Microsoft Shopping] usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) e [modelos de feed de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Para obter mais informações sobre [!DNL Microsoft Shopping] campanhas, consulte a [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/50903).
