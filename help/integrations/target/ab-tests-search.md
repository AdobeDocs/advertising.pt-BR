---
title: Configurar testes A/B para anúncios de pesquisa, sociais e do Commerce do Adobe Advertising no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para seu [!DNL Google Ads] e [!DNL Microsoft® Advertising] anúncios em Pesquisa, Social e Comércio.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para anúncios de pesquisa de publicidade, sociais e do Commerce

*Anunciantes com somente Advertising Search, Social e Commerce*

*[!DNL Google Ads]e [!DNL Microsoft® Advertising] somente contas*

O Adobe Advertising e o Adobe Target facilitam a configuração de testes A/B de experiência de página de aterrissagem para tráfego de publicidade digital [!DNL Google Ads] e [!DNL Microsoft® Advertising] para:

* Melhorar as taxas de conversão (CVR) e as medidas de eficiência de aquisição (como CPA, CPL e CAC).

* Ofereça uma experiência de página de aterrissagem mais personalizada que seja relevante para o anúncio (por exemplo, corresponder o criativo da imagem/vídeo, a cópia, a palavra-chave ou outro sinal de publicidade à página de aterrissagem).

Também é possível combinar o nativo [[!DNL Analytics] para publicidade](/help/integrations/analytics/overview.md) e [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) dimensões de relatório de integração integradas ao Adobe Analytics para medir e visualizar seus dados de teste com [!DNL Analytics] métricas e eventos de sucesso.

Consulte as seções a seguir para obter os pré-requisitos, instruções para configurar testes A/B no [!DNL Target] para tráfego de click-through de anúncios em Pesquisa, Social e Comércio, e dicas sobre como medir e visualizar seus testes em [!DNL Analytics].

## Pré-requisitos

### Produtos necessários

* Pesquisa, Social e Comércio
* [!DNL Target]

### Produtos e integrações recomendados

* [!DNL Analytics]

* [[!DNL Analytics] para publicidade](/help/integrations/analytics/overview.md) integração<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integração

## Etapa 1: criar uma atividade de teste A/B no [!DNL Target] para pesquisa, redes sociais e comércio

As instruções a seguir destacam informações relacionadas ao caso de uso de Pesquisa, Social e Comércio.

1. [Fazer logon no Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Criar um teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. No **[!UICONTROL Enter Activity URL]** insira o URL da página inicial do teste.

   1. No **[!UICONTROL Goal]** insira a métrica de sucesso do teste.

      >[!NOTE]
      >
      >Verifique se [!DNL Analytics] está ativado como uma fonte de dados no [!DNL Target]e que o conjunto de relatórios correto está selecionado.

   1. Defina o **[!UICONTROL Priority]** para `High` ou `999` para evitar conflitos quando os usuários no segmento de teste recebem uma experiência incorreta no site.


   1. Dentro de **[!UICONTROL Reporting Settings]**, selecione o **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** conectado à sua conta do Search, Social e Commerce.

      Para obter dicas adicionais sobre relatórios, consulte &quot;[Relatório de práticas recomendadas e solução de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. No **[!UICONTROL Date Range]** insira as datas de início e término apropriadas para o teste.

   1. Selecionar **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. No **[!UICONTROL Value]** insira o [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID]ou [!UICONTROL Network Ad ID] para a entidade de rede de anúncios relevante em Pesquisa, Social e Comércio. Isso permite usar o [!DNL Target] parâmetros de cadeia de caracteres de consulta para públicos-alvo de click-through da entidade.

      Você pode encontrar a ID por [adicionar a coluna de ID relevante à visualização de entidade](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] na [!UICONTROL Accounts] exibir](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] na [!UICONTROL Accounts] exibir")

      Entre em contato com a equipe de conta do Adobe se precisar de assistência.

   1. Para o **[!UICONTROL Traffic Allocation Method]**, selecione **[!UICONTROL Manual (Default)]** e dividir o público em 50 horas.

   1. Salve a atividade.

1. Uso [Visual Experience Composer do Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para fazer alterações de design no modelo da landing page de teste A/B.

   * Experiência A: não edite porque é a experiência padrão/de controle da página de aterrissagem sem personalização.

   * Experiência B: usar o [!DNL Target] interface para personalizar o modelo de página de aterrissagem com base nos ativos incluídos no teste (como títulos, cópia, posicionamento de botões e criação).

   >[!NOTE]
   >
   >Por exemplo, casos de uso de testes criativos, entre em contato com a equipe de conta do Adobe.

## Etapa 2: configurar o [!DNL Analytics for Target] Analysis Workspace em [!DNL Analytics]

[!DNL Analytics for Target] (A4T) é uma integração entre soluções que permite que os anunciantes criem [!DNL Target] atividades baseadas em [!DNL Analytics] métricas de conversão e segmentos de público-alvo e, em seguida, medir os resultados usando [!DNL Analytics] como fonte de relatórios. Todos os relatórios e segmentações dessa atividade são baseados no [!DNL Analytics] coleção de dados.

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para instruções de implementação, consulte &quot;[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurar o [!DNL Analytics for Target] Painel

No Analysis Workspace, configure o [!DNL Analytics for Target panel] para analisar o [!DNL Target] atividades e experiências. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel no espaço de trabalho específico para a conta, campanha ou grupo de anúncios do Adobe Advertising<!-- only applicable entities? --> para o qual o teste foi executado. Use as visualizações de resumo para mostrar as métricas de Adobe Advertising no mesmo relatório que a [!DNL Target] desempenho do teste.

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Adobe Advertising (como impressões, cliques e custos) não podem ser correspondidas ao [!DNL Target] métricas.

#### Dimension

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **Atividades do Target**: nome do teste A/B

* **Experiências do Target**: nomes das experiências de página de aterrissagem usadas na atividade

* **Atividade do Target** > **Experiência**: o nome da atividade e o nome da experiência na mesma linha

### Solução de problemas do Analytics para [!DNL Target] Dados

No Analysis Workspace, se você notar que os dados de atividade e experiências são mínimos ou não são preenchidos, faça o seguinte:

* Verifique se o mesmo [!UICONTROL Supplemental Data ID] (SDID) é usada para ambos [!DNL Target] e [!DNL Analytics]. É possível verificar os valores de SDID usando o [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) na página de aterrissagem para a qual a campanha está direcionando usuários.

[Valores de ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) a variável [!UICONTROL Hostname] mostrado na Adobe Debugger em [!UICONTROL Solutions] > [!UICONTROL Target] corresponde a b) o [!UICONTROL Tracking Server] mostrado em [!DNL Target] para a atividade (em [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] exige um [!DNL Analytics] servidor de rastreamento a ser enviado em chamadas de [!DNL Target] para o [!DNL Modstats] servidor de coleta de dados para o Analytics.<!-- just "to Analytics?"-->

[Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integração do Target ao Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explica como configurar [!DNL Target] relatórios no Analysis Workspace.
* [Visão geral do teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Descreve as atividades de teste A/B, que você pode usar com os anúncios de Pesquisa, Social e Comércio.
* [Visão geral do Analytics for Advertising](/help/integrations/analytics/overview.md) : apresenta o Analytics for Advertising, que permite rastrear interações do site de click-through e view-through nas instâncias do Analytics.

>[!MORELIKETHIS]
>
>* [Configurar testes A/B no Adobe Target para anúncios DSP](ab-tests-dsp.md)
