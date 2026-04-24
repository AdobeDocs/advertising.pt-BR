---
title: Configure testes A/B para anúncios do Adobe Advertising Search, Social e Commerce no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para seus [!DNL Google Ads] e [!DNL Microsoft Advertising] anúncios em Search, Social e Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
TQID: https://experienceleague.adobe.com/eu1dRdsQlJX4IlHLTUDyJ69r0txFvFUdzUiXpSAlpU8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para anúncios do Advertising Search, Social e Commerce

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

## Step 1: Create an A/B test activity in [!DNL Target] for Search, Social, &amp; Commerce

The following instructions highlight information pertaining to the Search, Social, &amp; Commerce use case.

1. [Sign in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=pt-BR).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

   1. In the **[!UICONTROL Goal]** field, enter the success metric for the test.

      >[!NOTE]
      >
      >Make sure that [!DNL Analytics] is enabled as a data source within [!DNL Target], and that the correct report suite is selected.

   1. Set the **[!UICONTROL Priority]** to `High` or `999` to prevent conflicts when users in the test segment receive an incorrect on-site experience.


   1. Within **[!UICONTROL Reporting Settings]**, select the **[!UICONTROL Company Name]** and **[!UICONTROL Report Suite]** connected to your Search, Social, &amp; Commerce account.

      For additional reporting tips, see &quot;[Reporting best practices and troubleshooting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=pt-BR).&quot;

   1. In the **[!UICONTROL Date Range]** field, enter the appropriate start and end dates for the test.

   1. Select **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In the **[!UICONTROL Value]** field, enter the [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], or [!UICONTROL Network Ad ID] for the relevant ad network entity in Search, Social, &amp; Commerce. This allows you to use the [!DNL Target] query string parameters for click-through audiences for the entity.

      You can find the ID by [adding the relevant ID column to the entity view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view")

      Work with your Adobe Account Team if you need assistance.

   1. For the **[!UICONTROL Traffic Allocation Method]**, select **[!UICONTROL Manual (Default)]** and split the audience 50/50.

   1. Save the activity.

1. Use [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=pt-BR) to make design changes to the A/B test landing page template.

   * Experience A: Don&#39;t edit because it&#39;s the default/control landing page experience without personalization.

   * Experience B: Use the [!DNL Target] user interface to customize the landing page template based on the assets included in the test (such as headlines, copy, button placement, and creatives).

   >[!NOTE]
   >
   >For example creative test use cases, contact your Adobe Account Team.

## Step 2: Set up your [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) is a cross-solution integration that lets advertisers create [!DNL Target] activities based on [!DNL Analytics] conversion metrics and audience segments and then measure the results using [!DNL Analytics] as the reporting source. Todos os relatórios e segmentações para essa atividade são baseados na coleção de dados do [!DNL Analytics].

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para instruções de implementação, consulte &quot;[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=pt-BR)&quot;.

### Configurar o painel [!DNL Analytics for Target]

No Analysis Workspace, configure o [!DNL Analytics for Target panel] para analisar suas atividades e experiências do [!DNL Target]. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel no espaço de trabalho específico para a conta, campanha ou grupo de anúncios do Adobe Advertising <!-- only applicable entities? --> para o qual o teste foi executado. Use visualizações de resumo para mostrar métricas do Adobe Advertising no mesmo relatório que o desempenho de teste [!DNL Target].

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Adobe Advertising (como impressões, cliques e custos) não podem ser correspondidas às métricas [!DNL Target].

#### Dimensões

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **Atividades do Target**: nome do teste A/B

* **Experiências do Target**: Nomes das experiências da página de aterrissagem usadas na atividade

* **Atividade do Target** > **Experiência**: o nome da atividade e o nome da experiência na mesma linha

### Solução de problemas do Analytics para dados do [!DNL Target]

No Analysis Workspace, se você notar que os dados de atividade e experiências são mínimos ou não são preenchidos, faça o seguinte:

* Verifique se o mesmo [!UICONTROL Supplemental Data ID] (SDID) é usado para [!DNL Target] e [!DNL Analytics]. Você pode verificar os valores SDID usando a [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=pt-BR) na página de aterrissagem para a qual a campanha está direcionando usuários.

  [Valores da ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) o [!UICONTROL Hostname] exibido no Adobe Debugger em [!UICONTROL Solutions] > [!UICONTROL Target] corresponde b) o [!UICONTROL Tracking Server] exibido em [!DNL Target] para a atividade (em [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requer que um servidor de rastreamento [!DNL Analytics] seja enviado em chamadas de [!DNL Target] para o servidor de coleta de dados [!DNL Modstats] do Analytics.<!-- just "to Analytics?"-->

  [Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integrate Target with Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=pt-BR) - Explains how to set up [!DNL Target] reporting in Analysis Workspace.
* [A/B Test Overview](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=pt-BR) - Describes A/B test activities, which you can use with Search, Social, &amp; Commerce ads.
* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - Introduces [!DNL Analytics for Advertising], which allows you to track click-through and view-through site interactions in your Analytics instances.

>[!MORELIKETHIS]
>
>* [Configure A/B tests in Adobe Target for Advertising DSP ads](ab-tests-dsp.md)
