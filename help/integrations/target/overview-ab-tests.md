---
title: Configurar testes A/B para anúncios publicitários em Adobe no Adobe Target
description: Saiba como configurar um teste A/B no [!DNL Target] para o seu DSP e [!DNL Search] anúncios.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: f6308ac9af8019987f4a2e501cba6b019cb032b6
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# Configurar testes A/B no Adobe Target para DSP de publicidade e [!DNL Advertising Search] Anúncios

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Anunciantes com somente DSP publicitário*

A Adobe Advertising e a Adobe Target facilitam ainda mais para os profissionais de marketing o fornecimento de uma experiência personalizada e conectada em mídia paga e mensagens no site. Ao compartilhar sinais entre os produtos, você pode:

* Diminuir as taxas de fallthrough do site, vinculando a exposição dos anúncios dos clientes das campanhas de DSP às suas experiências no site.

* Estabeleça testes A/B espelhando experiências no site com mensagens de publicidade usando dados de exposição do Adobe Audience Manager e públicos-alvo do tipo clique para alimentar.

* Meça o impacto da Unificação de Mensagens em um aumento de objetivos no site com visualizações simples no Adobe Analytics para [!DNL Target].

Consulte as seções a seguir para obter os pré-requisitos e instruções para configurar o rastreamento de click-through e view-through, implementar o compartilhamento de sinal entre o DSP e o [!DNL Target] e configurar uma atividade de teste A/B e configurar [!DNL Analytics] Analysis Workspace para visualizar os dados de teste.

Em caso de dúvidas adicionais, entre em contato com adcloud_support@adobe.com.

## Pré-requisitos

Este caso de uso requer os seguintes produtos e integrações:

* [!DNL Target]

* [[!DNL Analytics] para publicidade](/help/integrations/analytics/overview.md) integração<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integração

* Audience Manager (obrigatório somente para teste view-through)

## Etapa 1: configurar a Estrutura Click-through {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Estrutura de click-through](/help/integrations/assets/target-ct-framework.png)

Quando você adiciona macros DSP a um URL de click-through (o URL exibido quando um usuário clica em um anúncio e chega à página inicial), DSP captura automaticamente a chave de posicionamento incluindo `${TM_PLACEMENT_ID}` no URL de click-through. Esta macro captura a chave de posicionamento alfanumérico e não a ID de posicionamento numérico.

![URL de click-through anexado ao URL da página inicial](/help/integrations/assets/target-ct-url.jpg)

### (Somente DSP) Adicione macros DSP aos URLs de click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Em conversa com o Flash ou no Google Campaign Manager 360, atualize manualmente o URL de click-through para cada anúncio a fim de incluir as macros necessárias para capturar as variáveis de ID do AMO. As variáveis de ID do AMO são usadas para enviar dados de cliques para o Adobe Analytics e compartilhar chaves de posicionamento para testes A/B. Consulte as seguintes páginas para obter instruções:

* [Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade](/help/integrations/analytics/macros-flashtalking.md)

* [Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade](/help/integrations/analytics/macros-google-campaign-manager.md)

Entre em contato com a equipe de conta do Adobe e com o Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) para recuperar a chave de posicionamento necessária e finalizar a configuração e garantir que cada URL de click-through seja preenchido com a chave de posicionamento.

## Etapa 2: Configurar a estrutura de view-through usando o Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Estrutura de view-through](/help/integrations/assets/targetr-vt-framework.png)

Ao adicionar um pixel de evento de impressão de Audience Manager nas tags de anúncio e configurações de posicionamento, é possível criar um segmento de teste para oportunidades de teste de view-through adicionais.

1. Implemente um pixel de evento de impressão de Audience Manager nas tags de anúncio e configurações de posicionamento de DSP.

   Para obter instruções, consulte &quot;[Coletar dados de exposição da mídia de campanhas de publicidade com DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Certifique-se de adicionar [Macros do DSP](/help/dsp/campaign-management/macros.md) para capturar todos os dados que você deseja que o pixel de evento de impressão retorne, incluindo `${TM_PLACEMENT_ID_NUM}` para a ID de posicionamento numérico.

   >[!NOTE]
   >
   >Os URLs de rastreamento de cliques incluem o `${TM_PLACEMENT_ID}` macro para a chave de posicionamento alfanumérico, em vez de `${TM_PLACEMENT_ID_NUM}` para a ID de posicionamento numérico.

1. Configure um segmento Audience Manager a partir dos dados de impressão do DSP:

   1. Ir para **Audience Manager** > **Dados de público-alvo** > **Sinais** e selecione a variável **Pesquisar** no canto superior esquerdo.

   1. Insira o **Chave** e **Valor** para o sinal que determina em qual nível os usuários do segmento são agrupados. Use um [chave suportada](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) com um valor que corresponda a uma macro adicionada ao pixel de evento de impressão de Audience Manager.

      Por exemplo, para agrupar usuários para uma disposição específica, use o `d_placement` chave. Para o valor, use uma ID de posicionamento numérico real (como 2501853 na captura de tela acima) capturada pela macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Se o campo Contagem total mostrar contagens de usuários para o par de valores chave, o que indica que o pixel foi colocado corretamente e os dados estão fluindo, você pode continuar para a próxima etapa.
   ![Procurar sinais](/help/integrations/assets/target-am-signals.png)

1. [Criar uma característica com base em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) para criação de segmento no Audience Manager.

   1. Nomeie a característica para que seja facilmente identificável nas atividades de teste. Armazene a característica na pasta que preferir.

   1. No **Fonte de dados** selecione **Ad Cloud**.

   1. No Construtor de expressões, adicione `d_event` no campo Chave e `imp` no **Valor** selecione **Adicionar regra** e salve a característica.

   ![Captura de tela de uma característica com base em regras](/help/integrations/assets/target-am-trait.png)

1. Configurar um segmento de teste no Audience Manager:

   1. Na parte superior da página, acesse **Dados de público-alvo** > **Características** e pesquise pelo nome completo da característica. Marque a caixa de seleção ao lado do nome da característica e clique em **Criar segmento**.

   1. Nomeie o segmento, selecione `Ad Cloud` como o **Fonte de dados** e salve o segmento.

      O Audience Manager divide automaticamente o segmento em um grupo de controle que recebe a experiência padrão de página de aterrissagem e um grupo de teste que recebeu uma experiência personalizada no local.
   ![Captura de tela de um segmento de teste](/help/integrations/assets/target-am-segment.png)

## Etapa 3: configurar uma atividade &quot;Teste A/B&quot; no Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

As instruções a seguir destacam informações relacionadas ao caso de uso do DSP. Para obter instruções completas, consulte &quot;[Criar um teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)&quot;.

1. [Faça logon no Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. No **Atividades** clique em **Criar atividade** > **Teste A/B**.

   ![Criar uma atividade de Teste A/B](/help/integrations/assets/target-create-ab.png)

1. No **Inserir URL da atividade***, insira o URL da página inicial do teste.

   ![Insira o campo URL da atividade](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Você pode usar vários URLs para testar a entrada do site de view-through. Para obter mais informações, consulte &quot;[Atividade multipáginas](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Você pode identificar facilmente as principais entradas por URL de página criando uma [Relatório de Entrada de Site](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) no Analytics.

1. No **Meta** insira a métrica de sucesso do teste.

   >[!NOTE]
   >
   >Verifique se [!DNL Analytics] está ativado como uma fonte de dados no [!DNL Target]e que o conjunto de relatórios correto está selecionado.

1. Defina o **Prioridade** para `High` ou `999` para evitar conflitos quando os usuários no segmento de teste recebem uma experiência incorreta no site.

1. Dentro de **Configurações de relatório**, selecione o **Nome da empresa** e **Report Suite** conectado à sua conta DSP.

   Para obter dicas adicionais sobre relatórios, consulte &quot;[Relatório de práticas recomendadas e solução de problemas](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. No **Intervalo de datas** insira as datas de início e término apropriadas para o teste.

1. Adicionar públicos-alvo à atividade:

   1. Escolha o [segmento criado anteriormente no Audience Manager para testar públicos-alvo de view-through](#view-through-framework).

      ![Adicionar públicos-alvo à atividade](/help/integrations/assets/target-create-ab-audiences.png)

   1. Selecionar **Páginas do site** > **Landing Page** > **Query** e insira a chave de posicionamento do DSP no **Valor** para usar os parâmetros da cadeia de caracteres de consulta do Target para públicos-alvo de click-through.

      ![Captura de tela de um público-alvo de cliques](/help/integrations/assets/target-click-audience.jpg)

1. Para o **Método de alocação de tráfego**, selecione **Manual (Padrão)** e dividir o público em 50 horas.

1. Salve a atividade.

1. Uso [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para fazer alterações de design no modelo da landing page de teste A/B.

   * Experiência A: não edite porque é a experiência padrão/de controle da página de aterrissagem sem personalização.

   * Experiência B: usar o [!DNL Target] interface para personalizar o modelo de página de aterrissagem com base nos ativos incluídos no teste (como títulos, cópia, posicionamento de botões e criação).
   >[!NOTE]
   >
   >Por exemplo, casos de uso de testes criativos, entre em contato com a equipe de conta do Adobe.

## Etapa 4: configurar o [!DNL Analytics for Target] Analysis Workspace em [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) é uma integração entre soluções que permite que os anunciantes criem [!DNL Target] atividades baseadas em [!DNL Analytics] métricas de conversão e segmentos de público-alvo e, em seguida, medir os resultados usando [!DNL Analytics] como fonte de relatórios. Todos os relatórios e segmentações dessa atividade são baseados no [!DNL Analytics] coleção de dados.

Para obter mais informações sobre [!DNL Analytics for Target], incluindo um link para as instruções de implementação, consulte &quot;[Adobe Analytics como origem de relatório do Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurar o [!DNL Analytics for Target] Painel

No Analysis Workspace, configure o [!DNL Analytics for Target panel] para analisar o [!DNL Target] atividades e experiências. Lembre-se dos seguintes pontos importantes e informações sobre seus relatórios.

#### Métricas

* Crie um painel no espaço de trabalho específico para a campanha, o pacote ou a disposição de anúncio do Adobe para o qual o teste foi executado. Use as visualizações de resumo para mostrar as métricas de Anúncios de Adobe no mesmo relatório que o desempenho do teste do Target.

* Priorize o uso de métricas no site (como visitas e conversões) para medir o desempenho.

* Entenda que as métricas de mídia agregada do Adobe Advertising (como impressões, cliques e custos) não podem ser correspondidas às métricas do Target.

#### Dimension

As seguintes dimensões pertencem a [!DNL Analytics for Target]:

* **Atividades do Target**: nome do teste A/B

* **Experiências do Target**: nomes das experiências de página de aterrissagem usadas na atividade

* **Atividade do Target** > **Experiência**: o nome da atividade e o nome da experiência na mesma linha

### Solução de problemas do Analytics para [!DNL Target] Dados

No Analysis Workspace, se você notar que os dados de atividade e experiências são mínimos ou não são preenchidos, faça o seguinte:

* Verifique se a mesma ID de Dados Suplementares (SDID) é usada para o Target e para o Analytics. É possível verificar os valores de SDID usando o [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) na página de aterrissagem para a qual a campanha está direcionando usuários.

[Valores de ID de dados complementares (SDID) no Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Na mesma página de aterrissagem, verifique se a) o Nome do host mostrado no Depurador do Adobe em Soluções> Target corresponde b) o Servidor de rastreamento mostrado em [!DNL Target] para a atividade (em Metas e configurações > Configurações de relatórios).

   [!DNL Analytics For Target] exige um [!DNL Analytics] servidor de rastreamento a ser enviado em chamadas de [!DNL Target] para o [!DNL Modstats] servidor de coleta de dados para o Analytics.<!-- just "to Analytics?"-->

[Valor do nome do host no Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor do servidor de rastreamento no Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Leitura adicional

* [Integração do Target ao Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Explica como configurar relatórios do Target no Analysis Workspace.
* [Visão geral do teste A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Descreve as atividades de teste A/B, que podem ser usadas com anúncios DSP.
* [Experiências e ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explica [!DNL Target] ferramentas para determinar o conteúdo no local ao qual os usuários de teste de DSP estão expostos.
* [Sinais, características e segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Define algumas das ferramentas de Audience Manager que podem ajudar no teste de view-through do DSP.
* [Visão geral do Analytics for Advertising](/help/integrations/analytics/overview.md) : apresenta o Analytics for Advertising, que permite rastrear interações do site de click-through e view-through nas instâncias do Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
