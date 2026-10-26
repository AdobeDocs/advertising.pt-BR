---
title: Sobre o assistente de IA no Advertising DSP
description: Saiba como usar o assistente de IA do DSP para solucionar problemas de pacotes e posicionamentos, criar relatórios e pesquisar ajuda sobre o uso do produto.
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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# Sobre o assistente de IA no Advertising DSP

O Assistente de IA no DSP é uma interface conversacional que permite executar qualquer fluxo de trabalho prático disponível no DSP a partir de uma única caixa de bate-papo. Você pode criar uma nova tarefa ou pedir ajuda para continuar uma tarefa anterior.

Seu histórico de conversa é mantido para todos os workflows, com cada conversa nomeada automaticamente. Suas consultas não são compartilhadas com outros usuários.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Fluxos de trabalho compatíveis

Os seguintes fluxos de trabalho podem ajudar você a realizar seu trabalho com mais eficiência:

<!-- And links to all sections/pages -->

| Recurso | Descrição | Exemplo de consultas | Respostas |
| --- | --- | --- | --- |
| [Solução de problemas](troubleshooting-agent.md) | Diagnosticar problemas de desempenho e entrega para um pacote ou posicionamento ativo selecionado.<ul><li>Posicionamentos somente: diagnosticar gastos excessivos, subutilizados e falhas de gastos. O agente avalia fatores relacionados de ritmo, lance, direcionamento e limite de orçamento.</li><li>Somente pacotes: faça o diagnóstico dos problemas de desempenho, incluindo CPA crescente ou ROAS decrescente. O agente não diagnostica métricas de envolvimento como CTR, CPC, cliques ou impressões.</li></ul>Cada conversa abrange um diagnóstico para um pacote ou posicionamento. Depois de receber um resultado, inicie uma nova conversa para diagnosticar outro problema, pacote ou posicionamento.<br><br>O agente não pode alterar as configurações nem criar ou editar campanhas ou componentes da campanha. Ele também não pode diagnosticar pacotes ou posicionamentos pausados, concluídos, arquivados ou programados. | Problemas de gastos com posicionamento:<ul><li>Minha colocação parou de gastar ontem, mesmo que o negócio esteja ativo. Por quê?</li><li>Por que essa colocação tem sido subutilizada nos últimos 5 dias?</li><li>Estamos na metade do voo e significativamente atrasados no ritmo. Por quê?</li></ul>Problemas de desempenho do pacote:<ul><li>Por que o CPA aumentou para este pacote na última semana?</li><li>Por que o ROAS está se recusando para este pacote?</li></ul> | A resposta inclui fatores que limitam o desempenho e fornece recomendações para resolver os problemas. |
| [Insights](insights-agent.md) | Obtenha métricas de campanha e relatórios completos sem criar um relatório manualmente. Faça perguntas simples sobre uma métrica específica, como gasto ou CPA de uma campanha, ou peça um relatório mais complexo para uma dimensão específica (como uma única campanha, posicionamento ou público-alvo) ou entre dimensões (para detalhamentos por campanha e anunciante). Você pode baixar os resultados como um arquivo CSV. | <ul><li>Quanto [Nome da Campanha] gastou na semana passada?<li>Quantas conversões [Nome da Campanha] recebeu este mês?</li><li>Quais posicionamentos estão atrasados em mais de 20%?</li></li>Mostre-me o CPA por pacote para [Nome da Campanha]</li></ul> | As primeiras linhas do relatório são exibidas com links para visualizar o relatório completo e baixar o relatório como um arquivo de [!DNL Microsoft Excel] valores separados por vírgula (.csv). |
| [Pesquisa na documentação do produto](documentation-search.md) | Pesquise conteúdo conceitual e de instruções no [Guia do Advertising DSP](/help/dsp/home.md) e, para anunciantes com o Advertising Creative, no [Guia do Advertising Creative](/help/creative/home.md). As respostas são baseadas apenas no que está documentado para esses produtos no [Experience League](https://experienceleague.adobe.com/en/docs/advertising).<br><br>Pergunte sobre gerenciamento de campanhas, otimização, gerenciamento de público-alvo, ofertas, relatórios e outros recursos do produto. | <ul><li>Como anexar um anúncio a uma disposição?</li><li>Quais opções de direcionamento estão disponíveis no Adobe DSP?</li><li>Quais são as consequências do uso de diferentes opções de ritmo nas configurações de posicionamento?</li><li>Quais relatórios incluem dados domésticos?</li><li>Como criar uma tag de anúncio para uma experiência de [!DNL Creative]?</li></ul> | A resposta inclui citações embutidas e uma lista [!UICONTROL Documentation Sources] expansível na parte inferior. Clique em qualquer citação ou listagem de origem para abrir a página relevante.<br><br>A resposta também pode incluir perguntas de acompanhamento e sugestões para ajudá-lo a refinar sua consulta e encontrar mais informações. |

## Abrir o assistente do AI {#ai-assistant-open}

* Na parte superior direita de qualquer página, clique em ![Chat de agente](/help/dsp/assets/agent-chat.png "Chat de agente").

## Expandir a chatbox

1. Na parte superior da [caixa de chat](#ai-assistant-open), clique em ![Entrar na tela cheia](/help/dsp/assets/fullscreen.png "Entrar na tela cheia") para entrar no modo de tela cheia.

1. Para retornar a caixa de chat ao modo de painel, clique em **[!UICONTROL < Back>]**.

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## Práticas recomendadas para gravar consultas e prompts {#writing-queries}

* **Seja claro e específico**. Use perguntas completas (&quot;Como eu me inscrevo no inventário sob demanda?&quot;), frases de tarefas (&quot;Inscrever-se no inventário sob demanda&quot;) ou frases de tópicos (&quot;Inventário sob demanda&quot;).

* **Não combine diferentes tipos de solicitações na mesma consulta**, a menos que deseje que elas sejam armazenadas na mesma conversa.

* **Inclua intervalos de datas quando relevante** para restringir os dados desejados.

* **Corresponder termos da interface** quando possível para recursos do produto (como &quot;campanhas&quot; ou &quot;ofertas&quot;).

  Para ações comuns (como &quot;adicionar&quot;, &quot;anexar&quot; ou &quot;atribuir&quot;), é possível usar sinônimos.

* **Adicionar detalhes** para restringir ou ampliar resultados. Refine com perguntas de acompanhamento, conforme necessário.

* **Não se preocupe com pontuação e maiúsculas**, exceto quando afetarem o significado.

>[!MORELIKETHIS]
>
>* [Criar relatórios usando o assistente de IA](insights-agent.md)
>* [Solucionar problemas de desempenho e entrega usando o assistente de IA](troubleshooting-agent.md)
>* [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md)
>* [Procure a documentação do produto usando o Assistente de IA](documentation-search.md)
>* [Trabalhar com conversas anteriores do Assistente de IA](previous-conversations.md)
