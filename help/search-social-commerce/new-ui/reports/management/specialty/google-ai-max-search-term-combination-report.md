---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: Saiba mais sobre o [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Aplicável a contas [!DNL Google Ads] com campanhas habilitadas somente para AI max*

O [!UICONTROL Google AI Max Search Term Combination Report] mostra como consultas de pesquisa específicas são mapeadas para títulos gerados por IA e páginas de aterrissagem dinâmicas, bem como para ações de conversão para anúncios em campanhas habilitadas para [!DNL Google Ads AI Max] em contas especificadas. O relatório inclui duas folhas:

* Planilha [!UICONTROL AI Max Search Term]: o desempenho de combinações de anúncios específicas e páginas de aterrissagem com base em pesquisas na rede de pesquisa. A planilha inclui dados de impressão, cliques e custo, bem como quaisquer métricas de conversão [!DNL Google Ads] opcionais controladas especificadas nas configurações do relatório. Por padrão, os dados incluem uma linha para cada combinação de termo de pesquisa, título e página de aterrissagem que recebeu pelo menos uma impressão no intervalo de dados especificado. As linhas são classificadas em ordem crescente por campanha por padrão e, em seguida, por outra coluna de sua escolha.

  Use esta planilha para analisar a intenção e o desempenho dos elementos de anúncio resultantes por consulta, de modo que você possa criar listas de palavras-chave negativas robustas.

* <!-- [!UICONTROL Search Term x Conversion Action] sheet? -->Planilha [!UICONTROL AI Max Search Term #1]: [!DNL Google Ads] dados de conversão rastreados por ação de conversão para cada termo de pesquisa e tipo de correspondência. Cada linha inclui a ação de conversão, o número de conversões e o valor de conversão, bem como quaisquer outras métricas de conversão [!DNL Google Ads] opcionais rastreadas especificadas nas configurações do relatório. Por padrão, os dados incluem uma linha para cada combinação de termo de pesquisa e ação de conversão no intervalo de dados especificado. As linhas estão na mesma ordem que as linhas da primeira planilha.

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  Use esta planilha para entender como cada termo de pesquisa gerou conversões, divididas por ação de conversão.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Colunas padrão

Para obter descrições de todas as colunas padrão e personalizadas, consulte &quot;[Colunas de relatório para relatórios especializados](specialty-report-columns.md)&quot;.

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] (incluído automaticamente na planilha [!UICONTROL AI Max Search Term #1], mesmo que você não o inclua explicitamente)
* [!UICONTROL Conversions] (incluído automaticamente na planilha [!UICONTROL AI Max Search Term #1], mesmo que você não o inclua explicitamente)
* [!UICONTROL Conversions Value] (incluído automaticamente na planilha [!UICONTROL AI Max Search Term #1], mesmo que você não o inclua explicitamente)

>[!MORELIKETHIS]
>
>* [Sobre relatórios especializados](specialty-report-about.md)
>* [Gerenciar relatórios agendados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Configurações do relatório de especialidades](specialty-report-settings.md)
>* [Colunas de relatório para relatórios especializados](specialty-report-columns.md)
