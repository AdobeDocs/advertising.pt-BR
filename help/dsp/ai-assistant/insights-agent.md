---
title: Criar relatórios usando o assistente de IA
description: Saiba como usar o agente de insights do assistente do Adobe Advertising DSP AI para consultar métricas de campanha, gerar relatórios e baixar arquivos CSV.
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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%
---
# Criar relatórios usando o assistente de IA

*recurso do Beta*

Use o agente de insights do Assistente de IA para obter métricas e relatórios completos para suas campanhas, componentes de campanha, experiências do Advertising Creative, anunciantes e públicos-alvo de anúncios, sem criar um relatório manualmente. Faça perguntas simples sobre uma métrica específica, como gasto ou CPA de uma campanha, ou peça um relatório mais complexo para uma dimensão específica (como uma única campanha ou público-alvo) ou entre dimensões (para detalhamentos de cada campanha e anunciante). Você pode baixar os resultados como um arquivo CSV.

>[!IMPORTANT]
>
>As respostas geradas por IA podem ser imprecisas ou enganosas. Sempre verifique as respostas e origens antes de usá-las para decisões que afetam o custo ou o esforço.

## Exemplo de consultas

* Quanto [Nome da Campanha] gastou na semana passada?

* Quantas conversões [Nome da Campanha] recebeu este mês?

* Mostre-me o CPA por pacote para [Nome da Campanha].

* Quais posicionamentos estão atrasados em mais de 20%?

* Compare o gasto líquido de todas as campanhas e pacotes nos últimos 15 dias.

## Enviar uma consulta

Você pode fazer várias perguntas em uma mensagem, mas somente uma mensagem por vez. Aguarde uma resposta antes de enviar outra.

1. Na parte superior direita de qualquer página, clique em ![Chat de agente](/help/dsp/assets/agent-chat.png "Chat de agente").

1. Crie a consulta:

   1. Siga um destes procedimentos:

      * Insira sua própria consulta.

      * Para ver exemplos de consultas:

        1. Clique em **[!UICONTROL Insights]** para expandir a seção.

        1. (Opcional) Para copiar o texto de uma consulta de exemplo no campo de entrada:

           1. Clique no exemplo.

           1. (Opcional) Edite o texto de acordo com suas necessidades.

   1. (Opcional) Para focalizar sua consulta em um valor de dimensão específico (como uma campanha específica), opcionalmente insira o cursor onde deseja que o valor de dimensão apareça, clique em ![Mencionar uma entidade](/help/dsp/assets/prompt-entity.png "Mencionar uma entidade"), selecione a dimensão e selecione o valor de dimensão.

      Por exemplo, para a dimensão [!UICONTROL Campaign], você pode selecionar em uma lista de todas as suas campanhas para relatar.

      As dimensões disponíveis incluem:

      * Entidades de campanha: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * O anunciante: [!UICONTROL Advertiser]
      * Entidades Advertising Creative: [!UICONTROL Experience]
      * Destinos de anúncios: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   Para obter mais informações sobre consultas, consulte &quot;[Práticas recomendadas para gravar consultas e prompts](ai-assistant-about.md#writing-queries).&quot;

1. Clique em ![Enviar consulta](/help/dsp/assets/submit-prompt.png "Enviar consulta") ou pressione a tecla **Enter** no teclado. Se o agente solicitar informações adicionais, forneça as informações necessárias.

   As primeiras linhas do relatório são exibidas, com links para visualizar o relatório completo e baixar o relatório.

   Algumas linhas do relatório gerado são mostradas.

>[!TIP]
>
>Para perguntar sobre um problema diferente ou sobre um pacote ou posicionamento diferente, [inicie uma nova conversa](#conversation-new).

## Baixar ou visualizar um relatório completo da caixa de chat

* Para baixar uma cópia do relatório completo, clique em ![Export](/help/dsp/assets/download.png "Export").

  O arquivo é baixado como um [!DNL Microsoft Excel] arquivo de valores separados por vírgula (.csv) de acordo com o procedimento normal do navegador. O nome do arquivo é &quot;DSP_Insights_Report_&lt;job_number>&quot;.

* Para visualizar o relatório completo em um painel lateral, clique em ![Visualizar](/help/dsp/assets/agent-chat-preview.png "Visualizar"). Para baixar o relatório da visualização, clique em ![Exportar](/help/dsp/assets/download.png "Exportar").

  Se você baixar o relatório, ele será baixado como um [!DNL Microsoft Excel] arquivo de valores separados por vírgula (.csv) de acordo com o procedimento normal do seu navegador. O nome do arquivo é &quot;DSP_Insights_Report_&lt;job_number>&quot;.

## Iniciar uma nova conversa {#conversation-new}

Cada conversa, ou thread de consulta, é salva separadamente para que você possa distinguir suas conversas anteriores.

1. Na parte superior da [caixa de chat](#ai-assistant-open), clique em ![Iniciar uma nova conversa](/help/dsp/assets/new-selection.png "Iniciar uma nova conversa").

1. [Enviar uma consulta](#query-submit).

## Expandir e minimizar a chatbox

1. Na parte superior da [caixa de chat](#ai-assistant-open), clique em ![Entrar na tela cheia](/help/dsp/assets/fullscreen.png "Entrar na tela cheia") para entrar no modo de tela cheia.

1. Para retornar a caixa de chat ao modo de painel, clique em **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Sobre o Assistente de IA no Advertising DSP](ai-assistant-about.md)
>* [Trabalhar com conversas anteriores do Assistente de IA](previous-conversations.md)
