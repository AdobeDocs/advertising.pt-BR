---
title: Configurações do grupo de anúncios '[!DNL Google Ads]'
description: Referencie as configurações de  [!DNL Google Ads] grupos de anúncios.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# Configurações do grupo de anúncios [!DNL Google Ads]

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Um nome de grupo de anúncios exclusivo na campanha. O tamanho máximo é de 255 caracteres de byte duplo.

**[!UICONTROL Status]:** O status de exibição do grupo de anúncios: *Ativo* ou *Pausado*. O padrão para novos grupos de anúncios é *Ativo*.

**[!UICONTROL Ad Group Type]:** (Somente campanhas de anúncios de pesquisa dinâmica expandidas) O tipo de grupo de anúncios:

* *[!UICONTROL Search Standard]* (o padrão): Para anúncios padrão.

* *[!UICONTROL Search Dynamic]:* Para anúncios de pesquisa dinâmica.

**[!UICONTROL Ad Rotation Mode]:** Com que frequência o [!DNL Google Ads] fornece seus anúncios ativos em relação uns aos outros no grupo de publicidade:

* *[!UICONTROL Optimize]:* O Google Ads favorece anúncios com desempenho melhor do que outros anúncios no grupo de anúncios. Esses anúncios entram no leilão com mais frequência e, com o tempo, um único anúncio é favorecido. Isso pode ser inconsistente com seus objetivos de negócios e otimização.

* *[!UICONTROL Rotate forever]:*   Cada um de seus anúncios entra no leilão de anúncios um número mais uniforme de vezes, o que permite que o Search, Social e Commerce marquem seus anúncios não apenas na taxa de click-through, mas também em conversões.

* *[!UICONTROL Use campaign setting]*(o padrão para novos grupos de anúncios): usa a configuração existente de rotação de anúncios no nível da campanha. **Observação:** a configuração de nível de campanha não está visível no Search, Social e Commerce.

Se a campanha usar uma estratégia de oferta de Oferta Inteligente (como [!UICONTROL Target CPA], [!UICONTROL Target ROAS] ou [!UICONTROL Enhanced CPC]), [!DNL Google Ads] definirá automaticamente a opção como &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Campanhas que direcionam apenas a rede de exibição) Como licitar: por *[!UICONTROL Ad Group]* (padrão), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interesses e Remarketing em Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (site), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Ao fazer uma oferta por palavra-chave, crie modelos de rastreamento no nível da palavra-chave. Da mesma forma, ao fazer uma oferta por posicionamento, crie modelos de rastreamento no nível de posicionamento. Para todas as outras dimensões, crie modelos de rastreamento no nível do anúncio.
>* Quando você faz lances por Idade, Gênero, Interesse e Lista ou Vertical para campanhas em portfólios, o recurso de otimização não otimiza lances para a dimensão. Além disso, todas as atribuições são aplicadas ao grupo de anúncios.
>* Anúncios na rede de pesquisa sempre usam ofertas de palavra-chave.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campanhas com [!UICONTROL Target CPA] lance; opcional) o custo alvo por aquisição (CPA) para o grupo de anúncios. Esse valor substitui o target no nível da campanha.

**[!UICONTROL Target ROAS]:** (Campanhas com [!UICONTROL Target ROAS] lance; opcional) o ROAS (retorno sobre o investimento) desejado para o grupo de publicidade, como uma porcentagem. Esse valor substitui o target no nível da campanha.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campanhas somente na rede de pesquisa e campanhas [!DNL Gmail] existentes somente leitura na rede de exibição) Se:

* *[!UICONTROL Target and Bid]:* Para mostrar anúncios somente para usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios. Você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, no entanto, definindo lances mais altos para esses públicos-alvo.

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
