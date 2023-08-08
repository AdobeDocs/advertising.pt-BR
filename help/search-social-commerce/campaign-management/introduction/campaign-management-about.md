---
title: Sobre o gerenciamento de campanhas no Search, Social e Commerce
description: Saiba mais sobre os recursos de gerenciamento de campanhas em Pesquisa, Social e Comércio.
exl-id: e6fca48d-1f6c-4d36-a10d-e1a5db859a37
feature: Search Campaign Management
source-git-commit: d23b5a3c56c35fc5abbeafde681b9f584bf1c905
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Sobre o gerenciamento de campanhas no Search, Social e Commerce

O Search, Social, &amp; Commerce permite rastrear e/ou gerenciar suas campanhas de pesquisa, exibição/conteúdo, social, compras, público-alvo e desempenho máximo em um único local. Dependendo da rede de anúncios e do tipo de campanha, as funcionalidades disponíveis podem incluir a sincronização com suas redes de anúncios, criar e editar capacidades, rastreamento e atribuição de conversão, relatórios e otimização de orçamento e oferta. Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

À medida que você adiciona e edita dados da campanha no [!UICONTROL Campaigns] visualizações, Pesquisa, Social e Comércio enviam imediatamente as alterações de dados para a rede de anúncios. O Search, Social e Commerce também extrai dados de estrutura de campanha e dados de cliques de contas de rede de anúncios sincronizadas uma vez por dia (ou com mais frequência quando novas campanhas são detectadas) e sob demanda, conforme solicitado.

## Configuração do acesso às suas contas de rede de anúncios

Para acompanhar o desempenho dos anúncios na conta de rede de anúncios de um anunciante (e potencialmente fazer ofertas para os anúncios), a Equipe de conta da Adobe [cria um registro de conta correspondente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) em Pesquisa, Social e Comércio. O registro da conta inclui opções de rastreamento.

Para contas sincronizadas por meio da API da rede de anúncios, o registro da conta também inclui as credenciais de acesso da conta. Quando a conta está ativada, os dados são obtidos do com a rede de publicidade. Em seguida, é possível visualizar os dados da conta existentes, bem como criar e editar a estrutura da campanha e os dados de anúncios.

## Rastreamento de cliques para vincular cliques a conversões

Se você usa o serviço de rastreamento de conversão de Adobe Advertising, deve incluir o código de rastreamento de cliques de Pesquisa, Social e Comércio no sufixo da página de aterrissagem, modelos de rastreamento e URLs finais/de destino para anúncios, palavras-chave e inserções, links para sites e listas de produtos. Para [redes de publicidade e tipos de campanha compatíveis](/help/search-social-commerce/introduction/supported-inventory.md) cujas configurações de campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente seu próprio redirecionamento e código de rastreamento ao salvar o registro, de modo que não é necessário adicioná-lo manualmente. Caso contrário, você deve adicionar manualmente o código aos modelos de rastreamento ou URLs finais.

Para obter mais informações sobre rastreamento, consulte o capítulo em &quot;Rastreamento&quot;.

## Automatização do gerenciamento de lances e orçamentos

Para [redes de publicidade e tipos de campanha compatíveis](/help/search-social-commerce/introduction/supported-inventory.md), você pode agrupar suas campanhas em portfólios, cada um com um objetivo de negócios específico e um orçamento ou meta de desempenho específica. Em portfólios padrão, o Search, Social e Commerce otimiza ofertas de palavras-chave CPC e orçamentos de campanha. Os portfólios híbridos combinam tecnologias de otimização de pesquisa, social e comércio e suas redes de anúncios.

Para obter mais informações sobre as opções de portfólio disponíveis e como configurar portfólios, consulte o capítulo do Guia de otimização em &quot;Portfolio&quot;, que está disponível no Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

## As visualizações do gerenciamento de campanhas

As visualizações de gerenciamento de campanhas permitem monitorar e gerenciar as contas de pesquisa. As seguintes opções estão disponíveis:

* **[!UICONTROL Campaigns]** — A [!UICONTROL Campaigns] as exibições mostram dados de cada conta de rede de publicidade conectada. Você pode visualizar dados de custo, clique, impressão e receita em todas as contas de rede de publicidade e em contas individuais, campanhas, grupos de anúncios, palavras-chave, anúncios, grupos de produtos de compras, posicionamentos, direcionamentos automáticos (direcionamentos de pesquisa dinâmica), públicos-alvo e bibliotecas de extensão de anúncios e suas entidades de conta associadas. Para [tipos de campanha compatíveis em redes de anúncios compatíveis](/help/search-social-commerce/introduction/supported-inventory.md), você pode criar e editar dados para campanhas individuais e componentes de campanha diretamente na interface. Opcionalmente, é possível exportar os dados na maioria das subexibições para um arquivo de planilha.

  >[!NOTE]
  >
  >Os dados no nível do anúncio não estão disponíveis para [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA), desempenho máximo, compras inteligentes e [!DNL YouTube] campanhas.

* **[!UICONTROL Products]** — A [!UICONTROL Products] as exibições mostram dados para cada [[!DNL Google] or [!DNL Microsoft] conta do centro de comércio que está sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). O padrão [!UICONTROL Accounts] A subvisualização lista todas as contas sincronizadas; alguns tipos de usuários podem adicionar novas contas a partir desta visualização. A variável [!UICONTROL Products] A subexibição lista cada produto na conta.

* **[!UICONTROL Advanced (ACM)]** — Do [!DNL Advanced] ([!DNL AMC], para o Campaign Management avançado), é possível configurar processos automatizados para criar [anúncios dinâmicos e palavras-chave direcionados a cada item do inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) de acordo com um modelo de anúncio específico da rede de anúncios que você cria e o conteúdo de [!DNL Google Merchant Center] contas ou arquivos de dados de inventário carregados em um local FTP. As exibições secundárias mostram detalhes sobre cada modelo de feed para o anunciante e cada campanha, grupo de anúncios, palavra-chave e anúncio incluído em um feed que foi propagado por meio de um modelo de feed, mas não publicado na rede de anúncios.

* **[!UICONTROL Bulksheets]** — Utilizar o [!UICONTROL Bulksheets] exibir para criar [arquivos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contendo quantos dados você desejar para uma conta em uma [rede de publicidade compatível](/help/search-social-commerce/introduction/supported-inventory.md)e depois as publique na rede de publicidade.

* **[!UICONTROL Audiences]** — [A variável [!UICONTROL Audiences] visualizações](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) lista todos os seus [!DNL Google Ads] e [!DNL Microsoft Advertising] públicos-alvo gerados de vários tipos de listas de usuários. Você pode criar [!DNL Google Ads] públicos-alvo dos públicos-alvo existentes da Adobe Experience Cloud e das listas de email dos clientes. Você também pode visualizar e gerenciar metas de público-alvo e exclusões para o seu [!DNL Google Ads] e [!DNL Microsoft Advertising] anúncios.

* **[!UICONTROL Label Classifications]** — Use esta exibição para criar e excluir [classificações de etiquetas](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), que podem ajudá-lo a agrupar seus rótulos em conjuntos significativos.

>[!MORELIKETHIS]
>
>* [Visão geral da implementação de contas e campanhas de rede de anúncios](campaign-implemention-overview.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Dados de conversão do Google Ads em Pesquisa, Social e Comércio](google-conversion-data.md)
