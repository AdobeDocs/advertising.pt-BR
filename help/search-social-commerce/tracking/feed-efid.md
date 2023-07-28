---
title: Rastreamento de conversão usando um feed de ID EF
description: Saiba mais sobre como usar um feed de ID de EF para dados de rastreamento de conversão.
exl-id: db722a54-a9bf-4a31-a285-a82e6d79c34a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Rastreamento de conversão usando um feed de ID EF

Nesse método, a Advertising Cloud coleta uma `ef_id` cada vez que um usuário clicar e adicionar, e chegar à landing page, e o anunciante armazenar o `ef_id` com os dados de conversão e os envia em um feed de dados.

## Visão geral da implementação

*Gerente de conta da agência, [!DNL Adobe] funções de gerente de conta e administrador de usuário somente*

1. Usar as opções de rastreamento de conta ou campanha &quot;[!UICONTROL EF Redirect],&quot; o tipo de redirecionamento de &quot;[!UICONTROL Token],&quot; e &quot;[!UICONTROL Auto Upload]&quot; para gerar automaticamente um URL de destino ou URL final com um token de Adobe Advertising (ef_id) para cada palavra-chave (para rastreamento em nível de palavra-chave) ou anúncio (para rastreamento em nível de anúncio) na conta ou campanha.

   >[!NOTE]
   >* Esse método não exige que o anunciante use tags de rastreamento de conversão de Adobe Advertising.
   >* Se você alternar o tipo de redirecionamento para uma conta ou campanha existente de [!UICONTROL Standard] para [!UICONTROL Token], ou vice-versa, você deverá gerar novamente todas as URLs de rastreamento aplicáveis.

   O ef_id é preenchido e anexado ao URL da página inicial quando o usuário final clica no anúncio e é redirecionado para um servidor Adobe Advertising. A ef_id é passada para o anunciante no URL de destino ou URL final para o anúncio ou palavra-chave. Este é um exemplo de um URL de destino passado para o anunciante durante o redirecionamento:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. O anunciante extrai a ef_id do redirecionamento e a armazena com os dados de conversão relevantes a serem incluídos no arquivo de feed. Não altere a ef_id ou altere sua caixa.

1. (Opcional, mas recomendado) O anunciante pode criar uma ID de transação exclusiva para cada transação a ser incluída no arquivo de feed.

1. O anunciante carrega um arquivo com a [dados de conversão necessários](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) para o local do servidor designado.

1. Os Serviços técnicos analisam os dados de conversão nos arquivos carregados e, em seguida, fazem o upload dos dados no Adobe Advertising. Em seguida, o Adobe Advertising rastreia os dados em relação a palavras-chave, anúncios e posicionamentos individuais e cria uma previsão de receita para cada um.

1. Os serviços técnicos validam os dados processados em relação aos dados do feed e verificam se há [transações órfãs](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de arquivo para arquivos de feed de conversão](feed-file-requirements.md)
>* [Requisitos em matéria de dados aplicáveis aos feeds de dados que utilizam IDs de EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
