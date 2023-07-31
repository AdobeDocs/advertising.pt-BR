---
title: '[!UICONTROL Keyword Assist Report]'
description: Saiba mais sobre o [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# A variável [!UICONTROL Keyword Assist Report]

*Anunciantes com rastreamento de cliques em Search, Social e Commerce e com rastreamento de conversão do Adobe Advertising, Adobe Analytics (com um [!DNL Analytics] ), ou fornecidos em feeds usando um token (`ef_id`somente )*

A variável [!UICONTROL Keyword Assist Report] indica quais palavras-chave ou posicionamentos a unidade clica. O relatório mostra cada padrão de palavras-chave ou disposições de pesquisa paga que receberam cliques em um caminho de conversão e indica como esse padrão contribuiu para suas conversões gerais. Por exemplo, você poderia ver quantas conversões ocorreram quando os usuários clicaram em um anúncio pela primeira vez, resultante de uma pesquisa por palavra-chave para &quot;sapatos de couro&quot;, e depois clicaram em um anúncio após uma pesquisa por palavra-chave para &quot;sapatos de camurça&quot; e, em seguida, fizeram um pedido; ou você pode ver quantas conversões ocorreram depois que os usuários clicaram em anúncios resultantes de mais de 10 palavras-chave.

Os resultados do relatório incluem dados agregados para até N primeiras palavras-chave de pesquisa paga ou cliques de posicionamento no caminho de conversão ocorrido nas janelas de retrospectiva de cliques e retrospectiva de impressão do anunciante. Por exemplo, se você selecionar um tamanho de caminho de cinco (5), o relatório consistirá em caminhos de conversão que incluíram até as cinco palavras-chave ou disposições mais antigas que receberam cliques, com uma linha para cada padrão de cliques rastreados. Cada linha inclui a primeira palavra-chave ou posicionamento no caminho e a última palavra-chave ou posicionamento que resultou em conversões (mesmo se a última palavra-chave estiver fora do tamanho do caminho especificado). Por padrão, as linhas estão em ordem crescente pelo número de eventos no caminho.

>[!NOTE]
>
>Se o relatório incluir disposições de campanhas de pesquisa ativadas por conteúdo (que não incluem palavras-chave), a variável [!UICONTROL Keyword] A coluna mostra os nomes dos grupos de anúncios aplicáveis, como &quot;(adgroup content) Your Ad Group Name&quot;.

Opcionalmente, é possível incluir dados de conversão agregados para cada linha. Quando você inclui colunas de conversões/receita no relatório, cada tipo de conversão é representado em quatro colunas, mostrando a) o número total de conversões, b) a porcentagem de suas conversões gerais que foram atribuídas a esse padrão de palavra-chave, c) a latência média em dias desde o primeiro evento (na primeira palavra-chave) até uma conversão e d) a latência média em dias desde o último evento (na última palavra-chave) até uma conversão. Quando o caminho de conversão inclui mais palavras-chave do que o tamanho de caminho especificado, o relatório inclui linhas adicionais agregando dados para conversões resultantes do maior número de palavras-chave (como todos os padrões que incluíram cliques em seis palavras-chave).

Você pode exibir dados dos 18 meses anteriores.

## Colunas disponíveis

A seguir estão as colunas que estão disponíveis para cada relatório. As colunas padrão são incluídas automaticamente por padrão. Você pode adicionar as colunas personalizadas disponíveis na seção Colunas das configurações do relatório.

| Coluna | Padrão? | Descrição |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] para [!UICONTROL 5th Keyword] | Padrão | Os cinco primeiros cliques de inserção ou palavra-chave de pesquisa paga no caminho de conversão que ocorreram no anúncio [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Se o relatório incluir disposições de campanhas de pesquisa ativadas por conteúdo (que não incluem palavras-chave), essas colunas mostrarão os nomes de grupo de anúncios aplicáveis, como &quot;Seu nome de grupo de anúncios&quot;. |
| [!UICONTROL Path Size] | Padrão | O número de palavras-chave e/ou posicionamentos no caminho de conversão que ocorreram dentro do anúncio [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Padrão | A primeira palavra-chave ou posicionamento no caminho de conversão. |
| [!UICONTROL Last Keyword] | Padrão | A última palavra-chave ou posicionamento que resultou em conversões (mesmo se a última palavra-chave estiver fora do tamanho de caminho especificado). |
| \[Métricas personalizadas (derivadas) específicas do anunciante\] | Personalizado | O valor de uma métrica personalizada que você criou, calculado a partir das métricas existentes. |
| \[Propriedades de transação específicas do anunciante\] | Personalizado | O número de conversões de uma propriedade de transação ou métrica de envolvimento do site especificada. |
| [!UICONTROL % of Total] \[propriedade de transação\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada propriedade de transação incluída) A porcentagem de suas conversões gerais em portfólios que foram atribuídas à palavra-chave e/ou ao padrão de posicionamento. |
| [!UICONTROL 6th Keyword] para [!UICONTROL 10th Keyword] | Personalizado | A sexta a décima palavra-chave de pesquisa paga ou cliques de posicionamento no caminho de conversão que ocorreu dentro do anúncio [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Nota:</b> Se o relatório incluir disposições de campanhas de pesquisa ativadas por conteúdo (que não incluem palavras-chave), essas colunas mostrarão os nomes de grupo de anúncios aplicáveis, como &quot;Seu nome de grupo de anúncios&quot;. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[propriedade de transação\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório para cada propriedade de transação incluída) A latência média em dias desde o primeiro evento (na primeira palavra-chave ou disposição) até uma conversão. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[propriedade de transação\] | Automático | (Não disponível nas configurações do relatório, mas incluído automaticamente na saída do relatório) A latência média em dias desde o último evento (na última palavra-chave ou disposição) até uma conversão. |
| [!UICONTROL Path Frequency] | Personalizado | O número de vezes que o caminho desta linha ocorreu antes da conversão. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de assistência](assist-report-about.md)
>* [A variável [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [A variável [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Ajudar configurações do relatório](assist-report-settings.md)
>* [Gerar um relatório de assistência](assist-report-generate.md)
