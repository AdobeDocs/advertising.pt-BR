---
title: Colunas em planilhas baixadas/carregadas
description: Faça referência às colunas de configuração de posicionamento em planilhas baixadas e carregadas.
feature: DSP Placements
exl-id: 698c0d86-cb2e-4d76-89c7-5584b6cdb542
source-git-commit: ad0b5826e6639675f374837a04f9877fd05dd0c7
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# Colunas de configuração de posicionamento em planilhas baixadas/carregadas

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> Em uma planilha baixada, todas as colunas editáveis são destacadas em azul.

## Planilhas de nível de campanha

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
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Se dayparting é *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Nota:</b> Para verificar o horário real de faixa horária, abra as configurações de posicionamento no DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | O orçamento de posicionamento, se houver. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | O intervalo do orçamento: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sim |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | O objetivo do pacote. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | O valor de destino da meta. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Se a inserção está se encaminhando para a variável *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | O lance máximo para a inserção. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | A estratégia de ritmo de voo para a colocação: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | A estratégia de ritmo intradiário para o posicionamento: *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Quaisquer critérios de filtro pré-oferta a serem aplicados. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Se as regras de licitação (obsoletas) são *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | O limite de frequência primária para o posicionamento durante o período especificado [!UICONTROL Frequency Cap Interval]. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | O intervalo do limite de frequência primário: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundário para o posicionamento durante o período especificado [!UICONTROL Secondary Frequency Cap Interval] | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundário: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pela variável [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos para os quais o [!UICONTROL Secondary Frequency Cap] aplicável. Por exemplo, se o limite secundário for de três impressões a cada seis horas, o valor aqui será `6`. | Sim |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | O número de localizações geográficas visadas, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | As localizações geográficas direcionadas, separadas por ponto e vírgula ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | O número de localizações geográficas ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | As localizações geográficas excluídas, separadas por ponto e vírgula ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | O número de negociações de inventário público direcionadas, se houver, especificado, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | O número de negociações de estoque público excluídas, se houver, especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | O número de ofertas de estoque privado direcionadas, se houver, são especificadas, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | O número de negociações de estoque privado excluídas, se houver, especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | O número de públicos-alvos [!UICONTROL On-Demand Inventory] transações, se houver, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | O número de negociações de Inventário sob Demanda excluídas, se houver, que tenham sido especificadas, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | O tipo de tráfego direcionado: *[!UICONTROL Website]* e/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Se a opção de Direcionamento de Inventário para excluir o tráfego externo é &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* ou *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Anúncios de saída geralmente aparecem sobre o conteúdo como um pop-up ou recheados com conteúdo (na experiência nativa), em vez de anúncios de vídeo regulares em um reprodutor de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | A qualidade dos sites a serem direcionados: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | O número de categorias de site de destino, se houver, especificado, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | O número de categorias de site excluídas, se houver, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Os sites excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Os idiomas direcionados do site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Somente disposições de exibição padrão) Se permitir ou não a entrega de anúncios em sites não auditados: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Quando o posicionamento é direcionado ao estoque privado, essa opção pode fornecer anúncios em sites bloqueados. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | O número de sites direcionados, se houver, especificado, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Os públicos-alvo direcionados, se houver, foram especificados ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Os públicos-alvo excluídos, se houver, são especificados ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Se [!DNL Comscore] os segmentos demográficos são ativados para a inserção (e outras inserções na campanha): *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Esse recurso pode ser habilitado somente para campanhas para as quais [!DNL Audience Verification] recurso está habilitado para [!DNL Nielsen] e/ou [!DNL Comscore].  Incorre em taxas adicionais. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Se o direcionamento de anúncios deve ser estendido entre dispositivos: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. O direcionamento entre dispositivos estende seu direcionamento em todo o dispositivo conhecido de uma pessoa, de acordo com o gráfico de dispositivos especificado nas configurações da campanha. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Incluído # | O número de códigos de tópico direcionados, se houver, especificado, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | O número de códigos de tópico excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | O número de destinos de dispositivos de destino, se houver, especificado ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | O número de destinos de dispositivos excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | O número de provedores de ISP de destino, se houver, especificado, ou *[!UICONTROL All]/i> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | O número de provedores de ISP excluídos, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | O número de filtros de segurança da marca aplicados, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | O número de filtros de bloqueio de fraude pré-oferta aplicados, se houver, são especificados ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | O número de filtros de visibilidade pré-oferta aplicados, se houver, são especificados ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Se o Bloqueio de Segurança do Site está habilitado ou não: *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | O número de pixels de rastreamento de eventos de terceiros anexados ao posicionamento ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | O número de pixels de rastreamento de conversão anexados ao posicionamento ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Uma taxa de taxa estática de terceiros que deve ser rastreada como um custo não faturável por 1000 impressões, se aplicável. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | O número de anúncios anexados ao posicionamento, se houver, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Os nomes de qualquer anúncio anexado ao posicionamento ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | As IDs de anúncio exclusivas geradas pelo DSP de qualquer anúncio anexado ao posicionamento, separadas por ponto e vírgula. Para baixar uma lista de nomes de anúncios e IDs de anúncios associadas da [!UICONTROL Ads] crie uma exibição personalizada que inclua a variável [!UICONTROL Ad ID] e depois [exportar os dados](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sim |

## Planilhas de nível de posicionamento

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
| [!UICONTROL Budget Interval] | O intervalo do orçamento: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sim |
| [!UICONTROL Primary Frequency Cap] | O limite de frequência primária para o posicionamento durante o período especificado [!UICONTROL Primary Frequency Cap Interval]. | Sim |
| [!UICONTROL Primary Frequency Cap Interval] | O intervalo do limite de frequência primário: *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Sim |
| [!UICONTROL Secondary Frequency Cap] | O limite de frequência secundário para o posicionamento durante o período especificado [!UICONTROL Secondary Frequency Cap Interval] | Sim |
| [!UICONTROL Secondary Frequency Cap Interval] | O tipo de intervalo para o limite de frequência secundário: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. O número aplicável de semanas, dias, horas ou minutos é indicado pela variável [!UICONTROL Secondary Frequency Cap Interval Value]. | Sim |
| [!UICONTROL Secondary Frequency Cap Interval Value] | O número de semanas, dias, horas ou minutos para os quais o [!UICONTROL Secondary Frequency Cap] aplicável. Por exemplo, se o limite secundário for de três impressões a cada seis horas, o valor aqui será `6`. | Sim |
| [!UICONTROL Attached Ad ID] | As IDs de anúncio exclusivas geradas pelo DSP de qualquer anúncio anexado ao posicionamento, separadas por ponto e vírgula. Para baixar uma lista de nomes de anúncios e IDs de anúncios associadas da [!UICONTROL Ads] crie uma exibição personalizada que inclua a variável [!UICONTROL Ad ID] e depois [exportar os dados](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sim |

>[!MORELIKETHIS]
>
>* [Sobre a Correção de Configurações de Posicionamento Usando Planilhas](qa-about.md)
>* [Baixar configurações de posicionamento em uma planilha](qa-sheet-download.md)
>* [Carregar Configurações de Posicionamento em uma Planilha](qa-sheet-upload.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
