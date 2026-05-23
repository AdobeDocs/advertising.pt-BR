---
title: (Nova interface) Gerenciar alertas personalizados
description: Saiba como criar, configurar, pausar, ativar, excluir, exibir e exportar alertas e modelos de alerta personalizados.
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# (Nova interface) Gerenciar alertas personalizados

Crie modelos de alerta para identificar quando qualquer portfólio, campanha ou grupo de anúncios atende a condições específicas, como uma métrica de desempenho, durante um período especificado e gerar um alerta. Os alertas estão disponíveis para um único anunciante. Os alertas incluem todas as colunas na visualização padrão relevante. Por exemplo, alertas no nível da campanha incluem todas as colunas na exibição padrão [!UICONTROL Campaigns].

Você pode criar modelos de alerta na guia [!UICONTROL Alert Templates] do painel [!UICONTROL Custom Alerts] ou na parte superior de qualquer página.

Quando uma instância de alerta é acionada para um modelo de alerta:

* Os recipients especificados recebem um aviso por email. Quando o alerta contém até 1000 registros, o aviso de email inclui um arquivo [CSV](/help/search-social-commerce/glossary.md#c-d) com os dados de alerta, incluindo dados para todas as entidades que acionaram o alerta.

* O alerta está listado na guia [!UICONTROL Triggered Alerts] do painel [!UICONTROL Custom Alert Templates].<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## A visualização [!UICONTROL Custom Alerts]

Para abrir o painel [!UICONTROL Custom Alerts], clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") no canto superior direito.

O painel [!UICONTROL Custom Alerts] inclui a exibição [!UICONTROL Alert Templates], que lista todos os modelos de alerta criados para a conta e a partir da qual você pode criar, editar, pausar, reativar e excluir modelos de alerta. A exibição [!UICONTROL Triggered Alerts] lista as instâncias de alerta geradas.

## Ações disponíveis

* [Exibir alertas disparados](#alert-view)

* [Exibir modelos de alerta personalizados](#alert-template-view)

* [Criar um modelo de alerta personalizado](#alert-template-create)

* [Editar um modelo de alerta personalizado](#alert-template-edit)

* [Pausar um modelo de alerta personalizado](#alert-template-pause)

* [Ativar um modelo de alerta personalizado](#alert-template-activate)

* [Excluir um modelo de alerta personalizado](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## Exibir alertas disparados {#alert-view}

1. Na parte superior direita de qualquer página, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado").

1. Clique na guia **[!UICONTROL Triggered Alerts]**.

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

## Exibir modelos de alerta personalizados {#alert-template-view}

1. No canto superior direito de qualquer página, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado"), que será aberto na guia [!UICONTROL Alert Templates].

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

1. (Opcional) Para exibir todos os critérios de um modelo de alerta, clique no número de critérios (como ![Botão de exemplos de critérios de alerta personalizados](/help/search-social-commerce/assets/custom-alert-criteria.png "Botão de exemplos de critérios de alerta personalizados").

## Criar um modelo de alerta personalizado {#alert-template-create}

Novos modelos de alerta têm o status &quot;[!UICONTROL Active]&quot;.

1. Siga um destes procedimentos:

   * Na parte superior direita de qualquer página, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL Create Custom Alert]**.

   Na parte superior direita de qualquer página, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL View Custom Alerts]**, que abrirá a guia [!UICONTROL Alert Templates]. Clique em **[!UICONTROL Create Alert]**.

1. Especifique as [configurações de alerta](#alert-template-settings) nas guias **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** e **[!UICONTROL Scheduling and Delivery]**.

   Você pode se mover entre guias clicando no nome da guia (como &quot;Filtros&quot;) ou clicando em **[!UICONTROL Next]** no canto inferior direito.

1. Na guia [!UICONTROL Summary], clique em **[!UICONTROL Create Alert]**.

## Editar um modelo de alerta personalizado {#alert-template-edit}

1. No canto superior direito, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL View Custom Alerts]**, que será aberto na guia [!UICONTROL Alert Templates].

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

1. Ao lado do nome do modelo, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Na janela [!UICONTROL Edit Custom Alert], edite as [configurações de alerta](#alert-template-settings) nas guias **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** e **[!UICONTROL Scheduling and Delivery]**.

   Você pode se mover entre guias clicando no nome da guia (como &quot;Filtros&quot;) ou clicando em **[!UICONTROL Next]** no canto inferior direito.

1. Na guia [!UICONTROL Summary], clique em **[!UICONTROL Update Alert]**.

## Pausar um modelo de alerta personalizado {#alert-template-pause}

1. No canto superior direito, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL View Custom Alerts]**, que será aberto na guia [!UICONTROL Alert Templates].

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

1. Na linha de modelo, selecione *[!UICONTROL Paused]*.

## Ativar um modelo de alerta personalizado {#alert-template-activate}

1. No canto superior direito, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL View Custom Alerts]**, que será aberto na guia [!UICONTROL Alert Templates].

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

1. Na linha de modelo, selecione *[!UICONTROL Active]*.

## Excluir um modelo de alerta personalizado {#alert-template-delete}

Você pode excluir somente os modelos de alerta criados.

1. No canto superior direito, clique em ![Alerta personalizado](/help/search-social-commerce/assets/custom-alert.png "Alerta personalizado") > **[!UICONTROL View Custom Alerts]**, que será aberto na guia [!UICONTROL Alert Templates].

1. (Opcional) Filtre a lista para incluir alertas para um tipo de entidade específico ou procure uma string de texto no nome do modelo. As consultas de pesquisa não diferenciam maiúsculas de minúsculas.

1. Na linha de modelo, clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir").

1. Na caixa de mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Configurações do modelo de alerta personalizado {#alert-template-settings}

| Guia | Parâmetro | Descrição |
|--- |--- |--- |
|  | [!UICONTROL Name] | O nome do alerta. Deve incluir pelo menos cinco caracteres. |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | O tipo de entidade a ser avaliado: <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i> ou <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | O intervalo de datas para o qual avaliar as condições do alerta. As métricas são avaliadas de forma agregada ao longo do intervalo de datas. As opções variam de *[!UICONTROL Yesterday]* a *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Filtros definidos\] | As condições para acionar o alerta no horário especificado na guia [!UICONTROL Scheduling and Delivery]. As colunas disponíveis variam de acordo com o tipo de entidade. Todos os filtros são unidos usando a função booleana AND, o que significa que todas as condições especificadas devem ser atendidas.<ul><li><p>Para adicionar um filtro, faça o seguinte:<p><ol><li><p>(Opcional) Para filtrar os nomes de coluna por cadeia de texto, insira a cadeia de caracteres de pesquisa no campo de entrada [!UICONTROL ADD FILTER].</p></li><li><p>Na lista de colunas, selecione um nome de coluna.</p></li><li><p>Defina o filtro na coluna:</p></li><ul><li><p>(Filtros sem campos de entrada) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado do segundo menu e marque as caixas de seleção ao lado de cada valor a ser incluído.</p></li><li><p>(Todos os outros filtros com campos de entrada) Selecione um operador no segundo menu e insira o valor aplicável.</p><p>Por exemplo, se você selecionou a coluna &quot;Cliques&quot; e deseja retornar apenas linhas com mais de 100 cliques, selecione &quot;maior que&quot; e insira 100 no campo de entrada.</p><p>Dependendo do tipo de dados, os operadores disponíveis podem incluir <i>maior que</i>, <i>menor que</i>, <i>igual</i>, <i>contém</i>, <i>não contém</i>, <i>começa com</i>, <i>termina com</i>, <i>nenhum valor</i>, <i>tem valor</i>, <i>antes</i>, <i>depois de</i> ou <i>não data</i>.</p><p>**Observação:** os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você filtrar por campanhas com &quot;loan&quot; no nome, os resultados poderão incluir &quot;Consumer Loans&quot; e &quot;loan applications&quot;.</p></li></ol><li><p>Para remover um filtro, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da definição de filtro.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[quando\] | Com que frequência o alerta verifica os filtros de condição especificados e, quando todas as condições são atendidas, envia notificações por email:<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Dia da Semana*> às &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Dia NN*> em &lt;*NN*> `[AM\|PM]`]</p></li></ul>**Observação:** esse valor não afeta o período de avaliação. |
|  | [!UICONTROL Email Recipients] | (Editável somente pelo criador do modelo de alerta; somente leitura para todos os outros) Usuários registrados de pesquisa, social e Commerce para os quais enviar notificações quando um alerta for acionado. Por padrão, o nome da sua conta de usuário é selecionado. Opcionalmente, adicione ou remova usuários com acesso aos dados do anunciante.<br><br>Quando o alerta inclui até 1000 registros, uma versão CSV do alerta é anexada à mensagem de email. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
