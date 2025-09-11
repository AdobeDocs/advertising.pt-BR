---
title: Colunas de Relatório Disponíveis
description: Consulte descrições de colunas disponíveis em relatórios personalizados.
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: 4b09e4c09bd2d028365c820c24ac041fb5e5283c
workflow-type: tm+mt
source-wordcount: '2306'
ht-degree: 0%

---

# Colunas de Relatório Disponíveis

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| Tipo de métrica | Subtipo | Nome da coluna | Descrição |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | A ID do anúncio atribuída pelo servidor de anúncios externo. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | O identificador exclusivo do anúncio no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | O nome do anúncio conforme atribuído pelo usuário. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | O formato do anúncio. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | A classificação do anúncio como alterada pelo usuário ou indicada pelas entradas de data: *[!UICONTROL live]*, *[!UICONTROL scheduled]*, *[!UICONTROL completed]* ou *[!UICONTROL archived]*. |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | O nome do anunciante. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | O orçamento total atribuído pelo usuário para a campanha. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | A data final da campanha. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | O identificador exclusivo da campanha no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | O nome da campanha conforme atribuído pelo usuário. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | A primeira data da campanha. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | O título do conteúdo. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | A série de conteúdo. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | O gênero do conteúdo. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | A qualidade da produção, conforme definido pelo [Laboratório de Tecnologia do IAB](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Os valores podem `Unknown`, `Professionally Produced`, `Prosumer` ou `User Generated`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | O tipo de conteúdo, conforme definido pelo [Laboratório de Tecnologia do IAB](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Os valores podem incluir `Video,` `Game`, `Music`, `Application`, `Text`, `Other` ou `Unknown`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | A classificação de conteúdo, como PG ou R. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | Se o anúncio apareceu em uma transmissão ao vivo: `Not Live` ou `Live`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | A duração do conteúdo em segundos; normalmente usada para vídeo ou áudio. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | O idioma do conteúdo usando ISO-639-1-alpha-2. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | O ano, mês e dia. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | Dia [!UICONTROL of Week] | O dia específico, como [!UICONTROL Monday] ou [!UICONTROL Tuesday]. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | O ano, mês, dia e hora. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | O mês e o ano. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | O horário, de 0 a 23. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | O intervalo de datas da semana relevante, de domingo a sábado. Exemplo: 18/02/2021 a 7/03/2021. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | O fornecedor do navegador no qual o anúncio foi exibido (como Google ou Mozilla). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | A versão do navegador em que o anúncio foi exibido (como [!UICONTROL Safari 4.3] ou [!UICONTROL Chrome 7.0]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | O navegador no qual o anúncio foi exibido (como [!UICONTROL Chrome] ou [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Environment] | Se o anúncio foi mostrado em *[!UICONTROL sites]* ou *[!UICONTROL Apps]*. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | O tipo de dispositivo no qual o anúncio foi exibido (como [!UICONTROL Set Top Box] ou [!UICONTROL Mobile Phone]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | O fabricante do dispositivo no qual o anúncio foi exibido (como [!UICONTROL Samsung], [!UICONTROL Lenovo] ou [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | O modelo do dispositivo no qual o anúncio foi exibido (como [!UICONTROL iPhone XS] ou [!UICONTROL Galaxy Note 7]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | O fornecedor do sistema operacional no qual o anúncio foi exibido (como [!UICONTROL Microsoft] ou [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | A versão do sistema operacional no qual o anúncio foi exibido (como [!UICONTROL Windows 10] ou [!UICONTROL iOS Mojave]) |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | O sistema operacional no qual o anúncio foi exibido (como [!UICONTROL Apple iOS] ou [!UICONTROL Android]). |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal ID] | O identificador exclusivo atribuído a uma transação por meio do parceiro de fornecimento externo. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Name] | O nome atribuído pelo usuário para o negócio, conforme inserido no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Source] | O parceiro de suprimento que fornece o inventário. Normalmente, é um editor, mas também pode ser um SSP. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | A classificação do inventário: *[!UICONTROL Private],* *[!UICONTROL On Demand],* ou *[!UICONTROL Public]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | O parceiro do lado da oferta (SSP) ao qual a mídia é atribuída. |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | O número de vezes que um dispositivo recebeu um anúncio, com base no cookie exclusivo ou na ID do dispositivo. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | A cidade à qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | O país ao qual os dados reportados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | A Área de mercado designada (DMA) à qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | O estado ao qual os dados relatados são atribuídos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | A audiência. O relatório suporta até 10 públicos-alvo únicos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | A campanha. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | A duração do criativo. O relatório suporta até 10 comprimentos criativos exclusivos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | O dispositivo. O relatório suporta até 10 dispositivos únicos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | O tipo de feed. O relatório suporta até 10 tipos de feed exclusivos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | O tipo de mídia. O relatório suporta até 10 tipos de mídia exclusivos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | O editor. O relatório suporta até 10 editores únicos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | O pacote. <!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | O posicionamento.<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | O site ou aplicativo no qual a impressão do anúncio foi veiculada. O relatório suporta até 10 sites ou aplicativos exclusivos. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | A tag de posicionamento usada como um identificador personalizado para o posicionamento. O relatório suporta até 10 tags de posicionamento exclusivas. <!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | A audiência. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | A campanha. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | A duração do criativo. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | O dispositivo. (como CTV, Desktop etc.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | O tipo de mídia. (como Vídeo, Áudio etc.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | O editor. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | O posicionamento. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | A data final do pacote. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | O valor da meta de ritmo do pacote. Esse valor está em gastos ou impressões. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | O identificador exclusivo do pacote no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | O nome do pacote |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | A data de início do pacote. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | A data final do posicionamento. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | (Obsoleto) A ID de conversão atribuída pelo DSP aos eventos de conversão [!DNL TubeMogul] herdados. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | (Obsoleto) O nome de conversão atribuído aos [!DNL TubeMogul] eventos de conversão herdados. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | O identificador exclusivo do posicionamento no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | O nome do posicionamento conforme atribuído pelo usuário. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | O orçamento de posicionamento. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | O lance máximo para a inserção. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Device Environment] | Os ambientes de dispositivo aos quais o posicionamento se destina: (*[!UICONTROL Desktop]*, *[!UICONTROL Mobile]* e/ou *[!UICONTROL Connected TV])*. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | A data final do posicionamento. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | A data de início da colocação. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | A tag de posicionamento usada como um identificador personalizado para o posicionamento. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | A descrição associada a um segmento faturável. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | A chave exclusiva associada a um segmento faturável. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | O nome de um segmento faturável. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | A descrição associada a um segmento, fornecida pelo provedor de dados. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | A chave exclusiva associada a um segmento. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | O nome de um segmento. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | O nome do provedor de dados associado a um segmento. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | O identificador exclusivo do site ou aplicativo no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | O nome do site. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | A duração do vídeo, que é processado após o upload. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | O identificador exclusivo do criativo do vídeo no DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | O nome do criativo atribuído pelo usuário. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | O [!UICONTROL App/Site Distinct Uniques] dividido por [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | O número total de dispositivos que foram atingidos somente neste aplicativo. Um visualizador exposto a um anúncio em vários editores não é incluído nesse valor. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | O [!UICONTROL Total Spend] dividido por [!UICONTROL App/Site Distinct Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | O [!UICONTROL Total Spend] dividido por [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | A porcentagem estimada do universo doméstico alvo que recebeu uma exposição. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | O número médio de impressões mostradas para únicos. Para alguns inventários, os editores não transmitem um identificador de dispositivo e essas impressões não são incluídas nesse valor. Há uma métrica semelhante no relatório [!UICONTROL Frequency (by App/Site)], mas essa métrica não é estimada. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | (Incluído no relatório [!UICONTROL Frequency (by Impression)]) As impressões estimadas para uma determinada interrupção de frequência. As estimativas do DSP são baseadas em uma amostra de impressões. Para alguns inventários, os editores não transmitem um identificador de dispositivo e essas impressões não são incluídas nesse valor. Há uma métrica semelhante no relatório [!UICONTROL Frequency (by App/Site)], mas essa métrica não é estimada. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | (Incluído no relatório [!UICONTROL Frequency (by Impression)]) O número de navegadores ou dispositivos exclusivos gravados para uma determinada frequência. As estimativas do DSP são baseadas em uma amostra de impressões. Em alguns inventários, não transmita um identificador de dispositivo, e essas impressões não são incluídas nesse valor. Há uma métrica semelhante no relatório [!UICONTROL Frequency (by App/Site)], mas essa métrica não é estimada. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | A soma das famílias exclusivas que a DSP (leilões) viu dentro do intervalo de datas. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | O número total de impressões servidas como resultado do uso de um gráfico de dispositivos para direcionamento entre dispositivos com base em pessoas. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency] | A frequência das impressões por família. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | A frequência com que os agregados familiares chegam apenas através da dimensão comunicada, incluindo interseções de até três valores para a dimensão. Por exemplo, se você usar a dimensão [!UICONTROL Placement], poderá ver a frequência atingida por posicionamentos individuais, as frequências atingidas por uma combinação de dois posicionamentos quaisquer e as frequências atingidas por combinações de três posicionamentos quaisquer. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | O número de famílias atingidas somente pela dimensão relatada, calculado como <code>[endereços IP atingidos somente pela dimensão relatada] - [endereços IP atingidos por qualquer outra dimensão]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | A porcentagem de famílias atingidas somente pela dimensão relatada, calculada como <code>[a porcentagem de endereços IP atingidos pela dimensão] - [a porcentagem de endereços IP atingidos por qualquer outra dimensão]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Impressions] | O número total de impressões de anúncios veiculadas. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | O número total de impressões veiculadas que puderam ser medidas para fins de visibilidade. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | O número total de impressões mensuráveis servidas apenas pela dimensão relatada, incluindo interseções de até três valores para a dimensão. Por exemplo, se você usar a dimensão [!UICONTROL Placement], poderá ver as impressões mensuráveis atingidas por inserções individuais, impressões mensuráveis atingidas por uma combinação de dois posicionamentos quaisquer e impressões mensuráveis atingidas por combinações de três posicionamentos quaisquer. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | O gasto total. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | O total de domicílios únicos (endereços IP distintos) alcançados. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | O total de domicílios únicos (endereços IP distintos) atingido apenas pela dimensão reportada, incluindo interseções de até três valores para a dimensão. Por exemplo, se você usar a dimensão [!UICONTROL Placement], poderá ver as famílias exclusivas atingidas por posicionamentos individuais, residências comuns atingidas por uma combinação de dois posicionamentos e residências comuns atingidas por combinações de três posicionamentos. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | O Gasto Total dividido pelo Agregado Familiar Incremental Atingido. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | O Gasto Total dividido por Agregado Único Atingido. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | A frequência das impressões por família. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | O número de famílias atingidas somente pela dimensão relatada, calculado como [endereços IP atingidos somente pela dimensão relatada] - [endereços IP atingidos por qualquer outra dimensão]. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | A porcentagem de famílias atingidas somente pela dimensão relatada, calculada como [a porcentagem de endereços IP atingidos pela dimensão] - [a porcentagem de endereços IP atingidos por qualquer outra dimensão]. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | O número total de impressões de anúncios veiculadas. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | O número total de impressões veiculadas que puderam ser medidas para fins de visibilidade. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | O gasto total. |
| [!UICONTROL Metric] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | O total de domicílios únicos (endereços IP distintos) alcançados. |
| [!UICONTROL Metric] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | O tipo de ID direcionada. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | O custo bruto médio por aquisição, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | O custo bruto médio por clique no anúncio, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | O custo médio por visualização de vídeo concluída, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | O custo médio por 1000 impressões, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | O custo médio por visualização de vídeo, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | O custo médio por 1000 impressões visualizáveis, calculado por <code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | O custo líquido médio por clique no anúncio, calculado por <code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | O custo líquido médio por exibição de vídeo concluída, calculado por <code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | O custo líquido médio por 1000 impressões, calculado por <code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | O custo líquido médio por visualização de vídeo, calculado por <code>[!UICONTROL Net Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | A porcentagem do total de lances que foram oferecidos no CPM máximo. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | O número de usuários distintos para os quais a DSP ofereceu a inserção. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Data Net Spend] | O custo líquido total das taxas de dados do segmento de público-alvo faturadas por meio do DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Media Net Spend] | O custo líquido total da mídia faturável, incluindo a taxa de tecnologia, faturado pela DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Other Net Spend] | O custo total de outras taxas de serviço (parceiros de verificação de terceiros, veiculação de anúncios etc.) cobradas pela DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | O imposto estimado sobre segmentos de público-alvo de terceiros e serviços de dados. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | O imposto estimado sobre a mídia, incluindo o imposto aplicado à tarifação de custos de mídia e serviços de taxa técnica na DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | O imposto estimado sobre outras taxas de serviço (incluindo parceiros de verificação de terceiros, direcionamento de tópico etc.) cobradas pela DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Margin %] | (Quando o gerenciamento de margem está ativado) A porcentagem de margem, que é calculada por <code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | A soma do custo de mídia não faturável e faturável sem nenhuma taxa técnica. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | O custo líquido médio por 1000 impressões visualizáveis, calculado por <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Net Spend] | O custo líquido total das taxas de dados de segmento de público-alvo não faturadas por meio do DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Fees] | O custo líquido total da mídia não faturável, incluindo a taxa de tecnologia, não faturado por meio do DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | O custo total de outras taxas de serviço (parceiros de verificação de terceiros, veiculação de anúncios e assim por diante) não cobradas pela DSP. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Billable Net Spend] | A soma de [!UICONTROL Billable Spend (Media)], [!UICONTROL Billable Spend (Data)] e [!UICONTROL Billable Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | O custo líquido médio dos dados por 1000 impressões, calculado por <code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Data Net Spend] | O custo líquido total das taxas de dados do segmento de público-alvo. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | O custo líquido médio de mídia por 1000 impressões, calculado por <code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Media Net Spend] | O custo líquido total da mídia, incluindo taxas de tecnologia. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | A soma de [!UICONTROL Net Spend (Media)], [!UICONTROL Net Spend (Data)] e [!UICONTROL Net Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | A soma de [!UICONTROL Non-billable Spend (Media)], [!UICONTROL Non-billable Spend (Data)] e [!UICONTROL Non-billable Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | O custo líquido médio por 1000 impressões para outras taxas, calculado por <code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Other Net Spend] | O custo líquido total de outras taxas de serviço (parceiros de verificação de terceiros, veiculação de anúncios etc.). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | A porcentagem de visualizações que assistiram ao anúncio em sua totalidade. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | O número de visualizações que assistiram ao anúncio em sua totalidade. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | A porcentagem de impressões visualizáveis que assistiram ao anúncio em sua totalidade. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | A porcentagem de visualizações que assistiram a pelo menos um quarto do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | O número de visualizações que assistiram a pelo menos um quarto do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | A porcentagem de visualizações que assistiram a pelo menos dois quartis do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | O número de visualizações que assistiram a pelo menos dois quartis do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | A porcentagem de impressões visíveis que assistiram a pelo menos dois quartis do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | A porcentagem de visualizações que assistiram a pelo menos três quartis do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | O número de visualizações que assistiram a pelo menos três quartis do anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | A porcentagem média em que um anúncio foi observado até a conclusão, contabilizando todas as exibições. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | O número de cliques na sobreposição de anúncio e nos banners. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | A porcentagem de cliques dividida por impressões de anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | A porcentagem de cliques dividida pelas visualizações do vídeo. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | O número de cliques no banner complementar. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | A porcentagem de cliques dividida por impressões de banner complementares. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | O número de impressões de banner complementares. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | O tipo de conexão com a Internet usado para exibir o anúncio (como Wifi ou 4g LTE). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | O número de interações em um anúncio veiculado. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | O número total de impressões de anúncios. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | A porcentagem de impressões veiculadas que resultaram em visualizações de vídeo. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | A duração média de uma visualização de vídeo, medida em segundos. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | A soma de todos os cliques em um anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | O número total de minutos durante os quais um anúncio de vídeo foi exibido. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | O número total de visualizações de anúncios de vídeo. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | A largura e a altura médias do player. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | O número total de impressões veiculadas que puderam ser medidas para fins de visibilidade. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | A porcentagem de impressões servidas que puderam ser medidas para visibilidade, calculada como <code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | A porcentagem de impressões não mensuráveis para visibilidade devido a iFrames incompatíveis. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | O número de impressões não mensuráveis para visibilidade devido ao rastreamento de visibilidade não compatível na unidade de anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | A porcentagem de impressões não mensuráveis para visibilidade devido a outros motivos. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | O número de impressões de anúncios não mensurável para visibilidade. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | A porcentagem de impressões de anúncios não mensurável para visibilidade. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | A porcentagem de impressões não mensuráveis para visibilidade devido ao rastreamento de visibilidade não compatível nesta unidade de anúncio. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | A porcentagem de impressões visíveis de todas as impressões mensuráveis, calculada como <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | O número de impressões de anúncios consideradas visíveis. |
| [!UICONTROL Conversion Metrics] | [Agrupado pelo anunciante nas configurações do relatório] | [Conversão específica do anunciante] | O total de uma métrica de conversão específica do anunciante ou evento do Adobe Analytics. |
| [!UICONTROL Custom Goals] | [Agrupado pelo anunciante nas configurações do relatório] | [Meta personalizada específica do anunciante] | A soma ponderada de todas as conversões incluídas na [meta personalizada](/help/dsp/optimization/custom-goal.md) especificada. |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal CPA|The average cost per acquisition, calculated by <code>Gross Spend / Custom Goal</code> | -->
<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar um Relatório Personalizado](/help/dsp/reports/report-copy.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Configurações de Relatório Personalizado](/help/dsp/reports/report-settings.md)
