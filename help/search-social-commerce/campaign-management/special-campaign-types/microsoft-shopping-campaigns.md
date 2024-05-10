---
title: Implementar [!DNL Microsoft Advertising] campanhas de compras
description: Saiba mais sobre o fluxo de trabalho para configuração [!DNL Microsoft Advertising] campanhas de compras.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementar [!DNL Microsoft Advertising] campanhas de compras

Anúncios em campanhas de compras usam dados sobre produtos em suas campanhas existentes [!DNL Microsoft Merchant Center] feed do produto, em vez de palavras-chave, para decidir como e onde mostrar seus anúncios.

[!DNL Microsoft] campanhas de compras direcionadas para o [!DNL Microsoft Advertising Shopping Network]. As configurações para campanhas de compras incluem um país especificado no qual os produtos são vendidos e uma prioridade ([!DNL High], [!DNL Medium]ou [!DNL Low]). Opcionalmente, você pode filtrar seu inventário para anunciar produtos com atributos específicos e direcionar ou excluir locais e tipos de dispositivos específicos.

Você pode controlar quais produtos são mostrados com seus anúncios de compras configurando níveis múltiplos *[grupos de produtos](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* no nível do grupo de publicidade. Os grupos de produtos são baseados em quaisquer atributos de produto (categoria, tipo de produto, marca, condição, ID de produto e rótulos personalizados) e você pode criar até sete níveis de grupos de produtos para incluir ou excluir de lances, sem incluir &quot;[!DNL Add Products].&quot; Você pode definir ofertas no nível mais baixo de grupos de produtos, usando a mesma oferta para todos os produtos correspondentes. Quando o mesmo produto estiver incluído em mais de uma campanha, [!DNL Microsoft Advertising] usa a prioridade no nível da campanha primeiro para determinar qual campanha (e lances associados) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

## Etapas para configurar [!DNL Microsoft Advertising] campanhas de compras

Você pode configurar campanhas de compras usando [modelos de feed de estoque](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para [!DNL Microsoft Advertising], usando [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)ou individualmente. As instruções a seguir incluem links para a criação de entidades individuais.

1. Configure seu [!DNL Microsoft Merchant Center] conta e preencha-a com dados do produto.

1. [Permitir que o Search, Social e Commerce baixem dados do [!DNL Microsoft Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Criar uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) na rede de compras.

1. [Criar um grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) na campanha e defina a oferta padrão para todos os anúncios.

Você pode substituir a oferta padrão para grupos de produtos individuais.

1. Criar grupos de produtos para o grupo de publicidade:

   1. [Criar um grupo de produtos &quot;Todos os produtos&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Opcional) [Criar grupos de produtos secundários](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Criar [anúncios de produto](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) com [linhas de promoção a serem potencialmente incluídas em cada anúncio de compra](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) no grupo de publicidade.

      A Microsoft Advertising gera dinamicamente a cópia de anúncio e o URL da página de aterrissagem de cada anúncio.

      >[!NOTE]
      >
      >Mesmo que o grupo de anúncios não inclua entidades de anúncio, [!DNL Microsoft Advertising] O ainda exibe anúncios para os produtos.

1. (Opcional) Para rastrear cliques no anúncio, [gerar um URL de rastreamento usando a ferramenta URLs de rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md). A prática recomendada é adicionar o URL de rastreamento ao [!UICONTROL Tracking Template] nas configurações de conta, campanha ou grupo de produtos. Para facilitar a manutenção, adicione-a no mais alto nível possível.

   Como alternativa, você pode adicionar o URL de rastreamento aos dados do produto no [!DNL Microsoft Merchant Center] conta. Para fazer isso, inclua o URL de rastreamento, junto com o valor no campo &quot;link&quot; ou &quot;mobile_link&quot;, conforme apropriado, em uma coluna personalizada &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; no feed do produto. O valor no campo &quot;bingads_redirect&quot; substitui os valores nos campos &quot;link&quot; e &quot;mobile_link&quot;. Os URLs gerados usando esse método não incluem nenhum parâmetro de rastreamento especificado nas configurações de pesquisa, social e conta da Commerce ou da campanha.

1. Monitorar o desempenho por [gerando o [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Conforme necessário:

   1. [Editar as configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar o orçamento da campanha.

      Se a campanha fizer parte de um portfólio, a configuração do portfólio &quot;[!UICONTROL Auto adjust campaign budget limits]O &quot; permite que o Search, Social e Commerce otimizem os orçamentos para todas as campanhas no portfólio.

   1. Ajuste o lance máximo para grupos de produtos existentes, exclua grupos de produtos para os quais não deseja mais criar anúncios ou adicione um novo grupo de produtos &quot;todos os produtos&quot; ou novos grupos de produtos secundários para criar anúncios para produtos adicionais.

>[!NOTE]
>
>* Consulte os campos obrigatórios para gerenciar [!DNL Microsoft Shopping] campanhas e grupos de produtos usando o [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) e [modelos de feed de estoque](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Para obter mais informações sobre [!DNL Microsoft Shopping] campanhas, consulte o [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/50903).
