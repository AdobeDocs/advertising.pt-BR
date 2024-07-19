---
title: '[!UICONTROL Keyword Assist Report]'
description: Saiba mais sobre o [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# O [!UICONTROL Keyword Assist Report]

*Anunciantes com rastreamento de cliques em Search, Social e Commerce e com rastreamento de conversão do Adobe Advertising, Adobe Analytics (com uma integração [!DNL Analytics]) ou fornecidos em feeds usando apenas um token (`ef_id`)*

O [!UICONTROL Keyword Assist Report] indica quais palavras-chave ou posicionamentos são clicados na unidade. O relatório mostra cada padrão de palavras-chave ou disposições de pesquisa paga que receberam cliques em um caminho de conversão e indica como esse padrão contribuiu para suas conversões gerais. Por exemplo, você poderia ver quantas conversões ocorreram quando os usuários clicaram em um anúncio pela primeira vez, resultante de uma pesquisa por palavra-chave para &quot;sapatos de couro&quot;, e depois clicaram em um anúncio após uma pesquisa por palavra-chave para &quot;sapatos de camurça&quot; e, em seguida, fizeram um pedido; ou você pode ver quantas conversões ocorreram depois que os usuários clicaram em anúncios resultantes de mais de 10 palavras-chave.

Os resultados do relatório incluem dados agregados para até N primeiras palavras-chave de pesquisa paga ou cliques de posicionamento no caminho de conversão que ocorreram no do anunciante
clique em janelas de retrospectiva e de retrospectiva de impressão. Por exemplo, se você selecionar um tamanho de caminho de cinco (5), o relatório consistirá em caminhos de conversão que incluíram até as cinco palavras-chave ou disposições mais antigas que receberam cliques, com uma linha para cada padrão de cliques rastreados. Cada linha inclui a primeira palavra-chave ou posicionamento no caminho e a última palavra-chave ou posicionamento que resultou em conversões (mesmo se a última palavra-chave estiver fora do tamanho do caminho especificado). Por padrão, as linhas estão em ordem crescente pelo número de eventos no caminho.

>[!NOTE]
>
>Se o relatório incluir disposições de campanhas de pesquisa habilitadas para conteúdo (que não incluem palavras-chave), a coluna [!UICONTROL Keyword] mostrará os nomes de grupos de anúncios aplicáveis, como &quot;(conteúdo de grupo de anúncios) Nome do grupo de anúncios.&quot;

Opcionalmente, é possível incluir dados de conversão agregados para cada linha. Quando você inclui colunas de conversões/receita no relatório, cada tipo de conversão é representado em quatro colunas, mostrando a) o número total de conversões, b) a porcentagem de suas conversões gerais que foram atribuídas a esse padrão de palavra-chave, c) a latência média em dias desde o primeiro evento (na primeira palavra-chave) até uma conversão e d) a latência média em dias desde o último evento (na última palavra-chave) até uma conversão. Quando o caminho de conversão inclui mais palavras-chave do que o tamanho de caminho especificado, o relatório inclui linhas adicionais agregando dados para conversões resultantes do maior número de palavras-chave (como todos os padrões que incluíram cliques em seis palavras-chave).

Você pode exibir dados dos 18 meses anteriores.

## Colunas disponíveis

A seguir estão as colunas que estão disponíveis para cada relatório. As colunas padrão são incluídas automaticamente por padrão. Você pode adicionar as colunas personalizadas disponíveis na seção Colunas das configurações do relatório.

| Coluna | Padrão? | Descrição |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] a [!UICONTROL 5th Keyword] | Padrão | Os cinco primeiros cliques de posicionamento ou palavra-chave de pesquisa paga no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante.<br><br><b>Observação:</b> se o relatório incluir disposições de campanhas de pesquisa habilitadas para conteúdo (que não incluem palavras-chave), essas colunas mostrarão os nomes de grupos de anúncios aplicáveis, como &quot;Seu Nome de Grupo de Anúncios&quot;. |
| [!UICONTROL Path Size] | Padrão | O número de palavras-chave e/ou posicionamentos no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante. |
| [!UICONTROL First Keyword] | Padrão | A primeira palavra-chave ou posicionamento no caminho de conversão. |
| [!UICONTROL Last Keyword] | Padrão | A última palavra-chave ou posicionamento que resultou em conversões (mesmo se a última palavra-chave estiver fora do tamanho de caminho especificado). |
| \[Métricas personalizadas (derivadas) específicas do anunciante\] | Personalizado | O valor de uma métrica personalizada que você criou, calculado a partir das métricas existentes. |
| \[Métricas de conversão específicas do anunciante\] | Personalizado | O número de conversões de uma métrica de conversão ou métrica de envolvimento do site especificada. |
| [!UICONTROL % of Total] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) A porcentagem de suas conversões gerais em portfólios que foram atribuídas à palavra-chave e/ou ao padrão de posicionamento. |
| [!UICONTROL 6th Keyword] a [!UICONTROL 10th Keyword] | Personalizado | A sexta a décima palavra-chave de pesquisa paga ou os cliques de posicionamento no caminho de conversão que ocorreram na [janela de pesquisa de cliques](/help/search-social-commerce/glossary.md#c-d) e na [janela de pesquisa de impressão](/help/search-social-commerce/glossary.md#i-j) do anunciante.<br><br><b>Observação:</b> se o relatório incluir disposições de campanhas de pesquisa habilitadas para conteúdo (que não incluem palavras-chave), essas colunas mostrarão os nomes de grupos de anúncios aplicáveis, como &quot;Seu Nome de Grupo de Anúncios&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada métrica de conversão incluída) A latência média em dias desde o primeiro evento (na primeira palavra-chave ou disposição) até uma conversão. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[métrica de conversão\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório) A latência média em dias desde o último evento (na última palavra-chave ou disposição) até uma conversão. |
| [!UICONTROL Path Frequency] | Personalizado | O número de vezes que o caminho desta linha ocorreu antes da conversão. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de assistência](assist-report-about.md)
>* [O [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [O [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Ajudar configurações do relatório](assist-report-settings.md)
>* [Gerar um relatório de assistência](assist-report-generate.md)
