---
title: Configurações do modelo de alerta personalizado
description: Saiba mais sobre as configurações para modelos de alerta personalizados.
exl-id: 5ba98f48-c396-4b20-91dc-d45164097f9c
feature: Search Alerts
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Configurações do modelo de alerta personalizado

| Guia | Parâmetro | Descrição |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | O intervalo de datas para o qual avaliar as condições do alerta. As métricas são avaliadas de forma agregada ao longo do intervalo de datas. As opções variam de *[!UICONTROL Yesterday]* para *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | As condições para desencadear a indicação no momento especificado no [!UICONTROL Scheduling and Delivery] guia. As colunas disponíveis variam de acordo com o tipo de entidade (como campanha ou palavra-chave). Todos os filtros são unidos usando a função booleana AND, o que significa que todas as condições especificadas devem ser atendidas.<ul><li><p>Para adicionar um filtro, clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado de ![Adicionar](/help/search-social-commerce/assets/add.png "Adicionar") **[!UICONTROL ADD FILTER]**, e faça o seguinte:</p></li><ol><li><p>(Opcional) Para filtrar os nomes das colunas por sequência de texto, insira a sequência de pesquisa na **[!UICONTROL ADD FILTER]** campo de entrada.</p></li><li><p>Selecione um nome de coluna no menu de colunas.</p></li><li><p>Defina o filtro na coluna:</p></li><ul><li><p>(Filtros sem campos de entrada) Clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado do segundo menu e, em seguida, marque as caixas de seleção ao lado de cada valor a ser incluído.</p></li><li><p>(Colunas de métrica para as quais você deseja rastrear aumentos ou reduções no valor entre o intervalo de datas especificado e o período anterior) Para o operador, selecione *aumentos de* ou *diminui em* e, em seguida, insira o valor limite.</p><p>Por exemplo, se você selecionou a opção &quot;[!UICONTROL Cost]&quot;e deseja ser alertado quando o custo de qualquer campanha aumentar em 21%, depois selecione&quot;[!UICONTROL increases by]&quot; e digite 21 no campo de entrada. No [!UICONTROL Date Comparison Format] indique que você está interessado em uma alteração na porcentagem (em vez de uma alteração nas unidades monetárias).</p><p>Ao selecionar essa opção, duas colunas adicionais são adicionadas para cada coluna de dados regular. Por exemplo, em vez de incluir apenas uma coluna para &quot;Cliques&quot;, o relatório inclui colunas para &quot;Cliques R1&quot; (para Intervalo 1) &quot;Cliques R2&quot; (para Intervalo 2) e &quot;Cliques Diff&quot; ou &quot;Cliques Diff (%)&quot;, dependendo do especificado [!UICONTROL Date Comparison Format] (veja abaixo).</p><p>**Notas:**</p><ul><li><p>A coluna de diferença não é preenchida para métricas derivadas.<p></li><li><p>Este recurso não está disponível para colunas de métrica de conversão, ID ou classificação de etiqueta.</p></li><li><p>Relatórios que comparam intervalos de datas grandes podem levar mais tempo para serem gerados.</p></li></ul></ul><li><p>(Todos os outros filtros com campos de entrada) Selecione um operador no segundo menu e insira o valor aplicável.</p><p>Por exemplo, se você selecionou a coluna &quot;Cliques&quot; e deseja retornar apenas linhas com mais de 100 cliques, selecione &quot;maior que&quot; e insira 100 no campo de entrada.</p><p>Dependendo do tipo de dados, os operadores disponíveis podem incluir <i>maior que</i>, <i>menor que</i>, <i>igual a</i>, <i>contém</i>, <i>não contém</i>, <i>começa com</i>, <i>termina com</i>, <i>sem valor</i>, <i>tem valor</i>, <i>antes</i>, <i>após</i>ou <i>sem data</i>.</p><p>**Nota:** Os valores de texto não diferenciam maiúsculas de minúsculas. Por exemplo, se você filtrar por campanhas com &quot;loan&quot; no nome, os resultados poderão incluir &quot;Consumer Loans&quot; e &quot;loan applications&quot;.</p></li></ol><li><p>Para remover um filtro, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado da definição do filtro.</p></li></ul> |
|  | [!UICONTROL Comparing] | (Disponível quando o alerta rastreia aumentos ou reduções em uma ou mais colunas de métrica; somente leitura) Os dois intervalos de datas para os quais os dados são comparados. |
|  | [!UICONTROL Date Comparison Format] | (Disponível quando o alerta rastreia aumentos ou reduções em uma ou mais colunas de métrica) Como expressar a diferença entre dados nos dois intervalos de datas:<ul><li><p><i>[!UICONTROL Variance]</i> (o padrão) — Mostra a diferença como um valor numérico.</p></li><li><p><i>[!UICONTROL % Change]</i> — Mostra a diferença como uma porcentagem.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | O nome do alerta. Deve incluir pelo menos cinco caracteres. |
|  | [!UICONTROL Trigger this Alert] [quando] | Com que frequência o alerta verifica os filtros de condição especificados e, quando todas as condições são atendidas, envia notificações por email:<ul><li><p>[!UICONTROL Daily at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AM|PM]]</p></li></ul>**Nota:** Esse valor não afeta o período de avaliação. |
|  | [!UICONTROL Email Recipients] | (Editável somente pelo criador do modelo de alerta; somente leitura para todos os outros) Endereços de email nos quais enviar notificações quando um alerta for gerado. Por padrão, o endereço do criador do template é inserido.<br><br>Para adicionar um endereço, insira o endereço e clique em **[!UICONTROL Add]**. Para especificar vários endereços, separe-os com vírgulas ou espaços, ou adicione-os separadamente.<br><br>Quando o alerta inclui até 1000 registros, uma versão CSV do alerta é anexada à mensagem de email. |

>[!MORELIKETHIS]
>
>* [Sobre alertas personalizados](alert-about.md)
>* [Criar um modelo de alerta personalizado](alert-template-create.md)
>* [Editar um modelo de alerta personalizado](alert-template-edit.md)
>* [Pausar um modelo de alerta personalizado](alert-template-pause.md)
>* [Ativar um modelo de alerta personalizado](alert-template-activate.md)
>* [Excluir um modelo de alerta personalizado](alert-template-delete.md)
>* [Exibir alertas personalizados](alert-view.md)
>* [Exportar dados para alertas personalizados](alert-export-data.md)
