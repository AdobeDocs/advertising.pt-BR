---
title: Sobre o rastreamento para o Search, Social e Commerce
description: Saiba mais sobre as opções de rastreamento para Search, Social e Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Sobre o rastreamento para o Search, Social e Commerce

Para acompanhar o desempenho de seus anúncios, Search, Social e Commerce precisa de dados de impressão, clique, custo e conversão (transação) para seus anúncios. O Search, Social e Commerce usa esses dados para criar os modelos de previsão de dados necessários para otimizar seus portfólios de anúncios.

## Dados de custo, clique e impressão

O Search, Social e Commerce recupera dados de impressão, cliques e custos diretamente de [redes de anúncios com suporte](/help/search-social-commerce/introduction/supported-inventory.md), todos os dias. Além disso, o Search, Social e Commerce pode adicionar um código de rastreamento de cliques exclusivo (incluindo um redirecionamento para um servidor de rastreamento) em seus modelos de rastreamento e URLs de destino para rastrear impressões de exibição/conteúdo, cliques e custo e, posteriormente, vincular os eventos a conversões.

Se você quiser rastrear campanhas em redes de anúncios com as quais a Search, o Social e o Commerce não sincronizam dados, será necessário fornecer dados para essas campanhas enviando um arquivo de feed diário com os dados de impressão, clique e custo.

### Tags de rastreamento de cliques

Sua equipe de implementação de Search, Social e Commerce configura o rastreamento de cliques atualizando os modelos de rastreamento e os URLs de destino para anúncios, palavras-chave, disposições, grupos de produtos e extensões de sitelink em suas campanhas de anúncios sincronizados para incluir uma sequência de ID de rastreamento exclusiva e um redirecionamento de Adobe Advertising. Eles também adicionam rastreamento aos sufixos de página de aterrissagem (sufixos de URL finais) para suas contas e campanhas do [!DNL Google Ads] e do [!DNL Microsoft Advertising].

Os parâmetros de rastreamento permitem ao Adobe Advertising rastrear cliques em um nível de palavra-chave individual (campanhas de pesquisa) ou nível de variação de anúncio (campanhas de pesquisa com direcionamento de conteúdo ou site, campanhas de exibição e campanhas sociais). Cada vez que um usuário visualiza um anúncio de exibição/conteúdo ou clica em um de seus anúncios, a rede de anúncios envia o evento para os servidores de pixels do Adobe Advertising usando uma tag de rastreamento de cliques associada à palavra-chave ou ao anúncio. Para cliques:

* Para os anúncios do [!DNL Google Ads] e do [!DNL Microsoft Advertising] em navegadores que oferecem suporte para rastreamento paralelo, a rede de anúncios envia o clique para o seu site primeiro e, em seguida, para os servidores de pixels de Adobe Advertising, que, em seguida, colocam um cookie no computador do usuário, se esse cookie ainda não existir.

* Em todos os outros casos, a rede de publicidade envia o clique diretamente para os servidores de pixel de Adobe Advertising. O servidor de pixels coloca um cookie no computador do usuário (se ainda não existir um) e, em seguida, redireciona o usuário para o URL relevante em seu site. A experiência geral para o usuário final é a mesma que seria sem um redirecionamento.

O cookie é definido no domínio [!DNL Adobe] (`everesttech.net`) como um cookie próprio. Após um redirecionamento, o usuário fica no domínio do anunciante e o cookie é tratado como um cookie de terceiros. Para obter mais informações sobre cookies Adobe Advertising, consulte &quot;[cookies Adobe Advertising](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html)&quot;.

## Dados de conversão

Quando um cliente clica em um anúncio ou visualiza uma exibição ou anúncio social, o Search, Social e Commerce precisa mapear cada conversão resultante de volta para o clique ou exibição/impressão social original.

O anunciante desempenha uma função no fornecimento dos dados de conversão para todos os cliques e impressões sociais/de exibição. Os dados de conversão podem incluir informações sobre qualquer tipo de evento que ocorra em um site que possa ser usado para otimização de lances. Você pode fornecer dados de conversão implementando o código de rastreamento de conversão nas páginas de conversão do anunciante (como a página de &quot;sucesso&quot; exibida depois que um cliente conclui uma transação) ou enviando um arquivo de feed diário com dados de conversão capturados por outro método.

### Tags de rastreamento de conversão

Você pode usar [marcas de conversão de vários fornecedores](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Quando você usa uma tag de conversão de Adobe Advertising e um usuário conclui uma transação bem-sucedida e acessa uma página de &quot;sucesso&quot;, o servidor de pixels de Adobe Advertising verifica a existência do cookie no computador do usuário, que foi definido no momento do redirecionamento de clique. Quando encontra um cookie, as informações sobre o evento da transação são passadas usando o parâmetro ef_transid, e a transação é reconhecida como uma conversão e é creditada ao clique no anúncio anterior ou à impressão de exibição.

Se o usuário clicou em mais de um de seus anúncios, o Adobe Advertising credita a transação ao clique final do anúncio ou (para campanhas de exibição ou de vídeo) à impressão final do anúncio, a menos que você especifique o contrário. A [janela de retrospectiva de cliques](/help/search-social-commerce/glossary.md#c-d) e a [janela de retrospectiva de impressões](/help/search-social-commerce/glossary.md#i-j) determinam o número de dias após a ocorrência de um clique pago ou de uma impressão de exibição/vídeo (respectivamente) em que o evento pode ser atribuído a uma conversão.

A equipe de implementação do Adobe Advertising trabalha com o anunciante para determinar o formato das tags de conversão que ele precisa implementar, identificar as páginas da Web em que cada tag de conversão deve ser inserida e, em seguida, fornecer as tags de conversão para implementar.
