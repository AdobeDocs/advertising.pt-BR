---
title: Sobre o rastreamento para o Search, Social e Commerce
description: Saiba mais sobre as opções de rastreamento para Search, Social e Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Sobre o rastreamento para o Search, Social e Commerce

Para acompanhar o desempenho de seus anúncios, a Pesquisa, o Social e o Comércio precisam de dados de impressão, clique, custo e conversão (transação) para seus anúncios. O Search, Social e Commerce usa esses dados para criar os modelos de previsão de dados necessários para otimizar seus portfólios de anúncios.

## Dados de custo, clique e impressão

Os recursos de Pesquisa, Social e Comércio recuperam dados de impressão, clique e custo diretamente do [redes de publicidade suportadas](/help/search-social-commerce/introduction/supported-inventory.md) todos os dias. Além disso, o Search, Social e Commerce pode adicionar um código de rastreamento de cliques exclusivo (incluindo um redirecionamento para um servidor de rastreamento) em seus modelos de rastreamento e URLs de destino para rastrear impressões de exibição/conteúdo, cliques e custo, e depois vincular os eventos a conversões.

Se você quiser rastrear campanhas em redes de anúncios com as quais a Search, o Social e o Commerce não sincronizam dados, será necessário fornecer dados para essas campanhas enviando um arquivo de feed diário com dados de impressão, clique e custo.

### Tags de rastreamento de cliques

Sua equipe de implementação de Pesquisa, Social e Comércio configura o rastreamento de cliques atualizando os modelos de rastreamento e os URLs de destino para anúncios, palavras-chave, inserções, grupos de produtos e extensões de sitelink em suas campanhas de anúncios sincronizados para incluir uma sequência de ID de rastreamento exclusiva e um redirecionamento de publicidade Adobe. Eles também adicionam rastreamento aos sufixos de página de aterrissagem (sufixos de URL finais) para o seu [!DNL Google Ads] e [!DNL Microsoft Advertising] contas e campanhas.

Os parâmetros de rastreamento permitem que o Adobe Advertising rastreie cliques em um nível de palavra-chave individual (campanhas de pesquisa) ou nível de variação de anúncio (campanhas de pesquisa com direcionamento de conteúdo ou site, campanhas de exibição e campanhas sociais). Cada vez que um usuário visualiza um anúncio de exibição/conteúdo ou clica em um de seus anúncios, a rede de anúncios envia o evento para os servidores de pixels do Adobe Advertising usando uma tag de rastreamento de cliques associada à palavra-chave ou ao anúncio. Para cliques:

* Para anúncios do Google Ads e da Microsoft Advertising em navegadores que oferecem suporte ao rastreamento paralelo, a rede de anúncios envia o clique para o seu site primeiro e, em seguida, para os servidores de pixels do Adobe Advertising, que então colocam um cookie no computador do usuário, se ainda não existir um.

* Em todos os outros casos, a rede de publicidade envia o clique diretamente para os servidores de pixels de publicidade do Adobe. O servidor de pixels coloca um cookie no computador do usuário (se ainda não existir um) e, em seguida, redireciona o usuário para o URL relevante em seu site. A experiência geral para o usuário final é a mesma que seria sem um redirecionamento.

O cookie é definido na variável [!DNL Adobe] domínio (`everesttech.net`) como um cookie próprio. Após um redirecionamento, o usuário fica no domínio do anunciante e o cookie é tratado como um cookie de terceiros. Para obter mais informações sobre cookies de publicidade do Adobe, consulte &quot;[Cookies de publicidade do Adobe](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Dados de conversão

Quando um cliente clica em um anúncio ou visualiza uma exibição ou anúncio social, Search, Social e Commerce precisa mapear cada conversão resultante de volta para o clique ou exibição/impressão social de origem.

O anunciante desempenha uma função no fornecimento dos dados de conversão para todos os cliques e impressões sociais/de exibição. Os dados de conversão podem incluir informações sobre qualquer tipo de evento que ocorra em um site que possa ser usado para otimização de lances. Você pode fornecer dados de conversão implementando o código de rastreamento de conversão nas páginas de conversão do anunciante (como a página de &quot;sucesso&quot; exibida depois que um cliente conclui uma transação) ou enviando um arquivo de feed diário com dados de conversão capturados por outro método.

### Tags de rastreamento de conversão

Você pode usar [tags de conversão de vários fornecedores](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Quando você usa uma tag de conversão de Adobe e um usuário conclui uma transação bem-sucedida e chega a uma página de &quot;sucesso&quot;, o servidor de pixels de publicidade do Adobe verifica a existência do cookie no computador do usuário, que foi definido no momento do redirecionamento de clique. Quando encontra um cookie, as informações sobre o evento da transação são passadas usando o parâmetro ef_transid, e a transação é reconhecida como uma conversão e é creditada ao clique no anúncio anterior ou à impressão de exibição.

Se o usuário clicou em mais de um de seus anúncios, o Adobe Advertising credita a transação ao clique de anúncio final ou (para campanhas de exibição ou de vídeo) à impressão de anúncio final, a menos que você especifique o contrário. Seu [clique em janela de retrospectiva](/help/search-social-commerce/glossary.md#c-d) e [janela de retrospectiva de impressão](/help/search-social-commerce/glossary.md#i-j) determine o número de dias após um clique pago ou uma impressão de exibição/vídeo (respectivamente) ocorrer em que o evento pode ser atribuído a uma conversão.

A equipe de implementação do Adobe Advertising trabalha com o anunciante para determinar o formato das tags de conversão que ele precisa implementar, identificar as páginas da Web em que cada tag de conversão deve ser inserida e, em seguida, fornecer as tags de conversão para implementar.
