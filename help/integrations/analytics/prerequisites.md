---
title: Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]
description: Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]

*Anunciantes com DSP de publicidade e[!DNL Advertising Search, Social, & Commerce]*

Analise as seguintes informações antes de integrar a Adobe Systems Advertising com o Adobe Analytics.

## Requisitos para relatórios Adobe Systems dados de publicidade em [!DNL Analytics]

* Um dos itens a seguir:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Serviço de identidade: `visitorAPI.js` versão 2.0 ou superior
* Qualquer versão de Adobe Analytics (incluindo [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versão 2.1 ou superior
* (Clientes do DSP de publicidade) Um [snippet](javascript.md) do Advertising DSP JavaScript implantado em suas páginas da Web para faixa visualização-through de visitas.

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente de cada biblioteca.

## Requisitos para compartilhar segmentos Analytics com a Adobe Systems publicidade

* Experience Cloud Serviço de identidade: `visitorAPI.js` versão 2.1 ou superior
* Adobe Analytics: `appMeasurement.js` versão 1.8 ou superior

## Requisitos para relatórios de [!DNL Analytics] dados no Adobe Systems Advertising

Forneça o Adobe Systems Advertising implementação equipe com o seguinte:

* O [!DNL Analytics] ID de conjunto de relatórios para uso para relatórios no mídia paga atividade e para alimentar atividade do site para otimização e relatórios na Adobe Systems Advertising
* A ID da organização Experience Cloud do empresa (ID organizacional).

Você pode encontrar ambas as IDs na [guia Resumo do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dados em publicidade Adobe Systems {#lookback-a4adc}

Como [!DNL Analytics] os dados são enviados para a Adobe Systems Advertising para relatórios e otimização, os dados estão sujeitos às regras atribuição, incluindo as janelas de retrospectiva de impressão e cliques, configuradas para os anunciante na Adobe Systems Advertising.

![Configurações da janela de lookback em nível anunciante no Adobe Systems Publicidade](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Systems Advertising atribuição janela de lookback de cliques: o número de dias após o primeiro clique ocorre em que o clique pode ser atribuído a um conversão. Por padrão, esse valor é de 60 dias; o máximo é de 90 dias
* Adobe Systems advertising atribuição impressão janela de lookback: o número de dias após uma impressão publicitária em que os impressão podem ser atribuídos a um conversão. Por padrão, esse valor é de 14 dias; o máximo é de 30 dias

  >[!NOTE]
  >
  > A impressão janela de lookback é específica para o Adobe Systems Advertising, não [!DNL Analytics for Advertising]o relatórios.

O [!DNL Analytics for Advertising] JavaScript usa essas configurações para determinar o quanto tempo atrás considerar uma entrada de visualização ou entrada de click-through no site como válida. Para obter mais informações sobre como os visualização-throughs e click-throughs são determinados, consulte &quot;[Adobe Systems IDs de publicidade usadas pelo Analytics](ids.md)&quot;.

## Adobe Systems dados de publicidade no [!DNL Analytics]

[!DNL Analytics] define Adobe Systems IDs de publicidade (AMO IDs) no Analytics hit, sujeito à configuração de persistência do [!DNL eVar] anunciante, que se aplica a click-throughs e visualização-throughs. A configuração de persistência é configurada no back-end Adobe Systems Advertising e sua equipe de conta Adobe Systems pode alterá-la.

* [!DNL Analytics for Advertising][!DNL eVar] expiração: 60 dias por padrão para IDs AMO

>[!NOTE]
>
>Para segmento dados para diferentes período, você pode [configurar segmentos personalizados com diferentes janelas](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) de retrospectiva dentro Analysis Workspace.

## Ambientes de publicidade suportados

* Procurar
* Exposição
* Vídeo
* Vídeo online
* TV conectados
* Nativo

Entre em contato com a equipe de conta Adobe Systems para obter os ambientes de publicidade mais recentes suportados em cada canal.

## O que você deve saber antes da implementação

* O Adobe Systems Advertising implementação equipe configura a integração.

* Nenhum custo adicional é cobrado por essa integração, nem as chamadas do servidor resultam em taxas adicionais [!DNL Analytics] ou Adobe Systems de publicidade.

* [!DNL Analytics for Advertising] é servidor de publicidade independente: um visualização-through ou click-through pode ocorrer a partir de qualquer servidor de publicidade e as IDs adequadas são geradas na entrada do site.

* A integração passa apenas [!DNL Analytics] eventos padrão e personalizados para Adobe Systems Advertising para oferta otimização de esforços subsequentes de mídia paga e publicidade. Ele não transmite [!DNL Analytics] segmentos, métricas calculadas e [!DNL eVars] para Adobe Systems o Advertising para oferta otimização.

* Adobe Systems a publicidade cria IDs persistentes com base no último anúncio clicado ou visualizado antes da usuário entrar no site, com base no [clique e nas janelas [!DNL Analytics]](#lookback-a4adc) de lookback de visualização-through configuradas na Adobe Systems Advertising. Se um visitante do site tiver ambos os tipos de interações de entrada do site dentro do perfil e o clique estiver dentro do período de lookback, a ID de click-through do visitante substituirá a ID de visualização-through do relatórios do site.

* [!DNL Analytics for Advertising] conversão rastreamento no Adobe Analytics usa uma janela de lookback rastreamento configurável (60 dias por padrão). Adobe Systems relatórios de publicidade refletem as conversões e os envolvimento do site até o final desta rastreamento janela de retrospectiva.

* Todos os publicidade tipos são suportados. No entanto, nem todos os ambientes publicidade são suportados.

* [!DNL Analytics] no momento, as conversões são rastreadas e atribuídas apenas a um visitante no mesmo dispositivo.

* [!DNL Analytics for Advertising] não suporta conversões de visualização-through no aplicativo.

* Exibir rastreamento não é suportada por anunciantes que usam uma lado do servidor encaminhamento implementação de [!DNL Analytics].

### ID suplementar

Depois que o Experience Cloud Serviço de identidade for implementado para um site, ocorrências que contêm dados [!DNL Analytics] ou Adobe Systems Publicidade contêm uma ID adicional.

Exemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para uma integração precisa de dados, todas as chamadas Adobe Systems Advertising usadas por um [!DNL Analytics for Advertising] atividade para fornecer conteúdo ou registrar a meta métrica devem ter uma hit correspondente [!DNL Analytics] que compartilhe a mesma ID suplementar.

Ao solucionar [!DNL Analytics]problemas, confirme se a ID adicional está presente para [!DNL Analytics] as ocorrências. [No Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), você pode ver essa ID no Adobe Systems Advertising guia como o `sdid` parâmetro.

>[!NOTE]
>
> Esse implementação funciona de forma semelhante à [!DNL Analytics for Target] integração.

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
