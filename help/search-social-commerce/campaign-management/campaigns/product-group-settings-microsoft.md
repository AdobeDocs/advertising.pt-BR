---
title: Configurações do grupo de produtos [!DNL Microsoft Advertising]
description: Referencie as configurações de  [!DNL Microsoft Advertising] grupos de produtos de compras.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Configurações do grupo de produtos [!DNL Microsoft Advertising]

## Grupos de produtos &quot;Todos os produtos&quot;

**[!UICONTROL Condition]:** (Somente leitura) Todos os Produtos

**[!UICONTROL Bid]:** (Somente grupos de produtos incluídos) O custo máximo por clique (CPC), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários.

## Todos os outros grupos de produtos

**[!UICONTROL Condition/Value]:** (Somente leitura para grupos de produtos existentes) As dimensões de produto a serem direcionadas. Para novos grupos de produtos, insira a dimensão pela qual direcionar produtos e o atributo de qualificação para a categoria de informações selecionada (como &quot;Acme&quot; quando você está direcionando por marca ou &quot;New&quot; quando você está direcionando por condição).

Depois de criar um grupo de produtos para dimensões de produto específicas (ou seja, não &quot;Todos os produtos&quot;), o Search, Social e Commerce cria automaticamente um grupo de produtos para &quot;Tudo mais&quot;.

Para obter uma lista de dimensões de produto disponíveis, consulte &quot;[Filtros de produto da campanha de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;. Sua lista de dimensões pode ser limitada com base na configuração [!UICONTROL Inventory Filter] da campanha.

**[!UICONTROL Excluded]:** (Opcional para novos grupos de produtos; somente leitura para grupos de produtos existentes) Exclui ofertas em anúncios para produtos correspondentes.

**[!UICONTROL Bid]:** (Somente grupos de produtos incluídos) O custo máximo por clique (CPC), que é a maior quantia a ser paga por um clique em anúncio. Esse valor é usado somente para unidades sem grupos de produtos secundários e é usado no lugar do valor de nível de grupo de anúncios.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Este modelo substitui modelos em níveis superiores e é usado apenas para unidades sem grupos de produtos secundários.

>[!MORELIKETHIS]
>
>* [Sobre grupos de produtos de compras](product-group-about.md)
>* [Gerenciar grupos de produtos de compras](product-group-manage.md)
>* [Filtros de produto da campanha de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementar [!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
