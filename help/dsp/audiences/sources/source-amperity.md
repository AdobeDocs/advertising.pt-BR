---
title: Converter IDs de usuário de [!DNL Amperity] para Universal IDs
description: Saiba como habilitar o DSP para assimilar seus [!DNL Amperity] segmentos primários.
feature: DSP Audiences
source-git-commit: 25bcc2eefa4dc7873ab8189122d43da336e3e046
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL Amperity] para Universal IDs

*Recurso beta*

Use a integração do DSP com o [!DNL Amperity] plataforma de dados do cliente para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurar o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público no DSP](#source-create).

1. [Preparar e compartilhar dados de mapeamento de segmento](#map-data).

1. [Solicitar um push de dados de [!DNL Amperity] para DSP](#push-data).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

## Etapa 1: configurar o rastreamento do [!DNL Analytics] medição {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se você ainda não tiver feito isso) Conclua tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e certifique-se de que o [ID AMO e ID EF](/help/integrations/analytics/ids.md) estão sendo preenchidos nos URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** Você deve implantar uma tag JavaScript adicional em suas páginas da Web para corresponder às conversões das IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que fornecerá instruções para se registrar em um [!DNL LiveRamp] [!DNL LaunchPad] tag de [!DNL LiveRamp] Soluções de tráfego de autenticação. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante. É possível optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para enviar os dados do segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL Amperity] usuário.

## Etapa 3: Preparar e compartilhar dados de mapeamento de segmento {#map-data}

O anunciante deve preparar e compartilhar dados de mapeamento de segmento.

1. Dentro de [!DNL Amperity], coloque as IDs de email em hash para o público-alvo usando o algoritmo SHA -256.

1. O anunciante deve fornecer dados de mapeamento de segmento à Equipe de conta do Adobe para criar os segmentos no DSP. Use os seguintes nomes e valores de coluna em um arquivo de valores separados por vírgula:

   * **Chave de segmento externo:** A variável [!DNL Amperity] chave de segmento associada ao segmento.

   * **Nome do segmento:** O nome do segmento.

   * **Descrição do segmento:** A finalidade ou a regra do segmento, ou ambas.

   * **ID do pai:** Manter em branco

   * **CPM de vídeo:** 0

   * **Exibir CPM:** 0

   * **Janela Segmento:** O tempo de vida do segmento.

## Etapa 4: solicitar um push de dados do [!DNL Amperity] para DSP {#push-data}

1. Depois que o segmento é mapeado no DSP, o anunciante deve trabalhar com seu [!DNL Amperity] representante para distribuir os dados do segmento ao DSP.

1. O anunciante deve confirmar com a equipe da conta do Adobe que os dados do segmento foram recebidos.

Os segmentos devem estar disponíveis no DSP em 24 horas e são atualizados conforme configurado para o anunciante no [!DNL Amperity]. Independentemente da frequência com que o segmento é atualizado, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos enviando novamente de [!DNL Amperity] antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Etapa 5: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Após concluir todas as etapas, verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) de que o segmento está disponível e está sendo preenchido em 24 horas. Compare o número de IDs universais com o número de endereços de email com hash originais.

A taxa de conversão de endereços de email com hash em IDs universais deve ser superior a 90%. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para mais de 90 IDs universais. Uma taxa de tradução de 90% ou menos é um problema. Para obter mais informações sobre como as contagens de segmentos podem variar, consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Para obter suporte para solução de problemas, entre em contato com a equipe de conta da Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
