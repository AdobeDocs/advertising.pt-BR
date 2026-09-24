---
title: Solucionar problemas de desempenho e de delivery usando o assistente de IA
description: Saiba como usar o agente de solução de problemas do assistente de IA para diagnosticar problemas de gastos, ritmo e entrega de pacotes e posicionamentos do DSP.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 2e97652901e16bd1079fac445f9a2a4794dcda56
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# Solucionar problemas de desempenho e de delivery usando o assistente de IA do DSP

O agente de solução de problemas do assistente de IA pode identificar fatores que limitam o desempenho e fornece recomendações para resolver problemas. O agente de solução de problemas pode:

* Ajuda para diagnosticar problemas de desempenho e entrega de um pacote ou posicionamento ativo selecionado:

  * (Somente disposições) Problemas de gastos, incluindo gasto excessivo, subutilização e falha de gasto. O agente avalia fatores relacionados de ritmo, lance, direcionamento e limite de orçamento como parte do diagnóstico.

  * (Somente pacotes) Problemas de desempenho, incluindo um CPA crescente ou um ROAS decrescente. O agente não diagnostica métricas de envolvimento como CTR, CPC, cliques ou impressões.

  Cada conversa abrange um único diagnóstico para um único pacote ou posicionamento. Depois que o agente fornecer um resultado, inicie uma nova conversa para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente.

  O agente não pode alterar configurações nem criar ou editar campanhas ou componentes de campanha. Ele também não pode diagnosticar problemas de um pacote ou posicionamento pausado, concluído, arquivado ou programado.

* Pesquise conteúdo conceitual e de instruções no [Guia do Advertising DSP](/help/dsp/home.md) e (anunciantes com o Advertising Creative) no [Guia do Advertising Creative](/help/creative/home.md), da mesma forma que na [interface de Chat do Agentic](/help/dsp/agent-chat.md). Você pode fazer perguntas sobre gerenciamento de campanha, otimização, gerenciamento de público-alvo, ofertas, relatórios e outros recursos do produto.

>[!IMPORTANT]
>
>As respostas geradas por IA podem ser imprecisas ou enganosas. Sempre verifique as respostas e origens antes de usá-las para decisões que afetam o custo ou o esforço.

## Exemplo de consultas

>[!NOTE]
>
>Não é necessário especificar um intervalo de datas. Se você não incluir um, o agente selecionará um padrão razoável com base no tipo de problema.

### Posicionamentos: problemas de gastos

* Minha colocação parou de gastar ontem, mesmo que o negócio esteja ativo. Por quê?

* Por que essa colocação tem sido subutilizada nos últimos 5 dias?

* Estamos na metade do voo e significativamente atrasados no ritmo. Por quê?

### Pacotes: problemas de desempenho

* Por que o CPA aumentou para este pacote na última semana?

* Por que o ROAS está se recusando para este pacote?

>[!TIP]
>
>Se você tiver um CPA de destino em mente, inclua-o em sua consulta (por exemplo, &quot;diagnosticar CPA em relação a um CPA de US$ 50&quot;). Se você não especificar um, o agente usará um target padrão.

### Recursos do produto:

* Como criar uma inserção?

* Quais opções de direcionamento estão disponíveis no Adobe DSP?

* Como anexar um anúncio a uma disposição?

* Quais são as consequências do uso de diferentes opções de ritmo nas configurações de posicionamento?

* Quando devo usar cada tipo de meta de otimização?

* Por que os posicionamentos programáticos garantidos (PG) não servem impressões?

* Quais relatórios incluem dados domésticos?

* Qual é a diferença entre uma experiência direcionada e uma experiência não direcionada no [!DNL Creative]?

* Como criar uma tag de anúncio para uma experiência de [!DNL Creative]?

## Enviar uma consulta para um pacote ou posicionamento ativo

Você pode fazer várias perguntas em uma mensagem, mas somente uma mensagem por vez. Aguarde uma resposta antes de enviar outra.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. Siga um destes procedimentos:

   * (Para pacotes) Na exibição [!UICONTROL Packages], clique em **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** ao lado do nome do pacote.

   * (Para inserções) No submenu, clique em **[!UICONTROL Placements]**. Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Insira sua consulta e clique em ![Enviar prompt](/help/dsp/assets/submit-prompt.png "Enviar prompt").

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   Para consultas de desempenho e delivery, a resposta inclui fatores que limitam o desempenho e fornece recomendações para resolver os problemas.

   Para consultas de documentação, a resposta inclui citações em linha e uma lista **[!UICONTROL Documentation Sources]** na parte inferior. Perguntas e sugestões de acompanhamento também podem aparecer.

1. (Somente consultas de documentação; opcional) Para abrir uma página usada como fonte de dados, siga um destes procedimentos:

   * Clique na citação numerada.

   * Clique em **[!UICONTROL Documentation Sources]** para mostrar uma lista de todas as páginas citadas na resposta e, em seguida, clique no link da página.

1. (Opcional) Classifique a resposta usando o ícone de miniatura ou miniatura.

>[!TIP]
>
>Para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente, inicie uma nova conversa.
