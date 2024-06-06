---
title: Converter IDs de usuário de [!DNL Optimizely] para Universal IDs
description: Saiba como habilitar o DSP para assimilar seus [!DNL Optimizely] segmentos primários.
feature: DSP Audiences
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL Optimizely] para Universal IDs

Use a integração do DSP com o [!DNL Optimizely] plataforma de dados do cliente para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurar o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público no DSP](#source-create).

1. [Preparar e enviar os dados do segmento para o [!DNL Optimizely Data Platform]](#push-data).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

Os segmentos devem estar disponíveis no DSP em 24 horas e são atualizados a cada 24 horas. **[Expectativas verdadeiras ou diferentes para Otimizely?]**

## Etapa 1: configurar o rastreamento do [!DNL Analytics] medição {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se você ainda não tiver feito isso) Conclua tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e certifique-se de que o [ID AMO e ID EF](/help/integrations/analytics/ids.md) estão sendo preenchidos nos URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** Você deve implantar uma tag JavaScript adicional em suas páginas da Web para corresponder às conversões das IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que fornecerá instruções para se registrar em um [!DNL LiveRamp] [!DNL LaunchPad] tag de [!DNL LiveRamp] Soluções de tráfego de autenticação. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante. É possível optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para enviar os dados do segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL Optimizely] usuário.

## Etapa 3: preparar e enviar os dados do segmento {#push-data}

O anunciante deve preparar e enviar os dados no [!DNL Optimizely Data Platform].  **[Eles estão usando a plataforma de dados otimizados?]**  <!-- Data Platform? -->

1. Coloque as IDs de email em hash para o público-alvo do anunciante usando o algoritmo SHA -256.

1. Encaminhar o segmento para DSP, incluindo os seguintes campos:

   **[Eles estão usando os serviços da Web da Plataforma de dados, outro tipo de API ou uma interface do usuário? Adicione um link às instruções. E onde eles vão inserir esses campos?]**  <!-- Are they using the Data Platform web services or what? Add a link to instructions. And where will they input these fields?  -->

   * **Chave de origem:** Esta é a chave de origem criada em [Etapa 2](#source-create).

   * **Código da conta:** Este é o código alfanumérico da conta DSP, que você pode encontrar dentro do DSP em [!UICONTROL Settings] > [!UICONTROL Account].

## Etapa 4: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Após concluir todas as etapas, verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) de que o segmento está disponível e está sendo preenchido em 24 horas. Compare o número de IDs universais com o número de endereços de email com hash originais.

A taxa de conversão de endereços de email com hash em IDs universais deve ser superior a 90%. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para mais de 90 IDs universais. Uma taxa de tradução de 90% ou menos é um problema. Para obter mais informações sobre como as contagens de segmentos podem variar, consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Os segmentos são atualizados a cada 24 horas. No entanto, a inclusão em um segmento expira após 30 dias para garantir a conformidade com a privacidade. Portanto, atualize os públicos-alvo enviando-os novamente do [!DNL Optimizely] a cada 30 dias ou menos.

Para obter suporte para solução de problemas, entre em contato com a equipe de conta da Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Converter IDs de usuário de [!DNL Adobe Real-Time CDP] para Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de usuário de [!DNL Tealium] para Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
