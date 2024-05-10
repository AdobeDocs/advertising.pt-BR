---
title: Configurações da conta do anunciante
description: Consulte descrições das configurações disponíveis do anunciante.
role: User, Admin
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Configurações da conta do anunciante

*Não disponível para usuários somente leitura*

## [!UICONTROL General] Configurações

**[!UICONTROL Advertiser Name]:** O nome do anunciante.

**[!UICONTROL Category]:** A categoria em que o negócio do anunciante opera. A categoria é comunicada aos editores quando você faz uma oferta no inventário. Escolha uma categoria que se alinhe aos seus anúncios, ou os editores poderão rejeitar seus anúncios.

>[!NOTE]
>
>Se você selecionar *[!UICONTROL Other]*, o anunciante não poderá acessar o DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** A página inicial do anunciante ou o URL do site principal (começando com `http://` ou `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Somente novas contas de anunciante) Disponibiliza ao anunciante todos os feeds de troca privados configurados para a conta DSP da organização.

### [!UICONTROL Adobe IMS IDs]

Os anunciantes com produtos adicionais da Adobe Experience Cloud podem compartilhar dados entre alguns produtos usando a ID exclusiva da organização para o Experience Cloud. É possível configurar integrações específicas de produtos no [!UICONTROL Integrations] seção.

**[!UICONTROL Account IMS org and ID]:** (Anunciantes com produtos de Experience Cloud adicionais que são licenciados por meio de uma conta Experience Cloud com vários anunciantes; opcional) A ID de organização da Experience Cloud do anunciante.

**[!UICONTROL Advertiser IMS org and ID]:** (Anunciantes com licenças diretas para produtos de Experience Cloud adicionais; opcional) A ID da organização de Experience Cloud do anunciante.

### [!UICONTROL Integrations]

(Opcional) Produtos de Experience Cloud adicionais vinculados à conta DSP. Os produtos devem ser associados à mesma ID de organização de Experience Cloud fornecida no [!UICONTROL Adobe IMS IDs] seção.

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Anunciantes com [!DNL Advertising Search, Social, & Commerce] ou que usam pixels de conversão de Adobe Advertising) A [!DNL Search, Social, & Commerce] conta com a qual o DSP troca dados de atribuição.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Anunciantes com Adobe Analytics; opcional; aplicável somente aos dados coletados usando tags de rastreamento de conversão de Adobe Advertising que incluem uma [!DNL EF Redirect] e somente token) Um ou mais [!DNL Analytics] conjuntos de relatórios para os quais o DSP envia dados coletados de editores e parceiros do lado do suprimento. O Analytics também envia os dados coletados do site do cliente para o DSP.

Para que os dados apareçam nos conjuntos de relatórios, as [!DNL Search, Social, & Commerce] a configuração no nível do anunciante deve estar ativada. Além disso, o [!DNL Analytics] a conta deve ser configurada para receber dados do Adobe Advertising.

>[!WARNING]
>
>Se você remover um conjunto de relatórios vinculado anteriormente, o DSP não trocará mais dados com esse conjunto. Espere ver as flutuações de dados.

Para obter mais informações sobre a integração com o [!DNL Analytics], consulte &quot;[Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes com Adobe Audience Manager ou Adobe Analytics; opcional) Um Audience Manager ou [!DNL Analytics] conta da qual o DSP extrai metadados de segmento, dados de hierarquia e dados exclusivos de público-alvo para todos os públicos-alvo Adobe do anunciante. Isso inclui dados para:

* segmentos Audience Manager
* [!DNL Analytics] segmentos publicados no Adobe Experience Cloud
* Segmentos criados usando a Adobe Experience Cloud [!DNL Audience Library]
* Segmentos criados no Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager

A sincronização inicial leva cerca de 24 horas. Depois disso, os dados são sincronizados em tempo real, com um atraso de um a dois segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Configurações

Opcionalmente, é possível configurar destinos padrão para os novos posicionamentos do anunciante. Os usuários podem substituir os destinos padrão para qualquer novo posicionamento.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** O país padrão para cada geolocalização de posicionamento. Os usuários podem alterar o país e configurar uma geolocalização mais específica para cada posicionamento.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Quaisquer públicos ou segmentos a serem suprimidos por padrão. Os usuários podem alterar as exclusões de cada posicionamento.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39] filtros contextuais a serem aplicados. É possível substituir as configurações no nível do anunciante na [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário para segmentar por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo para adultos para o qual os anúncios devem ser bloqueados por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Alcohol Content]:** (Opcional) O grau de teor de álcool para o qual os anúncios são bloqueados por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipos de sites a serem bloqueados com base em tráfego fraudulento e atividades suspeitas medidas por [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39]. É possível substituir as configurações no nível do anunciante na [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Por padrão, o bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos sequestrados, para novos posicionamentos. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que faz com que o DSP bloqueie anúncios por padrão:  *[!UICONTROL None]* (o padrão, que não bloqueia o tráfego adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que fazem com que o DSP bloqueie anúncios por padrão: *[!UICONTROL Fraud]* (que bloqueia todos os sites com fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, e/ou *[!UICONTROL Fraud: Zero Ads]*. Taxas adicionais podem ser aplicadas.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia anúncios com base em atividades suspeitas), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Taxas adicionais podem ser aplicadas.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Por padrão, que nível de [[!DNL Ads.txt] filtragem pré-oferta](https://iabtechlab.com/ads-txt-about/) para usar aproveitando o de cada editor [!DNL Authorized Digital Sellers] lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar o inventário de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar a compra de estoque dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de vendedores diretos autorizados de um domínio.

É possível substituir a configuração no nível do anunciante na [nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Por padrão, o ativa um filtro de pós-oferta em tempo real para garantir que os anúncios sejam veiculados nos sites que o anunciante está direcionando. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] somente clientes; opcional) A ID do segmento de segurança da marca associada à [!DNL DoubleVerify] conta.

**[!UICONTROL Enable Authentic Brand Safety]:** (Opcional) Por padrão, ativa [!DNL DoubleVerify] Segurança de marca autêntica, que bloqueia impressões pós-oferta usando as regras personalizadas de segurança de marca configuradas para a ID de segmento especificada. O DSP fatura sua conta pelo uso da ID do segmento.

Você pode substituir a configuração no nível do anunciante no nível de posicionamento.

>[!MORELIKETHIS]
>
>* [Criar uma conta do anunciante](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
