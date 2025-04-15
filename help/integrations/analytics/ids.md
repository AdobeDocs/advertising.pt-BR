---
title: Adobe Advertising IDs Usadas por [!DNL Analytics]
description: Adobe Advertising IDs Usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1762'
ht-degree: 0%

---

# Adobe Advertising IDs Usadas por [!DNL Analytics]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável ao Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O Adobe Advertising usa duas IDs para o rastreamento de desempenho no site: a *EF ID* e a *AMO ID*.

Quando ocorre uma impressão de anúncio, o Adobe Advertising cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entra no site sem clicar em um anúncio, o [!DNL Analytics] chama esses valores do Adobe Advertising por meio do código JavaScript [!DNL Analytics for Advertising]. Para tráfego view-through, [!DNL Analytics] gera uma ID complementar (`SDID`), que é usada para compilar a ID EF e a ID AMO em [!DNL Analytics]. Para tráfego de click-through, essas IDs são incluídas na URL da página de aterrissagem usando os parâmetros da sequência de consulta `ef_id` e `s_kwcid` (para a ID AMO).

O Adobe Advertising faz a distinção entre uma entrada click-through ou view-through para o site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clica nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:

   * O visitante não tem click-throughs para um anúncio [!DNL DSP] ou [!DNL Search, Social, & Commerce] durante a [janela de retrospectiva de cliques](#lookback-a4adc).

   * O visitante viu pelo menos um anúncio [!DNL DSP] durante a [janela de retrospectiva de impressão](#lookback-a4adc). A última impressão é transmitida como view-through.

* Uma entrada click-through é capturada quando um visitante do site clica em um anúncio antes de entrar no site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:

   * O URL inclui uma EF ID e uma AMO ID conforme adicionada ao URL da página inicial pelo Adobe Advertising.

   * O URL não contém códigos de rastreamento, mas o código JavaScript do Adobe Advertising detecta um clique nos últimos dois minutos.

![Integração do [!DNL Analytics] baseada na visualização do Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Integração do [!DNL Analytics] baseada na visualização do Adobe Advertising*

![Integração [!DNL Analytics] baseada em URL de cliques do Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Integração [!DNL Analytics] baseada em URLs de cliques do Adobe Advertising*

## IDs EF do Adobe Advertising

A ID de EF é um token exclusivo que o Adobe Advertising usa para associar a atividade a uma exposição de cliques ou anúncios online. A ID EF é armazenada na dimensão [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (reservada [!DNL eVar]) (ID EF Adobe Advertising) e rastreia cada clique ou exposição de anúncio no nível de navegador ou dispositivo individual. As IDs de EF atuam principalmente como chaves para enviar dados do [!DNL Analytics] à Adobe Advertising para relatórios e otimização de oferta no Adobe Advertising.

### Formato de ID EF

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma implementação [!DNL Analytics] forçar o rastreamento de URL em minúsculas, o Adobe Advertising não reconhecerá a ID de EF. Isso afeta os lances e os relatórios do Adobe Advertising, mas não afeta os relatórios do Adobe Advertising no [!DNL Analytics].

#### [!DNL Google Ads] anúncios de pesquisa

```
{gclid}:G:s
```

em que:

* `gclid` é o [!DNL Google Click ID] (GCLID).
* `s` é o tipo de rede (s para pesquisa).

#### [!DNL Microsoft Advertising] anúncios de pesquisa

```
{msclkid}:G:s
```

em que:

* `msclkid` é o [!DNL Microsoft Click ID] (MSCLKID).
* `s` é o tipo de rede (s para pesquisa).

#### Exibir anúncios e anúncios de pesquisa em outros mecanismos de pesquisa

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

em que:

* &lt;*ID de visitante do Adobe Advertising*> é um identificador exclusivo por visitante (como UhKVaAAABCkJ0mDt). Também chamado de *ID do surfer*.

* &lt;*carimbo de data/hora*> é a hora no formato AAAAMMDDHHMMSS (como 20190821192533 para Ano 2019, Mês 08, Dia 21, Hora 19:25:33).

* &lt;*tipo de canal*> é o tipo de canal responsável pelo clique ou exposição:

   * `d` para um clique em um anúncio de exibição do DSP (click-through de exibição)
   * `i` para obter uma impressão de um anúncio de exibição do DSP (view-through)
   * `s` para um clique em um anúncio de Pesquisa (click-through de pesquisa).

Exemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### O Dimension da ID EF em [!DNL Analytics]

Em [!DNL Analytics] relatórios, você pode encontrar dados de EF ID procurando a dimensão [!UICONTROL EF ID] e usando a métrica [!UICONTROL EF ID Instance].

As IDs de EF estão sujeitas ao limite de identificador exclusivo de 500k no Analysis Workspace. Quando o valor 500k for atingido, todos os novos códigos de rastreamento serão relatados no título de item de uma linha &quot;[!UICONTROL Low Traffic].&quot; Devido à possibilidade de falta de fidelidade de relatório, as IDs de EF não são classificadas e você não deve usá-las para segmentos ou relatórios no [!DNL Analytics].

## IDs do Adobe Advertising AMO {#amo-id}

A ID do AMO rastreia cada combinação única de anúncios em um nível menos granular e é usada para a classificação de dados do [!DNL Analytics] e a assimilação de métricas de publicidade (como impressões, cliques e custo) do Adobe Advertising. A ID do AMO está armazenada em uma [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou dimensão de rVar (ID do AMO) e é usada exclusivamente para relatórios em [!DNL Analytics].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é pronunciado como &quot;[!DNL squid]&quot;.

### Formas de implementação da ID do AMO {#amo-id-implement}

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

* `{TM_AD_ID}` é a chave de anúncio alfanumérica gerada pela Adobe Advertising. Ele é usado como um identificador exclusivo para um anúncio e serve como uma chave para traduzir metadados de entidade do Adobe Advertising em dimensões [!DNL Analytics] legíveis.

* `{TM_PLACEMENT_ID}` é a chave de posicionamento alfanumérico gerada pela Adobe Advertising. Ele é usado como um identificador exclusivo para um posicionamento e serve como uma chave para traduzir metadados de entidade do Adobe Advertising em dimensões [!DNL Analytics] legíveis.

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
>Enquanto isso, os formatos herdados, como os seguintes, ainda funcionam:
>* Pesquisar campanhas:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campanhas de compras (usando [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campanhas de rede de público-alvo:
>  `s_kwcid=AL!{userid}!10!{AdId}`

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

### DIMENSION de ID AMO em [!DNL Analytics]

Nos relatórios do Analytics, você pode encontrar dados da ID do AMO pesquisando a dimensão [!UICONTROL AMO ID] e usando a métrica [!UICONTROL AMO ID Instances]. A dimensão [!UICONTROL AMO ID] hospeda todos os valores de ID do AMO capturados, enquanto a métrica [!UICONTROL AMO ID Instances] indica com que frequência um valor de ID do AMO foi capturado pelo site. Por exemplo, se o mesmo anúncio de pesquisa foi clicado quatro vezes, mas o Analytics rastreou sete entradas de site, então [!UICONTROL AMO ID Instances] seria sete (7) e [!UICONTROL Clicks] seriam quatro (4).

Para qualquer relatório ou auditoria em [!DNL Analytics], a prática recomendada é usar a ID do AMO junto com sua instância correspondente. Para obter mais informações, consulte &quot;[Validação de Dados de Click-Through para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; em &quot;Variações de Dados Esperadas Entre [!DNL Analytics] e o Adobe Advertising.&quot;

## Sobre as classificações do Analytics

Em [!DNL Analytics], uma [classificação](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados de um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Adobe Advertising categoriza dados brutos do Adobe Advertising usando classificações para que você possa exibir os dados de diferentes maneiras (por exemplo, por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios do Adobe Advertising em [!DNL Analytics] e podem ser usadas com as métricas AMO, como [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] e [!UICONTROL AMO Clicks], bem como com eventos personalizados e padrão no site, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Variações de Dados Esperadas Entre [!DNL Analytics] e Adobe Advertising](data-variances.md)
