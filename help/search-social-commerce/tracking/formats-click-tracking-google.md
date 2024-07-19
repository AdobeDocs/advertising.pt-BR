---
title: Formatos de rastreamento de cliques para  [!DNL Google Ads]
description: Saiba mais sobre os formatos de rastreamento de cliques para contas do  [!DNL Google Ads] .
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Formatos de rastreamento de cliques para [!DNL Google Ads]

A seguir estão os formatos de modelo base de rastreamento e sufixo de página de aterrissagem (sufixo de URL final) que o Search, Social e Commerce exige para [!DNL Google Ads].

## Formatos de modelo de rastreamento

### Rede de pesquisa/exibição, incluindo sitelinks

O formato a seguir se aplica a todos os tipos de anúncios rastreáveis em redes de pesquisa e exibição e para sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
>* Os parâmetros [!DNL ValueTrack] para indicar URLs finais em modelos de rastreamento devem ser `{lpurl}` ou `!{unescapedurl}`.
>
>* (Anúncios de texto) Quando você faz uma oferta por palavra-chave, o parâmetro `ev_pl` (para posicionamentos) não tem valor. Quando você faz uma oferta por posicionamento, `ev_ln` (para palavras-chave) não tem valor. Quando você faz uma oferta por grupo de publicidade ou por qualquer outra dimensão, `ev_ln` e `ev_pl` não têm valores.
>
>* (Anúncios de pesquisa dinâmica) `{keyword}` indica a expressão de destino de pesquisa dinâmica, como `_cat:[VALUE]` ou `_url:[VALUE]`.
>
>* (Anúncios de pesquisa dinâmica) [!DNL Google Ads] determina a URL final dinamicamente, portanto, você não precisa inserir uma.
>
>* (Sitelinks) Você pode ver quais conversões resultaram de um clique em um sitelink gerando um [!UICONTROL Transaction Report]. O valor da coluna [!UICONTROL Link Type] para um sitelink é `sl:<Sitelink text>`, como `sl:See Current Offers`.

### Rede de compras

O formato a seguir se aplica a anúncios de compras e grupos de produtos em redes de compras. Você pode especificar um modelo de rastreamento no nível de conta, campanha, grupo de anúncios ou grupo de produtos.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemplo:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` é uma variável para o identificador exclusivo do anunciante no Adobe Advertising.
>
>* Esse formato indica que a transmissão de token está habilitada para a campanha (o padrão). Se a passagem do token estiver desabilitada, substitua `cq?` após `<advertiser_ID>` por `c?`.
>
>* Os parâmetros [!DNL ValueTrack] para indicar URLs finais em modelos de rastreamento devem ser `{lpurl}` ou `!{unescapedurl}`.
>
>* O [!DNL Google Ads] usa URLs de produtos no feed do Google Merchant Center como as URLs finais, de modo que você não precisa inserir as URLs finais para seus dados de produtos ou grupos de produtos.
>
>* Você pode ver quais conversões resultaram de um clique em um anúncio de compras gerando um [!UICONTROL Transaction Report]. O valor da coluna [!UICONTROL Link Type] para um anúncio de produto é pla:`<product ID>`, como `pla:8525822`.

## Formatos de sufixo de página de aterrissagem (sufixo de URL final)

As contas que usam o rastreamento de conversão de Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`gclid` para [!DNL Google Ads]) no sufixo:

* Quando o anunciante tiver uma integração do Adobe Analytics, o sufixo deverá incluir um dos seguintes:

   * Contas do [!DNL Google Ads] que usam o [formato de ID do AMO](/help/integrations/analytics/ids.md#amo-id-formats) mais recente (começando com `s_kwcid`), que oferece suporte a relatórios de nível de campanha e grupo de anúncios para campanhas de desempenho máximo e campanhas de rascunhos e experimentos:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Se a conta tiver uma implementação de ID do AMO do lado do servidor e a configuração de conta ou campanha &quot;[!UICONTROL Auto Upload]&quot; estiver habilitada, o parâmetro será adicionado automaticamente. Caso contrário, é necessário adicioná-lo manualmente. Consulte &quot;[IDs de Adobe Advertising Usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement)&quot;.

   * Todas as outras contas do [!DNL Google Ads]:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Quando o anunciante não tiver uma integração do Adobe Analytics, o sufixo deve incluir o seguinte:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Os sufixos de página de aterrissagem em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.
>
>* (Anúncios de pesquisa dinâmica; anunciantes com Adobe Analytics e sem rastreamento do lado do servidor) Quando desejar incluir o rastreamento do feed reverso do Adobe Advertising para o Analytics, anexe o código de rastreamento da ID do AMO ao final do sufixo da página de aterrissagem no nível da conta.

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](formats-click-tracking-about.md)
>* [Formatos de ID AMO](/help/integrations/analytics/ids.md#amo-id-formats)
