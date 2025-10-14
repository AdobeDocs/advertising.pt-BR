---
title: (Nova interface do usuário) Sobre objetivos
description: Saiba mais sobre os objetivos para atingir suas metas comerciais.
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nova interface do usuário) Sobre objetivos

*recurso do Beta*

Objetivos são metas que um anunciante define para atender aos seus objetivos de negócios, como maximizar os lucros ou atingir uma meta de vendas específica. O Advertising Search, Social e Commerce e o Advertising DSP usam os objetivos:

* Cada portfólio de Pesquisa, Social e Commerce deve ter um objetivo para que o recurso de otimização possa criar modelos de clique e receita para o portfólio.

* No DSP, os objetivos são exibidos como metas personalizadas para contas do DSP vinculadas às contas do Search, Social e Commerce. Cada pacote que usa as metas de otimização &quot;Maior retorno do investimento em publicidade (ROAS)&quot; ou &quot;Menor custo por aquisição (CPA)&quot; deve incluir uma meta personalizada que ajude a alcançar a meta de otimização geral.

Um objetivo consiste nas métricas de conversão a serem rastreadas e otimizadas e nos pesos relativos dessas métricas. Por exemplo, suponha que uma revista online com dois níveis de assinatura online e um nível de assinatura para impressão e o objetivo &quot;maximizar lucros&quot; tenha três métricas: &quot;assinaturas online básicas&quot; com valor de 20 USD, &quot;assinaturas online premium&quot; com valor de 40 USD e &quot;assinaturas para impressão&quot; com valor de 30 USD. Se a revista quiser dar peso de acordo com o valor monetário único da subscrição, os pesos relativos das métricas serão 1, 2 e 1,5, respectivamente.

Para cada métrica no objetivo, você pode:

* Configure pesos separados para conversões de dispositivos móveis.

* Rotular a métrica como uma métrica [!UICONTROL Goal] ou uma métrica [!UICONTROL Assist].

* Aplique recomendações de peso às métricas.

>[!NOTE]
>* (Pesquisa, Social e Commerce) Você pode associar um objetivo a um portfólio ao [criar o portfólio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) ou ao [modificar as configurações do portfólio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md) posteriormente.
>* (Anunciantes com contas do DSP vinculadas a contas do Search, Social e Commerce) No Advertising DSP, você pode selecionar um objetivo como uma [meta de otimização personalizada](/help/dsp/campaign-management/packages/package-settings.md) para um pacote com ritmo no nível do pacote.
>* Você pode usar o mesmo objetivo para vários portfólios de Pesquisa, Social e Commerce e/ou vários pacotes do DSP.
>* As métricas para cada objetivo na exibição [!UICONTROL Objectives] não incluem dados do DSP.

## Métricas disponíveis

Você pode incluir qualquer um dos seguintes itens em seus objetivos:

* Métricas que o Adobe Advertising rastreia usando o [pixel de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Métricas rastreadas pelo anunciante a partir de arquivos de feed de conversão](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Anunciantes com [!DNL Adobe Analytics for Advertising]) [Métricas de conversão e envolvimento do site sincronizadas do Adobe Analytics](/help/integrations/analytics/overview.md).

  Em Pesquisa, Social e Commerce, as [métricas de envolvimento do site](/help/integrations/analytics/analytics-data-in-advertising.md) a seguir são automaticamente consideradas nos algoritmos de oferta do portfólio: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` e `bounces`.

* [!DNL Google] métricas:<!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads] conversões &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) rastreadas de contas [!DNL Google Ads] sincronizadas.

   * (Anunciantes com [[!DNL Google Analytics] integrações](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Exibições de página, Sessões, Taxa de rejeição (calculada como rejeições/sessões) e Duração da sessão.

     Em Pesquisa, Social e Commerce, essas métricas são automaticamente fatoradas nos algoritmos de lances do portfólio.

## Opção para fazer upload de objetivos para as redes de publicidade

É possível [carregar os objetivos dos portfólios da conta [!DNL Google Ads] e/ou [!DNL Microsoft Advertising] como conversões](/help/search-social-commerce/tools/objective-upload-to-networks.md), opcionalmente, para usá-los na otimização de nível de campanha ou grupo de anúncios. Quando você habilita a opção, o Search, Social e Commerce transmite os dados de receita ponderada no nível de EF ID (clique em ID) para a rede de publicidade diariamente. Ele omite qualquer métrica de anúncios rastreada pela rede.

>[!MORELIKETHIS]
>
>* [Criar um objetivo](objective-create.md)
>* [Editar um objetivo](objective-edit.md)
>* [Excluir um objetivo](objective-delete.md)
>* [Aplicar recomendações de peso a um objetivo](objective-apply-weight-recommendations.md)
>* [Configurações de objetivo](objective-settings.md)
