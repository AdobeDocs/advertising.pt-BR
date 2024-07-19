---
title: Código JavaScript para  [!DNL Analytics for Advertising]
description: Código JavaScript para  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising]

*Somente anunciantes com o Advertising DSP*

Para o Advertising DSP, a integração [!DNL Analytics for Advertising] rastreia interações de site view-through e click-through. As visitas click-through são rastreadas pelo código Adobe Analytics padrão em suas páginas da Web; o código [!DNL Analytics] captura os parâmetros de ID do AMO e ID do EF no URL da página de aterrissagem e os rastreia nos respectivos [!DNL eVars] reservados. Você pode rastrear visitas de view-through implantando um trecho do JavaScript em suas páginas da Web.

Na primeira exibição de página de uma visita ao site, o código Adobe Advertising JavaScript verifica se o visitante viu ou clicou anteriormente em um anúncio. Se o usuário tiver entrado anteriormente no site por um click-through ou não tiver visto um anúncio, o visitante será ignorado. Se o visitante tiver visto um anúncio e não tiver entrado no site por um click-through durante a [janela de pesquisa de cliques](/help/integrations/analytics/prerequisites.md#lookback-a4adc) definida no Adobe Advertising, o código JavaScript do Adobe Advertising a) usará o [Serviço de ID do Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para gerar uma ID complementar (`SDID`) ou b) usará o método Adobe Experience Platform [!DNL Web SDK] `generateRandomID` para gerar um `[!DNL StitchID]`. Qualquer ID é usada para compilar dados do Adobe Advertising na ocorrência do Adobe Analytics do visitante. Em seguida, o Adobe Analytics consulta o Adobe Advertising para a ID do AMO e a ID do EF associadas à exposição do anúncio. A ID do AMO e as IDs EF são preenchidas em seus respectivos [!DNL eVars]. Esses valores persistem por um período designado (por padrão, 60 dias).

[!DNL Analytics] envia métricas de tráfego do site (como exibições de página, visitas e tempo gasto) e qualquer evento personalizado ou padrão [!DNL Analytics] para Adobe Advertising por hora, usando a ID EF como chave. Essas [!DNL Analytics] métricas são executadas pelo sistema de atribuição do Adobe Advertising para conectar as conversões ao histórico de cliques e exposição.

>[!NOTE]
>
>A lógica de rastreamento do Adobe Advertising JavaScript ocorre no lado do Adobe e, portanto, praticamente não afeta o tempo de carregamento da página.
>
>Por outro lado, a lógica do conector de dados [!DNL DCM] para [!DNL Analytics] (usando [!DNL Google Campaign Manager 360]) para Advertising DSP ocorre no lado do cliente. A compilação no lado do cliente reduz o carregamento da página e aumenta o risco de perda de dados. Isso ocorre porque o JavaScript [!DNL Analytics] deve executar o ping de [!DNL DoubleClick] e esperar que [!DNL DoubleClick] retorne os últimos dados de clique/impressão para [!DNL Analytics]. Quando sua equipe do [!DNL DSP] configura o conector de dados do [!DNL DCM], você deve especificar quanto tempo você deseja atrasar a página.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Implantação do código JavaScript

A biblioteca JavaScript consiste em duas linhas que permitem que o [!DNL Analytics] e o Adobe Advertising se comuniquem entre si. Se a integração [!DNL Analytics for Advertising] foi concluída durante a implementação do Adobe Advertising, você já deve ter recebido esse código com instruções sobre como implantá-lo.

### O Código

#### Implementações que usam o código `visitorAPI.js` do Serviço de Identidade Experience Cloud

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementações que usam o código Experience Platform [!DNL Web SDK] `alloy.js`

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Onde colocar o código

A função JavaScript [!DNL Analytics for Advertising] deve vir após o Serviço de ID de Experience Cloud, mas antes do código de Medição do aplicativo Analytics. Isso garante que a ID complementar (`SDID`) ou `[!DNL StitchID]` esteja incluída na sua chamada do Analytics.

![Posicionamento do código](/help/integrations/assets/a4adc-code-placement.png)

### Validando a Implantação do Código

Você pode executar a validação usando qualquer tipo de ferramenta de farejador de pacotes (como [!DNL Charles], [!DNL Fiddler] ou [!DNL Chrome Developer Tools]) comparando os valores das quatro IDs entre a solicitação indo para Adobe Advertising e a solicitação indo para [!DNL Analytics], conforme descrito abaixo.

#### Como confirmar o código com [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abra [!DNL Chrome Developer Tools] e clique na guia **Rede**.

1. Carregue uma página de site que contenha o JavaScript [!DNL Analytics for Advertising].

1. Filtre a guia [!UICONTROL Network] por `last` e revise duas linhas:

   ![Filtrando no(s) último(s)](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * A primeira linha é a chamada para a biblioteca JavaScript e é denominada `last-event-tag-latest.min.js`.
   * A segunda linha é a chamada que envia a solicitação para o Adobe Advertising. Ele começa da seguinte forma: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Se você não vir a chamada para o Adobe Advertising, talvez não seja a primeira exibição de página da sua visita. Para fins de teste, você pode remover o cookie para que a próxima chamada seja a primeira exibição de página da visita correspondente:

   1. Na guia Aplicativo, localize o cookie `adcloud` e verifique se o cookie contém `_les_v` (última visita) com um valor de `y` e um carimbo de data e hora UTC que expira em 30 minutos.
      1. Exclua o cookie `adcloud` e atualize a página.

1. (Implementações que usam o código `visitorAPI.js` do serviço de identidade do Experience Cloud) Filtre em `/b/ss` para ver a ocorrência do Analytics.

   ![Filtrando em `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código) Filtrar em `/interact` para verificar se a carga da solicitação para o Edge Network contém `advertisingStitchID`.

   ![Filtrando em `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare os valores de ID entre as duas ocorrências. Todos os valores devem estar nos parâmetros da cadeia de caracteres de consulta, exceto a ID do conjunto de relatórios na ocorrência do Analytics, que é o caminho da URL imediatamente após `/b/ss/`.

   | ID | Parâmetro do Analytics | Edge Network | Parâmetro Adobe Advertising |
   | --- | --- | --- | --- |
   | Experience Cloud Organização IMS | `mcorgid` |  | `_les_imsOrgid` |
   | ID de dados complementares | sdid |  | `_les_sdid` |
   | ID da compilação | stitchId | `advertisingStitchID` na propriedade `_adcloud` |  |
   | Conjunto de relatórios do Analytics | O valor após `/b/ss/` | | `_les_rsid` |
   | ID de visitante Experience Cloud | mid |  | `_les_mid` |

   Se os valores de ID corresponderem, a implementação do JavaScript será confirmada. O Adobe Advertising envia ao servidor [!DNL Analytics] todos os detalhes de rastreamento de click-through ou view-through, se existirem.

#### Como confirmar o código com [!DNL Adobe Experience Cloud Debugger]

1. Abra o [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) em sua página inicial.
1. Vá para a guia [!UICONTROL Network].
1. Na barra de ferramentas [!UICONTROL Solutions Filter], clique em [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. Na linha de parâmetro [!UICONTROL Request URL - Hostname], localize `lasteventf-tm.everesttech.net`.
1. Na linha [!UICONTROL Request - Parameters], faça uma auditoria dos sinais gerados, semelhante à Etapa 3 em &quot;[Como confirmar o código com [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementações que usam o código `visitorAPI.js` do Experience Cloud Identity Service) Verifique se o parâmetro `Sdid` corresponde ao `Supplemental Data ID` no filtro Adobe Analytics.
   * (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código) Verifique se o valor do parâmetro `advertisingStitchID` corresponde ao `Sdid` enviado ao Edge Network Experience Platform.
   * Se o código não estiver sendo gerado, verifique se o cookie Adobe Advertising foi removido na guia [!UICONTROL Application]. Depois de removida, atualize a página e repita o processo.

   ![Auditando o código JavaScript [!DNL Analytics for Advertising] em [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]](prerequisites.md)
