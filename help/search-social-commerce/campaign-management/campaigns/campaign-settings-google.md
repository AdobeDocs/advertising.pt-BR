---
title: '[!DNL Google Ads] configurações da campanha'
description: Referencie as configurações de  [!DNL Google Ads] campanhas.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 760d46182a61588748cfd5031168266ba53c9dcc
workflow-type: tm+mt
source-wordcount: '2425'
ht-degree: 0%

---

# Configurações de campanha de [!DNL Google Ads]

## \[Tela de criação da campanha\]

**[!UICONTROL Campaign Type]:** (Disponível somente durante a criação da campanha) Onde colocar anúncios e quais tipos de anúncios
a campanha pode conter:

* *[!UICONTROL Search Network Only]:* Mostra anúncios na rede de pesquisa, que inclui [!DNL Google] resultados de pesquisa e, opcionalmente, sites de parceiros de pesquisa. Você deve especificar palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Search with Display Select]:* Mostra anúncios na rede de pesquisa (que inclui [!DNL Google] resultados de pesquisa e, opcionalmente, sites de parceiros de pesquisa) e potencialmente mostra anúncios em sites de rede de exibição. Na rede de exibição, o [!DNL Google Ads] exibe seus anúncios seletivamente usando lances automatizados, independentemente da estratégia de lances da campanha. Para anúncios de pesquisa, especifique palavras-chave para cada grupo de publicidade; para anúncios de exibição, especifique disposições e, opcionalmente, especifique palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Shopping Network]:* Mostra anúncios de produtos, que o [!DNL Google] gera automaticamente com base nos seus produtos no [!DNL Google Merchant Center] em [!DNL Google Shopping], a área ao lado de [!DNL Google] resultados de pesquisa (separados de anúncios de texto) e (opcionalmente) sites de parceiros de pesquisa. Para cada grupo de publicidade na campanha, você pode especificar grupos de produtos para anunciar.

* *[!UICONTROL Display Network Only]:* Mostra anúncios na rede de exibição. Para cada grupo de publicidade, você deve especificar disposições e pode, opcionalmente, especificar palavras-chave.

* *[!UICONTROL Performance Max]:* mostra e otimiza conversões para seus anúncios em canais usando a oferta inteligente do [!DNL Google Ads]. Nas configurações da campanha, você deve especificar um ou mais grupos de ativos, que incluem imagens, logotipos, títulos, descrições, vídeos opcionais e sinais de público-alvo. O [!DNL Google Ads] combina automaticamente os ativos para veicular anúncios com base no canal (como [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

  **Notas:**

   * Somente as configurações necessárias estão disponíveis. Para configurações opcionais, faça logon no editor [!DNL Google Ads].

   * Os links para feeds de produto do [!DNL Google Merchant Center] não são suportados.

   * Não há suporte disponível para a listagem de grupos. Para gerenciar e exibir dados de grupos de listagem, faça logon no editor do [!DNL Google Ads].

   * A otimização híbrida é compatível. As metas da estratégia de oferta e os orçamentos da campanha são definidos no nível da campanha.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Campanhas Gmail somente leitura existentes) Se:

* *[!UICONTROL Target and Bid]* Para mostrar anúncios somente a usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios. No entanto, você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, definindo ofertas mais altas para esses públicos-alvo.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campanhas que segmentam somente a rede de pesquisa, incluindo campanhas de compras) Mostra
seus anúncios nas redes de parceiros de pesquisa da rede de anúncios. Por padrão, esta opção é *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** A estratégia de oferta para a campanha:

* *[!UICONTROL Enhanced CPC]:* (Não disponível para desempenho máximo ou campanhas [!DNL Gmail] existentes somente leitura) Usa o modelo eCPC (custo por clique) aprimorado da rede de publicidade, o que permite que a rede de publicidade altere automaticamente a oferta do CPC (custo por clique) para cada leilão, na tentativa de maximizar as conversões, usando as conversões especificadas na rede de publicidade (não em Pesquisa, Social e Commerce), enquanto tenta manter o CPC médio abaixo do seu CPC máximo.

Quando você adiciona uma campanha com eCPC a um portfólio otimizado de Pesquisa, Social e Commerce, o Search, Social e Commerce otimiza as ofertas básicas e, quando a opção &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; está habilitada, o orçamento da campanha é otimizado. A rede de publicidade otimiza todos os ajustes de oferta e pode alterar as ofertas geradas pela Search, Social e Commerce no momento da consulta do usuário com base em dados e insights proprietários. **Cuidado:** use campanhas eCPC em portfólios somente quando o total de conversões rastreadas na rede de publicidade estiver alinhado ao objetivo do portfólio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (o padrão): (Não disponível para campanhas de desempenho máximo) Usa o modelo de custo por clique (CPC). Opcionalmente, é possível permitir que a rede de publicidade altere os lances da campanha:

   * **[!UICONTROL Enable Enhanced CPC]** (desabilitado por padrão): é o mesmo que usar a opção &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Campanhas de pesquisa, exibição e compras) A rede de publicidade — não as campanhas Search, Social e Commerce — otimiza ofertas para maximizar cliques. Opcionalmente, insira um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de publicidade não pague mais do que um valor específico para cada clique. **Cuidado:** quando você adiciona uma campanha com esta estratégia a um portfólio, as ofertas são orientadas pelo peso dos cliques, não pelo objetivo do portfólio.

* *[!UICONTROL Maximize Conversion Value]:* (Pesquisa, desempenho máximo e campanhas de compras inteligentes) A rede de anúncios — não Pesquisa, Social e Commerce — otimiza ofertas para maximizar o valor de conversão. Opcionalmente, insira um **[!UICONTROL Target Return on Ad Spend]** (ROAS) como uma porcentagem. **Observação:** use esta opção para campanhas em portfólios híbridos, mas não em portfólios padrão. Em portfólios híbridos, o Search, Social e Commerce otimiza o ROAS do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

* *[!UICONTROL Maximize Conversions]:* (Campanhas máximas de pesquisa, exibição e desempenho) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas para maximizar as conversões. Opcionalmente, insira um **[!UICONTROL Target CPA]** (custo por aquisição). **Observação:** use esta opção para campanhas em portfólios híbridos, mas não em portfólios padrão. Em portfólios híbridos, o Search, Social e Commerce otimiza o CPA do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

* *[!UICONTROL Target CPA]:* (Exibir campanhas) A rede de anúncios — não Search, Social, &amp; Commerce — otimiza ofertas com base em um **[!UICONTROL Target CPA]** opcional (custo por aquisição), que é o valor médio de 30 dias que você deseja pagar por uma aquisição (conversão). **Observação:** use esta opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA]. Em portfólios híbridos, o Search, Social e Commerce otimiza o CPA do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campanhas de pesquisa) A rede de publicidade, não a Search, Social e Commerce, otimiza ofertas para atingir um compartilhamento de impressões de destino e uma posição de anúncio. Opcionalmente, insira um **[!UICONTROL Target Impression Share]** como uma porcentagem, o **[!UICONTROL Target Ad Position]** e um **[!UICONTROL Max CPC]** (custo por clique). **Observação:** esta opção não tem suporte em portfólios.

* *[!UICONTROL Target Return on Ad Spend]:* (Campanhas de exibição e compras) A rede de anúncios — não Search, Social e Commerce — otimiza ofertas com base em um **[!UICONTROL Target ROAS]** especificado (retorno do investimento em anúncios), especificado como uma porcentagem. **Observação:** use esta opção para campanhas em portfólios híbridos (mas não em portfólios padrão) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS]. Em portfólios híbridos, o Search, Social e Commerce otimiza o ROAS do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Viewable CPM]:* (Somente campanhas [!DNL Gmail] existentes e somente leitura) A rede de publicidade, não Search, Social e Commerce, oferece ofertas somente em anúncios medidos como visíveis. **Observação:** não há suporte para a otimização desta estratégia em nenhum tipo de portfólio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Somente campanhas de compras; somente leitura para campanhas existentes) O país no qual
os produtos da campanha são vendidos. Como os produtos são associados aos países de destino, essa configuração determina quais produtos são anunciados na campanha.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Somente campanhas de compras; anunciantes já participando do programa de compras local com [!DNL Google Merchant Center] lojas nos EUA, Reino Unido, DE, FR, JP e AU; opcional) Permite que o [!DNL Google Ads] adicione automaticamente suas informações de estoque local aos seus anúncios de compras em Google.com.

**Dica:** se você usar essa configuração, não exclua anúncios locais na configuração [!UICONTROL Inventory Filter].

**Observação:** os anúncios de inventário locais exigem dois feeds adicionais para o [!DNL Google Merchant Center] — um com os dados do produto local e outro com o inventário de produto local. Consulte a documentação do [!DNL Google Ads] para obter mais informações sobre [anúncios de compras locais](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Pesquisar e exibir redes somente) Um ou mais idiomas de destino para anúncios na campanha.

[!DNL Google Ads] determina o idioma de um usuário na configuração de idioma [!DNL Google] do usuário ou o idioma da consulta de pesquisa, da página atual ou de páginas visualizadas recentemente no [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Localizações geográficas específicas de usuário a serem incluídas ou excluídas como destinos. Por padrão, todos os locais são direcionados. É possível incluir e excluir usuários em qualquer combinação de locais. As exclusões sempre substituem as inclusões.

* Para direcionar todos os locais, não selecione nenhum local.

* Para selecionar ou excluir locais específicos:

   * (Países, estados, regiões metropolitanas ou cidades) Clique em **[!UICONTROL Location Target]** (![Destino do local](/help/search-social-commerce/assets/location-target.png "Destino do local")) e localize os locais a serem incluídos e excluídos:

      * Para incluir um local e seus locais secundários, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) seja exibida.

      * Para excluir um local, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

      * Para expandir um local em seus subcomponentes (como estados, regiões metropolitanas ou cidades nos EUA), clique no nome do local.

      * Para pesquisar um local, insira ou cole pelo menos os três primeiros caracteres do local no campo de entrada. Nos resultados da pesquisa, clique em **[!UICONTROL Include]** ao lado de um local a ser incluído ou em **[!UICONTROL Exclude]** ao lado de um local a ser excluído.

   * (Locais próximos a um endereço; somente destinos incluídos) Clique em **[!UICONTROL Radius Target]** (![Destino do Raio](/help/search-social-commerce/assets/radius-target.png "Destino do Raio")) e em **[!UICONTROL Address]**. Digite o endereço e o raio em milhas ou quilômetros ao redor do endereço a ser direcionado e clique em **[!UICONTROL Add]**.

   * (Locais próximos a coordenadas geográficas; somente destinos incluídos) Clique em **[!UICONTROL Radius Target]** (![Destino do raio](/help/search-social-commerce/assets/radius-target.png "Destino do raio")) e em **[!UICONTROL Coordinate]**. Insira a latitude, a longitude e o raio em milhas ou quilômetros ao redor do local de destino e clique em **[!UICONTROL Add]**.

* (Para adicionar um ajuste de oferta para um local de destino incluído) Informe um valor de ajuste de oferta:

* 0%: Não ajustar lances para anúncios neste local.

* \[Outros valores de -90% a 300%\]: para aumentar ou diminuir a oferta de anúncios neste local.

**Nota:**

* O Search, Social e Commerce não fornece ajustes de oferta ajustados automaticamente para os seguintes destinos de localização devido a limitações nos dados que o [!DNL Google Ads] fornece para mapear locais de surfer para destinos de localização:

   * Alvos de raio.

   * Alguns locais abaixo do nível de estado/província/região/município/prefeitura para os quais [!DNL Google Ads] não envia um local principal na URL do surfista, incluindo aeroportos e distritos do Congresso dos EUA.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Exibir somente rede) Operadoras de celular específicas para direcionamento; as operadoras estão classificadas
por país. Se você não selecionar nenhum, todos serão direcionados.

**[!UICONTROL Mobile Carriers]:** (Exibir somente rede) Sistemas operacionais específicos para destino. Se você não selecionar nenhum, todos serão direcionados.

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

**[!UICONTROL Track Product Group]:** (Somente para [!UICONTROL EF Redirect]) Não implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (por grupo de ativos)

**[!UICONTROL Asset Group Name]:** O nome do grupo de ativos. Os links para feeds de produto do [!DNL Google Merchant Center] não são suportados.

**[!UICONTROL Asset Group Status]:** O status do grupo de ativos: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** A URL final para todos os anúncios criados a partir do grupo de ativos. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Até 15 imagens para o anúncio, incluindo os seguintes tamanhos: 1) pelo menos três imagens quadradas, 2) pelo menos três imagens de paisagem e 3) pelo menos uma imagem de retrato. Consulte as [[!DNL Google Ads] especificações da imagem](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las em [!UICONTROL Asset Library], mas não ambas, na mesma operação.

* Para carregar imagens:

   1. Na guia [!UICONTROL Upload from Device], clique em **[!UICONTROL +]** e selecione imagens do seu dispositivo ou rede.

   1. Para cada imagem:

      1. Selecione a taxa de proporção.

      1. Arraste e posicione a caixa de corte conforme necessário para selecionar a parte visível da imagem e redimensione a parte visível da imagem conforme necessário, quando possível.

      1. (Opcional) Selecione proporções adicionais e, opcionalmente, reposicione e redimensione a imagem conforme necessário para cada proporção selecionada.

         Um ativo é criado para cada taxa de proporção selecionada.

      1. Clique em **[!UICONTROL Proceed]**.

   1. Quando terminar de especificar imagens, clique em **[!UICONTROL Upload]**.

* Para selecionar imagens de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione as imagens.

**[!UICONTROL Logos]:** Pelo menos um logotipo quadrado (1:1) e um logotipo paisagem (4:1). É possível incluir até cinco de cada tamanho. Consulte as [[!DNL Google Ads] especificações do logotipo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las em [!UICONTROL Asset Library], mas não ambas, na mesma operação.

* Para carregar imagens:

   1. Na guia [!UICONTROL Upload from Device], clique em **[!UICONTROL +]** e selecione imagens do seu dispositivo ou rede.

   1. Para cada imagem:

      1. Selecione a taxa de proporção.

      1. Arraste e posicione a caixa de corte conforme necessário para selecionar a parte visível da imagem e redimensione a parte visível da imagem conforme necessário, quando possível.

      1. (Opcional) Selecione proporções adicionais e, opcionalmente, reposicione e redimensione a imagem conforme necessário para cada proporção selecionada.

         Um ativo é criado para cada taxa de proporção selecionada.

      1. Clique em **[!UICONTROL Proceed]**.

   1. Quando terminar de especificar imagens, clique em **[!UICONTROL Upload]**.

* Para selecionar imagens de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione as imagens.

**[!UICONTROL Videos]:** (Opcional) No mínimo um e no máximo cinco vídeos [!DNL YouTube] com duração mínima de 10 segundos. Você pode inserir URLs ou selecioná-las em seu [!UICONTROL Asset Library], mas não ambos, na mesma operação.

* Para inserir URLs:

   1. Na guia [!UICONTROL Enter Video Url], insira uma URL.

   1. (Opcional) Para adicionar outra URL, clique em **[!UICONTROL + Add]** e insira a URL.

* Para selecionar vídeos de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os vídeos.

**[!UICONTROL Headlines]:** Pelo menos três e até cinco títulos curtos com no máximo 30 caracteres cada. Pelo menos um título deve ter no mínimo 15 caracteres. Se a opção no nível da campanha para habilitar a expansão final da URL estiver definida como [!DNL Google Ads], então [!DNL Google Ads] substituirá esse valor por um título personalizado com base no conteúdo da página de aterrissagem.

Você pode inserir texto ou selecionar ativos de [!UICONTROL Asset Library], mas não ambos, na mesma operação.

* Para inserir texto:

   1. Na guia [!UICONTROL Enter Text], insira o texto.

   1. (Opcional) Para adicionar outra cadeia de texto, clique em **[!UICONTROL + Add]** e insira a cadeia de caracteres.

* Para selecionar ativos de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Long Headlines]:** Pelo menos uma e até cinco manchetes longas com no máximo 90 caracteres cada. Você pode inserir texto ou selecionar ativos de [!UICONTROL Asset Library], mas não ambos, na mesma operação.

* Para inserir texto:

   1. Na guia [!UICONTROL Enter Text], insira o texto.

   1. (Opcional) Para adicionar outra cadeia de texto, clique em **[!UICONTROL + Add]** e insira a cadeia de caracteres.

* Para selecionar ativos de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Descriptions]:** Pelo menos duas e até quatro descrições com no máximo 90 caracteres cada. Pelo menos uma descrição deve ter no mínimo 30 caracteres. Você pode inserir texto ou selecionar ativos de [!UICONTROL Asset Library], mas não ambos, na mesma operação.

* Para inserir texto:

   1. Na guia [!UICONTROL Enter Text], insira o texto.

   1. (Opcional) Para adicionar outra cadeia de texto, clique em **[!UICONTROL + Add]** e insira a cadeia de caracteres.

* Para selecionar ativos de [!UICONTROL Asset Library], clique em **[!UICONTROL Asset Library]** e selecione os ativos.

**[!UICONTROL Call to Action]:** O plano de ação a ser incluído no anúncio. Por padrão, *[!UICONTROL Automated]* está selecionado e [!DNL Google Ads] seleciona o plano de ação. Como opção, você pode escolher uma ação diferente.

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Google Ads] públicos-alvo a serem usados como sinais de público-alvo para a campanha. Os modelos de aprendizado de máquina do [!DNL Google Ads] usam os públicos-alvo para encontrar navegadores da web semelhantes ao público-alvo, e também podem mostrar anúncios para públicos-alvo que não são especificados como sinais para ajudá-lo a atingir suas metas de desempenho. Escolha os públicos-alvo com maior probabilidade de conversão.

>[!NOTE]
>Os sinais do público são diferentes dos [alvos de público-alvo no nível da campanha e do grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Permite que você especifique outro grupo de ativos.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se deseja *[!UICONTROL Use account conversion goals for this campaign]* (o padrão) ou *[!UICONTROL Use campaign specific conversion goals]*. Se você optar por especificar metas de conversão para a campanha, selecione metas padrão e/ou crie uma meta personalizada para a campanha.

As metas são sincronizadas diariamente, portanto, as metas existentes criadas nas 24 horas anteriores podem não ser listadas. Para atualizar a lista, [sincronize manualmente os dados da rede de anúncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Para criar uma meta de conversão personalizada, clique em **[!UICONTROL + Add custom goal]**, insira o nome da meta personalizada, selecione as [ações de conversão](https://support.google.com/google-ads/answer/6032150) a serem incluídas na meta personalizada e clique em **[!UICONTROL Save]**. **Observação:** cada campanha pode ter apenas uma meta personalizada.

>[!TIP]
>
>Se a campanha for parte de um portfólio híbrido, a prática recomendada é usar metas de nível de campanha que correspondam às metas de conversão no objetivo do portfólio; incluir metas de conversão adicionais pode afetar o desempenho do portfólio.
>
>No entanto, para campanhas em portfólios híbridos para os quais você [carrega objetivos na rede de anúncios](/help/search-social-commerce/tools/objective-upload-to-networks.md), faça o seguinte no editor da rede de anúncios, em vez de aqui: a) adicione a métrica de objetivo do portfólio Search, Social e Commerce carregada (que começa com &quot;O_ACS_OBJ&quot;) como uma ação de conversão para a campanha e b) adicione quaisquer metas de campanha que incluam [!DNL Google] conversões rastreadas, pois as métricas rastreadas pela rede de anúncios não são carregadas na rede de anúncios com o objetivo.

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

