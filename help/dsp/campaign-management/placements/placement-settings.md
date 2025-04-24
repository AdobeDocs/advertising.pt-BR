---
title: Configurações de posicionamento
description: Consulte descrições das configurações de posicionamento disponíveis.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: eaa25ce24bf00fb5ff7ea1e4a3364d4439f49b00
workflow-type: tm+mt
source-wordcount: '4039'
ht-degree: 0%

---

# Configurações de posicionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** O nome do posicionamento.

>[!TIP]
>Use uma convenção de nomenclatura que faça sentido para a sua situação. Uma convenção de nomenclatura sugerida é &quot;*\&lt;Campaign Name\>: \&lt;Ad Unit\>: \&lt;Duration\>: \&lt;Targeting\>*.&quot;

**[!UICONTROL Status]:** O status do posicionamento: *[!UICONTROL Active]* (o padrão) ou *[!UICONTROL Paused]*.

>[!TIP]
>A prática recomendada é pausar o posicionamento até que você esteja pronto para iniciá-lo.

**[!UICONTROL Details]:** (Somente leitura) O tipo de anúncio aplicável, a conta que está criando ou criou o posicionamento e a campanha pai. Para ver mais detalhes, clique em **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Abre uma lista de modelos de posicionamento existentes. Para preencher automaticamente as configurações de direcionamento a partir de um modelo:

1. Siga um destes procedimentos:

   * Para reutilizar todos os alvos de um modelo, marque a caixa de seleção ao lado do nome do modelo.

   * Para reutilizar tipos de alvo individuais de um modelo, expanda o nome do modelo e marque a caixa de seleção ao lado dos tipos de alvo que deseja reutilizar.

1. Clique em **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Somente formatos de anúncio de vídeo) A duração do anúncio e/ou as especificações do anúncio, que são usadas para calcular a projeção de Previsão à direita. Os campos variam de acordo com o tipo de anúncio.

**[!UICONTROL Environment]:** (somente formato de anúncio de Vídeo Universal) Os ambientes de dispositivo (Desktop, Móvel, TV Conectada) a serem incluídos como destinos no posicionamento. Especifique pelo menos um.

Nos relatórios personalizados, a dimensão no nível de posicionamento &quot;Ambiente do dispositivo&quot; indica o ambiente direcionado.

**[!UICONTROL Placement tags]:** (Opcional) Palavras-chave ou apelidos para ajudá-lo a localizar este posicionamento.

## Metas

**[!UICONTROL Package]:** (Opcional) Um pacote ao qual o posicionamento está atribuído. Clique em ![Editar](/help/dsp/assets/edit.png) para selecionar um pacote existente ou criar um pacote. Quando você atribui o posicionamento a um pacote, a seção [!UICONTROL Goals] é atualizada com as datas de início e término, a meta de entrega e o orçamento do pacote.

**[!UICONTROL Flight Dates]:** A data de início e a data de término do posicionamento. Os anúncios aprovados estão qualificados para execução durante o voo quando a inserção estiver ativa e atribuída a um pacote ou campanha ativa.

As datas do pacote (quando aplicável) ou da campanha são preenchidas automaticamente por padrão.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha e nas datas de voo do pacote.

### Posicionamentos atribuídos a pacotes com ritmo no nível do pacote

**[!UICONTROL Placement Funding]:** Como fazer orçamento para o posicionamento:

* *[!UICONTROL Optimize based on performance]:* Controla o orçamento no nível do pacote.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Permite definir um orçamento de posicionamento mínimo e/ou máximo. Especifique pelo menos um tipo de orçamento:

   * *[!UICONTROL Maximum Budget]*: Insira um valor e a duração (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: o orçamento mínimo como uma porcentagem do orçamento do pacote. Quando um limite de intervalo é especificado, o valor de orçamento mínimo é sempre calculado como uma porcentagem do limite de intervalo. Caso contrário, será calculado como uma porcentagem do orçamento do pacote.

**[!UICONTROL Max Bid]:** O máximo a ser pago por 1000 impressões.

**[!UICONTROL Placement Pre-bid Filters]:** Até cinco limites de KPI (como uma métrica de visibilidade mínima ou taxa de click-through) que devem ser atingidos para que a oferta ocorra. Você pode usar filtros de pré-oferta como táticas de otimização, mas entende que cada regra pode limitar as oportunidades nas quais esse posicionamento pode fazer ofertas. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

Consulte as descrições de cada filtro de pré-oferta em &quot;[Filtros de pré-oferta no nível de posicionamento e Como usá-los](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Todas as outras disposições

**[!UICONTROL Budget Goal]:** O limite de orçamento bruto e o intervalo de orçamento (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Posicionamentos em campanhas somente com gerenciamento de margem) O limite de orçamento bruto e o intervalo de orçamento (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** A meta de otimização do pacote. Consulte as descrições de cada meta de otimização em &quot;[Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** A meta de destino, que é usada para monitorar o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para decisões.

**[!UICONTROL Pace on]:** A base para o ritmo:

* **[!UICONTROL Budget goal]:** (padrão) essa opção fornece o máximo de impressões possível dentro do orçamento alocado.

* **[!UICONTROL Impressions]:** Essa opção fornece impressões até que uma quantidade especificada seja atingida dentro de um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** O máximo a ser pago por 1000 impressões.

**[!UICONTROL Flight pacing]:** (Posicionamentos com ritmo de nível de posicionamento somente) Como posicionar e entregar:

* *[!UICONTROL Even]:* (padrão) Atua a entrega de maneira uniforme em cada voo, com uma meta de 50% da entrega na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (o padrão) Acelera a entrega para que esteja 55 a 65% concluído na metade da duração do voo.

* *[!UICONTROL Frontload]:* acelera a entrega de modo que esteja 65 a 75% concluído na metade do processo.

* *[!UICONTROL Aggressive Frontload]:* acelera a entrega de modo que esteja 75 a 85% concluído na metade do processo.

**[!UICONTROL Intraday pacing]:** (Posicionamentos com ritmo de nível de posicionamento somente) Como acompanhar e entregar em cada dia dentro do voo:

* *[!UICONTROL Even]:* (padrão) Dimensiona a entrega com base na disponibilidade de estoque. Geralmente, mais anúncios são entregues por hora durante o dia, quando o volume do leilão é maior, e menos anúncios são entregues de manhã e à noite.

* *[!UICONTROL ASAP]:* (o padrão) Acelera a entrega para o dobro da velocidade de *Even*.

  >[!CAUTION]
  >
  >Essa opção pode afetar negativamente o desempenho. Use-a somente quando estiver priorizando totalmente o delivery e o gasto em relação à otimização de desempenho.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Até cinco filtros que devem ser atendidos para que a oferta ocorra. Você pode usar filtros de pré-oferta como táticas de otimização, mas lembre-se de que cada regra pode limitar as oportunidades nas quais esse posicionamento pode licitar. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Opcional) Locais específicos nos quais incluir ou excluir anúncios no posicionamento. Se você não especificar nenhum local, todos os locais serão direcionados.

>[!NOTE]
>
>Os locais de cidade e DMA não estão disponíveis para inserções do Roku.

Para especificar locais:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para incluir ou excluir um País, Estado, Cidade, DMA, Distrito Legislativo Federal ou Distrito Legislativo Estadual:
      1. Selecione o tipo de local na coluna à esquerda.
      1. (Conforme necessário) Clique em um local para expandi-lo.
      1. Ao lado do local, clique em *[!UICONTROL Include]* para incluí-lo como um destino ou *[!UICONTROL Exclude]* para excluí-lo como um destino.
   * Para pesquisar um código postal e incluir ou excluir todos os resultados selecionados:
      1. Clique em **[!UICONTROL Search Postal Code]**.
      1. Selecione o país.
      1. Insira o nome da cidade e clique em ![Editar](/help/dsp/assets/search.png).
      1. Clique no resultado de pesquisa correto.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como destinos ou *[!UICONTROL Exclude All]* para excluir todos os locais como destinos.
   * Para informar ou colar códigos postais e incluir ou excluir todos eles:
      1. Clique em **[!UICONTROL Paste Postal Code]**.
      1. Selecione o país.
      1. Insira ou cole até 1000 códigos postais.
Inclua um código postal por linha ou insira vários valores separados por vírgulas ou guias.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como destinos ou *[!UICONTROL Exclude All]* para excluir todos os locais como destinos.
   * Para remover um local da lista [!UICONTROL Included] ou [!UICONTROL Excluded], clique em **[!UICONTROL X]** ao lado do local na coluna à direita.
1. Clique em **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nem todos os países têm localizações de Estado, Cidade ou Código Postal.
>* O DMA (área de mercado designada), os Distritos Legislativos Federais e os Distritos Legislativos Estaduais estão disponíveis somente para locais nos EUA.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Faz inventário das fontes a serem incluídas ou excluídas como destinos. Para a maioria dos tipos de posicionamento, todos os tipos de inventário e todas as origens para cada tipo são incluídos por padrão. Para [!DNL Roku] posicionamentos, você deve especificar o tipo de inventário e as fontes. Você pode escolher entre os seguintes tipos de inventário:

* [!UICONTROL Public]: (Todos os tipos de posicionamento exceto Roku) Todos os inventários de intercâmbio aberto aos quais a DSP tem acesso. Você pode incluir e excluir inventário público.

  Você pode visualizar a lista por fonte ou por feed. Ao visualizar a lista por feed, você pode pesquisar por nome do feed, chave do feed ou uma tag característica selecionada.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Suas ofertas privadas existentes (ou ofertas [!DNL Roku] privadas existentes para [!DNL Roku] inserções) com editores que você configurou no DSP. Você pode incluir, mas não excluir, inventário público.

  Você pode pesquisar a lista por palavra-chave, chave, ID de negócio ou tag personalizada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) substitui o algoritmo de preço de oferta para oferecer pelo menos os preços fixo e mínimo para ofertas.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Todos os [estoque [!UICONTROL On Demand] premium não garantido](/help/dsp/inventory/on-demand-inventory-about.md) (ou [!UICONTROL On Demand] ofertas de [!DNL Roku] para [!DNL Roku] posicionamentos) que você assinou no [!DNL DSP]. Você pode incluir e excluir o inventário de [!UICONTROL On Demand].

  Você pode visualizar a lista por fonte ou por feed. Ao visualizar a lista por feed, você pode pesquisar por nome do feed, chave do feed ou uma região do editor, tag de categoria ou tag característica selecionada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) substitui o algoritmo de preço de oferta para oferecer pelo menos os preços fixo e mínimo para ofertas.

Para especificar o direcionamento de inventário:

* Para excluir um tipo de inventário, desmarque a caixa de seleção ao lado do nome.
* Para direcionar um tipo de inventário:
   1. Marque a caixa de seleção ao lado do nome do tipo de inventário.
   1. (Opcional) Altere as origens para incluir:
      1. Clique em ![Editar](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventário) Clique em **[!UICONTROL View by Source]** ou **[!UICONTROL View by Feed]** para alterar a forma como as fontes são listadas.
      1. (Quando aplicável) Filtre o inventário conforme necessário.
      1. Especifique as fontes a serem incluídas e excluídas:
         * Para incluir uma origem [!UICONTROL Public] ou [!UICONTROL On Demand], clique em **[!UICONTROL Include]** ao lado do nome da origem.
         * Para incluir [!UICONTROL Private] fontes:
            * Para incluir todo o inventário em uma oferta, clique em **[!UICONTROL Include all]** ao lado do nome da oferta.
            * Para incluir uma origem de inventário individual, expanda o nome da negociação e clique na caixa de seleção ao lado do nome da origem.
         * Para excluir um [!UICONTROL Public] ou [!UICONTROL On source], clique em **[!UICONTROL Exclude]** ao lado do nome de origem.
   1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento para o local de Downloads do seu navegador, clique em **[!UICONTROL Save & Export]**.
   1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>Se você se inscreveu no inventário [!UICONTROL On Demand], mas não pode localizar os editores ou ofertas para o público-alvo, verifique o status das ofertas. Para obter mais informações sobre status, consulte [Sobre [!DNL On Demand] Inventário Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (somente posicionamentos de vídeo) Exclui o tráfego externo.

Anúncios de saída geralmente aparecem sobre o conteúdo como um pop-up ou recheados com conteúdo (na experiência nativa), em vez de anúncios de vídeo regulares em um reprodutor de vídeo.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** Os tipos de tráfego para direcionamento. As opções incluem **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (Disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) A qualidade do tráfego para direcionamento. As camadas 1 a 3 são seguras para suas marcas e foram aprovadas pela equipe de mapeamento da DSP.

* *[!UICONTROL Tier 1]:* sites e aplicativos Premium reconhecíveis nacionalmente.

* *[!UICONTROL Tier 2]:* Direciona a Camada 1, bem como sites e aplicativos de qualidade menos conhecidos que a Camada 1.

* *[!UICONTROL Tier 3]:* Direciona os níveis 1 e 2 além de sites e aplicativos legítimos e seguros para a marca, que atendem a um público-alvo de nicho. Use o Nível 3 para compras de alcance ou direcionamento de dados.

* *[!UICONTROL All Sites or Apps]:* Direciona as Camadas 1 a 3 e o novo inventário que não foi filtrado ou categorizado, que você pode usar para alcance.

>[!NOTE]
>
>O estoque é específico para as unidades de anúncio no posicionamento.

>[!TIP]
>
>Para campanhas de desempenho, a prática recomendada é selecionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (Opcional; disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) Categorias de site nos níveis de site selecionados para incluir ou excluir (mas não ambos) como destinos. Escolha entre as listas verticais de sites que o DSP mapeou com base no assunto:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique as categorias de site a serem incluídas ou excluídas:
   * Para incluir categorias de site:
      1. Clique em **[!UICONTROL Include categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser direcionada.
   * Para excluir categorias de site:
      1. Clique em **[!UICONTROL Exclude categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser excluída.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento para o local de Downloads do seu navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (Opcional; disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) Sites a serem excluídos. Você pode pesquisar e selecionar sites ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para pesquisar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione um nível de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites a serem excluídos:
         * Para excluir um site individual, marque a caixa de seleção adjacente.
         * (Quando mais de 50 resultados estiverem disponíveis) Para excluir os primeiros 50 resultados, clique em **[!UICONTROL Exclude these 50]**. Para excluir todos os resultados da pesquisa, clique em **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. Clique em **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Exclude All]**.
1. Clique em **[!UICONTROL Done]** quando terminar.

>[!NOTE]
>
>* Listas de sites bloqueados no nível da conta e do anunciante também são aplicadas, além da [lista de sites bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md) do DSP, que inclui sites considerados inseguros para anúncios.
>* As listas de sites bloqueados sempre substituem as listas de sites direcionados. Se uma disposição excluir e incluir o mesmo target para um anúncio, a target será excluída.

**[!UICONTROL Language]:** (Opcional) Um único idioma a ser escolhido.

**[!UICONTROL Site or App List Preview]:** (Somente leitura) Todos os sites direcionados e bloqueados para o posicionamento.

Como opção, é possível exportar a lista de sites direcionados e bloqueados como um arquivo de valores separados por vírgula (CSV). Para exportar a lista, clique em **[!UICONTROL Export full site list]** e abra ou salve o arquivo de acordo com o procedimento normal do navegador.

**[!UICONTROL Allow unscreened sites]:** (somente posicionamentos de exibição padrão) Habilita a entrega de anúncios em sites não auditados. Quando o posicionamento é direcionado ao estoque privado, essa opção pode fornecer anúncios em sites bloqueados.

**[!UICONTROL Paste list of targeted sites]:** Permite direcionar somente a sites específicos. Ao habilitar essa opção, as outras opções de direcionamento de site são desabilitadas.

**[!UICONTROL Sites]:** (Disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL On]*) Sites para direcionamento. Você pode pesquisar e selecionar sites ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para pesquisar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione um nível de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites a serem incluídos:
         * Para excluir um site individual, marque a caixa de seleção adjacente.
         * (Quando mais de 50 resultados estiverem disponíveis) Para incluir os primeiros 50 resultados, clique em **[!UICONTROL Include these 50]**. Para incluir todos os resultados da pesquisa, clique em **[!UICONTROL Include these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. clique em **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Include All]**.
1. Clique em **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Qualquer público alvo para o posicionamento, incluindo [segmentos de terceiros, segmentos primários, segmentos do Adobe, segmentos personalizados e públicos salvos](/help/dsp/audiences/audience-settings.md). O tamanho total e ativo do público-alvo desduplicado em todos os segmentos selecionados e nos públicos salvos também é exibido. Você pode selecionar um público existente, criar um público que possa ser reutilizado posteriormente ou selecionar segmentos específicos de público:

* Para selecionar um público existente, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences] e selecione o público.
* Para criar uma audiência, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences] e selecione **[!UICONTROL + Create Audience]**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), a partir da Etapa 3.
* Para selecionar segmentos específicos de público, clique em **[!UICONTROL Select segments for this placement only]**. Selecione a lógica do segmento. Para obter instruções, consulte a Etapa 6 em &quot;[Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md).&quot; Quando terminar, clique em **Salvar**.

**[!UICONTROL Excluded Audiences]:** Qualquer público-alvo a ser excluído para o posicionamento, incluindo públicos-alvo com [segmentos de terceiros, segmentos primários, segmentos do Adobe, segmentos personalizados e públicos-alvo salvos](/help/dsp/audiences/audience-settings.md). O tamanho total e ativo do público desduplicado em todos os públicos excluídos também é exibido. Você pode selecionar um público existente ou criar um novo público que poderá reutilizar posteriormente:

* Para selecionar um público existente, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences] e selecione o público.

* Para criar uma audiência, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences] e selecione **+ Criar Audiência**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), a partir da Etapa 3.

**[!UICONTROL Targeting]:** Os tipos de IDs de usuário para direcionamento. Não é possível alterar essa configuração depois que o posicionamento está ativo (ou seja, depois que o voo começou).

Ao selecionar IDs herdadas e IDs universais, a preferência de lances é dada às IDs universais.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (padrão) é direcionado a usuários com base em cookies, IDs de anúncios móveis ou IDs de TV conectada. As IDs são selecionadas com base no inventário do navegador, no aplicativo ou CTV.

* *[!UICONTROL Universal ID Beta]*: segmenta as IDs focadas na privacidade do usuário; selecione um tipo de ID. As opções disponíveis são determinadas pelos destinos geográficos selecionados na seção [!UICONTROL Geo-Targeting]. Use com [[!DNL RampID] segmentos importados diretamente para o DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segmentos para os quais o DSP converte suas PIIs em IDs universais](/help/dsp/audiences/sources/source-about.md) ou [segmentos personalizados que rastreia IDs universais](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: [!DNL ID5] IDs de Públicos-alvo criadas probabilisticamente a partir de endereços de email e outros sinais.<!-- What countries/geos are these available for? Everywhere?--> IDs ID5 estão disponíveis sem taxa. **Observação:** segmentos de terceiros de [!DNL Eyeota] podem incluir IDs ID5.

   * *[!UICONTROL RampID]*: Destina-se a [!DNL LiveRamp] [!DNL RampIDs] usuários conectados ao seu site usando seus endereços de email.<!-- Verify --> [!DNL RampIDs] estão disponíveis para usuários na América do Norte, Austrália e Nova Zelândia.

   * *[!UICONTROL Unified ID2.0]*: Destina [!DNL Unified ID2.0] (UID2) IDs de usuários conectados ao seu site usando seus endereços de email.<!-- Verify -->[!DNL UID2 IDs] não está disponível para usuários no Espaço Econômico Europeu e em alguns outros países. Consulte a [lista de países proibidos](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: os termos do contrato de serviço para usar IDs universais. Você ou outro usuário na conta do DSP deve aceitar os termos uma vez antes de converter os dados em um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta da Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **>**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Disponível quando a [campanha está configurada para segmentação entre dispositivos com base em pessoas](/help/dsp/campaign-management/campaigns/campaign-settings.md), você só segmenta IDs herdadas (não IDs universais) e seleciona pelo menos um segmento ou público. Permite estender o direcionamento em todos os dispositivos conhecidos de uma pessoa (de acordo com o gráfico de dispositivos especificado nas configurações da campanha), até mesmo dispositivos que não estão nos segmentos especificados. As tarifas podem ser aplicadas dependendo do gráfico especificado para a campanha. Os dados do gráfico de dispositivos estão disponíveis somente na América do Norte.

**[!UICONTROL Placement Cap]:** (Opcional) O número de vezes que um dispositivo exclusivo, ID universal ou pessoa (dependendo do [!UICONTROL Cross Device Level] especificado para a campanha e da configuração [!UICONTROL Targeting] do posicionamento) pode receber anúncios do posicionamento. As opções incluem *[!UICONTROL Unlimited]* ou um valor específico por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

**[!UICONTROL Secondary Cap]:** (Opcional; disponível ao incluir um [!UICONTROL Placement Cap] numérico) Uma limitação adicional dentro dos limites do limite de posicionamento principal. Selecione o número de impressões e o período de tempo (como 3 a cada 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Dias da semana e hora do dia específicos em que os anúncios podem ser executados. Para especificar intervalos dayparting:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Selecione o fuso horário aplicável.
1. Especifique os intervalos:
   * Para selecionar um intervalo predefinido, clique em um dos botões de intervalo. As opções incluem *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime).
   * Para selecionar manualmente um intervalo, clique dentro de uma célula e, como opção, arraste para selecionar o intervalo.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Opcional; disponível para anunciantes configurados com [!DNL Proximic by Comscore] segmentos) Nomes ou IDs de segmento específicos de [!DNL Proximic by Comscore] para incluir como destinos. Taxas adicionais podem ser aplicadas para este recurso. Para ativar esse recurso e configurar segmentos de tópico, entre em contato com a equipe de conta da Adobe.

Para especificar o direcionamento de tópico:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os segmentos a serem direcionados:
   1. Na coluna à esquerda, selecione o parceiro: (*[!UICONTROL Comscore]*.
   1. No campo de entrada, digite os nomes ou IDs de segmento.
1. (Opcional) Para baixar um arquivo CSV com as informações do tópico no local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>* O direcionamento de tópico limita o inventário no qual a disposição pode fazer ofertas. Portanto, use o direcionamento de tópico somente para uma pequena porcentagem da sua compra geral.
>
>* Configure qualquer direcionamento negativo dentro do segmento em [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (Opcional) Informações específicas do dispositivo, incluindo tipos de dispositivo, fabricantes, sistemas operacionais, navegadores e tipos de conectividade, a serem incluídas e excluídas como destinos. Os tipos variam de acordo com o tipo de posicionamento. Para especificar o direcionamento de dispositivo:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os detalhes do dispositivo a serem incluídos e excluídos:
   1. Na coluna à esquerda, selecione a categoria.
   1. Especificar direcionamento:
      * Para incluir um valor, clique em **[!UICONTROL Include]** ao lado do nome do valor.
      * Para excluir um valor, clique em **[!UICONTROL Exclude]** ao lado do nome do valor.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento do dispositivo no local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Provedores de serviços de Internet específicos (ISPs) a serem incluídos ou excluídos (mas não ambos) como destinos. Para especificar o direcionamento do ISP:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os ISPs a serem incluídos ou excluídos:
   * Para incluir ISPs:
      1. Clique em **[!UICONTROL Include ISPs]**.
      1. (Opcional) Filtre a lista por palavra-chave.
      1. Marque a caixa de seleção ao lado de cada ISP para direcionamento.
   * Para excluir ISPs:
      1. Clique em **[!UICONTROL Exclude ISPs]**.
      1. (Opcional) Filtre a lista por palavra-chave.
      1. Marque a caixa de seleção ao lado de cada ISP a ser excluído.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento do ISP para o local de Downloads do seu navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Opcional; somente clientes [!DNL DoubleVerify]; disponível apenas para posicionamento de vídeo e exibição padrão e click-to-play na área de trabalho; sem suporte para [posicionamentos programáticos padrão garantidos para ofertas](/help/dsp/inventory/programmatic-guaranteed-about.md)) Uma ID de segmento [!DNL DoubleVerify Authentic Brand Safety] associada à conta [!DNL DoubleVerify] da organização para usar no posicionamento. Especificar uma ID bloqueia impressões pós-oferta usando as regras personalizadas de segurança da marca configuradas para a ID do segmento especificada. A DSP fatura sua conta pelo uso da ID de segmento.

A ID deve começar com &quot;51&quot; e consistir em oito dígitos. Por padrão, se uma ID de segmento for especificada nas configurações da conta do anunciante, a ID de nível do anunciante será inserida, mas você poderá alterar a ID para usar um segmento diferente ou excluí-la para desativar o recurso.

**[!UICONTROL Contextual filtering]:** (Aplicável para exibição na Web móvel e desktop, anúncios nativos e de vídeo) Tipos de filtros contextuais [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] a serem aplicados. Os padrões no nível do anunciante são selecionados para novos posicionamentos, mas você pode alterar as configurações:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Peer 39]:

   * **Sites de destino que são:** (Opcional) Um ou mais tipos de atributos de inventário para direcionar por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL ComScore]:

   * **Bloquear sites que sejam:** (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo adulto para o qual os anúncios serão bloqueados por padrão: *[!UICONTROL Do Not Block]* (padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

   * **[!UICONTROL Alcohol Content]:** (Opcional) O grau de alcoolemia para o qual os anúncios devem ser bloqueados por padrão: *[!UICONTROL Do Not Block]* (padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sites a serem bloqueados com base em tráfego fraudulento e atividades suspeitas medidas através de [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Os padrões no nível do anunciante são selecionados para novos posicionamentos, mas você pode alterar as configurações:

* [!UICONTROL DoubleVerify]: (Aplicável para exibição na Web móvel e desktop, nativo e anúncios em vídeo) <!-- Applicable for desktop and mobile web display, native, video, and standard connected TV ads -->

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Por padrão, bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos sequestrados, para novos posicionamentos. Taxas adicionais podem ser aplicadas.

   * **[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia tráfego adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Peer 39]: (Aplicável para exibição na Web móvel e de desktop, nativo e anúncios em vídeo)

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que fazem com que o DSP bloqueie anúncios por padrão: *[!UICONTROL Fraud]* (que bloqueia todos os sites com fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/ou *[!UICONTROL Fraud: Zero Ads]*. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Integral Ad Science]: (Aplicável para exibição na Web móvel e de desktop, nativo e anúncios em vídeo)

   * **[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia anúncios baseados em atividades suspeitas), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Pre-bid viewability]:** (Aplicável para exibição na Web móvel e desktop, anúncios nativos e de vídeo) Que filtram a visibilidade antes da oferta por [!DNL DoubleVerify] e [!DNL Integral Ad Science] para aplicar ao posicionamento. Os padrões no nível do anunciante são selecionados para novos posicionamentos, mas você pode alterar as configurações. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Ads.txt filtering]:** (Aplicável para exibição na Web móvel e desktop, anúncios nativos, de vídeo e de áudio) Qual nível de [Ads.txt](https://iabtechlab.com/ads-txt-about/) filtragem de pré-oferta usar aplicando a lista de Vendedores digitais autorizados de cada fornecedor. O padrão no nível do anunciante é selecionado para novos posicionamentos, mas você pode alterar as configurações:

* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar inventário de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: priorizar a compra de estoque dos revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o estoque somente de revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de vendedores diretos autorizados de um domínio.

**[!UICONTROL Attention Targeting]:** (Aplicável para exibição na Web móvel e desktop, vídeo e anúncios de TV conectados padrão) Segmenta [!DNL Adelaide] segmentos pré-oferta com um nível de atenção específico (alto, médio ou baixo) com base no site, formato e tamanho do anúncio especificados. Os segmentos são atualizados semanalmente. **Observação:** o uso de [!DNL Adelaide] segmentos para direcionamento incorre em uma taxa do CPM para cada impressão entregue com [!DNL Adelaide] direcionamento de atenção; esta taxa é separada das taxas para [medição de atenção](/help/dsp/campaign-management/campaigns/campaign-settings.md). Para inserções interativas antes da exibição, você é cobrado apenas por impressões VAST.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] posicionamentos) Os fornecedores de rastreamento de terceiros aprovados por [!DNL Roku] incluem [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] e [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (opcional) pixels de rastreamento de eventos de terceiros a serem anexados por padrão a todos os novos anúncios no posicionamento. Para especificar pixels de evento:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para selecionar um pixel existente, marque a caixa de seleção na linha de pixels.
   * Para criar um pixel:
      1. Clique em **[!UICONTROL Create]**.
      1. Insira as seguintes informações:
         * **[!UICONTROL Pixel name]:** O nome do pixel; o comprimento máximo é de 500 caracteres. Use um nome que ajude a identificar facilmente o pixel.
         * **[!UICONTROL Pixel event fires on]:** O evento que aciona o pixel. Os eventos disponíveis variam de acordo com o tipo de anúncio.
         * **[!UICONTROL Pixel type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem de 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** A URL da imagem pixel.
      1. Clique em **[!UICONTROL Create and attach]**.
   1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Opcional) Rastreamento de conversão de pixels para anexar por padrão a todos os novos anúncios no posicionamento. Para especificar os pixels de conversão:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para selecionar um pixel existente, marque a caixa de seleção na linha de pixels.
   * Para criar um pixel:
      1. Clique em **[!UICONTROL Create]**.
      1. Insira as seguintes informações:
         * **[!UICONTROL Conversion pixel name]:** O nome do pixel; o comprimento máximo é de 500 caracteres. Use um nome que ajude a identificar facilmente o pixel.
         * **[!UICONTROL Conversion category]:** O tipo de conversão.
         * **[!UICONTROL Impression conversion window]:** O número de dias após a ocorrência de uma impressão de anúncio em que a impressão pode ser atribuída a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Click conversion window]:** O número de dias após um clique de anúncio, nos quais o clique pode ser atribuído a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Notes]:** (Opcional) Uma descrição ou outra informação sobre o pixel.
      1. Clique em **[!UICONTROL Create and attach]**.
      1. Implemente o pixel de conversão nas páginas da Web relevantes:
         1. No menu principal, vá para **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Na linha de pixels, clique em **[!UICONTROL edit]**.
         1. Copie o(s) valor(es) nos campos [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag], conforme necessário, para fornecer ao anunciante ou contato do site.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.
   1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Uma taxa de taxa de terceiros estática para ser rastreada como um custo não faturável por 1000 impressões. O padrão no nível do pacote é aplicado automaticamente para novos posicionamentos, quando aplicável, a menos que você insira um valor diferente.

>[!NOTE]
>
>Taxas faturáveis são refletidas na métrica [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Posicionamento](placement-about.md)
>* [Criar um posicionamento](placement-create.md)
>* [Editar posicionamentos](placement-edit.md)
>* [Gerenciar multiplicadores de oferta para posicionamentos](placement-manage-bid-multipliers.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Perguntas frequentes sobre o gerenciamento de campanhas](/help/dsp/campaign-management/faq-campaign-management.md)
