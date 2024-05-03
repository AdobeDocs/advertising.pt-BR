---
title: Configurações de posicionamento
description: Consulte descrições das configurações de posicionamento disponíveis.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: caab8c3163a7ffdbc0b5ef28176b2ee73f83b6e8
workflow-type: tm+mt
source-wordcount: '3540'
ht-degree: 0%

---

# Configurações de posicionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** O nome do posicionamento.

>[!TIP]
>Use uma convenção de nomenclatura que faça sentido para a sua situação. Uma convenção de nomenclatura sugerida é &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** O status do posicionamento: *[!UICONTROL Active]* (o padrão) ou *[!UICONTROL Paused]*.

>[!TIP]
>A prática recomendada é pausar o posicionamento até que você esteja pronto para iniciá-lo.

**[!UICONTROL Details]:** (Somente leitura) O tipo de anúncio aplicável, a conta que está criando ou criou o posicionamento e a campanha principal. Para ver mais detalhes, clique em **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Abre uma lista de modelos de posicionamento existentes. Para preencher automaticamente as configurações de direcionamento a partir de um modelo:

1. Siga um destes procedimentos:

   * Para reutilizar todos os alvos de um modelo, marque a caixa de seleção ao lado do nome do modelo.

   * Para reutilizar tipos de alvo individuais de um modelo, expanda o nome do modelo e marque a caixa de seleção ao lado dos tipos de alvo que deseja reutilizar.

1. Clique em **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Somente formatos de anúncio de vídeo) A duração do anúncio e/ou as especificações do anúncio, que são usadas para calcular a projeção da Previsão à direita. Os campos variam de acordo com o tipo de anúncio.

**[!UICONTROL Environment]:** (Somente formato de anúncio de vídeo universal) Os ambientes do dispositivo (desktop, dispositivo móvel, TV conectada) a serem incluídos como destinos no posicionamento. Especifique pelo menos um.

Nos relatórios personalizados, a dimensão no nível de posicionamento &quot;Ambiente do dispositivo&quot; indica o ambiente direcionado.

**[!UICONTROL Placement tags]:** (Opcional) Palavras-chave ou apelidos para ajudar a localizar este posicionamento.

## Metas

**[!UICONTROL Package]:** (Opcional) Um pacote ao qual o posicionamento é atribuído. Clique em ![Editar](/help/dsp/assets/edit.png) para selecionar um pacote existente ou criar um pacote. Ao atribuir o posicionamento a um pacote, a variável [!UICONTROL Goals] A seção é atualizada com as datas de voo, a meta do delivery e o orçamento do pacote.

**[!UICONTROL Flight Dates]:** A data inicial e a data final do posicionamento. Os anúncios aprovados estão qualificados para execução durante o voo quando a inserção estiver ativa e atribuída a um pacote ou campanha ativa.

As datas do pacote (quando aplicável) ou da campanha são preenchidas automaticamente por padrão.

>[!NOTE]
>
>* As datas de voo devem ser incluídas nas datas de voo da campanha e nas datas de voo do pacote.

### Posicionamentos atribuídos a pacotes com ritmo no nível do pacote

**[!UICONTROL Placement Funding]:** Como fazer o orçamento do posicionamento:

* *[!UICONTROL Optimize based on performance]:* Controla o orçamento no nível do pacote.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Permite definir um orçamento de posicionamento mínimo e/ou máximo. Especifique pelo menos um tipo de orçamento:

   * *[!UICONTROL Maximum Budget]*: insira um valor e a duração (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: o orçamento mínimo como uma porcentagem do orçamento do pacote. Quando um limite de intervalo é especificado, o valor de orçamento mínimo é sempre calculado como uma porcentagem do limite de intervalo. Caso contrário, será calculado como uma porcentagem do orçamento do pacote.

**[!UICONTROL Max Bid]:** O máximo a pagar por 1000 impressões.

**[!UICONTROL Placement Pre-bid Filters]:** Até cinco limites de KPI (como uma métrica de visibilidade mínima ou taxa de cliques) que devem ser atingidos para que o lance ocorra. Você pode usar filtros de pré-oferta como táticas de otimização, mas entende que cada regra pode limitar as oportunidades nas quais esse posicionamento pode fazer ofertas. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

Consulte as descrições de cada filtro de pré-oferta em &quot;[Filtros pré-oferta no nível de posicionamento e como usá-los](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Todas as outras disposições

**[!UICONTROL Budget Goal]:** O limite orçamentário bruto e o intervalo orçamentário (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Posicionamentos em campanhas somente com gerenciamento de margem) O limite de orçamento bruto e o intervalo de orçamento (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  A meta de otimização do pacote. Consulte as descrições de cada meta de otimização em &quot;[Metas de otimização e como usá-las](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** A meta, que é usada para monitorar o desempenho.

>[!NOTE]
>
>Este campo é apenas um referencial e não é usado para decisões.

**[!UICONTROL Pace on]:** A base para o ritmo:

* **[!UICONTROL Budget goal]:** (Padrão) Essa opção fornece o máximo de impressões possível dentro do orçamento alocado.

* **[!UICONTROL Impressions]:** Essa opção fornece impressões até que uma quantidade especificada seja atingida em um intervalo especificado. Ao selecionar essa opção, especifique o número de impressões e o intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** O máximo a pagar por 1000 impressões.

**[!UICONTROL Flight pacing]:** (Posicionamentos com ritmo de nível de posicionamento somente) Como programar e entregar:

* *[!UICONTROL Even]:* (O padrão) Acompanha o delivery uniformemente em cada voo, com uma meta de 50% do delivery na primeira metade do voo.

* *[!UICONTROL Slightly Ahead]:* (O padrão) Acelera a entrega para que esteja 55 a 65% concluído na metade da duração do voo.

* *[!UICONTROL Frontload]:* Acelera a entrega para que esteja 65 a 75% concluído na metade do voo.

* *[!UICONTROL Aggressive Frontload]:* Acelera a entrega para que esteja 75 a 85% concluído na metade do voo.

**[!UICONTROL Intraday pacing]:** (Posicionamentos com ritmo de nível de posicionamento somente) Como acompanhar e entregar em cada dia no voo:

* *[!UICONTROL Even]:* (O padrão) Dimensiona a entrega com base na disponibilidade do inventário. Geralmente, mais anúncios são entregues por hora durante o dia, quando o volume do leilão é maior, e menos anúncios são entregues de manhã e à noite.

* *[!UICONTROL ASAP]:* (O padrão) Acelera a entrega para o dobro da velocidade de *Par*.

  >[!CAUTION]
  >
  >Essa opção pode afetar negativamente o desempenho. Use-a somente quando estiver priorizando totalmente o delivery e o gasto em relação à otimização de desempenho.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Até cinco filtros que devem ser atendidos para que os lances ocorram. Você pode usar filtros de pré-oferta como táticas de otimização, mas lembre-se de que cada regra pode limitar as oportunidades nas quais esse posicionamento pode licitar. Para adicionar ou editar filtros:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para adicionar um filtro:
      1. Clique em **[!UICONTROL Add Filter]**.
      1. Ao lado de **[!UICONTROL Only bid if]**, selecione uma métrica e insira um valor.
   * Para remover um filtro, clique em **[!UICONTROL X]** na linha de filtro.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Opcional) Locais específicos onde incluir ou excluir anúncios no posicionamento. Se você não especificar nenhum local, todos os locais serão direcionados.

>[!NOTE]
>
>Os locais de cidade e DMA não estão disponíveis para inserções do Roku.

Para especificar locais:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para incluir ou excluir um País, Estado, Cidade, DMA, Distrito Legislativo Federal ou Distrito Legislativo Estadual:
      1. Selecione o tipo de local na coluna à esquerda.
      1. (Conforme necessário) Clique em um local para expandi-lo.
      1. Ao lado do local, clique em *[!UICONTROL Include]* para incluí-lo como um target ou *[!UICONTROL Exclude]* para excluí-lo como um target.
   * Para pesquisar um código postal e incluir ou excluir todos os resultados selecionados:
      1. Clique em **[!UICONTROL Search Postal Code]**.
      1. Selecione o país.
      1. Insira o nome da cidade e clique em ![Editar](/help/dsp/assets/search.png).
      1. Clique no resultado de pesquisa correto.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como alvos ou *[!UICONTROL Exclude All]* para excluir todos os locais como destinos.
   * Para informar ou colar códigos postais e incluir ou excluir todos eles:
      1. Clique em **[!UICONTROL Paste Postal Code]**.
      1. Selecione o país.
      1. Insira ou cole até 1000 códigos postais.
Inclua um código postal por linha ou insira vários valores separados por vírgulas ou guias.
      1. Clique em *[!UICONTROL Include All]* para incluir todos os locais como alvos ou *[!UICONTROL Exclude All]* para excluir todos os locais como destinos.
   * Para remover um local da lista [!UICONTROL Included] ou [!UICONTROL Excluded] clique em **[!UICONTROL X]** ao lado do local na coluna à direita.
1. Clique em **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nem todos os países têm localizações de Estado, Cidade ou Código Postal.
>* O DMA (área de mercado designada), os Distritos Legislativos Federais e os Distritos Legislativos Estaduais estão disponíveis somente para locais nos EUA.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Origens de inventário a serem incluídas ou excluídas como destinos. Para a maioria dos tipos de posicionamento, todos os tipos de inventário e todas as origens para cada tipo são incluídos por padrão. Para [!DNL Roku] posicionamentos, você deve especificar o tipo de inventário e as origens. Você pode escolher entre os seguintes tipos de inventário:

* [!UICONTROL Public]: (Todos os tipos de posicionamento, exceto Roku) Todos os inventários de intercâmbio aberto aos quais o DSP tem acesso. Você pode incluir e excluir inventário público.

  Você pode visualizar a lista por fonte ou por feed. Ao visualizar a lista por feed, você pode pesquisar por nome do feed, chave do feed ou uma tag característica selecionada.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: suas ofertas privadas existentes (ou ofertas privadas existentes), [!DNL Roku] ofertas para [!DNL Roku] posicionamentos) com editores configurados no DSP. Você pode incluir, mas não excluir, inventário público.

  Você pode pesquisar a lista por palavra-chave, chave, ID de negócio ou tag personalizada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) Substitui o algoritmo de preço de compra para oferecer pelo menos os preços fixo e mínimo para as negociações.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Todos [prêmio, não garantido [!UICONTROL On Demand] inventário](/help/dsp/inventory/on-demand-inventory-about.md) (ou [!UICONTROL On Demand] [!DNL Roku] ofertas para [!DNL Roku] posicionamentos) nos quais você se inscreveu [!DNL DSP]. É possível incluir e excluir [!UICONTROL On Demand] inventário.

  Você pode visualizar a lista por fonte ou por feed. Ao visualizar a lista por feed, você pode pesquisar por nome do feed, chave do feed ou uma região do editor, tag de categoria ou tag característica selecionada.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Opcional) Substitui o algoritmo de preço de compra para oferecer pelo menos os preços fixo e mínimo para as negociações.

Para especificar o direcionamento de inventário:

* Para excluir um tipo de inventário, desmarque a caixa de seleção ao lado do nome.
* Para direcionar um tipo de inventário:
   1. Marque a caixa de seleção ao lado do nome do tipo de inventário.
   1. (Opcional) Altere as origens para incluir:
      1. Clique em ![Editar](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventário) Clique em **[!UICONTROL View by Source]** ou **[!UICONTROL View by Feed]** para alterar como as origens são listadas.
      1. (Quando aplicável) Filtre o inventário conforme necessário.
      1. Especifique as fontes a serem incluídas e excluídas:
         * Para incluir um [!UICONTROL Public] ou [!UICONTROL On Demand] origem, clique em **[!UICONTROL Include]** ao lado do nome de origem.
         * Para incluir [!UICONTROL Private] fontes:
            * Para incluir todo o inventário em um negócio, clique em **[!UICONTROL Include all]** ao lado do nome do contrato.
            * Para incluir uma origem de inventário individual, expanda o nome da negociação e clique na caixa de seleção ao lado do nome da origem.
         * Para excluir um [!UICONTROL Public] ou [!UICONTROL On source], clique em **[!UICONTROL Exclude]** ao lado do nome de origem.
   1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento no local de Downloads do navegador, clique em **[!UICONTROL Save & Export]**.
   1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>Se você se inscreveu no [!UICONTROL On Demand] inventário, mas não for possível localizar os editores ou as negociações para direcionamento e, em seguida, verificar o status das negociações. Para obter mais informações sobre status, consulte [Sobre [!DNL On Demand] Inventário Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Somente inserções de vídeo) Exclui o tráfego externo.

Anúncios de saída geralmente aparecem sobre o conteúdo como um pop-up ou recheados com conteúdo (na experiência nativa), em vez de anúncios de vídeo regulares em um reprodutor de vídeo.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Os tipos de tráfego a serem direcionados. As opções incluem **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) A qualidade dos sites a serem direcionados. As camadas 1 a 3 são seguras para a marca e foram verificadas e aprovadas pela equipe de mapeamento do DSP.

* *[!UICONTROL Tier 1]:* Sites e aplicativos premium reconhecidos nacionalmente.

* *[!UICONTROL Tier 2]:* Tem como alvo o Nível 1, bem como sites e aplicativos de qualidade menos conhecidos do que o Nível 1.

* *[!UICONTROL Tier 3]:* Segmenta níveis de 1 a 2, além de sites e aplicativos legítimos e seguros para a marca, que atendem a um público-alvo de nicho. Use o Nível 3 para compras de alcance ou direcionamento de dados.

* *[!UICONTROL All Sites]:* Segmenta níveis 1 a 3 e novo inventário que não foi filtrado ou categorizado, que você pode usar para alcance.

>[!NOTE]
>
>O estoque é específico para as unidades de anúncio no posicionamento.

>[!TIP]
>
>Para campanhas de desempenho, a prática recomendada é selecionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Opcional; disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) Categorias de site nos níveis de site selecionados para incluir ou excluir (mas não ambos) como alvos. Escolha nas listas verticais de sites que o DSP mapeou com base no assunto:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique as categorias de site a serem incluídas ou excluídas:
   * Para incluir categorias de site:
      1. Clique em **[!UICONTROL Include categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser direcionada.
   * Para excluir categorias de site:
      1. Clique em **[!UICONTROL Exclude categories]**.
      1. Marque a caixa de seleção ao lado de cada categoria a ser excluída.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento no local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Opcional; disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL Off]*) Sites a serem excluídos. Você pode pesquisar e selecionar sites ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para pesquisar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione um nível de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites a serem excluídos:
         * Para excluir um site individual, marque a caixa de seleção ao lado dele.
         * (Quando mais de 50 resultados estiverem disponíveis) Para excluir os primeiros 50 resultados, clique em **[!UICONTROL Exclude these 50]**. Para excluir todos os resultados da pesquisa, clique em **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. Clique em **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Exclude All]**.
1. Clique em **[!UICONTROL Done]** quando terminar.

>[!NOTE]
>
>* Listas de sites bloqueados no nível da conta e do anunciante também são aplicadas, além do DSP [lista de sites bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md), que inclui sites considerados inseguros para anúncios.
>* As listas de sites bloqueados sempre substituem as listas de sites direcionados. Se uma disposição excluir e incluir o mesmo target para um anúncio, a target será excluída.

**[!UICONTROL Language]:** (Opcional) Um único idioma a ser direcionado.

**[!UICONTROL Site List Preview]:** (Somente leitura) Todos os sites direcionados e bloqueados para o posicionamento.

Como opção, é possível exportar a lista de sites direcionados e bloqueados como um arquivo de valores separados por vírgula (CSV). Para exportar a lista, clique em **[!UICONTROL Export full site list]** e, em seguida, abra ou salve o arquivo de acordo com o procedimento normal do navegador.

**[!UICONTROL Allow unscreened sites]:** (Somente disposições de exibição padrão) Permite a entrega de anúncios em sites não auditados. Quando o posicionamento é direcionado ao estoque privado, essa opção pode fornecer anúncios em sites bloqueados.

**[!UICONTROL Paste list of targeted sites]:** Permite direcionar somente a sites específicos. Ao habilitar essa opção, as outras opções de direcionamento de site são desabilitadas.

**[!UICONTROL Sites]:** (Disponível quando **[!UICONTROL Paste list of targeted sites]** é *[!UICONTROL On]*) Sites para direcionar. Você pode pesquisar e selecionar sites ou inserir ou colar nomes de domínio:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os sites:
   * Para pesquisar um site:
      1. Clique em **[!UICONTROL Search]**.
      1. Insira uma palavra-chave, selecione um nível de site e/ou selecione uma categoria de site.
      1. Nos resultados da pesquisa, selecione os sites a serem incluídos:
         * Para excluir um site individual, marque a caixa de seleção ao lado dele.
         * (Quando mais de 50 resultados estiverem disponíveis) Para incluir os primeiros 50 resultados, clique em **[!UICONTROL Include these 50]**. Para incluir todos os resultados da pesquisa, clique em **[!UICONTROL Include these \<*NN *\>]**.
   * Para inserir nomes de domínio:
      1. click **[!UICONTROL Paste]**.
      1. Insira um ou mais nomes de domínio em linhas separadas.
      1. Clique em **[!UICONTROL Include All]**.
1. Clique em **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Quaisquer públicos-alvo para a inserção, incluindo [segmentos de terceiros, segmentos primários, segmentos de Adobe, segmentos personalizados e públicos salvos](/help/dsp/audiences/audience-settings.md). O tamanho total e ativo do público-alvo desduplicado em todos os segmentos selecionados e nos públicos salvos também é exibido. Você pode selecionar um público existente, criar um público que possa ser reutilizado posteriormente ou selecionar segmentos específicos de público:

* Para selecionar um público existente, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences]e selecione o público.
* Para criar um público, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Included Audiences]e selecione **[!UICONTROL + Create Audience]**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), começando com a Etapa 3.
* Para selecionar segmentos específicos de público, clique em **[!UICONTROL Select segments for this placement only]**. Selecione a lógica do segmento. Para obter instruções, consulte Etapa 6 em &quot;[Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md).&quot; Quando terminar, clique em **Salvar**.

**[!UICONTROL Excluded Audiences]:** Quaisquer públicos-alvo a serem excluídos para o posicionamento, incluindo públicos-alvo com [segmentos de terceiros, segmentos primários, segmentos de Adobe, segmentos personalizados e públicos salvos](/help/dsp/audiences/audience-settings.md). O tamanho total e ativo do público desduplicado em todos os públicos excluídos também é exibido. Você pode selecionar um público existente ou criar um novo público que poderá reutilizar posteriormente:

* Para selecionar um público existente, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences]e selecione o público.
* Para criar um público, clique em ![Selecionar](/help/dsp/assets/chevron-down.png) ao lado de [!UICONTROL Excluded Audiences]e selecione **+ Criar público-alvo**. Para obter instruções, consulte [Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md), começando com a Etapa 3.
* Para selecionar segmentos específicos de público, clique em **[!UICONTROL Select segments for this placement only]**. Selecione a lógica do segmento. Para obter instruções, consulte Etapa 6 em &quot;[Criar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-create.md).&quot; Quando terminar, clique em **Salvar**.

**[!UICONTROL Cross Device Targeting]:** (Disponível quando você seleciona pelo menos um segmento ou público-alvo e [o campaign está configurado para direcionamento entre dispositivos com base em pessoas](/help/dsp/campaign-management/campaigns/campaign-settings.md). Permite estender o direcionamento em todos os dispositivos conhecidos de uma pessoa (de acordo com o gráfico de dispositivos especificado nas configurações da campanha), até mesmo dispositivos que não estão nos segmentos especificados. As tarifas podem ser aplicadas dependendo do gráfico especificado para a campanha. Os dados do gráfico de dispositivos estão disponíveis somente na América do Norte.

**[!UICONTROL Placement Cap]:** (Opcional) O número de vezes que um dispositivo ou pessoa única (dependendo do [!UICONTROL Cross Device Level] para a campanha) são anúncios veiculados a partir do posicionamento. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

**[!UICONTROL Secondary Cap]:** (Opcional; disponível ao incluir uma variável numérica [!UICONTROL Placement Cap]) Uma limitação adicional dentro dos limites do limite de posicionamento principal. Selecione o número de impressões e o período de tempo (como 3 a cada 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Dias específicos da semana e hora do dia em que os anúncios podem ser executados. Para especificar intervalos dayparting:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Selecione o fuso horário aplicável.
1. Especifique os intervalos:
   * Para selecionar um intervalo predefinido, clique em um dos botões de intervalo. As opções incluem *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime) (em inglês).
   * Para selecionar manualmente um intervalo, clique dentro de uma célula e, como opção, arraste para selecionar o intervalo.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Opcional; disponível para anunciantes configurados com [!DNL Comscore] e [!DNL Grapeshot] segmentos) Nomes de segmentos ou IDs específicos de [!DNL Comscore] e [!DNL Grapeshot] para incluir como targets. Taxas adicionais podem ser aplicadas para este recurso. Para ativar esse recurso e configurar segmentos de tópico, entre em contato com a equipe de conta do Adobe.

Para especificar o direcionamento de tópico:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os segmentos a serem direcionados:
   1. Na coluna à esquerda, selecione o parceiro (*[!UICONTROL Comscore]* ou *[!UICONTROL Grapeshot]*).
   1. No campo de entrada, digite os nomes ou IDs de segmento.
1. (Opcional) Para baixar um arquivo CSV com as informações do tópico no local Downloads do seu navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

>[!TIP]
>
>* O direcionamento de tópico limita o inventário no qual a disposição pode fazer ofertas. Portanto, use o direcionamento de tópico somente para uma pequena porcentagem da sua compra geral.
>
>* Configurar qualquer direcionamento negativo no segmento em [!DNL Comscore] ou [!DNL Grapeshot].

**[!UICONTROL Device Targeting]:** (Opcional) Informações específicas do dispositivo, incluindo tipos de dispositivo, fabricantes, sistemas operacionais, navegadores e tipos de conectividade, a serem incluídas e excluídas como destinos. Para especificar o direcionamento de dispositivo:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Especifique os detalhes do dispositivo a serem incluídos e excluídos:
   1. Na coluna à esquerda, selecione a categoria.
   1. Especificar direcionamento:
      * Para incluir um valor, clique em **[!UICONTROL Include]** ao lado do nome do valor.
      * Para excluir um valor, clique em **[!UICONTROL Exclude]** ao lado do nome do valor.
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento do dispositivo no local de Downloads do navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Provedores de serviços de internet específicos (ISPs) a serem incluídos ou excluídos (mas não ambos) como alvos. Para especificar o direcionamento do ISP:

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
1. (Opcional) Para baixar um arquivo CSV com as informações de direcionamento do ISP no local de Downloads do seu navegador, clique em **[!UICONTROL Export]**.
1. Clique em **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39] filtros contextuais a serem aplicados. Os padrões no nível do anunciante são selecionados para novos posicionamentos, mas você pode alterar as configurações:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de contexto de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Peer 39]:

   * **Sites de destino que são:** (Opcional) Um ou mais tipos de atributos de inventário para segmentar por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL ComScore]:

   * **Bloquear sites que são:** (Opcional) Um ou mais tipos de atributos de inventário a serem bloqueados por padrão. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) O grau de conteúdo para adultos para o qual os anúncios devem ser bloqueados por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

   * **[!UICONTROL Alcohol Content]:** (Opcional) O grau de teor de álcool para o qual os anúncios são bloqueados por padrão: *[!UICONTROL Do Not Block]* (o padrão), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sites a serem bloqueados com base em tráfego fraudulento e atividades suspeitas medidas por [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39]. Os padrões no nível do anunciante são selecionados para novos posicionamentos, mas você pode alterar as configurações:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Por padrão, o bloqueia todo o tráfego 100% inválido, incluindo o tráfego em dispositivos sequestrados, para novos posicionamentos. Taxas adicionais podem ser aplicadas.

   * **[!UICONTROL Also block sites with]:** (Opcional) Um nível adicional de fraude e tráfego inválido que faz com que o DSP bloqueie anúncios por padrão:  *[!UICONTROL None]* (o padrão, que não bloqueia o tráfego adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um ou mais tipos de fraude que fazem com que o DSP bloqueie anúncios por padrão: *[!UICONTROL Fraud]* (que bloqueia todos os sites com fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, e/ou *[!UICONTROL Fraud: Zero Ads]*. Taxas adicionais podem ser aplicadas.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Um tipo de atividade suspeita de site ou aplicativo que faz com que o DSP bloqueie anúncios por padrão: *[!UICONTROL None]* (o padrão, que não bloqueia anúncios com base em atividades suspeitas), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Taxas adicionais podem ser aplicadas.

**[!UICONTROL Ads.txt filtering]:**

Qual nível de [Anúncios.txt](https://iabtechlab.com/ads-txt-about/) filtragem pré-oferta a ser usada aplicando a lista de Vendedores digitais autorizados de cada editor. O padrão no nível do anunciante é selecionado para novos posicionamentos, mas você pode alterar as configurações:

* *[!UICONTROL Opt out of ads.txt (default)]*: para comprar o inventário de todos os vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: para priorizar a compra de estoque dos vendedores diretos e revendedores autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de revendedores e vendedores diretos autorizados de um domínio.
* *[!UICONTROL Ads.txt sellers only]*: para comprar o inventário somente de vendedores diretos autorizados de um domínio.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Anunciantes configurados com o [!UICONTROL DoubleVerify Authentic Brand Safety] option) Habilita [!DNL DoubleVerify Authentic Brand Safety], que bloqueia impressões pós-oferta usando as regras de segurança da marca personalizada configuradas para a ID de segmento especificada. O DSP fatura sua conta pelo uso da ID de segmento especificada nas configurações do anunciante.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] posicionamentos) Fornecedores de rastreamento de terceiros aprovados por [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], e [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Opcional) pixels de rastreamento de eventos de terceiros a serem anexados por padrão a todos os novos anúncios no posicionamento. Para especificar pixels de evento:

1. Clique em ![Editar](/help/dsp/assets/edit.png).
1. Siga um destes procedimentos:
   * Para selecionar um pixel existente, marque a caixa de seleção na linha de pixels.
   * Para criar um pixel:
      1. Clique em **[!UICONTROL Create]**.
      1. Insira as seguintes informações:
         * **[!UICONTROL Pixel name]:** O nome do pixel; o comprimento máximo é de 500 caracteres. Use um nome que ajude a identificar facilmente o pixel.
         * **[!UICONTROL Pixel event fires on]:** O evento que aciona o pixel para ser acionado. Os eventos disponíveis variam de acordo com o tipo de anúncio.
         * **[!UICONTROL Pixel type]:** Se o pixel é um *[!UICONTROL IMG URL]* (arquivo de imagem com 1x1 pixels), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.
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
         * **[!UICONTROL Impression conversion window]:** O número de dias após a impressão de um anúncio em que a impressão pode ser atribuída a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Click conversion window]:** O número de dias após um clique de anúncio, nos quais o clique pode ser atribuído a uma conversão. O padrão é 30 dias.
         * **[!UICONTROL Notes]:** (Opcional) Uma descrição ou outras informações sobre o pixel.
      1. Clique em **[!UICONTROL Create and attach]**.
      1. Implemente o pixel de conversão nas páginas da Web relevantes:
         1. No menu principal, acesse **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Na linha pixel, clique em **[!UICONTROL edit]**.
         1. Copie os valores na variável [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag] campos, conforme necessário, para fornecer ao anunciante ou contato do site.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.
   1. Clique em **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Uma taxa de taxa de terceiros estática que deve ser rastreada como um custo não faturável por 1000 impressões. O padrão no nível do pacote é aplicado automaticamente para novos posicionamentos, quando aplicável, a menos que você insira um valor diferente.

>[!NOTE]
>
>As taxas faturáveis são refletidas na [!UICONTROL Net CPM] métrica.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de posicionamento](placement-about.md)
>* [Criar uma disposição](placement-create.md)
>* [Editar uma disposição](placement-edit.md)
>* [Gerenciar multiplicadores de oferta para disposições](placement-manage-bid-multipliers.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Perguntas frequentes sobre o Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
