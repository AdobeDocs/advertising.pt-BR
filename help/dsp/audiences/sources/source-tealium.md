---
title: Converter IDs de usuário de [!DNL Tealium] para Universal IDs
description: Saiba como habilitar o DSP para assimilar seus [!DNL Tealium] segmentos primários.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 606e721d80f30fa3a3546a14f0f876f4338dd30c
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL Tealium] para Universal IDs

*Recurso beta*

Use a integração do DSP com o [!DNL Tealium] plataforma de dados do cliente para converter os endereços de email com hash primários da sua organização em IDs universais para publicidade direcionada. O processo usa o [!DNL Amazon Web Services] Conector de mangueira de incêndio do (AWS). Siga estas etapas para compartilhar dados do Tealium com o DSP:

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurar o rastreamento para habilitar [!DNL Analytics] medição](#analytics-tracking).

1. [Criar uma fonte de público no DSP](#source-create).

1. [Preparar e compartilhar dados de mapeamento de segmento](#map-data).

1. [Criar conectores no [!DNL Tealium] para compartilhar dados de segmento](#tealium-connector).

1. [Duplicação do conector existente no [!DNL Tealium] para continuar a compartilhar segmentos](#duplicate-connector).

1. [Comparar o número de IDs universais com o número de endereços de email com hash](#compare-id-count).

Os segmentos devem estar disponíveis no DSP em 24 horas e são atualizados a cada 24 horas.

## Etapa 1: configurar o rastreamento do [!DNL Analytics] medição {#analytics-tracking}

*Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para converter endereços de email em [!DNL RampIDs] ou [!DNL ID5] IDs, você deve fazer o seguinte:

1. (Se você ainda não tiver feito isso) Conclua tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e certifique-se de que o [ID AMO e ID EF](/help/integrations/analytics/ids.md) estão sendo preenchidos nos URLs de rastreamento.

1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

   * **Para [!DNL RampIDs]:** Você deve implantar uma tag JavaScript adicional em suas páginas da Web para corresponder às conversões das IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que fornecerá instruções para se registrar em um [!DNL LiveRamp] [!DNL LaunchPad] tag de [!DNL LiveRamp] Soluções de tráfego de autenticação. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

## Etapa 2: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-create.md) para importar públicos para sua conta DSP ou uma conta de anunciante. É possível optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará para preparar os dados de mapeamento de segmento.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL Tealium] usuário.

## Etapa 3: Preparar e compartilhar dados de mapeamento de segmento {#map-data}

1. O anunciante deve preparar e compartilhar dados de mapeamento de segmento:

   1. O anunciante deve preparar os dados no [!DNL Tealium]:

      1. Coloque as IDs de email em hash para o público-alvo do anunciante usando o algoritmo SHA -256.

      1. Mapeie a coluna que contém IDs de email com hash para o atributo do tipo de ID de visitante.

      1. Crie o público-alvo com o `Tealium_visitor_id` atributo. Aplique o enriquecimento correto para acionar o público-alvo. Consulte a [[!DNL Tealium] documentação sobre atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. O anunciante deve fornecer dados de mapeamento de segmento à Equipe de conta do Adobe para criar os segmentos no DSP. Use os seguintes nomes e valores de coluna em um arquivo de valores separados por vírgula:

      * **Chave de segmento externo:** A chave do segmento externo, que você especificará posteriormente nas configurações de ação do conector em [!DNL Tealium]. A convenção de nomenclatura recomendada é &quot;`<DSP source key>_<Tealium segment name>`,&quot; como &quot;57bf424dc10_coffee-drinkers.&quot; Para a chave de origem do DSP, use o [!UICONTROL Source Key] nas configurações de fonte de público-alvo do DSP.

      * **Nome do segmento:** O nome do segmento.

      * **Descrição do segmento:** A finalidade ou a regra do segmento, ou ambas.

      * **ID do pai:** Manter em branco

      * **CPM de vídeo:** 0

      * **Exibir CPM:** 0

      * **Janela Segmento:** O tempo de vida do segmento.

## Etapa 4: Criar conectores no [!DNL Tealium] para compartilhar dados de segmento {#tealium-connector}

Para cada segmento que você deseja compartilhar, crie um conector separado para cada ação que aciona alterações de dados. Por exemplo, para compartilhar dois segmentos com dois acionadores, crie quatro conectores.

1. A Equipe de conta do Adobe fornece ao anunciante as credenciais do conector firehose do AWS.

1. Entrada [!DNL Tealium], [adicionar um conector](https://docs.tealium.com/server-side/connectors/add/), usando as seguintes opções:

   1. Selecione o [!DNL AWS Firehose] conector.

   1. Nas configurações de origem:

      1. Selecione o segmento de público-alvo a ser compartilhado.

      1. Configurar um acionador:

         * Para o primeiro conector do segmento, selecione o acionador `Joined Audience`. Isso garante que os dados sejam compartilhados com DSP sempre que um usuário ingressar em um segmento.

         * Para o segundo conector do segmento, selecione o acionador `Left Audience`. Esse conector é usado para lidar com todos os cancelamentos e usuários que deixam o segmento no DSP.

   1. Nas configurações, especifique o conector de firehose do AWS. Se você ainda não tiver adicionado o conector do firehose para DSP, adicione um conector do firehose usando as seguintes informações:

      * **Nome:** O nome do conector.

      * **Chave de Acesso:** A chave de acesso fornecida pela equipe da conta do Adobe.

      * **Chave secreta:** A chave secreta fornecida pela equipe da conta do Adobe.

      * **Região:** Leste dos EUA e Virgínia do Norte (us-east-1)

   1. Nas configurações de ação, faça o seguinte:

      1. Crie uma ação &quot;Enviar dados do cliente para fluxo do delivery (avançado)&quot; para adicionar dados ao segmento, usando as seguintes informações:

         * **Nome da ação:** O nome da ação.

         * **Tipo de ação:** Enviar dados do cliente para fluxo de entrega (avançado)

         * **Fluxo de entrega:** Tealium_CDP_Connector

         * **Dados da mensagem:**  Faça o seguinte:

            1. Escolha um atributo para o segmento:

               * Para o atributo Hash_Email, nomeie a mensagem personalizada `hashed_email`.

               * Para o atributo Cookies, nomeie a mensagem personalizada `cookies`.

            1. Na opção para criar um campo personalizado, na variável [!DNL Source Key] insira o [!UICONTROL External Segment Key] que foi incluído no [dados de mapeamento de segmento](#map-data) no procedimento anterior.

               O DSP usará essa chave para preencher seu segmento.

            1. (Recomendado) Crie uma ação de atualização para manter o segmento atualizado.

## Etapa 5: Duplicar o conector existente em [!DNL Tealium] para continuar a compartilhar segmentos {#duplicate-connector}

Você pode ter apenas um conector por segmento e um segmento por conector.

1. Entrada [!DNL Tealium], duplique o segmento para o qual deseja criar outro segmento e renomeie o novo segmento.

1. Entrada [!DNL Tealium], duplicar [o conector que você criou](#tealium-connector) no procedimento anterior, e renomeie o novo conector de &quot;`<original name>-copy`&quot; para o novo nome de segmento.

## Etapa 6: Comparar o número de IDs universais com o número de endereços de email com hash {#compare-id-count}

Após concluir todas as etapas, verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que o segmento está preenchendo em 24 horas. Compare o número de IDs universais com o número de endereços de email com hash originais.

A taxa de conversão de endereços de email com hash em IDs universais deve ser superior a 90%. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para mais de 90 IDs universais. Uma taxa de tradução de 90% ou menos é um problema. Para obter mais informações sobre como as contagens de segmentos podem variar, consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Os segmentos são atualizados a cada 24 horas. No entanto, a inclusão em um segmento expira após 30 dias para garantir a conformidade com a privacidade. Portanto, atualize os públicos-alvo enviando-os novamente do [!DNL Tealium] a cada 30 dias ou menos.

Para obter suporte para solução de problemas, entre em contato com a equipe de conta da Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo da Universal ID](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Converter IDs de usuário de [!DNL Adobe Real-Time CDP] para Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
