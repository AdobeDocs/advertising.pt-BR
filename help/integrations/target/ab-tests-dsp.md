---
title: Configurar testes A/B para anúncios do Adobe Advertising DSP no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para seus anúncios do DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: f4a8bfc77b4d99dd2e54f7441ec0afd0c17c0252
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para Advertising DSP Ads

*Somente anunciantes com o Advertising DSP*

O Adobe Advertising e o Adobe Target tornam ainda mais fácil para os profissionais de marketing fornecer uma experiência personalizada e conectada em mídia paga e mensagens no site. Ao compartilhar sinais entre os produtos, você pode:

* Diminuir as taxas de fallthrough do site, vinculando a exposição de anúncios dos clientes das campanhas do DSP às suas experiências no site.

* Estabeleça um teste A/B espelhando experiências no site com mensagens de publicidade usando dados de exposição da Adobe Audience Manager e públicos-alvo [!DNL Target] do tipo clique-para-feed.

* Meça o impacto da Unificação de Mensagens em um aumento de objetivos no site com visualizações simples no Adobe Analytics para [!DNL Target].

Consulte as seções a seguir para obter os pré-requisitos e instruções para configurar o rastreamento de click-through e view-through, implementar o compartilhamento de sinal entre o DSP e o [!DNL Target] e configurar uma atividade de teste A/B, e configurar o Analysis Workspace [!DNL Analytics] para exibir os dados de teste.

Em caso de dúvidas adicionais, entre em contato com a equipe de conta da Adobe.

## Pré-requisitos

Este caso de uso requer os seguintes produtos e integrações:

* [!DNL Target]

* [[!DNL Analytics] para integração com o Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR) integração

* Audience Manager (obrigatório somente para teste view-through)

## Etapa 1: configurar a Estrutura Click-through {#click-through-framework}

![Estrutura de click-through](/help/integrations/assets/target-ct-framework.png)

Ao adicionar macros do DSP a uma URL de click-through (a URL exibida quando um usuário clica em um anúncio e chega à página inicial), o DSP captura automaticamente a chave de posicionamento incluindo `${TM_PLACEMENT_ID}` na URL de click-through. Esta macro captura a chave de posicionamento alfanumérico e não a ID de posicionamento numérico.

![URL de click-through anexado à URL da página de aterrissagem](/help/integrations/assets/target-ct-url.jpg)

### (Somente no DSP) Adicionar macros do DSP aos URLs de click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

No [!DNL Flashtalking] ou no Google Campaign Manager 360, atualize manualmente a URL de click-through para cada anúncio a fim de incluir as macros necessárias para capturar as variáveis de ID do AMO. As variáveis de ID do AMO são usadas para enviar dados de cliques para o Adobe Analytics e compartilhar chaves de posicionamento para testes A/B. Consulte as seguintes páginas para obter instruções:

* [Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio](/help/integrations/analytics/macros-flashtalking.md). **Observação:** este procedimento não será necessário se sua organização tiver uma parceria direta com [!DNL Flashtalking] e você usar macros de passagem de dados para rastrear os parâmetros de rastreamento `s_kwcid` e `ef_id` de acordo com a documentação de suporte do [!DNL Flashtalking] em [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Acrescentar  [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Marcas de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md)

Entre em contato com a equipe de conta da Adobe para recuperar a chave de posicionamento necessária e finalizar a configuração e garantir que cada URL de click-through seja preenchido com a chave de posicionamento.

## Etapa 2: Configurar a estrutura de view-through usando o Audience Manager {#view-through-framework}

![Estrutura de view-through](/help/integrations/assets/targetr-vt-framework.png)

Ao adicionar um pixel de evento de impressão do Audience Manager em suas tags de anúncio e configurações de posicionamento, é possível criar um segmento de teste para oportunidades de teste de view-through adicionais.

1. Implemente um pixel de evento de impressão do Audience Manager em suas tags de anúncio e configurações de posicionamento do DSP.

   Para obter instruções, consulte &quot;[Coletar dados de exposição de mídia das campanhas do Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Adicione [macros do DSP](/help/dsp/campaign-management/macros.md) para capturar todos os dados que você deseja que o pixel de evento de impressão retorne, incluindo `${TM_PLACEMENT_ID_NUM}` para a ID de posicionamento numérica.

   >[!NOTE]
   >
   >As URLs de rastreamento de cliques incluem a macro `${TM_PLACEMENT_ID}` para a chave de posicionamento alfanumérico, em vez de `${TM_PLACEMENT_ID_NUM}` para a ID de posicionamento numérico.

1. Configure um segmento do Audience Manager com base nos dados de impressão do DSP:

   1. Verifique se os dados do segmento estão disponíveis:

      1. [Procure o sinal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html?lang=pt-BR) para o [par de valores-chave](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html?lang=pt-BR) que determina em qual nível os usuários do segmento são agrupados.

         Use uma [chave com suporte](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=pt-BR) com um valor que corresponda a uma macro adicionada ao pixel de evento de impressão do Audience Manager.

         Por exemplo, para agrupar usuários para um posicionamento específico, use a chave `d_placement`. Para o valor, use uma ID de posicionamento numérico real (como 2501853) capturada pela macro do DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Se os resultados da pesquisa mostrarem contagens de usuários para o par de valores chave, o que indica que o pixel foi colocado corretamente e os dados estão fluindo, continue para a próxima etapa.

   1. [Crie uma característica com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=pt-BR) para a criação de segmentos no Audience Manager.

      * Nomeie a característica para que seja facilmente identificável nas atividades de teste. Armazene a característica na pasta que preferir.

      * Selecione `Ad Cloud` como **[!UICONTROL Data Source]**.

      * Para a expressão de característica, use `d_event` como **[!UICONTROL Key]** e `imp` como **[!UICONTROL Value]**.

   1. [Configurar um segmento de teste](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html?lang=pt-BR) para a nova característica no Audience Manager, selecionando `Ad Cloud` como **[!UICONTROL Data Source]**.

      O Audience Manager divide automaticamente o segmento em um grupo de controle que recebe a experiência padrão de página de aterrissagem e um grupo de teste que recebeu uma experiência personalizada no local.

## Etapa 3: configurar uma Atividade de Teste A/B no [!DNL Target] para DSP

As instruções a seguir destacam informações relacionadas ao caso de uso do DSP.

1. [Entrar no Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=pt-BR).

1. [Criar um teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR):

   1. No campo **[!UICONTROL Enter Activity URL]**, insira a URL da página de aterrissagem do teste.

      >[!NOTE]
      >
      >Você pode usar vários URLs para testar a entrada do site de view-through. Para obter mais informações, consulte &quot;[Atividade multipáginas](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html?lang=pt-BR).&quot; Você pode identificar facilmente as principais entradas por URL de página, criando um [relatório de Entrada de Site](https://experienceleague.adobe.com/pt-br/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) no Analytics.

   1. No campo **[!UICONTROL Goal]**, insira a métrica de sucesso do teste.

      >[!NOTE]
      >
      >Verifique se [!DNL Analytics] está habilitado como fonte de dados em [!DNL Target] e se o conjunto de relatórios correto está selecionado.

   1. Defina o **[!UICONTROL Priority]** como `High` ou `999` para evitar conflitos quando os usuários no segmento de teste receberem uma experiência no site incorreta.

   1. Em **[!UICONTROL Reporting Settings]**, selecione o **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** conectados à sua conta do DSP.

      Para obter dicas adicionais sobre relatórios, consulte &quot;[Práticas recomendadas e solução de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=pt-BR) para relatórios.&quot;

   1. No campo **[!UICONTROL Date Range]**, insira as datas de início e término apropriadas para o teste.

   1. Adicionar públicos-alvo à atividade:

      1. Escolha o [segmento criado anteriormente no Audience Manager para testar os públicos-alvo de view-through](#view-through-framework).

      1. Selecione **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** e insira a chave de posicionamento do DSP no campo **[!UICONTROL Value]** para usar os parâmetros da cadeia de caracteres de consulta do Target para públicos-alvo de click-through.

   1. Para o **[!UICONTROL Traffic Allocation Method]**, selecione **[!UICONTROL Manual (Default)]** e divida o público em 50/50.

   1. Salve a atividade.

1. Use o [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR) para fazer alterações de design no modelo de página de aterrissagem de teste A/B.

   * Experiência A: não edite porque é a experiência padrão/de controle da página de aterrissagem sem personalização.

   * Experiência B: use a interface do usuário [!DNL Target] para personalizar o modelo de página de aterrissagem com base nos ativos incluídos no teste (como títulos, cópia, posicionamento de botões e criação).

   >[!NOTE]
   >
   >Por exemplo, casos de uso de teste criativo, entre em contato com a equipe de conta da Adobe.

## Etapa 4: configurar seu Analysis Workspace [!DNL Analytics for Target] no [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

O [!DNL Analytics for Target] (A4T) é uma integração entre soluções que permite aos anunciantes criar atividades do [!DNL Target] com base em [!DNL Analytics] métricas de conversão e segmentos de público-alvo e, em seguida, medir os resultados usando o [!DNL Analytics] como fonte de relatórios. Todos os relatórios e segmentações para essa atividade são baseados na coleção de dados do [!DNL Analytics].

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para instruções de implementação, consulte &quot;[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR)&quot;.

### Configurar o painel [!DNL Analytics for Target]

No Analysis Workspace, configure o [!DNL Analytics for Target panel] para analisar suas atividades e experiências do [!DNL Target]. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel no espaço de trabalho específico para a campanha, o pacote ou o posicionamento do Adobe Advertising para o qual o teste foi executado. Use visualizações de resumo para mostrar métricas do Adobe Advertising no mesmo relatório que o desempenho de teste [!DNL Target].

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Adobe Advertising (como impressões, cliques e custos) não podem ser correspondidas às métricas [!DNL Target].

#### Dimensões

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Nome do teste A/B

* **[!UICONTROL Target Experiences]**: Nomes das experiências da página de aterrissagem usadas na atividade

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: o nome da atividade e o nome da experiência na mesma linha

### Solução de problemas do Analytics para dados do [!DNL Target]

No Analysis Workspace, se você notar que os dados de atividade e experiências são mínimos ou não são preenchidos, faça o seguinte:

* Verifique se o mesmo [!UICONTROL Supplemental Data ID] (SDID) é usado para [!DNL Target] e [!DNL Analytics]. Você pode verificar os valores SDID usando o [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=pt-BR) na página de aterrissagem para a qual a campanha está direcionando usuários.

[Valores da ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) o [!UICONTROL Hostname] exibido no Adobe Debugger em [!UICONTROL Solutions] > [!UICONTROL Target] corresponde b) o [!UICONTROL Tracking Server] exibido em [!DNL Target] para a atividade (em [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requer que um servidor de rastreamento [!DNL Analytics] seja enviado em chamadas de [!DNL Target] para o servidor de coleta de dados [!DNL Modstats] do Analytics.<!-- just "to Analytics?"-->

[Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integrar o Target ao Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=pt-BR) - Explica como configurar relatórios do [!DNL Target] no Analysis Workspace.
* [Visão geral do teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=pt-BR) - Descreve as atividades do teste A/B, que você pode usar com anúncios do DSP.
* [Experiências e ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html?lang=pt-BR) - Explica as ferramentas [!DNL Target] para determinar o conteúdo no site ao qual os usuários de teste do DSP estão expostos.
* [Sinais, Características e Segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=pt-BR) - Define algumas das ferramentas do Audience Manager que podem ajudar no teste view-through do DSP.
* [Visão geral do Analytics para Advertising](/help/integrations/analytics/overview.md) - Apresenta o Analytics para Advertising, que permite rastrear interações de site click-through e view-through nas instâncias do Analytics.

>[!MORELIKETHIS]
>
>* [Configurar testes A/B no Adobe Target para Advertising Search, Social e Commerce Ads](ab-tests-search.md)
