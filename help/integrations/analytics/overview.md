---
title: Visão geral de  [!DNL Analytics for Advertising]
description: Visão geral de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 8911f6ea16878bede96151f004e6de2717484140
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Visão geral do [!DNL Analytics for Advertising]

*Anunciantes com o Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

O [!DNL Analytics for Advertising] integra o Adobe Analytics e o Adobe Advertising para estender e aprimorar os recursos de cada produto.

A integração permite que os anunciantes rastreiem interações do site de click-through e view-through em suas instâncias do [!DNL Analytics], permitindo que as marcas vejam como seus gastos com publicidade levam ao engajamento do site e aos objetivos comerciais críticos.

Além disso, o Adobe Advertising pode acessar os vastos dados primários que o [!DNL Analytics] coleta usando as tags [!DNL Analytics] já existentes no site. Isso permite um gerenciamento de jornadas mais robusto, remarketing próprio e relatórios de site de mídia paga. O Adobe Advertising pode usar ainda mais os dados [!DNL Analytics] para otimização de gastos e ofertas.

Quando adequadamente empregado, o [!DNL Analytics for Advertising] ofusca as linhas entre duas funções tradicionais: gerenciamento de jornadas de publicidade (o ato de enviar usuários para o site por meio de anúncios) e compreensão desse engajamento do site por meio da análise da Web.

Principais benefícios:

* Envie [!DNL Analytics] segmentos diretamente para o Adobe Advertising para remarketing de site próprio.
* Use [!DNL Analytics] eventos personalizados e padrão como sinais de conversão para otimizar a publicidade de mídia paga.
* Aproveite o Analysis Workspace [!DNL Analytics] para entender melhor os pontos de entrada do site e o comportamento da visita.
* Permita uma colaboração mais estreita entre analistas da Web e equipes de mídia paga.
* Adobe Advertising Use IDs de view-through e click-through persistentes no [!DNL Analytics] para entender o engajamento do site.
* Aprimore os relatórios tradicionais de mídia paga no Analysis Workspace com métricas, dimensões e atividades do site personalizadas que não são viáveis ao exportar dados ou pixels para servidores de publicidade ou outro DSP.
* Aproveite o código [!DNL Analytics] já existente no seu site para rastreamento e otimização no Adobe Advertising.

>[!TIP]
>
> Assista a uma [introdução de vídeo [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=pt-BR#analytics).

## Utilização do Analytics para relatórios de mídia paga

[!DNL Analytics for Advertising] melhora os relatórios e insights sobre como sua publicidade direciona o comportamento do site, permitindo:

* Adobe Advertising Use IDs de view-through e click-through persistentes no [!DNL Analytics] para entender o engajamento do site.
* Aproveite o Analysis Workspace para entender melhor os pontos de entrada do site e o comportamento da visita. É possível acessar dados dimensionais e de eventos de mídia paga, que incluem nomes de entidades de campanha de Adobe Advertising (até inserções e anúncios) e suas métricas associadas, como cliques, impressões e custo.

Para usar o [!DNL Analytics] como sua ferramenta de relatório de mídia paga, sua organização precisa de um logon de Experience Cloud com acesso ao Analysis Workspace. Sua equipe de Adobe Advertising ajudará você a mapear os dados de Adobe Advertising para conjuntos de relatórios individuais no Analysis Workspace. Você pode enviar dados de Adobe Advertising para qualquer conjunto de relatórios, mas esteja ciente dos conjuntos de relatórios que foram mapeados para o Adobe Advertising e daqueles que não foram. Dependendo do conjunto de relatórios, isso pode alterar os dados relatados.

[IDs de Adobe Advertising em  [!DNL Analytics]](ids.md) funcionam como outros [!DNL eVars], com uma expiração persistente e personalizada. Por padrão, a janela de retrospectiva de atribuição é definida como 60 dias durante a implementação do Adobe Advertising. Para alterar essa configuração, entre em contato com a equipe de conta do Adobe.

As dimensões Adobe Advertising são anexadas com o sufixo &quot;(ID AMO)&quot; (como &quot;Tipo de anúncio (ID AMO)&quot;). Consulte &quot;[Métricas de Adobe Advertising no Analysis Workspace](advertising-metrics-in-analytics.md)&quot; para obter uma lista das dimensões disponíveis.

>[!NOTE]
>
> Ao exibir dados de Adobe Advertising (ou qualquer conjunto de dados) em [!DNL Analytics], esteja ciente de que as métricas e os relatórios são baseados nas regras definidas em [!DNL Analytics]. Os dados podem ser diferentes do que você vê em outros sistemas de relatórios, como relatórios de servidor de publicidade, relatórios do [!DNL DSP] ou relatórios de mecanismo de pesquisa. Para entender as diferenças de dados em [!DNL Analytics], você precisa saber quando os dados de [!DNL eVar] expiram, o que define uma visita, o que é considerado atribuição de último contato versus atribuição persistente total e outros fatores. Para obter mais informações, consulte [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](data-variances.md).

## Uso do Analytics para potencializar campanhas e Portfolio do Adobe Advertising

Sem a necessidade de pixels adicionais, o [!DNL Analytics for Advertising] permite uma melhor otimização e uma segmentação mais fácil do público-alvo enviando dois sinais principais para o Adobe Advertising:

* Métricas de conversão a serem usadas como sinais de oferta:
   * métricas padrão, como [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * métricas de envolvimento com o site, como exibições de página e métricas de visita.
   * métricas de receita personalizadas.
   * métricas de receita reservadas.
* Segmentos criados em [!DNL Analytics] e publicados no Experience Cloud.

  Você pode usar [!DNL Analytics] segmentos para redirecionamento de site próprio em [!DNL DSP] e anúncios de pesquisa pagos.

  ([!DNL Search, Social, & Commerce] somente) Anunciantes com [!DNL Analytics], mas não com Audience Manager, também podem criar públicos com base em tags do site da Google (listas de remarketing) e públicos com correspondência de clientes (listas de clientes) de [!DNL Analytics] segmentos que são compartilhados com Experience Cloud.

### Métricas de conversão de site como sinais de oferta

Você pode usar seus eventos padrão e personalizados do [!DNL Analytics] para criar objetivos ponderados no Adobe Advertising. Os objetivos informam as decisões de licitação para seus pacotes do [!DNL DSP] e portfólios de Pesquisa, Social e Commerce.

Para campanhas de [!DNL Google Ads] e [!DNL Google Microsoft Advertising] em portfólios híbridos de Pesquisa, Social e Commerce, você pode, opcionalmente, fazer upload dos objetivos — incluindo quaisquer eventos [!DNL Analytics] nos objetivos — diretamente para as redes de anúncios, onde eles ficam disponíveis como ações de conversão para metas de conversão personalizadas a nível de conta e de campanha.

>[!NOTE]
>
> Você não pode mapear métricas calculadas de [!DNL Analytics] para Adobe Advertising.

Sua equipe de Adobe Advertising ajudará você a identificar e mapear os eventos aplicáveis ao desempenho de mídia paga no Adobe Advertising, onde eles estão listados em [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Consulte &quot;[Métricas do Analytics no Adobe Advertising](analytics-data-in-advertising.md)&quot; para obter uma lista das métricas disponíveis.

### Segmentos do Analytics para redirecionamento de site

O Adobe Advertising pode assimilar [!DNL Analytics] segmentos para fins de remarketing para Advertising DSP e [!DNL Search, Social, & Commerce] anúncios usando a integração nativa de Públicos-alvo Experience Cloud entre [!DNL Analytics] e Experience Cloud.

Para acessar os segmentos [!DNL Analytics], uma conta de anunciante deve habilitar o [Serviço de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=pt-BR). Quando o Serviço de ID está habilitado, todos os segmentos de Experience Cloud (incluindo segmentos criados em [!DNL Analytics] e publicados em Experience Cloud, segmentos criados em Adobe Audience Manager, segmentos criados em Experience Cloud usando o [!DNL People core service] e segmentos criados em Adobe Experience Platform e enviados para o Adobe Advertising via Audience Manager) ficam disponíveis no Adobe Advertising assim que são processados.

[!DNL Analytics] segmentos estão disponíveis em 24 horas e são atualizados diariamente.

Para obter mais informações sobre o serviço Experience Cloud Audiences, consulte [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=pt-BR).

## Exemplos de como usar a integração {#integration-examples}

### Utilização de dados de Adobe Advertising no Analysis Workspace

Para saber como você pode usar seus dados de Adobe Advertising para criar relatórios visuais no Analysis Workspace, assista ao vídeo &quot;[Introdução ao Workspace e Relatórios](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html?lang=pt-BR).&quot;

#### Uso de Conversões de View-Through de TV Conectada em Relatórios

*Somente usuários do Advertising DSP*

Você pode medir a eficácia total do funil de suas campanhas de TV conectada (CTV) vinculando a exposição de anúncios em dispositivos de CTV a conversões no site. O novo filtro [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; divide as conversões em linhas separadas para valores [!UICONTROL Click Through], [!UICONTROL View Through] e [!UICONTROL View Through (CTV)].

Para visualizar suas métricas de conversão de view-through de CTV, use a exibição Disposição ou a exibição Canal de marketing no Analysis Workspace.

Uso da exibição de Posicionamento:

1. Incluir posicionamentos de gastos com CTV na exibição de relatório.

1. Inclua as métricas desejadas, como &quot;Impressões&quot;, &quot;Cliques&quot; e assim por diante.

1. Aplique os seguintes filtros:

   Plataforma de publicidade: `Advertising Cloud DSP`

   Página de aterrissagem: `View-Through (CTV)`

Uso da exibição Canal de marketing:

1. Incluir a dimensão `Marketing Channel`.

1. Inclua as métricas desejadas, como &quot;Impressões&quot;, &quot;Cliques&quot; e assim por diante.

1. Aplique os seguintes filtros:

   Plataforma de publicidade: `Advertising Cloud DSP`

   Página de aterrissagem: `View-Through (CTV)`

### Criação de painéis do Adobe Advertising

Para saber como rastrear seus dados de Adobe Advertising em relação às suas metas no Analysis Workspace, assista ao vídeo &quot;[Criar painéis de Adobe Advertising com o Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html?lang=pt-BR)&quot;.

### Uso da ID de Adobe Advertising para a Análise de entrada de site

Para saber como criar um relatório de entrada de site Adobe Advertising para monitorar as influências de dia da semana, hora do dia, navegador e geográficas, assista ao vídeo &quot;[Criar relatórios de entrada de site Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html?lang=pt-BR).&quot;

## Como iniciar uma implementação do [!DNL Analytics for Advertising]

Entre em contato com a equipe de conta do Adobe, que concluirá a configuração inicial necessária para começar e ajudará você a planejar a implementação e o uso de dados com base nas necessidades da organização.

>[!MORELIKETHIS]
>
>* [Vídeo: Introdução a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=pt-BR)
>* [Pré-requisitos e informações-chave para implementação [!DNL Analytics for Advertising]](prerequisites.md)
>* [IDs de Adobe Advertising usadas pelo Analytics](ids.md)
>* [Código JavaScript do Analytics para Advertising](/help/integrations/analytics/javascript.md)
>* [Variações de Dados Esperadas Entre [!DNL Analytics] e Adobe Advertising](data-variances.md)
>* [Métricas de Adobe Advertising no Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
