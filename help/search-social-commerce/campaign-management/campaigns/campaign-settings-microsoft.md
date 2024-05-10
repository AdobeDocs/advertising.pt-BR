---
title: '[!DNL Microsoft® Advertising] configurações da campanha'
description: Referenciar as configurações de [!DNL Microsoft® Advertising] campanhas.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1966'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] configurações da campanha

## \[Tela de criação da campanha\]

**[!UICONTROL Campaign Type]:** (Disponível somente durante a criação da campanha) Onde colocar anúncios e quais tipos de anúncios a campanha pode conter:

* *[!UICONTROL Search]:* Mostra anúncios de texto na rede de pesquisa.

* *[!UICONTROL Shopping Network]:* Mostra anúncios de produtos — para os seus produtos na [!DNL Microsoft® Merchant Center] catálogo de produtos — na rede de compras.

* *[!UICONTROL Audience]:* Mostra anúncios nativos/de exibição na [!DNL Microsoft® Audience Network]. Você pode a) gerar automaticamente anúncios baseados em feed, vinculando a campanha a uma loja de centro de comércio na [!UICONTROL Shopping Settings] ou b) crie anúncios responsivos com ativos de texto e imagens carregadas. Ambas as opções exigem que você crie grupos de anúncios com direcionamento de usuário.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Recurso Beta) Promove seus produtos por meio de varejistas vinculados nas redes de pesquisa e público-alvo. Você pode criar grupos de anúncios secundários e grupos de produtos (aplicativos para promover), além de anúncios de produtos opcionais para a campanha; [!DNL Microsoft® Advertising] O cria anúncios automaticamente para os grupos de produtos. Para campanhas de compra de marcas, use a estratégia de oferta [!UICONTROL Manual CPC]; para promoções de compras de marcas, use a estratégia de oferta [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Recurso Beta) Promove seus aplicativos e jogos que estão disponíveis na [!DNL Microsoft® Store]. Você pode criar grupos de anúncios secundários, grupos de produtos e anúncios de produtos opcionais para a campanha; [!DNL Microsoft® Advertising] O cria anúncios automaticamente para os grupos de produtos.

* *[!UICONTROL Audience CTV Video]:* (Recurso Beta) Mostra anúncios de vídeo de TV conectada (CTV) na rede de público-alvo.

* *[!UICONTROL Audience Video]:* (Recurso Beta) Mostra anúncios de vídeo padrão na rede de público-alvo.

* *[!UICONTROL Performance Max]:* (Recurso Beta) Mostra vários tipos de anúncios em todas as redes que usam [!DNL Microsoft® Advertising] oferta inteligente. Nas configurações da campanha, você deve especificar um ou mais grupos de ativos, que incluem imagens, logotipos, títulos, descrições, uma chamada para ação opcional e sinais de público-alvo. A rede de anúncios combina automaticamente os ativos para veicular anúncios com base no canal.

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

* *[!UICONTROL Cost per Sale]:* (Somente campanhas de compras) A rede de publicidade — não Search, Social e Commerce — otimiza ofertas com base na [!UICONTROL Target CPS] (custo por venda). Você paga somente quando um clique no anúncio do produto resulta em uma venda em 24 horas. **Nota:** Não inclua campanhas com essa estratégia de oferta em portfólios. A otimização de Pesquisa, Social e Commerce não está disponível para campanhas com essa estratégia de oferta.

  Depois de salvar uma campanha de compras para marcas com essa estratégia de oferta, você não pode alterar a estratégia de oferta. Para outros tipos de campanha de compras, essa estratégia está disponível somente para novas campanhas.

* *[!UICONTROL CPV]* (Somente campanhas de vídeo de CTV de público-alvo) Usa o modelo de custo por visualização (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campanhas nas redes de público, pesquisa e compras) Usa o modelo de custo por clique (eCPC) aprimorado da rede de anúncios, o que permite que a rede de anúncios altere automaticamente a oferta de custo por clique (CPC) para cada leilão, em uma tentativa de maximizar as conversões, usando conversões especificadas na rede de anúncios (não em Pesquisa, Social e Commerce), enquanto tenta manter o CPC médio abaixo do CPC máximo.

  Quando você adiciona uma campanha com eCPC a um portfólio otimizado de Pesquisa, Social e Commerce, o Search, Social e Commerce otimiza as ofertas básicas e, quando &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; opção está ativada — o orçamento da campanha. A rede de publicidade otimiza todos os ajustes de oferta e pode alterar as ofertas geradas pela Search, Social e Commerce no momento da consulta do usuário com base em dados e insights proprietários. **Atenção:** Use campanhas eCPC em portfólios somente quando o total de conversões rastreadas na rede de anúncios estiver alinhado ao objetivo do portfólio.

* *[!UICONTROL Manual CPC]*: (campanhas de compras para marcas; [!DNL Microsoft® Store Ads] campanhas; descontinuado por [!DNL Microsoft® Advertising] em 2021 para outros tipos de campanha) Usa o modelo de custo por clique (CPC). Para alguns tipos de anúncios, você pode permitir que a rede de anúncios altere ofertas para a campanha:

   * **[!UICONTROL Enable Enhanced CPC]** (desativado por padrão): essa opção é a mesma que usar o &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft® Store Ads] campanhas) Usa o modelo de custo por aquisição (CPA).

* *[!UICONTROL Manual CPM]* (Somente campanhas de público e campanhas de vídeo de público) Usa o modelo de custo por mil impressões (CPM), para o qual você especifica o que deseja gastar por 1.000 impressões visualizadas. Campanhas com essa estratégia de oferta não são otimizadas quando são incluídas em portfólios.

* *[!UICONTROL Maximize Clicks]:* (Campanhas de pesquisa e compras) A rede de publicidade — não Search, Social e Commerce — otimiza ofertas para maximizar os cliques. Opcionalmente, informe um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de anúncios não pague mais do que um valor específico para cada clique. **Atenção:** Quando você adiciona uma campanha com essa estratégia a um portfólio, o peso dos cliques (não o objetivo do portfólio) gera ofertas.

* *[!UICONTROL Maximize Conversion Value]:* (Redes de pesquisa e compras/compras inteligentes, campanhas de desempenho máximo) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas para maximizar o valor de conversão. Opcionalmente, informe um **[!UICONTROL Target Return on Ad Spend]** (ROAS) como uma porcentagem. **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Maximize Conversions]:* (Desempenho máximo de campanhas e campanhas na rede de pesquisa ou na rede de público (mas não de vídeos de público ou TV conectada) A rede de anúncios, não de Pesquisa, Social e Commerce, otimiza ofertas para maximizar as conversões. Opcionalmente, informe um **[!UICONTROL Target CPC]** (custo por clique). Para campanhas de público, você também pode inserir uma **[!UICONTROL Target CPA]** (custo por aquisição). **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Target CPA]:* (Campanhas na rede de pesquisa) A rede de publicidade — não a Search, Social e Commerce — otimiza ofertas com base em uma **[!UICONTROL Target CPA]** (custo por aquisição), que é o valor médio de 30 dias que você deseja pagar por uma aquisição (conversão). **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campanhas na rede de pesquisa) A rede de publicidade — não a Search, Social e Commerce — otimiza ofertas para atingir um compartilhamento de impressões de público-alvo e uma posição de anúncio. Opcionalmente, informe um **[!UICONTROL Target Impression Share]** em porcentagem, a variável **[!UICONTROL Target Ad Position]**, e uma **[!UICONTROL Max CPC]** (custo por clique). **Nota:** Essa opção não é compatível com portfólios híbridos.

* *[!UICONTROL Target Return on Ad Spend]:* (Campanhas nas redes de pesquisa e compras) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas com base em suas **[!UICONTROL Target ROAS]** (retorno do investimento em publicidade), especificado como uma porcentagem. Opcionalmente, informe um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de anúncios não pague mais do que um valor específico para cada clique. **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

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

**[!UICONTROL Languages]:** (Somente campanhas de desempenho máximo) O idioma do anúncio, que deve corresponder ao idioma dos sites nos quais o anúncio pode aparecer. [!DNL Microsoft® Advertising] determina o idioma de um usuário a partir de vários sinais, incluindo o query do usuário, o país do editor e a configuração de idioma do usuário.

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

## [!UICONTROL Asset Groups] (por grupo de ativos)

**[!UICONTROL Asset Group Name]:** O nome da pasta de ativos (grupo de ativos).

**[!UICONTROL Asset Group Status]:** O status do grupo de ativos: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** O URL final de todos os anúncios criados a partir do grupo de ativos.

**[!UICONTROL Images]:** Até 20 imagens para o anúncio, incluindo pelo menos uma imagem quadrada e uma imagem paisagem. Consulte a [[!DNL Microsoft® Advertising] diretrizes de imagem](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Você pode carregar imagens ou selecioná-las na sua [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para carregar imagens:

   1. No [!UICONTROL Upload from Device] clique em **[!UICONTROL +]** e selecione imagens do seu dispositivo ou rede.

   1. Para cada imagem:

      1. Selecione a taxa de proporção.

      1. Arraste e posicione a caixa de corte conforme necessário para selecionar a parte visível da imagem e redimensione a parte visível da imagem conforme necessário, quando possível.

      1. (Opcional) Selecione proporções adicionais e, opcionalmente, reposicione e redimensione a imagem conforme necessário para cada proporção selecionada.

         Um ativo é criado para cada taxa de proporção selecionada.

      1. Clique em **[!UICONTROL Proceed]**.

   1. Quando terminar de especificar imagens, clique em **[!UICONTROL Upload]**.

* Para selecionar imagens de seu [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione as imagens.

**[!UICONTROL Logos]:** Pelo menos um logotipo. É possível incluir até cinco. Consulte a [[!DNL Microsoft® Advertising] diretrizes do ativo](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Você pode carregar imagens ou selecioná-las na sua [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para carregar imagens:

   1. No [!UICONTROL Upload from Device] clique em **[!UICONTROL +]** e selecione imagens do seu dispositivo ou rede.

   1. Para cada imagem:

      1. Selecione a taxa de proporção.

      1. Arraste e posicione a caixa de corte conforme necessário para selecionar a parte visível da imagem e redimensione a parte visível da imagem conforme necessário, quando possível.

      1. (Opcional) Selecione proporções adicionais e, opcionalmente, reposicione e redimensione a imagem conforme necessário para cada proporção selecionada.

         Um ativo é criado para cada taxa de proporção selecionada.

      1. Clique em **[!UICONTROL Proceed]**.

   1. Quando terminar de especificar imagens, clique em **[!UICONTROL Upload]**.

* Para selecionar imagens de seu [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione as imagens.

**[!UICONTROL Headlines]:** Pelo menos três e até 15 títulos curtos com no máximo 30 caracteres cada. É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Long Headlines]:** Pelo menos uma e até cinco manchetes longas com no máximo 90 caracteres cada. É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Descriptions]:** Pelo menos duas e até cinco descrições com no máximo 90 caracteres cada. É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Call to Action]:** O plano de ação a ser incluído no anúncio. Por padrão, *[!UICONTROL Act Now]* está selecionada.

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres. Ele não pode conter scripts, HTML ou outro idioma de marcação.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Microsoft® Advertising] públicos-alvo a serem usados como sinais de público-alvo para a campanha. [!DNL Microsoft® Advertising] os modelos de aprendizado de máquina usam os públicos-alvo para encontrar navegadores da web semelhantes ao público-alvo e também podem mostrar anúncios para públicos-alvo que não são especificados como sinais para ajudar você a atingir suas metas de desempenho. Escolha os públicos-alvo com maior probabilidade de conversão.

>[!NOTE]
>Os sinais de público são diferentes dos [metas de público-alvo no nível do grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Permite especificar outro grupo de ativos.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se deseja *[!UICONTROL Use account conversion goals for this campaign]* (o padrão) ou *[!UICONTROL Use campaign specific conversion goals]*. Se você optar por especificar metas de conversão para a campanha, selecione as metas na lista de todas as metas disponíveis. **Nota:** As metas são sincronizadas diariamente, portanto, as metas criadas nas 24 horas anteriores podem não ser listadas. Para atualizar a lista, [sincronizar manualmente os dados da rede de publicidade](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Para portfólios híbridos para os quais você faz upload de objetivos na rede de publicidade, a prática recomendada é usar metas de nível de campanha que correspondam às metas de conversão no objetivo do portfólio. No entanto, se as metas da campanha incluírem conversões rastreadas pelo [!DNL Microsoft Advertising] universal event tracking (UET), em seguida, adicione-os na tag [!DNL Microsoft Advertising] editor porque eles não são recarregados na rede de publicidade com o objetivo. Além disso, no âmbito do [!DNL Microsoft Advertising] editor, remova as ações de conversão da campanha como metas padrão da conta ao desmarcar &quot;incluir em conversões&quot;.

<!-- Check on this:
>If the campaign is part of a hybrid portfolio, then use only conversion goals that are included in the portfolio's objective for the campaign. Including additional conversion goals may impact portfolio performance.
>
>The objective may include conversion goals or other conversions that aren't included for the campaign, but the campaign can't include conversion goals that aren't included in the objective.
-->

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
