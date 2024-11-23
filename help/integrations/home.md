---
title: Novidades
description: Saiba mais sobre atualizações nas integrações entre o Adobe Advertising e outros produtos e serviços na Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: 1e5c1fb6b164e95612b3815f44d2d4f8b3613d7a
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Novidades

Os seguintes recursos são novos ou foram alterados recentemente.

| Data | Recurso | Descrição | Para obter mais informações |
| ---- | ------- | ----------- | -------------------- |
| Lançado em 29 de outubro de 2024 | [!DNL Adobe Analytics for Advertising] | (Anunciantes com [!DNL Adobe Analytics for Advertising] e [!DNL Microsoft Advertising] campanhas de desempenho máximo) Os dados de nível de grupo de ativos para suas campanhas de desempenho máximo agora estão disponíveis no Adobe Analytics quando você implementa um novo parâmetro de ID do AMO ([!DNL s_kwcid]) nas URLs de rastreamento para suas campanhas de desempenho máximo, que não incluem anúncios e palavras-chave. O rastreamento da maioria das campanhas de desempenho máximo já foi migrado para o novo formato. Para campanhas de desempenho máximo sem a opção de rastreamento [!UICONTROL Auto Upload] que ainda não foram migradas para o novo formato, no entanto, você deve atualizar manualmente cada sufixo da página de aterrissagem para incluir o seguinte formato de ID AMO:<br><br>`AL!%(userid)d!%(sid)d!%(creativeref)s!!!%(termid/orderid)d!!!%(campaignid)!%(adref)`<br><br>Os dados do Adobe Analytics para suas campanhas de desempenho máximo também estão disponíveis em Pesquisa, Social e Commerce. | Veja o novo [formato de ID do AMO](/help/integrations/analytics/ids.md##amo-id-formats) e [quando e como adicionar o parâmetro às URLs de rastreamento](/help/integrations/analytics/ids.md#amo-id-implement). |
| 13 de novembro de 2024 | [!DNL Analytics for Advertising] | (Anunciantes com [!DNL Analytics for Advertising] e Adobe Customer Journey Analytics) Se você usar variáveis reservadas para capturar suas IDs AMO e IDs EF, você pode se preparar para uma integração futura entre o Adobe Advertising e o Adobe Customer Journey Analytics copiando suas variáveis reservadas para a ID AMO e a ID EF no padrão [!DNL eVars] assim que possível. Isso permitirá a coleta de dados históricos para as IDs AMO e EF assim que você concluir a tarefa, e os dados históricos estarão disponíveis para uso futuro. A equipe de conta do Adobe avisará se você usa variáveis reservadas e se precisa concluir essa tarefa. | Consulte &quot;[Coletar Dados Históricos para IDs AMO e IDs EF para Uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).&quot; |
| 16 de dezembro de 2023 | Ajuda | Um novo documento explica como configurar testes A/B no [!DNL Target] para tráfego de click-through de anúncios no Search, Social e Commerce, além de dicas sobre como medir e visualizar seus testes no [!DNL Analytics]. | Consulte &quot;[Configurar testes A/B no Adobe Target para Search, Social e Commerce Ads](/help/integrations/target/ab-tests-search.md).&quot; |
| 8 de agosto de 2023 | [!DNL Analytics for Advertising] | Algumas métricas de evento de sucesso do [!DNL Analytics], incluindo métricas de conversão e métricas de tráfego padrão, personalizadas e reservadas, estão automaticamente disponíveis no DSP e em Pesquisa, Social e Commerce. Agora, você também pode configurar suas próprias métricas de sucesso com base nas [!DNL Analytics] [!DNL eVars] e [!DNL props] existentes, canalizando dados de nível [!DNL eVar] e [!DNL prop] para um evento bem-sucedido personalizado. | Consulte &quot;[Criar Métricas de Conversão do Adobe Analytics [!DNL eVars] and [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;. |
| 13 de julho de 2023 | Relatórios | (Usuários de DSP com [!DNL Analytics for Advertising]) Conversões de viewthrough para inserções de TV conectada (CTV) agora são incluídas nos dados de conversão disponíveis no Adobe Analytics. | Consulte a seção &quot;Exemplos de Como Usar a Integração&quot; em &quot;[Visão Geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| 1 de novembro de 2022 | Ajuda | Um novo documento explica como implementar o compartilhamento de sinal click-through e view-through entre o Advertising DSP e o Adobe Target, configurar uma atividade de teste A/B no [!DNL Target] para seus anúncios DSP e como configurar o Adobe Analytics Analysis Workspace para exibir os dados de teste. | Consulte &quot;[Configurar testes A/B no Adobe Target para Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md).&quot; |
| 17 de agosto de 2022 | Ajuda | Um novo capítulo explica todas as maneiras em que o Adobe Advertising é integrado ao Adobe Audience Manager. | Consulte o capítulo sobre &quot;Integração com o Adobe Audience Manager&quot;, incluindo uma visão geral das &quot;[Integrações de Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| 27 de abril de 2021 | [!DNL Analytics for Advertising] | Saiba por que e como adicionar macros do [!DNL Analytics for Advertising] às suas marcas de anúncio do [!DNL Google Campaign Manager 360] para enviar dados de clique para a Adobe Analytics. | Consulte &quot;[Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Marcas de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot; |
| 19 de abril de 2021 | [!DNL Analytics for Advertising] | Saiba por que e como anexar macros às suas marcas de anúncio do [!DNL Flashtalking] para enviar dados de cliques para a Adobe Analytics. | Consulte &quot;[Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio](/help/integrations/analytics/macros-flashtalking.md).&quot; |
| 27 de outubro de 2021 | [!DNL Analytics for Advertising] | Se a sua empresa deseja mudar da biblioteca herdada do Adobe Analytics `visitorAPI.js` para a biblioteca do [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`) para coleta de dados, será necessário fazer algumas alterações para habilitar a unificação de ID. | Consulte &quot;[Usando a [!DNL Last Event Service] Biblioteca da JavaScript com o Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md).&quot; |
| 26 de maio de 2021 | Ajuda | O capítulo &quot;[!DNL Analytics for Advertising]&quot; agora inclui um subcapítulo sobre &quot;Trabalhando em [!DNL Analytics Marketing Channels].&quot; | Consulte: &quot;[Princípios básicos dos canais de marketing](/help/integrations/analytics/marketing-channels/mc-overview.md),&quot; &quot;[Uso de IDs de Adobe Advertising para criar [!DNL Analytics Marketing Channels] Regras de processamento](/help/integrations/analytics/marketing-channels/mc-ids.md),&quot; &quot;[Uso [!DNL Analytics Marketing Channels] com Dados de Adobe Advertising](/help/integrations/analytics/marketing-channels/mc-ac-data.md),&quot; e &quot;[Por que os Dados de canal podem variar entre Adobe Advertising e [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md).&quot; |
| 26 de maio de 2021 | Ajuda | Um link para todos os tutoriais em vídeo sobre [!DNL Analytics for Advertising] foi adicionado. | Consulte: &quot;[Tutoriais em vídeo sobre integrações do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html).&quot; |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
