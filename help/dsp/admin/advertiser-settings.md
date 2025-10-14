---
title: Configurações da conta do anunciante
description: Consulte descrições das configurações disponíveis do anunciante.
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Configurações da conta do anunciante

*Não disponível para usuários somente leitura*

<!-- Not published -->

## Configurações de [!UICONTROL General]

**[!UICONTROL Advertiser Name]:** O nome do anunciante.

**[!UICONTROL Category]:** A categoria na qual os negócios do anunciante operam. A categoria é comunicada aos editores quando você faz uma oferta no inventário. Escolha uma categoria que se alinhe aos seus anúncios, ou os editores poderão rejeitar seus anúncios.

>[!NOTE]
>
>Se você selecionar *[!UICONTROL Other]*, o anunciante não poderá acessar o DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** A página inicial do anunciante ou a URL do site principal (começando com `http://` ou `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Somente novas contas de anunciante) Disponibiliza ao anunciante todos os feeds privados do Exchange configurados para a conta DSP da organização.

### [!UICONTROL Adobe IMS IDs]

Os anunciantes com produtos adicionais da Adobe Experience Cloud podem compartilhar dados entre alguns produtos usando a ID exclusiva da organização para o Experience Cloud. Você pode configurar integrações específicas de produtos na seção [!UICONTROL Integrations].

**[!UICONTROL Account IMS org and ID]:** (anunciantes com produtos Experience Cloud adicionais que são licenciados por meio de uma conta da Experience Cloud com vários anunciantes; opcional) a ID da organização da Experience Cloud do anunciante.

**[!UICONTROL Advertiser IMS org and ID]:** (anunciantes com licenças diretas para produtos adicionais da Experience Cloud; opcional) a ID da organização da Experience Cloud do anunciante.

### [!UICONTROL Integrations]

(Opcional) Produtos adicionais da Experience Cloud vinculados à conta da DSP. Os produtos devem ser associados à mesma ID de organização da Experience Cloud fornecida na seção [!UICONTROL Adobe IMS IDs].

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Anunciantes com [!DNL Advertising Search, Social, & Commerce] ou que usam pixels de conversão de Adobe Advertising) Uma conta [!DNL Search, Social, & Commerce] com a qual a DSP troca dados de atribuição.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Anunciantes com Adobe Analytics; opcional; aplicável somente a dados coletados usando as marcas de rastreamento de conversão da Adobe Advertising que incluem um [!DNL EF Redirect] e somente um token) Um ou mais conjuntos de relatórios [!DNL Analytics] para os quais a DSP envia dados coletados de editores e parceiros do lado do suprimento. O Analytics também envia os dados coletados do site do cliente para o DSP.

Para que os dados sejam exibidos nos conjuntos de relatórios, a configuração apropriada no nível do anunciante do [!DNL Search, Social, & Commerce] deve estar habilitada. Além disso, a conta [!DNL Analytics] do anunciante deve ser configurada para receber dados do Adobe Advertising.

>[!WARNING]
>
>Se você remover um conjunto de relatórios vinculado anteriormente, o DSP não trocará mais dados com esse conjunto. Espere ver as flutuações de dados.

Para obter mais informações sobre a integração com [!DNL Analytics], consulte &quot;[Visão geral de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes com Adobe Audience Manager ou Adobe Analytics; opcional) uma conta do Audience Manager ou [!DNL Analytics] da qual o DSP obtém metadados de segmento, dados de hierarquia e dados de público-alvo exclusivos para todos os públicos-alvo do Adobe do anunciante. Isso inclui dados para:

* Segmentos do Audience Manager
* [!DNL Analytics] segmentos publicados no Adobe Experience Cloud
* Segmentos criados usando o Adobe Experience Cloud [!DNL Audience Library]
* Segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager

A sincronização inicial leva cerca de 24 horas. Depois disso, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## Configurações de [!UICONTROL Targeting]

Opcionalmente, é possível configurar destinos padrão para os novos posicionamentos do anunciante. Os usuários podem substituir os destinos padrão para qualquer novo posicionamento.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** O país padrão para o geolocalização de cada posicionamento. Os usuários podem alterar o país e configurar uma geolocalização mais específica para cada posicionamento.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Qualquer público ou segmento a ser suprimido por padrão. Os usuários podem alterar as exclusões de cada posicionamento.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Tipos de filtros contextuais [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] a serem aplicados. Você pode substituir as configurações no nível do anunciante no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário para direcionar por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo adulto para o qual os anúncios serão bloqueados por padrão: *[!UICONTROL Do Not Block]* (padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Alcohol Content]:** (Opcional) O grau de alcoolemia para o qual os anúncios devem ser bloqueados por padrão: *[!UICONTROL Do Not Block]* (padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Tipos de sites a serem bloqueados com base em tráfego fraudulento e atividades suspeitas medidas através de [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Você pode substituir as configurações no nível do anunciante no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Por padrão, bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos sequestrados, para novos posicionamentos. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia tráfego adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que fazem com que o DSP bloqueie anúncios por padrão: *[!UICONTROL Fraud]* (que bloqueia todos os sites com fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/ou *[!UICONTROL Fraud: Zero Ads]*. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia anúncios baseados em atividades suspeitas), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Taxas adicionais podem ser aplicadas.

#### [!UICONTROL Pre-Bid Viewability]

Filtros opcionais de visibilidade pré-oferta por [!DNL DoubleVerify] e [!DNL Integral Ad Science] para aplicar a posicionamentos. Os padrões no nível do anunciante são selecionados para novos posicionamentos. Você pode substituir as configurações no nível do anunciante no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Vídeo

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**. Com essa opção, selecione os critérios.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Com essa opção, selecione os critérios.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average player size composition is]**. Com essa opção, selecione os critérios.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Exibir

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Com essa opção, selecione os critérios.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Com essa opção, selecione os critérios.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Um filtro **[!UICONTROL Video Viewability Targets]** opcional e um filtro **[!UICONTROL Display Viewability Targets]** opcional. Taxas adicionais podem ser aplicadas.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Por padrão, qual nível de [[!DNL Ads.txt] filtragem pré-oferta](https://iabtechlab.com/ads-txt-about/) usar ao aproveitar cada lista [!DNL Authorized Digital Sellers] de editor:
* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar inventário de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: priorizar a compra de estoque dos revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o estoque somente de revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de vendedores diretos autorizados de um domínio.

Você pode substituir a configuração no nível do anunciante no [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Por padrão, habilita um filtro de pós-oferta em tempo real para garantir que os anúncios sejam veiculados nos sites para os quais o anunciante está direcionando. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] clientes somente; opcional) Uma ID de segmento [!DNL DoubleVerify Authentic Brand Safety] associada à conta [!DNL DoubleVerify] da organização para ser usada como padrão para todos os posicionamentos. Especificar uma ID bloqueia impressões pós-oferta usando as regras personalizadas de segurança da marca configuradas para a ID do segmento especificada. A DSP fatura sua conta pelo uso da ID de segmento.

A ID deve começar com &quot;51&quot; e consistir em oito dígitos. Você pode alterar ou excluir a ID no nível do anunciante no nível de posicionamento.

>[!MORELIKETHIS]
>
>* [Criar uma Conta de Anunciante](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
