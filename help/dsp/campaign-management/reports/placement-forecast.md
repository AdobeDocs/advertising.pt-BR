---
title: Exibir o Relatório de Previsão de Posicionamento
description: Consulte o número de impressões, gastos e lance máximo ideal previstos para uma estratégia de direcionamento específica para uma inserção.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: e901087b9128779bb4d55194cebfdc84c7c2ba2a
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Exibir o Relatório de Previsão de Posicionamento

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

A ferramenta de previsão de posicionamento mostra o número previsto de impressões, gastos e lance máximo ideal para uma estratégia de direcionamento específica. A previsão é calculada com base no inventário geral disponível com a disposição e nos usuários únicos disponíveis.

>[!NOTE]
>
>* Os códigos postais não são considerados nos cálculos de previsão de posicionamento.
>* Nenhuma previsão é gerada para inserções com direcionamento apenas programático garantido (PG), pois a disponibilidade e os gastos são determinísticos.

## Informações na Previsão

A previsão inclui as seguintes informações:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** O custo estimado por mil impressões (eCPM) que as configurações de direcionamento podem esperar alcançar.

   * **[!UICONTROL Budget]:** O orçamento estimado para as configurações de direcionamento.

   * **[!UICONTROL Impression]:** O número estimado de impressões para as configurações de direcionamento.

* **[!UICONTROL Budget Yield Curve]:** O número estimado de impressões que o posicionamento pode gerar em diferentes níveis de orçamento se todas as outras configurações de direcionamento forem iguais.

* **[!UICONTROL Max Bid Yield Curve]:** O gasto estimado para o posicionamento em diferentes níveis Máximos de Oferta, quando todas as outras configurações de direcionamento são iguais.

* **[!UICONTROL Message]:** Fornece informações sobre a saída prevista, incluindo cenários nos quais a previsão não pôde ser gerada. Também destaca as configurações de direcionamento analisadas, mas não consideradas nesse cenário devido à falta de dados.

### Cálculo de Orçamento

* Para inserções não atribuídas a um pacote, o orçamento de inserção é usado para cálculos. Dentro de um voo, o mesmo orçamento geral é calculado.

* Para posicionamentos em um pacote, o orçamento atribuído ao posicionamento é usado para cálculos. Durante o voo, o orçamento alocado para o posicionamento é calculado e incluído na mensagem.

* Para inserções adicionadas a um pacote em andamento, o orçamento é dividido igualmente com base no número de inserções. Quando a inserção é ativada, o orçamento atribuído pelo pacote é calculado.

## Requisitos

* Gasto mínimo: US$ 25 por dia ou equivalente em moeda local por posicionamento.

* Gasto máximo: US$ 15.000 por dia ou o equivalente em moeda local por posicionamento.

* Lance Máximo Mínimo, Lance Máximo Máximo: Há um lance máximo mínimo (para a Curva de Aproveitamento do Orçamento) e um lance máximo (para a Curva de Aproveitamento Máximo do Lance) por tipo de posicionamento. Esses valores são verdadeiros globalmente e não levam em conta as variações regionais. Às vezes, esses valores podem ser muito altos ou baixos para a região direcionada.

* Dados Históricos: A previsão de posicionamento estará disponível quando dados históricos suficientes estiverem disponíveis. Veja a seguir exemplos de quando dados históricos insuficientes podem estar disponíveis:

   * A disposição é direcionada a uma nova região para a campanha.

   * O posicionamento é direcionado a uma nova oferta de inventário para a campanha.

   * O posicionamento usa um novo tipo de anúncio para a campanha.

     Uma inserção geralmente é uma coleção de vários modelos de anúncio, conforme definido pelas plataformas do lado da oferta. Portanto, mesmo que o posicionamento já exista há muito tempo, o modelo de anúncio subjacente pode ser novo e a ferramenta de previsão não será capaz de fazer a previsão.

## Abrir o Relatório de Previsão de Posicionamento

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha e em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Localize o **[!UICONTROL Forecast]** na parte superior direita. Se necessário, clique em ![Previsão](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Às vezes, a previsão pode estar indisponível devido ao cache do navegador. Se isso acontecer, limpe o cache e tente novamente.

>[!MORELIKETHIS]
>
>* [Tipos de relatórios de desempenho em visualizações do Campaign Management](campaign-reports-about.md)
>* [Exibir os Relatórios de Diagnóstico de Posicionamento](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
