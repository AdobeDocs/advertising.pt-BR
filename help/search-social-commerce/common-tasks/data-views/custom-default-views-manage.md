---
title: Gerenciar exibições padrão e personalizadas
description: Saiba como personalizar exibições padrão e personalizadas.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '2842'
ht-degree: 0%

---

# Gerenciar exibições padrão e personalizadas

Suas visualizações padrão e personalizadas permitem personalizar os dados de desempenho exibidos nas visualizações de dados da campanha de pesquisa. As configurações de exibição incluem as colunas a serem incluídas, os filtros, o intervalo de datas, as configurações de atribuição de conversão e outras configurações avançadas — e você pode aplicar as configurações temporariamente ou salvá-las. (Exceção: não é possível salvar filtros para exibições padrão.) Cada exibição personalizada padrão e regular é aplicável para uma exibição de entidade específica (como [!UICONTROL Campaigns]) e somente uma conta específica de anunciante. Cada exibição personalizada universal é aplicável em exibições de entidade para um anunciante específico e, portanto, não pode incluir colunas de propriedade (como nome da entidade ou status), que variam de acordo com o tipo de entidade.

As exibições padrão são exibidas por padrão sempre que você faz logon. É possível criar exibições personalizadas adicionais e aplicá-las a qualquer momento. Como opção, é possível compartilhar qualquer visualização personalizada criada com todos os outros usuários que podem visualizar os dados do anunciante. Nas listas de exibição, cada exibição compartilhada por outra pessoa é em itálico, como &quot;*Campanhas com melhor desempenho*.&quot; Somente a pessoa que cria uma exibição personalizada pode excluí-la.

Cada exibição está disponível como atalho no [!UICONTROL Custom Views] seção do painel esquerdo.

## Aplicar um modo de exibição padrão ou personalizado

* (Exibições padrão) No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]** \> **\[tipo de entidade\]**.

* (Exibições personalizadas) No painel de navegação esquerdo:

   1. No painel esquerdo, clique na guia **[!UICONTROL Custom Views]** para expandi-la.

      As exibições são classificadas por entidade aplicável.

   1. Expanda os menus disponíveis.

      &quot;[!UICONTROL Universal Views]&quot; inclui exibições personalizadas que podem ser usadas em todas as exibições de entidade. Todas as outras exibições personalizadas são agrupadas por tipo de entidade.

   1. Clique no nome da exibição.

      Se a exibição for universal ou se aplicar à entidade atual, a tabela de dados será exibida novamente de acordo com a configuração de exibição. Se a exibição se aplicar a uma entidade diferente, os dados da entidade aplicável serão exibidos de acordo com a configuração de exibição.

## Criar um modo de exibição personalizado {#create-custom-view}

As exibições personalizadas se aplicam somente às exibições de gerenciamento de campanha.

>[!NOTE]
>
>Além das configurações de exibição especificadas para a exibição personalizada, a ordem de classificação da coluna atual também é salva.

1. No lado direito da barra de ferramentas acima da tabela de dados, clique no nome da exibição atual (que pode ser &quot;[!UICONTROL Default]&quot;).

1. Especifique a [configurações de exibição personalizadas](#view-settings):

   1. (Opcional) Para disponibilizar as configurações de dados em todas as exibições de entidade (para [!UICONTROL Campaigns], [!UICONTROL Ads]e assim por diante), selecione **[!UICONTROL Universal View]**.

      Depois de ativar ou desativar essa opção, você não poderá salvar a alteração na exibição existente, mas poderá criar uma nova exibição com a alteração.

   1. (Opcional) Para disponibilizar a exibição para todos os outros usuários que podem exibir os dados do anunciante, mova a variável **[!UICONTROL Shared]** controle deslizante para *[!UICONTROL Yes]*.

   1. (Opcional) No **[!UICONTROL Columns]** altere as colunas disponíveis para a guia, sua ordem e como classificar as linhas.

   1. (Opcional) Clique no link **[!UICONTROL Filters]** e especifique os filtros a serem aplicados.

      A aplicação de filtros retorna linhas somente quando o valor de uma métrica atende aos critérios especificados, quer a métrica esteja ou não incluída como uma coluna no relatório.

   1. (Opcional) Clique no link **[!UICONTROL Date]** e altere as configurações de data padrão.

   1. (Opcional) Clique no link **[!UICONTROL Additional Settings]** e altere as configurações.

1. Clique em **[!UICONTROL Save as New]**.

1. Insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Use um nome que ajudará a identificar a guia e as informações às quais ela se aplica (como &quot;Campanhas pausadas&quot; ou &quot;Os 50 anúncios principais&quot;).

### Editar um modo de exibição padrão ou personalizado

1. Abra as configurações de exibição:

   * (Se você já tiver aplicado a visualização) No lado direito da barra de ferramentas acima da tabela de dados, clique no nome da visualização atual (que pode ser &quot;[!UICONTROL Default]&quot;).

   * (Exibições personalizadas que não são aplicadas) No painel esquerdo, clique em ![Exibições personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Exibições personalizadas") para expandir o [!UICONTROL Custom Views] menu. Clique no nome da exibição personalizada.

1. Edite o [configurações de visualização](#view-settings):

   1. (Opcional) Para ativar ou desativar as configurações de dados em todas as exibições de entidade de pesquisa (para [!UICONTROL Campaigns], [!UICONTROL Ad Groups]e assim por diante), selecione ou desmarque **[!UICONTROL Universal View]**.

      Você não pode salvar a alteração na exibição existente, mas pode criar uma nova exibição com a alteração.

   1. (Opcional; exibições personalizadas que você criou apenas) Se a exibição ainda não for pública, disponibilize-a para todos os outros usuários que podem exibir os dados do anunciante movendo a variável **[!UICONTROL Shared]** controle deslizante para *[!UICONTROL Yes]*.

   1. (Opcional) No **[!UICONTROL Columns]** altere as colunas disponíveis para a guia, sua ordem e como classificar as linhas.

   1. (Opcional) Clique no link **[!UICONTROL Filters]** e edite os filtros que serão aplicados.

      A aplicação de filtros retorna linhas somente quando o valor de uma métrica atende aos critérios especificados, quer a métrica esteja ou não incluída como uma coluna no relatório.

      >[!NOTE]
      >
      >É possível aplicar, mas não salvar, alterações em filtros nas configurações de exibição padrão.

   1. (Opcional) Clique no link **[!UICONTROL Date]** e altere as configurações de data padrão.

   1. (Opcional) Clique no link **[!UICONTROL Additional Settings]** e altere as configurações.

1. Aplique ou salve as configurações:

   * Para aplicar as configurações temporariamente sem salvá-las na exibição, clique em **[!UICONTROL Apply]**.

     As configurações são aplicadas à guia até que você saia da exibição de gerenciamento de nível superior ou (quando aplicável) [exibir dados de outro anunciante](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Para exibições padrão e personalizadas que você criou) Para salvar as configurações na exibição atual, clique em **[!UICONTROL Save]**.

   * Para salvar as configurações em um novo modo de exibição personalizado, clique em **[!UICONTROL Save As]**. No [!UICONTROL Enter New Custom View Name] insira o nome da nova exibição e clique em **[!UICONTROL Save]**.

## Redefinir uma visualização padrão para as configurações padrão do sistema

Restaurar as configurações de exibição padrão remove todas as configurações salvas e reaplica as configurações padrão do sistema.

As configurações padrão do sistema variam de acordo com a guia. Para a maioria das guias, a exibição padrão do sistema mostra dados do dia anterior para itens em contas habilitadas e que estão ativas (por exemplo, somente grupos de anúncios ativos em campanhas ativas), com os dados classificados por custo e com dados de conversão baseados na data da transação.

1. No painel esquerdo, clique em ![Exibições personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Exibições personalizadas") para expandir o [!UICONTROL Custom Views] menu.

   As exibições são classificadas por entidade aplicável.

1. Ao lado do nome da exibição, clique em ![Restaurar para as configurações padrão](/help/search-social-commerce/assets/revert.png "Restaurar para as configurações padrão").

## Excluir um modo de exibição personalizado

É possível excluir qualquer exibição personalizada criada.

Se você excluir um modo de exibição personalizado aplicado à guia atual, a guia continuará a mostrar o modo de exibição personalizado até você sair do conjunto de modos de exibição (por exemplo, de modos de exibição dentro da [!UICONTROL Search] menu para a [!UICONTROL Reports] ou (quando aplicável) quando [exibir dados de outro anunciante](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. No painel esquerdo, clique em ![Exibições personalizadas](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Exibições personalizadas") para expandir o [!UICONTROL Custom Views] menu.

1. Mantenha o cursor sobre o nome da exibição personalizada e clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Continue]**.

## Configurações de exibição padrão e personalizada {#view-settings}

| **Guia** | **Campo** | **Descrição** |
| --- | --- | --- |
| [Acima de todas as guias] | Nome | Um nome exclusivo para a exibição. Não é possível editar o nome de uma exibição padrão. <p><b>Dica:</b> Use um nome que ajudará a identificar a guia e as informações às quais ela se aplica (como &quot;Campanhas pausadas&quot; ou &quot;Os 50 anúncios principais&quot;). |
|   | Visualização universal | Disponibiliza as configurações de dados em todas as visualizações de entidade (para Campanhas, Anúncios e assim por diante). As exibições universais podem incluir colunas de classificação de métricas e rótulos — mas não colunas de propriedades (como nome e status da entidade) porque diferem por tipo de entidade — bem como todos os outros atributos de exibição. Quaisquer critérios de filtro são aplicados à exibição de entidade quando aplicável e, caso contrário, são ignorados. Todos os filtros de métrica são avaliados localmente (por exemplo, para cliques \> 1000, a visualização Campanhas mostrará campanhas com mais de 1000 cliques e a visualização Grupos de anúncios mostrará grupos de anúncios com mais de 1000 cliques).<p>As colunas de propriedade de uma exibição universal são extraídas da exibição padrão da entidade. Você pode alterar as colunas de propriedade padrão de uma entidade específica nas configurações de exibição padrão.<p>Depois de ativar ou desativar essa opção, você não poderá salvar a alteração na exibição existente, mas poderá criar uma nova exibição com a alteração. |
|   | Compartilhar | (Somente visualizações personalizadas; opcional) Disponibiliza a visualização a todos os outros usuários que possam visualizar os dados do anunciante. Outros usuários não podem editar ou excluir a exibição, mas podem criar uma nova exibição nas configurações.Nas listas de exibição, cada exibição que outra pessoa está compartilhando está em itálico, como &quot;_Campanhas com melhor desempenho_.&quot; |
| Colunas | Colunas selecionadas e ordenação | As colunas de dados exibidas e sua ordem:<ul><li> (Para adicionar uma coluna) Na lista Colunas disponíveis, clique em um nome de coluna e arraste-o para a lista Colunas selecionadas e ordenação ou clique em ![seta para a direita](/help/search-social-commerce/assets/chevron-right.png) para movê-lo para lá.</li><li>(Para alterar a posição horizontal de uma coluna) Na lista Colunas selecionadas e ordenação, clique no nome da coluna e arraste-a para a posição desejada ou clique em ![seta para cima](/help/search-social-commerce/assets/chevron-up.png) ou ![seta para baixo](/help/search-social-commerce/assets/chevron-down.png) para movê-lo para lá. O nome da coluna superior aparecerá na coluna esquerda.</li><li>(Para remover uma coluna) Na lista Colunas selecionadas e ordenação, clique em um nome de coluna e arraste-o para a lista Colunas disponíveis ou clique em ![seta para a esquerda](/help/search-social-commerce/assets/chevron-left.png) para movê-lo para lá.</li></ul><b>Filtrar dados</b><p>Para listar apenas um tipo específico de dados, clique em qualquer um dos ícones ao lado da lista:<ul><li>![ícone propriedades](/help/search-social-commerce/assets/properties-icon.png) para nomes de propriedades e IDs para componentes de pesquisa, como Status</li><li>![ícone de tráfego](/help/search-social-commerce/assets/traffic-metrics-icon.png) para métricas de tráfego padrão, como impressões e cliques</li><li>![ícone de receita](/help/search-social-commerce/assets/revenue-metrics-icon.png) (para métricas de conversão rastreadas para o anunciante, incluindo métricas de conversão e envolvimento do site sincronizadas do Analytics)</li><li>![ícone personalizado](/help/search-social-commerce/assets/custom-metrics-icon.png) (para métricas derivadas personalizadas criadas pelo anunciante)</li><li>![ícone de classificação](/help/search-social-commerce/assets/classifications-icon.png) (para classificações de etiquetas).</li></ul> <b>Observações adicionais:</b><ul><li>Para adicionar, criar ou editar novas métricas, consulte &quot;Criar uma métrica personalizada&quot;, &quot;Editar uma métrica personalizada&quot; e &quot;Excluir uma métrica personalizada&quot;.</li><li>Se o relatório incluir dados para contas com moedas diferentes, os totais não serão incluídos para colunas baseadas em moeda (como Custo e CPC).</li><li>Você pode [editar temporariamente o conjunto de colunas no menu de cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), e [edite e classifique o conjunto de colunas na [!UICONTROL Columns] ícone](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Ícone Colunas](/help/search-social-commerce/assets/custom-columns.png "Ícone Colunas")).</li></ul> |
|   | Classificar por | A coluna pela qual classificar os dados. O valor padrão é diferente para cada tipo de relatório. |
|   | Ordem de classificação | Classificar ou não os dados **Crescente** ou **Decrescente** pedido. Mova o controle deslizante para selecionar uma opção. |
| Filtros | [Definições de filtro] | (Opcional) Filtros a serem aplicados aos dados. A aplicação de filtros retorna linhas somente quando o valor de uma coluna atende aos critérios especificados.<p>Para cada filtro a ser aplicado:<ol><li>No menu Adicionar filtro, selecione um nome de coluna. A lista inclui todas as colunas disponíveis e é classificada pelo tipo de coluna, com as colunas de propriedade primeiro.</li><li>Definir o filtro na coluna</li></ol>(Filtros com campos de entrada) Selecione um operador no segundo menu e insira o valor aplicável. Os valores não diferenciam maiúsculas de minúsculas. Clique em ![ícone de verificação](/help/search-social-commerce/assets/select.png) quando terminar.<p>Por exemplo, se você selecionou a coluna &quot;Cliques&quot; e deseja retornar apenas linhas com mais de 100 cliques, selecione _\>_ e insira `100` no campo de entrada.<p>Dependendo do tipo de dados, os operadores disponíveis podem incluir <i>maior que</i>, <i>menor que</i>, <i>igual a</i>, <i>contém</i>, <i>não contém</i>, <i>começa com</i>, <i>termina com</i>,<i>sem valor</i>ou <i>tem valor</i> <i>antes</i>, <i>após</i>ou <i>sem data</i>.<p>(Filtros sem campos de entrada) Clique em ![seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png) ao lado do menu Selecionar itens da lista e marque as caixas de seleção ao lado de cada valor a ser incluído. Clique em ![ícone de verificação](/help/search-social-commerce/assets/select.png) quando terminar.<p><b>Notas:</b><ul><li>É possível aplicar, mas não salvar, alterações em filtros nas configurações de exibição padrão.</li><li>Você também pode [alterar temporariamente os filtros aplicáveis](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) na visualização.</li></ul> |
|   | Incluir linhas somente com dados de desempenho | (Somente para exibições de Grupos de anúncios, Palavra-chave, Grupos de produtos, Disposições e Segmentações automáticas) <p>Inclui somente linhas com dados de desempenho durante as datas especificadas. Por padrão, essa opção é selecionada para reduzir o tempo de carregamento da página. <p><b>Aviso</b>: se você desmarcar a opção e a exibição incluir muitas entidades sem dados de desempenho, os dados levarão mais tempo para serem exibidos.<p> <b>Nota</b>: é possível aplicar, mas não salvar, as alterações nos filtros para as configurações de exibição padrão. As exibições padrão sempre mostram apenas entidades com dados de desempenho. |
| Data | Intervalo de datas | (Quando &quot;Incluir intervalo de datas&quot; estiver selecionado)<p>O intervalo de datas para o qual gerar dados. Escolha uma opção:<ul><li><i>[Intervalo predefinido]</i>: uma lista de incrementos de tempo comuns, que variam de <i>Hoje</i> para <i>Últimos 180 dias</i>. Escolha um na lista; o padrão é <i>Ontem</i>. Nota: <i>Mês passado</i>, <i>Últimos 3 meses</i>, e <i>Últimos 6 meses</i> mostrar dados dos meses anteriores.</li><li><i>Intervalo de datas personalizado:</i> Especifique a data inicial e a data final. Insira as datas no formato MM/DD/AAAA ou M/D/AAAA ou clique em ![ícone de calendário](/help/search-social-commerce/assets/calendar.png) ao lado de um campo e selecione uma data.</li></ul> |
|   | Comparação | Compara os dados do intervalo de datas especificado com os dados do segundo intervalo de datas. Ao selecionar essa opção, duas colunas adicionais são adicionadas para cada coluna de dados regular. Por exemplo, em vez de incluir apenas uma coluna para &quot;Impressões&quot;, o relatório inclui colunas para &quot;Intervalo de impressões 1&quot;, &quot;Intervalo de impressões 2&quot; e &quot;Diferença de impressões&quot;.<p><b>Notas:</b><ul><li>A coluna de diferença não é mostrada para métricas derivadas.</li><li>Relatórios que comparam intervalos de datas grandes podem levar mais tempo para serem gerados.</li></ul> |
|   | Formato de comparação | Como expressar a diferença entre os dados nos dois intervalos de datas selecionados na &quot;[_Campo de dados_] coluna &quot;Diferença&quot; Escolha uma opção:<ul><li><i>Variação</i> (o padrão): mostra a diferença como um valor numérico.</li><li><i>% de mudança</i>: mostra a diferença como uma porcentagem.</li></ul> |
| Configurações adicionais | Usar padrão | Aplica as configurações de atribuição especificadas nas configurações de atribuição de conversão no nível do anunciante. |
|   | Regra de atribuição | (Somente anunciantes com o serviço de rastreamento de conversão baseado em pixel do Adobe Advertising) Na guia, saiba como atribuir dados de conversão — possivelmente em vários canais de anúncios e portfólios — em uma série de eventos que levam a uma conversão. Por padrão, a regra especificada nas configurações de atribuição de conversão no nível do anunciante é selecionada.<ul><li> <i>Primeiro evento</i>: atribui a conversão ao primeiro clique pago da série na janela de lookback de cliques do anunciante ou, se nenhum clique pago ocorrer, à última impressão na janela de lookback de impressão do anunciante.</li><li><i>Peso Primeiro Evento Mais</i>: atribui a conversão a todos os eventos na série que ocorreu na janela de lookback de clique e na janela de lookback de impressão do anunciante, mas fornece o máximo de peso para o primeiro evento e, sucessivamente, menos peso para os eventos seguintes. Quando a conversão é precedida por cliques pagos e impressões, o peso de substituição de impressão especificado é aplicado ainda mais às impressões. Quando a conversão é precedida apenas por impressões, as impressões são ponderadas de acordo com o peso de viewthrough do anunciante em vez do peso de substituição de impressão.</li><li><i>Distribuição par</i>: atribui a conversão igualmente a cada evento na série que ocorreu na janela de retrospectiva de cliques e na janela de retrospectiva de impressão do anunciante. Quando a conversão é precedida por cliques pagos e impressões, o peso de substituição de impressão especificado é aplicado ainda mais às impressões. Quando a conversão é precedida apenas por impressões, as impressões são ponderadas de acordo com o peso de viewthrough do anunciante em vez do peso de substituição de impressão.</li><li><i>Peso Último Evento Mais</i>: atribui a conversão a todos os eventos na série que ocorreu na janela de retrospectiva de clique e na janela de retrospectiva de impressão do anunciante, mas fornece o máximo de peso para o último evento e, sucessivamente, menos peso para os eventos anteriores. Quando a conversão é precedida por cliques pagos e impressões, o peso de substituição de impressão especificado é aplicado ainda mais às impressões. Quando a conversão é precedida apenas por impressões, as impressões são ponderadas de acordo com o peso de viewthrough do anunciante em vez do peso de substituição de impressão.</li><li><i>Último evento</i> (o padrão): Atribui a conversão ao último clique pago da série na janela de lookback de cliques do anunciante ou, se nenhum clique pago ocorreu, à última impressão na janela de lookback de impressão do anunciante.</li><li><i>Em forma de U</i>: atribui a conversão a todos os eventos na série que ocorreu na janela de retrospectiva de clique e na janela de retrospectiva de impressão do anunciante, mas fornece mais peso para o primeiro evento e os últimos eventos, com peso sucessivamente menor para os eventos no meio do caminho de conversão. Quando a conversão é precedida por cliques pagos e impressões, o peso de substituição de impressão especificado é aplicado ainda mais às impressões. Quando a conversão é precedida apenas por impressões, as impressões são ponderadas de acordo com o peso de viewthrough do anunciante em vez do peso de substituição de impressão.</li></ul><p><b>Notas:</b><ul><li>Todas as regras de atribuição além de Último evento estão disponíveis apenas para anunciantes com rastreamento de cliques em Adobe Advertising e com rastreamento de conversão de Adobe Advertising ou Adobe Analytics (com uma integração do Analytics).</li><li>As regras de atribuição se aplicam aos cliques nos anúncios pagos em qualquer canal. Elas não se aplicam a impressões para anúncios de pesquisa paga, que não podem ser rastreados no nível do evento.</li><li>Ao relatar dados de conversão usando qualquer regra de atribuição, exceto uma das regras de &quot;Último evento&quot;, os eventos que antecedem a conversão podem ocorrer em vários portfólios. Quando isso ocorrer, a visualização incluirá dados para a conversão somente quando os anúncios ou palavras-chave nesses portfólios forem incluídos na visualização.</li><li>Para exibições padrão, recomendamos que você mantenha a regra de atribuição padrão, que é usada para calcular o [valor do objetivo](/help/search-social-commerce/glossary.md#o-p) (anteriormente chamada de &quot;receita ponderada&quot;) para cada unidade de oferta durante a otimização da oferta.</li></ul> |
|   | Conversões Baseadas Em | Como relatar dados de conversão:<ul><li><i>Data da transação</i> (o valor-padrão): Para ver as transações cuja data de transação ocorreu durante o período especificado. Isso indica quanta receita foi ganha dentro do período especificado.</li><li><i>Data do clique</i>: Para ver as transações que resultaram de um clique que ocorreu durante o período especificado. Quando um portfólio tem atraso significativo entre cliques e transações, essa opção é útil para calcular a receita histórica por clique do portfólio, que indica os comportamentos de receita a serem esperados ao longo do tempo. |
