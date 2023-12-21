---
title: Sobre a ativação de segmentos autenticados de fontes de público-alvo
description: Saiba mais sobre como assimilar segmentos primários de uma plataforma de dados do cliente.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: e3e8753db31bc835c49eb2037fdcd7696a895a8c
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Sobre a ativação de segmentos autenticados de fontes de público-alvo

O DSP pode assimilar segmentos primários compostos de IDs de email com hash ou IDs universais criadas em uma CDP (Plataforma de dados do cliente). Você pode usar os segmentos assimilados como destinos de suas inserções.

As CDPs a seguir estabeleceram conectores, mas o DSP também pode se conectar a qualquer CDP usando lote, transmissão ou compartilhamento de dados baseado em API. Para integrar com uma nova CDP, entre em contato com a equipe de conta da Adobe.

## [!DNL Adobe Real-Time Customer Data Platform]

O DSP é integrado ao [o [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), que faz parte do Adobe Experience Platform.

Entrada [!DNL Real-Time CDP], *destinos* são conexões com plataformas de dados externas que permitem ativação de dados contínua. Por exemplo, você pode usar destinos para ativar seus relacionamentos de cliente conhecidos (como endereços de email com hash) para publicidade direcionada em formatos digitais suportados pelo DSP. Para obter mais informações sobre destinos, consulte a Experience Platform [Guia de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluindo uma visão geral do produto, instruções para [criação de espaços de trabalho de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [criação de conexões de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), e [ativação de dados para destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Consulte &quot;[Fluxo de trabalho para usar a integração do DSP com o [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

## [!DNL ActionIQ]

Você pode compartilhar os dados primários de sua organização na [!DNL Action IQ] plataforma de dados do cliente com DSP. Em seguida, é possível direcionar os posicionamentos do DSP para os segmentos usando [!DNL RampIDs] ou [!DNL Unified IDs 2.0].

Essa integração requer personalização. Entre em contato com a equipe de conta do Adobe para obter mais informações.

## [!DNL Tealium]

Você pode compartilhar os dados primários de sua organização na [!DNL Tealium] plataforma de dados do cliente usando [!DNL Amazon Web Services]. Em seguida, é possível direcionar os posicionamentos do DSP para os segmentos usando [!DNL RampIDs]. Consulte &quot;[Fluxo de trabalho para usar a integração do DSP com o [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Fluxo de trabalho para usar a integração do DSP com o [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Fluxo de trabalho para usar a integração do DSP com o [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
