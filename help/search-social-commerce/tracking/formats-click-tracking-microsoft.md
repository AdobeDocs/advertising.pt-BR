---
title: Formatos de rastreamento de cliques para [!DNL Microsoft Advertising]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Microsoft Advertising] contas.
exl-id: 725981db-1b9a-4c89-b95d-98d07ec99756
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para [!DNL Microsoft Advertising]

A seguir estão os formatos de modelo base de rastreamento e sufixo de página de aterrissagem (sufixo de URL final) exigidos pelo Search, Social e Commerce para [!DNL Microsoft Advertising].

## Formatos de modelo de rastreamento

### Redes de pesquisa e público-alvo (exceto sitelinks)

O formato a seguir se aplica a todos os tipos de anúncios rastreáveis em redes de pesquisa e público-alvo.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* `{TargetId}` representa a ID de a) a palavra-chave ou b) a palavra-chave e a lista de remarketing (público-alvo) que acionou o anúncio (por exemplo, &quot;kwd-123:aud-456&quot; para uma palavra-chave e uma lista de remarketing ou &quot;kwd-123&quot; para uma palavra-chave somente).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* `{TargetId}` representa a ID de a) a palavra-chave ou b) a palavra-chave e a lista de remarketing (público-alvo) que acionou o anúncio (por exemplo, &quot;kwd-123:aud-456&quot; para uma palavra-chave e uma lista de remarketing ou &quot;kwd-123&quot; para uma palavra-chave somente).
>
>* `{adextensionid}` não é usado.
>
>* (Sitelinks) Você pode ver quais conversões resultaram de um clique em um sitelink gerando um [!UICONTROL Transaction Report]. A variável [!UICONTROL Link Type] o valor da coluna para um sitelink é `sl:<Sitelink text>`, como `sl:See Current Offers`.

### Rede de compras

Os formatos a seguir se aplicam a anúncios de compras em redes de compras. Você pode especificar um modelo de rastreamento no nível de conta, campanha, grupo de anúncios ou grupo de produtos.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemplo:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* `{TargetId}` representa a ID de a) a palavra-chave ou b) a palavra-chave e a lista de remarketing (público-alvo) que acionou o anúncio (por exemplo, &quot;kwd-123:aud-456&quot; para uma palavra-chave e uma lista de remarketing ou &quot;kwd-123&quot; para uma palavra-chave somente).
>
>* (Opcional) Em vez de inserir modelos de rastreamento no nível da conta, campanha, grupo de anúncios ou grupo de produtos, você pode adicionar o URL de rastreamento aos dados do produto no [!DNL Microsoft Merchant Center] conta. Para fazer isso, inclua o URL de rastreamento junto com o valor no &quot;`link`&quot; ou &quot;`mobile_link`&quot;campo, conforme apropriado, em uma coluna personalizada&quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; no feed do produto. O valor no campo &quot;`bingads_redirect`O campo &quot; substituirá os valores na &quot;`link`&quot; e &quot;`mobile_link`&quot;. Os URLs gerados usando esse método não incluem nenhum parâmetro de rastreamento especificado nas configurações de campanha ou conta de Pesquisa, Social e Comércio.

## Formatos de sufixo de página de aterrissagem (sufixo de URL final)

>[!NOTE]
>
>Os sufixos de página de aterrissagem em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.

### Redes de pesquisa e público

As contas que usam o rastreamento de conversão de Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]) no sufixo:

* Quando o anunciante tiver uma integração do Adobe Analytics, o sufixo deverá incluir o seguinte:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Quando o anunciante não tiver uma integração do Adobe Analytics, o sufixo deve incluir o seguinte:

  `&ev_efid={msclkid}:G:s`

### Rede de compras

As contas que usam o rastreamento de conversão de Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]) no sufixo:

* Quando o anunciante tiver uma integração do Adobe Analytics, o sufixo deverá incluir o seguinte:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Quando o anunciante não tiver uma integração do Adobe Analytics, o sufixo deve incluir o seguinte:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para o código de rastreamento s\_kwcid](skwcid-tracking-parameter.md)
