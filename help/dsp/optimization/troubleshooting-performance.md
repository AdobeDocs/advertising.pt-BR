---
title: Solução de problemas de desempenho
description: Consulte problemas comuns de desempenho e veja como solucioná-los.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Solução de problemas de desempenho

| Problema | Causa possível | Ações a serem executadas |
| --- | --- | --- |
| Nenhum gasto com posicionamento | O posicionamento não inclui anúncios e/ou os anúncios não estão ativos. | Verifique se todos os anúncios esperados estão anexados ao posicionamento e se foram aprovados e estão ativos.<br><br>Além disso, veja se o posicionamento inclui um agendamento de anúncio personalizado, o que pode limitar o período de veiculação de cada anúncio. Para ver a programação de anúncio para uma disposição da exibição Disposições, clique em  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** ao lado do nome do posicionamento. |
|  | As datas afetadas não estão dentro das datas de voo configuradas. | Verifique se as datas de início e término são válidas nos níveis &#x200B; campanha, pacote e posicionamento. |
|  | A meta de orçamento foi atingida e/ou não é alta o suficiente. | Verifique as configurações de orçamento nos níveis de campanha, pacote e posicionamento. |
|  | A conta não tem financiamento suficiente. | Para verificar se a sua conta possui financiamento adequado, acesse **[!UICONTROL Settings]** > **[!UICONTROL Account]** e observe a quantidade de [!UICONTROL Usable Funds]. Se precisar adicionar mais fundos, entre em contato com a equipe de conta do Adobe. |
|  | Nenhum inventário disponível. | Verifique se as origens de inventário especificadas ([!UICONTROL Public], [!UICONTROL Private]ou [!UICONTROL On Demand]) são:<ul><li>Configure corretamente.</li><li>Ativo e envio em leilões.</li><li>Compatível com o tipo de anúncio e posicionamento aplicável.</li></ul><br>Se todas as origens de inventário forem válidas e ativas, direcione para origens adicionais ou todas as origens de inventário, quando possível. |
|  | Não há usuários disponíveis. | Verifique se os públicos-alvo especificados incluem um número suficiente de usuários ativos. Caso contrário, expanda os públicos-alvo adicionando mais públicos-alvo. |
| Baixo gasto com posicionamento | A variável [!UICONTROL Non Bids] seção do relatório diagnóstico de posicionamento mostra possíveis motivos para o posicionamento não ter dado lance. | [Revise o [!UICONTROL Non Bids] relatório](/help/dsp/campaign-management/reports/placement-diagnostics.md) para entender por que a inserção não deu certo.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | O posicionamento usa [filtros pré-oferta](/help/dsp/campaign-management/placements/placement-settings.md) que limitam a licitação. | Diminua os limites dos filtros de pré-oferta em 5% para avaliar o equilíbrio entre gasto e desempenho. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Lembre-se de que o uso de vários públicos-alvo de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | A colocação tem uma baixa taxa de vitória. | Aumente o [!UICONTROL Max Bid] para melhorar a taxa de ganhos.<br><br><b>NOTA:</b> Os preços de estoque podem variar com base no direcionamento do posicionamento.<br><br>Uma taxa de ganho de 10% é considerada saudável. |
|  | Um número baixo de estoque está disponível. | Direcione todas as origens de inventário ou adicionais, se possível.<br><br>Lembre-se de que o uso de vários públicos-alvo de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | Um número baixo de usuários está disponível. | Verifique se os públicos-alvo especificados incluem um número suficiente de usuários ativos. Caso contrário, expanda os públicos-alvo adicionando mais públicos-alvo.<br><br>Lembre-se de que o uso de vários públicos-alvo de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente os lances e os gastos. |
|  | O pacote inclui um grande número de disposições ativas. | Reduza o número de posicionamentos ativos no pacote ou aumente o orçamento geral do pacote.<br><br>Se o pacote tiver muitas disposições, mas não tiver orçamento suficiente, o DSP talvez não consiga alocar orçamento suficiente para cada disposição. Cada posicionamento deve ter a oportunidade de gastar pelo menos 2 dólares por dia. Por exemplo, se o pacote tiver um orçamento de US$ 10 por dia, será melhor incluir cinco ou menos disposições. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)

