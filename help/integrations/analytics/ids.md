---
title: IDs de publicidade do Adobe usadas por [!DNL Analytics]
description: IDs de publicidade do Adobe usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# IDs de publicidade do Adobe usadas por [!DNL Analytics]

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

*Aplicável à publicidade de DSP e[!DNL Advertising Search]*

A Adobe Advertising usa duas IDs para o rastreamento de desempenho no site: a *ID EF* e a variável *ID AMO*.

Quando ocorre uma impressão de anúncio, a Adobe Advertising cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entra no site sem clicar em um anúncio, [!DNL Analytics] O chama esses valores da Publicidade de Adobe por meio da [!DNL Analytics for Advertising] Código JavaScript. Para tráfego de view-through, [!DNL Analytics] gera uma ID complementar (`SDID`), que é utilizada para compilar a ID EF e a ID AMO em [!DNL Analytics]. Para tráfego de click-through, essas IDs são incluídas no URL da página de aterrissagem usando o `s_kwcid` e `ef_id` parâmetros da sequência de consulta.

A Adobe Advertising distingue entre uma entrada click-through ou view-through para o site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clica nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:
   * O visitante não tem click-throughs para uma [!DNL DSP] ou [!DNL Search] anúncio durante o [clique em janela de retrospectiva](#lookback-a4adc).
   * O visitante viu pelo menos um [!DNL DSP] anúncio durante o [janela de retrospectiva de impressão](#lookback-a4adc). A última impressão é transmitida como view-through.
* Uma entrada click-through é capturada quando um visitante do site clica em um anúncio antes de entrar no site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:
   * O URL inclui uma EF ID e uma AMO ID conforme adicionada ao URL da página de aterrissagem pela Adobe Advertising.
   * O URL não contém códigos de rastreamento, mas o código JavaScript do Adobe Advertising detecta um clique nos últimos dois minutos.

![Adobe Baseado em visualização de publicidade [!DNL Analytics] integração](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Adobe Baseado na visualização [!DNL Analytics] integração*

![Adobe Baseado em URL de clique de publicidade [!DNL Analytics] integração](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe Advertising click URL-based (Baseado em URL de cliques do Advertising) [!DNL Analytics] integração*

## IDs EF de publicidade do Adobe

A ID EF é um token exclusivo que a Adobe Advertising usa para associar uma atividade a uma exposição de cliques ou anúncios online. A ID de EF é armazenada num [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou a dimensão rVar (eVar reservado) (Adobe ID EF de anúncio) e rastreia cada clique de anúncio ou exposição no navegador individual ou no nível do dispositivo. As IDs EF agem principalmente como chaves para envio [!DNL Analytics] dados para a Adobe Advertising para relatórios e otimização de oferta na Adobe Advertising.

### Formato de ID EF

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se um [!DNL Analytics] A implementação força o rastreamento de URL para letras minúsculas, então a Adobe Advertising não reconhecerá a ID de EF. Isso afetará os lances e os relatórios da Adobe Advertising, mas não tem impacto nos relatórios da Adobe Advertising no [!DNL Analytics].

#### [!DNL Google Ads] pesquisar anúncios

```
{gclid}:G:s
```

em que:

* `gclid` é o [!DNL Google Click ID] (GCLID).
* `s` é o tipo de rede (&quot;s&quot; para pesquisa).

#### Anúncios de pesquisa da Microsoft Advertising

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

## IDs AMO de publicidade do Adobe

A ID do AMO rastreia cada combinação de anúncios exclusiva em um nível menos granular e é usada para [!DNL Analytics] classificação de dados e assimilação de métricas de publicidade (como impressões, cliques e custo) da Adobe Advertising. A ID do AMO é armazenada em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID) e é usada exclusivamente para relatórios no [!DNL Analytics].

A ID do AMO também é chamada de `s_kwcid`, que às vezes é pronunciado como &quot;[!DNL the squid].&quot;

### Formato de ID AMO para [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

em que:

* &lt;*ID do canal*> pode ser:

   * `AC` = DSP publicitário
   * `AL` para [!DNL Advertising Search]

* &lt;*ID do anúncio*> é usado como um identificador exclusivo gerado pela Adobe Advertising para um anúncio. Ele serve como uma chave para converter metadados de entidade de publicidade Adobe em legíveis [!DNL Analytics] dimensões.

* &lt;*ID de posicionamento*> é um identificador exclusivo gerado pela Adobe Advertising para uma inserção. Ele serve como uma chave para converter metadados de entidade de publicidade Adobe em legíveis [!DNL Analytics] dimensões.

Exemplo de ID do AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato de ID AMO para [!DNL Search]

IDs AMO para [!DNL Search] siga um formato distinto para cada mecanismo de pesquisa. O formato para todos os mecanismos de pesquisa começa com o seguinte:

```
AL!{userid}!{sid}
```

em que:

* `AL` é a ID do canal para a rede de publicidade.
* `{userid}` é a ID de usuário numérica exclusiva que a Adobe Advertising atribui ao anunciante.
* `{sid}` é a ID numérica que a Adobe Advertising usa para a rede de publicidade especificada, como `3` para [!DNL Google Ads] ou `10` para [!DNL Microsoft Advertising].

A seguir estão os formatos completos de ID do AMO para algumas redes de anúncios. Para formatos de ID AMO para outras redes de anúncios, entre em contato com a equipe de conta do Adobe.

Formato de ID AMO para [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

em que:

* `{creative}` é o [!DNL Google Ads] ID numérica exclusiva do criativo.
* `{matchtype}` é o tipo de correspondência da palavra-chave que acionou o anúncio: `e` para obter informações exatas, `p` para frase, ou `b` para amplo.
* `{placement}` é o nome de domínio do site em que o anúncio foi clicado. Um valor está disponível para anúncios em campanhas direcionadas para posicionamento e para anúncios em campanhas direcionadas por palavras-chave que são exibidas em sites de conteúdo.
* `{network}` indica a rede da qual o clique ocorreu:  `g` para [!DNL Google] pesquisa (somente para anúncios direcionados a palavras-chave), `s` para um parceiro de pesquisa (somente para anúncios direcionados a palavras-chave) ou `d` para a Rede de exibição (para anúncios direcionados a palavras-chave ou de posicionamento).
* `{keyword}` é a palavra-chave específica que acionou seu anúncio (em sites de pesquisa) ou a palavra-chave com melhor correspondência (em sites de conteúdo).

Formato de ID AMO para [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

em que:

* `{AdId}` é o [!DNL Microsoft Advertising] ID numérica exclusiva do criativo.
* `{OrderItemId}` é o [!DNL Microsoft Advertising] ID numérica para a palavra-chave.

### DIMENSION de ID AMO em [!DNL Analytics]

Nos relatórios do Analytics, você pode encontrar dados da ID do AMO procurando pela variável [!UICONTROL AMO ID] dimensão e usando o [!UICONTROL AMO ID Instance] métrica. A variável [!UICONTROL AMO ID] dimensão armazena todos os valores de ID do AMO capturados, enquanto a variável [!UICONTROL AMO ID Instance] indica a frequência com que um valor de ID do AMO foi capturado pelo site. Por exemplo, se o mesmo anúncio de pesquisa foi clicado quatro vezes, mas o Analytics rastreou sete entradas de site, então [!UICONTROL AMO ID Instance] seria sete (7) e [!UICONTROL Clicks] seria quatro (4).

Para qualquer relatório ou auditoria [!DNL Analytics], a prática recomendada é usar a ID do AMO junto com a instância correspondente. Para obter mais informações, consulte &quot;[Validação de dados para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; em &quot;Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising.&quot;

## Sobre as classificações do Analytics

Entrada [!DNL Analytics], um [classificação](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados para um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Adobe Advertising categoriza dados brutos de publicidade de Adobe usando classificações para que você possa exibir os dados de diferentes maneiras (por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios de Publicidade em Adobe no [!DNL Analytics] e podem ser usadas com as métricas do AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], e [!UICONTROL AMO Clicks]e com eventos personalizados e padrão no local, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](data-variances.md)

