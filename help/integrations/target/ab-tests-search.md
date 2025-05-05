---
title: Configurar testes A/B para anúncios do Adobe Advertising Search, Social e Commerce no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para seus [!DNL Google Ads] e [!DNL Microsoft Advertising] anúncios em Search, Social e Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para Advertising Search, Social e Commerce Ads

*Somente anunciantes com Advertising Search, Social e Commerce*

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

O Adobe Advertising e o Adobe Target facilitam a configuração de testes A/B de experiência de página de aterrissagem para o tráfego de publicidade digital [!DNL Google Ads] e [!DNL Microsoft Advertising] para:

* Melhorar as taxas de conversão (CVR) e as medidas de eficiência de aquisição (como CPA, CPL e CAC).

* Ofereça uma experiência de página de aterrissagem mais personalizada que seja relevante para o anúncio (por exemplo, corresponder o criativo da imagem/vídeo, a cópia, a palavra-chave ou outro sinal de publicidade à página de aterrissagem).

Você também pode combinar as dimensões de relatório de integração do [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) e do [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR) nativas integradas ao Adobe Analytics para medir e visualizar seus dados de teste com [!DNL Analytics] métricas e eventos de sucesso.

Consulte as seções a seguir para obter os pré-requisitos, instruções para configurar testes A/B no [!DNL Target] para tráfego de click-through de anúncios em Pesquisa, Social e Commerce e dicas sobre como medir e visualizar seus testes no [!DNL Analytics].

## Pré-requisitos

### Produtos necessários

* Pesquisa, Social e Commerce
* [!DNL Target]

### Produtos e integrações recomendados

* [!DNL Analytics]

* [[!DNL Analytics] para integração com o Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR) integração

## Etapa 1: criar uma atividade de teste A/B no [!DNL Target] para Search, Social e Commerce

As instruções a seguir destacam informações relacionadas ao caso de uso de Pesquisa, Social e Commerce.

1. [Faça logon no Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=pt-BR).

1. [Criar um teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR):

   1. No campo **[!UICONTROL Enter Activity URL]**, insira a URL da página de aterrissagem do teste.

   1. No campo **[!UICONTROL Goal]**, insira a métrica de sucesso do teste.

      >[!NOTE]
      >
      >Verifique se [!DNL Analytics] está habilitado como fonte de dados em [!DNL Target] e se o conjunto de relatórios correto está selecionado.

   1. Defina o **[!UICONTROL Priority]** como `High` ou `999` para evitar conflitos quando os usuários no segmento de teste receberem uma experiência no site incorreta.


   1. Em **[!UICONTROL Reporting Settings]**, selecione o **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** conectados à sua conta do Search, Social e Commerce.

      Para obter dicas adicionais sobre relatórios, consulte &quot;[Práticas recomendadas e solução de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=pt-BR) para relatórios.&quot;

   1. No campo **[!UICONTROL Date Range]**, insira as datas de início e término apropriadas para o teste.

   1. Selecione **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. No campo **[!UICONTROL Value]**, digite o [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] ou [!UICONTROL Network Ad ID] para a entidade de rede de anúncios relevante em Pesquisa, Social e Commerce. Isso permite usar os parâmetros da cadeia de caracteres de consulta [!DNL Target] para públicos-alvo de click-through para a entidade.

      Você pode encontrar a ID [adicionando a coluna de ID relevante à exibição de entidade](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] coluna na [!UICONTROL Accounts] exibição](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] coluna na [!UICONTROL Accounts] exibição")

      Entre em contato com a equipe de conta do Adobe se precisar de assistência.

   1. Para o **[!UICONTROL Traffic Allocation Method]**, selecione **[!UICONTROL Manual (Default)]** e divida o público em 50/50.

   1. Salve a atividade.

1. Use o [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR) para fazer alterações de design no modelo de página de aterrissagem de teste A/B.

   * Experiência A: não edite porque é a experiência padrão/de controle da página de aterrissagem sem personalização.

   * Experiência B: use a interface do usuário [!DNL Target] para personalizar o modelo de página de aterrissagem com base nos ativos incluídos no teste (como títulos, cópia, posicionamento de botões e criação).

   >[!NOTE]
   >
   >Por exemplo, casos de uso de testes criativos, entre em contato com a equipe de conta do Adobe.

## Etapa 2: Configurar seu Analysis Workspace [!DNL Analytics for Target] no [!DNL Analytics]

O [!DNL Analytics for Target] (A4T) é uma integração entre soluções que permite aos anunciantes criar atividades do [!DNL Target] com base em [!DNL Analytics] métricas de conversão e segmentos de público-alvo e, em seguida, medir os resultados usando o [!DNL Analytics] como fonte de relatórios. Todos os relatórios e segmentações para essa atividade são baseados na coleção de dados do [!DNL Analytics].

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para instruções de implementação, consulte &quot;[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR)&quot;.

### Configurar o painel [!DNL Analytics for Target]

No Analysis Workspace, configure o [!DNL Analytics for Target panel] para analisar suas atividades e experiências do [!DNL Target]. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel no espaço de trabalho específico para a conta Adobe Advertising, campanha ou grupo de anúncios <!-- only applicable entities? --> para o qual o teste foi executado. Use visualizações de resumo para mostrar métricas de Adobe Advertising no mesmo relatório que o desempenho de teste [!DNL Target].

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Adobe Advertising (como impressões, cliques e custos) não podem ser correspondidas às métricas [!DNL Target].

#### Dimension

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **Atividades do Target**: nome do teste A/B

* **Experiências do Target**: Nomes das experiências da página de aterrissagem usadas na atividade

* **Atividade do Target** > **Experiência**: o nome da atividade e o nome da experiência na mesma linha

### Solução de problemas do Analytics para dados do [!DNL Target]

No Analysis Workspace, se você notar que os dados de atividade e experiências são mínimos ou não são preenchidos, faça o seguinte:

* Verifique se o mesmo [!UICONTROL Supplemental Data ID] (SDID) é usado para [!DNL Target] e [!DNL Analytics]. Você pode verificar os valores SDID usando o [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=pt-BR) na página de aterrissagem para a qual a campanha está direcionando usuários.

[Valores de ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) o [!UICONTROL Hostname] exibido no Adobe Debugger em [!UICONTROL Solutions] > [!UICONTROL Target] corresponde b) o [!UICONTROL Tracking Server] exibido em [!DNL Target] para a atividade (em [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requer que um servidor de rastreamento [!DNL Analytics] seja enviado em chamadas de [!DNL Target] para o servidor de coleta de dados [!DNL Modstats] do Analytics.<!-- just "to Analytics?"-->

[Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integrar o Target ao Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=pt-BR) - Explica como configurar relatórios do [!DNL Target] no Analysis Workspace.
* [Visão geral do teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=pt-BR) - Descreve as atividades do teste A/B, que você pode usar com os anúncios de Pesquisa, Social e Commerce.
* [Visão geral do Analytics para Advertising](/help/integrations/analytics/overview.md) - Apresenta o Analytics para Advertising, que permite rastrear interações de site click-through e view-through nas instâncias do Analytics.

>[!MORELIKETHIS]
>
>* [Configurar testes A/B no Adobe Target para Advertising DSP Ads](ab-tests-dsp.md)
