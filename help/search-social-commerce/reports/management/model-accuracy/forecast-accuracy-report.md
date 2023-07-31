---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Saiba mais sobre o Relatório de Precisão da Previsão, incluindo as colunas de dados.
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# A variável [!UICONTROL Forecast Accuracy Report]

O relatório mostra a precisão dos modelos de custo e receita por dia para portfólios especificados. Por padrão, inclui a receita, o custo e os cliques diários previstos e reais — e a precisão das previsões — para cada portfólio. Inclui dados de campanhas que estão mapeadas para os portfólios no momento.

Você pode exibir dados dos 18 meses anteriores.

>[!NOTE]
>
>* Esse relatório fornece os mesmos dados que o nível de portfólio [!UICONTROL Model Accuracy Report] exceto que é possível executá-lo em vários portfólios e alterar a regra de atribuição. Você também pode executar e agendar o relatório usando parâmetros personalizados e pode usá-lo para criar feeds de planilha.
>
>* A prática recomendada é exibir as [!UICONTROL Forecast Accuracy Report] durante pelo menos os últimos sete dias, pois, independentemente da estratégia de gastos do portfólio, a maioria dos portfólios vê uma tendência inerente de dia da semana. A capacidade de otimização leva essa tendência em consideração e aloca os gastos de acordo.
>
>* Para previsões de custos, um desvio de 10% nos últimos sete dias é considerado aceitável, portanto, o gasto real que está entre 90% e 110% do gasto previsto está correto. Para previsões de receita, um desvio de 15% nos últimos sete dias é considerado aceitável, portanto, a receita real que está entre 85% e 115% do gasto previsto está boa. Previsões com desvios maiores devem ser investigadas.
>
>* Quando palavras-chave no portfólio são associadas a restrições de mudança de oferta, o portfólio gasta mais ou menos pelo valor total causado pela mudança de oferta. Como resultado, as colunas de custo previstas se desviam do gasto pretendido pelo aumento ou diminuição do gasto.

## Colunas disponíveis

A seguir estão as colunas que estão disponíveis para cada relatório. As colunas padrão são incluídas automaticamente por padrão. É possível adicionar as colunas personalizadas disponíveis na [!UICONTROL Columns] seção das configurações do relatório.

| Coluna | Padrão? | Descrição |
|----|----|----|
| [!UICONTROL Portfolio] | Padrão | O portfólio. |
| [!UICONTROL Day of Week] | Padrão | O dia da semana relatado: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Padrão | O primeiro dia reportado. |
| [!UICONTROL End Date] | Padrão | O último dia reportado. |
| [!UICONTROL Predicted Revenue] | Padrão | A receita prevista do portfólio. |
| [!UICONTROL Revenue] | Padrão | A receita real do portfólio. |
| [!UICONTROL Revenue Accuracy] | Padrão | A precisão da previsão de receita, expressa como uma porcentagem. |
| [!UICONTROL Predicted Cost] | Padrão | O custo previsto do portfólio. |
| [!UICONTROL Cost] | Padrão | O custo real do portfólio. |
| [!UICONTROL Cost Accuracy] | Padrão | A precisão da previsão de custos, expressa como uma porcentagem. |
| [!UICONTROL Predicted Clicks] | Padrão | O número de cliques previstos para o portfólio. |
| [!UICONTROL Clicks] | Padrão | O número real de cliques do portfólio. |
| [!UICONTROL Click Accuracy] | Padrão | A precisão da previsão de cliques, expressa como uma porcentagem. |
| [!UICONTROL EF Portfolio Group ID] | Padrão | A ID numérica do grupo de portfólios ao qual o portfólio pertence. |
| [!UICONTROL Portfolio Group Name] | Padrão | O nome do grupo de portfólio ao qual o portfólio pertence. |
| [!UICONTROL Portfolio ID] | Padrão | A ID numérica do portfólio. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de precisão de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [A variável [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Gerar um relatório de precisão de modelo](model-accuracy-report-generate.md)
>* [Configurações do relatório de precisão do modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
