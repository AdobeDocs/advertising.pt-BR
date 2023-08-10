---
title: O parâmetro de rastreamento da ID do AMO (s_kwcid)
description: Saiba mais sobre o parâmetro de rastreamento usado para compartilhar dados do Adobe Advertising com o Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 47cb00bc456601ef943c37de14a2047220f756f1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# O parâmetro de rastreamento da ID do AMO (s_kwcid)

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

O Adobe Advertising compartilha dados sobre suas campanhas com a Adobe Analytics usando o parâmetro de acréscimo da ID do AMO, também chamado de `s_kwcid` que consiste em elementos específicos do canal de publicidade e da rede de publicidade.

<!-- add everything below to IDs page -->

O parâmetro é adicionado aos URLs de rastreamento de uma das seguintes maneiras:

* (Recomendado) O recurso de inserção do lado do servidor é implementado.

  Para [!DNL Google Ads] e [!DNL Microsoft Advertising] contas com o [!UICONTROL Auto Upload] configuração ativada para a conta ou campanha, o servidor de pixels anexa automaticamente o parâmetro da ID do AMO aos sufixos da página de aterrissagem quando um usuário final clica em um anúncio <!-- click a search ad or views a display ad --> com o pixel Adobe Advertising.

  Para outras redes de publicidade, ou [!DNL Google Ads] e [!DNL Microsoft Advertising] contas com o [!UICONTROL Auto Upload] configuração desativada, adicione manualmente o parâmetro da ID do AMO aos parâmetros de acréscimo no nível da conta, que o anexam aos URLs base.

* <!-- (Search, Social, & Commerce only) -->O recurso de inserção do lado do servidor não está implementado e você precisa adicionar manualmente o parâmetro da ID do AMO ao seu ([!DNL Google Ads] e [!DNL Microsoft Advertising]) sufixos de página de aterrissagem ou (outras redes de anúncios) parâmetros de acréscimo no nível da conta.

Para implementar o recurso de inserção do lado do servidor ou determinar a melhor opção para sua empresa, entre em contato com a equipe de conta da Adobe.

## Formato de ID AMO para anúncios DSP de publicidade

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

em que:

* `AC` indica o canal de exibição.

* `{TM_AD_ID}` é a chave alfanumérica do anúncio.

* `{TM_PLACEMENT_ID}` é a chave de posicionamento alfanumérico.

## Formatos de ID do AMO para anúncios de Pesquisa, Social e Comércio

Os parâmetros variam por rede de anúncios, mas os seguintes parâmetros são comuns a todos:

* `AL` indica o canal de pesquisa. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` é uma ID de usuário exclusiva atribuída ao anunciante.

* `{sid}` é substituído pela ID numérica da conta de rede de anúncios do anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto) ou *106* para [!DNL Pinterest] (obsoleto).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Isso inclui campanhas de compras usando o [!DNL Google Merchant Center].

* Contas que usam o formato de ID AMO mais recente, compatível com relatórios de nível de campanha e grupo de anúncios para campanhas de desempenho máximo e campanhas de rascunhos e experimentos:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Todas as outras contas:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Para anúncios de pesquisa dinâmica, {keyword} é preenchida com o direcionamento automático.
>* Ao gerar o rastreamento para [!DNL Google] anúncios de compras, um parâmetro de ID do produto, `{adwords_producttargetid}`, é inserido antes do parâmetro de palavra-chave. O parâmetro da ID do produto não aparece no [!DNL Google Ads] parâmetros de rastreamento no nível da conta e no nível da campanha.
>* Para usar o código de rastreamento de ID do AMO mais recente, consulte &quot;[Atualizar o código de rastreamento da ID do AMO para um [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Pesquisar campanhas:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campanhas de compras (usando [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campanhas de rede de público-alvo:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Gerenciar contas de rede de publicidade](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Configurações da campanha no Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Configurações da campanha do Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Configurações da campanha de publicidade do Microsoft](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Configurações da campanha de anúncios no Japão](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Configurações da campanha Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
