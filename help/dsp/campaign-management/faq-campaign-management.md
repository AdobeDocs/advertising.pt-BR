---
title: Perguntas frequentes sobre o gerenciamento de campanhas
description: Saiba mais sobre o gerenciamento de campanhas, incluindo o período de latência das alterações e o que acontece quando você faz alterações de orçamento durante uma veiculação.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Perguntas frequentes sobre o gerenciamento de campanhas

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latência das alterações de configuração

* Quando você altera uma configuração de posicionamento ou pacote, quando a alteração entra em vigor?

  As alterações nas configurações geralmente têm efeito imediatamente, mas podem levar até 12 horas.

  Se for o último dia do delivery, faça alterações no início do dia, para que o DSP tenha tempo de sobra para recalibrar o pacote com base nas alterações. Por exemplo, se você alterar o ritmo de evento para o ritmo de carregamento prévio, o DSP precisará reavaliar como distribuir os gastos durante o restante do voo. Não faça esse tipo de mudança se você só tiver uma hora para entregar no último dia do voo.

## Atualizações de orçamento no meio do voo

* Quando você faz uma alteração em uma disposição, quanto tempo o DSP leva para realocar o orçamento do pacote?

  A alocação de orçamento se baseia no desempenho de posicionamento, que é avaliado usando uma média de 14 dias. As alterações em um posicionamento resultam em alterações na alocação de orçamento somente quando causam alterações no desempenho durante a média de 14 dias.

  Quando ocorrem alterações de desempenho, o DSP realoca o orçamento do pacote entre os posicionamentos adequadamente durante o próximo ciclo de otimização de orçamento, que ocorre por volta da meia-noite (00:00) no fuso horário da campanha.

* Como o orçamento é realocado quando um posicionamento é removido de um pacote e adicionado a outro pacote?

  Todo o histórico de gastos de uma disposição é anexado à disposição e se move com ela de pacote para pacote.

  Ao remover um posicionamento de um pacote, ele não terá mais nenhum histórico do gasto com o posicionamento. O orçamento do pacote se torna (orçamento do pacote - orçamento de posicionamento removido) / intervalo de tempo restante em andamento. O orçamento do pacote é então alocado para as disposições restantes no pacote.

  Da mesma forma, se você adicionar o mesmo posicionamento a um pacote diferente, o DSP considerará o histórico de gastos do posicionamento quando alocar orçamento para todos os posicionamentos no novo pacote.

* Como o ritmo do pacote muda no último dia de um voo?

  No último dia de um voo, o dia é encurtado de 24 horas para 23 horas para que o orçamento do pacote não seja excedido. Além disso, a estratégia de preenchimento de ritmo do pacote muda automaticamente para &quot;[!UICONTROL Frontload]&quot;, mesmo que esteja definida como &quot;[!UICONTROL even]&quot;. Isso significa que 65% do orçamento diário deve ser entregue até às 11h00 EST.:30

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Práticas recomendadas para configurar campanhas de desempenho](/help/dsp/optimization/campaign-best-practices-performance.md)
