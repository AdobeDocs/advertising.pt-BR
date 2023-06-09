---
title: Anúncio de texto e configurações responsivas de modelo de anúncio de pesquisa para feeds de inventário
description: Consulte as configurações de anúncio de texto e modelos de anúncio de pesquisa responsivos para feeds de inventário.
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '3329'
ht-degree: 0%

---

# Anúncio de texto e configurações responsivas de modelo de anúncio de pesquisa para feeds de inventário


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

>[!NOTE]
>
>* Os seguintes caracteres são reservados para designar nomes de colunas e nomes de modificadores no modelo e, portanto, são proibidos como texto em todos os campos de atributo:  `[ ] < > `
>* Entrada [!DNL Yandex templates], é possível usar os parâmetros dinâmicos `{param1}` e `{param2}` somente em URLs, e não é possível usar a inserção dinâmica de preço em descrições de anúncios.

## \[Acima de todas as guias\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Painel esquerdo\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Opcional) Mapeia todos os novos grupos de anúncios (não disponível para [!DNL Yandex]), palavras-chave e anúncios a campanhas existentes, em vez de criar campanhas. Se você ativar essa opção, selecione o método de mapeamento.

Usar [!UICONTROL Map Only] no nível da campanha requer uma estrutura de conta existente intimamente ligada à taxonomia do produto e que mapeie facilmente para o feed de dados.

**[!UICONTROL Map Method]:** (Quando [!UICONTROL Map Only] está ativado para a campanha) O método pelo qual novos grupos de anúncios (não disponível para [!DNL Yandex]), palavras-chave e anúncios são mapeados para campanhas existentes:

* *[!UICONTROL Contains Anywhere]:* Adiciona dados a uma campanha existente cujo nome inclui a cadeia de caracteres especificada, se existir.

* *[!UICONTROL Contains Exactly]:* Adiciona dados a uma campanha existente cujo nome inclui a cadeia de caracteres especificada, se existir.

* *[!UICONTROL Exactly Matches]* (o padrão): adiciona dados a uma campanha existente com o mesmo nome, se existir.

Quando nenhuma correspondência é encontrada, todos os dados da campanha são ignorados. Se várias correspondências de campanha forem encontradas, as palavras-chave e os anúncios serão mapeados para todas elas.

**[!UICONTROL Campaign Tracking Template]:** (Contas somente com URLs finais/avançados; opcional) o modelo de rastreamento de nível de campanha, que especifica todos os redirecionamentos e parâmetros de rastreamento de domínio fora da aterrissagem e incorpora o URL final em um parâmetro. Esse valor substitui a configuração no nível da conta, mas os modelos de rastreamento em níveis mais granulares (com a palavra-chave como o mais granular) substituem esse valor.

* Para rastreamento de conversão de anúncio de Adobe, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente o código de redirecionamento e rastreamento ao salvar o registro.

* Para incorporar o URL final:

   * ([!DNL Google Ads] e [!DNL Microsoft® Advertising] somente) Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte o ([!DNL Microsoft® Advertising] somente) [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799/2) ou ([!DNL Google Ads] somente) os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Parâmetros ValueTrack disponíveis&quot; no [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] somente) Usar o parâmetro `!{unescapedurl}` para indicar o URL da landing page.

   * Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Para redirecionamentos e rastreamento de terceiros, insira um valor.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (Em [!DNL Google Ads] e [!DNL Yandex] configurações de campanha) As redes nas quais colocar anúncios:

* *[!UICONTROL Search]:* Para fazer lances de anúncios de pesquisa patrocinados.

  ([!DNL Google Ads] campanhas) Para incluir lances em listagens para [!DNL Google Ads] pesquisar parceiros, marque a caixa de seleção ao lado de **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* Para fazer ofertas de disposições em listagens de rede de conteúdo (exibição). **Nota:** Não é possível criar inserções usando o modelo. Ao selecionar essa opção, crie disposições para cada grupo de anúncios e especifique quais páginas da rede de exibição devem ser direcionadas para cada grupo de anúncios usando <!-- insert link --> bulksheets ou o <!-- insert links --> grupo de publicidade e configurações de posicionamento no [!UICONTROL Search] > [!UICONTROL Campaigns] exibições.

**[!UICONTROL Languages]:** ([!DNL Google Ads] pesquisar e exibir redes somente) Um ou mais idiomas de destino para anúncios na campanha.

[!DNL Google Ads] determina o idioma de um usuário a partir de seu [!DNL Google] configuração de idioma ou o idioma da consulta de pesquisa, da página atual ou das páginas visualizadas recentemente no [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Contas com URLs finais/avançados somente) O modelo de rastreamento de nível de grupo de anúncios, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora o URL final em um parâmetro.

Para o rastreamento de conversão de Adobe, que é aplicado quando as configurações da campanha incluem &quot;EF Redirect&quot; e &quot;Auto Upload&quot;, o Search, Social e &amp; Commerce adiciona automaticamente o redirecionamento e o código de rastreamento quando você salva o registro.

Para redirecionamentos e rastreamento de terceiros, insira um valor. Para indicar o URL da landing page:

* Para o Yahoo! Contas do Japan Ads, use o parâmetro {lpurl}.

* Para obter os parâmetros disponíveis para as contas do Microsoft® Advertising e do Google Ads, consulte a [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ou nos parâmetros &quot;Somente modelo de rastreamento&quot; na seção &quot;Parâmetros ValueTrack disponíveis&quot; no [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

Esse valor substitui as configurações no nível da conta e da campanha, mas os modelos de rastreamento em níveis mais granulares (com a palavra-chave como a mais granular) substituem esse valor.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Palavras-chave do grupo de publicidade especificado (ou campanha para [!DNL Yandex] contas), que podem consistir em qualquer combinação de texto estático, colunas no arquivo especificado e modificadores. Os nomes e os modificadores das colunas são substituídos pelos dados reais quando o arquivo de feed especificado é propagado pelo modelo.

Para inserir um nome de coluna ou grupo de modificadores como um parâmetro dinâmico, clique no campo de entrada e, em seguida, clique em um nome de coluna na lista de colunas ou em uma [nome do modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) na lista Modificadores. Para especificar várias palavras-chave ou vários tipos de correspondência para a mesma palavra-chave, insira-os em linhas separadas. Para especificar o tipo de correspondência de palavra-chave, use a seguinte sintaxe de tipo de correspondência ao redor do nome da coluna:

* Para [!DNL Google Ads], [!DNL Microsoft® Advertising], e [!DNL Yahoo! Japan Ads] modelos:

   * Para parâmetros dinâmicos: Ampla correspondência = `[keyword]`, Modificador de correspondência ampla para o primeiro termo na [!UICONTROL Keyword] coluna (como +sapatos de camurça azuis) = `+[keyword]`, Modificador de correspondência ampla para cada termo na coluna Palavra-chave (como +azul +camurça +sapatos) = `+[keyword]+`, Correspondência de Frase = `"[keyword]"`, Correspondência exata = `[[keyword]]`

   * Para palavras-chave estáticas: Ampla correspondência = `keyword`, Modificador de correspondência ampla = `+keyword`, ou Correspondência de Frases = `"keyword"`

     Não é possível inserir palavras-chave estáticas com correspondência exata e sintaxe de correspondência padrão aqui porque elas estão entre colchetes (`[]`), como são os parâmetros dinâmicos.

* Para [!DNL Yandex] modelos:

   * Para parâmetros dinâmicos: insira o nome da coluna, como `[keyword]`. Para indicar o tipo de correspondência, use o [[!DNL Yandex]sintaxe específica do](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Nota:** Para termos de correspondência ampla, use a seguinte sintaxe: Broad Match Modifier para o primeiro termo na coluna Palavra-chave (como +blue suede shoes) = `+[keyword]`, Modificador de correspondência ampla para cada termo na coluna Palavra-chave (como +azul +camurça +sapatos) = `+[keyword]+`

   * Para palavras-chave estáticas: somente as palavras-chave de pesquisa são suportadas. Use o [[!DNL Yandex]sintaxe específica do](https://yandex.com/support/direct/keywords/symbols-and-operators.html) para a palavra-chave. Colchetes (`[]`) para indicar a ordem das palavras não são suportados.

>[!NOTE]
>
>* Você pode incluir manualmente vários valores do modificador no campo Palavras-chave colocando valores separados por vírgula entre parênteses antes ou depois de um parâmetro de palavra-chave (mas não em ambos os lugares). Por exemplo, `(cheap, discount, affordable)[product]` O produz três anúncios separados para cada produto.
>* Se você não especificar um tipo de correspondência, o tipo de correspondência padrão &quot;broad&quot; será usado.
* Correspondências negativas não são suportadas.
* Os modificadores de correspondência ampla do Google agora têm o mesmo comportamento de correspondência que a correspondência de frases para alguns idiomas e você não pode criar novas palavras-chave do modificador de correspondência ampla. Consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/10286719) para obter mais informações.

**[!UICONTROL Map Only]:** Adiciona quaisquer novos anúncios a grupos de anúncios (ou a campanhas para [!DNL Yandex] contas) nas quais as palavras-chave especificadas são encontradas, em vez de criar novas palavras-chave. Para ativar essa opção, marque a caixa de seleção. Quando essa opção está habilitada, qualquer variável Param 1 e Param 2 nas palavras-chave especificadas não se aplicam porque as palavras-chave existem.

**[!UICONTROL Keyword Final URL]:** (Contas com URLs finais/avançados; opcional) O URL da página inicial para o qual os usuários da rede de publicidade são direcionados quando clicam no seu anúncio. Ele deve incluir o mesmo domínio que o URL de exibição, e todos os parâmetros no URL final devem corresponder aos parâmetros no URL da página inicial após o clique no anúncio. Ela pode conter redirecionamentos no domínio ou subdomínio da página de aterrissagem, mas nenhum redirecionamento fora do domínio da página de aterrissagem.

Se você usar um [!DNL Google Merchant Center] e inclua esse valor no campo &quot;[!DNL Link]&quot; e, em seguida, insira essa coluna neste campo.

>[!NOTE]
>
* Se você gerar URLs de rastreamento ao publicar dados propagados por meio do modelo, os parâmetros de rastreamento serão anexados a esse valor com base nas configurações de rastreamento da conta.
* ([!DNL Google Ads] contas do ) Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

**[!UICONTROL Keyword Tracking Template]:** (Contas com URLs finais/avançados; opcional) o modelo de rastreamento, que especifica todos os redirecionamentos de domínio fora da aterrissagem e parâmetros de rastreamento, além de incorporar o URL final em um parâmetro. O modelo de rastreamento no nível mais granular (com a palavra-chave como mais granular) substitui os valores em todos os outros níveis.

* Para o rastreamento de conversão de Adobe, que é aplicado quando as configurações da campanha incluem &quot;EF Redirect&quot; e &quot;Auto Upload&quot;, o Search, Social e &amp; Commerce adiciona automaticamente o redirecionamento e o código de rastreamento quando você salva o registro.

* Opcionalmente, é possível informar redirecionamentos e rastreamento de terceiros.

* Para indicar o URL da landing page:

   * ([!DNL Google Ads] e [!DNL Microsoft® Advertising] somente) Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte o ([!DNL Microsoft® Advertising] somente) [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] somente) os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Parâmetros ValueTrack disponíveis&quot; no [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] somente) Usar o parâmetro `!{lpurl}` para indicar o URL da landing page.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** ([!DNL Google Ads] modelos apenas) A coluna no arquivo especificado que representa a variável [!DNL Google Ads] `{param1}` ou `{param2}` , que pode ser incluída na cópia de anúncio ou no URL de exibição para qualquer anúncio criado a partir do modelo. Para inserir o parâmetro dinâmico, clique em no campo de entrada e, em seguida, em um nome de coluna na lista de colunas. O nome da coluna é substituído pelos dados reais quando o arquivo de feed é propagado pelo modelo.

Se você usar um dos parâmetros, terá a opção de aplicar o parâmetro somente a novas palavras-chave ou também atualizar os valores de palavras-chave existentes que não foram criadas a partir do modelo:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (o padrão): simplesmente insere o valor do parâmetro para novas palavras-chave criadas usando o modelo.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Além de criar novas palavras-chave do feed, o Search, Social e Commerce também atualiza o valor do parâmetro para todas as palavras-chave existentes no grupo de anúncios que não foram criadas usando o modelo. Insira um único valor numérico que seja usado para todas essas palavras-chave. O modelo deve conter pelo menos uma palavra-chave.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Além de criar novas palavras-chave do feed, o Search, Social e Commerce também atualiza o valor do parâmetro para todas as palavras-chave existentes no grupo de anúncios que não foram criadas usando o modelo, desde que o arquivo de feed contenha valores numéricos para o parâmetro, com até uma casa decimal, mas sem vírgulas, símbolos ou códigos de moeda ou quaisquer outros caracteres. O valor mínimo do parâmetro no arquivo de feed é usado para todas as palavras-chave existentes. Por exemplo, se o arquivo de feed tiver [!UICONTROL Param1] valores de 21500 e 22000, então a variável [!UICONTROL Param1] os valores das palavras-chave existentes são alterados para 21500. O modelo deve conter pelo menos uma palavra-chave. **Dica:** Use essa opção somente quando tiver grupos de anúncios com temas restritos, para que faça sentido que as palavras-chave tenham o mesmo valor.

Os campos de dados no arquivo de feed podem ter no máximo 25 caracteres e podem consistir apenas em dados numéricos com os seguintes caracteres não numéricos:

* (Quando você usa o comando &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parâmetro) Somente até uma casa decimal.

* (Quando você não usa o comando &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parâmetro):

   * O valor pode ser precedido ou anexado com um símbolo ou código de moeda. Por exemplo, £2.000,00 e 2000GBP são válidos.

   * O valor pode incluir vírgula (,) ou ponto (.) como separador, com ponto opcional (.) ou vírgula (,) para valores fracionais. Por exemplo, 1.000,00 e 2.000,10 são válidos.

   * O valor pode ser prefixado ou anexado com um sinal de porcentagem (%), sinal de adição (+) ou sinal de subtração (-). Por exemplo, 20%, 208+ e -42,32 são válidos.

   * Dois números podem ser incorporados com uma barra. Por exemplo, 4/1 e 0.95/0.45 são válidos.

**[!UICONTROL Param 2]\[[!DNL Microsoft® Advertising] templates\]:** ([!DNL Microsoft® Advertising] apenas templates) A string a ser usada como valor de substituição em um anúncio se o título, texto, URL de exibição ou URL final contiver a variável `{Param2}` cadeia de caracteres de substituição dinâmica. O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo do elemento de anúncio no qual ele é usado (por exemplo, um título de anúncio pode incluir até 25 caracteres).

**[!UICONTROL Param 3]:** ([!DNL Microsoft® Advertising] apenas templates) A string a ser usada como valor de substituição em um anúncio se o título, texto, URL de exibição ou URL final contiver a variável `{Param3}` cadeia de caracteres de substituição dinâmica. O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo do elemento de anúncio no qual ele é usado (por exemplo, um título de anúncio pode incluir até 25 caracteres).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** O lance inicial para cada palavra-chave com o tipo de correspondência ou tipo de anúncio especificado.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] e [!DNL Microsoft® Advertising] somente campanhas) O tipo de anúncios: *[!UICONTROL Expanded Search Ads]* ou *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Opcional) Preenche todos os campos de texto alternativo de anúncios com texto dos campos de cópia de anúncio originais.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Somente anúncios de pesquisa responsivos) A posição do anúncio em que o título/título deve ser incluído (como &quot;[!UICONTROL Pinned at position 1]&quot;). O padrão é [!UICONTROL Unpinned].

Pelo menos um título deve estar disponível para cada posição. Se você fixar vários títulos na mesma posição, o anúncio final sempre incluirá um desses títulos na posição especificada. Os títulos fixados na posição 3 podem não ser mostrados com o anúncio.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Somente anúncios de pesquisa responsivos) Os títulos de anúncios (títulos). Cada variação de anúncio deve incluir pelo menos três e até 15 títulos de anúncio. A rede de anúncios exibe anúncios com até três títulos. O tamanho máximo de cada título é de 30 caracteres, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Somente anúncios de texto padrão da Microsoft® Advertising; somente leitura) O título, ou a primeira linha, de um anúncio. A Microsoft® Advertising descontinuou a criação e edição de anúncios de texto padrão.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] e [!DNL Yahoo! Japan Ads] modelos de anúncio de texto expandidos/estendidos) O título de um anúncio. O comprimento máximo de cada linha (após a substituição de qualquer parâmetro dinâmico) é de 30 caracteres ou 15 caracteres de byte duplo.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] modelos de anúncio de texto expandidos; opcional) Um terceiro título para um anúncio. O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 30 caracteres ou 15 caracteres de byte duplo.

**[!UICONTROL Title]:** ([!DNL Yandex] somente) O título ou a primeira linha de um anúncio. O máximo é de 33 caracteres.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Somente para anúncios de texto expandidos da Microsoft® Advertising) O título de um anúncio. O comprimento máximo de cada linha (após a substituição de qualquer parâmetro dinâmico) é de 30 caracteres ou 15 caracteres de byte duplo.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Somente para anúncios de texto expandidos da Microsoft® Advertising) O corpo de um anúncio. O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 80 caracteres ou 40 caracteres de byte duplo (como chinês, japonês e coreano).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** O corpo do anúncio.

* (Modelos de anúncio de texto expandidos do Google Ads) O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 90 caracteres ou 45 caracteres de byte duplo.

* (Yahoo! Modelos de anúncios do Japão) O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 80 caracteres ou 40 caracteres de byte duplo.

* (Modelos Yandex) O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 75 caracteres e uma única palavra não pode ter mais de 22 caracteres.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Somente anúncios de pesquisa responsivos) A posição do anúncio em que a descrição deve ser incluída (como &quot;[!UICONTROL Pinned at position 1]&quot;). O padrão é [!UICONTROL Unpinned]. Pelo menos uma descrição deve estar disponível para cada posição.

Se você fixar várias descrições na mesma posição, o anúncio final sempre incluirá uma dessas descrições na posição especificada. As descrições fixadas na posição 2 podem não ser mostradas com o anúncio.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Somente anúncios de pesquisa responsivos) As descrições dos anúncios. Cada variação de anúncio deve incluir pelo menos duas e até quatro descrições de anúncio. A rede de publicidade exibe anúncios com até duas descrições; insira pelo menos duas. O comprimento máximo de cada descrição é de 90 caracteres, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Somente modelos de anúncio de texto expandidos do Google; opcional) Uma segunda linha do anúncio. O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) é de 90 caracteres ou 45 caracteres de byte duplo.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Somente anúncios de texto expandido e de pesquisa responsiva; opcional) Um ou dois caminhos de URL para incluir consecutivamente após o URL de base. Eles devem descrever o produto ou serviço no anúncio com mais detalhes. Por exemplo, se você adicionar um [!UICONTROL Display Path 1] de &quot;Sapatos&quot; e [!UICONTROL Display Path 2] de &quot;Outdoor&quot; para o URL base www.example.com, o URL é www.example.com/Shoes/Outdoor. O comprimento máximo (após a substituição de qualquer parâmetro dinâmico) para cada campo é de 15 caracteres ou 7 caracteres de byte duplo.

Para anúncios de pesquisa responsivos, insira um personalizador de anúncios usando os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Existente) [!DNL Microsoft® Advertising] e [!DNL Yahoo! Japan Ads] somente anúncios de texto padrão; somente leitura) O URL exibido em um anúncio.

[!DNL Microsoft® Advertising] e [!DNL Yahoo! Japan Ads] substituíram a criação e a edição de anúncios de texto padrão.

**[!UICONTROL Base URL]:** (Contas com URLs de destino somente) A página para a qual os usuários são levados. Ele pode incluir redirecionamento e código de rastreamento de terceiros. Se você usar o serviço de rastreamento de conversão de Adobe Advertising e as configurações da campanha incluírem o uso de [!UICONTROL EF Redirect] Além disso, adicionar o rastreamento no nível do anúncio, em seguida, Pesquisar, Social e Comércio adiciona automaticamente seu próprio redirecionamento e código de rastreamento ao anúncio.

Para inserir um nome de coluna ou grupo de modificadores como um parâmetro dinâmico, clique no campo de entrada e, em seguida, clique em um nome de coluna na lista de colunas ou em uma [nome do modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) no [!UICONTROL Modifiers] lista.

**[!UICONTROL Final URL]:** (Contas com URLs finais/avançados) O URL da página inicial para o qual os usuários são levados quando clicam em seu anúncio. Ele deve incluir o mesmo domínio que o URL de exibição, e todos os parâmetros no URL final devem corresponder aos parâmetros no URL da página inicial após o clique no anúncio. Ela pode conter redirecionamentos no domínio ou subdomínio da página de aterrissagem, mas nenhum redirecionamento fora do domínio da página de aterrissagem.

Se você usar um [!DNL Google Merchant] Centralizar o feed e incluir esse valor no &quot;[!UICONTROL Link]&quot; e, em seguida, insira essa coluna neste campo.

>[!NOTE]
>
* Se você gerar URLs de rastreamento ao publicar dados propagados por meio do modelo, os parâmetros de rastreamento serão anexados a esse valor com base nas configurações de rastreamento da conta.
* ([!DNL Google Ads] contas ) Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

**[!UICONTROL Tracking Template]:** (Contas com URLs finais/avançados; opcional) o modelo de rastreamento, que especifica todos os redirecionamentos de domínio fora da aterrissagem e parâmetros de rastreamento, além de incorporar o URL final em um parâmetro. O modelo de rastreamento no nível mais granular (com a palavra-chave como mais granular) substitui os valores em todos os outros níveis.

Para rastreamento de conversão de anúncio de Adobe, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente o código de redirecionamento e rastreamento ao salvar o registro.

Para redirecionamentos e rastreamento de terceiros, insira um valor. Para indicar o URL da landing page:

* Para o Yahoo! Contas do Japan Ads, use o parâmetro {lpurl}.

* Para obter os parâmetros disponíveis para as contas do Microsoft® Advertising e do Google Ads, consulte a [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ou nos parâmetros &quot;Somente modelo de rastreamento&quot; na seção &quot;Parâmetros ValueTrack disponíveis&quot; no [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

**\[Campos de anúncios alternativos abaixo dos campos de anúncios originais\]:** (Opcional) Um conjunto alternativo de cópias de anúncios para um anúncio, que pode ser usado se qualquer uma das linhas do anúncio original exceder o comprimento máximo permitido, uma vez que quaisquer parâmetros dinâmicos sejam preenchidos com dados durante a propagação.

>[!NOTE]
>
* Se a variável [!UICONTROL Prefill] for selecionada, os campos alternativos serão pré-preenchidos com os campos originais e você poderá editá-los conforme necessário.
* Somente os campos de cópia de anúncio que excedem o comprimento máximo são substituídos pelo valor alternativo. Por exemplo, se apenas um título ou título original for muito longo, a variação de anúncio gerada usará o título ou título alternativo e as descrições originais. Portanto, certifique-se de que a cópia alternativa de anúncio faça sentido quando combinada com a cópia de anúncio original.
* Se a cópia do anúncio original atender aos requisitos de comprimento do mecanismo de pesquisa, a cópia alternativa do anúncio será descartada.

**\[Componente\] [!UICONTROL Ad Label Classifications] > \[Classificação de rótulo e valor\]:** (Opcional) Valores de até cinco classificações de etiquetas existentes a serem atribuídos às variações de anúncios criadas ou editadas usando o modelo. Para cada componente de campanha ao qual deseja atribuir classificações de rótulo:

1. Clique na caixa de seleção.

1. Configure os valores de classificação de etiquetas para o modelo de variação de anúncios:

   * Para cada classificação e valor de rótulo a ser atribuído ao componente, faça o seguinte:

      1. Clique em **[!UICONTROL Add Label Classification]**.

      1. Selecione a classificação de etiqueta existente e, em seguida, selecione um valor existente ou insira um novo valor.

         O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

         Para inserir um nome de coluna como um parâmetro dinâmico para um valor de classificação de rótulo, clique no campo de entrada (o segundo campo) e, em seguida, clique em um nome de coluna na lista de colunas.

         É possível incluir apenas um valor por classificação por componente de campanha. Por exemplo, uma campanha pode ter Color=Red, mas não Color=Red e Color=Blue.

         * Para alterar um valor de classificação de etiqueta existente, selecione ou insira um novo valor.

         * Para remover um valor de classificação de etiqueta existente, clique em **[!UICONTROL X]** ao lado do valor.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
* [Sobre a automatização do gerenciamento de anúncios usando feeds de inventário](../inventory-feeds-about.md)
* [Gerenciar modificadores](../modifiers-manage.md)
* [Gerenciamento de arquivos de feed de dados de inventário](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
* [Propagar dados do feed por meio de modelos](../feed-data-propagate.md)
* [Publicar dados de campanha de feeds de inventário em redes de anúncios](../propagated-data-post.md)
