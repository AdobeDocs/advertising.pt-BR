---
title: (Nova interface do usuário) Sobre contas de rede de anúncios
description: Saiba mais sobre contas de rede de anúncios na nova interface do Search, Social e Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Nova interface do usuário) Sobre contas de rede de anúncios

Search, Social e Commerce podem rastrear qualquer conta de um anunciante em redes de anúncios compatíveis. Para habilitar o rastreamento de uma conta, você deve criar um registro de conta correspondente. Você deve configurar os detalhes de qualquer tipo de conta, seja Pesquisa, Social e Commerce sincronizados ou otimizados lances e orçamentos em seus anúncios.

## Contas sincronizadas por meio de APIs

*[!DNL Google Ads], [!DNL Microsoft Advertising] (antigo [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e contas [!DNL Baidu] existentes*

O Search, Social e Commerce sincroniza (*sincronizações*) com contas de rede de anúncios com suporte, para que você possa acompanhar, relatar e visualizar o desempenho de seus anúncios. Para todas as redes de anúncios, exceto para [!DNL Yahoo! Display Network], você pode opcionalmente gerenciar as campanhas para sua conta em Search, Social, &amp; Commerce; [!DNL Yahoo! Display Network], as campanhas são somente leitura. Para todas as redes de anúncios, você pode permitir o recurso de otimização para ofertas, orçamentos de campanha e metas de estratégia de oferta de campanha para campanhas em contas gerenciadas, adicionando as campanhas aos portfólios.

Para habilitar a sincronização de uma conta, o registro da conta deve conter as credenciais de acesso da conta e estar habilitado (ativo).

Durante a sincronização, a Pesquisa, o Social e o Commerce extrai as estruturas de campanha do anunciante e as entidades de campanha compatíveis, incluindo a maioria de seus atributos gerenciados ou relatados na Pesquisa, no Social e no Commerce. Ela não inclui dados de cliques, nem lances e modificadores de lances inseridos fora da Pesquisa, Social e Commerce, que são coletados separadamente. O Search, Social e Commerce sincroniza automaticamente com suas contas de rede de anúncios uma vez por dia e sempre que detecta uma nova campanha em uma de suas redes de anúncios. Além disso, envia imediatamente todas as alterações nos dados da campanha feitas no Search, Social e Commerce para a rede de anúncios. Opcionalmente, você pode solicitar uma sincronização manual quando necessário.

Para obter mais informações sobre como criar e editar campanhas sincronizadas, consulte o capítulo sobre &quot;Gerenciamento de campanhas&quot;.

## Contas para as quais você faz upload manual de dados

Para redes de anúncios online para as quais a Search, Social e Commerce não oferece suporte a API, você pode fazer upload de conteúdo de campanha e de custo offline, cliques e dados de conversão de uma conta para relatórios e simulações de desempenho. O Search, Social e Commerce não sincroniza dados com a rede de anúncios, fornece lances automatizados ou qualquer tipo de otimização, mas permite simplificar insights entre canais e identificar oportunidades de otimização manual.

## Contas somente de rastreamento baseadas em modelo

*Disponível somente para contas [!DNL Naver] existentes*

As campanhas de rastreamento permitem rastrear, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios. O Search, Social e Commerce não sincroniza dados com a rede de anúncios, fornece lances automatizados ou fornece qualquer tipo de otimização ou simulações.

Para permitir que o Search, Social e Commerce atribua conversões a cliques, configure opções de rastreamento no registro de conta e habilite o registro de conta. Você pode usar bulksheets para gerar URLs de rastreamento para seus anúncios e palavras-chave e adicionar manualmente as URLs de rastreamento no gerenciador de anúncios [!DNL Naver].

Você não pode configurar novas contas do [!DNL Naver] no Search, Social e Commerce. Veja mais informações sobre [!DNL Naver] campanhas somente de rastreamento, consulte &quot;[Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gerenciar contas de rede de publicidade por meio da conexão com a API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Gerenciar contas de rede de publicidade para carregamentos de dados](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Gerenciar [!DNL Naver] contas apenas para rastreamento](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Gerenciar contas do centro de comércio](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
