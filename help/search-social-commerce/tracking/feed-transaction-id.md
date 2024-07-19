---
title: Rastreamento de conversão usando um feed de ID de transação
description: Saiba mais sobre como usar um feed de ID de transação para dados de rastreamento de conversão.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Rastreamento de conversão usando um feed de ID de transação

Quando um anunciante tem transações online e offline, o Adobe Advertising pode rastrear as transações online por meio do pixel de rastreamento de conversão de Adobe Advertising, e o anunciante pode rastrear as transações offline usando uma ID de transação e entregá-las por meio de um feed:

* Para as transações online, o Adobe Advertising rastreia os cliques nos anúncios e as transações resultantes no site.

* O anunciante deve rastrear conversões offline e enviar arquivos de feed de nível de transação para o Adobe Advertising.

## Visão geral da implementação

*Somente funções de gerente de conta da agência, gerente de conta [!DNL Adobe] e usuário administrador*

1. Use as opções de rastreamento de conta ou campanha &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot; para gerar automaticamente uma URL de destino ou uma URL final para cada palavra-chave (para rastreamento em nível de palavra-chave) ou anúncio (para rastreamento em nível de anúncio) na conta ou campanha.

1. Configurar o rastreamento de conversão de Adobe Advertising para as conversões online. Esse processo é o mesmo para anunciantes com rastreamento de conversão baseado em pixel de Adobe Advertising. É importante gerar marcas de conversão que incluam um parâmetro para uma ID de transação exclusiva (`ev_transid=<transid>`).

1. Para a parte offline de cada transação, o anunciante gera a mesma ID de transação que foi usada na parte online da transação para incluir no arquivo de feed.

1. O anunciante carrega um arquivo com os [dados de conversão necessários](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) no local do servidor designado.

1. Os Serviços técnicos analisam os dados de conversão nos arquivos carregados e, em seguida, fazem o upload dos dados no Adobe Advertising. O Adobe Advertising rastreia os dados em relação a palavras-chave, anúncios e posicionamentos individuais e cria uma previsão de receita para cada um.

1. Os Serviços técnicos validam os dados processados em relação aos dados de feed e verificam se há [transações órfãs](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Requisitos de dados para feeds de dados usando uma ID de transação](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
