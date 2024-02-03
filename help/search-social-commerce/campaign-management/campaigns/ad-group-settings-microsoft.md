---
title: '[!DNL Microsoft Advertising] configurações do grupo de publicidade'
description: Referenciar as configurações de [!DNL Microsoft Advertising] grupos de publicidade.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: a31179383fa9c1c9f6eb697d0aa3dd3301d41823
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configurações do grupo de publicidade

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Um nome de grupo de anúncios exclusivo na campanha. O comprimento máximo é de 128 caracteres.

**[!UICONTROL Status]:** O status de exibição do grupo de anúncios: *Ativo* ou *Pausado*. O padrão para novos grupos de anúncios é *Ativo*.

**[!UICONTROL Ad Language]:** (Campanhas de pesquisa) O idioma de destino para anúncios.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Anúncios de pesquisa) Como e onde colocar anúncios no grupo de anúncios:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (o padrão): Para fazer ofertas de anúncios na rede de pesquisa.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Para fazer lances para anúncios em sites de parceiros sindicalizados.

* *[!UICONTROL Content network]:* Obsoleto

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsoleto

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Grupos de anúncios de público-alvo) Se deve:

* *[!UICONTROL Target and Bid]:* Para mostrar anúncios somente a usuários associados a públicos-alvo que também satisfaçam a quaisquer outros alvos para o grupo de anúncios.

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo a pessoas que não estão associadas a públicos-alvo, desde que atendam a outros alvos de nível de grupo de anúncios. Você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, no entanto, definindo lances mais altos para esses públicos-alvo.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Para [!DNL Microsoft Advertising] grupos de anúncios na rede de público-alvo, os modificadores de oferta para públicos-alvo de localização não são otimizados em portfólios padrão com o &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Grupos de anúncios de público-alvo; opcional) Gêneros específicos a serem incluídos ou excluídos como metas: *[!UICONTROL Male]*, *[!UICONTROL Female]*, e *[!UICONTROL Unknown]*. Por padrão, todos os gêneros são direcionados. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo ao lado dele uma vez para que uma marca azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) será exibida. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada gênero direcionado.

* Para excluir um valor, clique no círculo ao lado dele duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) será exibida.

**[!UICONTROL Age]:** (Grupos de anúncios de público-alvo; opcional) Categorias etárias específicas a serem incluídas ou excluídas como metas: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, e *[!UICONTROL Unknown]*. Por padrão, todas as idades são direcionadas. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo ao lado dele uma vez para que uma marca azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) será exibida. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada faixa etária de destino.

* Para excluir um valor, clique no círculo ao lado dele duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) será exibida.

**[!UICONTROL Industry]:** (Grupos de anúncios de público-alvo; opcional) Setores específicos a serem incluídos ou excluídos como metas. Por padrão, todos os setores são direcionados. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo ao lado dele uma vez para que uma marca azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) será exibida. Opcionalmente, você pode aumentar ou diminuir ofertas em uma porcentagem especificada para cada setor direcionado.

* Para excluir um valor, clique no círculo ao lado dele duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) será exibida.

**[!UICONTROL Job Function Targets]:** (Grupos de anúncios de público-alvo; opcional) Funções de trabalho específicas a serem incluídas ou excluídas como metas. Por padrão, todas as funções de trabalho são direcionadas. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo ao lado dele uma vez para que uma marca azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) será exibida. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada função da ordem de produção pretendida.

* Para excluir um valor, clique no círculo ao lado dele duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) será exibida.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Opcional) O número de vezes que um cliente receberá anúncios do grupo de anúncios. Insira um valor e selecione a unidade de tempo (*[!UICONTROL Hour]*, *[!UICONTROL Day]* ou *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campanhas somente na exibição/rede nativa; opcional) Sites na rede de exibição na qual você não deseja que seus anúncios sejam exibidos. Insira um URL válido, como www.example.com. Para especificar várias cadeias de caracteres, separe-as com vírgulas ou insira-as em linhas separadas.

Para obter informações sobre a disponibilidade, consulte a ajuda da Microsoft Advertising em &quot;[Impedir a exibição de anúncios em sites específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Gerenciar grupos de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
