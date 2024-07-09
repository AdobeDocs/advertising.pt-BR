---
title: Converter IDs de usuário de [!DNL Optimizely] para Universal IDs
description: Saiba como habilitar o DSP para assimilar seus [!DNL Optimizely] segmentos primários.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 49902a99b78f867dd71c0cd15b97342a70abbc97
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL Optimizely] para Universal IDs

*Recurso do Beta*

Use a integração do DSP com o [!DNL Optimizely] plataforma de dados do cliente para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurar o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público no DSP](#source-create).

1. [Preparar e enviar os dados do segmento](#push-data).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

## Etapa 1: configurar o rastreamento do [!DNL Analytics] medição {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se você ainda não tiver feito isso) Conclua tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e certifique-se de que o [ID AMO e ID EF](/help/integrations/analytics/ids.md) estão sendo preenchidos nos URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** Você deve implantar uma tag JavaScript adicional em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que fornecerá instruções para se registrar em um [!DNL LiveRamp] [!DNL LaunchPad] tag de [!DNL LiveRamp] Soluções de tráfego de autenticação. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante. É possível optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para enviar os dados do segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL Optimizely] usuário.

## Etapa 3: preparar e enviar os dados do segmento {#push-data}

O anunciante deve preparar e enviar os dados usando o [!DNL Optimizely Data Platform]. Em caso de dúvidas sobre o processo, entre em contato com [!DNL Optimizely] representante.

1. Dentro de [!DNL Optimizely Data Platform], coloque as IDs de email em hash para o público-alvo usando o algoritmo SHA -256.

1. Seguir [[!DNL Optimizely's] instruções para encaminhar o segmento para DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inclua as seguintes informações para habilitar a integração:

   * **Chave do Source:** Esta é a chave de origem criada em [Etapa 2](#source-create).

   * **Código da conta:** Este é o código alfanumérico da conta DSP, que você pode encontrar dentro do DSP em [!UICONTROL Settings] > [!UICONTROL Account].

Os segmentos serão atualizados conforme configurados para o anunciante. Independentemente da frequência com que o segmento é atualizado, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos enviando novamente de [!DNL Optimizely] antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Etapa 4: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas.

Verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que o segmento está disponível e preenchendo, e compare o número de IDs universais com o número de endereços de email com hash originais.

A taxa de conversão de endereços de email com hash para IDs universais deve ser maior que 90%; a taxa de conversão para [!DNL RampIDs] em particular, deve ser de 95% se todos os endereços de email com hash forem exclusivos. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para pelo menos 95 [!DNL RampIDs] ou mais de 90 outros tipos de IDs universais. Uma taxa de tradução mais baixa é um problema. Para obter mais informações sobre como as contagens de segmentos podem variar, consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Para obter suporte para solução de problemas, entre em contato com a equipe de conta da Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
