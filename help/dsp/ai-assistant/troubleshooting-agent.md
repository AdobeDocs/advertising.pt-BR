---
title: Solucionar problemas de desempenho e de delivery usando o assistente de IA
description: Use o agente de solução de problemas do Assistente do Adobe Advertising DSP AI para diagnosticar problemas de gastos, ritmo e entrega de pacotes e posicionamentos do DSP.
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
source-git-commit: 41d3ab985831a1432e775277384661643a9f55c4
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%
---
# Solucionar problemas de desempenho e delivery usando o Assistente de IA


*recurso do Beta*

O agente de solução de problemas do Assistente de IA identifica fatores que limitam o desempenho de pacotes e posicionamentos ativos e fornece instruções passo a passo e recomendações com base em dados históricos para resolver problemas. O agente de solução de problemas pode ajudar a diagnosticar os seguintes tipos de problemas de desempenho e de delivery:

* (Somente disposições) Problemas de gastos, incluindo gasto excessivo, subutilização e falha de gasto. O agente avalia fatores relacionados de ritmo, lance, direcionamento e limite de orçamento como parte do diagnóstico.

* (Somente pacotes) Problemas de desempenho, incluindo aumento do CPA ou queda do ROAS. O agente não diagnostica métricas de envolvimento como CTR, CPC, cliques ou impressões.

Cada conversa abrange um único diagnóstico para um único pacote ou posicionamento. Depois que o agente fornecer um resultado, inicie uma nova conversa para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente.

O agente não pode alterar configurações, criar ou editar campanhas ou componentes de campanha, nem diagnosticar problemas de um pacote ou posicionamento pausado, concluído, arquivado ou agendado.

>[!IMPORTANT]
>
>As respostas geradas por IA podem ser imprecisas ou enganosas. Sempre verifique as respostas e origens antes de usá-las para decisões que afetam o custo ou o esforço.

## Exemplo de consultas

### Resolução de problemas de despesas de posicionamento

* Minha colocação parou de gastar ontem, mesmo que o negócio esteja ativo. Por quê?

* Por que essa colocação tem sido subutilizada nos últimos 5 dias?

* Estamos na metade do voo e significativamente atrasados no ritmo. Por quê?

### Solução de problemas de desempenho de pacotes

* Por que o CPA aumentou para este pacote na última semana?

* Por que o ROAS está se recusando para este pacote?

## Enviar uma consulta do Assistente de IA

Você pode fazer várias perguntas em uma mensagem, mas somente uma mensagem por vez. Aguarde uma resposta antes de enviar outra.

1. Na parte superior direita de qualquer página, clique em ![Chat de agente](/help/dsp/assets/agent-chat.png "Chat de agente").

1. Crie a consulta:

   * Insira sua própria consulta.

   * Para ver exemplos de consultas, clique em **[!UICONTROL Troubleshoot]** para expandir a seção.

     1. (Opcional) Para copiar o texto de uma consulta de exemplo no campo de entrada:

        1. Clique no exemplo.

        1. (Opcional) Edite o texto de acordo com suas necessidades.

   Para obter mais informações sobre consultas, consulte &quot;[Práticas recomendadas para gravar consultas e prompts](ai-assistant-about.md#writing-queries).&quot;

   >[!NOTE]
   >
   >* Se você não especificar um intervalo de datas, o agente selecionará um padrão razoável com base no tipo de problema. Por exemplo, se você perguntar sobre métricas de campanha sem especificar um intervalo de datas, os resultados serão para a duração da campanha.
   >* Se você tiver um CPA de destino em mente, inclua-o em sua consulta (por exemplo, &quot;diagnosticar CPA em relação a um CPA de US$ 50&quot;). Se você não especificar um, o agente usará um target padrão.

1. Clique em ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") ou pressione a tecla **Enter** no teclado.

1. Se o Assistente de IA solicitar informações adicionais, forneça-as.

>[!TIP]
>
>Para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente, [inicie uma nova conversa](#conversation-new).

## Enviar uma consulta da exibição [!UICONTROL Packages] ou [!UICONTROL Placements]

Você pode fazer várias perguntas em uma mensagem, mas somente uma mensagem por vez. Aguarde uma resposta antes de enviar outra.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. Siga um destes procedimentos:

   * (Para pacotes) Na exibição [!UICONTROL Packages], clique em **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** ao lado do nome do pacote.

   * (Para inserções) No submenu, clique em **[!UICONTROL Placements]**. Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Crie a consulta:

   * Insira sua própria consulta.

   * Para ver exemplos de consultas, clique em **[!UICONTROL Troubleshoot]** para expandir a seção.

     1. (Opcional) Para copiar o texto de uma consulta de exemplo no campo de entrada:

        1. Clique no exemplo.

        1. (Opcional) Edite o texto de acordo com suas necessidades.

   Para obter mais informações sobre consultas, consulte &quot;[Práticas recomendadas para gravar consultas e prompts](ai-assistant-about.md#writing-queries).&quot;

   >[!NOTE]
   >
   >* Se você não especificar um intervalo de datas, o agente selecionará um padrão razoável com base no tipo de problema. Por exemplo, se você perguntar sobre métricas de campanha sem especificar um intervalo de datas, os resultados serão para a duração da campanha.
   >* Se você tiver um CPA de destino em mente, inclua-o em sua consulta (por exemplo, &quot;diagnosticar CPA em relação a um CPA de US$ 50&quot;). Se você não especificar um, o agente usará um target padrão.

1. Clique em ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") ou pressione a tecla **Enter** no teclado.

1. Se o Assistente de IA solicitar informações adicionais, forneça-as.

>[!TIP]
>
>Para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente, [inicie uma nova conversa](#conversation-new).

## Iniciar uma nova conversa {#conversation-new}

Cada conversa (ou thread de consulta) é salva separadamente para que você possa distinguir suas conversas anteriores.

1. Na parte superior da [caixa de chat](#ai-assistant-open), clique em ![Iniciar uma nova conversa](/help/dsp/assets/new-selection.png "Iniciar uma nova conversa").

1. [Enviar uma consulta](#query-submit).

## Expandir e minimizar a chatbox

1. Na parte superior da [caixa de chat](#ai-assistant-open), clique em ![Entrar na tela cheia](/help/dsp/assets/fullscreen.png "Entrar na tela cheia") para entrar no modo de tela cheia.

1. Para retornar a caixa de chat ao modo de painel, clique em **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Sobre o Assistente de IA no Advertising DSP](ai-assistant-about.md)
>* [Trabalhar com conversas anteriores do Assistente de IA](previous-conversations.md)
