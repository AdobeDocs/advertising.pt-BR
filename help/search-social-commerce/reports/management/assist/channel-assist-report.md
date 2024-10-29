---
title: '[!UICONTROL Channel Assist Report]'
description: Saiba mais sobre o [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# O [!UICONTROL Channel Assist Report]

*Anunciantes com rastreamento de cliques em Search, Social e Commerce e com rastreamento de conversão do Adobe Advertising, Adobe Analytics (com uma integração [!DNL Analytics]) ou fornecidos em feeds usando apenas um token (`ef_id`)*

O [!UICONTROL Channel Assist Report] indica como vários canais de marketing (pesquisa ou social do Search, Social, &amp; Commerce; ou exibição ou vídeo do Advertising DSP) ajudaram no processo de conversão. O relatório mostra como cada padrão de tipos de evento que levou a uma ou mais conversões contribuiu para suas conversões gerais. Por exemplo, você veria quantas conversões ocorreram quando os usuários viram pela primeira vez uma impressão de anúncio de exibição, clicaram em um anúncio de pesquisa e colocaram um pedido ou quantas conversões ocorreram depois que os usuários interagiram com mais de 10 anúncios. Os tipos de evento incluem cliques de pesquisa, impressões e cliques de exibição, impressões e cliques de vídeo e outras impressões e outros cliques. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Os resultados do relatório incluem dados agregados para cada padrão de tipos de evento no caminho de conversão — até os N primeiros tipos de evento — que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. Por exemplo, se você selecionar um tamanho de caminho de cinco (5), o relatório incluirá caminhos de conversão que incluíram até os cinco eventos mais antigos, com uma linha para cada padrão de tipos de evento rastreados (como &quot;clique de pesquisa&quot; e &quot;impressão de exibição&quot;). Cada linha mostra um padrão de eventos, incluindo o primeiro evento no caminho e o último evento que resultou em conversões (mesmo se o último evento estiver fora do tamanho do caminho especificado). Por padrão, as linhas estão em ordem crescente pelo número de eventos no caminho.

Opcionalmente, é possível incluir dados de conversão agregados para cada linha. Quando você inclui colunas de conversões/receita no relatório, cada tipo de conversão é representado em quatro colunas, mostrando a) o número total de conversões, b) a porcentagem de suas conversões gerais que foram atribuídas a esse padrão de evento, c) a latência média no dia, desde o primeiro evento até uma conversão, e d) a latência média em dias, desde o último evento até uma conversão. Quando o caminho de conversão inclui mais eventos do que o tamanho de caminho especificado, o relatório inclui linhas adicionais agregando dados para conversões resultantes do maior número de eventos (como todos os padrões que incluíam seis tipos de evento).

Você pode exibir dados dos 18 meses anteriores.

## Colunas disponíveis

A seguir estão as colunas que estão disponíveis para cada relatório. As colunas padrão são incluídas automaticamente por padrão. Você pode adicionar as colunas personalizadas disponíveis na seção Colunas das configurações do relatório.

| Coluna | Padrão? | Descrição |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] a [!UICONTROL 5th Event] | Padrão | Os cinco primeiros tipos de evento no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. |
| [!UICONTROL Path Size] | Padrão | O número de tipos de evento no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. |
| [!UICONTROL First Event Type] | Padrão | O tipo do primeiro evento (mais antigo) no caminho de conversão. |
| [!UICONTROL Last Event Type] | Padrão | O tipo do último evento que resultou em conversões (mesmo se o último evento estiver fora do tamanho de caminho especificado). |
| \[Métricas personalizadas (derivadas) específicas do anunciante\] | Personalizado | O valor de uma métrica personalizada que você criou, calculado a partir das métricas existentes. |
| \[Métricas de conversão específicas do anunciante\] | Personalizado | O número de conversões de uma métrica de conversão ou métrica de envolvimento do site especificada. |
| [!UICONTROL % of Total] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) A porcentagem de suas conversões gerais em portfólios que foram atribuídas ao padrão do evento. |
| [!UICONTROL 6th Event] a [!UICONTROL 30th Event] | Personalizado | Os tipos de evento do sexto ao trigésimo no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) A latência média em dias desde o primeiro evento até uma conversão. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório) A latência média em dias desde o último evento até uma conversão. |
| [!UICONTROL Path Frequency] | Personalizado | O número de vezes que o caminho desta linha ocorreu antes da conversão. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de assistência](assist-report-about.md)
>* [O [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [O [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Ajudar configurações do relatório](assist-report-settings.md)
>* [Gerar um relatório de assistência](assist-report-generate.md)
