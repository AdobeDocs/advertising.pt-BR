---
title: Sobre as tags de rastreamento de conversão de publicidade do Adobe
description: Saiba mais sobre como usar as tags de rastreamento de conversão do Adobe Advertising.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Sobre as tags de rastreamento de conversão de publicidade do Adobe

O Adobe Advertising rastreia conversões resultantes de cliques em anúncios usando tags de rastreamento de conversão do Adobe Advertising inseridas nas páginas da Web que abrem quando um evento de conversão ocorre, como uma página de &quot;sucesso&quot;. As tags incluem informações incorporadas para enviar os dados da transação, juntamente com o cookie Adobe do usuário Advertising, para um servidor de rastreamento, do qual a transação é creditada ao clique ou impressão de anúncio apropriado (de acordo com as configurações de atribuição de conversão do anunciante).

>[!NOTE]
>
>Se o usuário não tiver um cookie válido, a Adobe Advertising não relatará a conversão.

Para cada conjunto de métricas de conversão que você deseja rastrear, é necessário criar uma tag de conversão separada. Forneça as tags ao anunciante ou à agência uma lista de páginas da Web nas quais inserir cada uma. Você pode gerar qualquer um dos seguintes tipos de tags de conversão. Consulte &quot;[Gerar uma tag de conversão Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; para obter instruções.

* (Recomendado) Tags do JavaScript (Versão 3 ou Versão 2), que não estão visíveis nas páginas da Web.

* HTML tags de imagem para exibir imagens transparentes (pixels) de 1 pixel x 1 pixel, que são invisíveis para os usuários finais, nas páginas da Web. Use tags de imagem somente quando a empresa tiver uma política contra o uso de tags JavaScript.

Para obter mais informações sobre as diferenças entre os tipos de tag, consulte &quot;[Perguntas frequentes sobre as tags de rastreamento de conversão do Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Esse recurso não adiciona tags de imagem ou tags JavaScript às páginas da Web do anunciante. As tags devem ser adicionadas de acordo com o procedimento normal do anunciante para atualização de páginas da Web.
>* Considere quanto tempo levará para implementar as tags. Dependendo das políticas da empresa, a implementação pode levar semanas ou até meses.


## Recursos das tags de rastreamento de conversão de publicidade do Adobe

O pixel de rastreamento de conversão permite que a Adobe Advertising faça o seguinte:

* Rastreie e relate os dados de conversão no nível de palavra-chave para campanhas de pesquisa.

* Rastreie e relate os dados de conversão no nível de anúncio (criativo) em todos os canais de marketing (pesquisa e exibição pagas), o que pode facilitar o teste criativo.

* Rastreie e relate os dados de conversão no nível da transação em todos os canais de marketing.

* Mostre como suas conversões são distribuídas em seus diferentes canais de marketing para que você possa ver qual é mais eficaz.

* Relate e otimize em diferentes níveis de atribuição (como atribuir conversões ao último evento relacionado ou ponderar todos os eventos uniformemente).

* Forneça visibilidade sobre as assistências a cliques (palavras-chave de pesquisa ou disposições que contribuíram para um funil de conversão) e assistências a canais (eventos de usuário que contribuíram para um funil de conversão, possivelmente em vários canais de marketing).

* Forneça visibilidade sobre a distribuição geográfica e os domínios de referência do tráfego e das conversões do site para que você possa refinar o direcionamento geográfico e de site.

* Analise as tendências diárias ou intradiárias, que podem ser usadas para melhorar as taxas de conversão.

>[!MORELIKETHIS]
>
>* [Opções de rastreamento de conversão](conversion-tracking-about.md)
>* [Gerar uma tag de conversão Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 3](format-conversion-tag-jsv3.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 2](format-conversion-tag-jsv2.md)
>* [Formato das tags de rastreamento de conversão de imagem](format-conversion-tag-image.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](faqs-conversion-page-view-tracking-tags.md)
>* [A tag de mapeamento de conversão do Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

