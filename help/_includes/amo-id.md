---
source-git-commit: 6fa4e5d06271789edc915d67d320f775a83ed653
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 0%

---
# IDs do Adobe Advertising AMO

## IDs do Adobe Advertising AMO {#amo-id}

A ID do AMO rastreia cada combinação única de anúncios em um nível menos granular e é usada para a classificação de dados do [!DNL Analytics] e do Customer Journey Analytics, além da assimilação de métricas de publicidade (como impressões, cliques e custo) do Adobe Advertising.

Para [!DNL Analytics], a ID do AMO é armazenada em uma [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=pt-BR) ou dimensão de rVar (ID do AMO).

Para o Customer Journey Analytics, a ID do AMO é armazenada na propriedade `trackingCode` do objeto `conversionDetails`, que faz parte do [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é pronunciado como &quot;[!DNL squid]&quot;.

### ([!DNL Analytics] usuários) Maneiras de Implementar a ID do AMO {#amo-id-implement}

<!-- Add info about implementing in CJA -->

O parâmetro é adicionado aos URLs de rastreamento de uma das seguintes maneiras:

* (Recomendado) Quando o recurso de inserção do lado do servidor é implementado.

   * Clientes do DSP: o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final visualiza um anúncio de exibição com o pixel do Adobe Advertising.

   * Clientes do Search, Social e Commerce:

      * Para contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising] com a configuração [!UICONTROL Auto Upload] ativada para a conta ou campanha, o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final clica em um anúncio com o pixel do Adobe Advertising.

      * Para outras redes de publicidade, ou contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising] com a configuração [!UICONTROL Auto Upload] desabilitada, adicione manualmente o parâmetro aos seus [parâmetros de acréscimo no nível da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que o anexam às suas URLs base.

* Quando o recurso de inserção do lado do servidor não está implementado:

   * Clientes do DSP: o [código JavaScript](javascript.md) registra automaticamente click-throughs e view-throughs. Quando um navegador não é compatível com cookies de terceiros, você ainda pode rastrear conversões baseadas em cliques para os seguintes tipos de anúncio:

      * Para marcas de anúncio [!DNL Flashtalking], insira manualmente macros adicionais por &quot;[Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio](/help/integrations/analytics/macros-flashtalking.md).&quot; **Observação:** este procedimento não será necessário se sua organização tiver uma parceria direta com [!DNL Flashtalking] e você usar macros de passagem de dados para rastrear os parâmetros de rastreamento `s_kwcid` e `ef_id` de acordo com a documentação de suporte do [!DNL Flashtalking] em [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Para marcas de anúncio [!DNL Google Campaign Manager 360], insira manualmente macros adicionais por &quot;[Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Marcas de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Clientes do Search, Social e Commerce:

      * Para os anúncios ([!DNL Google Ads] e [!DNL Microsoft Advertising]), adicione manualmente o parâmetro da ID do AMO aos sufixos da sua página de aterrissagem, idealmente no [nível de conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, a menos que seja necessário um rastreamento diferente para componentes de conta individuais.

      * Para anúncios em todas as outras redes de anúncios, adicione manualmente o parâmetro da ID do AMO aos seus [parâmetros de acréscimo no nível da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que o anexam às suas URLs base.

Para implementar o recurso de inserção do lado do servidor ou determinar a melhor opção para sua empresa, entre em contato com a equipe de conta da Adobe.

### Formatos de ID AMO {#amo-id-formats}

#### Formato de ID AMO para [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

em que:

* `AC` indica o canal de exibição.

* `{TM_AD_ID}` é a chave de anúncio alfanumérica gerada pela Adobe Advertising. Ele é usado como um identificador exclusivo para um anúncio e serve como uma chave para traduzir metadados de entidade do Adobe Advertising em dimensões do Customer Journey Analytics e do [!DNL Analytics] legíveis.

* `{TM_PLACEMENT_ID}` é a chave de posicionamento alfanumérico gerada pela Adobe Advertising. Ele é usado como um identificador exclusivo para um posicionamento e serve como uma chave para traduzir metadados de entidade do Adobe Advertising em dimensões do Customer Journey Analytics e do [!DNL Analytics] legíveis.

Exemplo de ID do AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formatos de ID do AMO para anúncios de Pesquisa, Social e Commerce {#amo-id-format-search}

Os parâmetros variam por rede de anúncios, mas os seguintes parâmetros são comuns a todos:

* `AL` indica o canal de pesquisa. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` é um identificador de usuário único atribuído ao anunciante.

* `{sid}` é substituído pelo ID numérico da conta de rede de publicidade do anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto) ou *106* para [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

em que:

* `{creative}` é o identificador numérico exclusivo da rede de publicidade para o criativo.
* `{placement}` é o site no qual o anúncio foi clicado.
* `{keywordid}` é o identificador numérico exclusivo da rede de publicidade para a palavra-chave que disparou o anúncio.

##### [!DNL Google Ads]

Isso incluindo campanhas de compras usando [!DNL Google Merchant Center].

* Contas que usam o formato de ID AMO mais recente, compatível com relatórios de nível de campanha e grupo de anúncios para campanhas de desempenho máximo e campanhas de rascunhos e experimentos:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Todas as outras contas:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

em que:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` é a ID numérica exclusiva de [!DNL Google Ads] do criativo.
* `{matchtype}` é o tipo de correspondência da palavra-chave que disparou o anúncio: `e` para exato, `p` para frase ou `b` para amplo.
* `{placement}` é o nome de domínio do site em que o anúncio foi clicado. Um valor está disponível para anúncios em campanhas direcionadas para posicionamento e para anúncios em campanhas direcionadas por palavras-chave que são exibidas em sites de conteúdo.
* `{network}` indica a rede a partir da qual o clique ocorreu: `g` para [!DNL Google] pesquisa (somente para anúncios direcionados por palavra-chave), `s` para um parceiro de pesquisa (somente para anúncios direcionados por palavra-chave) ou `d` para a rede de exibição (para anúncios direcionados por palavra-chave ou de posicionamento).
* `{product_partition_id}` é o identificador numérico exclusivo da rede de publicidade para o grupo de produtos usado com anúncios de produtos.
* `{keyword}` é a palavra-chave específica que disparou seu anúncio (em sites de pesquisa) ou a palavra-chave com melhor correspondência (em sites de conteúdo).
* `{campaignid}` é o identificador numérico exclusivo da rede de publicidade para a campanha.
* `{adgroupid}` é o identificador numérico exclusivo da rede de publicidade para o grupo de publicidade.

>[!NOTE]
>
>* Para anúncios de pesquisa dinâmica, {keyword} é preenchido com o direcionamento automático.
>* Ao gerar o rastreamento para [!DNL Google] anúncios de compras, um parâmetro de ID de produto, `{adwords_producttargetid}`, é inserido antes do parâmetro de palavra-chave. O parâmetro da ID do produto não aparece nos parâmetros de rastreamento de nível de conta e nível de campanha [!DNL Google Ads].
>* Para usar o código de rastreamento da ID do AMO mais recente, consulte &quot;[Atualizar o código de rastreamento da ID do AMO para uma [!DNL Google Ads] conta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Todos os tipos de campanha:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

em que:

* `{AdId}` é o identificador numérico exclusivo da rede de publicidade para o criativo.
* `{OrderItemId}` é a ID numérica da rede de publicidade para a palavra-chave.
* `{CampaignId}` é o identificador numérico exclusivo da rede de publicidade para a campanha.
* `{AdGroupId}` é o identificador numérico exclusivo da rede de publicidade para o grupo de publicidade.

>[!NOTE]
>
> Para contas com campanhas sem a opção de rastreamento [!UICONTROL Auto Upload] que ainda não foram migradas para o novo formato, atualize manualmente cada sufixo de página de aterrissagem para incluir o formato acima.
> &#x200B;>Enquanto isso, os formatos herdados, como os seguintes, ainda funcionam:
>* Pesquisar campanhas:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campanhas de compras (usando [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campanhas de rede de público-alvo:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

em que:

* `{creative}` é o identificador numérico exclusivo da rede de publicidade para o criativo.
* `{matchtype}` é o tipo de correspondência da palavra-chave que disparou o anúncio: `be` para exato, `bp` para frase ou `bb` para amplo.
* `{network}` indica a rede da qual o clique ocorreu: `n` para nativo ou `s` para pesquisa.
* `{keyword}` é a palavra-chave que disparou seu anúncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

em que:

* `{ad_id}` é o identificador numérico exclusivo da rede de publicidade para o criativo.
* `{source_type}` é o tipo de site no qual o anúncio foi exibido: *b* para pesquisa, *c* para contexto (conteúdo) ou *ct* para categoria.
* `{phrase_id}` é a ID numérica da rede de publicidade para a palavra-chave.
