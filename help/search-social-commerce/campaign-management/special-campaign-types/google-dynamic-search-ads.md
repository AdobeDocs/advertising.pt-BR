---
title: Implementar [!DNL Google Ads] anúncios de pesquisa dinâmica
description: Saiba mais sobre o fluxo de trabalho para configuração [!DNL Google Ads] anúncios de pesquisa dinâmica.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] anúncios de pesquisa dinâmica

*[!DNL Google Ads]campanhas somente de pesquisa com nível criativo ou nível de palavra-chave e nível criativo somente.*

Os anúncios de pesquisa dinâmicos usam o conteúdo de seu site, em vez de palavras-chave, para decidir quando mostrar seus anúncios. Você pode definir as páginas dos sites cujo conteúdo é usado para direcionar os anúncios de pesquisa dinâmica, configurando alvos de pesquisa dinâmica separados para o grupo de publicidade ou escolhendo uma configuração no nível da campanha para direcionar os anúncios usando o conteúdo do site.

Você pode configurar anúncios de pesquisa dinâmica individualmente ou usando bulksheets. As instruções a seguir incluem links para a criação de entidades individuais.

## Etapas para configurar [!DNL Google Ads] anúncios de pesquisa dinâmica

1. [Criar uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para anúncios de pesquisa dinâmica:

   1. Inicialmente, defina o orçamento da campanha para 10% do gasto diário com a campanha de pesquisa.

      Posteriormente, você pode aumentar o orçamento depois que os anúncios provarem seu valor.

   1. (Se desejar [!DNL Google Ads] para mostrar os anúncios de pesquisa dinâmica com base no conteúdo do site) Especifique o domínio raiz e o idioma para o domínio na [!UICONTROL DSA Options] seção das configurações da campanha.

      >[!NOTE]
      >
      >Seu domínio deve ser indexado pelo [!DNL Google Ads] índice de pesquisa orgânica a ser direcionado. Além disso, se o domínio contiver páginas em vários idiomas e você quiser direcionar todas elas, crie uma campanha separada para cada idioma.

      Se você não usar o domínio do site para direcionar anúncios, crie metas de pesquisa dinâmica (consulte a Etapa 4) para cada grupo de anúncios. Você pode criar os destinos [individualmente](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) ou usando [planilhas em massa](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Certifique-se de que a campanha seja direcionada ao canal de pesquisa e somente ao [!DNL Google Ads] rede de pesquisa (não a rede de exibição). Essas configurações estão disponíveis no [!UICONTROL Networks and Devices] guia.

   1. (Opcional) Excluir palavras-chave na [!UICONTROL Negatives] guia.

   1. (Opcional) Configure um modelo de rastreamento de nível de campanha, que substitui o modelo de rastreamento de nível de conta, mas pode ser substituído nos níveis inferiores.

      (Anunciantes com Adobe Analytics sem rastreamento do lado do servidor) Quando quiser incluir o rastreamento do feed reverso do Search, Social e Commerce para o Analytics, adicione o código de rastreamento da ID do AMO aos parâmetros de acréscimo no nível da conta, que adicionam o código ao URL final. Consulte &quot;[O parâmetro de rastreamento da ID do AMO](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Criar um grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) na campanha, incluindo as seguintes etapas:

   1. Defina o [!UICONTROL Ad Group Type] para **[!UICONTROL Search Dynamic].**

   1. Defina a oferta padrão para todos os anúncios.

      Você poderá substituir o lance padrão para destinos de pesquisa dinâmica individuais, se configurá-los.

   1. (Opcional) Configure um modelo de rastreamento do nível do grupo de anúncios, que substitui todos os modelos de rastreamento em níveis superiores, mas pode ser substituído no nível do anúncio.

      Se você adicionou o rastreamento de Adobe Analytics no nível da campanha e deseja incluí-lo no grupo de publicidade, adicione-o aqui. Consulte a Etapa 1e.

1. [Criar cada anúncio de pesquisa dinâmica](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) no grupo de publicidade.

   [!DNL Google Ads] gera dinamicamente o título, o URL de exibição e o URL da página inicial para cada anúncio. Opcionalmente, é possível adicionar redirecionamentos e rastreamento ao modelo de rastreamento de nível de anúncio, que substitui os modelos de rastreamento em níveis superiores.
Se você quiser substituir qualquer rastreamento de Adobe Analytics em níveis superiores com rastreamento no nível do anúncio, adicione-o aqui. Consulte as etapas 1e e 2c.

1. (Obrigatório quando você não inclui o domínio raiz e o idioma do domínio na seção Opções de DSA das configurações da campanha; opcional; caso contrário) Criar [destinos de pesquisa dinâmica](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) para o grupo de publicidade. Opcionalmente, você pode sobrepor o lance de nível de grupo de anúncios com lances de nível de destino.

   Os destinos definem se a rede de publicidade usa todas ou um subconjunto das páginas do site para direcionar seus anúncios de pesquisa dinâmica. Para melhor rastrear o desempenho, configure sua campanha com um grupo de anúncios por público alvo de pesquisa dinâmica e inclua um grupo de anúncios que segmente todos os critérios.

1. Se necessário, [editar as configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) para ajustar o orçamento da campanha e refinar o tráfego excluindo palavras-chave adicionais da campanha.
