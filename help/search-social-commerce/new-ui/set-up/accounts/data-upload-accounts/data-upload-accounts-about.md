---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Sobre o upload de dados da conta para relatórios e simulações

<!-- Move all related files into one page? -->

Se você usa redes de anúncios online para as quais a Search, Social e Commerce não oferece suporte a API, é possível fazer upload de conteúdo da campanha e custo offline, cliques e dados de conversão de uma conta para relatórios e simulações de desempenho. Os anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md) também podem exibir dados para suas contas no Adobe Analytics.

Esse recurso está disponível para redes de anúncios que seguem a estrutura padrão de três camadas da campanha (campanha, grupo de anúncios ou conjunto de anúncios e unidade de oferta (anúncio ou palavra-chave)). Para o Adobe DSP, o recurso está disponível para pacotes e as disposições atribuídas a um pacote, mas não para campanhas nem disposições com ritmo de nível de disposição.

O suporte pronto para uso está disponível para as seguintes redes:<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

O rastreamento de cliques de Search, Social e Commerce e o rastreamento de conversão do Adobe Advertising não são compatíveis com esse recurso.

## Funcionalidade disponível no Search, Social e Commerce

* Rastreamento e relatórios:

   * Componentes de campanha somente leitura até o nível de unidade de oferta nas visualizações de gerenciamento de campanha.

   * Dados de desempenho até o nível do grupo de anúncios <!-- verify the entity level --> nas exibições de gerenciamento de campanhas e relatórios personalizados. Anunciantes com [!DNL Adobe Analytics for Advertising]) também obtêm dados de desempenho até o nível de grupo de anúncios <!-- verify the entity level --> nos conjuntos de relatórios do Adobe Analytics especificados para o anunciante.&lt;!— Verifica se os tipos de dados são limitados — custo, clique, impressão de exibição, receita? —>

* Simulações de desempenho quando você adiciona as campanhas a um portfólio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social e Commerce não otimizam nada, nem fazem ofertas para esses tipos de campanhas em um portfólio.

## Fluxo de trabalho para configurar contas offline

<!-- subtitle wording? -->

1. [Configurar um registro de conta fictício](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Crie um arquivo de dados para uma única conta <!--  in what file format? -->, incluindo o status no nível do dia para campanhas, grupos de anúncios e anúncios.

Os dados devem seguir os requisitos de dados da rede de anúncios, de modo que os campos de dados de cada entidade possam variar de acordo com a rede de anúncios.

1. &#x200B;<!-- For all ad networks (excluding DSP), -->Faça upload dos dados iniciais de uma única conta de uma das seguintes maneiras:

* Faça upload manual de um arquivo do seu dispositivo ou rede.

* Carregar os dados para uma pasta atribuída à Search, Social e Commerce em um bucket do [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

  >[!PREREQUISITES]
  >
  >* Entre em contato com a equipe de conta da Adobe para ativar os uploads de dados da conta para sua conta de anunciante do Search, Social e Commerce. A equipe facilitará a criação de uma pasta específica da organização em um bucket do [!DNL S3], e avisará quando ele for concluído.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Recupere o caminho de armazenamento na nuvem [!DNL S3], a ID da chave de acesso e a chave de acesso secreta para sua conta. A mesma ID de chave de acesso e chave de acesso secreta são usadas para todas as contas de upload de dados da organização do <!-- naming convention?-->.

1. Continue a fazer upload de novos arquivos de dados diariamente.

1. Após carregar os dados por 30 dias, você pode, opcionalmente, adicionar as campanhas aos portfólios <!--what type? how should we refer to them? --> e gerar simulações.

Você pode [exibir um log de cada carregamento de dados](upload-log.md) para ver seu status. Além disso, se você iniciar um carregamento, mas ele não for bem-sucedido, você receberá uma notificação de erro por meio da [Central de notificações](/help/search-social-commerce/notifications/notification-about.md), com base nas configurações de notificação.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [Sobre o carregamento de dados da conta para relatórios e simulações](data-upload-accounts-about.md)
>* [Carregar dados da conta para um bucket [!DNL Amazon] [!DNL S3]](upload-data-from-s3-bucket.md)
>* [Carregar dados da conta manualmente](upload-data-manually.md)
>* [Exibir um log de arquivos de dados de conta carregados](upload-log.md)
>* [Gerenciar contas de rede de publicidade para carregamentos de dados](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
