---
title: Rastreamento de conversão usando um feed de ID EF
description: Saiba mais sobre como usar um feed de ID de EF para dados de rastreamento de conversão.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
TQID: https://experienceleague.adobe.com/D4OpKvTL-jjIOgMaakH78aYA7q9p2BXcc2P-RI8blfY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---

# Rastreamento de conversão usando um feed de ID EF

Neste método, a Advertising Cloud coleta um valor `ef_id` sempre que um usuário clica e anúncio e chega à página de aterrissagem, e o anunciante armazena o valor `ef_id` com os dados de conversão e o envia em um feed de dados.

## Visão geral da implementação

*Somente funções de gerente de conta da agência, gerente de conta [!DNL Adobe] e usuário administrador*

1. Use as opções de rastreamento de conta ou campanha &quot;[!UICONTROL EF Redirect]&quot;, o tipo de redirecionamento de &quot;[!UICONTROL Token]&quot; e &quot;[!UICONTROL Auto Upload]&quot; para gerar automaticamente uma URL de destino ou uma URL final com um token Adobe Advertising (ef_id) para cada palavra-chave (para rastreamento em nível de palavra-chave) ou anúncio (para rastreamento em nível de anúncio) na conta ou campanha.

   >[!NOTE]
   >* Esse método não exige que o anunciante use tags de rastreamento de conversão do Adobe Advertising.
   >* Se você alternar o tipo de redirecionamento de uma conta ou campanha existente de [!UICONTROL Standard] para [!UICONTROL Token], ou vice-versa, será necessário regenerar todas as URLs de rastreamento aplicáveis.

   A ef_id é preenchida e anexada ao URL da página inicial quando o usuário final clica no anúncio e é redirecionado para um servidor do Adobe Advertising. A ef_id é passada para o anunciante no URL de destino ou URL final para o anúncio ou palavra-chave. Este é um exemplo de um URL de destino passado para o anunciante durante o redirecionamento:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. O anunciante extrai a ef_id do redirecionamento e a armazena com os dados de conversão relevantes a serem incluídos no arquivo de feed. Não altere a ef_id ou altere sua caixa.

1. (Opcional, mas recomendado) O anunciante pode criar uma ID de transação exclusiva para cada transação a ser incluída no arquivo de feed.

1. O anunciante carrega um arquivo com os [dados de conversão necessários](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) no local do servidor designado.

1. Os Serviços técnicos analisam os dados de conversão nos arquivos carregados e, em seguida, fazem o upload dos dados no Adobe Advertising. Em seguida, o Adobe Advertising rastreia os dados em relação a palavras-chave, anúncios e posicionamentos individuais e cria uma previsão de receita para cada um.

1. Os Serviços técnicos validam os dados processados em relação aos dados de feed e verificam se há [transações órfãs](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Requisitos de dados para feeds de dados usando EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
