---
title: Converter IDs de Usuário de  [!DNL Amperity]  em IDs Universais
description: Saiba como habilitar o DSP para assimilar seus [!DNL Amperity] segmentos primários.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Converter IDs de Usuário de [!DNL Amperity] em IDs Universais

*recurso do Beta*

Use a integração do DSP com a plataforma de dados do cliente [!DNL Amperity] para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público-alvo no DSP](#source-create).

1. [Preparar e compartilhar dados de mapeamento de segmento](#map-data).

1. [Solicitar um push de dados de [!DNL Amperity] para DSP](#push-data).

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

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com o usuário [!DNL Amperity].

## Etapa 3: Preparar e compartilhar dados de mapeamento de segmento {#map-data}

O anunciante deve preparar e compartilhar dados de mapeamento de segmento.

1. Em [!DNL Amperity], coloque as IDs de email da audiência em hash usando o algoritmo SHA -256.

1. O anunciante deve fornecer dados de mapeamento de segmento à Equipe de conta do Adobe para criar os segmentos no DSP. Use os seguintes nomes e valores de coluna em um arquivo de valores separados por vírgula:

   * **Chave de Segmento Externo:** A chave de segmento [!DNL Amperity] associada ao segmento.

   * **Nome do segmento:** O nome do segmento.

   * **Descrição do segmento:** A finalidade ou a regra do segmento, ou ambas.

   * **ID do Pai:** Manter em branco

   * **CPM de Vídeo:** 0

   * **Exibir CPM:** 0

   * **Janela de Segmento:** o tempo de vida do segmento.

## Etapa 4: solicitar um push de dados de [!DNL Amperity] para DSP {#push-data}

1. Depois que o segmento é mapeado no DSP, o anunciante deve trabalhar com o representante [!DNL Amperity] para distribuir os dados do segmento para DSP.

1. O anunciante deve confirmar com a equipe da conta do Adobe que os dados do segmento foram recebidos.

Os segmentos devem estar disponíveis no DSP em 24 horas. Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público-alvo a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está disponível e se está sendo preenchido.

Os segmentos serão atualizados conforme configurados para o anunciante em [!DNL Amperity]. Independentemente da frequência com que o segmento é atualizado, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos reenviando por push a partir de [!DNL Amperity] antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Etapa 5: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas.

Na biblioteca de público-alvo (que está disponível quando você cria ou edita um público-alvo a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento), compare o número de IDs universais com o número de endereços de email com hash originais. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
