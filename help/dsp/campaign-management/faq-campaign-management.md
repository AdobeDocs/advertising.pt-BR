---
title: Perguntas frequentes sobre o Campaign Management
description: Saiba mais sobre o gerenciamento de campanhas, incluindo o período de latência das alterações e o que acontece quando você faz alterações de orçamento durante uma veiculação.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Perguntas frequentes sobre o Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latência das Alterações de Configuração

* Quando você altera uma configuração de posicionamento ou pacote, quando a alteração entrará em vigor?

  As alterações nas configurações geralmente têm efeito imediatamente, mas podem levar até 12 horas.

  Se for o último dia do delivery, faça alterações no início do dia, portanto, o DSP tem muito tempo para recalibrar o pacote com base nas alterações. Por exemplo, se você mudar de ritmo par para ritmo de carregamento prévio, o DSP precisa reavaliar como ele distribuirá os gastos pelo restante do voo. Não faça esse tipo de mudança se você só tiver uma hora para entregar no último dia do voo.

## Atualizações de orçamento no meio do voo

* Quando você faz uma alteração em uma disposição, quanto tempo o DSP leva para realocar o orçamento do pacote?

  A alocação de orçamento se baseia no desempenho de posicionamento, que é avaliado usando uma média de 14 dias. As alterações em um posicionamento resultam em alterações na alocação de orçamento somente quando causam alterações no desempenho durante a média de 14 dias.

  Quando ocorrem alterações de desempenho, o DSP realoca o orçamento do pacote entre os posicionamentos de acordo durante o próximo ciclo de otimização do orçamento, que ocorre por volta da meia-noite (00:00) no fuso horário da campanha.

* Como o orçamento é realocado quando um posicionamento é removido de um pacote e adicionado a outro pacote?

  Todo o histórico de gastos de uma disposição é anexado à disposição e se move com ela de pacote para pacote.

  Ao remover um posicionamento de um pacote, ele não terá mais nenhum histórico do gasto com o posicionamento. O orçamento do pacote se torna (orçamento do pacote - orçamento de posicionamento removido) / intervalo de tempo restante em andamento. O orçamento do pacote é então alocado para as disposições restantes no pacote.

  Da mesma forma, se você adicionar o mesmo posicionamento a um pacote diferente, o DSP considerará o histórico de gastos do posicionamento quando alocar orçamento para todos os posicionamentos no novo pacote.

* Como o ritmo do pacote muda no último dia de um voo?

  No último dia de um voo, o dia é encurtado de 24 horas para 23 horas para que o orçamento do pacote não seja excedido. Além disso, a estratégia de preenchimento de ritmo do pacote muda automaticamente para &quot;[!UICONTROL Frontload],&quot; mesmo que esteja definido como &quot;[!UICONTROL even].&quot; Isso significa que 65% do orçamento diário deve ser entregue até às 11h30 EST.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
