---
title: Visão geral da implementação de contas e campanhas de rede de anúncios
description: Saiba mais sobre as tarefas envolvidas na configuração, sincronização e gerenciamento de suas contas de rede de anúncios.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Visão geral da implementação de contas e campanhas de rede de anúncios

O Adobe trabalha com cada anunciante para configurar suas contas e campanhas de rede de anúncios. Isso inclui configurar o Search, Social e Commerce para se conectar e sincronizar com as contas do anunciante, criar novas campanhas e componentes de campanha conforme necessário, configurar o rastreamento para os anúncios de componentes, adicionar opcionalmente as campanhas aos portfólios para permitir que o Search, Social e Commerce otimizem ofertas nos anúncios e validar os dados iniciais de custo, clique e receita.

Depois que uma campanha é ativada e opcionalmente adicionada a um portfólio, a equipe de gerenciamento de contas do Adobe, a equipe da agência ou o anunciante (dependendo dos termos do contrato de nível de serviço) precisarão monitorar cada campanha e alterar os componentes e as configurações relevantes, conforme necessário, para atender às metas do anunciante.

Esta página inclui informações sobre todos os tipos de conta, incluindo como configurar a estrutura de campanha para contas sincronizadas. Para obter instruções adicionais sobre como configurar contas somente de rastreamento para [!DNL Naver], consulte &quot;[Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

## Tarefas de configuração inicial para contas e campanhas

[!DNL Adobe] e/ou sua agência trabalharão com você da seguinte maneira:

1. (Novas contas de anunciante) Configurar contas administrativas:

   1. Configure a conta do anunciante.

   1. (Se necessário) Crie contas de usuário para o anunciante exibir e gerenciar seus dados de campanha e gerar relatórios.

1. (Algumas redes de anúncios) Obtenha autorização para o Search, Social e Commerce acessarem cada conta usando a API da rede de anúncios e a interface do usuário do Search, Social e Commerce.

1. Para cada conta de rede de publicidade:

   1. (Se necessário) Configure a conta na rede de publicidade.

   1. Integre com a conta [criando um registro de conta correspondente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) em Pesquisa, Social e Commerce contendo as credenciais de acesso e as opções de rastreamento da conta, e defina o status da conta como habilitado.

      O Search, Social e Commerce sincroniza com a rede de anúncios. Se a conta já tiver dados de campanha, os dados estarão disponíveis em cerca de 24 horas.

   1. ([Tipos de anúncios que você pode criar/editar](/help/search-social-commerce/introduction/supported-inventory.md) em Search, Social e Commerce) Se a conta ainda não tiver dados de campanha, crie a estrutura de campanha e os componentes da campanha em Search, Social e Commerce por qualquer um dos métodos a seguir que estejam disponíveis para o tipo de anúncio:

      * (Google Ads, Microsoft Advertising, Yahoo! Contas do Yandex e de anúncios somente) Configure um [processo automatizado para criar anúncios dinâmicos e palavras-chave direcionados a cada item no inventário](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) de acordo com um modelo de anúncio específico da rede de anúncios que você criar e o conteúdo dos arquivos de dados de inventário que você carregar para um local FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Anúncios do Japão e contas do Yandex somente) Faça upload de [arquivos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contendo quantos dados você quiser para uma conta e, em seguida, poste-os para as redes de publicidade.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! contas do Japan Ads e do Yandex somente) Insira dados para componentes individuais diretamente na interface. Para a maioria dos tipos de campanha e anúncios, você pode criar dados no nível da campanha, no nível do grupo de anúncios e nos níveis de palavra-chave, posicionamento e anúncio individuais.

      Alguns tipos de campanha e anúncios, no entanto, exigem workflows exclusivos. Consulte as instruções para configurar [[!DNL Microsoft Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads] anúncios de pesquisa dinâmica](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads] campanhas de desempenho máximo](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) e [[!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. (Somente contas de rastreamento do [!DNL Naver]) Carregue [arquivos de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) com dados para replicar as campanhas, grupos de anúncios e palavras-chave existentes no Search, Social e Commerce, sem postá-los no [!DNL Naver].

1. Configure o rastreamento de todos os anúncios para os quais o Adobe Advertising rastreará conversões:

   1. (Anunciantes com o serviço de rastreamento de conversão de Adobe Advertising) Se necessário, [configure o rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) para anúncios e, opcionalmente, para palavras-chave, inserções e extensões de anúncios, gerando e carregando URLs de rastreamento de cliques de Pesquisa, Social e Commerce.

      Para campanhas de desempenho máximo de [!DNL Google Ads], configure todo o rastreamento nas [configurações de rastreamento da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Para campanhas somente de rastreamento, você deve gerar URLs de destino usando bulksheets e, em seguida, adicionar os URLs de destino gerados às entidades relevantes usando o editor nativo da rede de publicidade.

   1. Configurar o rastreamento de conversão. Dependendo da implementação, isso pode envolver a adição de tags de rastreamento de conversão às páginas da Web do anunciante e/ou a configuração de uma queda de feed diária para dados de conversão que o anunciante coletou separadamente.

      Se você usa o serviço de rastreamento de conversão de Adobe Advertising, é possível gerar as tags de rastreamento de conversão [no Search, Social e Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) ou [usando o Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Valide os dados que são rastreados.

   Para obter mais detalhes sobre como configurar o rastreamento, consulte o capítulo em &quot;Rastreamento&quot;.

1. (Anunciantes com o Adobe Analytics) [Integre o Adobe Advertising e o Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) para que eles possam trocar dados.

1. (Para permitir que o Search, Social e &amp; Commerce otimizem ofertas, orçamentos de campanha e/ou alvos de estratégia de oferta de campanha; [somente tipos de campanha com suporte](/help/search-social-commerce/introduction/supported-inventory.md)) [Atribua a campanha a um portfólio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Se o portfólio ainda não tiver sido iniciado (otimização de lances e/ou orçamentos), deixe o recurso de otimização coletar dados suficientes para criar modelos de custo e receita para que você possa estabelecer o desempenho da linha de base para o portfólio antes de iniciá-lo.

   Se o portfólio já tiver sido iniciado, ative o aprendizado para o portfólio. Para obter mais informações, consulte &quot;Ajustar as estratégias de portfólio&quot;. Você deve esperar que o portfólio seja volátil depois de adicionar novas campanhas, enquanto o recurso de otimização coleta dados nas unidades de oferta da campanha. A licitação é automaticamente ajustada em uma a três semanas.

   Para obter mais informações sobre portfólios, consulte o Guia de Otimização, disponível no Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Se quaisquer novas conversões forem rastreadas para o anunciante) [Disponibilize as conversões](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) para relatórios, exibições de gerenciamento de campanhas e objetivos de portfólio.

1. Para cada campanha, verifique se o Search, Social e Commerce está recebendo dados de cliques e custos da rede de anúncios e valide os dados de receita exibidos em Search, Social e Commerce com os dados de receita do próprio anunciante.

1. (Opcional) Automatize os relatórios configurando modelos de relatório, feeds de planilha e entrega FTP de relatórios agendados.

   Para obter instruções, consulte o capítulo em &quot;Relatórios&quot;.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de campanhas no Search, Social e Commerce](campaign-management-about.md)
>* [Monitore e gerencie o desempenho de suas campanhas de rede de anúncios](monitor-performance-campaigns.md)
>* [Dados de conversão do Google Ads em Pesquisa, Social e Commerce](google-conversion-data.md)
>* [Estoque com suporte](/help/search-social-commerce/introduction/supported-inventory.md)
