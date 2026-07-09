---
title: Configurar a coleta de dados, a transferência de dados e os relatórios
description: Saiba como configurar a coleta de dados, a transferência de dados e os relatórios.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ede5b5b1eb8ab449b982fdadba93e944cd2e062f
workflow-type: tm+mt
source-wordcount: 2103
ht-degree: 1%

---

# Configurar a coleta de dados, a transferência de dados e os relatórios

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

*Anunciantes sem [!DNL Analytics for Advertising] somente*

<!-- may need to remove references to Experience Platform if it's not really required, just Data Collection? In that case, I may need to change all of the links accordingly.... -->

As tarefas a seguir são necessárias para trocar dados nativamente entre o Adobe Advertising e a Customer Journey Analytics usando o [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). A transferência e a atribuição de dados começam após o lançamento; nenhum dado histórico é incluído.

Estas tarefas não são necessárias para anunciantes com [!DNL Analytics for Advertising].

1. (O administrador de site da sua organização para o Adobe Experience Platform) [Configure a coleta de dados no Experience Platform e implemente as tags de rastreamento de conversão](#data-collection).

1. (Administrador do site da sua organização para o Customer Journey Analytics) [Crie uma conexão com seus conjuntos de dados do Experience Platform no Customer Journey Analytics](#dataset-connection).

1. (O analista da Web de sua organização) [Configurar visualizações de dados no Customer Journey Analytics](#cja-data-views).

1. (O analista da Web de sua organização) [Configurar relatórios e visualizações no Customer Journey Analytics Workspace](#cja-reports).

As seções a seguir incluem os procedimentos detalhados, que incluem as tarefas e as configurações necessárias para a integração, mas não explicam todos os recursos disponíveis nos fluxos de trabalho. Consulte os recursos vinculados para obter informações completas.

## Configurar a coleção de dados no Adobe Experience Platform e em seu site {#data-collection}

As tarefas a seguir são necessárias para configurar a coleta de dados no Experience Platform e implementar tags de rastreamento de conversão. O administrador do site da sua organização para o Experience Platform pode executar essas tarefas, mas o departamento de TI da sua organização pode precisar ajudar com a implantação de tags de rastreamento.

### Coletar e enviar dados do Adobe Advertising para o Experience Platform Edge Network como um conjunto de dados {#dataset-datastream}

Esse procedimento inclui a criação de um schema. Como opção, você pode editar um esquema existente; nesse caso, não é necessário criar um conjunto de dados ou uma sequência de dados.

1. Na interface da Coleção de dados, [defina um esquema](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) para os dados do site que você deseja coletar usando o Experience Data Model (XDM).

   Se você já tiver um esquema para os dados do seu site, poderá usá-lo com as seguintes configurações.

   * Em [!UICONTROL Schema Details], selecione **[!UICONTROL Experience Event]** como classe base do esquema para capturar eventos do site. Nomeie seu esquema e clique em **[!UICONTROL Finish]**.

   * No painel esquerdo, adicione a [Extensão completa do ExperienceEvent da Adobe Advertising Cloud](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) ao grupo de campos para adicionar campos específicos ao Adobe Advertising. No mínimo, inclua o objeto conversionDetails com as propriedades `trackingCode` e `trackingIdentities`, que incluem a [ID do AMO e a EF ID](ids.md). Os outros campos são opcionais. Nenhuma outra configuração é necessária.

   * (Opcional) Adicione outros grupos de campos conforme necessário para conectar campos de dados adicionais aos dados do Adobe Advertising.

   **Observação:** você pode criar vários esquemas, mas pode usar apenas um esquema por conjunto de dados e por sequência de dados, que você criará nas etapas a seguir.

1. [Crie um conjunto de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) com base no esquema para armazenar e gerenciar a coleção de dados do evento. Este será seu *conjunto de dados de evento*. Se você estiver editando um esquema existente com um conjunto de dados, ignore esta etapa.

   * Escolha a opção para **[!UICONTROL Create dataset from schema]** e selecione seu esquema.

     Com base no seu conjunto de dados de evento, a Adobe Advertising cria dois conjuntos de dados adicionais: 1\) um *conjunto de dados de resumo* com os dados de resumo relacionados (como cliques agregados e impressões agregadas) e 2\) um *conjunto de dados de pesquisa* (com metadados de dimensões/classificação, como o nome da campanha do Adobe Advertising). Os dados dos conjuntos de dados são preenchidos diariamente no Experience Platform.

   >[!TIP]
   >
   >Crie um conjunto de dados de evento fictício primeiro para validar o fluxo de dados antes de usar um conjunto de dados de produção.

1. [Crie uma sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) para especificar para onde enviar dados do seu site ou aplicativo e como lidar com os dados recebidos.

   * Para a configuração [!UICONTROL Mapping schema], selecione seu esquema, que você criou na Etapa 1.

   * Adicione e habilite os serviços `Adobe Advertising` e `Adobe Experience Platform` à sequência de dados.

     O serviço [!UICONTROL Adobe Advertising] permite que as exposições dos anúncios sejam associadas à carga, e o [!UICONTROL Adobe Experience Platform] permite que a Edge Network armazene o conjunto de dados e o direcione para a Adobe Advertising.

   * Para a configuração [!UICONTROL Event dataset], selecione seu conjunto de dados de evento.

     Cada sequência de dados pode inserir dados em apenas um conjunto de dados.

### Envie os dados do site de sua organização para sua <!-- ?? -->sequência de dados do Experience Platform {#tags-websdk}

Use a extensão Adobe Experience Platform Web SDK em Tags do Adobe para enviar os dados do site de sua organização para a sequência de dados da Experience Platform.

>[!NOTE]
>
>Somente as tags do Adobe são compatíveis. Não há suporte disponível para Experience Platform Web SDK (`alloy.js`) autônomo ou gerenciadores de tags de terceiros.

1. Use as [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) da Experience Platform (antes conhecidas como [!DNL Launch]) para gerar uma tag da JavaScript e enviar os dados do site de sua organização para a sequência de dados.

   * Crie uma propriedade de tag, que é o container da configuração de tag.

   * Para sua propriedade, [instale a extensão &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) do catálogo de extensões.

     Essa extensão envia dados de suas propriedades da Web para o Adobe CX Enterprise por meio do Experience Platform Edge Network.

     Não use a extensão do Adobe Advertising.

   * Criar uma [compilação personalizada do Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * Na seção [!UICONTROL Custom build components], habilite o componente **Advertising**.

        Este componente inclui todo o código JavaScript necessário para o Adobe Advertising na tag e é necessário para clientes do Advertising DSP e do Advertising Search, Social e Commerce. O componente também adiciona uma configuração &quot;Advertising&quot; nas regras de tag (que são opcionais) para definir como os dados de publicidade são usados para medição de atribuição.

        Opcionalmente, é possível ativar componentes adicionais, conforme necessário.

      * Na seção [!UICONTROL SDK Instances]:

         * Nas configurações do [!UICONTROL Datastreams], selecione a sequência de dados a ser usada para cada um dos ambientes da Web (produção, preparo, desenvolvimento).

         * (Somente organizações com Adobe Advertising DSP) Nas [[!UICONTROL Adobe Advertising] configurações](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising), habilite **[!UICONTROL Adobe Advertising DSP]** para permitir o rastreamento de view-through e especifique os anunciantes para os quais habilitar o rastreamento de view-through. Você pode, opcionalmente, coletar IDs de IDs universais (traduzidas de suas [fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)) adicionando a ID de parceiro ID5 da sua organização e/ou o caminho para o código JavaScript (ats.js) do [!DNL LiveRamp] [!DNL LaunchPad] da sua organização para [!DNL RampIDs].

           Se seus anunciantes não estiverem listados, insira a ID de anunciante para cada anunciante. Se necessário, peça as IDs à sua equipe de conta da Adobe.

           Se você inserir IDs incorretas, sua equipe de conta da Adobe será notificada.

           Exemplo de um caminho do JavaScript [!DNL RampID]: `https://launchpad-wrapper.privacymanager.io/<customer-specific-id>/launchpad-liveramp.js`

         * Salve a criação.

   * (Opcional) [Crie regras](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) conforme necessário para determinar quando o Web SDK deve enviar dados para a Edge Network.

      * Para ações `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`, use a configuração [[!UICONTROL Advertising]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) para definir como os dados de publicidade são usados para medição de atribuição. Essa configuração é útil quando a regra inclui uma sequência de várias ações e está disponível somente quando você seleciona o componente &quot;[!UICONTROL Advertising]&quot; para o componente de compilação personalizado.

   * Crie [elementos de dados](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) conforme necessário para mapear variáveis no seu site para a estrutura do esquema XDM criado anteriormente.

1. Peça ao administrador do Adobe Experience Platform para [publicar a tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) em um ambiente de teste, no qual você possa iterar o desenvolvimento de tags.

### Validar entrega de dados

1. Peça à equipe de conta da Adobe para validar o rastreamento em seu site.

   ![Exemplo de validação da carga de rastreamento de click-through](/help/integrations/assets/cja-example-click-through-validation.png "Exemplo de validação da carga de rastreamento de click-through")

   ![Exemplo de validação da carga de rastreamento de view-through](/help/integrations/assets/cja-example-view-through-validation.png "Exemplo de validação da carga de rastreamento de view-through")

1. Valide a entrega de dados [verificando a atividade para cada um de seus três conjuntos de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets) (seu conjunto de dados de evento de site, seu conjunto de dados de classificação do Adobe Advertising e seu conjunto de dados de métricas de resumo do Adobe Advertising).

   Você deve ver a atividade do conjunto de dados para assimilação diária em lotes. Se o conjunto de dados do evento mostrar zero registros após 24 horas, verifique novamente sua [sequência de dados](#dataset-datastream) e sua [configuração de extensão do Web SDK nas Tags do Adobe](#tags-websdk).

1. Peça ao administrador do Adobe Experience Platform para [publicar a tag no ambiente de produção ativo](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   O departamento de TI de sua organização ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

## Criar uma conexão com seus conjuntos de dados do Experience Platform no Customer Journey Analytics {#dataset-connection}

Siga estas etapas para extrair dados do Adobe Advertising dos conjuntos de dados do Experience Platform para a Customer Journey Analytics. O administrador do site da sua organização para o Customer Journey Analytics pode executar essas tarefas.

Opcionalmente, também é possível editar uma conexão existente com as mesmas informações.

1. No Customer Journey Analytics, [crie ou edite uma conexão](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) que inclua seus conjuntos de dados e esquema do Experience Platform.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Confirme se a sandbox correta (configurada por sua organização) está selecionada.

   * Calcule o número médio de eventos diários (abaixo de 1 milhão para a maioria das organizações).

   * Adicione seu conjunto de dados de métricas de eventos do Experience Platform (tipo: `Event`), seu conjunto de dados de métricas de resumo de eventos <!-- Adobe Advertising --> (tipo: `Event`) e seu conjunto de dados de dimensões <!-- Adobe Advertising --> (classificações/metadados) (tipo: `Lookup`).

     Sua equipe criou o conjunto de dados do evento, e a Adobe Advertising criou os conjuntos de dados de resumo e dimensões com base em seu conjunto de dados de evento.

     Opcionalmente, é possível incluir conjuntos de dados adicionais, conforme necessário.

   * Defina as configurações do conjunto de dados:

      * Para as configurações de [!UICONTROL Event Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]:** Se quiser usar um conjunto de dados e um esquema para a Customer Journey Analytics e a Adobe Real-Time CDP, habilite essa configuração e defina a identidade primária no grupo de campos `IdentityMap`. `Required Field` também é suportado.

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:** Habilitar a configuração

      * Para as configurações de Classificação ([!UICONTROL Lookup Dataset]), mapeie o conjunto de dados de dimensões para o conjunto de dados de eventos:

         * **[!UICONTROL Key]** (o campo a ser usado como a chave para o conjunto de dados de dimensões): `Tracking Code` (que é o mesmo que o campo `trackingCode` no esquema).

         * **[!UICONTROL Matching key]** (o campo a ser usado como a chave correspondente para o conjunto de dados de eventos): `Tracking Code (Event datasets)`.

         * **[!UICONTROL Import all new data]:** Habilitar a configuração

         * **[!UICONTROL Backfill all existing data]:** Habilitar a configuração

      * Para as configurações de [!UICONTROL Metrics Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:** Confirmar o valor

         * **[!UICONTROL Import all new data]:** Habilitar a configuração

2. Em três horas, verifique se os dados estão disponíveis no Customer Journey Analytics.

   1. No Customer Journey Analytics, vá para **[!UICONTROL Connections]** e selecione sua conexão.

   2. Na lista de conjuntos de dados exibidos, verifique se o relatório &quot;[!UICONTROL Number of Records]&quot; mostra que os dados foram adicionados.

## Configurar visualizações de dados no Customer Journey Analytics {#cja-data-views}

No Customer Journey Analytics, crie uma ou mais visualizações de dados para definir as métricas e dimensões para os relatórios. Um analista da Web pode executar essas tarefas.

1. No Customer Journey Analytics, [crie uma visualização de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure a exibição para incluir as informações a seguir.

   * Se você tiver uma conta Adobe Analytics, use o [!UICONTROL Time Zone] para sua conta [!DNL Analytics] na seção [!UICONTROL Calendar] da guia [!UICONTROL Configure].

   * Na guia [!UICONTROL Components]:

      * Adicione seu conjunto de dados de pesquisa (com dimensões/dados de classificação), conjunto de dados de evento (com seus dados no nível do evento) e conjunto de dados de resumo (com suas outras métricas, como cliques).

      * Escolha métricas do conjunto de dados do evento e do conjunto de dados de pesquisa para incluir na visualização de dados.

      * Procure por &quot;[!UICONTROL Tracking Code]&quot; (que faz parte do conjunto de dados de evento com caminho de esquema `_experience.adcloud.conversionDetails.trackingCode`). Defina **[!UICONTROL Persistence]** como *[!UICONTROL Most Recent]*.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Configurar relatórios e visualizações no Customer Journey Analytics Workspace {#cja-reports}

No Customer Journey Analytics Workspace, siga estas etapas para configurar relatórios e visualizações. Um analista da Web pode executar essas tarefas.

1. [Crie um projeto](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) no Workspace para criar relatórios e visualizações com base nas dimensões e métricas configuradas na visualização de dados.

   Por exemplo, inclua as dimensões [!UICONTROL Tracking Code (2)] (para vincular eventos aos metadados da campanha), [!UICONTROL Adobe Advertising Campaign] (para dados no nível da campanha), [!UICONTROL Adobe Advertising Placement] ou [!UICONTROL Adobe Advertising Ad Group] (para dados no nível do posicionamento ou do grupo de anúncios), [!UICONTROL Events], [!UICONTROL Impressions] e [!UICONTROL Clicks].

Você pode classificar métricas de resumo e dados de evento usando a mesma dimensão em uma tabela de forma livre.

1. (Se você tiver dados de [!DNL Google Ads] ou [!DNL Microsoft Advertising]) Crie um relatório de conversões controladas pelo editor usando campos de métricas específicas de rede de anúncios, que são agrupadas como `googleConversions` e `microsoftConversions`.

1. Confirme se os dados aparecem.

>[!TIP]
>
>Os eventos de resumo normalmente adicionam uma pequena quantidade de dados extras aos relatórios, como alguns eventos extras, uma sessão extra por dia ou uma pessoa extra por relatório. Essas adições são insignificantes em comparação aos eventos padrão da Web. No entanto, você pode filtrar esses dados adicionais do evento de resumo excluindo dados para a ID de pessoa fictícia `00000000-0000-0000-0000-000000000000`.Exemplo de exclusão de dados usando uma ID de pessoa&rbrack;(/help/integrations/assets/cja-report-with-person-id.png "Exemplo de exclusão de dados usando uma ID de pessoa")

![Como seus conjuntos de dados podem aparecer no Customer Journey Analytics](/help/integrations/assets/cja-report-example.png "Como seus conjuntos de dados podem aparecer no Customer Journey Analytics")

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* [Pré-requisitos](prerequisites.md)
>* [Adobe Advertising IDs usadas por [!DNL Customer Journey Analytics]](ids.md)
>* [Métricas e dimensões do Adobe Advertising no Customer Journey Analytics](advertising-data-in-cja.md)
>* [Coletar dados históricos para IDs AMO e IDs EF para uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Solução de problemas](troubleshooting.md)
>* [Guia do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* [Guia do usuário do Customer Journey Analytics para usuários do Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
