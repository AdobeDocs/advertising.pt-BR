---
title: Sobre grupos de produtos de compras
description: Saiba mais sobre grupos de produtos de compras em campanhas de compras.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Sobre grupos de produtos de compras

*[!DNL Google Ads]e [!DNL Microsoft Advertising] campanhas de compras somente*

Nas campanhas de compras, os grupos de produtos (e não as palavras-chave) determinam os produtos na conta da central de compras para os quais os anúncios de compras são exibidos. Cada grupo de produtos é baseado em um único atributo de produto (como categoria, tipo de produto, marca, condição, ID de produto ou rótulos personalizados) e usa a mesma oferta para todos os produtos correspondentes. É possível incluir ou excluir ofertas para os produtos em cada grupo.

Os grupos de produtos são configurados no nível do grupo de anúncios para determinar quais produtos nas contas do centro de comércio aparecem nos anúncios de compras do grupo de anúncios. Mesmo que o grupo de publicidade não inclua entidades de publicidade, a rede de publicidade ainda exibirá anúncios dos produtos.

Quando o mesmo produto é incluído em mais de uma campanha, a rede de publicidade usa primeiro a prioridade de campanha para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada.

Para obter mais informações sobre [!DNL Google] campanhas de compras e anúncios, consulte &quot;[Implementar [!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; e a [documentação do Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Para obter mais informações sobre [!DNL Microsoft] campanhas de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; e a [[!DNL Microsoft Advertising] documentação](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Não há suporte disponível para [!DNL Google Ads] grupos de listagem em campanhas de desempenho máximo, que estão substituindo campanhas de compras inteligentes. Para gerenciar e exibir dados de grupos de listagem, use o editor [!DNL Google Ads].

## Hierarquia de grupo de produtos

Antes de criar grupos de produtos com atributos específicos para um grupo de anúncios, você deve primeiro criar um grupo de produtos com tudo incluído chamado &quot;[!UICONTROL All Products]&quot;. A partir desse grupo de produtos principal, você pode criar grupos de produtos secundários para subconjuntos de produtos e criar netos a partir dos grupos de produtos secundários. Depois de criar o primeiro grupo de produtos filho para um grupo de anúncios, outro grupo de produtos chamado &quot;[!UICONTROL Everything Else]&quot; será criado automaticamente usando a oferta padrão de grupo de anúncios. À medida que você adiciona mais grupos de produtos, o grupo &quot;[!UICONTROL Everything Else]&quot; é ajustado de acordo para constituir todos os produtos que não estão em outro grupo de produtos.

Em um grupo de anúncios, é possível criar até sete níveis de grupos de produtos (sem incluir &quot;[!UICONTROL All Products]&quot;) para incluir ou excluir de ofertas, com um ou mais grupos de produtos direcionados ao mesmo atributo em cada nível (por exemplo, [!UICONTROL Brand]=Acme para um grupo de produtos e [!UICONTROL Brand]=AcmePlus para outro no mesmo nível). Os grupos de produtos principais são chamados de subdivisões, e o nível mais baixo de subdivisão é conhecido como uma unidade. Você pode definir lances e modelos de rastreamento ou excluir completamente lances no nível da unidade. O conjunto inteiro de grupos de produtos ativos de um grupo de publicidade é aplicado hierarquicamente para determinar os produtos elegíveis. Por exemplo, se você subdividir o [!UICONTROL All Products] em [!UICONTROL Brand]=AcmeBasic e [!UICONTROL Brand]=AcmePlus e subdividir cada um desses grupos de produtos em [!UICONTROL Condition]=Novos e definir ofertas, apenas os novos produtos com as marcas AcmeBasic e AcmePlus poderão ser anunciados ou excluídos dos anúncios.

![Exemplo de um conjunto de grupos de produtos](/help/search-social-commerce/assets/product-group-list.png "Exemplo de um conjunto de grupos de produtos")

![Exemplo de hierarquia de grupo de produtos](/help/search-social-commerce/assets/product-group-tree.png "Exemplo de hierarquia de grupo de produtos")

## A visualização [!UICONTROL Product Groups]

Você pode criar e editar grupos de produtos, além de excluir grupos de produtos e seus grupos de produtos filhos, na exibição [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Dados de rastreamento e desempenho para grupos de produtos de compras

(Contas/campanhas com a opção de rastreamento &quot;[!UICONTROL EF Redirect]&quot;) Para permitir que o Search, Social e Commerce rastreiem conversões de grupos de produtos, [gere URLs de rastreamento para grupos de produtos usando a ferramenta URLs de Rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md) e siga um destes procedimentos:

* (Obrigatório para [!DNL Google Ads]; prática recomendada para [!DNL Microsoft Advertising]) Adicione a URL de rastreamento ao campo [!DNL Tracking Template] na configuração de conta, campanha ou grupo de produtos. Para facilitar a manutenção, adicione-os no mais alto nível possível. Nenhum parâmetro de acréscimo especificado para a conta ou campanha foi incluído.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Use esta opção somente quando não incluir URLs de rastreamento de Pesquisa, Social e Commerce em uma coluna personalizada no feed do produto. Se você fizer ambos, os URLs incluirão dois redirecionamentos e causarão links com falha.

* ([!DNL Microsoft Advertising] somente) Adicione a URL de rastreamento aos dados do produto dentro da conta [!DNL Microsoft Merchant Center]. Para fazer isso, inclua a URL de rastreamento, juntamente com o valor no campo `link` ou `mobile_link`, conforme apropriado, em uma coluna personalizada chamada [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) no feed do produto. Os URLs gerados usando esse método não incluem nenhum parâmetro de rastreamento especificado nas configurações de conta ou campanha em Search, Social e Commerce.

Você pode exibir dados sobre grupos de produtos em [o [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Gerenciar grupos de produtos de compras](product-group-manage.md)
>* [[!DNL Google Ads] configurações do grupo de produtos](product-group-settings-google.md)
>* [Implementar [!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] configurações do grupo de produtos](product-group-settings-microsoft.md)
>* [Implementar [!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
