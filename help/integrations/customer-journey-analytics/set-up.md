---
title: Configurar a coleta de dados, a transferência de dados e os relatórios
description: Saiba como configurar a coleta de dados, a transferência de dados e os relatórios.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Configurar a coleta de dados, a transferência de dados e os relatórios

*recurso do Beta*

As tarefas a seguir são necessárias para exibir os dados da Advertising Cloud no Customer Journey Analytics.

1. (O analista da Web de sua organização; opcional) [Coletar dados históricos para IDs AMO e IDs EF](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Esta etapa só é aplicável para anunciantes com [!DNL Analytics for Advertising].

1. (O administrador de site da sua organização para o Adobe Experience Platform) [Configure a coleta de dados no Experience Platform e implemente as tags de rastreamento de conversão](#data-collection).

1. (Administrador do site da sua organização para o Customer Journey Analytics) [Crie uma conexão com seus conjuntos de dados do Experience Platform no Customer Journey Analytics](#dataset-connection).

1. (O analista da Web de sua organização) [Configurar visualizações de dados no Customer Journey Analytics](#cja-data-views).

1. (O analista da Web de sua organização) [Configurar relatórios e visualizações no Customer Journey Analytics Workspace](#cja-reports).

As seções a seguir incluem os procedimentos detalhados, que incluem as tarefas e as configurações necessárias para a integração, mas não explicam todos os recursos disponíveis nos fluxos de trabalho. Consulte os recursos vinculados para obter informações completas.

## Configurar a coleção de dados no Adobe Experience Platform e em seu site {#data-collection}

As tarefas a seguir são necessárias para configurar a coleta de dados no Experience Platform e implementar tags de rastreamento de conversão. O administrador do site da sua organização para o Experience Platform pode executar essas tarefas, mas o departamento de TI da sua organização pode precisar ajudar com a implantação de tags de rastreamento.

1. Colete e envie dados do Adobe Advertising para o Experience Platform Edge Network como um conjunto de dados:

   1. No Experience Platform, [defina um esquema manual](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) para os dados que deseja coletar usando o Experience Data Model (XDM).

      * Em [!UICONTROL Schema Details], selecione **[!UICONTROL Experience Event]** como classe base do esquema para capturar eventos do site. Nomeie seu esquema e clique em **[!UICONTROL Finish]**.

      * No painel esquerdo, adicione o grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` para adicionar campos específicos ao Adobe Advertising.<!-- Add link once published --> No mínimo, inclua o objeto conversionDetails com as propriedades `trackingCode` e `trackingIdentities`, que incluem a [ID de AMO e EF ID](ids.html). Os outros campos são opcionais.

      * (Opcional) Adicione outros grupos de campos conforme necessário para conectar campos de dados adicionais aos dados do Adobe Advertising.

      **Observação:** você pode criar vários esquemas, mas pode usar apenas um esquema por conjunto de dados e por sequência de dados, que você criará nas etapas a seguir.

   1. [Crie um conjunto de dados](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) com base no esquema para armazenar e gerenciar a coleção de dados do evento.

      * Escolha a opção para **[!UICONTROL Create dataset from schema]** e selecione seu esquema.

        O Adobe Advertising cria conjuntos de dados adicionais para os dados de métricas de resumo relacionados (como valores de conversão) e dados de pesquisa (metadados de dimensões/classificação, como nome de campanha do Adobe Advertising) com base no conjunto de dados do evento. Os dados dos conjuntos de dados são preenchidos diariamente no Experience Platform.

   1. [Crie uma sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) para o esquema.

      * Para a configuração [!UICONTROL Mapping schema], selecione seu esquema.

      * Adicione e habilite os serviços `Adobe Advertising` e `Adobe Experience Platform` à sequência de dados.

        Esses serviços permitem que a Edge Network armazene o conjunto de dados e o roteie para a Adobe Advertising.

      * Para a configuração [!UICONTROL Event dataset], selecione seu conjunto de dados.

        Cada sequência de dados pode inserir dados em apenas um conjunto de dados.

1. Envie os dados do site da organização para a sequência de dados da Experience Platform:

   1. Use as [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) da Experience Platform (antes conhecidas como [!DNL Launch]) para gerar uma tag da JavaScript e enviar os dados do site de sua organização para a sequência de dados.

      * Crie uma propriedade de tag, que é o container da configuração de tag.

      * Para sua propriedade, [instale a extensão &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) do catálogo de extensões.

        Essa extensão envia dados de suas propriedades da Web para o Experience Cloud por meio do Experience Platform Edge Network.

        Não use a extensão do Adobe Advertising.

      * Crie uma build personalizada do Web SDK:

         * Na seção [!UICONTROL Custom build components], habilite o componente **Advertising**.

           Esse componente inclui todo o código JavaScript necessário para o Adobe Advertising na tag. Ele também adiciona uma configuração &quot;Advertising&quot; nas regras de tag (que são opcionais) para definir como os dados de publicidade são usados para medição de atribuição.

           Opcionalmente, é possível ativar componentes adicionais, conforme necessário.

         * Na seção [!UICONTROL SDK Instances]:

            * Nas configurações do [!UICONTROL Datastreams], selecione a sequência de dados a ser usada para cada um dos ambientes da Web (produção, preparo, desenvolvimento).

            * (Somente organizações com Adobe Advertising DSP) Nas configurações de [!UICONTROL Adobe Advertising]:

               * Habilite a configuração **[!UICONTROL Adobe Advertising DSP]** para habilitar o rastreamento de view-through.

               * Especifique os anunciantes para os quais ativar o rastreamento de view-through.

               * (Opcional) Insira a ID de parceiro ID5 da organização para coletar IDs.

               * (Opcional) Insira o caminho para o código JavaScript [!DNL LiveRamp RampID] da sua organização (ats.js) para coletar IDs.

            * Salve a criação.

      * (Opcional) [Crie regras](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) conforme necessário para determinar quando o Web SDK deve enviar dados para a Edge Network.

         * Para a configuração [!UICONTROL Advertising], defina como os dados de publicidade são usados para a medição de atribuição. Essa configuração é útil quando a regra inclui uma sequência de várias ações e está disponível somente quando você seleciona o componente &quot;[!UICONTROL Advertising]&quot; para o componente de compilação personalizado. As opções incluem:

           *Automático:* Permite que dados de publicidade sejam usados para medir a atribuição de publicidade na ação `sendEvent` atual com base nos dados do cache. Nesse caso, o evento de exposição do anúncio é acionado quando recebe a chance e pode não estar disponível para o evento atual. Por exemplo, se você acionar um evento de finalização de compra e nenhum dado de exposição do anúncio estiver disponível no cache, o evento de finalização não será atribuído à exposição do anúncio.

           *Aguardar:* atrasa a execução da chamada até que os dados de anúncio sejam recuperados do servidor e resolvidos com êxito, o que garante uma medição de atribuição precisa. Por exemplo, talvez você queira aguardar a resolução do evento de exposição do anúncio antes de acionar um evento de finalização de compra. **Observação:** a resolução de IDs pode levar alguns segundos, dependendo do navegador e do tipo de ID. Use esta opção se a ação `sendEvent` atual puder acomodar alguns segundos de atraso.

           *Desabilitado:* (padrão) exclui dados de publicidade da solicitação que você está acionando, tornando-a indisponível para atribuição ou rastreamento relacionado.

           *Forneça um elemento de dados:* Use um elemento de dados para incluir ou excluir dados de publicidade durante o carregamento da página. Os valores resolvidos para o elemento de dados podem incluir `automatic`, `wait` e `disabled`. Consulte a próxima etapa.

        Se você não usar uma regra para configurar uma ação `sendEvent`, os dados de anúncio serão enviados como um evento de enriquecimento de Anúncio separado.

      * Crie [elementos de dados](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) conforme necessário para mapear variáveis no seu site para a estrutura do esquema XDM criado anteriormente.

   1. [Publique a marca](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) em um ambiente de teste no qual você possa iterar o desenvolvimento de marcas.

   1. Valide a entrega dos conjuntos de dados e [publique a tag no seu ambiente de produção em tempo real](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

      O departamento de TI de sua organização ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

## Criar uma conexão com seus conjuntos de dados do Experience Platform no Customer Journey Analytics {#dataset-connection}

Siga estas etapas para extrair dados do Adobe Advertising dos conjuntos de dados do Experience Platform para a Customer Journey Analytics. O administrador do site da sua organização para o Customer Journey Analytics pode executar essas tarefas.

*Em breve*

## Configurar visualizações de dados no Customer Journey Analytics {#cja-data-views}

No Customer Journey Analytics, crie uma ou mais visualizações de dados para definir as métricas e dimensões para os relatórios. Um analista da Web pode executar essas tarefas.

*Em breve*

## Configurar relatórios e visualizações no Customer Journey Analytics Workspace {#cja-reports}

No Customer Journey Analytics Workspace, siga estas etapas para configurar relatórios e visualizações. Um analista da Web pode executar essas tarefas.

1. [Crie um projeto](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) no Workspace para criar relatórios e visualizações com base nas dimensões e métricas configuradas na visualização de dados.

1. (Se você tiver dados de [!DNL Google Ads] ou [!DNL Microsoft Advertising]) Crie um relatório de conversões controladas pelo editor usando campos de métricas específicas de rede de anúncios, que são agrupadas como `googleConversions` e `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* [Pré-requisitos](prerequisites.md)
>* [Adobe Advertising IDs Usadas por [!DNL Customer Journey Analytics]](ids.md)
>* [Métricas e dimensões do Adobe Advertising no Customer Journey Analytics](advertising-data-in-cja.md)
>* [Coletar Dados Históricos para IDs AMO e IDs EF para Uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guia do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* [Guia do usuário do Customer Journey Analytics para usuários do Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
