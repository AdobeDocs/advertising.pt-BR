---
title: Converter IDs de usuários de [!DNL Optimizely] IDs universais
description: Aprenda a habilitar DSP para assimilar seus [!DNL Optimizely] segmentos primários.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Converter IDs de usuários de [!DNL Optimizely] IDs universais

*recurso de beta*

Use the DSP integration with the [!DNL Optimizely] customer data platform to convert your organization&#39;s first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and push the segment data](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email ou [!DNL RampIDs] [!DNL ID5] IDs, faça o seguinte:

1. (Caso ainda não tenha feito) Todos os Apps todos os [pré-requisitos para a implementação [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e verifique se a ID do AMO e a [ID](/help/integrations/analytics/ids.md) de EF estão sendo preenchidas nos URLs rastreamento.

1. Registre-se com o parceiro de ID universal e implantar código específico da ID universal em suas páginas da Web para corresponder às conversões das IDs em navegadores de desktop e da Web móvel (mas não aplicativos móveis) para visualização-throughs:

   * **Para [!DNL RampIDs]:** você deve implantar uma JavaScript tag adicional em suas páginas da Web para corresponder às conversões das IDs em desktop e navegadores móveis da Web (mas não aplicativos móveis) para visualização-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you&#39;ll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Optimizely] user.

## Etapa 3: preparar e enviar os dados segmento {#push-data}

A anunciante deve preparar e enviar os dados com a ajuda de seu [!DNL Optimizely] representante.

1. Dentro disso [!DNL Optimizely Data Platform], hash as IDs de email do público-alvo do anunciante usando o algoritmo SHA-256.

1. Siga as instruções para [[!DNL Optimizely's] encaminhar o segmento para DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inclua as seguintes informações para ativar a integração:

   * **Source Key:** This is the source key created in [Step 2](#source-create).

   * **Account Code:** This is the alphanumeric DSP Account Code, which you can find within DSP at [!UICONTROL Settings] > [!UICONTROL Account].

The segments should be available in DSP within 24 hours and are refreshed as configured for the advertiser. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Optimizely] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Step 4: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

Depois de concluir todas as etapas, verifique na biblioteca de público-alvo (que está disponível ao criar ou editar uma público-alvo a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas posicionamento configurações) se a segmento está disponível e está sendo preenchida dentro de 24 horas. Compare the number of universal IDs with the number of original hashed email addresses.

A taxa de tradução dos endereços de email com hash para IDs universais deve ser maior que 90%. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para mais de 90 IDs universais. Uma taxa de tradução de 90% ou menos é um problema. Para obter mais informações sobre como as contagens de segmento podem variar, consulte &quot;[Causas de variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

Para solucionar problemas de suporte, entre em contato com seu Adobe Systems equipe de conta ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
