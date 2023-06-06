---
title: Configurar o rastreamento de conversão para suas páginas da Web
description: Saiba como ativar o Adobe Advertising para rastrear conversões resultantes de impressões e cliques de anúncios.
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Configurar o rastreamento de conversão para suas páginas da Web

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

Antes de gerar relatórios sobre dados de conversão, o Adobe Advertising precisa de dados de impressão, clique, custo e conversão (transação) para cada uma de suas palavras-chave e anúncios. A Adobe Advertising também usa esses dados para criar os modelos de previsão de dados necessários para otimizar os orçamentos da campanha e os lances de suas palavras-chave e anúncios.

Para permitir que o Adobe Advertising rastreie as conversões resultantes de impressões e cliques de anúncios, é necessário fazer o seguinte:

* Inclua um código exclusivo de rastreamento de cliques (e talvez um código adicional para redirecionar o usuário final para um servidor de rastreamento) no modelo de rastreamento ou URL de destino para cada palavra-chave, anúncio, posicionamento, sitelink e grupo de produtos em cada campanha de publicidade gerenciada pelo Search, Social e Commerce. Isso permite que a Adobe Advertising rastreie cada impressão de anúncio (somente para exibição e anúncios sociais) e cada clique em um anúncio.

* Rastreie os dados de conversão de uma das seguintes maneiras:

   * **Conversões rastreadas por publicidade do Adobe:** O anunciante insere uma tag de rastreamento de conversão de anúncio de Adobe em cada página de conversão.

   * **Conversões do Adobe Analytics:** O anunciante usa o rastreamento de Adobe Analytics para todas as conversões.

   * **[!DNL Google Analytics]conversões:** O anunciante usa o [!DNL Google Analytics] para rastrear todas as conversões.

   * **Conversões rastreadas pelo anunciante:** O anunciante fornece um arquivo de feed diário com qualquer combinação de dados de conversão online e offline.

Para obter informações detalhadas sobre como implementar o rastreamento, consulte o capítulo de ajuda em &quot;Rastreamento&quot;.

>[!MORELIKETHIS]
>
>* [Gerar uma tag de conversão Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Gerar um URL de rastreamento de cliques de Pesquisa, Social e Comércio usando a ferramenta URLs de rastreamento](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [Decodificar um URL de rastreamento de cliques de Pesquisa, Social e Comércio](/help/search-social-commerce/tools/click-tracking-url-decode.md)

