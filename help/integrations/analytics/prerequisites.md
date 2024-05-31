---
title: Pré-requisitos e informações-chave para implementação do [!DNL Analytics for Advertising]
description: Pré-requisitos e informações-chave para implementação do [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 63b91d84118c6b84fe72ae1c3ac1a9f68d7201fc
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%

---

# Pré-requisitos e informações-chave para implementação do [!DNL Analytics for Advertising]

*Anunciantes com DSP e[!DNL Advertising Search, Social, & Commerce]*

Analise as informações a seguir antes de integrar o Adobe Advertising ao Adobe Analytics.

## Requisitos para relatórios de dados do Adobe Advertising no [!DNL Analytics]

* Qualquer uma das seguintes opções:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Serviço de identidade Experience Cloud: `visitorAPI.js` versão 2.0 ou superior
* Qualquer versão do Adobe Analytics (incluindo [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versão 2.1 ou superior
* (Clientes de publicidade DSP) Uma [Anunciando trecho JavaScript do DSP](javascript.md) implantado em suas páginas da web para rastrear visitas de view-through.
* O parâmetro da ID do AMO nos URLs de rastreamento dos seus anúncios.

  O parâmetro é adicionado automaticamente aos URLs de rastreamento em algumas circunstâncias, mas pode ser necessário adicioná-lo manualmente. Em &quot;Adobe Advertising IDs Used by [!DNL Analytics]/help/integrations/analytics/ids.md,&quot; consulte &quot;[Formas de implementação da ID do AMO](/help/integrations/analytics/ids.md#amo-id-implement).&quot;

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente de cada biblioteca.

## Requisitos para o compartilhamento de segmentos do Analytics com o Adobe Advertising

* Serviço de identidade Experience Cloud: `visitorAPI.js` versão 2.1 ou superior
* Adobe Analytics: `appMeasurement.js` versão 1.8 ou superior

## Requisitos para relatórios [!DNL Analytics] Dados no Adobe Advertising

Forneça o seguinte à equipe de implementação do Adobe Advertising:

* A variável [!DNL Analytics] ID do conjunto de relatórios a ser usada para relatórios sobre a atividade de mídia paga e para alimentar a atividade do site para otimização e relatórios no Adobe Advertising
* A ID da organização Experience Cloud da empresa (ID da organização).

Você pode encontrar ambas as IDs no [Guia Resumo do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dados no Adobe Advertising {#lookback-a4adc}

Porque [!DNL Analytics] Os dados do são enviados para o Adobe Advertising para relatórios e otimização, os dados estão sujeitos às regras de atribuição, incluindo as janelas de retrospectiva de impressão e clique, que são configuradas para o anunciante no Adobe Advertising.

![configurações da janela de retrospectiva no nível do anunciante no Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Janela de retrospectiva de clique para atribuição de Adobe Advertising: o número de dias após o primeiro clique em que o clique pode ser atribuído a uma conversão. Por padrão, esse valor é 60 dias; o máximo é 90 dias
* Janela de retrospectiva de impressão de atribuição de Adobe Advertising: o número de dias após a ocorrência de uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. Por padrão, esse valor é 14 dias; o máximo é 30 dias

  >[!NOTE]
  >
  > A janela de retrospectiva de impressão é específica do Adobe Advertising, não [!DNL Analytics for Advertising], relatórios.

A variável [!DNL Analytics for Advertising] O JavaScript usa essas configurações para determinar até que ponto considerar uma entrada view-through ou entrada click-through para o site como válida. Para obter mais informações sobre como view-throughs e click-throughs são determinados, consulte &quot;[IDs de Adobe Advertising usadas pelo Analytics](ids.md).&quot;

## Entrada de dados Adobe Advertising [!DNL Analytics]

[!DNL Analytics] O define IDs de Adobe Advertising (IDs AMO) na ocorrência do Analytics, sujeitas às solicitações [!DNL eVar] configuração de persistência, que se aplica a click-throughs e view-throughs. A configuração de persistência está definida no back-end do Adobe Advertising e sua equipe de conta do Adobe pode alterá-la.

* [!DNL Analytics for Advertising] [!DNL eVar] expiração: 60 dias por padrão para IDs do AMO

>[!NOTE]
>
>Para segmentar dados para um período diferente, é possível [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) com diferentes janelas de pesquisa no Analysis Workspace.

## Ambientes de anúncios compatíveis

* Pesquisar
* Exibir
* Vídeo
* Vídeo online
* Nativo

Entre em contato com a equipe de conta do Adobe para obter os ambientes de anúncios mais recentes compatíveis em cada canal.

## O que você deve saber antes da implementação

* A equipe de implementação do Adobe Advertising configura a integração.

* Não serão cobrados custos adicionais por essa integração, nem as chamadas do servidor resultarão em custos adicionais [!DNL Analytics] ou Adobe Advertising.

* [!DNL Analytics for Advertising] é independente de servidor de anúncios: um view-through ou click-through pode ocorrer a partir de qualquer servidor de anúncios, e as IDs adequadas são geradas após a entrada do site.

* A integração passa somente pelo [!DNL Analytics] eventos padrão e personalizados para o Adobe Advertising para otimização de oferta de mídia paga e esforços de publicidade subsequentes. Não passa [!DNL Analytics] segmentos, métricas calculadas e [!DNL eVars] para Adobe Advertising para otimização de oferta.

* O Adobe Advertising cria IDs persistentes no [!DNL Analytics] com base no último anúncio clicado ou exibido antes que o usuário entre no site, com base no [janelas de retrospectiva de click-through e view-through](#lookback-a4adc) configurado no Adobe Advertising. Se um visitante do site tiver ambos os tipos de interações de entrada de site em seu perfil e o clique estiver dentro do período de lookback, a ID de click-through do visitante substituirá a ID de view-through para relatórios do site.

* [!DNL Analytics for Advertising] o rastreamento de conversão no Adobe Analytics usa uma janela de pesquisa de rastreamento configurável (60 dias por padrão). Os relatórios de Adobe Advertising refletem conversões e engajamento do site até o final desta janela de retrospectiva de rastreamento.

* Todos os tipos de anúncios são compatíveis. No entanto, nem todos os ambientes de anúncios são compatíveis.

  Por exemplo, anúncios de TV conectada (CTV) não são rastreados porque nenhum clique ocorre em CTV e nenhuma conversão pode ocorrer no mesmo dispositivo. No entanto, se o anúncio for visualizado em um ambiente de desktop, alguns dados de entrada do site de view-through poderão ser rastreados.

* [!DNL Analytics] no momento, as conversões são rastreadas e atribuídas apenas a um visitante no mesmo dispositivo.

* [!DNL Analytics for Advertising] O não oferece suporte a conversões de view-through no aplicativo.

* O rastreamento de view-through não é compatível com anunciantes que usam uma implementação de encaminhamento pelo lado do servidor do [!DNL Analytics].

### ID suplementar

Depois que o Serviço de identidade do Experience Cloud é implementado em um site, as ocorrências que contêm dados de [!DNL Analytics] ou Adobe Advertising contêm uma ID complementar.

Exemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para uma integração de dados precisa, todas as chamadas de Adobe Advertising usadas por um [!DNL Analytics for Advertising] atividade para fornecer conteúdo ou registrar, a métrica de meta deve ter uma [!DNL Analytics] que compartilha a mesma ID complementar.

Quando estiver solucionando problemas no [!DNL Analytics], confirme se a ID complementar está presente para [!DNL Analytics] ocorrências. No [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), você poderá ver essa ID na guia Adobe Advertising como a variável `sdid` parâmetro.

>[!NOTE]
>
> Esta implementação funciona de forma semelhante à [!DNL Analytics for Target] integração.

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para o Analytics para publicidade](/help/integrations/analytics/javascript.md)
