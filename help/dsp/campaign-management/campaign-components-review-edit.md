---
title: Revisar e editar configurações do componente de campanha usando bulksheets
description: Saiba como revisar e editar o pacote de chaves, a disposição e as configurações de anúncio em massa usando planilhas.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Revisar e editar configurações do componente de campanha usando bulksheets

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

É possível baixar as configurações dos pacotes, posicionamentos e anúncios em uma única campanha no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. Por padrão, o arquivo baixado inclui guias separadas para configurações de pacote, informações de voo do pacote, configurações de posicionamento e agendamentos de anúncios de posicionamento. Opcionalmente, é possível excluir as configurações de alguns tipos de componentes da campanha.

Para atualizar várias configurações de uma só vez, carregue um arquivo de bulksheet válido com as alterações. Para criar a planilha em massa, você pode baixar um modelo de planilha em branco que inclui guias para cada tipo de componente da campanha, inserir ou colar configurações novas ou atualizadas no arquivo de modelo e salvar o arquivo para carregá-lo. Os campos editáveis incluem a maioria das configurações que normalmente são editáveis.

>[!NOTE]
>
>Também é possível baixar e editar as configurações somente para pacotes e disposições específicos. Consulte &quot;[Revisar e Editar Configurações de Pacote Usando Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)&quot; e &quot;[Revisar e Editar Configurações de Posicionamento Usando Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)&quot;.&quot;

## Configurações de download para pacotes, disposições e anúncios em uma campanha

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Na caixa de diálogo [!UICONTROL QA Sheet Download], desmarque todos os componentes da campanha cujas configurações você deseja excluir do arquivo baixado e clique em **[!UICONTROL Download]**.

Por padrão, as configurações para todos os componentes da campanha são selecionadas.

Uma mensagem de notificação indica quando o arquivo está disponível para download.

1. Para baixar o arquivo, siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

     O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

>[!NOTE]
>
>Você não pode editar e recarregar arquivos de controle de qualidade no nível da campanha. Para alterar as configurações do componente de campanha nesses arquivos, [baixe um arquivo de modelo de configurações separado (arquivo de configuração)](#download-template), insira ou cole linhas do arquivo de controle de qualidade no modelo e salve o arquivo e [carregue o arquivo de modelo preenchido](#upload-bulksheet-campaign-components).

## Baixar um modelo de bulksheet para uma campanha {#download-template}

Baixe um modelo de bulksheet em branco que inclui guias para cada tipo de componente de campanha. Posteriormente, você pode adicionar linhas a qualquer guia no modelo e [carregar o arquivo editado](##upload-bulksheet-campaign-components) para fazer alterações nos componentes da campanha.

1. Clique no nome da campanha.

1. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Na caixa de diálogo [!UICONTROL Upload Bulksheet], clique em **[!UICONTROL Bulksheet Template].**

   O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

## Fazer upload de um Bulksheet com configurações de pacote, posicionamento e anúncios para uma campanha{#upload-bulksheet-campaign-components}

Faça upload das configurações para pacotes, disposições e anúncios em uma única campanha, tudo de uma só vez em uma bulksheet preenchida.

1. [Baixe um modelo de bulksheet](#download-template) se necessário, insira ou cole configurações de pacote, posicionamento e/ou anúncio nas guias relevantes de um modelo de bulksheet e salve o arquivo no seu dispositivo ou rede.

   Consulte as configurações disponíveis abaixo.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. No diálogo [!UICONTROL Upload Bulksheet]:

   1. Arraste e solte um arquivo na caixa ou clique dentro dela para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

1. (Opcional) Para verificar se as atualizações foram processadas, clique em ![Trabalhos](/help/dsp/assets/downloads.png) à direita da barra de menu superior.

## Colunas de configuração de posicionamento em planilhas baixadas/carregadas{#qa-sheet-columns}

>[!TIP]
>
> Em uma planilha baixada, todas as colunas editáveis são destacadas em azul.

### Planilhas de nível de campanha

| Seção | Coluna | Descrição | Editável? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | A ID numérica do posicionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | O nome do posicionamento. | Sim |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Quaisquer rótulos aplicados, para relatórios. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Um link para abrir a disposição no modo de Edição. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | O status do posicionamento: *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Sim |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | O tipo de posicionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | O nome do pacote principal, quando aplicável. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | A data de início do posicionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | A data final do posicionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Se dayparting é *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Observação:</b> para verificar a agenda atual de dayparting, abra as configurações de posicionamento no DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | O orçamento de posicionamento, se houver. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | O intervalo de orçamento: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | O objetivo do pacote. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | O valor de destino da meta. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Se o posicionamento está se aproximando de *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | O lance máximo para a inserção. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | A estratégia de ritmo de voo para o posicionamento: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | A estratégia de ritmo intradiário para o posicionamento: *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Quaisquer critérios de filtro pré-oferta a serem aplicados. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Se as regras de licitação (obsoletas) são *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | O limite de frequência primária para o posicionamento durante o [!UICONTROL Frequency Cap Interval] especificado. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | O intervalo para o limite de frequência primária: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundário para o posicionamento durante o [!UICONTROL Secondary Frequency Cap Interval] especificado | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundário: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pelo [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos aos quais o [!UICONTROL Secondary Frequency Cap] se aplica. Por exemplo, se o limite secundário for de três impressões a cada seis horas, o valor aqui será `6`. | Sim |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | O número de localizações geográficas de destino, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | As localizações geográficas de destino, separadas por ponto e vírgula ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | O número de localizações geográficas excluídas ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | As localizações geográficas excluídas, separadas por ponto e vírgula ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | O número de ofertas de estoque público direcionadas, se houver, são especificadas: *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | O número de negociações de estoque público excluídas, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | O número de ofertas de estoque privado direcionadas, se alguma for especificada, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | O número de ofertas de estoque privado excluídas, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | O número de ofertas de [!UICONTROL On-Demand Inventory] alvos, se alguma for especificada, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | O número de ofertas de Estoque por Demanda excluídas, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | O tipo de tráfego direcionado: *[!UICONTROL Website]* e/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Se a opção de Direcionamento de Inventário para excluir o tráfego externo é &lt;i[!UICONTROL >ON]* ou *[!UICONTROL OFF]*.<br>Anúncios de saída geralmente aparecem sobre o conteúdo como um pop-up ou recheados em conteúdo (na experiência nativa), em vez de anúncios de vídeo comuns em um player de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | A qualidade dos sites a serem direcionados: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | O número de categorias de site de destino, se houver, especificado, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | O número de categorias de site excluídas, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Os sites excluídos, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Os idiomas direcionados do site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Somente posicionamentos de exibição padrão) Se permite ou não a entrega de anúncios em sites não auditados: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Quando o posicionamento é direcionado ao estoque privado, essa opção pode fornecer anúncios em sites bloqueados. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | O número de sites de destino, se houver, especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Os públicos-alvo direcionados, se houver, foram especificados ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Os públicos excluídos, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Se os segmentos demográficos de [!DNL Comscore] estão ou não habilitados para o posicionamento (e outros posicionamentos na campanha): *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Este recurso pode ser habilitado apenas para campanhas para as quais o recurso [!DNL Audience Verification] está habilitado para [!DNL Nielsen] e/ou [!DNL Comscore].  Incorre em taxas adicionais. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Se o direcionamento de anúncios deve ser estendido entre dispositivos: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. O direcionamento entre dispositivos estende seu direcionamento em todo o dispositivo conhecido de uma pessoa, de acordo com o gráfico de dispositivos especificado nas configurações da campanha. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Incluído # | O número de códigos de tópico de destino, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | O número de códigos de tópico excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | O número de destinos de dispositivos de destino, se algum for especificado, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | O número de destinos de dispositivos excluídos, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | O número de provedores ISP de destino, se houver, especificado, ou *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | O número de provedores de ISP excluídos, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | O número de filtros de segurança da marca aplicados, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | O número de filtros de bloqueio de fraude pré-oferta aplicados, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | O número de filtros de visibilidade pré-oferta aplicados, se algum for especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Se o Bloqueio de Segurança do Site está habilitado ou não: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | O número de pixels de rastreamento de eventos de terceiros anexados ao posicionamento, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | O número de pixels de rastreamento de conversão anexados ao posicionamento, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Uma taxa de taxa estática de terceiros que deve ser rastreada como um custo não faturável por 1000 impressões, se aplicável. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | O número de anúncios anexados ao posicionamento, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Os nomes de quaisquer anúncios anexados ao posicionamento, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | As IDs de anúncio exclusivas geradas pelo DSP de qualquer anúncio anexado ao posicionamento, separadas por ponto e vírgula. Para baixar uma lista de nomes de anúncios e IDs de Anúncios associadas da exibição [!UICONTROL Ads], crie uma exibição personalizada que inclua a métrica [!UICONTROL Ad ID] e [exporte os dados](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sim |

>[!MORELIKETHIS]
>
>* [Revisar e Editar Configurações do Pacote Usando Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)
>* [Revisar e Editar Configurações de Posicionamento Usando Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)
