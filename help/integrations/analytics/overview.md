---
title: Visão geral do [!DNL Analytics for Advertising]
description: Visão geral do [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Visão geral do [!DNL Analytics for Advertising]

*Anunciantes com DSP e[!DNL Advertising Search]*

[!DNL Analytics for Advertising] A integra o Adobe Analytics e o Adobe Advertising para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem interações do site de click-through e view-through em seus [!DNL Analytics] permitindo que as marcas vejam como seus gastos com publicidade levam ao engajamento do site e aos objetivos comerciais críticos.

Além disso, a Adobe Advertising pode acessar os vastos dados primários que [!DNL Analytics] coleta usando [!DNL Analytics] já no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. A Adobe Advertising pode usar ainda mais o [!DNL Analytics] dados para otimização de gastos e ofertas.

Quando adequadamente empregado, [!DNL Analytics for Advertising] ofusca as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e compreensão desse envolvimento por meio da análise da web.

Principais benefícios:

* Enviar [!DNL Analytics] segmentos diretamente para a Adobe Advertising para remarketing de site próprio.
* Uso [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Aproveite [!DNL Analytics] Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita.
* Permita uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Usar IDs de view-through e click-through de publicidade Adobe persistente no [!DNL Analytics] para entender o engajamento no site.
* Aprimore os relatórios tradicionais de mídia paga no Analysis Workspace com métricas, dimensões e atividades do site personalizadas que não são viáveis ao exportar dados ou pixels para servidores de publicidade ou outro DSP.
* Aproveite [!DNL Analytics] já em seu site para rastreamento e otimização na Adobe Advertising.

>[!TIP]
>
> Assista a um [vídeo de introdução ao [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Utilização do Analytics para relatórios de mídia paga

[!DNL Analytics for Advertising] melhora os relatórios e insights sobre como sua publicidade direciona o comportamento do site, permitindo:

* Usar IDs de view-through e click-through de publicidade Adobe persistente no [!DNL Analytics] para entender o engajamento no site.
* Aproveite o Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita. É possível acessar dados dimensionais e de eventos de mídia paga, que incluem nomes de entidades de campanha do Adobe (até inserções e anúncios) e suas métricas associadas, como cliques, impressões e custo.

Para usar [!DNL Analytics] como sua ferramenta de relatório de mídia paga, sua organização precisa de um logon de Experience Cloud com acesso ao Analysis Workspace. Sua equipe de publicidade de Adobe ajudará você a mapear seus dados de publicidade de Adobe para conjuntos de relatórios individuais no Analysis Workspace. Você pode enviar dados de publicidade de Adobe para qualquer conjunto de relatórios, mas esteja ciente dos conjuntos de relatórios que foram mapeados para a publicidade de Adobe e daqueles que não os receberam. Dependendo do conjunto de relatórios, isso pode alterar os dados relatados.

[IDs de publicidade do Adobe no [!DNL Analytics]](ids.md) O funciona como outras eVars, com uma expiração persistente e personalizada. Por padrão, a janela de retrospectiva de atribuição é definida como 60 dias durante a implementação do Adobe Advertising. Para alterar essa configuração, entre em contato com a equipe de conta do Adobe.

As dimensões de publicidade do Adobe são anexadas com o sufixo &quot;(ID AMO)&quot; (como &quot;Tipo de anúncio (ID AMO)&quot;). Consulte &quot;[Métricas de publicidade Adobe no Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obter uma lista das dimensões disponíveis.

>[!NOTE]
>
> Ao visualizar os dados de publicidade do Adobe (ou qualquer conjunto de dados) no [!DNL Analytics], esteja ciente de que as métricas e os relatórios são baseados nas regras definidas no [!DNL Analytics]. Os dados podem ser diferentes do que você vê em outros sistemas de relatórios, como relatórios de servidor de anúncios, [!DNL DSP] relatórios ou relatórios de mecanismo de pesquisa. Para compreender as diferenças de dados em [!DNL Analytics]Além disso, você precisa saber quando os dados de eVar expiram, o que define uma visita, o que é considerado atribuição de último contato versus atribuição persistente total e outros fatores. Para obter mais informações, consulte [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](data-variances.md).

## Uso do Analytics para potencializar campanhas e Portfolio de publicidade de Adobe

Sem exigir pixels adicionais, [!DNL Analytics for Advertising] O habilita uma melhor otimização e uma segmentação mais fácil do público enviando dois sinais principais para a Adobe Advertising:

* Métricas de conversão a serem usadas como sinais de oferta:
   * métricas padrão, como [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * métricas de envolvimento com o site, como exibições de página e métricas de visita.
   * métricas de receita personalizadas.
   * métricas de receita reservadas.
* Segmentos criados no [!DNL Analytics] e publicado no Experience Cloud.

   Você pode usar [!DNL Analytics] segmentos para redirecionamento de site próprio no [!DNL DSP] e publicidade de pesquisa paga.

   ([!DNL Search] somente) Anunciantes com [!DNL Analytics] mas não o Audience Manager também pode criar públicos-alvo com base em tags do site da Google (listas de remarketing) e públicos-alvo de correspondência do cliente (listas de clientes) do [!DNL Analytics] segmentos que são compartilhados com o Experience Cloud.

### Métricas de conversão de site como sinais de oferta

Você pode usar os eventos padrão e personalizados em [!DNL Analytics] para construir objetivos ponderados na Adobe Advertising. Os objetivos informam as decisões de licitação do seu [!DNL DSP] pacotes e portfólios de pesquisa.

>[!NOTE]
>
> Não é possível mapear métricas calculadas de [!DNL Analytics] na Adobe Advertising.

Sua equipe de publicidade Adobe o ajudará a identificar e mapear os eventos aplicáveis ao desempenho de mídia paga na Adobe Advertising, onde eles aparecerão em [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas do Analytics na publicidade do Adobe](analytics-data-in-advertising.md)&quot; para obter uma lista das métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

A publicidade Adobe pode assimilar [!DNL Analytics] para fins de remarketing para DSP publicitário e [!DNL Search] anúncios usando a integração nativa de públicos-alvo do Experience Cloud entre [!DNL Analytics] e Experience Cloud.

Para acessar o [!DNL Analytics] segmentos, uma conta de anunciante precisa ter a [Serviço de ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) ativado. Quando o serviço de ID está ativado, todos os segmentos de Experience Cloud (incluindo os segmentos criados no [!DNL Analytics] e publicado no Experience Cloud, segmentos criados no Adobe Audience Manager, segmentos criados no Experience Cloud usando o [!DNL People core service], e os segmentos criados no Adobe Experience Platform e enviados ao Adobe Advertising via Audience Manager) ficam disponíveis no Adobe Advertising assim que são processados.

[!DNL Analytics] Os segmentos do estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço Experience Cloud Audiences, consulte [Públicos do Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemplos de como usar a integração

### Uso de dados de publicidade do Adobe no Analysis Workspace

Para saber como você pode usar os dados de publicidade do Adobe para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Criação de painéis de publicidade do Adobe

Para saber como rastrear seus dados de publicidade Adobe em relação às suas metas no Analysis Workspace, assista ao vídeo &quot;[Criar painéis de publicidade do Adobe com o Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Uso da ID de publicidade do Adobe para análise de entrada de site

Para saber como criar um relatório de entrada de site de publicidade do Adobe para monitorar as influências diárias, diárias, de horas do dia, do navegador e geográficas, assista ao vídeo &quot;[Criar relatórios de entrada de site de publicidade do Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução ao [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Pré-requisitos e informações-chave para implementação do [!DNL Analytics for Advertising]](prerequisites.md)
>* [IDs de publicidade do Adobe usadas pelo Analytics](ids.md)
>* [Código JavaScript para o Analytics para publicidade](/help/integrations/analytics/javascript.md)
>* [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](data-variances.md)
>* [Métricas de publicidade Adobe no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados em publicidade de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

