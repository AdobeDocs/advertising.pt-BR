---
title: Configurações de métrica personalizada
description: Fazer referência às configurações de métricas personalizadas, que são calculadas a partir das métricas padrão.
exl-id: f4b8c44e-ecb3-46dc-9a68-c079188e1d75
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Configurações de métrica personalizada

As configurações de métrica personalizada são um pouco diferentes em diferentes partes da interface.

## Configurações de métrica personalizada em exibições de gerenciamento de campanha

| Parâmetro/Seção | Descrição |
|----|----|
| Nome da métrica personalizada | O nome da métrica, que aparece como o nome da coluna. <b>Dica:</b> Use um nome de métrica significativo, mas considere que nomes mais longos tornam a coluna mais larga. |
| Inserir métrica | A fórmula matemática usada para calcular a nova métrica (como [Custo]/[Registros]:<ul><li>Para inserir uma métrica da lista de métricas de tráfego e receita, coloque o cursor onde deseja inserir a métrica e, em seguida, selecione a métrica na lista ou insira-a manualmente e entre colchetes (por exemplo, `[CPC]`).</li><li>Para inserir um operador, coloque o cursor onde deseja inserir o operador e clique no botão ou insira o símbolo manualmente. Os operadores matemáticos disponíveis: `+ - * / ( ) ()`</li></ul><b>Nota:</b> Métricas personalizadas complexas demoram mais para serem calculadas, e relatórios e visualizações que as incluem — especialmente quando incluem colunas separadas para conversões click-through e view-through — demoram mais para serem geradas. |
| Formato | Como apresentar os dados para esta métrica: *[!UICONTROL Currency]* (valor monetário), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (uma porcentagem com duas casas decimais).<br><br><b>Atenção:</b> Se você criar uma métrica derivada com o formato [!UICONTROL Number w/out Decimal Points] (que mostra dados como números inteiros) e os inclui em uma exibição ou em um relatório que usa uma regra de atribuição de conversão ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]ou [!UICONTROL Even Distribution]), então a saída é mostrada em números inteiros, não em decimais. Como resultado, campos de dados individuais podem estar incorretos, mesmo que os totais estejam corretos. Por exemplo, se uma ordem é dividida uniformemente entre três eventos, uma ordem (em vez de 0,33) é atribuída a cada um dos três eventos. Para evitar o problema, use o formato de métrica [!UICONTROL Number to 2 Decimal Points]. |

## Configurações de métrica personalizada em relatórios e modelos de relatório e na [!UICONTROL Portfolios] visualizações

| Parâmetro/Seção | Descrição |
|----|----|
| Nome da métrica personalizada | O nome da métrica, que aparece como o nome da coluna. <b>Dica:</b> Use um nome de métrica significativo, mas considere que nomes mais longos tornam a coluna mais larga. |
| Formato | Como apresentar os dados para esta métrica: *[!UICONTROL Currency]* (valor monetário), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (uma porcentagem com duas casas decimais).<br><br><b>Atenção:</b> Se você criar uma métrica derivada com o formato [!UICONTROL Number w/out Decimal Points] (que mostra dados como números inteiros) e os inclui em uma exibição ou em um relatório que usa uma regra de atribuição de conversão ponderada ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]ou [!UICONTROL Even Distribution]), então a saída é mostrada em números inteiros, não em decimais. Como resultado, campos de dados individuais podem estar incorretos, mesmo que os totais estejam corretos. Por exemplo, se uma ordem é dividida uniformemente entre três eventos, uma ordem (em vez de 0,33) é atribuída a cada um dos três eventos. Para evitar o problema, use o formato de métrica [!UICONTROL Number to 2 Decimal Points]. |
| Inserir métrica | Uma lista de métricas existentes a partir das quais é possível criar uma fórmula.<br><br>Para inserir uma métrica no campo de entrada da fórmula, coloque o cursor onde deseja inserir a métrica e, em seguida, selecione a métrica na lista ou insira-a manualmente e entre colchetes (por exemplo, `[CPC]`). |
| Inserir Operador | Os operadores matemáticos disponíveis: `+ - x / ( )`<br><br>Para inserir um operador no campo de entrada da fórmula, coloque o cursor onde deseja inserir o operador e clique no botão ou insira o símbolo manualmente. |
| [Campo de entrada de fórmula para a métrica] | A fórmula matemática usada para calcular a nova métrica com base em uma ou mais propriedades existentes ou métricas padrão (como `[Cost]/[Registrations]`. Pode incluir qualquer combinação de métricas e operadores.<br><br><b>Nota:</b> Métricas personalizadas complexas demoram mais para serem calculadas, e relatórios e visualizações que as incluem — especialmente quando incluem colunas separadas para conversões click-through e view-through — demoram mais para serem geradas. |

>[!MORELIKETHIS]
>
>* [Sobre métricas personalizadas](custom-metric-about.md)
>* [Criar uma métrica personalizada](custom-metric-create.md)
>* [Editar uma métrica personalizada](custom-metric-edit.md)
>* [Excluir uma métrica personalizada](custom-metric-delete.md)
