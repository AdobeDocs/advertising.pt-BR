---
title: Adobe Advertising IDs Usadas por [!DNL Analytics]
description: Adobe Advertising IDs Usadas por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dede10acca1540a10699be3c14564a6f9360edd2
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# Adobe Advertising IDs Usadas por [!DNL Analytics]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável ao Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O Adobe Advertising usa duas IDs para o rastreamento de desempenho no site: a *EF ID* e a *AMO ID*.

Quando ocorre uma impressão de anúncio, o Adobe Advertising cria os valores de ID AMO e ID EF e os armazena. Quando um visitante que viu um anúncio entra no site sem clicar em um anúncio, o [!DNL Analytics] chama esses valores do Adobe Advertising por meio do código JavaScript [!DNL Analytics for Advertising]. Para tráfego view-through, [!DNL Analytics] gera uma ID complementar (`SDID`), que é usada para compilar a ID EF e a ID AMO em [!DNL Analytics]. Para tráfego de click-through, essas IDs são incluídas na URL da página de aterrissagem usando os parâmetros da sequência de consulta `ef_id` e `s_kwcid` (para a ID AMO).

O Adobe Advertising faz a distinção entre uma entrada click-through ou view-through para o site usando os seguintes critérios:

* Uma entrada view-through é capturada quando um usuário visita o site após visualizar um anúncio, mas não clica nele. [!DNL Analytics] registra um view-through se duas condições forem atendidas:

   * O visitante não tem click-throughs para um anúncio [!DNL DSP] ou [!DNL Search, Social, & Commerce] durante a [janela de retrospectiva de cliques](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * O visitante viu pelo menos um anúncio [!DNL DSP] durante a [janela de retrospectiva de impressão](/help/integrations/analytics/prerequisites.md#lookback-a4adc). A última impressão é transmitida como view-through.

* Uma entrada click-through é capturada quando um visitante do site clica em um anúncio antes de entrar no site. [!DNL Analytics] captura um click-through quando uma das seguintes condições ocorre:

   * O URL inclui uma EF ID e uma AMO ID conforme adicionada ao URL da página inicial pelo Adobe Advertising.

   * O URL não contém códigos de rastreamento, mas o código JavaScript do Adobe Advertising detecta um clique nos últimos dois minutos.

![Integração do [!DNL Analytics] baseada na visualização do Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Integração do [!DNL Analytics] baseada na visualização do Adobe Advertising*

![Integração [!DNL Analytics] baseada em URL de cliques do Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Integração [!DNL Analytics] baseada em URLs de cliques do Adobe Advertising*

## IDs EF do Adobe Advertising

A ID de EF é um token exclusivo que o Adobe Advertising usa para associar a atividade a um clique ou exposição de anúncios online em um navegador ou dispositivo individual. As EF IDs atuam principalmente como chaves para enviar dados do [!DNL Analytics] e dados do Customer Journey Analytics para a Adobe Advertising para otimização de relatórios e ofertas no Adobe Advertising.

Para [!DNL Analytics], a ID EF é armazenada em [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (reservada [!DNL eVar]) dimensão (ID EF Adobe Advertising).

Para o Customer Journey Analytics, a ID EF é armazenada na propriedade `trackingIdentities` do objeto `conversionDetails`, que faz parte do [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

### Formatos de ID EF {#ef-id-formats}

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma implementação do [!DNL Analytics] ou do Customer Journey Analytics forçar o rastreamento de URL em minúsculas, o Adobe Advertising não reconhecerá a EF ID. Isso afeta os lances e os relatórios da Adobe Advertising, mas não afeta os relatórios do Adobe Advertising no [!DNL Analytics] ou na Customer Journey Analytics.

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

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

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

### DIMENSION de ID AMO em [!DNL Analytics]

Nos relatórios do Analytics, você pode encontrar dados da ID do AMO pesquisando a dimensão [!UICONTROL AMO ID] e usando a métrica [!UICONTROL AMO ID Instances]. A dimensão [!UICONTROL AMO ID] hospeda todos os valores de ID do AMO capturados, enquanto a métrica [!UICONTROL AMO ID Instances] indica com que frequência um valor de ID do AMO foi capturado pelo site. Por exemplo, se o mesmo anúncio de pesquisa foi clicado quatro vezes, mas o Analytics rastreou sete entradas de site, então [!UICONTROL AMO ID Instances] seria sete (7) e [!UICONTROL Clicks] seriam quatro (4).

Para qualquer relatório ou auditoria em [!DNL Analytics], a prática recomendada é usar a ID do AMO junto com sua instância correspondente. Para obter mais informações, consulte &quot;[Validação de Dados de Click-Through para [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; em &quot;Variações de Dados Esperadas Entre [!DNL Analytics] e o Adobe Advertising.&quot;

## Sobre as classificações do Analytics

Em [!DNL Analytics], uma [classificação](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) é uma parte dos metadados de um determinado código de rastreamento, como Conta, Campanha ou Anúncio. O Adobe Advertising categoriza dados brutos do Adobe Advertising usando classificações para que você possa exibir os dados de diferentes maneiras (por exemplo, por Tipo de anúncio ou Campanha) ao gerar relatórios. As classificações formam a base dos relatórios do Adobe Advertising em [!DNL Analytics] e podem ser usadas com as métricas AMO, como [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] e [!UICONTROL AMO Clicks], bem como com eventos personalizados e padrão no site, como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Variações de Dados Esperadas Entre [!DNL Analytics] e Adobe Advertising](data-variances.md)
