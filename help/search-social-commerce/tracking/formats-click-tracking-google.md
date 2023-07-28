---
title: Formatos de rastreamento de cliques para [!DNL Google Ads]
description: Saiba mais sobre os formatos de rastreamento de cliques do [!DNL Google Ads] contas.
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para [!DNL Google Ads]

A seguir estão os formatos de modelo base de rastreamento e sufixo de página de aterrissagem (sufixo de URL final) exigidos pelo Search, Social e Commerce para [!DNL Google Ads].

## Formatos de modelo de rastreamento

### Rede de pesquisa/exibição, incluindo sitelinks

O formato a seguir se aplica a todos os tipos de anúncios rastreáveis em redes de pesquisa e exibição e para sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* A variável [!DNL ValueTrack] parâmetros para indicar URLs finais em modelos de rastreamento devem ser `{lpurl}` ou `!{unescapedurl}`.
>
>* (Anúncios de texto) Quando você faz uma oferta por palavra-chave, o parâmetro `ev_pl` (para inserções) não tem valor. Quando você faz ofertas por posicionamento, `ev_ln` (para palavras-chave) não tem valor. Quando você faz uma oferta por grupo de anúncios ou por qualquer outra dimensão, ambos `ev_ln` e `ev_pl` não têm valores.
>
>* (Anúncios de pesquisa dinâmica) `{keyword}` indica a expressão de destino da pesquisa dinâmica, como `_cat:[VALUE]` ou `_url:[VALUE]`.
>
>* (Anúncios de pesquisa dinâmica) [!DNL Google Ads] determina o URL final dinamicamente, de modo que não é necessário inserir um.
>
>* (Sitelinks) Você pode ver quais conversões resultaram de um clique em um sitelink gerando um [!UICONTROL Transaction Report]. A variável [!UICONTROL Link Type] o valor da coluna para um sitelink é `sl:<Sitelink text>`, como `sl:See Current Offers`.

### Rede de compras

O formato a seguir se aplica a anúncios de compras e grupos de produtos em redes de compras. Você pode especificar um modelo de rastreamento no nível de conta, campanha, grupo de anúncios ou grupo de produtos.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável do identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a transmissão de token estiver desativada, substitua `cq?` após `<advertiser_ID>` com `c?`.
>
>* A variável [!DNL ValueTrack] parâmetros para indicar URLs finais em modelos de rastreamento devem ser `{lpurl}` ou `!{unescapedurl}`.
>
>* [!DNL Google Ads] O usa URLs de produtos no feed do Google Merchant Center como os URLs finais, de modo que você não precisa inserir URLs finais para os dados do produto ou grupos de produtos.
>
>* Você pode ver quais conversões resultaram de um clique em um anúncio de compras gerando um [!UICONTROL Transaction Report]. A variável [!UICONTROL Link Type] o valor da coluna para um anúncio de produto é pla:`<product ID>`, como `pla:8525822`.

## Formatos de sufixo de página de aterrissagem (sufixo de URL final)

As contas que usam o rastreamento de conversão de Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`gclid` para [!DNL Google Ads]) no sufixo:

* Quando o anunciante tiver uma integração do Adobe Analytics, o sufixo deverá incluir um dos seguintes:

   * [!DNL Google Ads] contas que usam a mais recente `s_kwcid` formato, que oferece suporte a relatórios no nível da campanha e do grupo de anúncios para campanhas de desempenho máximo e campanhas de rascunhos e experimentos:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Se a conta tiver uma implementação s_kwcid do lado do servidor e a configuração de conta ou campanha &quot;[!UICONTROL Auto Upload]&quot; estiver ativado, o parâmetro será adicionado automaticamente. Caso contrário, é necessário adicioná-lo manualmente.

   * Todos os outros [!DNL Google Ads] contas:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Quando o anunciante não tiver uma integração do Adobe Analytics, o sufixo deve incluir o seguinte:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Os sufixos de página de aterrissagem em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.
>
>* (Anúncios de pesquisa dinâmica; anunciantes com Adobe Analytics e sem rastreamento do lado do servidor) Quando desejar incluir o rastreamento do feed reverso do Adobe Advertising para o Analytics, anexe o `s_kwcid` código de rastreamento até o final do sufixo da página de aterrissagem no nível da conta.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos para o código de rastreamento s\_kwcid](skwcid-tracking-parameter.md)
