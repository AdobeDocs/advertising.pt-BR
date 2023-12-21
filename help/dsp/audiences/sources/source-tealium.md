---
title: "Fluxo de trabalho para usar a integração do DSP com o [!DNL Tealium]"
description: "Saiba como habilitar o DSP para assimilar seus [!DNL Tealium] segmentos primários."
feature: DSP Audiences
source-git-commit: e7c967d66be9c8ca78a64d644c7e3a691f1e216a
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Fluxo de trabalho para usar a integração do DSP com o [!DNL Tealium]

Você pode compartilhar os dados primários de sua organização na [!DNL Tealium] plataforma de dados do cliente usando o [!DNL Amazon Web Services] Conector de mangueira de incêndio do (AWS). Há quatro etapas para compartilhar dados do Tealium com o DSP:

1. [Criar uma fonte de público no DSP](#source-create).

1. [Preparar e compartilhar dados de mapeamento de segmento](#map-data).

1. [Criar conectores no [!DNL Tealium] para compartilhar dados de segmento](#tealium-connector).

1. [Duplicação do conector existente no [!DNL Tealium] para continuar a compartilhar segmentos](#duplicate-connector).

## Etapa 1: criar uma fonte de público-alvo no DSP {#source-create}

* [Criar uma fonte de público-alvo](source-create.md) para importar públicos-alvo para sua conta DSP ou uma conta de anunciante e compartilhar a chave do código-fonte com a [!DNL Tealium] usuário.

## Etapa 2: Preparar e compartilhar dados de mapeamento de segmento {#map-data}

1. O anunciante deve preparar e compartilhar dados de mapeamento de segmento:

   1. O anunciante deve preparar os dados no [!DNL Tealium]:

      1. As IDs de email do público-alvo do anunciante devem ser transformadas em hash usando o algoritmo SHA -256.

      1. A coluna contendo IDs de email com hash deve ser mapeada para o atributo do tipo de ID de visitante.

      1. O público-alvo deve ser criado com o `Tealium_visitor_id` atributo. O enriquecimento correto deve ser aplicado para acionar o público-alvo. Consulte a [[!DNL Tealium] documentação sobre atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. O anunciante deve fornecer dados de mapeamento de segmento à Equipe de conta do Adobe para criar os segmentos no DSP. Use os seguintes nomes e valores de coluna em um arquivo de valores separados por vírgula:

      * **Chave de segmento externo:** A chave do segmento externo, que você especificará posteriormente nas configurações de ação do conector em [!DNL Tealium]. A convenção de nomenclatura recomendada é &quot;`<DSP source key>_<Tealium segment name>`,&quot; como &quot;57bf424dc10_coffee-drinkers.&quot;

      * **Nome do segmento:** O nome do segmento.

      * **Descrição do segmento:** A finalidade ou a regra do segmento, ou ambas.

      * **ID do pai:** Manter em branco

      * **CPM de vídeo:** 0

      * **Exibir CPM:** 0

      * **Janela Segmento:** O tempo de vida do segmento.

## Etapa 3: Criar conectores no [!DNL Tealium] para compartilhar dados de segmento {#tealium-connector}

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

            1. Na opção para criar um campo personalizado, na variável [!DNL Source Key] insira o [!UICONTROL External Segment Key] que foi incluído nos dados de mapeamento de segmentos no [Etapa 2](#map-data).

               O DSP usará essa chave para preencher seu segmento.

            1. (Recomendado) Crie uma ação de atualização para manter o segmento atualizado.

## Etapa 4: Duplicar o conector existente em [!DNL Tealium] para continuar a compartilhar segmentos {#duplicate-connector}

Você pode ter apenas um conector por segmento e um segmento por conector.

1. Entrada [!DNL Tealium], duplique o segmento para o qual deseja criar outro segmento e renomeie o novo segmento.

1. Entrada [!DNL Tealium], duplique o conector criado em [Etapa 3](#tealium-connector)e renomeie o novo conector de &quot;`<original name>-copy`&quot; para o novo nome de segmento.

>[!MORELIKETHIS]
>
>* [Sobre a ativação de segmentos autenticados de fontes de público-alvo](/help/dsp/audiences/sources/source-about.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Fluxo de trabalho para usar a integração do DSP com o [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
