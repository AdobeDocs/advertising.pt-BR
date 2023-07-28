---
title: '[!DNL Google Ads] configurações do grupo de publicidade'
description: Referenciar as configurações de [!DNL Google Ads] grupos de publicidade.
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] configurações do grupo de publicidade

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Um nome de grupo de anúncios exclusivo na campanha. O tamanho máximo é de 255 caracteres de byte duplo.

**[!UICONTROL Status]:** O status de exibição do grupo de anúncios: *Ativo* ou *Pausado*. O padrão para novos grupos de anúncios é *Ativo*.

**[!UICONTROL Ad Group Type]:** (Somente campanhas de publicidade de pesquisa dinâmica expandidas) O tipo de grupo de anúncios:

* *[!UICONTROL Search Standard]* (o padrão): Para anúncios padrão.

* *[!UICONTROL Search Dynamic]:* Para anúncios de pesquisa dinâmica.

**[!UICONTROL Ad Rotation Mode]:** Com que frequência [!DNL Google Ads] O entrega seus anúncios ativos em relação uns aos outros no grupo de publicidade:

* *[!UICONTROL Optimize]:* O Google Ads favorece anúncios com desempenho melhor do que outros anúncios no grupo de anúncios. Esses anúncios entram no leilão com mais frequência e, com o tempo, um único anúncio é favorecido. Isso pode ser inconsistente com seus objetivos de negócios e otimização.

* *[!UICONTROL Rotate forever]:*   Cada um de seus anúncios entra no leilão de anúncios um número mais uniforme de vezes, o que permite que a Search, Social e &amp; Commerce marquem seus anúncios não apenas na taxa de click-through, mas também em conversões.

* *[!UICONTROL Use campaign setting]*(o padrão para novos grupos de anúncios): usa a configuração existente de rotação de anúncios no nível da campanha. **Nota:** A configuração no nível da campanha não está visível no Search, Social e Commerce.

Se a campanha usar uma estratégia de oferta inteligente (como [!UICONTROL Target CPA], [!UICONTROL Target ROAS]ou [!UICONTROL Enhanced CPC]), depois [!DNL Google Ads] define automaticamente a opção como &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Campanhas direcionadas somente à rede de exibição) Como oferecer: por *[!UICONTROL Ad Group]* (o padrão), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interesses e remarketing no Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (sítio Web), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Ao fazer uma oferta por palavra-chave, crie modelos de rastreamento no nível da palavra-chave. Da mesma forma, ao fazer uma oferta por posicionamento, crie modelos de rastreamento no nível de posicionamento. Para todas as outras dimensões, crie modelos de rastreamento no nível do anúncio.
>* Quando você faz lances por Idade, Gênero, Interesse e Lista ou Vertical para campanhas em portfólios, o recurso de otimização não otimiza lances para a dimensão. Além disso, todas as atribuições são aplicadas ao grupo de anúncios.
>* Anúncios na rede de pesquisa sempre usam ofertas de palavra-chave.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campanhas com [!UICONTROL Target CPA] lance; opcional) o custo alvo por aquisição (CPA) para o grupo de anúncios. Esse valor substitui o target no nível da campanha.

**[!UICONTROL Target ROAS]:** (Campanhas com [!UICONTROL Target ROAS] lance; opcional) a meta de ROAS (Return on Ad Gaste, retorno sobre o investimento em anúncios) para o grupo de anúncios, como uma porcentagem. Esse valor substitui o target no nível da campanha.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campanhas somente na rede de pesquisa e campanhas existentes, somente leitura [!DNL Gmail] campanhas na rede de exibição) Se deseja:

* *[!UICONTROL Target and Bid]:* Para mostrar anúncios somente a usuários associados a públicos-alvo que também satisfaçam a quaisquer outros alvos para o grupo de anúncios.

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo a pessoas que não estão associadas a públicos-alvo, desde que atendam a outros alvos de nível de grupo de anúncios. Você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, no entanto, definindo lances mais altos para esses públicos-alvo.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar grupos de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
