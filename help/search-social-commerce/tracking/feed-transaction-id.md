---
title: Rastreamento de conversão usando um feed de ID de transação
description: Saiba mais sobre como usar um feed de ID de transação para dados de rastreamento de conversão.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Rastreamento de conversão usando um feed de ID de transação

Quando um anunciante tem transações online e offline, o Adobe Advertising pode rastrear as transações online por meio do pixel de rastreamento de conversão do Adobe Advertising, e o anunciante pode rastrear as transações offline usando uma ID de transação e entregá-las por meio de um feed:

* Para as transações online, o Adobe Advertising rastreia os cliques em seus anúncios e as transações resultantes em seu site.

* O anunciante deve rastrear conversões offline e enviar arquivos de feed de nível de transação para a Adobe Advertising.

## Visão geral da implementação

*Gerente de conta da agência, [!DNL Adobe] funções de gerente de conta e administrador de usuário somente*

1. Usar as opções de rastreamento de conta ou campanha &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot; para gerar automaticamente um URL de destino ou URL final para cada palavra-chave (para rastreamento em nível de palavra-chave) ou anúncio (para rastreamento em nível de anúncio) na conta ou campanha.

1. Configure o rastreamento de conversão de Publicidade em Adobe para as conversões online. Esse processo é igual ao dos anunciantes com rastreamento de conversão baseado em pixel de publicidade do Adobe. É importante gerar tags de conversão que incluam um parâmetro para uma ID de transação exclusiva (`ev_transid=<transid>`).

1. Para a parte offline de cada transação, o anunciante gera a mesma ID de transação que foi usada na parte online da transação para incluir no arquivo de feed.

1. O anunciante carrega um arquivo com a [dados de conversão necessários](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) para o local do servidor designado.

1. Os Serviços técnicos analisam os dados de conversão nos arquivos carregados e, em seguida, fazem o upload dos dados na Adobe Advertising. A Adobe Advertising rastreia os dados em relação a palavras-chave, anúncios e inserções individuais e cria uma previsão de receita para cada um.

1. Os serviços técnicos validam os dados processados em relação aos dados do feed e verificam se há [transações órfãs](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam uma ID de transação](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

