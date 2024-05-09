---
title: Coletar dados de cliques e impressões de campanhas de DSP
description: Saiba como capturar eventos de cliques e impressões baseados em cookies de anúncios de DSP usando pixels de Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Coletar dados de exposição da mídia de campanhas de publicidade com DSP

*Anunciantes com somente DSP publicitário*

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Audience Manager*

Este documento explica como marcar anúncios DSP de publicidade para capturar eventos de impressão e clique baseados em cookies usando pixels de Audience Manager e tarefas adicionais necessárias para usar os dados.

Os pixels do evento não capturam eventos que ocorrem em ambientes sem cookies, como aplicativos para dispositivos móveis e TV conectada (CTV).

## Etapa 1: configurar uma fonte de dados no Audience Manager {#set-up-data-source}

No Audience Manager, crie um [fonte de dados](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) para os dados de impressão do DSP e cliques. Incluir a ID da fonte de dados [em cada tag de evento](#implement-dsp-pixels) para que todos os eventos rastreados sejam atribuídos à fonte de dados.

>[!NOTE]
> É possível coletar todos os dados de impressões e cliques para campanhas de publicidade executadas em vários DSP em uma única fonte de dados.

## Etapa 2: Implementar pixels de impressão e de evento de clique nas páginas da Web {#implement-dsp-pixels}

Os anunciantes podem criar e implementar tags de evento para suas próprias marcas. Se necessário, entre em contato com seu consultor da Adobe Audience Manager ou com sua equipe de conta da Adobe para obter suporte.

>[!NOTE]
>
>Se sua organização usar [!DNL Analytics] , talvez você não precise do rastreamento de cliques do Audience Manager. O Adobe Analytics captura sinais de cliques e pode enviá-los para o Audience Manager por meio de [encaminhamento pelo lado do servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintaxe do pixel

Os pixels do evento devem incluir os seguintes parâmetros.

**Pixels de rastreamento de impressão:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

com [parâmetros adicionais opcionais](#parameters) prefixado com `&`

**Pixels de rastreamento de cliques:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

com [parâmetros adicionais opcionais](#parameters) prefixado com `&`

Onde:

* `[Audience Manager customer domain]` é o nome de domínio que enviará eventos de impressão ou clique para [!DNL Adobe].

* `[source id]` é a ID do [fonte de dados](#set-up-data-source) no qual você rastreará os dados de impressão e cliques do DSP.

* `[redirect URL]` é o URL de redirecionamento codificado duas vezes. Se estiver usando uma ferramenta de codificação online, como www.urlencoder.org, execute a cadeia de caracteres por meio do codificador e codifique novamente o resultado.

* `${TM_CAMPAIGN_ID_NUM}` é a ID numérica da campanha no DSP. Se você quiser codificar uma ID de campanha individual em vez de usar a macro DSP, localize a ID nas configurações da campanha.

* Each [parâmetro](#key-value-pairs) tem o prefixo `&` e está no formato `d_parameter=parameter_id`, onde `parameter` é substituído pelo par chave-valor para o novo campo. Exemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parâmetros como pares de valor-chave {#parameters}

**Formato:**  `d_parameter=parameter_id`

    em que:
    
    * o parâmetro tem o prefixo &quot;&amp;&quot;
    
    * Parâmetro é substituído pelo par de valores chave para o novo campo
    
    Exemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos os tipos de pixel podem conter parâmetros adicionais, como *pares de valor-chave* para coletar características ou fornecer metadados de campanha (como um nome de inserção ou um nome de campanha) para outros relatórios. Um par de valor-chave consiste em dois elementos relacionados: um *key*, que é uma constante que define o conjunto de dados, e uma *value*, que é uma variável que pertence ao conjunto.

No par de valor principal, a variável de valor pode ser uma ID codificada ou uma *macro*, que é uma pequena unidade de código independente, substituída dinamicamente pelos valores correspondentes quando a tag de anúncio é carregada para rastreamento de campanha e usuário. Para parâmetros relacionados à campanha, é possível usar [Macros do DSP](/help/dsp/campaign-management/macros.md) em vez de macros de Audience Manager para enviar atributos de campanha junto com a impressão correspondente ou dados de cliques para o Audience Manager, usando um único pixel em todos os anúncios. As macros DSP inseridas nos pixels do evento devem ser valores apropriados para os pares de valores chave incluídos nos pixels. Por exemplo, para o `d_placement` , você usaria a macro DSP `${TM_PLACEMENT_ID_NUM}` como o valor para capturar IDs de posicionamento geradas pela macro Adobe Advertising.

Para obter uma lista de macros compatíveis com o Audience Manager para pixels de evento de impressão, consulte &quot;[Captura de dados de impressão da campanha via Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Para obter uma lista de macros compatíveis com o Audience Manager para pixels de evento de clique, consulte &quot;[Captura de dados de cliques da campanha via Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* A prática recomendada é incluir a campanha, a inserção, o criativo (anúncio) e as IDs do site para que você possa usar os atributos da campanha para criar características de Audience Manager.
>* Para criar relatórios de Audience Optimization, são necessários parâmetros adicionais.
>* Nos pares de valor-chave, substitua os valores pelos valores relevantes [Macros do DSP](/help/dsp/campaign-management/macros.md) assim, você pode usar um único pixel em todos os anúncios em todas as campanhas. Por exemplo, alterar `d_campaign=[%campaignID%]`para `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar IDs de campanha geradas pela macro Adobe Advertising.
>* Você pode criar seus próprios parâmetros com valores codificados, se necessário. Exemplo: `d_DSP=AdCloud`

Exemplo de um pixel de evento de impressão:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Onde adicionar os pixels

#### Pixel de rastreamento de impressão

Anexe um pixel de rastreamento de eventos de impressão a todos os anúncios em seu [!DNL DSP] campanhas. Você pode fazer isso em qualquer um dos seguintes locais:

* No nível de posicionamento, que aplica o pixel por padrão a todos os anúncios no posicionamento. Na seção Rastreamento das configurações de posicionamento, adicione o pixel no [[!UICONTROL Event pixels] campo](/help/dsp/campaign-management/placements/placement-settings.md).

* No nível do anúncio, que substitui quaisquer pixels de evento no nível de posicionamento. Nas configurações do anúncio, [criar um pixel de evento na [!UICONTROL Pixel] guia](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anúncios em um servidor de anúncios de terceiros) No nível do anúncio no servidor de anúncios.

#### Pixel de rastreamento de cliques

No servidor de publicidade, insira o pixel do evento de clique (com o URL codificado anexado) onde você normalmente insere o URL de click-through do anúncio.

## Etapa 3: Tarefas Pós-Implementação

Depois que as tags de evento forem implementadas, os dados fluirão para os servidores de coleta de dados do Audience Manager. Conclua as seguintes tarefas antes de usar os dados nos relatórios.

### Criar um [!DNL Amazon S3] Classificação e fonte de dados

Quando seus dados estiverem nos servidores Audience Manager, você deverá criar um [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) e, em seguida, uma fonte de dados, para a qual todos os dados de pixels são enviados. Entre em contato com seu consultor do Audience Manager ou [Atendimento ao cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) se precisar de suporte.

### Criar características e segmentos do Audience Manager

Seus dados do evento fluirão para o Audience Manager como [sinais não utilizados](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Criar manualmente [características com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) dos dados assimilados e, em seguida, crie [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) usando essas características, antes de poder usar os dados nos relatórios.

Exemplo de característica que preenche dados no nível do usuário para usuários expostos a um criativo específico no DSP:

1. Identificar o evento como `d_event = imp`.
1. Identifique a ID criativa na campanha de DSP e mapeie-a para a característica como `d_creative=[Creative ID]`.

![Tela de criação de característica](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macros do DSP](/help/dsp/campaign-management/macros.md)
>* [Visão geral do envio de dados de exposição da mídia DSP para o Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)
