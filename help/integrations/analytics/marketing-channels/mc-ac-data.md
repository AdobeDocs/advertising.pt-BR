---
title: Usar [!DNL Marketing Channels] com dados de publicidade do Adobe
description: Saiba como usar os dados de publicidade do Adobe no [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Usar [!DNL Analytics Marketing Channels] com dados de publicidade do Adobe

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

Ao usar a publicidade de Adobe e [!DNL Analytics Marketing Channels] relatórios, você pode obter insights valiosos sobre como a mídia digital influencia a atividade do site.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

A ilustração a seguir mostra como a Adobe Advertising e a [!DNL Marketing Channels] rastrear as visitas individuais que compõem a jornada de um visitante. Relatórios de publicidade Adobe em [!DNL Analytics] estão limitados apenas a publicidade de canais de exibição, pesquisa, social e comércio pagos e traficados pela Adobe Advertising, usando a AMO ID. No entanto, [!DNL Marketing Channels] rastreia todos os canais configurados no [!DNL Marketing Channels] Regras de processamento.

![Como a Adobe Advertising e [!DNL Marketing Channels] rastrear as visitas individuais na jornada de um visitante](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Na primeira visita, o usuário entrou no site por meio de uma campanha de email, executou dez exibições de página e saiu. Na segunda visita, o usuário entrou no site por meio de um anúncio de exibição, executou dez exibições de página e saiu. Na terceira visita, o usuário entrou no site por meio de pesquisa natural, executou cinco visualizações de página, executou uma conversão de US$ 250 e à esquerda. Observe a diferença no rastreamento entre [!DNL Marketing Channels] e Adobe Advertising. O único canal que a Adobe Advertising rastreia nesta jornada é [!UICONTROL Display]. A Adobe Advertising rastreia o [!UICONTROL Display] visita de canal e atribui os dados de engajamento subsequentes (como exibições de página) e as conversões de volta à influência desse anúncio. [!DNL Marketing Channels], por outro lado, fornece uma visão completa de todos os canais.

Como a ID do AMO persiste durante a jornada do visitante, você pode usar os dados da ID do AMO para ver como a Adobe Advertising influencia outros canais de marketing. A ID do AMO [persiste por 60 dias por padrão](/help/integrations/analytics/overview.md), mas você poderá configurar a persistência conforme necessário.

## Como combinar dados de Canais de marketing e publicidade do Adobe para analisar o desempenho da mídia

Dentro de [!DNL Analytics], você poderá combinar os dados persistentes de publicidade paga da Adobe Advertising e a variável [!DNL Marketing Channels] dados abrangentes de visitas para analisar melhor o desempenho da mídia e influenciar melhor a jornada do cliente.

A análise a seguir usa os dados de Anúncios de Adobe para mostrar diferentes versões de como um anúncio de exibição afeta a conversão do site. Todas as três colunas usam as mesmas métricas de conversão, mas cada coluna conta uma história diferente:

* A Coluna 1 analisa os dados da ID do AMO que são persistentes na jornada do visitante. A coluna 1 indica que 641 inicializações de aplicativos foram, em um ponto, vinculadas a um anúncio de publicidade Adobe, por meio de um evento de view-through ou click-through. Esta visualização não aceita nenhuma outra [!DNL Marketing Channels] atribuição em consideração.

* No [!DNL Marketing Channels] No entanto, os 641 Inícios de aplicações são atribuídos a outros canais de marketing. As duas últimas colunas usam as 641 Inicializações de Aplicativos e limitam os dados ao [!UICONTROL Display Click-Through] e [!UICONTROL Display View-Through] canais, mostrando as conversões que ocorrem em um modelo de atribuição de último contato.

![exemplo de como um anúncio de exibição afeta a conversão do site](/help/integrations/assets/a4adc-mc-display-impact.png)

Você pode levar essa análise um passo além. Você pode detalhar ainda mais a linha Anúncios de Adobe por canal de marketing para ver onde as conversões de Anúncios de Adobe são atribuídas aos 641 Inícios de aplicativos. Você já sabe que cinco dessas conversões são atribuídas a um Click-through de exibição de último toque e 19 são atribuídas a um View-through de exibição de último toque. Ainda restam 617 Inscrições atribuídas a outros canais de marketing. Você pode arrastar e soltar a dimensão Canal de último contato na parte superior do item de linha DSP de anúncio para revelar a atribuição do canal para o restante dos Inícios de aplicativos e mostrar o impacto entre canais do canal de exibição.

![como adicionar a dimensão Canal de último contato](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Agora você pode ver como os Inícios de Aplicações restantes são atribuídos. O email recebe crédito por 357 Aplicativos de último contato iniciados, para os quais uma ID do AMO persistiu. Usando esse tipo de análise, você pode ver o impacto que os anúncios de exibição da Adobe Advertising tiveram em todos os canais. Com apenas um conjunto de dados e um modelo de atribuição, esse tipo de insight não estaria disponível.

![exemplo do impacto entre canais dos canais de exibição](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

É possível melhorar ainda mais a análise usando um Gráfico de pilha definido como &quot;100% empilhado&quot; para mostrar dados de tendência ao longo do tempo. Essa visualização facilita o monitoramento de quais canais de marketing de último contato são mais afetados pelas campanhas de marketing de exibição.

![exemplo do impacto entre canais da tendência dos canais de exibição](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Fundamentos da [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras de processamento](mc-ids.md)
>* [Por que os dados de canal podem variar entre anúncios de Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vídeo: usar [!DNL Marketing Channels] para Relatórios de publicidade do Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

