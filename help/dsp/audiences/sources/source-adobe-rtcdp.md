---
title: Fluxo de trabalho para usar a integração do DSP com o [!DNL Adobe] [!DNL Real-time CDP]
description: Saiba como habilitar o DSP para assimilar seus [!DNL Adobe] [!DNL Real-time CDP] segmentos primários.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Fluxo de trabalho para usar a integração do DSP com o [!DNL Adobe Real-Time CDP]

1. [Permitir que o DSP traduza segmentos de dados do cliente em [!DNL LiveRamp RampIDs]](source-universal-id.md) que são reconhecíveis em um ambiente licitável.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Criar uma fonte de público-alvo](source-create.md) para importar públicos para sua conta DSP ou uma conta de anunciante.

1. No Experience Platform, configure uma conexão de destino DSP de publicidade usando o [!UICONTROL Source Key] que foi gerado nas configurações da fonte DSP.

   Para obter instruções sobre como ativar a conexão de destino DSP, selecionar segmentos e acessar permissões de controle, consulte &quot;[Conexão com o Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Para obter suporte adicional, entre em contato com a equipe da conta Adobe ou `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Ativar segmentos autenticados de parceiros de ID universal](source-universal-id.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Fluxo de trabalho para usar a integração do DSP com o [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
