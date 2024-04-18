---
title: '[!DNL Google Ads] configurações da campanha'
description: Referenciar as configurações de [!DNL Google Ads] campanhas.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 66f6f659e46d2a08e0f7b958be8f60ba5e9720b3
workflow-type: tm+mt
source-wordcount: '2378'
ht-degree: 0%

---

# [!DNL Google Ads] configurações da campanha

## \[Tela de criação da campanha\]

**[!UICONTROL Campaign Type]:** (Disponível somente durante a criação da campanha) Onde colocar anúncios e quais tipos de anúncios a campanha pode conter:

* *[!UICONTROL Search Network Only]:* Mostra anúncios na rede de pesquisa, que inclui [!DNL Google] resultados da pesquisa e, opcionalmente, pesquisar sites de parceiros. Você deve especificar palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Search with Display Select]:* Mostra anúncios na rede de pesquisa (que inclui [!DNL Google] resultados de pesquisa e, opcionalmente, pesquisar sites de parceiros) e potencialmente mostra anúncios em sites de rede de exibição. Na rede de exibição, [!DNL Google Ads] exibe seus anúncios de forma seletiva usando a licitação automatizada, independentemente da estratégia de oferta da campanha. Para anúncios de pesquisa, especifique palavras-chave para cada grupo de publicidade; para anúncios de exibição, especifique disposições e, opcionalmente, especifique palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Shopping Network]:* Mostra anúncios de produtos, que [!DNL Google] O é gerado automaticamente com base nos produtos na [!DNL Google Merchant Center] em [!DNL Google Shopping], a área ao lado de [!DNL Google] resultados de pesquisa (separados de anúncios de texto) e (opcionalmente) sites de parceiros de pesquisa. Para cada grupo de publicidade na campanha, você pode especificar grupos de produtos para anunciar.

* *[!UICONTROL Display Network Only]:* Mostra anúncios na rede de exibição. Para cada grupo de publicidade, você deve especificar disposições e pode, opcionalmente, especificar palavras-chave.

* *[!UICONTROL Performance Max]:* (Recurso Beta) Mostra e otimiza conversões para seus anúncios em canais usando [!DNL Google Ads] oferta inteligente. Nas configurações da campanha, você deve especificar um ou mais grupos de ativos, que incluem imagens, logotipos, títulos, descrições, vídeos opcionais e sinais de público-alvo. [!DNL Google Ads] combina automaticamente os ativos para veicular anúncios com base no canal (como [!DNL YouTube], [!DNL Gmail]ou [!DNL Search]).

  **Notas:**

   * Somente as configurações necessárias estão disponíveis. Para configurações opcionais, faça logon na [!DNL Google Ads] editor.

   * Links para [!DNL Google Merchant Center] os feeds de produto do não são compatíveis.

   * Não há suporte disponível para a listagem de grupos. Para gerenciar e exibir dados de grupos de listagem, efetue logon na [!DNL Google Ads] editor.

   * A otimização híbrida é compatível. As metas da estratégia de oferta e os orçamentos da campanha são definidos no nível da campanha.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo na conta.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Campanhas do Gmail somente leitura existentes) Se:

* *[!UICONTROL Target and Bid]* Para mostrar anúncios somente a usuários associados a públicos-alvo que também satisfaçam a quaisquer outros alvos para o grupo de anúncios.

* *[!UICONTROL Bid Only]:*  Para mostrar anúncios até mesmo a pessoas que não estão associadas a públicos-alvo, desde que atendam a outros alvos de nível de grupo de anúncios. No entanto, você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, definindo ofertas mais altas para esses públicos-alvo.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativo* ou *Pausado*. O padrão para novas campanhas de publicidade é *Ativo*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campanhas direcionadas somente à rede de pesquisa, incluindo campanhas de compras) Mostra seus anúncios nas redes de parceiros de pesquisa da rede de anúncios. Por padrão, essa opção é *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** A estratégia de oferta da campanha:

* *[!UICONTROL Enhanced CPC]:* (Não disponível para desempenho máximo ou existente, somente leitura [!DNL Gmail] campanhas) Usa o modelo de custo por clique (eCPC) aprimorado da rede de anúncios, que permite que a rede de anúncios altere automaticamente a oferta de custo por clique (CPC) para cada leilão, em uma tentativa de maximizar as conversões, usando as conversões especificadas na rede de anúncios (não em Pesquisa, Social e Commerce), ao tentar manter seu CPC médio abaixo do CPC máximo.

Quando você adiciona uma campanha com eCPC a um portfólio otimizado de Pesquisa, Social e Commerce, o Search, Social e Commerce otimiza as ofertas básicas e, quando &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; opção está ativada — o orçamento da campanha. A rede de publicidade otimiza todos os ajustes de oferta e pode alterar as ofertas geradas pela Search, Social e Commerce no momento da consulta do usuário com base em dados e insights proprietários. **Atenção:** Use campanhas eCPC em portfólios somente quando o total de conversões rastreadas na rede de anúncios estiver alinhado ao objetivo do portfólio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (o padrão): (não disponível para campanhas de desempenho máximo) usa o modelo de custo por clique (CPC). Opcionalmente, é possível permitir que a rede de publicidade altere os lances da campanha:

   * **[!UICONTROL Enable Enhanced CPC]** (desativado por padrão): é o mesmo que usar o &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Campanhas de pesquisa, exibição e compras) A rede de publicidade — não as campanhas Search, Social e Commerce — otimiza ofertas para maximizar os cliques. Opcionalmente, informe um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de anúncios não pague mais do que um valor específico para cada clique. **Atenção:** Quando você adiciona uma campanha com essa estratégia a um portfólio, as ofertas são orientadas pelo peso dos cliques, não pelo objetivo do portfólio.

* *[!UICONTROL Maximize Conversion Value]:* (Campanhas de pesquisa, desempenho máximo e compras inteligentes) A rede de publicidade, não a Search, Social e Commerce, otimiza ofertas para maximizar o valor de conversão. Opcionalmente, informe um **[!UICONTROL Target Return on Ad Spend]** (ROAS) em porcentagem. **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Maximize Conversions]:* (Campanhas máximas de pesquisa, exibição e desempenho) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas para maximizar as conversões. Opcionalmente, informe um **[!UICONTROL Target CPA]** (custo por aquisição). **Nota:** Use essa opção para campanhas em portfólios híbridos, mas não em portfólios padrão.

* *[!UICONTROL Target CPA]:* (Campanhas de exibição; campanhas de pesquisa existentes) A rede de publicidade — não Search, Social e Commerce — otimiza ofertas com base em uma **[!UICONTROL Target CPA]** (custo por aquisição), que é o valor médio de 30 dias que você deseja pagar por uma aquisição (conversão). **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

  Para novas campanhas de pesquisa, [!DNL Google Ads] substituiu esta estratégia de licitação pela [!UICONTROL Maximize Conversions] estratégia usando um [!UICONTROL Target CPA] valor. Para campanhas de pesquisa existentes com essa estratégia, é possível editar somente o valor do target, e isso altera a estratégia para o [!UICONTROL Maximize Conversions] usando a estratégia especificada [!UICONTROL Target CPA] valor.

* *[!UICONTROL Target Impression Share]:* (Campanhas de pesquisa) A rede de publicidade, não a Search, Social e Commerce, otimiza ofertas para atingir um compartilhamento de impressões de público-alvo e uma posição de anúncio. Opcionalmente, informe um **[!UICONTROL Target Impression Share]** em porcentagem, a variável **[!UICONTROL Target Ad Position]**, e uma **[!UICONTROL Max CPC]** (custo por clique). **Nota:** Esta opção não é permitida em portfólios.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campanhas de exibição e compras; campanhas de pesquisa existentes) A rede de publicidade — não Pesquisar, Social e Commerce — otimiza ofertas com base em uma **[!UICONTROL Target ROAS]** (retorno do investimento em publicidade), especificado como uma porcentagem. **Nota:** Use essa opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

  Para novas campanhas de pesquisa, [!DNL Google Ads] substituiu esta estratégia de licitação pela [!UICONTROL Maximize Conversion Value] estratégia usando um [!UICONTROL Target Return on Ad Spend value]. Para campanhas de pesquisa existentes com essa estratégia, é possível editar somente o valor do target, e isso altera a estratégia para o [!UICONTROL Maximize Conversion Value] usando a estratégia especificada [!UICONTROL Target Return on Ad Spend] valor.

* *[!UICONTROL Viewable CPM]:* (Existente, somente leitura) [!DNL Gmail] somente campanhas) A rede de publicidade — não a Search, Social e Commerce — oferece ofertas somente em anúncios que são medidos como visualizáveis. **Nota:** A otimização para essa estratégia não é compatível com nenhum tipo de portfólio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Somente campanhas de compras; somente leitura para campanhas existentes) O país no qual os produtos da campanha são vendidos. Como os produtos são associados aos países de destino, essa configuração determina quais produtos são anunciados na campanha.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Somente campanhas de compras; anunciantes que já participam do programa de compras local com o [!DNL Google Merchant Center] lojas nos EUA, Reino Unido, DE, FR, JP e AU; opcional) Permite [!DNL Google Ads] para adicionar automaticamente as informações do inventário local aos anúncios de compras em Google.com.

**Dica:** Se você usar essa configuração, não exclua anúncios locais na [!UICONTROL Inventory Filter] configuração.

**Nota:** Os anúncios de inventário locais exigem dois feeds adicionais para [!DNL Google Merchant Center] — um com os dados do produto local e outro com o inventário de produto local. Consulte a [!DNL Google Ads] para obter mais informações sobre [anúncios de compras locais](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Pesquisar e exibir redes somente) Um ou mais idiomas de destino para anúncios na campanha.

[!DNL Google Ads] determina o idioma de um usuário a partir de seu [!DNL Google] configuração de idioma ou o idioma da consulta de pesquisa, da página atual ou das páginas visualizadas recentemente no [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Localizações geográficas específicas do usuário a serem incluídas ou excluídas como alvos. Por padrão, todos os locais são direcionados. É possível incluir e excluir usuários em qualquer combinação de locais. As exclusões sempre substituem as inclusões.

* Para direcionar todos os locais, não selecione nenhum local.

* Para selecionar ou excluir locais específicos:

   * (Países, estados, regiões metropolitanas ou cidades) Clique **[!UICONTROL Location Target]** (![Destino do local](/help/search-social-commerce/assets/location-target.png "Destino do local")) e localize os locais a serem incluídos e excluídos:

      * Para incluir um local e seus locais secundários, clique no círculo ao lado dele uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) será exibida.

      * Para excluir um local, clique duas vezes no círculo ao lado dele para que uma marca vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) será exibida.

      * Para expandir um local em seus subcomponentes (como estados, regiões metropolitanas ou cidades nos EUA), clique no nome do local.

      * Para pesquisar um local, insira ou cole pelo menos os três primeiros caracteres do local no campo de entrada. Nos resultados da pesquisa, clique em **[!UICONTROL Include]** ao lado de um local para incluir ou **[!UICONTROL Exclude]** ao lado de um local a ser excluído.

   * (Locais próximos a um endereço; somente targets incluídos) Clique em **[!UICONTROL Radius Target]** (![Alvo do Raio](/help/search-social-commerce/assets/radius-target.png "Alvo do Raio")) e clique em **[!UICONTROL Address]**. Insira o endereço e o raio em milhas ou quilômetros ao redor do endereço a ser direcionado e clique em **[!UICONTROL Add]**.

   * (Locais próximos a coordenadas geográficas; destinos incluídos apenas) Clique em **[!UICONTROL Radius Target]** (![Alvo do Raio](/help/search-social-commerce/assets/radius-target.png "Alvo do Raio")) e clique em **[!UICONTROL Coordinate]**. Insira a latitude, a longitude e o raio em milhas ou quilômetros ao redor do local de destino e clique em **[!UICONTROL Add]**.

* (Para adicionar um ajuste de oferta para um local de destino incluído) Informe um valor de ajuste de oferta:

* 0%: Não ajustar lances para anúncios neste local.

* \[Outros valores de -90% a 300%\]: para aumentar ou diminuir a oferta de anúncios neste local.

**Nota:**

* O Search, Social e Commerce não fornece ajustes de oferta ajustados automaticamente para os seguintes públicos-alvo de localização devido a limitações nos dados que [!DNL Google Ads] O fornece o mapeamento de locais de surfer para destinos de localização:

   * Alvos de raio.

   * Alguns locais abaixo do nível de estado/província/região/condado/prefeitura para os quais [!DNL Google Ads] O não envia uma localização principal na URL do surfer, incluindo aeroportos e distritos do Congresso dos EUA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Somente rede de exibição) Operadoras de celular específicas para direcionamento; as operadoras são classificadas por país. Se você não selecionar nenhum, todos serão direcionados.

**[!UICONTROL Mobile Carriers]:** (Exibir somente rede) Sistemas operacionais específicos para direcionamento. Se você não selecionar nenhum, todos serão direcionados.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

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

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]:** O nome do grupo de ativos. Links para [!DNL Google Merchant Center] os feeds de produto do não são compatíveis.

**[!UICONTROL Asset Group Status]:** O status do grupo de ativos: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** O URL final de todos os anúncios criados a partir do grupo de ativos. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Até 15 imagens para o anúncio, incluindo os seguintes tamanhos: 1) pelo menos três imagens quadradas, 2) pelo menos três imagens de paisagem e 3) pelo menos uma imagem retrato. Consulte a [[!DNL Google Ads] especificações da imagem](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las na sua [!UICONTROL Asset Library] — mas não ambas na mesma operação.

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

**[!UICONTROL Logos]:** Pelo menos um logotipo quadrado (1:1) e um logotipo paisagem (4:1). É possível incluir até cinco de cada tamanho. Consulte a [[!DNL Google Ads] especificações do logotipo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las na sua [!UICONTROL Asset Library] — mas não ambas na mesma operação.

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

**[!UICONTROL Videos]:** (Opcional) Pelo menos um e até cinco, [!DNL YouTube] vídeos com pelo menos 10 segundos de duração. Você pode inserir URLs ou selecioná-los nos seus [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir URLs:

   1. No [!UICONTROL Enter Video Url] insira um URL.

   1. (Opcional) Para adicionar outro URL, clique em **[!UICONTROL + Add]** e insira o URL.

* Para selecionar vídeos de sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os vídeos.

**[!UICONTROL Headlines]:** Pelo menos três e até cinco manchetes curtas com no máximo 30 caracteres cada. Pelo menos um título deve ter no mínimo 15 caracteres. Se a opção no nível da campanha para habilitar a expansão final do URL estiver definida em [!DNL Google Ads], depois [!DNL Google Ads] O substitui esse valor por um título personalizado com base no conteúdo da página de aterrissagem.

É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Long Headlines]:** Pelo menos uma e até cinco manchetes longas com no máximo 90 caracteres cada. É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Descriptions]:** Pelo menos duas e até quatro descrições com no máximo 90 caracteres cada. Pelo menos uma descrição deve ter no mínimo 30 caracteres. É possível inserir texto ou selecionar ativos a partir da [!UICONTROL Asset Library] — mas não ambas na mesma operação.

* Para inserir texto:

   1. No [!UICONTROL Enter Text] insira o texto.

   1. (Opcional) Para adicionar outra sequência de texto, clique em **[!UICONTROL + Add]** e digite a string.

* Para selecionar ativos da sua [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Call to Action]:** O plano de ação a ser incluído no anúncio. Por padrão, *[!UICONTROL Automated]* estiver selecionado e [!DNL Google Ads] seleciona o plano de ação. Como opção, você pode escolher uma ação diferente.

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Google Ads] públicos-alvo a serem usados como sinais de público-alvo para a campanha. [!DNL Google Ads] os modelos de aprendizado de máquina usam os públicos-alvo para encontrar navegadores da web semelhantes ao público-alvo e também podem mostrar anúncios para públicos-alvo que não são especificados como sinais para ajudar você a atingir suas metas de desempenho. Escolha os públicos-alvo com maior probabilidade de conversão.

>[!NOTE]
>Os sinais de público são diferentes dos [metas de público-alvo no nível da campanha e do grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Permite especificar outro grupo de ativos.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se deseja *[!UICONTROL Use account conversion goals for this campaign]* (o padrão) ou *[!UICONTROL Use campaign specific conversion goals]*. Se você optar por especificar metas de conversão para a campanha, selecione metas padrão e/ou crie uma meta personalizada para a campanha.

As metas são sincronizadas diariamente, portanto, as metas existentes criadas nas 24 horas anteriores podem não ser listadas. Para atualizar a lista, [sincronizar manualmente os dados da rede de publicidade](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Para criar uma meta de conversão personalizada, clique em **[!UICONTROL + Add custom goal]**, insira o nome da meta personalizada, selecione o [ações de conversão](https://support.google.com/google-ads/answer/6032150) para incluir na meta personalizada e clique em **[!UICONTROL Save]**. **Nota:** Cada campanha pode ter apenas uma meta personalizada.

>[!TIP]
>
>Se a campanha fizer parte de um portfólio, use as mesmas metas de conversão que o objetivo do portfólio. Usar diferentes metas de conversão pode afetar o desempenho do portfólio.

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
