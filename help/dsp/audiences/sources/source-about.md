---
title: Sobre a ativação de segmentos autenticados de fontes de público-alvo
description: Saiba mais sobre como assimilar segmentos primários de uma plataforma de dados do cliente.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 68095fc77659826fae43f2453d17022ef1880807
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# Sobre a ativação de segmentos autenticados de fontes de público-alvo

<!-- Doesn't specifically explain what you can do in our UI -->

O DSP pode assimilar segmentos primários compostos de sinais autenticados criados em uma CDP (Plataforma de dados do cliente). Você pode usar os segmentos assimilados como destinos de suas inserções.

## [!DNL Adobe Real-Time Customer Data Profile]

O DSP está integrado ao [o [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), que faz parte do Adobe Experience Platform.

Entrada [!DNL Real-time CDP], *destinos* são conexões com plataformas de dados externas que permitem ativação de dados contínua. Por exemplo, você pode usar destinos para ativar seus relacionamentos de cliente conhecidos (como endereços de email com hash) para publicidade direcionada em formatos digitais suportados pelo DSP.

Para obter mais informações sobre destinos, consulte a Experience Platform [Guia de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluindo uma visão geral do produto, instruções para [criação de espaços de trabalho de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [criação de conexões de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), e [ativação de dados para destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Fluxo de trabalho para usar a integração do DSP com o [!DNL Real-time CDP] {#workflow-sources}

1. [Permitir que o DSP traduza segmentos de dados do cliente em [!DNL LiveRamp RampIDs]](source-durable-id.md) que são reconhecíveis em um ambiente licitável.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Criar uma fonte de público-alvo](source-create.md) para importar públicos para sua conta DSP ou uma conta de anunciante.

1. [Configurar um [!DNL Real-Time CDP] conexão de destino no Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Para obter suporte adicional, entre em contato com a equipe da conta Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Ativar segmentos autenticados de parceiros de ID durável](source-durable-id.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Conexão de publicidade do Adobe DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

