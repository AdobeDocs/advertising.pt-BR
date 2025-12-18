---
title: Exibir alertas
description: Saiba como visualizar alertas e resoluções recomendadas para suas campanhas e componentes da campanha.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# Exibir alertas

O DSP ajuda a identificar quando qualquer uma das campanhas ou componentes da campanha tem problemas. Para cada problema, o DSP cria um alerta com um carimbo de data e hora e a ação recomendada para resolver o problema. Os motivos para os alertas incluem problemas de configuração (por exemplo, quando nenhum anúncio está anexado a um posicionamento ou quando um negócio é configurado incorretamente), rejeição de anúncios e problemas de integridade da campanha (como baixa entrega de anúncios ou desempenho). Os alertas estão disponíveis nos níveis de campanha, pacote, posicionamento, anúncio e negociação.

Os alertas estão disponíveis nos seguintes locais:

* Um ícone [!UICONTROL Pulse Panel] nas exibições [!UICONTROL Campaigns], [!UICONTROL Packages] e detalhes do pacote, [!UICONTROL Placements] e [!UICONTROL Ads] indica se há alertas disponíveis para os itens nessa exibição. Quando o ícone tem um ponto azul (![ícone de Painel de Pulso quando os alertas estão disponíveis](/help/dsp/assets/alerts-panel.png "ícone de Painel de Pulso quando os alertas estão disponíveis")), os alertas estão disponíveis. Quando nenhum ponto estiver visível (![Ícone Pulse Panel quando nenhum alerta estiver disponível](/help/dsp/assets/alerts-panel-empty.png "Ícone Pulse Panel quando nenhum alerta estiver disponível")), nenhum alerta estará disponível.

* As tabelas de dados nas mesmas exibições incluem uma coluna &quot;[!UICONTROL Alerts]&quot; que indica quando o item — ou seus componentes — tem um problema. Os indicadores de alerta incluem &quot;Crítico&quot; (![Crítico](/help/dsp/assets/indicator-critical.png "Crítico")), &quot;Aviso&quot; (![Aviso](/help/dsp/assets/indicator-warning.png "Aviso")) e &quot;Informações&quot; (![Informações](/help/dsp/assets/indicator-information.png "Informações")).

É possível abrir a visualização relevante do gerenciamento de campanha para qualquer alerta, para que você possa editar as configurações conforme necessário para resolver o problema.

Você também pode optar por ignorar um alerta individual, o que o remove do painel [!UICONTROL Pulse].

Os alertas e indicadores de alerta desaparecem automaticamente quando os problemas subjacentes são resolvidos.

## Exibir Alertas no [!UICONTROL Pulse Panel]

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * (Para todos os alertas aplicáveis ao modo de exibição) À direita da barra de ferramentas em qualquer modo de exibição de gerenciamento de campanha, clique no ícone ![Painel de Pulso quando os alertas estiverem disponíveis](/help/dsp/assets/alerts-panel.png "Painel de Pulso quando os alertas estiverem disponíveis").

   * (Para todos os alertas de uma campanha específica) Clique no indicador de alerta de uma linha de campanha e clique em **[!UICONTROL View in Pulse panel]**.

   * (Para todos os alertas de um pacote, posicionamento ou anúncio específico) Faça o seguinte:

      1. Clique no nome da campanha.

      1. No submenu, clique em **[!UICONTROL Packages]**, **[!UICONTROL Placements]** ou **[!UICONTROL Ads]** para abrir a exibição de componente de campanha relevante.

      1. Clique no indicador de alerta de um pacote, posicionamento ou linha de anúncio e clique em **[!UICONTROL View in Pulse Panel]**.

   Todos os alertas associados à campanha e seus componentes, incluindo ofertas segmentadas, são listados. Por padrão, os alertas críticos são listados primeiro.

1. (Opcional) Para agrupar os alertas de acordo com sua primeira data de detecção, ou para filtrar os alertas por status de alerta, status do componente, tipo de componente ou com um nome de campanha específico, clique no ![botão Filtrar](/help/dsp/assets/filter.png) no canto superior direito do painel, selecione as opções de filtro e clique em **[!UICONTROL Apply]**.

1. Para exibir uma lista de todos os componentes afetados da campanha para um tipo de alerta específico, clique no nome do alerta, como &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Para exibir os detalhes de cada componente afetado, incluindo a ação recomendada, clique em [!UICONTROL EXPAND ALL] ou clique no nome do componente. Para abrir o modo de exibição de gerenciamento de campanha relevante para qualquer componente afetado, de modo que você possa fazer as alterações recomendadas, mantenha o cursor sobre o nome do componente e clique em ![Ir para o modo de exibição](/help/dsp/assets/go-to-view.png "Ir para o modo de exibição").

1. (Opcional) Para ignorar (ocultar) um alerta, mantenha o cursor sobre o nome do componente e clique em ![Ignorar](/help/dsp/assets/alert-ignore.png "Ignorar") e em **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]** ou **[!UICONTROL Ignore indefinitely]**.

Você tem alguns segundos após ignorar um alerta para desfazer a ação. Depois que a mensagem de opção é fechada, você não pode cancelar a ação.

1. (Opcional) Para recuperar alertas ignorados, filtre os alertas para mostrar um [!UICONTROL Alert Status] de &quot;[!UICONTROL All]&quot; ou &quot;[!UICONTROL Ignored]&quot;.&quot; Para não ignorar um alerta, mantenha o cursor sobre o nome do componente e clique em ![Cancelar ignorância](/help/dsp/assets/alert-un-ignore.png "Cancelar ignorância").

## Fechar o [!UICONTROL Pulse Panel]

* À direita da barra de ferramentas, clique no ícone ![Painel de Pulso quando os alertas estiverem disponíveis](/help/dsp/assets/alerts-panel.png "ícone do Painel de Pulso quando os alertas estiverem disponíveis") ou ![Ícone Pulse Panel quando nenhum alerta estiver disponível](/help/dsp/assets/alerts-panel-empty.png "Ícone Pulse Panel quando nenhum alerta estiver disponível").

>[!MORELIKETHIS]
>
>* [Tipos de Relatórios de Desempenho em Exibições de Gerenciamento de Campanha](campaign-reports-about.md)
