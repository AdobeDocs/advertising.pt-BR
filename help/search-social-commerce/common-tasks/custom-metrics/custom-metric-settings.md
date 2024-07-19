---
title: Configurações de métrica personalizada
description: Fazer referência às configurações de métricas personalizadas, que são calculadas a partir das métricas padrão.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Configurações de métrica personalizada

As configurações de métrica personalizada são um pouco diferentes em diferentes partes da interface.

## Configurações de métrica personalizada em exibições de gerenciamento de campanha

| Parâmetro/Seção | Descrição |
|----|----|
| Nome da métrica personalizada | O nome da métrica, que aparece como o nome da coluna. <b>Dica:</b> use um nome de métrica significativo, mas considere que nomes mais longos tornam a coluna mais larga. |
| Inserir métrica | A fórmula matemática usada para calcular a nova métrica (como [Custo]/[Registros]:<ul><li>Para inserir uma métrica da lista de métricas de tráfego e receita, coloque o cursor onde deseja inserir a métrica e selecione-a na lista ou insira-a manualmente e entre parênteses (por exemplo, `[CPC]`).</li><li>Para inserir um operador, coloque o cursor onde deseja inserir o operador e clique no botão ou insira o símbolo manualmente. Os operadores matemáticos disponíveis: `+ - * / ( ) ()`</li></ul><b>Observação:</b> métricas personalizadas complexas demoram mais para serem calculadas, e os relatórios e modos de exibição que as incluem (especialmente quando incluem colunas separadas para conversões click-through e view-through) demoram mais para serem gerados. |
| Formato | Como apresentar os dados para esta métrica: *[!UICONTROL Currency]* (um valor monetário), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (uma porcentagem com dois pontos decimais).<br><br><b>Cuidado:</b> se você criar uma métrica derivada com o formato [!UICONTROL Number w/out Decimal Points] (que mostra dados como números inteiros) e incluí-la em uma exibição ou em um relatório que use uma regra de atribuição de conversão ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), a saída será mostrada em números inteiros, não em decimais. Como resultado, campos de dados individuais podem estar incorretos, mesmo que os totais estejam corretos. Por exemplo, se uma ordem é dividida uniformemente entre três eventos, uma ordem (em vez de 0,33) é atribuída a cada um dos três eventos. Para evitar o problema, use o formato de métrica [!UICONTROL Number to 2 Decimal Points]. |

## Configurações de métrica personalizada em relatórios e modelos de relatório e nos modos de exibição [!UICONTROL Portfolios]

| Parâmetro/Seção | Descrição |
|----|----|
| Nome da métrica personalizada | O nome da métrica, que aparece como o nome da coluna. <b>Dica:</b> use um nome de métrica significativo, mas considere que nomes mais longos tornam a coluna mais larga. |
| Formato | Como apresentar os dados para esta métrica: *[!UICONTROL Currency]* (um valor monetário), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (uma porcentagem com dois pontos decimais).<br><br><b>Cuidado:</b> se você criar uma métrica derivada com o formato [!UICONTROL Number w/out Decimal Points] (que mostra dados como números inteiros) e incluí-la em uma exibição ou em um relatório que use uma regra de atribuição de conversão ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), a saída será mostrada em números inteiros, não em decimais. Como resultado, campos de dados individuais podem estar incorretos, mesmo que os totais estejam corretos. Por exemplo, se uma ordem é dividida uniformemente entre três eventos, uma ordem (em vez de 0,33) é atribuída a cada um dos três eventos. Para evitar o problema, use o formato de métrica [!UICONTROL Number to 2 Decimal Points]. |
| Inserir métrica | Uma lista de métricas existentes a partir das quais é possível criar uma fórmula.<br><br>Para inserir uma métrica no campo de entrada da fórmula, coloque o cursor onde deseja inserir a métrica e selecione-a na lista ou insira-a manualmente e entre parênteses (por exemplo, `[CPC]`). |
| Inserir Operador | Os operadores matemáticos disponíveis: `+ - x / ( )`<br><br>Para inserir um operador no campo de entrada da fórmula, coloque o cursor onde deseja inserir o operador e clique no botão ou insira o símbolo manualmente. |
| [Campo de entrada da fórmula para a métrica] | A fórmula matemática usada para calcular a nova métrica com base em uma ou mais propriedades existentes ou métricas padrão (como `[Cost]/[Registrations]`). Pode incluir qualquer combinação de métricas e operadores.<br><br><b>Observação:</b> métricas personalizadas complexas demoram mais para serem calculadas, e os relatórios e modos de exibição que as incluem (especialmente quando incluem colunas separadas para conversões click-through e view-through) demoram mais para serem gerados. |

>[!MORELIKETHIS]
>
>* [Sobre métricas personalizadas](custom-metric-about.md)
>* [Criar uma métrica personalizada](custom-metric-create.md)
>* [Editar uma métrica personalizada](custom-metric-edit.md)
>* [Excluir uma métrica personalizada](custom-metric-delete.md)
