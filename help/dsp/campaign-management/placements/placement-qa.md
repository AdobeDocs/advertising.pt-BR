---
title: Revisar e editar configurações de posicionamento usando planilhas
description: Saiba como revisar e editar configurações de posicionamento de chaves usando planilhas.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 0%

---

# Revisar e editar configurações de posicionamento usando planilhas

Você pode baixar as configurações para um ou mais posicionamentos, ou para todos os posicionamentos em uma campanha, no formato XLSX ([!DNL Microsoft Excel] planilha) para revisão. Use esse recurso para analisar rapidamente detalhes como:

* O público alvo da campanha.
* Quando os posicionamentos começam a entregar e quando param.
* Quais anúncios são anexados aos posicionamentos.

Em seguida, é possível fazer alterações em campos selecionados e carregá-los de volta para o DSP de uma só vez. Os campos editáveis incluem nomes de posicionamento, status, lances, orçamentos, estratégias de ritmo e limites de frequência.

>[!TIP]
>
>Para editar mais campos para um ou mais posicionamentos, consulte &quot;[Editar Posicionamentos](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Configurações de download para todos os posicionamentos em uma campanha

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Ao lado do nome da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * Clique no nome da campanha para exibir seus detalhes. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   Uma mensagem de notificação indica quando o arquivo está disponível para download.

1. Siga um destes procedimentos:

   * Na mensagem de notificação, clique em **[!UICONTROL Download].**

   * À direita da barra de menu superior, clique em ![Trabalhos](/help/dsp/assets/downloads.png). Clique em **[!UICONTROL Download]** ao lado do trabalho.

   O arquivo é salvo na pasta Downloads do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

## Baixar configurações para uma ou mais disposições

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada posicionamento cujas configurações você deseja baixar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

O arquivo é salvo automaticamente na pasta Download do navegador. Consulte &quot;[Colunas de posicionamento em planilhas baixadas/carregadas](#qa-sheet-columns)&quot; para obter uma lista das colunas incluídas.

## Configurações de upload para todos os posicionamentos em uma campanha

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Siga um destes procedimentos:

   * Ao lado do nome da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * Clique no nome da campanha para exibir seus detalhes. No canto superior direito, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. No diálogo [!UICONTROL Edit in Excel]:

   1. Arraste e solte um arquivo na caixa ou clique dentro dela para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

1. (Opcional) Para verificar se as atualizações foram processadas, clique em ![Trabalhos](/help/dsp/assets/downloads.png) à direita da barra de menu superior.

## Configurações de upload para um ou mais posicionamentos

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada posicionamento cujas configurações você deseja fazer upload.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. No diálogo [!UICONTROL Edit in Excel]:

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

### Planilhas de nível de posicionamento

| Coluna | Descrição | Editável? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | A ID numérica do posicionamento. | — |
| [!UICONTROL Placement Name] | O nome do posicionamento. | Sim |
| [!UICONTROL Package Name] | O nome do pacote principal, quando aplicável. | — |
| [!UICONTROL Start Date] | A data de início do posicionamento. | — |
| [!UICONTROL End Date] | A data final do posicionamento. | — |
| [!UICONTROL Status] | O status do posicionamento: *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | O lance máximo para a inserção. | Sim |
| [!UICONTROL Budget] | O orçamento de posicionamento, se houver. | Sim |
| [!UICONTROL Budget Interval] | O intervalo de orçamento: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Sim |
| [!UICONTROL Primary Frequency Cap] | O limite de frequência primária para o posicionamento durante o [!UICONTROL Primary Frequency Cap Interval] especificado. | Sim |
| [!UICONTROL Primary Frequency Cap Interval] | O intervalo para o limite de frequência primária: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundário para o posicionamento durante o [!UICONTROL Secondary Frequency Cap Interval] especificado | Sim |
| [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundário: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pelo [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos aos quais o [!UICONTROL Secondary Frequency Cap] se aplica. Por exemplo, se o limite secundário for de três impressões a cada seis horas, o valor aqui será `6`. | Sim |
| [!UICONTROL Attached Ad ID] | As IDs de anúncio exclusivas geradas pelo DSP de qualquer anúncio anexado ao posicionamento, separadas por ponto e vírgula. Para baixar uma lista de nomes de anúncios e IDs de Anúncios associadas da exibição [!UICONTROL Ads], crie uma exibição personalizada que inclua a métrica [!UICONTROL Ad ID] e [exporte os dados](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sim |

>[!MORELIKETHIS]
>
>* [Editar posicionamentos](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
