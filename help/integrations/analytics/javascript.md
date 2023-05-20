---
title: Código JavaScript para [!DNL Analytics for Advertising]
description: Código JavaScript para [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 96b71e8c99ee30254b4bdc4ef0cb8af359f64c5e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising]

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

*Anunciantes com somente DSP publicitário*

Para a publicidade do DSP, a [!DNL Analytics for Advertising] A integração do rastreia as interações do site de view-through e click-through. As visitas click-through são rastreadas pelo código Adobe Analytics padrão em suas páginas da Web; a variável [!DNL Analytics] O código do captura os parâmetros ID do AMO e ID do EF no URL da página de aterrissagem e os rastreia em suas respectivas eVars reservadas. Você pode rastrear visitas view-through implantando um trecho JavaScript nas páginas da Web.

Na primeira exibição de página de uma visita ao site, o código JavaScript do Adobe Advertising verifica se o visitante viu ou clicou anteriormente em um anúncio. Se o usuário tiver entrado anteriormente no site por um click-through ou não tiver visto um anúncio, o visitante será ignorado. Se o visitante tiver visto um anúncio e não tiver entrado no site por um click-through durante o [clique em janela de retrospectiva](/help/integrations/analytics/prerequisites.md#lookback-a4adc) definido no Adobe Advertising, o código JavaScript do Adobe Advertising a) usa a variável [Serviço de ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para gerar uma ID complementar (`SDID`) ou b) usa o Adobe Experience Platform [!DNL Web SDK] `generateRandomID` método para gerar um `[!DNL StitchID]`. Ambas as IDs são usadas para compilar dados da publicidade do Adobe com a ocorrência do Adobe Analytics do visitante. Em seguida, a Adobe Analytics consulta a Adobe Advertising para a AMO ID e EF ID associadas à exposição do anúncio. A ID do AMO e as IDs do EF são preenchidas nas respectivas eVars. Esses valores persistem por um período designado (por padrão, 60 dias).

[!DNL Analytics] envia métricas de tráfego do site (como exibições de página, visitas e tempo gasto) e qualquer [!DNL Analytics] eventos personalizados ou padrão para o Adobe Advertising por hora, usando a ID EF como a chave. Esses [!DNL Analytics] As métricas são executadas pelo sistema de atribuição Adobe Advertising para conectar as conversões ao histórico de cliques e exposição.

>[!NOTE]
>
>A lógica de rastreamento do JavaScript do Adobe Advertising ocorre no lado do Adobe e, portanto, praticamente não afeta o tempo de carregamento da página.
>
>Em contrapartida, a lógica da [!DNL DCM] conector de dados para [!DNL Analytics] (usando [!DNL Google Campaign Manager 360]) para Advertising DSP ocorre no lado do cliente. A compilação no lado do cliente reduz o carregamento da página e aumenta o risco de perda de dados. Isso ocorre porque [!DNL Analytics] É necessário fazer ping no JavaScript [!DNL DoubleClick] e aguardar [!DNL DoubleClick] para transmitir os últimos dados de clique/impressão para [!DNL Analytics]. Quando o [!DNL DSP] a equipe configura o [!DNL DCM] conector de dados, você deve especificar quanto tempo você deseja atrasar a página.

## Implantação do código JavaScript

A biblioteca do JavaScript do consiste em duas linhas que permitem [!DNL Analytics] e a Adobe Advertising para se comunicar entre si. Se a variável [!DNL Analytics for Advertising] A integração foi concluída durante a implementação do Adobe Advertising, portanto, esse código já deve ter sido recebido com instruções sobre como implantá-lo.

### O Código

#### Implementações que usam o serviço de identidade Experience Cloud `visitorAPI.js` código

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`código

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Onde colocar o código

A variável [!DNL Analytics for Advertising] A função JavaScript deve vir após o Serviço de ID do Experience Cloud, mas antes do código de medição do aplicativo do Analytics. Isso garante que a ID complementar (`SDID`ou `[!DNL StitchID]` está incluído na sua chamada do Analytics.

![Inserção de código](/help/integrations/assets/a4adc-code-placement.png)

### Validando a Implantação do Código

Você pode executar a validação usando qualquer tipo de ferramenta de sniffer de pacote (como [!DNL Charles], [!DNL Fiddler]ou [!DNL Chrome Developer Tools]) comparando os valores das quatro IDs entre a solicitação que vai para o Adobe Advertising e a solicitação que vai para o [!DNL Analytics], conforme descrito abaixo.

#### Como confirmar o código com [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abertura [!DNL Chrome Developer Tools] e clique no link **Rede** guia.

1. Carregar uma página do site que contenha a [!DNL Analytics for Advertising] JavaScript.

1. Filtre o [!UICONTROL Network] guia por `last` e revise duas linhas:

   ![Filtragem nos últimos](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * A primeira linha é a chamada para a biblioteca do JavaScript e é intitulada `last-event-tag-latest.min.js`.
   * A segunda linha é a chamada que envia a solicitação para a Adobe Advertising. Ele começa da seguinte maneira: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Se você não vir a chamada para a Adobe Advertising, talvez não seja a primeira exibição de página da sua visita. Para fins de teste, você pode remover o cookie de modo que a próxima chamada seja a primeira exibição de página da visita correspondente:
   1. Na guia Aplicativo, localize o `adcloud` cookie e verifique se o cookie contém `_les_v` (última visita) com um valor de `y` e um carimbo de data e hora UTC que expira em 30 minutos.
      1. Exclua o `ad cloud` cookie e atualiza a página.


1. (Implementações que usam o serviço de identidade Experience Cloud) `visitorAPI.js` code) Filtrar em `/b/ss` para ver a ocorrência do Analytics.

   ![Filtragem ativada `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`code) Filtrar em `/interact` para verificar se a carga da solicitação para a Rede de borda contém `advertisingStitchID`.

   ![Filtragem ativada `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare os valores de ID entre as duas ocorrências. Todos os valores estarão em parâmetros de sequência de consulta, exceto a ID do conjunto de relatórios na ocorrência do Analytics, que é o caminho do URL imediatamente após `/b/ss/`.

   | ID | Parâmetro do Analytics | Rede de borda | Parâmetro de publicidade do Adobe |
   | --- | --- | --- | --- |
   | Experience Cloud Organização IMS | `mcorgid` |  | `_les_imsOrgid` |
   | ID de dados complementares | sdid |  | `_les_sdid` |
   | ID da compilação | stitchId | `advertisingStitchID` no `_adcloud` propriedade |  |
   | Conjunto de relatórios do Analytics | O valor depois de `/b/ss/` |  | `_les_rsid` |
   | ID de visitante Experience Cloud | mid |  | `_les_mid` |

   Se os valores de ID corresponderem, a implementação do JavaScript será confirmada. A Adobe Advertising enviará o [!DNL Analytics] servidor quaisquer detalhes de rastreamento de click-through ou view-through, se existirem.

#### Como confirmar o código com [!DNL Adobe Experience Cloud Debugger]

1. Abra o [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) na sua página inicial.
1. Vá para a [!UICONTROL Network] guia.
1. No [!UICONTROL Solutions Filter] barra de ferramentas, clique [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. No [!UICONTROL Request URL – Hostname] linha de parâmetro, localizar `lasteventf-tm.everesttech.net`.
1. No [!UICONTROL Request – Parameters] linha, audite os sinais gerados, semelhante à Etapa 3 em &quot;[Como confirmar o código com [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementações que usam o serviço de identidade Experience Cloud) `visitorAPI.js` código) Verifique se o `Sdid` O parâmetro do corresponde ao `Supplemental Data ID` no filtro Adobe Analytics.
   * (Implementações que usam o Experience Platform [!DNL Web SDK] `alloy.js`code) Verifique se o valor do campo `advertisingStitchID` O parâmetro do corresponde ao `Sdid` enviado para a Rede de borda do Experience Platform.
   * Se o código não estiver sendo gerado, verifique se o cookie do Adobe Advertising foi removido na variável [!UICONTROL Application] guia. Depois de removida, atualize a página e repita o processo.

   ![Auditoria [!DNL Analytics for Advertising] Código JavaScript no [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Pré-requisitos e informações-chave para implementação do [!DNL Analytics for Advertising]](prerequisites.md)

