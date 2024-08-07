---
title: '[!UICONTROL Campaign Assist Report]'
description: Saiba mais sobre o [!UICONTROL Campaign Assist Report].
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# O [!UICONTROL Campaign Assist Report]

*Anunciantes com rastreamento de cliques em Search, Social e Commerce e com rastreamento de conversão do Adobe Advertising, Adobe Analytics (com uma integração [!DNL Analytics]) ou fornecidos em feeds usando apenas um token (`ef_id`)*

O [!UICONTROL Campaign Assist Report] indica quais campanhas ajudaram no processo de conversão. Os relatórios mostram como cada padrão de campanhas cujos anúncios levaram a uma ou mais conversões contribuiu para suas conversões gerais. Por exemplo, você pode ver quantas conversões ocorreram quando os usuários viram um anúncio da Campanha A pela primeira vez, clicaram em um anúncio da Campanha B e fizeram um pedido. Da mesma forma, você pode ver quantas conversões ocorreram depois que os usuários interagiram com anúncios de mais de 10 campanhas.

Os resultados do relatório incluem dados agregados para cada padrão de campanhas no caminho de conversão — até as N primeiras campanhas — para eventos que ocorreram na [janela de retrospectiva de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. Por exemplo, se você selecionar um tamanho de caminho de cinco (5), o relatório incluirá caminhos de conversão que incluíram até as cinco campanhas mais antigas, com uma linha para cada padrão de campanhas cujos eventos foram rastreados. Cada linha mostra um padrão de campanhas, incluindo a primeira campanha no caminho e a última campanha que resultou em conversões (mesmo se a última campanha estiver fora do tamanho do caminho especificado). Por padrão, as linhas são em ordem crescente pelo número de campanhas no caminho.

Opcionalmente, é possível incluir dados de conversão agregados, incluindo suas métricas personalizadas, para cada linha. Ao incluir colunas de conversões/receita no relatório, cada tipo de conversão é representado em quatro colunas, mostrando a) o número total de conversões, b) a porcentagem de suas conversões gerais que foram atribuídas a esse padrão de campanha, c) a latência média em dias desde o primeiro evento (na primeira campanha) até uma conversão e d) a latência média em dias desde o último evento (na última campanha) até uma conversão. Quando o caminho de conversão inclui mais campanhas do que o tamanho do caminho especificado, o relatório inclui linhas adicionais agregando dados para conversões resultantes de números mais altos de campanhas (como todos os padrões que incluíam seis campanhas).

Também é possível incluir a rede de publicidade e/ou o tipo de evento após o nome da campanha, como `<campaign name> (Google) click`.

Você pode exibir dados dos 18 meses anteriores.

>[!TIP]
>
>Se as palavras-chave da sua marca estiverem em uma campanha diferente das palavras-chave genéricas, o relatório indicará se as palavras-chave da sua marca contribuem para conversões.

## Colunas disponíveis

A seguir estão as colunas que estão disponíveis para cada relatório. As colunas padrão são incluídas automaticamente por padrão. Você pode adicionar as colunas personalizadas disponíveis na seção Colunas das configurações do relatório.

| Coluna | Padrão? | Descrição |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] a [!UICONTROL 5th Campaign] | Padrão | As cinco primeiras campanhas no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante.<br><br>Se você incluiu qualquer uma das opções de relatório para indicar a rede de publicidade, o nome da conta ou o tipo de evento após o nome da entidade, essas informações serão incluídas após o nome da campanha (como `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Padrão | O número de campanhas no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. |
| [!UICONTROL First Campaign] | Padrão | A primeira campanha no caminho de conversão. |
| [!UICONTROL Last Campaign] | Padrão | A última campanha que resultou em conversões (mesmo se a última palavra-chave estiver fora do tamanho de caminho especificado.)<br><br>Se você incluiu qualquer uma das opções de relatório para indicar a rede de publicidade, o nome da conta ou o tipo de evento após o nome da entidade, essas informações serão incluídas após o nome da campanha (como `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Métricas personalizadas (derivadas) específicas do anunciante\] | Personalizado | O valor de uma métrica personalizada que você criou, calculado a partir das métricas existentes. |
| \[Métricas de conversão específicas do anunciante\] | Personalizado | O número de conversões de uma métrica de conversão ou métrica de envolvimento do site especificada. |
| [!UICONTROL % of Total] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) O número de conversões de uma métrica de conversão especificada que resultou do padrão da campanha. |
| [!UICONTROL 6th Campaign] a [!UICONTROL 20th Campaign] | Personalizado | A sexta a 20ª campanhas no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante.<br><br>Se você incluiu qualquer uma das opções de relatório para indicar a rede de publicidade, o nome da conta ou o tipo de evento após o nome da entidade, essas informações serão incluídas após o nome da campanha (como `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) A latência média em dias desde o primeiro evento (na primeira campanha) até uma conversão. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório) A latência média em dias desde o último evento (na última campanha) até uma conversão. |
| [!UICONTROL EF Campaign ID] | Personalizado | A ID numérica que o Search, Social e Commerce atribui à campanha. |
| [!UICONTROL EF Portfolio Group ID] | Personalizado | A ID numérica do grupo de portfólios ao qual o portfólio pertence. |
| [!UICONTROL EF Search Engine ID] | Personalizado | A ID numérica que o Search, Social e Commerce atribui à rede de publicidade: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto) ou <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| [!UICONTROL Portfolio ID] | A ID numérica do portfólio. |
| [!UICONTROL User SE Account ID] | A ID numérica que o Search, Social e Commerce atribui à rede de publicidade. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de assistência](assist-report-about.md)
>* [O [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [O [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Ajudar configurações do relatório](assist-report-settings.md)
>* [Gerar um relatório de assistência](assist-report-generate.md)
