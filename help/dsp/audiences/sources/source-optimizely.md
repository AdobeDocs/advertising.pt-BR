---
title: Converter IDs de Usuário de  [!DNL Optimizely]  em IDs Universais
description: Saiba como habilitar o DSP para assimilar seus [!DNL Optimizely] segmentos primários.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Converter IDs de Usuário de [!DNL Optimizely] em IDs Universais

*recurso do Beta*

Use a integração do DSP com a plataforma de dados do cliente [!DNL Optimizely] para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público-alvo no DSP](#source-create).

1. [Preparar e enviar os dados do segmento](#push-data).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

## Etapa 1: configurar o rastreamento da medição de [!DNL Analytics] {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se ainda não tiver feito isso) Conclua todos os [pré-requisitos para implementação [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e verifique se a [ID do AMO e a EF ID](/help/integrations/analytics/ids.md) estão sendo preenchidas nas URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** você deve implantar uma marca JavaScript adicional em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e para dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que lhe dará instruções para se registrar para uma tag [!DNL LiveRamp] [!DNL LaunchPad] das Soluções de tráfego de autenticação [!DNL LiveRamp]. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Crie uma fonte de público-alvo](source-manage.md) para importar públicos-alvo para sua conta DSP ou para uma conta de anunciante. Você pode optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para enviar os dados do segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com o usuário [!DNL Optimizely].

## Etapa 3: preparar e enviar os dados do segmento {#push-data}

O anunciante deve preparar e enviar os dados usando o [!DNL Optimizely Data Platform]. Em caso de dúvidas sobre o processo, contate o representante do [!DNL Optimizely].

1. Em [!DNL Optimizely Data Platform], coloque as IDs de email da audiência em hash usando o algoritmo SHA -256.

1. Siga as [[!DNL Optimizely's] instruções de para encaminhar o segmento para DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Inclua as seguintes informações para habilitar a integração:

   * **Chave do Source:** Esta é a chave de origem criada em [Etapa 2](#source-create).

   * **Código da Conta:** Este é o Código da Conta DSP alfanumérico, que você pode encontrar dentro do DSP em [!UICONTROL Settings] > [!UICONTROL Account].

Os segmentos serão atualizados conforme configurados para o anunciante. Independentemente da frequência com que o segmento é atualizado, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos reenviando por push a partir de [!DNL Optimizely] antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Etapa 4: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas.

Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está disponível e preenchendo, e compare o número de IDs universais com o número de endereços de email com hash originais. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
