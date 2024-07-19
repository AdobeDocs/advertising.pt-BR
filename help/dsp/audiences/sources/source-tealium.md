---
title: Converter IDs de Usuário de  [!DNL Tealium]  em IDs Universais
description: Saiba como habilitar o DSP para assimilar seus [!DNL Tealium] segmentos primários.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Converter IDs de Usuário de [!DNL Tealium] em IDs Universais

*recurso do Beta*

Use a integração do DSP com a plataforma de dados do cliente [!DNL Tealium] para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada. O processo usa o conector de firehose do [!DNL Amazon Web Services] (AWS). Siga estas etapas para compartilhar dados do Tealium com o DSP:

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público-alvo no DSP](#source-create).

1. [Preparar e compartilhar dados de mapeamento de segmento](#map-data).

1. [Criar conectores em [!DNL Tealium] para compartilhar dados de segmento](#tealium-connector).

1. [Duplique o conector existente em [!DNL Tealium] para continuar a compartilhar segmentos](#duplicate-connector).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

## Etapa 1: configurar o rastreamento da medição de [!DNL Analytics] {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se ainda não tiver feito isso) Conclua todos os [pré-requisitos para implementação [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e verifique se a [ID do AMO e a EF ID](/help/integrations/analytics/ids.md) estão sendo preenchidas nas URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** você deve implantar uma marca JavaScript adicional em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e para dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que lhe dará instruções para se registrar para uma tag [!DNL LiveRamp] [!DNL LaunchPad] das Soluções de tráfego de autenticação [!DNL LiveRamp]. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Crie uma fonte de público-alvo](source-manage.md) para importar públicos-alvo para sua conta DSP ou para uma conta de anunciante. Você pode optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para preparar os dados de mapeamento de segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com o usuário [!DNL Tealium].

## Etapa 3: Preparar e compartilhar dados de mapeamento de segmento {#map-data}

O anunciante deve preparar e compartilhar dados de mapeamento de segmento.

1. O anunciante deve preparar os dados em [!DNL Tealium]:

   1. Coloque as IDs de email em hash para o público-alvo do anunciante usando o algoritmo SHA -256.

   1. Mapeie a coluna que contém IDs de email com hash para o atributo do tipo de ID de visitante.

   1. Crie o público com o atributo `Tealium_visitor_id`. Aplique o enriquecimento correto para acionar o público-alvo. Consulte a [[!DNL Tealium] documentação sobre atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. O anunciante deve fornecer dados de mapeamento de segmento à Equipe de conta do Adobe para criar os segmentos no DSP. Use os seguintes nomes e valores de coluna em um arquivo de valores separados por vírgula:

   * **Chave de Segmento Externo:** A chave de segmento externo, que você especificará posteriormente nas configurações de ação do conector em [!DNL Tealium]. A convenção de nomenclatura recomendada é &quot;`<DSP source key>_<Tealium segment name>`&quot;, como &quot;57bf424dc10_coffee-drinkers&quot;. Para a chave de origem do DSP, use o [!UICONTROL Source Key] das configurações de origem do público-alvo do DSP.

   * **Nome do segmento:** O nome do segmento.

   * **Descrição do segmento:** A finalidade ou a regra do segmento, ou ambas.

   * **ID do Pai:** Manter em branco

   * **CPM de Vídeo:** 0

   * **Exibir CPM:** 0

   * **Janela de Segmento:** o tempo de vida do segmento.

## Etapa 4: criar conectores em [!DNL Tealium] para compartilhar dados de segmento {#tealium-connector}

Para cada segmento que você deseja compartilhar, crie um conector separado para cada ação que aciona alterações de dados. Por exemplo, para compartilhar dois segmentos com dois acionadores, crie quatro conectores.

1. A Equipe de conta do Adobe fornece ao anunciante as credenciais do conector firehose do AWS.

1. Em [!DNL Tealium], [adicione um conector](https://docs.tealium.com/server-side/connectors/add/), usando estas opções:

   1. Selecione o conector [!DNL AWS Firehose].

   1. Nas configurações de origem:

      1. Selecione o segmento de público-alvo a ser compartilhado.

      1. Configurar um acionador:

         * Para o primeiro conector do segmento, selecione o acionador `Joined Audience`. Isso garante que os dados sejam compartilhados com DSP sempre que um usuário ingressar em um segmento.

         * Para o segundo conector do segmento, selecione o acionador `Left Audience`. Esse conector é usado para lidar com todos os cancelamentos e usuários que deixam o segmento no DSP.

   1. Nas configurações, especifique o conector de firehose do AWS. Se você ainda não tiver adicionado o conector do firehose para DSP, adicione um conector do firehose usando as seguintes informações:

      * **Nome:** O nome do conector.

      * **Chave de Acesso:** A chave de acesso fornecida pela Equipe de Conta do Adobe.

      * **Chave secreta:** A chave secreta fornecida pela Equipe de Conta do Adobe.

      * **Região:** Leste EUA e Virgínia do Norte (us-east-1)

   1. Nas configurações de ação, faça o seguinte:

      1. Crie uma ação &quot;Enviar dados do cliente para fluxo do delivery (avançado)&quot; para adicionar dados ao segmento, usando as seguintes informações:

         * **Nome da Ação:** O nome da ação.

         * **Tipo de Ação:** Enviar Dados do Cliente para Fluxo de Entrega (Avançado)

         * **Fluxo de Entrega:** Tealium_CDP_Connector

         * **Dados da Mensagem:** Faça o seguinte:

            1. Escolha um atributo para o segmento:

               * Para o atributo Hash_Email, nomeie a mensagem personalizada `hashed_email`.

               * Para o atributo Cookies, nomeie a mensagem personalizada `cookies`.

            1. Na opção para criar um campo personalizado, no campo [!DNL Source Key], insira o [!UICONTROL External Segment Key] que foi incluído nos [dados de mapeamento de segmento](#map-data) no procedimento anterior.

               O DSP usará essa chave para preencher seu segmento.

            1. (Recomendado) Crie uma ação de atualização para manter o segmento atualizado.

## Etapa 5: duplicar o conector existente em [!DNL Tealium] para continuar a compartilhar segmentos {#duplicate-connector}

Você pode ter apenas um conector por segmento e um segmento por conector.

1. Em [!DNL Tealium], duplique o segmento para o qual deseja criar outro segmento e renomeie o novo segmento.

1. Em [!DNL Tealium], duplique [o conector que você criou](#tealium-connector) no procedimento anterior e renomeie o novo conector de &quot;`<original name>-copy`&quot; para o novo nome de segmento.

## Etapa 6: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas.

Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está preenchendo e compare o número de IDs universais com o número de endereços de email com hash originais. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

Os segmentos são atualizados a cada 24 horas. No entanto, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos reenviando por push a partir de [!DNL Tealium] antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
