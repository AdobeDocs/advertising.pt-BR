---
title: Gerenciar restrições para pesquisar unidades de oferta
description: Saiba mais sobre as restrições para restringir ofertas de unidades de oferta em campanhas CPC em portfólios herdados de nível de palavra-chave.
feature: Search Campaign Management, Search Optimization
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: c800239a-06eb-4249-9aef-771973d24d35
source-git-commit: 9cc395a6b0fe25435ca6ed022f8da767d525d68e
workflow-type: tm+mt
source-wordcount: 2660
ht-degree: 0%

---

# Gerenciar restrições para pesquisar unidades de oferta

*Aplicável para unidades de oferta em campanhas CPC somente em portfólios de nível de palavra-chave herdados*

As restrições de unidade de oferta são regras que restringem ofertas otimizadas para todas as [unidades de oferta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html?lang=pt-BR) com modelos de custo e receita associados à restrição.

## Sobre restrições

Cada restrição se aplica a uma moeda específica e, opcionalmente, inclui condições de acionamento que devem ser atendidas durante um período de avaliação de dados especificado para que a regra seja aplicada. Os dados a serem avaliados podem incluir tipo de canal, tipo de correspondência, dados de cliques, dados de conversão ou métricas derivadas. Por exemplo, você pode restringir lances a um intervalo monetário específico, aumentar ou diminuir continuamente os lances por uma quantia especificada ou lance de acordo com o lance médio da carteira. Cada restrição tem uma data de início aplicável e expira em uma data específica ou é aplicada indefinidamente.

Depois de configurar uma restrição, você pode atribuí-la a unidades de oferta específicas ou a todas as unidades de oferta em grupos de publicidade ou campanhas específicas. Cada unidade de oferta pode ter uma restrição. As restrições são herdadas por entidades filhas, mas podem ser substituídas. Uma restrição atribuída no nível mais baixo sempre substitui uma restrição atribuída em um nível pai. Quando você atribui uma restrição a uma unidade de lance, o lance opera dentro das restrições especificadas para essa unidade de lance, independentemente de quanta receita a unidade de lance gera, quando a unidade de lance tem modelos de custo e receita.

>[!CAUTION]
>
>Ao atribuir restrições a uma unidade de oferta, você sobrepõe a decisão do sistema de otimização de oferta e assume a responsabilidade pelo ROI dessa unidade de oferta.

>[!NOTE]
>
>* As restrições ativas restringem os lances somente para unidades de lance atribuídas em portfólios de nível de palavra-chave herdada otimizados. Elas são ignoradas para unidades de oferta que estão em portfólios híbridos, estão em portfólios ativos ou não estão em portfólios. **Dica:** nas configurações do portfólio, ative a opção de portfólio para &quot;Ajustar automaticamente os limites de orçamento da campanha&quot;. O valor &quot;Múltiplo&quot; recomendado é &quot;1&quot;.
>* As restrições de lance são ignoradas para unidades de lance sem dados suficientes para gerar modelos de custo e receita.
>* (Campanhas com uma estratégia de oferta CPC ou eCPC) Quando uma restrição de oferta entra em conflito com um limite de oferta no nível de portfólio, a restrição substitui o limite no nível de portfólio. Por exemplo, se a oferta mínima de um portfólio for de US$ 5, mas você restringir uma unidade de oferta no portfólio a um lance mínimo de US$ 3, a unidade de oferta será de US$ 3 ou superior. No entanto, o gasto geral para unidades de oferta restritas é determinado pelo parâmetro [&quot;Gastos em torno de Restrições&quot; do portfólio](#spend-around-constraints).
>* Restrições operam na oferta base. Qualquer tipo de ajuste de oferta para a oferta base (como aumentar a oferta para os usuários finais em dispositivos móveis) pode mover a oferta para fora do intervalo permitido para a restrição. Por exemplo, se a restrição exigir um CPC máximo de 6 USD, a oferta base já será de 6 USD e o portfólio otimizará automaticamente os ajustes de oferta para dispositivos móveis em 50% a 60%, o CPC máximo será de 9,00 a 9,60 USD — não 6 USD.

### Tipos de restrição {#constraint-types}

* **[!UICONTROL Bid]:** Restringe lances a um intervalo monetário.

* **[!UICONTROL Bid Shift]:** altera continuamente os lances otimizados para todas as unidades de lance associadas por um valor especificado, dentro dos limites de lances. Uma mudança de oferta faz com que os portfólios relevantes superem ou subutilizem o valor total causado pela mudança de oferta, independentemente da configuração do portfólio para &quot;Gastos em torno de restrições&quot;. Nota: Se a oferta atual do CPC já for igual ou maior que o Lance Máximo ou igual ou inferior ao Lance Mínimo, a restrição será ignorada e o lance não será alterado. Além disso, as restrições de alternância de oferta não são aplicadas a unidades de oferta sem dados suficientes para gerar modelos de custo e receita.

* **[!UICONTROL Incremental Bidding]:** (Aplicável somente a palavras-chave sem impressões) Aumenta ou diminui o lance incrementalmente em uma taxa especificada até que o lance atinja um destino designado.

* **[!UICONTROL Search Engine Min Bid]:** (somente contas do [!DNL Google Ads]) Usa as ofertas de CPC mínimas determinadas pelo mecanismo de pesquisa como suas ofertas mínimas. À medida que o mecanismo de pesquisa altera seus lances mínimos, seu lance muda de acordo. Opcionalmente, você pode especificar limites de lance adicionais para todas as unidades de lance associadas.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] campanhas CPC com correspondência exata apenas) Restringe ofertas a um intervalo monetário quando os anúncios estão entre um compartilhamento de impressões mínimo e máximo. **Observação:** quando a restrição não é econômica, o recurso de otimização pode substituí-la.

### Quando aplicar restrições

Alguns motivos para restringir as unidades de oferta incluem:

* Para expor rapidamente palavras-chave e anúncios não testados.

* Para reduzir riscos de novos portfólios, contas, campanhas e grupos de anúncios. Por exemplo, antes de iniciar um portfólio, é possível definir lances máximos em unidades de lance de alto tráfego e, em seguida, aumentar gradualmente os valores a cada dia. Isso permite que o modelo de licitação se ajuste a cada dia sem o risco de grandes aumentos de oferta.

* Para garantir que as palavras-chave tail com altas taxas de conversão não apresentem lances negativos.

* Para oferecer termos específicos que são fundamentais para sua marca ou durante promoções.

### Onde exibir informações sobre restrições na interface

Além de abrir a [[!UICONTROL Constraints] visualização](#constraints-view), você também pode ver informações relacionadas às suas restrições das seguintes maneiras:

* Todas as suas restrições são valores de etiquetas para uma única [classificação de etiqueta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html?lang=pt-BR) chamada &quot;[!UICONTROL Constraints]&quot;.

   * &quot;[!UICONTROL Constraints]&quot; está incluído na lista &quot;[!UICONTROL Classifications]&quot; nas configurações de exibição padrão e personalizada e nos relatórios agendados. Você pode adicionar a coluna sempre que quiser ver as restrições atribuídas às entidades relevantes.

   * Quando você baixa uma bulksheet, &quot;[!UICONTROL Constraints]&quot; é listado na coluna &quot;[!UICONTROL Classifications]&quot; para as entidades aplicáveis na caixa de diálogo [!UICONTROL Download Bulksheet]. Ao incluir a coluna, o bulksheet baixado inclui todas as restrições atribuídas às entidades relevantes.

  A classificação [!UICONTROL Constraints] não está incluída na exibição [!UICONTROL Label Classifications] — a exibição [!UICONTROL Constraints] é separada. A classificação [!UICONTROL Constraints] também não está incluída no limite de classificação de 30 rótulos.

* [A [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md) inclui dados de custo, clique e conversão (opcionalmente) para restrições que usam a arquitetura de classificação de etiquetas.

### A visualização [!UICONTROL Constraints] {#constraints-view}

A exibição [!UICONTROL Goals] > [!UICONTROL Constraints] lista todas as suas restrições. As colunas disponíveis incluem o status da restrição; o tipo de restrição, as datas de início e término; o número de campanhas, grupos de anúncios, palavras-chave, anúncios, posicionamentos, direcionamentos automáticos e grupos de produtos aos quais a restrição está associada; impressões, cliques e dados de custo; e dados de receita para todas as métricas de conversão visíveis.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>Os dados de desempenho de uma linha na exibição [!UICONTROL Constraints] podem não corresponder aos dados de desempenho da entidade de nível superior à qual a restrição está atribuída. Como uma restrição atribuída no nível inferior sempre substitui uma restrição atribuída em um nível principal, uma restrição atribuída a uma campanha ou grupo de anúncios pode não permanecer atribuída aos grupos de anúncios secundários e palavras-chave. Por exemplo, se a Campanha A receber a Restrição A, todos os grupos de anúncios e palavras-chave na Campanha A herdarão automaticamente a Restrição A. No entanto, esses grupos de anúncios e palavras-chave poderiam ser posteriormente atribuídos a outras restrições, como a Restrição B, e eles perderiam sua associação com a Restrição A.

>[!NOTE]
>
>Atribuir restrições a unidades de oferta e cancelá-las, da exibição de gerenciamento de entidade relevante (como da exibição [!UICONTROL Campaigns] para restrições no nível da campanha).

#### Ações disponíveis

* [Criar uma restrição](#constraint-create).

* [Editar configurações de restrição](#constraint-edit).

* [Alterar o status das restrições](#constraint-change-status).

## Criar uma restrição {#constraint-create}

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. Na barra de ferramentas superior direita acima da tabela de dados, clique em **[!UICONTROL Create Constraint]**.

1. Insira as [configurações de restrição](#constraint-settings).

   Para mover entre as guias [!UICONTROL Constraint Type] e [!UICONTROL Conditions], clique na guia que você deseja abrir ou clique nos botões [!UICONTROL Next] e [!UICONTROL Back].

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

Depois de criar uma restrição, você pode [atribuí-la](#constraint-assign) a campanhas, grupos de anúncios, palavras-chave, posicionamentos e grupos de produtos de nível de unidade.

## Editar configurações de restrição {#constraint-edit}

É possível editar as configurações de uma restrição por vez.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Opcional) Filtre a lista [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de um [cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Marque a caixa de seleção ao lado da restrição que deseja editar.

1. Na barra de ferramentas de ações em massa, clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar").

1. Editar as [configurações de restrição](#constraint-settings).

   Para mover entre as guias [!UICONTROL Constraint Type] e [!UICONTROL Conditions], clique na guia que você deseja abrir ou clique nos botões [!UICONTROL Next] e [!UICONTROL Back].

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

## Alterar o status das restrições {#constraint-change-status}

Você pode pausar qualquer restrição ativa para desativá-la. Você pode habilitá-lo mais tarde alterando o status de volta para *ativo*.

Também é possível excluir uma restrição, o que remove todas as associações com componentes de conta e torna a restrição indisponível para uso futuro. Os dados de relatório para a restrição não estão mais disponíveis. **Observação:** para simplesmente desassociar uma restrição de um componente de conta, consulte &quot;[Cancelar atribuição de restrições de unidades de oferta de pesquisa](#constraints-unassign).&quot;

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Opcional) Filtre a lista [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de um [cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Marque a caixa de seleção ao lado de cada restrição cujo status você deseja alterar.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique no botão de status:

   * Para ativar todas as linhas selecionadas, clique em ![Ativar](/help/search-social-commerce/assets/activate-new.png "Ativar").

   * Para pausar todas as linhas selecionadas, clique em ![Pausar](/help/search-social-commerce/assets/pause-new.png "Pausar").

   * Para excluir todas as linhas selecionadas, clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Configurações de restrição {#constraint-settings}

| Guia | Parâmetro | Descrição |
|---|---|---|
| \[Informações básicas\] | [!UICONTROL Constraint Name] | Um nome exclusivo para a restrição. |
| | [!UICONTROL Currency] | A moeda em que as unidades de oferta aplicáveis são propostas. As unidades de oferta para as quais uma moeda diferente é usada são ignoradas. |
| | [!UICONTROL Status] | O status da restrição:<ul><li>**Ativo:** (padrão) A restrição é aplicada durante as condições e o intervalo de datas especificados.</li><li>**Pausado:** a restrição não foi aplicada.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | O tipo de restrição. Para obter descrições dos tipos de restrição e das redes de anúncios qualificadas para cada um, consulte &quot;[Tipos de restrição](#constraint-types).&quot; |
| | [!UICONTROL Start Date] | O primeiro dia em que a restrição entra em vigor. O padrão é o dia atual. Para alterar a data, insira uma data ou clique em ![Calendário](/help/search-social-commerce/assets/calendar-new.png "Calendário") para abrir o calendário e selecionar uma data. |
| | [Data de término] | Se a restrição se tornará ineficaz em uma data específica. Para aplicar a restrição indefinidamente, como quando a unidade de oferta é central para a marca da empresa, deixe o campo vazio. Para finalizar a restrição em uma data específica, insira uma data ou clique em ![Calendário](/help/search-social-commerce/assets/calendar-new.png "Calendário") para abrir o calendário e selecionar uma data. **Observação:** a restrição não pode expirar antes de amanhã. |
| | [!UICONTROL Set constraint options for Bid] | (Somente restrições [!UICONTROL Bid]) As configurações incluem:<ul><li>**[!UICONTROL Min Bid]:** A oferta básica mínima para unidades de oferta associadas.</li><li>**[!UICONTROL Max Bid]:** A oferta básica máxima para unidades de oferta associadas.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | (Somente restrições [!UICONTROL Bid Shift]) O tipo e a quantidade de alternância de oferta a serem aplicados continuamente à oferta base:<ul><li>*[!UICONTROL Increases]:* Aumenta as ofertas de acordo com uma porcentagem especificada ou o valor da moeda. Insira o valor a ser alterado e selecione *$* ou *%*. Insira também um **[!UICONTROL Max Limit]**, que é o lance mais alto possível (teto) quando a restrição é aplicada. **Observação:** se a oferta CPC atual já for igual ou maior que [!UICONTROL Max Limit], a restrição será ignorada e a oferta não será alterada.</li><li>*[!UICONTROL Decreases]:* Diminui os lances de acordo com uma porcentagem ou valor de moeda especificado. Insira o valor a ser alterado e selecione *$ ou %*. Insira também um **[!UICONTROL Min Limit]**, que é o menor lance possível (piso) quando a restrição é aplicada. **Observação:** se a oferta CPC atual já for igual ou inferior a [!UICONTROL Min Limit], a restrição será ignorada e a oferta não será alterada.</li></ul>**Notas:**<ul><li>Um deslocamento de oferta fará com que os portfólios relevantes sejam sobre ou subutilizados pelo valor total causado pelo deslocamento de oferta, independentemente da configuração do portfólio para &quot;[!UICONTROL Spend Around Constraints]&quot;.</li><li>Se você especificar uma data final para a restrição e o recurso de otimização estiver ajustando automaticamente os limites de gastos para as campanhas no portfólio, as ofertas não serão simplesmente revertidas para as quantias originais após a data final, mas serão ajustadas como ideais.</li><li>Os deslocamentos de oferta não são aplicados a unidades de oferta sem dados suficientes para gerar modelos de custo e receita.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | (Somente restrições [!UICONTROL Incremental Bidding]) Uma meta de oferta e quanto e com que frequência aumentar ou diminuir a oferta incrementalmente até atingir a meta:<ul><li>**[!UICONTROL Bid target]:** O valor da oferta de destino.</li><li>**[!UICONTROL Incrementally change bids by]** e **[Tipo]:** Quanto aumentar ou diminuir incrementalmente as ofertas e se alterar as ofertas de acordo com um valor de moeda (**$**) ou porcentagem (*%*).</li><li>**[!UICONTROL Every __ days]:** Com que frequência incrementar lances.</li></ul>Por exemplo, digamos que a oferta atual para uma das palavras-chave seja de 100 centavos e que você deseja alterar a oferta em 10% todos os dias até atingir uma meta de oferta de 500 centavos. No Dia 1 após a definição da restrição, a oferta para essa palavra-chave é de 110 centavos (oferta atual + 10%). No Dia 2, o lance será de 120 centavos (lance atual para o Dia 1 + 20%) e assim por diante. No entanto, se o objetivo da oferta for de 50 centavos e os outros parâmetros forem os mesmos, então as ofertas diminuem gradualmente até que a oferta atinja 50 centavos. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] restrições) Usa o lance mínimo necessário para mostrar uma unidade de lance na primeira página dos resultados de pesquisa no Google ([!UICONTROL Google First Page CPC]). Opcionalmente, insira um valor **[!UICONTROL Min Bid]** e/ou um valor **[!UICONTROL Max Bid]** para definir o intervalo de ofertas qualificadas para a restrição. Por exemplo, se você especificar um [!UICONTROL Min Bid] de US$ 2,50 e um [!UICONTROL Max Bid] de US$ 4, você não fará uma oferta na unidade de oferta se o lance da primeira página de [!DNL Google Ads] estiver abaixo de US$ 2,50 ou acima de US$ 4. |
| | [!UICONTROL Set constraint options for Impression Share] | (Somente restrições [!UICONTROL Impression Share]) As configurações incluem:<ul><li>**[!UICONTROL Min Bid]** (Opcional) A oferta básica mínima para unidades de oferta associadas.</li><li>**[!UICONTROL Max Bid]:** (Opcional) A oferta básica máxima para unidades de oferta associadas.</li><li>**[!UICONTROL Min Impression Share]:** O compartilhamento de impressão mais baixo, como uma porcentagem, que disparará a restrição para as unidades de oferta aplicáveis. Deve estar entre 10 e 90. **Observação:** quando a restrição não é econômica, o recurso de otimização pode substituí-la.</li><li>**[!UICONTROL Max Impression Share]:** O compartilhamento de impressão mais alto, como uma porcentagem, que disparará a restrição para as unidades de oferta aplicáveis. Deve estar entre 10 e 90.**Observação:** quando a restrição não é econômica, o recurso de otimização pode substituí-la.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Se aplicar condições à restrição:<ul><li>*[!UICONTROL No Condition]:* (padrão) A restrição é aplicada incondicionalmente durante o intervalo de datas especificado.</li><li>*[!UICONTROL Satisfy]:* A restrição é aplicada somente quando as condições especificadas são atendidas durante um período de avaliação de dados especificado.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Quando as condições são definidas) O período para o qual os dados dos critérios especificados devem ser avaliados. Se você selecionar *[!UICONTROL Custom date range],**&#x200B; especifique o &#x200B;** [!UICONTROL Start Date] **&#x200B; e o &#x200B;** [!UICONTROL End Date]** inserindo cada data no formato `MM-DD-YYYY` (como 03-29-2026 para 29 de março de 2026) ou clicando no ![botão Calendário](/help/search-social-commerce/assets/calendar-new.png "botão Calendário") para abrir o calendário e selecionar cada data. |
| | [!UICONTROL When to Apply Constraints] | (Quando as condições são definidas) Quantas condições de filtro devem ser atendidas para aplicar a restrição:<ul><li>*[!UICONTROL Match All Filters]:* Aplica a restrição quando cada condição de filtro especificada é atendida.</li><li>*[!UICONTROL Match Any Filters]:* Aplica a restrição quando pelo menos uma das condições de filtro especificadas é atendida.</li></ul> |
| | [!UICONTROL Filters] | (Quando as condições são definidas) Um ou mais critérios que devem ser atendidos. Para criar um filtro, selecione uma propriedade ou métrica na lista. Para propriedades (como [!UICONTROL Channel Type]), selecione os valores aplicáveis na lista. Para métricas (como [!UICONTROL Clicks]), selecione um operador e insira o valor aplicável. Por exemplo, para retornar apenas unidades de oferta com mais de 100 cliques, selecione **Cliques**, selecione **maior que** e digite `100` no campo de entrada.</li></ul> |

## Atribuir restrições às unidades de oferta de pesquisa {#constraint-assign}

Você pode aplicar restrições de unidade de oferta a qualquer campanha, grupo de publicidade, palavra-chave, disposição ou público-alvo de pesquisa dinâmica (direcionamento automático).

Cada entidade pode ter apenas uma restrição. É possível atribuir uma única restrição a uma ou mais entidades ao mesmo tempo.

>[!NOTE]
>
>* Posteriormente, se você editar uma palavra-chave ou a cópia de um anúncio — criando assim uma nova palavra-chave ou anúncio — a restrição não será atribuída à nova entidade.
>* Veja as mesmas instruções no [[!UICONTROL Campaigns] modo de exibição](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups] modo de exibição](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords] modo de exibição](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md) ou [[!UICONTROL Placements] modo de exibição](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. No menu principal, abra a visualização de gerenciamento relevante.

   Por exemplo, para atribuir restrições no nível da campanha, vá para [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. (Opcional) Filtre a lista [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de um [cabeçalho de coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Marque a caixa de seleção ao lado de cada entidade à qual você atribuirá uma única restrição.

1. Na barra de ferramentas de ações em massa, clique em **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecione a restrição.

1. Clique em **[!UICONTROL Assign Now]**.

## Cancelar atribuição de restrições de unidades de oferta de pesquisa {#constraints-unassign}

>[!NOTE]
>
>* Para excluir uma restrição, tornando-a indisponível para uso futuro, consulte &quot;[Alterar o status das restrições](#constraint-change-status)&quot;.
>* Veja as mesmas instruções no [[!UICONTROL Campaigns] modo de exibição](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups] modo de exibição](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords] modo de exibição](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md) ou [[!UICONTROL Placements] modo de exibição](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. No menu principal, abra a visualização de gerenciamento relevante.

   Por exemplo, para desatribuir restrições no nível da campanha, vá para [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Marque a caixa de seleção ao lado de cada entidade da qual você cancelará a atribuição de restrições.

1. Na barra de ferramentas de ações em massa, clique em **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Clique em **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Gerenciar atribuições de restrição para campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para grupos de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gerenciar atribuições de restrição para palavras-chave](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [Gerenciar atribuições de restrição para posicionamentos](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [O [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
