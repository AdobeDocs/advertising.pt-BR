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
| Nenhum gasto com posicionamento | O posicionamento não inclui anúncios e/ou os anúncios não estão ativos. | Verifique se todos os anúncios esperados estão anexados ao posicionamento e se foram aprovados e estão ativos.<br><br>Além disso, veja se o posicionamento inclui um agendamento de anúncio personalizado, o que pode limitar o período de veiculação de cada anúncio. Para ver o agendamento de anúncio para um posicionamento no modo de exibição de Posicionamentos, clique em **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** ao lado do nome do posicionamento. |
| | As datas afetadas não estão dentro das datas de voo configuradas. | Verifique se as datas de início e término são válidas nos níveis &#x200B; campanha, pacote e posicionamento. |
| | A meta de orçamento foi atingida e/ou não é alta o suficiente. | Verifique as configurações de orçamento nos níveis de campanha, pacote e posicionamento. |
| | A conta não tem financiamento suficiente. | Para ver se sua conta possui fundos adequados, vá para **[!UICONTROL Settings]** > **[!UICONTROL Account]** e verifique o valor de [!UICONTROL Usable Funds]. Se precisar adicionar mais fundos, entre em contato com a equipe de conta do Adobe. |
| | Nenhum inventário disponível. | Verifique se as fontes de estoque especificadas ([!UICONTROL Public], [!UICONTROL Private] ou [!UICONTROL On Demand]) são:<ul><li>Configure corretamente.</li><li>Ativo e envio em leilões.</li><li>Compatível com o tipo de anúncio e posicionamento aplicável.</li></ul><br>Se todas as origens de estoque forem válidas e ativas, direcione para origens adicionais ou todas as origens de estoque, quando possível. |
| | Não há usuários disponíveis. | Verifique se os públicos-alvo especificados incluem um número suficiente de usuários ativos. Caso contrário, expanda os públicos-alvo adicionando mais públicos-alvo. |
| Baixo gasto com posicionamento | A seção [!UICONTROL Non Bids] do relatório de diagnóstico de posicionamento mostra possíveis motivos para o posicionamento não ter dado lance. | [Revise o relatório [!UICONTROL Non Bids]](/help/dsp/campaign-management/reports/placement-diagnostics.md) para entender por que o posicionamento não deu lance.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | O posicionamento usa [filtros pré-oferta](/help/dsp/campaign-management/placements/placement-settings.md) que limitam a oferta. | Diminua os limites dos filtros de pré-oferta em 5% para avaliar o equilíbrio entre gasto e desempenho. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Lembre-se de que o uso de vários destinos de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente ofertas e gastos. |
| | A colocação tem uma baixa taxa de vitória. | Aumente o [!UICONTROL Max Bid] para melhorar a taxa de vitória.<br><br><b>OBSERVAÇÃO:</b> os preços de estoque podem variar com base no direcionamento da disposição.<br><br>Uma taxa de ganhos de 10% é considerada íntegra. |
| | Um número baixo de estoque está disponível. | Direcione todas as origens de inventário ou adicionais, se possível.<br><br>Lembre-se de que o uso de vários destinos de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente ofertas e gastos. |
| | Um número baixo de usuários está disponível. | Verifique se os públicos-alvo especificados incluem um número suficiente de usuários ativos. Caso contrário, expanda os públicos-alvo adicionando mais públicos-alvo.<br><br>Lembre-se de que o uso de vários destinos de posicionamento, como filtros pré-oferta, geografia, inventário e públicos-alvo, pode limitar cumulativamente ofertas e gastos. |
| | O pacote inclui um grande número de disposições ativas. | Reduza o número de posicionamentos ativos no pacote ou aumente o orçamento geral do pacote.<br><br>Se o pacote tiver muitas disposições, mas não tiver orçamento suficiente, o DSP talvez não consiga alocar orçamento suficiente para cada disposição. Cada posicionamento deve ter a oportunidade de gastar pelo menos 2 dólares por dia. Por exemplo, se o pacote tiver um orçamento de US$ 10 por dia, será melhor incluir cinco ou menos disposições. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)
