---
title: Pré-requisitos e Informações-Chave para Implementação [!DNL Analytics for Advertising]
description: Pré-requisitos e Informações-Chave para Implementação [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Pré-requisitos e Informações-Chave para Implementação de [!DNL Analytics for Advertising]

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Analise as informações a seguir antes de integrar o Adobe Advertising ao Adobe Analytics.

## Requisitos para Dados de Adobe Advertising de Relatório em [!DNL Analytics]

* Qualquer uma das seguintes opções:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` versão 2.0 ou superior
* Qualquer versão do Adobe Analytics (incluindo [!DNL Prime], [!DNL Premium] ou [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versão 2.1 ou superior
* (Clientes do Advertising DSP) Um [trecho do Advertising DSP JavaScript](javascript.md) implantado em suas páginas da Web para rastrear visitas de view-through.

>[!TIP]
>
>Para melhorar a fidelidade dos dados, use a versão mais recente de cada biblioteca.

## Requisitos para o compartilhamento de segmentos do Analytics com o Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` versão 2.1 ou superior
* Adobe Analytics: `appMeasurement.js` versão 1.8 ou superior

## Requisitos para relatório de dados [!DNL Analytics] no Adobe Advertising

Forneça o seguinte à equipe de implementação do Adobe Advertising:

* A ID do conjunto de relatórios [!DNL Analytics] a ser usada para relatórios sobre atividades de mídia paga e para alimentar atividades do site com otimização e relatórios no Adobe Advertising
* A ID da organização Experience Cloud da empresa (ID da organização).

Você pode encontrar essas duas IDs na [guia Resumo do Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=pt-BR).

![tela Resumo do Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dados no Adobe Advertising {#lookback-a4adc}

Como os dados do [!DNL Analytics] são enviados ao Adobe Advertising para relatórios e otimização, os dados estão sujeitos às regras de atribuição, incluindo as janelas de retrospectiva de impressões e cliques, que são configuradas para o anunciante no Adobe Advertising.

![configurações da janela de pesquisa no nível do anunciante no Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Janela de retrospectiva de clique para atribuição de Adobe Advertising: o número de dias após o primeiro clique em que o clique pode ser atribuído a uma conversão. Por padrão, esse valor é 60 dias; o máximo é 90 dias
* Janela de retrospectiva de impressão de atribuição de Adobe Advertising: o número de dias após a ocorrência de uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. Por padrão, esse valor é 14 dias; o máximo é 30 dias

  >[!NOTE]
  >
  > A janela de retrospectiva de impressão é específica do Adobe Advertising, não do [!DNL Analytics for Advertising], para relatórios.

O JavaScript [!DNL Analytics for Advertising] usa essas configurações para determinar até que ponto considerar uma entrada de view-through ou de click-through para o site como válida. Para obter mais informações sobre como view-throughs e click-throughs são determinados, consulte &quot;[IDs de Adobe Advertising usadas pelo Analytics](ids.md)&quot;.

## Dados Adobe Advertising em [!DNL Analytics]

[!DNL Analytics] define IDs de Adobe Advertising (AMO IDs) na ocorrência do Analytics, sujeito à configuração de persistência [!DNL eVar] do anunciante, que se aplica a click-throughs e view-throughs. A configuração de persistência está definida no back-end do Adobe Advertising e sua equipe de conta do Adobe pode alterá-la.

* [!DNL Analytics for Advertising] [!DNL eVar] expiração: 60 dias por padrão para IDs AMO

>[!NOTE]
>
>Para segmentar dados para um período diferente, você pode [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=pt-BR) com diferentes janelas de pesquisa no Analysis Workspace.

## Ambientes de anúncios compatíveis

* Pesquisar
* Exibir
* Vídeo
* Vídeo online
* TV conectada
* Nativo

Entre em contato com a equipe de conta do Adobe para obter os ambientes de anúncios mais recentes compatíveis em cada canal.

## O que você deve saber antes da implementação

* A equipe de implementação do Adobe Advertising configura a integração.

* Não serão cobrados custos adicionais por essa integração, nem as chamadas do servidor resultarão em [!DNL Analytics] ou taxas Adobe Advertising adicionais.

* [!DNL Analytics for Advertising] é independente de servidor de anúncios: um view-through ou click-through pode ocorrer de qualquer servidor de anúncios, e as IDs adequadas são geradas na entrada do site.

* A integração passa somente eventos padrão e personalizados do [!DNL Analytics] para o Adobe Advertising para otimização de oferta de mídia paga e esforços de publicidade subsequentes. Ele não passa [!DNL Analytics] segmentos, métricas calculadas e [!DNL eVars] para Adobe Advertising para otimização de oferta.

* O Adobe Advertising cria IDs persistentes em [!DNL Analytics] com base no último anúncio clicado ou exibido antes que o usuário entre no site, com base nas [janelas de retrospectiva de clique e de view-through](#lookback-a4adc) configuradas no Adobe Advertising. Se um visitante do site tiver ambos os tipos de interações de entrada de site em seu perfil e o clique estiver dentro do período de lookback, a ID de click-through do visitante substituirá a ID de view-through para relatórios do site.

* O rastreamento de conversão do [!DNL Analytics for Advertising] no Adobe Analytics usa uma janela de retrospectiva de rastreamento configurável (60 dias por padrão). Os relatórios de Adobe Advertising refletem conversões e engajamento do site até o final desta janela de retrospectiva de rastreamento.

* Todos os tipos de anúncios são compatíveis. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] conversões são atualmente rastreadas e atribuídas apenas a um visitante no mesmo dispositivo.

* [!DNL Analytics for Advertising] não oferece suporte para conversões view-through no aplicativo.

* O rastreamento de view-through não tem suporte para anunciantes que usam uma implementação de encaminhamento pelo lado do servidor de [!DNL Analytics].

### ID suplementar

Depois que o Serviço de Identidade do Experience Cloud é implementado para um site, as ocorrências que contêm dados de [!DNL Analytics] ou Adobe Advertising contêm uma ID complementar.

Exemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para uma integração de dados precisa, todas as chamadas de Adobe Advertising usadas por uma atividade [!DNL Analytics for Advertising] para fornecer conteúdo ou registrar a métrica de meta devem ter uma ocorrência [!DNL Analytics] correspondente que compartilhe a mesma ID complementar.

Ao solucionar problemas no [!DNL Analytics], confirme se a ID complementar está presente para [!DNL Analytics] ocorrências. No [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=pt-BR), você pode ver essa ID na guia Adobe Advertising como o parâmetro `sdid`.

>[!NOTE]
>
> Esta implementação funciona de forma semelhante à integração do [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript do Analytics para Advertising](/help/integrations/analytics/javascript.md)
