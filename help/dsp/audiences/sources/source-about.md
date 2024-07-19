---
title: Sobre fontes de público-alvo primárias
description: Saiba mais sobre como converter outros identificadores de usuário em seus segmentos primários em IDs universais para direcionamento sem cookies.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 78ee6ddbfb87915475bcf84bd7cd405a58eccf14
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Sobre fontes de público-alvo primárias

*recurso do Beta*

O DSP pode assimilar segmentos primários compostos de IDs de email com hash criadas na CDP (Plataforma de dados do cliente) e convertê-los em segmentos compostos de IDs universais. Cada ID resultante é baseada em pessoas, e limites de frequência de anúncio são aplicados no nível de ID<!-- Move that info. to somewhere else? -->.

Os detalhes do segmento incluem o tamanho de cada tipo de ID universal, bem como o tamanho de cada tipo de dispositivo rastreado por cookies ou IDs de dispositivo.

## Tipos de ID universal {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Você pode traduzir segmentos primários para segmentos com IDs autenticadas (determinísticas) dos seguintes parceiros de ID universal.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Para redirecionar usuários conectados.

     [!DNL RampIDs] estão disponíveis para usuários na América do Norte, Austrália e Nova Zelândia.

     As taxas são de US$ 0,15 por impressão de anúncio de exibição entregue e US$ 0,25 por impressão de anúncio de vídeo entregue.

   * Para medição usando [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com):

   * Para redirecionar usuários conectados.

     [!DNL UID2 IDs] não está disponível para usuários no Espaço Econômico Europeu e em alguns outros países. Consulte a [lista de países proibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     As taxas são de US$ 0,15 por impressão de anúncio de exibição entregue e US$ 0,25 por impressão de anúncio de vídeo entregue.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Plataformas de dados do cliente compatíveis com segmentos primários

O DSP estabeleceu conectores para as seguintes CDPs para assimilar rapidamente seus segmentos primários.

O DSP também pode se conectar a qualquer CDP adicional usando compartilhamento de dados em lote, transmissão ou API. Para integrar com uma nova CDP, entre em contato com a equipe de conta da Adobe.

### [!DNL Adobe Real-Time Customer Data Platform]

O DSP é um *destino* integrado para [o [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), que faz parte da Adobe Experience Platform.

No [!DNL Real-Time CDP], os destinos são conexões com plataformas de dados externas que permitem ativação de dados sem interrupção. Você pode usar destinos para ativar seus endereços de email com hash para publicidade direcionada no DSP. Para obter mais informações sobre destinos, consulte o Experience Platform [Guia de Destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluindo uma visão geral do produto, instruções para [criar espaços de trabalho de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [criar conexões de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) e [ativar dados para destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Para permitir que o DSP assimile seus segmentos primários do [!DNL Adobe] [!DNL Real-time CDP] e converta seus endereços de email com hash em IDs universais, consulte &quot;[Converter IDs de usuários do [!DNL Adobe Real-Time CDP] em IDs universais](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL ActionIQ]

Você pode compartilhar os dados primários de sua organização da plataforma de dados do cliente [!DNL ActionIQ] com o DSP para converter seus endereços de email com hash em IDs universais para publicidade direcionada no DSP. Essa integração requer personalização. Entre em contato com a equipe de conta do Adobe para obter mais informações.

### [!DNL Amperity]

Você pode compartilhar os dados primários de sua organização da plataforma de dados do cliente [!DNL Amperity] com o DSP para converter seus endereços de email com hash em IDs universais para publicidade direcionada no DSP. Para obter mais informações, consulte &quot;[Converter IDs de usuário de [!DNL Amperity] em IDs universais](/help/dsp/audiences/sources/source-amperity.md).&quot;

### [!DNL Optimizely]

Você pode compartilhar os dados primários de sua organização da plataforma de dados do cliente [!DNL Optimizely] com o DSP para converter seus endereços de email com hash em IDs universais para publicidade direcionada no DSP. Para obter mais informações, consulte &quot;[Converter IDs de usuário de [!DNL Optimizely] em IDs universais](/help/dsp/audiences/sources/source-optimizely.md).&quot;

### [!DNL Tealium]

Você pode compartilhar os dados primários da sua organização na plataforma de dados do cliente [!DNL Tealium] usando o [!DNL Amazon Web Services]. Para obter mais informações sobre como converter seus endereços de email com hash em IDs universais para publicidade direcionada em DSP, consulte &quot;[Converter IDs de usuário de [!DNL Tealium] em IDs universais](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Converter IDs de Usuário de [!DNL Adobe Real-Time CDP] em IDs Universais](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de Usuário de [!DNL Amperity] em IDs Universais](/help/dsp/audiences/sources/source-amperity.md)
>* [Converter IDs de Usuário de [!DNL Optimizely] em IDs Universais](/help/dsp/audiences/sources/source-optimizely.md)
>* [Converter IDs de Usuário de [!DNL Tealium] em IDs Universais](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
