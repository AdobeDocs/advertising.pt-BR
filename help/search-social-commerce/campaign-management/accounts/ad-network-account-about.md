---
title: Sobre contas de rede de publicidade
description: Saiba mais sobre contas de rede de anúncios em Pesquisa, Social e Comércio.
exl-id: fca469f1-502c-415a-897d-03b6e6ba34e8
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Sobre contas de rede de publicidade

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Search, Social e Commerce podem rastrear qualquer conta de um anunciante em redes de anúncios compatíveis. Para habilitar o rastreamento de uma conta, você deve criar um registro de conta correspondente. Você deve configurar os detalhes de qualquer tipo de conta, seja Pesquisa, Social e Comércio sincronizados ou otimizados lances e orçamentos em seus anúncios.

## Contas sincronizadas por meio de APIs

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] (antigo [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], e [!DNL Yandex] contas*

Sincronizações de Pesquisa, Social e Comércio (*sincronizações*) com contas de rede de publicidade compatíveis, para que você possa rastrear, relatar e visualizar o desempenho de seus anúncios. Para todas as redes de publicidade, exceto para [!DNL Yahoo! Display Network], você pode gerenciar opcionalmente as campanhas da sua conta no Search, Social, &amp; Commerce; [!DNL Yahoo! Display Network], as campanhas são somente leitura. Para todas as redes de anúncios, você pode permitir o recurso de otimização para ofertas de anúncios em contas gerenciadas ao adicioná-las aos portfólios.

Para habilitar a sincronização de uma conta, o registro da conta deve conter as credenciais de acesso da conta e estar habilitado (ativo).

Durante a sincronização, a Pesquisa, o Social e o Comércio extrai as estruturas de campanha do anunciante e as entidades de campanha compatíveis, incluindo a maioria de seus atributos gerenciados ou relatados na Pesquisa, no Social e no Comércio. Ela não inclui dados de cliques, nem ofertas e modificadores de ofertas inseridos fora da Pesquisa, Social e Comércio, que são coletados separadamente. O Search, Social e Commerce sincroniza automaticamente com suas contas de rede de anúncios uma vez por dia e sempre que detecta uma nova campanha em uma de suas redes de anúncios. Além disso, ele envia imediatamente todas as alterações nos dados da campanha feitas no Search, Social e Commerce para a rede de anúncios. Opcionalmente, você pode solicitar uma sincronização manual quando necessário.

Para obter mais informações sobre como criar e editar campanhas sincronizadas, consulte o capítulo sobre &quot;Campaign Management&quot;.

## Contas somente de rastreamento

*[!DNL Naver]Contas*

As campanhas de rastreamento permitem rastrear, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios. A Search, Social e Commerce não sincroniza dados com a rede de anúncios, faz ofertas para a conta, nem fornece qualquer tipo de otimização ou simulações.

Para permitir que o Search, Social e Commerce atribua conversões a cliques, configure opções de rastreamento no registro de conta e habilite esse registro. Você pode usar bulksheets para gerar URLs de rastreamento para seus anúncios e palavras-chave e adicionar manualmente os URLs de rastreamento na [!DNL Naver] gerente de publicidade.

Veja mais informações sobre [!DNL Naver] campanhas somente de rastreamento, consulte &quot;[Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gerenciar contas de rede de publicidade](ad-network-account-manage.md)
>* [Gerenciar contas do centro de comércio](merchant-account-manage.md)
>* [Atualizar o código de rastreamento da ID do AMO para um [!DNL Google Ads] account](update-amo-id-google.md)
