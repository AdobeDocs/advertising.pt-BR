---
title: IDs de Adobe Advertising usadas por [!DNL Analytics]
description: IDs de Adobe Advertising usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 9374f5ef6aaff1f638022bc878c7af190e31888f
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# IDs de Adobe Advertising usadas por [!DNL Analytics]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável à publicidade de DSP e[!DNL Advertising Search, Social, & Commerce]*

O Adobe Advertising usa duas IDs para o rastreamento de desempenho no site: a variável *ID EF* e a variável *ID AMO*.

Quando ocorre uma impressão de anúncio, o Adobe Advertising cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entra no site sem clicar em um anúncio, [!DNL Analytics] chama esses valores do Adobe Advertising até a variável [!DNL Analytics for Advertising] Código JavaScript. Para tráfego de view-through, [!DNL Analytics] gera uma ID complementar (`SDID`), que é utilizada para compilar a ID EF e a ID AMO em [!DNL Analytics]. Para tráfego de click-through, essas IDs são incluídas no URL da página de aterrissagem usando o `ef_id` e `s_kwcid` (para a ID do AMO) parâmetros de sequência de consulta.

O Adobe Advertising distingue entre uma entrada click-through ou view-through para o site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clica nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:

   * O visitante não tem click-throughs para uma [!DNL DSP] ou [!DNL Search, Social, & Commerce] anúncio durante o [clique em janela de retrospectiva](#lookback-a4adc).

   * O visitante viu pelo menos um [!DNL DSP] anúncio durante o [janela de retrospectiva de impressão](#lookback-a4adc). A última impressão é transmitida como view-through.

* Uma entrada click-through é capturada quando um visitante do site clica em um anúncio antes de entrar no site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:

   * O URL inclui um EF ID e um AMO ID conforme adicionado ao URL da página inicial pelo Adobe Advertising.

   * O URL não contém códigos de rastreamento, mas o código JavaScript do Adobe Advertising detecta um clique nos últimos dois minutos.

![Adobe Advertising baseado em visualização [!DNL Analytics] integração](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Adobe Advertising baseado na visualização [!DNL Analytics] integração*

![Adobe Advertising click URL-based [!DNL Analytics] integração](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Baseado em URL do clique de Adobe Advertising [!DNL Analytics] integração*

## IDs EF Adobe Advertising

A ID de EF é um token exclusivo que o Adobe Advertising usa para associar a atividade a uma exposição de cliques ou anúncios online. A ID de EF é armazenada em [um [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (reservado) [!DNL eVar]) (ID EF Adobe Advertising) e rastreia cada clique de anúncio ou exposição no navegador individual ou no nível do dispositivo. As IDs EF agem principalmente como chaves para envio [!DNL Analytics] dados para Adobe Advertising para relatórios e otimização de oferta no Adobe Advertising.

### Formato de ID EF

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se um [!DNL Analytics] A implementação força o rastreamento de URL para letras minúsculas, em seguida, o Adobe Advertising não reconhecerá a ID EF. Isso afetará os lances e os relatórios do Adobe Advertising, mas não afetará os relatórios do Adobe Advertising no [!DNL Analytics].

#### [!DNL Google Ads] pesquisar anúncios

```
{gclid}:G:s
```

em que:

* `gclid` é o [!DNL Google Click ID] (GCLID).
* `s` é o tipo de rede (&quot;s&quot; para pesquisa).

#### [!DNL Microsoft Advertising] pesquisar anúncios

```
{msclkid}:G:s
```

em que:

* `msclkid` é o [!DNL Microsoft Click ID] (MSCLKID).
* `s` é o tipo de rede (&quot;s&quot; para pesquisa).

#### Exibir anúncios e anúncios de pesquisa em outros mecanismos de pesquisa

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

em que:

* &lt;*ID de visitante do Adobe Advertising*> é um identificador exclusivo por visitante (como UhKVaAAABCkJ0mDt). Também chamado de *ID do surfer*.

* &lt;*carimbo de data e hora*> é a hora no formato AAAAMMDDHHMMSS (como 20190821192533 para o Ano 2019, Mês 08, Dia 21, Hora 19:25:33).

* &lt;*tipo de canal*> é o tipo de canal responsável pelo clique ou exposição:

   * `d` para um clique em um anúncio de exibição do DSP (click-through de exibição)
   * `i` para obter uma impressão de um anúncio de exibição do DSP (display view-through)
   * `s` para um clique em um anúncio de Pesquisa (click-through de pesquisa).

Exemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### O Dimension de ID EF em [!DNL Analytics]

Entrada [!DNL Analytics] relatórios, é possível encontrar dados de EF ID procurando pela variável [!UICONTROL EF ID] dimensão e usando o [!UICONTROL EF ID Instance] métrica.

As IDs de EF estão sujeitas ao limite de identificador exclusivo de 500k no Analysis Workspace. Quando o valor 500k for atingido, todos os novos códigos de rastreamento serão relatados no título de uma linha de item &quot;[!UICONTROL Low Traffic].&quot; Devido à possibilidade de falta de fidelidade de relatório, as IDs de EF não são classificadas e você não deve usá-las para segmentos ou relatórios no [!DNL Analytics].

## IDs do Adobe Advertising AMO {#amo-id}

A ID do AMO rastreia cada combinação de anúncios exclusiva em um nível menos granular e é usada para [!DNL Analytics] classificação de dados e assimilação de métricas de publicidade (como impressões, cliques e custo) do Adobe Advertising. A ID do AMO é armazenada em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID) e é usada exclusivamente para relatórios no [!DNL Analytics].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é pronunciado como &quot;[!DNL the squid].&quot;

### Formas de implementação da ID do AMO {#amo-id-implement}

O parâmetro é adicionado aos URLs de rastreamento de uma das seguintes maneiras:

* (Recomendado) Quando o recurso de inserção do lado do servidor é implementado.

   * Clientes DSP: o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final visualiza um anúncio de exibição com o pixel Adobe Advertising.

   * Clientes de pesquisa, social e comércio:

      * Para [!DNL Google Ads] e [!DNL Microsoft® Advertising] contas com o [!UICONTROL Auto Upload] configuração ativada para a conta ou campanha, o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final clica em um anúncio com o pixel Adobe Advertising.

      * Para outras redes de publicidade, ou [!DNL Google Ads] e [!DNL Microsoft® Advertising] contas com o [!UICONTROL Auto Upload] configuração desativada, adicione manualmente o parâmetro ao seu [parâmetros de acréscimo no nível da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que o anexam aos URLs base.

* Quando o recurso de inserção do lado do servidor não está implementado:

   * Clientes do DSP: a [Código JavaScript](javascript.md) registra automaticamente click-throughs e view-throughs. Quando um navegador não é compatível com cookies de terceiros, você ainda pode rastrear conversões baseadas em cliques para os seguintes tipos de anúncio:

      * Para [!DNL Flashtalking] adicionar tags, insira manualmente macros adicionais de acordo com &quot;[Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Para [!DNL Google Campaign Manager 360] adicionar tags, insira manualmente macros adicionais de acordo com &quot;[Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Clientes de pesquisa, social e comércio:

      * Para ([!DNL Google Ads] e [!DNL Microsoft® Advertising]), adicione manualmente o parâmetro da ID do AMO aos sufixos da sua página de aterrissagem, de preferência no [nível da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} a menos que seja necessário um rastreamento diferente para componentes de conta individuais.

      * Para anúncios em todas as outras redes de anúncios, adicione manualmente o parâmetro da ID do AMO à [parâmetros de acréscimo no nível da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, que o anexam aos URLs base.

Para implementar o recurso de inserção do lado do servidor ou determinar a melhor opção para sua empresa, entre em contato com a equipe de conta da Adobe.

### Formatos de ID AMO {#amo-id-formats}

#### Formato de ID AMO para [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

em que:

* `AC` indica o canal de exibição.

* `{TM_AD_ID}` é a chave de anúncio alfanumérica gerada por Adobe Advertising. Ele é usado como um identificador exclusivo para um anúncio e serve como uma chave para converter metadados de entidade Adobe Advertising em legíveis [!DNL Analytics] dimensões.

* `{TM_PLACEMENT_ID}` é a chave de posicionamento alfanumérico gerada por Adobe Advertising. Ele é usado como um identificador exclusivo para um posicionamento e serve como uma chave para converter metadados de entidade de Adobe Advertising em legíveis [!DNL Analytics] dimensões.

Exemplo de ID do AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formatos de ID do AMO para anúncios de Pesquisa, Social e Comércio {#amo-id-format-search}

Os parâmetros variam por rede de anúncios, mas os seguintes parâmetros são comuns a todos:

* `AL` indica o canal de pesquisa. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` é uma ID de usuário exclusiva atribuída ao anunciante.

* `{sid}` é substituído pela ID numérica da conta de rede de anúncios do anunciante: *3* para [!DNL Google Ads], *10* para [!DNL Microsoft Advertising], *45* para [!DNL Meta], *86* para [!DNL Yahoo! Display Network], *87* para [!DNL Naver], *88* para [!DNL Baidu], *90* para [!DNL Yandex], *94* para [!DNL Yahoo! Japan Ads], *105* para [!DNL Yahoo Native] (obsoleto) ou *106* para [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

em que:

* `{creative}` é a ID numérica exclusiva da rede de publicidade para o criativo.
* `{placement}` é o site em que o anúncio foi clicado.
* `{keywordid}` é a ID numérica exclusiva da rede de publicidade para a palavra-chave que disparou o anúncio.

##### [!DNL Google Ads]

Isso inclui campanhas de compras usando o [!DNL Google Merchant Center].

* Contas que usam o formato de ID AMO mais recente, compatível com relatórios de nível de campanha e grupo de anúncios para campanhas de desempenho máximo e campanhas de rascunhos e experimentos:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Todas as outras contas:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

em que:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` é o [!DNL Google Ads] ID numérica exclusiva do criativo.
* `{matchtype}` é o tipo de correspondência da palavra-chave que acionou o anúncio: `e` para obter informações exatas, `p` para frase, ou `b` para amplo.
* `{placement}` é o nome de domínio do site em que o anúncio foi clicado. Um valor está disponível para anúncios em campanhas direcionadas para posicionamento e para anúncios em campanhas direcionadas por palavras-chave que são exibidas em sites de conteúdo.
* `{network}` indica a rede da qual o clique ocorreu: `g` para [!DNL Google] pesquisa (somente para anúncios direcionados a palavras-chave), `s` para um parceiro de pesquisa (somente para anúncios direcionados a palavras-chave) ou `d` para a rede de exibição (para anúncios direcionados por palavra-chave ou de posicionamento).
* `{product_partition_id}` é o identificador numérico exclusivo da rede de publicidade para o grupo de produtos usado com anúncios de produtos.
* `{keyword}` é a palavra-chave específica que acionou seu anúncio (em sites de pesquisa) ou a palavra-chave com melhor correspondência (em sites de conteúdo).
* `{campaignid}` é o identificador numérico exclusivo da rede de publicidade para a campanha.
* `{adgroupid}` é o identificador numérico exclusivo da rede de publicidade para o grupo de publicidade.

>[!NOTE]
>
>* Para anúncios de pesquisa dinâmica, {keyword} é preenchida com o direcionamento automático.
>* Ao gerar o rastreamento para [!DNL Google] anúncios de compras, um parâmetro de ID do produto, `{adwords_producttargetid}`, é inserido antes do parâmetro de palavra-chave. O parâmetro da ID do produto não aparece no [!DNL Google Ads] parâmetros de rastreamento no nível da conta e no nível da campanha.
>* Para usar o código de rastreamento de ID do AMO mais recente, consulte &quot;[Atualizar o código de rastreamento da ID do AMO para um [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Pesquisar campanhas:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campanhas de compras (usando [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campanhas de rede de público-alvo:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

em que:

* `{AdId}` é a ID numérica exclusiva da rede de publicidade para o criativo.
* `{OrderItemId}` é a ID numérica da rede de publicidade para a palavra-chave.
* `{CriterionId}` é a ID numérica da rede de publicidade para o grupo de produtos usado com anúncios de produtos.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

em que:

* `{creative}` é a ID numérica exclusiva da rede de publicidade para o criativo.
* `{matchtype}` é o tipo de correspondência da palavra-chave que acionou o anúncio: `be` para obter informações exatas, `bp` para frase, ou `bb` para amplo.
* `{network}` indica a rede da qual o clique ocorreu: `n` para nativo ou `s` para pesquisa.
* `{keyword}` é a palavra-chave que acionou seu anúncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

em que:

* `{ad_id}` é a ID numérica exclusiva da rede de publicidade para o criativo.
* `{source_type}` é o tipo de site no qual o anúncio foi exibido: *b* para pesquisa, *c* para contexto (conteúdo), ou *ct* para categoria.
* `{phrase_id}` é a ID numérica da rede de publicidade para a palavra-chave.

### DIMENSION de ID AMO em [!DNL Analytics]

Nos relatórios do Analytics, você pode encontrar dados da ID do AMO procurando pela variável [!UICONTROL AMO ID] dimensão e usando o [!UICONTROL AMO ID Instances] métrica. A variável [!UICONTROL AMO ID] dimensão armazena todos os valores de ID do AMO capturados, enquanto a variável [!UICONTROL AMO ID Instances] indica a frequência com que um valor de ID do AMO foi capturado pelo site. Por exemplo, se o mesmo anúncio de pesquisa foi clicado quatro vezes, mas o Analytics rastreou sete entradas de site, então [!UICONTROL AMO ID Instances] seria sete (7) e [!UICONTROL Clicks] seria quatro (4).

Para qualquer relatório ou auditoria [!DNL Analytics], a prática recomendada é usar a ID do AMO junto com a instância correspondente. Para obter mais informações, consulte &quot;[Validação de dados de click-through para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; em &quot;Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising.&quot;

## Sobre as classificações do Analytics

Entrada [!DNL Analytics], um [classificação](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados para um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Adobe Advertising categoriza dados brutos de Adobe Advertising usando classificações para que você possa exibir os dados de diferentes maneiras (por exemplo, por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios de Adobe Advertising no [!DNL Analytics] e podem ser usadas com as métricas do AMO, como [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions], e [!UICONTROL AMO Clicks]e com eventos personalizados e padrão no local, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e ADOBE ADVERTISING](data-variances.md)
