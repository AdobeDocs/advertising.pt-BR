---
title: Configurações de campanha de [!DNL Google Ads]
description: Referencie as configurações de  [!DNL Google Ads] campanhas.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 3057
ht-degree: 0%

---

# Configurações de campanha de [!DNL Google Ads]

## \[Início da página]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign Type]:** Onde colocar anúncios e quais tipos de anúncios a campanha pode conter:

* *[!UICONTROL Search Network Only]:* Mostra anúncios na rede de pesquisa, que inclui [!DNL Google] resultados de pesquisa e, opcionalmente, sites de parceiros de pesquisa. Você deve especificar palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Search with Display Select]:* Mostra anúncios na rede de pesquisa (que inclui [!DNL Google] resultados de pesquisa e, opcionalmente, sites de parceiros de pesquisa) e potencialmente mostra anúncios em sites de rede de exibição. Na rede de exibição, o [!DNL Google Ads] exibe seus anúncios seletivamente usando lances automatizados, independentemente da estratégia de lances da campanha. Para anúncios de pesquisa, especifique palavras-chave para cada grupo de publicidade; para anúncios de exibição, especifique disposições e, opcionalmente, especifique palavras-chave para cada grupo de publicidade.

* *[!UICONTROL Shopping Network]:* Mostra anúncios de produtos, que o [!DNL Google] gera automaticamente com base nos seus produtos no [!DNL Google Merchant Center] em [!DNL Google Shopping], a área ao lado de [!DNL Google] resultados de pesquisa (separados de anúncios de texto) e (opcionalmente) sites de parceiros de pesquisa. Para cada grupo de publicidade na campanha, você pode especificar grupos de produtos para anunciar.

* *[!UICONTROL Display Network Only]:* Mostra anúncios na rede de exibição. Para cada grupo de publicidade, você deve especificar disposições e pode, opcionalmente, especificar palavras-chave.

* *[!UICONTROL Performance Max]:* mostra e otimiza conversões para seus anúncios em canais usando a oferta inteligente do [!DNL Google Ads]. Nas configurações da campanha, você deve especificar um ou mais grupos de ativos, que incluem imagens, logotipos, títulos, descrições, vídeos opcionais e sinais de público-alvo. O [!DNL Google Ads] combina automaticamente os ativos para veicular anúncios com base no canal (como [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

  **Notas:**

  * Somente as configurações necessárias estão disponíveis. Para configurações opcionais, faça logon no editor [!DNL Google Ads].

  * Os links para feeds de produto do [!DNL Google Merchant Center] não são suportados.

  * Não há suporte disponível para a listagem de grupos. Para gerenciar e exibir dados de grupos de listagem, faça logon no editor do [!DNL Google Ads].

## Guia [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campanhas direcionadas somente à rede de pesquisa, incluindo campanhas de compras) Mostra seus anúncios nas redes de parceiros de pesquisa da rede de anúncios. Por padrão, esta opção é *[!UICONTROL Off]*.

**[!UICONTROL Audience Target Method]:**(Campanhas Gmail somente leitura existentes) Se:

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios. No entanto, você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, definindo ofertas mais altas para esses públicos-alvo.

* *[!UICONTROL Target and Bid]* Para mostrar anúncios somente a usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.

**[!UICONTROL Contains EU Political Ads]:**(Aplicável a campanhas direcionadas a públicos na União Europeia (UE)) Se a campanha contém ou não anúncios políticos de acordo com os requisitos para anúncios veiculados na União Europeia nos termos do Regulamento UE 2024/90: *[!UICONTROL No]* ou *[!UICONTROL Yes]*.

## Guia [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** (Opcional; aplicável para desempenho máximo e campanhas de pesquisa com todas as configurações necessárias e que incluem apenas grupos de anúncios) Clique em **[!UICONTROL Show Recommendation]** para exibir o orçamento recomendado por [!DNL Google Ads]. Atualmente, somente campanhas com menos de 40.000 palavras-chave são qualificadas.

Para campanhas de desempenho máximo e de pesquisa, as seguintes configurações são necessárias para o Recommendations:

* tipo de estratégia de oferta
* URL final
* grupos de ativos

Para campanhas de pesquisa, as seguintes configurações adicionais também são necessárias para as recomendações:

* meta da estratégia de oferta
* país
* idioma
* um local incluído ou excluído
* palavras-chave

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** A estratégia de oferta para a campanha:

* *[!UICONTROL Enhanced CPC]:* Obsoleto. [!DNL Google Ads] começou a alterar automaticamente [estratégias de oferta de CPC aprimoradas](https://support.google.com/google-ads/answer/2464964) existentes para CPC manual em 2025.

* *[!UICONTROL Manual CPC]* (o padrão): (Não disponível para campanhas de desempenho máximo) Usa o modelo de custo por clique (CPC). Opcionalmente, é possível permitir que a rede de publicidade altere os lances da campanha:

  * **[!UICONTROL Enable Enhanced CPC]** (desabilitado por padrão): é o mesmo que usar a opção &quot;[!UICONTROL Enhanced CPC]&quot;, que está obsoleta. [!DNL Google Ads] começou a alterar automaticamente [estratégias de oferta de CPC aprimoradas](https://support.google.com/google-ads/answer/2464964) existentes para CPC manual em 2025.

* *[!UICONTROL Maximize Clicks]:* (Campanhas de pesquisa, exibição e compras) A rede de publicidade — não as campanhas Search, Social e Commerce — otimiza ofertas para maximizar cliques. Opcionalmente, insira um **[!UICONTROL Max CPC]** (custo por clique) para garantir que a rede de publicidade não pague mais do que um valor específico para cada clique. **Cuidado:** quando você adiciona uma campanha com esta estratégia a um portfólio, as ofertas são orientadas pelo peso dos cliques, não pelo objetivo do portfólio.

* *[!UICONTROL Maximize Conversion Value]:* (Pesquisa, desempenho máximo e campanhas de compras inteligentes) A rede de anúncios — não Pesquisa, Social e Commerce — otimiza ofertas para maximizar o valor de conversão. Opcionalmente, insira um **[!UICONTROL Target Return on Ad Spend]** (ROAS) como uma porcentagem. **Observação:** use esta opção para campanhas em portfólios com otimização em nível de campanha ou de grupo de anúncios, mas não em portfólios com otimização em nível de palavra-chave. Em portfólios com otimização no nível da campanha ou do grupo de anúncios, o Search, Social e Commerce otimiza o ROAS do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

* *[!UICONTROL Maximize Conversions]:* (Campanhas máximas de pesquisa, exibição e desempenho) A rede de anúncios, não a Search, Social e Commerce, otimiza ofertas para maximizar as conversões. Opcionalmente, insira um **[!UICONTROL Target CPA]** (custo por aquisição) e a estratégia de oferta **[!UICONTROL Portfolio]** aplicável. **Observação:** use esta opção para campanhas em portfólios com otimização em nível de campanha ou de grupo de anúncios, mas não em portfólios com otimização em nível de palavra-chave. Em portfólios com otimização no nível da campanha ou do grupo de anúncios, o Search, Social e Commerce otimiza o CPA no nível da campanha ou (quando disponível) do Target.

* *[!UICONTROL Target CPA]:* (Campanhas somente para exibição) A rede de publicidade — não Search, Social e Commerce — otimiza ofertas com base em um **[!UICONTROL Target CPA]** opcional (custo por aquisição), que é o valor médio de 30 dias que você deseja pagar por uma aquisição (conversão). **Observação:** campanhas em portfólios com otimização de nível de campanha ou de grupo de anúncios (mas não portfólios com otimização de nível de palavra-chave) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA]. Em portfólios com otimização no nível da campanha ou do grupo de anúncios, o Search, Social e Commerce otimiza o CPA no nível da campanha ou (quando disponível) do Target.

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Target Impression Share]:* (Campanhas de pesquisa) A rede de publicidade, não a Search, Social e Commerce, otimiza ofertas para atingir um compartilhamento de impressões de destino e uma posição de anúncio. Opcionalmente, insira um **[!UICONTROL Target Impression Share]** como uma porcentagem, o **[!UICONTROL Target Ad Position]** e um **[!UICONTROL Max CPC]** (custo por clique). **Observação:** esta opção não tem suporte em portfólios.

* *[!UICONTROL Target Return on Ad Spend]:* (Campanhas de compras) A rede de anúncios — não Pesquisa, Social e Commerce — otimiza ofertas com base em um **[!UICONTROL Target ROAS]** especificado (retorno do investimento em anúncios), especificado como uma porcentagem. **Observação:** use esta opção para campanhas em portfólios com otimização em nível de campanha ou de grupo de anúncios (mas não em portfólios com otimização em nível de palavra-chave) com qualquer estratégia de gastos, exceto [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS]. Em portfólios com otimização no nível da campanha ou do grupo de anúncios, o Search, Social e Commerce otimiza o ROAS do Target no nível da campanha ou (quando disponível) no nível do grupo de anúncios.

  Os dados de posição média e oferta de CPC não estão disponíveis para campanhas com essa estratégia de oferta.

* *[!UICONTROL Viewable CPM]:* (Somente campanhas [!DNL Gmail] existentes e somente leitura) A rede de publicidade, não Search, Social e Commerce, oferece ofertas somente em anúncios medidos como visíveis. **Observação:** não há suporte para a otimização desta estratégia em nenhum tipo de portfólio.

## Guia [!UICONTROL Shopping Settings]

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

## Guia [!UICONTROL Campaign Targeting]

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

## Guia [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Exibir somente rede) Operadoras de celular específicas para direcionamento; as operadoras estão classificadas
por país. Se você não selecionar nenhum, todos serão direcionados.

**[!UICONTROL Mobile Carriers]:** (Exibir somente rede) Sistemas operacionais específicos para destino. Se você não selecionar nenhum, todos serão direcionados.

## Guia [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## Guia [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## Guia [!UICONTROL AI Max]

*Campanhas que só visam a rede de pesquisa*

**[!UICONTROL AI Max]:** Se deseja habilitar [[!UICONTROL AI Max]](https://support.google.com/google-ads/answer/15910366) — correspondência de termos de pesquisa orientada por IA, personalização de texto e expansão de URL final — para a campanha. Quando você habilita **[!UICONTROL AI Max]**, duas configurações adicionais são disponibilizadas:

* **[!UICONTROL Text customization]:** Se deve permitir que [!DNL Google Ads] use a IA gerativa para personalizar a cópia de anúncios, títulos e descrições com base nos anúncios existentes e na cópia da página de aterrissagem.

* **[!UICONTROL Final URL expansion]:** Determina se deve permitir que [!DNL Google Ads] roteie o tráfego para a página de aterrissagem mais relevante em seu site com base na intenção de pesquisa. Esta configuração está disponível somente quando **[!UICONTROL Text customization]** está habilitado.

<!-- Clarify why this is "Unspecified" and read-only for me as of 7/23. Also, shouldn't we reword this? -->

**[!UICONTROL Bundling required]:** (Campanhas existentes com o recurso [!UICONTROL AI Max] somente habilitado; somente leitura) Se [!UICONTROL AI Max] deve ser habilitado para respeitar ou modificar a personalização de texto e os controles da lista de marcas para a campanha: *[!UICONTROL Required]*, *[!UICONTROL Not required]* ou *[!UICONTROL Unspecified]*.

<!-- Is this based on the advanced location options set elsewhere in Google Ads editor? -->

**[!UICONTROL Geo Targeting Type]:** (Campanhas existentes com o recurso [!UICONTROL AI Max] habilitado somente; somente leitura) Quando qualquer um dos grupos de anúncios da campanha inclui [!UICONTROL Locations of Interest] destinos, os tipos de interesse de usuário que estão sendo direcionados são indicados: *[!UICONTROL Search Interest]* (usuários interessados em um local especificado), *[!UICONTROL Presence]* (usuários em ou regularmente em um local especificado), ou *[!UICONTROL Presence or Interest]* (usuários em, regularmente em ou interessados em um local especificado).

## Guia [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Somente para [!UICONTROL EF Redirect]) O nível em que os cliques e as receitas devem ser rastreados, adicionando um redirecionamento (quando relevante) e anexando parâmetros às URLs relevantes:

* *[!UICONTROL Keyword]:* Para rastrear dados somente no nível da palavra-chave.

* *[!UICONTROL Creative]:* Para rastrear dados somente no nível de anúncio (criativo).

* *[!UICONTROL Creative and Keyword]:* Para rastrear dados nos níveis de anúncio (criativo) e palavra-chave.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Adiciona um parâmetro de URL a anúncios na conta ou campanha para rastreamento de conversão.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

**[!UICONTROL Track Product Group]:** (Somente para [!UICONTROL EF Redirect]) Não implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

### [!UICONTROL Asset Groups] (por grupo de ativos)

*Somente campanhas de desempenho máximo*

**[!UICONTROL Asset Group Name]:** O nome do grupo de ativos. Os links para feeds de produto do [!DNL Google Merchant Center] não são suportados.

**[!UICONTROL Asset Group Status]:** O status do grupo de ativos: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** A URL final para todos os anúncios criados a partir do grupo de ativos. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and [!DNL Google Ads] replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Até 15 imagens para o anúncio, incluindo pelo menos uma imagem de paisagem (1.91:1, pelo menos 600 x 314 pixels) e pelo menos uma imagem quadrada (1:1, pelo menos 300 x 300 pixels). Opcionalmente, é possível incluir uma imagem retrato (4:5, pelo menos 480 x 600 pixels). Consulte as [[!DNL Google Ads] especificações da imagem](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las em [!UICONTROL Asset Library], mas não ambas, na mesma operação.

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

**[!UICONTROL Logos]:** Pelo menos um logotipo quadrado (1:1, pelo menos 128 x 128 pixels). Opcionalmente, é possível incluir um logotipo paisagem (4:1, pelo menos 512 x 218 pixels). É possível incluir até cinco logotipos no total. Consulte as [[!DNL Google Ads] especificações do logotipo](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Você pode carregar imagens ou selecioná-las em [!UICONTROL Asset Library], mas não ambas, na mesma operação.

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

**[!UICONTROL Call to Action]:** A call to action a ser incluída no anúncio. Por padrão, *[!UICONTROL Automated]* está selecionado e [!DNL Google Ads] seleciona o call to action. Como opção, você pode escolher uma ação diferente.

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres.

**[!UICONTROL Audience Signal]:** (Opcional) [!DNL Google Ads] públicos-alvo a serem usados como sinais de público-alvo para a campanha. Os modelos de aprendizado de máquina do [!DNL Google Ads] usam os públicos-alvo para encontrar navegadores da web semelhantes ao público-alvo, e também podem mostrar anúncios para públicos-alvo que não são especificados como sinais para ajudá-lo a atingir suas metas de desempenho. Escolha os públicos-alvo com maior probabilidade de conversão.

>[!NOTE]
>
>Os sinais do público são diferentes dos [alvos de público-alvo no nível da campanha e do grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (campo somente leitura para grupos de ativos existentes em campanhas de desempenho máximo) Por que o grupo de ativos está ou não servindo na capacidade total. Ele leva em conta o status do grupo de ativos, bem como outros sinais, como aprovações de política e qualidade. Os valores podem incluir *ELEGÍVEL,* *LIMITADO,* *NÃO_ELEGÍVEL,* *PAUSADO,* *PENDENTE,* *REMOVIDO,* *DESCONHECIDO,* ou *NÃO ESPECIFICADO.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (Campo somente leitura para grupos de ativos existentes em campanhas de desempenho máximo) Detalhes adicionais sobre o status primário do grupo de ativos. Os valores podem incluir *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAIGN_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *DESCONHECIDO,* ou *NÃO ESPECIFICADO.*

### [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se deseja *[!UICONTROL Use account conversion goals for this campaign]* (o padrão) ou *[!UICONTROL Use campaign specific conversion goals]*. Se você optar por especificar metas de conversão para a campanha, selecione metas padrão e/ou crie uma meta personalizada para a campanha.

As metas são sincronizadas diariamente, portanto, as metas existentes criadas nas 24 horas anteriores podem não ser listadas. Para atualizar a lista, [sincronize manualmente os dados da rede de anúncios](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Para criar uma meta de conversão personalizada, clique em **[!UICONTROL + Add custom goal]**, insira o nome da meta personalizada, selecione as [ações de conversão](https://support.google.com/google-ads/answer/6032150) a serem incluídas na meta personalizada e clique em **[!UICONTROL Save]**. **Observação:** cada campanha pode ter apenas uma meta personalizada.

>[!TIP]
>
>Se a campanha for parte de um portfólio híbrido, a prática recomendada é usar metas de nível de campanha que correspondam às metas de conversão no objetivo do portfólio; incluir metas de conversão adicionais pode afetar o desempenho do portfólio.
>
>No entanto, para campanhas em portfólios híbridos para os quais você [carrega objetivos na rede de anúncios](/help/search-social-commerce/tools/objective-upload-to-networks.md), faça o seguinte no editor da rede de anúncios, em vez de aqui: a) adicione a métrica de objetivo do portfólio Search, Social e Commerce carregada (que começa com &quot;O_ACS_OBJ&quot;) como uma ação de conversão para a campanha e b) adicione quaisquer metas de campanha que incluam [!DNL Google] conversões rastreadas, pois as métricas rastreadas pela rede de anúncios não são carregadas na rede de anúncios com o objetivo.

### [!UICONTROL Set Customer Acquisition Goal]

Otimize sua campanha para novos clientes, clientes existentes ou ambos. Para usar essa configuração, primeiro ative a nova meta de aquisição de cliente para a conta [!DNL Google Ads] ou, se aplicável, para a conta de gerente. A meta define as listas de clientes existentes qualificados e o valor de conversão adicional para novos clientes nas configurações de conversão. Consulte as Etapas de 1 a 2 na ajuda do [!DNL Google Ads] &quot;[Ativar a nova meta de aquisição de clientes](https://support.google.com/google-ads/answer/14007601).&quot;

**[!UICONTROL Customer Goal]:** O tipo de meta de aquisição de cliente:

* *[!UICONTROL All Customers]* (o padrão): otimizar igualmente para clientes novos e existentes.

* *[!UICONTROL New Customers]:* Priorizar a aquisição de novos clientes. Selecionar essa opção exibe a configuração **[!UICONTROL New Customer Bid Adjustment]**.

* *[!UICONTROL Existing Customers]:* Priorize a retenção de clientes existentes.

**[!UICONTROL New Customer Bid Adjustment]:** (**[!UICONTROL Customer Goal]** definido como **[!UICONTROL New Customers]** somente) Um multiplicador aplicado a ofertas ao direcionar novos clientes, de 0,1 a 10,0. O padrão é 1,0 (sem ajuste). Por exemplo, 1,5x aumenta ofertas em 50% para novos clientes, 2,0x dobra ofertas para novos clientes e 0,5x reduz ofertas em 50% para novos clientes.

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
