---
title: '[!DNL Microsoft® Advertising] configurações da campanha'
description: Referenciar as configurações de [!DNL Microsoft® Advertising] campanhas.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 22fd10dec43c43c6f03860e6e4839a8bb8d56017
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] configurações da campanha

## \[Tela de criação da campanha\]

**[!UICONTROL Campaign Type]:** (Disponível somente durante a criação da campanha) Onde colocar anúncios e quais tipos de anúncios a campanha pode conter:

* *[!UICONTROL Search]:* Mostra anúncios de texto na rede de pesquisa.

* *[!UICONTROL Shopping Network]:* Mostra anúncios de produtos — para os seus produtos na [!DNL Microsoft® Merchant Center] catálogo de produtos — na rede de compras.

* *[!UICONTROL Audience]:* Mostra anúncios nativos/de exibição na [!DNL Microsoft® Audience Network]. Você pode a) gerar automaticamente anúncios baseados em feed, vinculando a campanha a uma loja de centro de comércio na [!UICONTROL Shopping Settings] ou b) crie anúncios responsivos com ativos de texto e imagens carregadas. Ambas as opções exigem que você crie grupos de anúncios com direcionamento de usuário.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Recurso Beta) Promove seus produtos por meio de varejistas vinculados nas redes de pesquisa e público-alvo. Você pode criar grupos de anúncios secundários e grupos de produtos (aplicativos para promover), além de anúncios de produtos opcionais para a campanha; [!DNL Microsoft® Advertising] O cria anúncios automaticamente para os grupos de produtos.

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Recurso Beta) Promove seus aplicativos e jogos que estão disponíveis na [!DNL Microsoft® Store]. Você pode criar grupos de anúncios secundários, grupos de produtos e anúncios de produtos opcionais para a campanha; [!DNL Microsoft® Advertising] O cria anúncios automaticamente para os grupos de produtos.

* *[!UICONTROL Audience Video]:* (Recurso Beta) Mostra anúncios de vídeo padrão na rede de público-alvo.

* *[!UICONTROL Audience Video]:* (Recurso Beta) Mostra anúncios de vídeo de TV conectada (CTV) na rede de público-alvo.

* *[!UICONTROL Performance Max]:* (Recurso Beta) Mostra vários tipos de anúncios em todas as redes. Atribuir grupos de ativos separadamente dentro do [!DNL Microsoft® Advertising] editor de anúncios.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo na conta. O comprimento máximo é de 128 caracteres.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativo* ou *Pausado*. O padrão para novas campanhas de publicidade é *Ativo*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** A estratégia de oferta da campanha:

* *[!UICONTROL CPV]* (Somente campanhas de vídeo de CTV de público-alvo) Usa o modelo de custo por visualização (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campanhas nas redes de público, pesquisa e compras) Usa o modelo de custo por clique (eCPC) aprimorado da rede de anúncios, o que permite que a rede de anúncios altere automaticamente a oferta de custo por clique (CPC) para cada leilão, em uma tentativa de maximizar as conversões, usando conversões especificadas na rede de anúncios (não em Pesquisa, Social e Comércio), enquanto tenta manter o CPC médio abaixo do seu CPC máximo.

  Ao adicionar uma campanha com eCPC a um portfólio otimizado de Pesquisa, Social e Comércio, o Search, Social e Comércio otimiza as ofertas básicas e, quando &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; opção está ativada — o orçamento da campanha. A rede de publicidade otimiza todos os ajustes de oferta e pode alterar as ofertas geradas por Pesquisa, Social e Comércio no momento da consulta do usuário com base em dados e insights proprietários. **Atenção:** Use campanhas eCPC em portfólios somente quando o total de conversões rastreadas na rede de anúncios estiver alinhado ao objetivo do portfólio.

* *[!UICONTROL Manual CPC]*: (campanhas de compras para marcas; [!DNL Microsoft Store Ads] campanhas; descontinuado por [!DNL Microsoft® Advertising] em 2021 para outros tipos de campanha) Usa o modelo de custo por clique (CPC). Para alguns tipos de anúncios, você pode permitir que a rede de anúncios altere ofertas para a campanha:

   * **[!UICONTROL Enable Enhanced CPC]** (desativado por padrão): é o mesmo que usar o &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campanhas) Usa o modelo de custo por aquisição (CPA).

* *[!UICONTROL Manual CPM]* (Somente campanhas de público e campanhas de vídeo de público) Usa o modelo de custo por mil impressões (CPM), para o qual você especifica o que deseja gastar por 1.000 impressões visualizadas. Campanhas com essa estratégia de oferta não são otimizadas quando são incluídas em portfólios.

* *[!UICONTROL Maximize Clicks]:* (Campanhas de pesquisa e compras) A rede de publicidade — não de pesquisa, social e comércio — otimiza ofertas para maximizar os cliques. Opcionalmente, informe um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de anúncios não pague mais do que um valor específico para cada clique. **Atenção:** Quando você adiciona uma campanha com essa estratégia a um portfólio, as ofertas são orientadas pelo peso dos cliques, não pelo objetivo do portfólio.

* *[!UICONTROL Maximize Conversion Value]:* (Redes de pesquisa e compras/compras inteligentes, campanhas de desempenho máximo) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas para maximizar o valor de conversão. Opcionalmente, informe um **[!UICONTROL Target Return on Ad Spend]** (ROAS) como uma porcentagem. **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Maximize Conversions]:* (Campanhas na rede de pesquisa <!-- future: and audience network -->, desempenho máximo de campanhas) A rede de anúncios — não de Pesquisa, Social e Comércio — otimiza ofertas para maximizar as conversões. Opcionalmente, informe um **[!UICONTROL Target CPC]** (custo por clique)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Target CPA]:* (Campanhas na rede de pesquisa) A rede de publicidade — não Pesquisar, Social e Comércio — otimiza ofertas com base em uma **[!UICONTROL Target CPA]** (custo por aquisição), que é o valor médio de 30 dias que você deseja pagar por uma aquisição (conversão). **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campanhas na rede de pesquisa) A rede de publicidade — não Pesquisar, Social e Comércio — otimiza ofertas para alcançar um compartilhamento de impressões alvo e uma posição de anúncio. Opcionalmente, informe um **[!UICONTROL Target Impression Share]** em porcentagem, a variável **[!UICONTROL Target Ad Position]**, e uma **[!UICONTROL Max CPC]** (custo por clique). **Nota:** Essa opção não é compatível com portfólios híbridos.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campanhas nas redes de pesquisa e compras) A rede de anúncios, e não a Search, Social e Commerce, otimiza ofertas com base em suas **[!UICONTROL Target ROAS]** (retorno do investimento em publicidade), especificado como uma porcentagem. Opcionalmente, informe um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de anúncios não pague mais do que um valor específico para cada clique. **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Somente campanhas de compras; somente leitura para campanhas existentes) O país no qual os produtos da campanha são vendidos. Como os produtos são associados aos países de destino, essa configuração determina quais produtos são anunciados na campanha.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Somente campanhas de público; opcional) Vincula a campanha a uma loja do centro de comércio específica para anúncios com base em feed automatizados, em vez de anúncios responsivos. Ao selecionar essa opção, especifique o [!UICONTROL Merchant ID] e [!UICONTROL Products]. É necessário criar grupos de anúncios para a campanha, mas não é necessário criar anúncios.

Depois de vincular a campanha a uma loja e salvar as configurações, não é possível alterar essa opção.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Campanhas de público-alvo vinculadas somente a uma loja de centro de comércio) Os produtos a serem anunciados. Por padrão, *[!UICONTROL All products]* está selecionada. Para anunciar apenas produtos com atributos específicos, selecione *[!UICONTROL Filter products]* e especifique até sete combinações de dimensão e atributo de produto nas quais filtrar seus produtos. Todos os valores especificados devem ser aplicáveis para que os anúncios apareçam para o produto. Por exemplo, para mostrar anúncios de suprimentos para animais de estimação da Acme, você pode criar os filtros `Custom Label 1=animals`, `Category=pet supplies`, e `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campanhas somente na exibição/rede nativa; opcional) Sites na rede de exibição na qual você não deseja que seus anúncios sejam exibidos. Insira um URL válido, como www.example.com. Para especificar várias cadeias de caracteres, separe-as com vírgulas ou insira-as em linhas separadas.

Para obter informações sobre disponibilidade, consulte a ajuda da Microsoft® Advertising para &quot;[Impedir a exibição de anúncios em sites específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Para [!UICONTROL EF Redirect] somente) Não implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se deseja *[!UICONTROL Use account conversion goals for this campaign]* (o padrão) ou *[!UICONTROL Use campaign specific conversion goals]*. Se você optar por especificar metas de conversão para a campanha, selecione as metas na lista de todas as metas disponíveis. **Nota:** As metas são sincronizadas diariamente, portanto, as metas criadas nas 24 horas anteriores podem não ser listadas. Para atualizar a lista, [sincronizar manualmente os dados da rede de publicidade](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Se a campanha fizer parte de um portfólio, use as mesmas metas de conversão que o objetivo do portfólio. Usar diferentes metas de conversão pode afetar o desempenho do portfólio.

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
