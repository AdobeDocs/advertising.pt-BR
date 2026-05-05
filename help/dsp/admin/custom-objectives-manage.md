---
title: Gerenciar objetivos personalizados
description: Saiba como definir os eventos de sucesso que ajudam a atingir as metas de otimização em nível de pacote.
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# Gerenciar objetivos personalizados

*Disponível para contas do DSP vinculadas às contas do Search, Social e Commerce*

Os objetivos definem os eventos bem-sucedidos que um anunciante define para atender aos seus objetivos de negócios. Os objetivos estão disponíveis para pacotes DSP como [metas personalizadas](/help/dsp/campaign-management/packages/package-settings.md). Cada pacote que usa a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve incluir uma meta personalizada para ajudar a alcançar a meta de otimização geral.

Um objetivo consiste nas métricas (propriedades) a serem rastreadas e otimizadas e nos pesos relativos dessas métricas. Cada objetivo pode incluir:

* **[!UICONTROL Goal]métricas**, que representam as métricas de sucesso principais de um anunciante. Normalmente, incluem resultados comerciais essenciais para um pacote, como Receita, Clientes potenciais ou Vendas. Cada objetivo deve ter pelo menos uma métrica de meta.

* **[!UICONTROL Assist]métricas** opcionais que auxiliam, preveem, precedem ou contribuem para a definição de métricas de meta. Os exemplos incluem métricas de engajamento, como Unidades de teste e Avaliações.

  Você pode permitir que o [!DNL Adobe AI] atribua e atualize automaticamente eventos de assistência ponderada para maximizar seus eventos de meta. Se você preferir atribuir suas próprias métricas de assistência ponderadas, o DSP pode, opcionalmente, recomendar métricas de assistência com base em dados de desempenho anteriores do Adobe Advertising e do Adobe Analytics. Você pode escolher se aplica ou não as recomendações.

Todas as alterações nas opções de objetivo são rastreadas no nível do campo e são listadas em um log de alterações.

>[!PREREQUISITES]
>
>Antes de criar objetivos, a conta do DSP deve ser vinculada a uma conta do Search, Social e Commerce com a mesma ID de organização da Adobe Experience Cloud, mesmo se você não for um cliente do Search, Social e Commerce. Se sua conta do DSP não estiver vinculada a uma conta do [!DNL Search, Social, & Commerce], entre em contato com a equipe de conta da Adobe.

>[!NOTE]
>
>* O Advertising Search, Social e Commerce também usa objetivos. Cada portfólio de Pesquisa, Social e Commerce deve ter um objetivo para que o recurso de otimização possa criar modelos de clique e receita para o portfólio.
>* Você pode usar o mesmo objetivo para vários pacotes do DSP e/ou vários portfólios do Search, Social e Commerce.

## Métricas disponíveis

Você pode incluir qualquer um dos seguintes itens em seus objetivos:

* Métricas que o Adobe Advertising rastreia usando o [pixel de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* (Anunciantes com [!DNL Adobe Analytics for Advertising]) [Métricas de conversão e envolvimento do site sincronizadas do Adobe Analytics](/help/integrations/analytics/overview.md).

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## Status do objetivo

A exibição [!UICONTROL Settings] > [!UICONTROL Custom Objectives] indica o status de cada objetivo. Os valores podem incluir:

* *[!UICONTROL Waiting]*: O objetivo estará em um estado de rascunho até que as recomendações sejam geradas.

* *[!UICONTROL Active]*: O objetivo é salvo e utilizável.

## Status da recomendação

* *[!UICONTROL Not Initiated]*: Nenhuma recomendação foi solicitada.

* *[!UICONTROL Generating]*: as recomendações estão sendo geradas.

* *[!UICONTROL Ready]*: as recomendações estão disponíveis para aplicação.

* *[!UICONTROL Error]*: Não foi possível gerar as recomendações.

## Criar um objetivo

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. No canto superior direito, clique em **[!UICONTROL Create]**.

1. Insira as [configurações de objetivo](#custom-objective-settings).

   Ao escolher a oferta automatizada, você pode atribuir propriedades (métricas) ao objetivo como &quot;[!UICONTROL Goal]&quot; métricas. Para lances personalizados, você pode atribuir propriedades como métricas &quot;[!UICONTROL Goal]&quot; ou &quot;[!UICONTROL Assist]&quot; ponderadas, mas deve incluir pelo menos uma métrica de meta.

   Os rótulos de meta e assistência não afetam a otimização. Somente os pesos das métricas incluídas afetam a otimização.

1. (Objetivos com lances personalizados; opcional) Para gerar as métricas de assistência recomendadas com base em dados de desempenho anteriores, clique em **[!UICONTROL Generate]** na seção inferior. No **[!UICONTROL Generate Recommendation]**, clique em **[!UICONTROL Generate]**.

   As métricas recomendadas levam até 20 minutos para serem geradas. Enquanto as recomendações estão sendo geradas, o status do objetivo personalizado é *[!UICONTROL Waiting]*. Depois que as recomendações forem geradas, você poderá &quot;[exibir e aplicar os eventos de assistência recomendados](#view-apply-recommendations).&quot;

1. (Se você não gerou recomendações) No canto superior direito, clique em **[!UICONTROL Save]**.

Nas [configurações de pacote do DSP](/help/dsp/campaign-management/packages/package-settings.md) para pacotes que usam a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, o nome do objetivo agora está incluído na lista [!UICONTROL Custom Goals]. Quando você seleciona o objetivo como meta personalizada para um pacote, a lista [!UICONTROL Conversion Metric] inclui todas as métricas de meta para o objetivo.

## Editar um objetivo

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Na linha, clique em **...*** > **[!UICONTROL Edit]**.

1. Altere qualquer uma das [configurações do objetivo](#custom-objective-settings).

1. (Quando as recomendações estiverem disponíveis; opcional) Exiba e, opcionalmente, aplique as métricas recomendadas:

   1. Na seção inferior, clique em **[!UICONTROL View Recommendations]**.

   1. Para aplicar uma recomendação, siga um destes procedimentos:

      * Clique em **[!UICONTROL Apply]** ao lado da recomendação.

      * Ajuste manualmente a recomendação e clique em **[!UICONTROL Apply]** ao lado dela.

   1. Clique em **[!UICONTROL Close]** para fechar a lista [!UICONTROL Recommendations].

   As alterações entram em vigor após a sincronização das configurações do objetivo.

1. (Objetivos com lances personalizados; opcional) Para gerar métricas de assistência recomendadas com base em dados de desempenho anteriores, clique em **[!UICONTROL Generate]** na seção inferior. No **[!UICONTROL Generate Recommendation]**, clique em **[!UICONTROL Generate]**.

   As métricas recomendadas levam até 20 minutos para serem geradas. Enquanto as recomendações estão sendo geradas, o status do objetivo personalizado é *[!UICONTROL Waiting]*. Depois que as recomendações forem geradas, você poderá &quot;[exibir e aplicar os eventos de assistência recomendados](#view-apply-recommendations).&quot;

1. (Se você não gerou novas recomendações) No canto superior direito, clique em **[!UICONTROL Save]**.

## Exibir e aplicar eventos de assistência recomendados {#view-apply-recommendations}

*Objetivos com lance personalizado*

Você pode exibir recomendações e, opcionalmente, aplicá-las quando o status do objetivo for *[!UICONTROL Active]* e o [!UICONTROL Recommendation Status] for *[!UICONTROL Ready]*.

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Na linha, clique em **...*** > **[!UICONTROL Edit]**.

1. Na seção inferior, clique em **[!UICONTROL View Recommendations]**.

1. (Opcional) Para aplicar uma recomendação, siga um destes procedimentos:

   * Clique em **[!UICONTROL Apply]** ao lado da recomendação.

   * Ajuste manualmente a recomendação e clique em **[!UICONTROL Apply]** ao lado dela.

1. Clique em **[!UICONTROL Close]** para fechar a lista [!UICONTROL Recommendations].

1. No canto superior direito, clique em **[!UICONTROL Save]**.

   As alterações entram em vigor após a sincronização das configurações do objetivo.

## Exibir o log de alterações para um objetivo personalizado

1. No menu principal, clique em **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Na linha, clique em **...*** > **[!UICONTROL Change Log]**.

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Configurações de objetivo personalizado {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Seção | Parâmetro | Descrição |
|---------|-----------|-------------|
| Detalhes básicos | AMOClient | A Adobe Advertising ID exclusiva do anunciante. |
| Detalhes básicos | Nome do objetivo | O nome do objetivo.<br><br>Todos os nomes de objetivos do Advertising DSP devem receber o prefixo &quot;ADSP_&quot; (não diferencia maiúsculas de minúsculas), como &quot;ADSP_Registrations&quot;. Use um nome fácil de identificar quando quiser atribuí-lo a um pacote. |
|  | Descrição | (Opcional) Uma descrição do objetivo. A descrição é exibida quando você mantém o cursor sobre o nome na lista de Objetivos personalizados. Se você não incluir uma descrição, o nome do objetivo será repetido. |
| Estratégia de lance |  | A estratégia de lance do objetivo, que determina os tipos de eventos que você pode configurar:<ul><li><b>[!UICONTROL Automated Bidding]:</b> Atribuir propriedades (métricas) ao objetivo como [!DNL goal] métricas. O [!DNL Adobe AI] atribui e atualiza automaticamente eventos de assistência ponderada para maximizar seus eventos de meta usando uma abordagem equilibrada do funnel.</li><li><b>[!UICONTROL Custom Bidding]:</b> Configure sua própria estratégia de lances atribuindo propriedades como eventos &quot;[!DNL goal]&quot; ou eventos &quot;[!DNL assist]&quot; ponderados. Use essa opção avançada para estratégias predefinidas.</li></ul>Alterar a estratégia de lances apaga todas as métricas selecionadas anteriormente. |
| Propriedades | [!UICONTROL Available Metrics] | Todas as métricas rastreadas para o anunciante. Para adicionar uma métrica como meta, clique em <b>[!UICONTROL Goal]</b> ao lado do nome da métrica. ([!UICONTROL Custom Bidding] somente) Para adicionar uma métrica que auxilie as métricas de meta atribuídas, clique em <b>[!UICONTROL Assist]</b> ao lado do nome da métrica.<br><br><b>Observações:</b> [!DNL Analytics] eventos personalizados seguem esta convenção de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid.` [!DNL Analytics] dimensões e segmentos não estão disponíveis para otimização do Adobe Advertising.<br><br><b>Dica:</b> Para obter o desempenho ideal, as métricas combinadas na meta personalizada (objetivo) devem totalizar pelo menos dez conversões por dia. Caso contrário, a prática recomendada é adicionar outras métricas de conversão de suporte, como páginas de produtos ou inícios de aplicativos, ao objetivo. Consulte [Práticas recomendadas para criar uma meta personalizada](#custom-goal-best-practices) para obter diretrizes. |
|  | Métricas selecionadas | O nome de cada métrica de conversão incluída no objetivo. Siga um destes procedimentos:<ul><li>Para adicionar uma métrica como meta, clique em <b>[!UICONTROL Goal]</b> ao lado do nome da métrica na coluna [!UICONTROL Available Metrics].</li><li>(Somente estratégia [!UICONTROL Custom Bidding]) Para adicionar uma métrica que auxilie as métricas de meta atribuídas, clique em <b>[!UICONTROL Assist]</b> ao lado do nome da métrica na coluna [!UICONTROL Available Metrics]. Em seguida, insira o peso numérico da métrica em relação a outras métricas no objetivo. O peso deve ser de 0,001 a 1 e pode incluir decimais. O peso padrão é 1.</li><li>(Somente estratégia [!UICONTROL Custom Bidding]) Para editar o peso de uma métrica de assistência, clique dentro do campo e insira o peso numérico da métrica em relação a outras métricas no objetivo. O peso deve ser maior que zero (0) e pode incluir decimais. O peso padrão é 1.</li><li>Para remover uma métrica do objetivo, mantenha o cursor sobre o nome da métrica e clique em **[!UICONTROL X]**./li></ul>**Notas:**<ul><li>Verifique se as diferentes métricas e seus pesos fazem sentido relativamente. Por exemplo, você não pode comparar diretamente uma contagem com um valor em dólar.</li><li>As grandes alterações relativas entre os pesos objetivos podem causar volatilidade temporária no desempenho, portanto, monitore o desempenho após a alteração.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md)
>* [Práticas recomendadas para metas personalizadas](/help/dsp/optimization/custom-goal.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Gerenciar conversões](/help/dsp/admin/conversion-metrics-manage.md)
