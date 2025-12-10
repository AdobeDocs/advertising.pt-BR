---
title: Dados de bulksheet necessários para  [!DNL Microsoft Advertising] contas
description: Referencie os campos de cabeçalho e de dados necessários em bulksheets para contas do  [!DNL Microsoft Advertising] .
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '6934'
ht-degree: 0%

---

# Apêndice - Dados de bulksheet necessários para contas do [!DNL Microsoft Advertising]

Para criar e atualizar dados de campanha do [!DNL Microsoft Advertising] em massa, você pode usar os arquivos de bulksheet do Search, Social e Commerce formatados especificamente para contas do [!DNL Microsoft Advertising]. Você pode a) [gerar arquivos de planilha em massa para contas existentes](../bulksheet-download.md) no formato de arquivo necessário ou b) criá-los manualmente (consulte &quot;[Formatos de Arquivo de Planilha em Massa com Suporte](bulksheet-file-formats.md)&quot; para obter informações gerais sobre os formatos de arquivo com suporte).

Cada bulksheet deve incluir os campos de cabeçalho e os campos de dados correspondentes necessários para as [operações específicas que você deseja executar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (como criar um anúncio). Quando um campo não é obrigatório, você pode omiti-lo das linhas de cabeçalho e dados. Todas as colunas personalizadas são excluídas ao fazer upload do arquivo de planilha em massa.

A seguir há uma tabela de todos os campos de dados disponíveis e tabelas adicionais indicando quais campos são necessários para adicionar, editar ou excluir dados de entidades individuais (como campanhas e palavras-chave).

## Todos os campos de dados disponíveis {#bulksheet-fields-all-microsoft}

A tabela a seguir descreve todos os campos de dados disponíveis.

Para os campos de dados relevantes para entidades de conta, consulte &quot;[Campos necessários para criar, editar ou excluir cada componente de conta](#bulksheet-fields-per-component-microsoft).&quot;

| Campo | Descrição |
|----|----|
| [!UICONTROL Platform] | (Incluído nos bulksheets gerados para fins de informação) A plataforma de anúncios. Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Acct Name] | O nome exclusivo que identifica uma conta de rede de anúncios. Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | O nome exclusivo que identifica uma campanha para uma conta. O comprimento máximo é de 128 caracteres. |
| [!UICONTROL Campaign Budget] | O orçamento da campanha diário ou mensal, com ou sem símbolos e pontuação monetários. Ele não pode ser menor que 0,05. |
| [!UICONTROL Channel Type] | O tipo de canal ao qual a campanha se destina: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> ou <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Campanhas somente com orçamentos diários) A rapidez com que os anúncios da campanha são exibidos diariamente:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (o padrão para novas campanhas): para espalhar suas impressões de anúncios ao longo do dia.</li><li><i>[!UICONTROL Accelerated]:</i> Para exibir seus anúncios o máximo possível até que seu orçamento seja alcançado. Como resultado, seus anúncios podem não aparecer no final do dia.</li></ul> |
| [!UICONTROL Campaign Priority] | (Somente campanhas de compras) A prioridade com a qual a campanha é usada quando várias campanhas anunciam o mesmo produto: <i>[!UICONTROL Low]</i> (o padrão para novas campanhas), <i>[!UICONTROL Medium]</i> ou <i>[!UICONTROL High]</i>.<br><br>Quando o mesmo produto é incluído em mais de uma campanha, a rede de publicidade usa a prioridade de campanha primeiro para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada. |
| [!UICONTROL Has EU Political Ads] | (Aplicável a campanhas direcionadas a públicos na União Europeia (UE)) Se a campanha contém ou não anúncios políticos de acordo com os requisitos para anúncios veiculados na União Europeia nos termos do Regulamento UE 2024/90: <i>[!UICONTROL Yes]</i> ou <i>[!UICONTROL No]</i>. |
| [!UICONTROL Merchant ID] | (Campanhas de compras e campanhas de público vinculadas somente a um feed de comerciante) A ID do cliente da conta do comerciante cujos produtos são usados para a campanha. |
| [!UICONTROL Sales Country] | (Somente campanhas de compras; somente leitura para campanhas existentes) O país no qual os produtos da campanha são vendidos. Como os produtos são associados aos países de destino, essa configuração determina quais produtos são anunciados na campanha. |
| [!UICONTROL Product Scope Filter] | (Campanhas que usam somente a rede de compras) Os produtos em sua conta de comerciante para os quais anúncios de produtos podem ser criados para a campanha. É possível inserir até sete dimensões de produto e combinações de atributo nas quais filtrar seus produtos, usando o formato dimension=attribute. Separe vários filtros com um delimitador &quot;>&quot;. Para obter uma lista de dimensões de produto disponíveis, consulte &quot;[Filtros de produto da campanha de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.<br><br> Exemplo: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Para excluir os valores existentes, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL DSA Domain Name] | (Campanhas do tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; ou b) &quot;<i>[!UICONTROL Search]</i>&quot; quando o elemento [!DNL ExperimentId] não está definido) O nome de domínio do site a ser direcionado para anúncios de pesquisa dinâmica. O comprimento máximo é de 2.048 caracteres. Se o nome de domínio incluir `www`, ele será aparado e não será usado.<br><br>Para campanhas existentes, não é possível editar o domínio, mas você deve incluí-lo para atualizar outras propriedades. |
| [!UICONTROL DSA Domain Language] | (Campanhas do tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; ou b) &quot;<i>[!UICONTROL Search]</i>&quot; quando o elemento [!DNL ExperimentId] não está definido) O idioma das páginas do site a serem direcionadas para anúncios de pesquisa dinâmica. Os idiomas de domínio com suporte são [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] e [!UICONTROL Swedish].<br><br>Para campanhas existentes, não é possível editar o idioma, mas você deve incluí-lo para atualizar outras propriedades. |
| [!UICONTROL Ad Group Name] | O nome exclusivo que identifica um grupo de anúncios. O comprimento máximo é de 128 caracteres. Caracteres em branco à direita não são salvos (por exemplo, &quot;Grupo de anúncios 1&quot; é salvo como &quot;Grupo de anúncios 1&quot;). |
| [!UICONTROL Ad Group Type] | (Campanhas na rede de pesquisa; somente leitura para grupos de anúncios existentes) O tipo de grupo de anúncios: <i>[!UICONTROL Audience]</i> (somente para campanhas de público), <i>[!UICONTROL Search Dynamic]</i> (somente para anúncios de pesquisa dinâmica) e <i>[!UICONTROL Search Standard]</i> (somente para anúncios de pesquisa responsivos e anúncios de texto expandidos existentes). Alguns tipos de campanha podem incluir vários tipos de grupos de anúncios. |
| [!UICONTROL Keyword] | (Campanhas somente na rede de pesquisa) A sequência de palavras-chave. O comprimento máximo é de 50 caracteres.<br><br><b>Notas:</b><ul><li>Para excluir uma palavra-chave no nível do grupo de anúncios ou da campanha, defina o [!UICONTROL Match Type] como `Negative`. Se a linha incluir o nome do grupo de anúncios, a palavra-chave será excluída do grupo de anúncios. Se a linha não incluir o nome do grupo de anúncios, a palavra-chave será excluída para toda a campanha.</li><li>Alterar uma palavra-chave [!DNL Microsoft Advertising] exclui a palavra-chave existente e cria uma nova com uma nova ID de palavra-chave. No entanto, alterar o tipo de correspondência não exclui a palavra-chave existente.</li></ul> |
| Posicionamento | Obsoleto |
| [!UICONTROL Audience] | A lista de remarketing para o público-alvo de pesquisa de anúncios (RLSA) da campanha ou do grupo de anúncios. |
| [!UICONTROL Target Type] | (Somente destinos RLSA) O tipo de destino: <i>[!UICONTROL Inclusion]</i> ou <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Destinos de pesquisa dinâmica para o grupo de publicidade. Para todos os destinos, use &quot;[!UICONTROL All Web Pages]&quot;.<br><br>Para direcionar até três critérios de pesquisa dinâmica, use o formato `<category>=<target>`, em que &lt;category> pode incluir qualquer uma das categorias abaixo. Ingressar em vários destinos para uma categoria individual com &quot;`[blank space] and [blank space]`&quot; e ingressar em várias categorias com &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Categoria:</i> Para mostrar anúncios de pesquisa dinâmica para páginas indexadas com uma categoria de conteúdo Google específica.</li><li><i>URL:</i> Para mostrar anúncios de pesquisa dinâmica para páginas indexadas com uma URL específica, onde o valor pode ser incluído em qualquer lugar da URL.</li><li><i>Título da Página:</i> Para mostrar anúncios de pesquisa dinâmica para páginas indexadas com texto específico no título da página.</li><li><i>Conteúdo da Página:</i> Para mostrar anúncios de pesquisa dinâmica para páginas indexadas com conteúdo específico.</li></ul>Exemplo: url=shoes.example.com e page title=footwear<br>Exemplo: Todas as Páginas da Web |
| [!UICONTROL Location] | Uma localização geográfica na qual colocar anúncios para a campanha ou grupo de anúncios; os valores não fazem distinção entre maiúsculas e minúsculas. Se você não inserir nenhum valor para a campanha ou grupo de publicidade, todos os locais serão direcionados. Para direcionar locais específicos, insira o local usando os formatos de código de local [!DNL Microsoft Advertising]. Para baixar uma lista de locais, faça logon no portal do desenvolvedor [!DNL Microsoft Advertising] usando suas credenciais de conta publicitária [!DNL Microsoft Advertising]. <b>Observação:</b> para excluir um local, preceda o código do local com um sinal de menos (`-`), como `-United States`. |
| [!UICONTROL Location Type] | O tipo de local, como Cidade, País, MetroArea, Código Postal e Estado. Para baixar uma lista de locais, faça logon no portal do desenvolvedor [!DNL Microsoft Advertising] usando suas credenciais de conta publicitária [!DNL Microsoft Advertising]. |
| [!UICONTROL Match Type] | (Campanhas somente na rede de pesquisa) As opções de correspondência de palavras-chave. Isso pode incluir a opção de correspondência de palavras-chave para um público-alvo de pesquisa dinâmica ou grupo de produtos. Os valores incluem: <i>[!UICONTROL Broad]</i> (o padrão para novas palavras-chave), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (definido automaticamente para palavras-chave quando o grupo de publicidade é direcionado à rede de conteúdo), <i>[!UICONTROL Negative]</i> (para excluir uma palavra-chave da rede de conteúdo), <i>[!UICONTROL Dynamic Ad Target]</i> (o padrão para novos destinos de pesquisa dinâmica), <i>[!UICONTROL Product Group]</i> (o padrão para novos grupos de produtos) ou <i>[!UICONTROL Negative Product Group]</i> (para excluir um grupo de produtos).  Um valor para o tipo de correspondência ou ID de palavra-chave é necessário para editar ou excluir uma palavra-chave com vários tipos de correspondência.<br><br>Para o Modificador de Correspondência Ampla, escolha &quot;Amplo&quot; e insira um `+` antes de qualquer palavra na palavra-chave necessária (como &quot;`+red +shoes`&quot; para exigir &quot;vermelho&quot; e &quot;sapatos&quot;).<br><br>A alteração do tipo de correspondência para uma palavra-chave [!DNL Microsoft Advertising] não exclui a palavra-chave existente. |
| [!UICONTROL Max CPC] | (Campanhas na rede de pesquisa) O custo máximo por clique (CPC), que é a quantia mais alta a ser paga por um clique de anúncio com base na palavra-chave, grupo de produtos ou público alvo de pesquisa dinâmica, com ou sem símbolos e pontuação monetários.  Para palavras-chave e registros de grupos de produtos existentes em portfólios otimizados, as atualizações são eficazes por apenas um dia e são substituídas durante o próximo ciclo de otimização. <b>Observação:</b> não é possível definir ofertas para palavras-chave negativas. |
| [!UICONTROL Max Content CPC] | (Somente leitura para campanhas CPC criadas antes da desativação da rede de conteúdo em 2017 apenas ) O custo máximo de conteúdo por clique (CPC), que é o valor mais alto a ser pago por um clique de anúncio em um site de rede de exibição, com ou sem símbolos monetários e pontuação. |
| [!UICONTROL Audience Target Method] | (Grupos de anúncios de público-alvo) Se deve:<ul><li><i>[!UICONTROL Target and Bid]:</i> Para mostrar anúncios somente para usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.</li><li><i>[!UICONTROL Bid Only]:</i>Para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios.</li></ul> No entanto, você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, definindo ofertas mais altas para esses públicos-alvo. |
| [!UICONTROL Parent Product Groupings] | A hierarquia de qualquer grupo de produtos principal.<br><br>Exemplo: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | O grupo de produtos (como &quot;brand=acme&quot; ou &quot;All Products&quot;).<br><br><b>Notas:</b><ul><li>Quando um grupo de produtos especificado não existe na hierarquia de Agrupamentos de Produtos Pai, o Search, Social e Commerce cria qualquer parte da hierarquia que seja necessária.</li><li>O Search, Social e Commerce cria automaticamente um grupo &quot;[!UICONTROL All Products]&quot; sempre que você cria um grupo de anúncios em uma campanha de compras com uma oferta padrão definida para a oferta padrão do grupo de anúncios. O Search, Social e Commerce cria automaticamente um grupo &quot;[!UICONTROL Everything Else]&quot; com a oferta padrão do grupo de anúncios em cada nível da hierarquia de grupos de produtos. Você ainda pode criar explicitamente esses grupos padrão e excluí-los ou alterar seus lances.</li><li>Cada grupo de publicidade pode incluir até oito camadas de grupos de produtos, incluindo &quot;[!UICONTROL All Products]&quot; e sete outras camadas.</li></ul> |
| [!UICONTROL Partition Type] | O tipo de partição do grupo de produtos: <i>[!UICONTROL subdivision]</i> (quando há grupos de produtos filho) ou <i>[!UICONTROL unit]</i> (quando não há grupos de produtos filho). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Anúncios de texto expandidos, anúncios multimídia, anúncios responsivos e anúncios de pesquisa responsivos apenas) Os títulos de um anúncio. O tamanho máximo para cada campo de título de anúncio é de 30 caracteres ou 15 caracteres de byte duplo, incluindo qualquer texto dinâmico (como os valores de palavras-chave, `{Param2}` e `{Param3}` variáveis de substituição dinâmica e personalizadores de anúncios).<br><br> Para anúncios de pesquisa responsivos, insira um personalizador de anúncios usando o seguinte formato, onde &quot;Texto padrão&quot; é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Para anúncios de texto expandidos, Título de anúncio e Título de anúncio 2 são obrigatórios, e [!UICONTROL Ad Title 3] é opcional. [!DNL Microsoft Advertising] anúncios de texto expandidos obsoletos em agosto de 2022, e agora você só pode relatá-los e excluí-los.<br><br>Para anúncios multimídia, anúncios responsivos e anúncios de pesquisa responsivos, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] são obrigatórios, e todos os outros campos de título de anúncio são opcionais.<br><br>Para excluir o valor existente de um campo não obrigatório, use o valor `[delete]` (incluindo os colchetes).<br><br>Para todos os tipos de anúncios, exceto anúncios de texto expandidos, alterar a cópia de anúncio exclui o anúncio existente e cria um novo anúncio com as mesmas propriedades. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Somente anúncios de pesquisa responsivos; opcional) Uma posição na qual fixar o título do anúncio correspondente: `[null]` (sem valor, o que torna o título do anúncio qualificado para todas as posições), 1, 2 ou 3. Por exemplo, se [!UICONTROL Ad Title Position] tiver um valor de 1, então [!UICONTROL Ad Title] poderá aparecer somente na Posição 1. Por padrão, todos os títulos de anúncios são nulos (sem valores). Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes).<br><br><b>Observação:</b> você pode fixar vários títulos de anúncios na mesma posição. A rede de anúncios usa um dos títulos de anúncios fixados na posição. Os títulos fixados na posição 3 podem não ser mostrados com o anúncio. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Anúncios de texto, anúncios de pesquisa dinâmica, anúncios multimídia, anúncios responsivos, anúncios de pesquisa responsivos e sitelinks aprimorados em nível de campanha somente) O corpo de um anúncio ou sitelink.<br><br>Para sitelinks, você pode usar [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] para incluir texto extra que a rede de publicidade possa exibir sob o texto do link. Cada campo de descrição pode incluir até 35 caracteres de byte único ou 17 caracteres de byte duplo.<br><br>Para anúncios, o tamanho máximo de cada campo de descrição é de 90 caracteres ou 45 caracteres de byte duplo, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).<br><br>Para anúncios de pesquisa responsivos, insira um personalizador de anúncios usando o seguinte formato, em que Texto padrão é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Para anúncios de texto e anúncios de pesquisa dinâmica, a Linha de descrição 1 é obrigatória e [!UICONTROL Description Line 2] é opcional.<br><br>Para anúncios multimídia, anúncios responsivos e anúncios de pesquisa responsivos, [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] são obrigatórios, e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] são opcionais.<br><br>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes).<br><br><b>Notas:</b><ul><li>(Anúncios de texto padrão) O título e o texto combinados devem ter pelo menos três palavras.</li><li>(Anúncios de texto expandidos) Como opção, este campo pode incluir as variáveis de substituição dinâmica {Param2} e {Param3}. Em caso afirmativo, o tamanho máximo do texto do anúncio é de 300 caracteres de byte único ou 150 caracteres de byte duplo. [!DNL Microsoft Advertising] anúncios de texto expandidos obsoletos em agosto de 2022, e agora você só pode relatá-los e excluí-los.</li><li>(Anúncios de pesquisa dinâmica) Texto de substituição dinâmica não permitido.</li><li>Para todos os tipos de anúncios, exceto anúncios de texto expandidos, alterar a cópia de anúncio exclui o anúncio existente e cria um novo.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Somente anúncios de pesquisa responsivos; opcional) Uma posição na qual fixar a descrição correspondente: `[null]` (nenhum valor, o que torna a descrição qualificada para todas as posições), 1, 2 ou 3. Por exemplo, se [!UICONTROL Description 1 Position] tiver um valor igual a 1, a Descrição 1 poderá aparecer somente na Posição 1. Por padrão, nenhuma descrição é fixada a uma posição.<br><br>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes).<br><br><b>Observação:</b> você pode fixar várias descrições na mesma posição. A rede de anúncios usa uma das descrições fixadas na posição. As descrições fixadas na posição 2 podem não ser mostradas com o anúncio. |
| [!UICONTROL Business Name] | (Somente anúncios multimídia) O nome comercial, com no máximo 25 caracteres. |
| [!UICONTROL Promotion Line] | (Somente anúncios de listagem de produtos) Uma linha de promoção exclusiva a ser incluída na lista de produtos nos resultados da pesquisa (como &quot;Frete gratuito agora!&quot;). O comprimento máximo é de 45 caracteres.<br><br>A linha de promoção pode aparecer em locais diferentes relacionados ao anúncio (como abaixo do anúncio), dependendo de onde o anúncio aparece na página. |
| [!UICONTROL Display URL] | O URL incluído no anúncio.<br><br>Para anúncios de pesquisa dinâmica expandidos, a rede de anúncios gera esse valor dinamicamente a partir do domínio do site e você não precisa inserir um valor.<br><br>Para anúncios de texto expandidos e anúncios de pesquisa responsivos, não é necessário inserir um valor. O URL de exibição é extraído automaticamente do domínio no URL final. Opcionalmente, é possível personalizar o URL usando os campos Caminho 1 e Caminho 2.<br><br><b>Notas:</b><ul><li>(Contas com URLs finais) Os nomes de domínio no URL de exibição e no URL final devem corresponder.</li><li>[!DNL Microsoft Advertising] anúncios de texto expandidos obsoletos em agosto de 2022, e agora você só pode relatá-los e excluí-los.</li></ul> |
| [!UICONTROL Display Path 1] | (Somente anúncios de texto expandidos, anúncios de pesquisa dinâmica e anúncios de pesquisa responsivos) Texto adicionado ao URL de exibição que é extraído automaticamente do URL final. Cada caminho é precedido no URL por uma barra (/). Um caminho não pode conter caracteres de barra (/) ou de nova linha (\n). O comprimento máximo de cada caminho é de 15 caracteres ou 7 caracteres de byte duplo.<br><br>Para inserir um personalizador de anúncios, use os seguintes formatos, onde &quot;Texto padrão&quot; é um valor opcional a ser inserido quando o arquivo de feed não incluir um valor válido: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`<br><br>Por exemplo, se [!UICONTROL Display Path 1] for &quot;ofertas&quot;, a URL de exibição será &lt;URL de exibição>/ofertas, como www.example.com/deals.<br><br>[!DNL Microsoft Advertising] anúncios de texto expandidos obsoletos em agosto de 2022, e agora você só pode relatá-los e excluí-los. |
| [!UICONTROL Display Path 1] | (Somente anúncios de texto expandidos, anúncios de pesquisa dinâmica e anúncios de pesquisa responsivos) Um caminho de exibição adicional; consulte a entrada para [!UICONTROL Display Path 1].<br><br>Exemplo: se [!UICONTROL Display Path 1] for &quot;ofertas&quot; e [!UICONTROL Display Path 2] for &quot;local&quot;, a URL de exibição será &lt;<i>URL de exibição</i>>/ofertas/local, como www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Somente sitelinks aprimorados) A primeira data em que podem ser feitas ofertas para o sitelink, no fuso horário do anunciante e em um dos seguintes formatos: m/d/aaaa, m/d/aa, m-d-aaaa ou m-d-aa. O padrão para novos sitelinks aprimorados é o dia atual. <b>Observação:</b> novos sitelinks aprimorados podem ser criados apenas em campanhas com sitelinks aprimorados existentes ou sem sitelinks. |
| [!UICONTROL End Date] | A última data em que o sitelink pode aparecer com anúncios, no fuso horário do anunciante e em um dos seguintes formatos: m/d/aaaa, m/d/aaaa, m-d-aaaa ou m-d-aa. Para um novo sitelink, o padrão é `[blank]` (ou seja, sem data final). |
| [!UICONTROL Call To Action] | A call to action a ser incluída no anúncio. Consulte a [Referência da API para obter uma lista de valores possíveis](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), mas insira chamadas de várias palavras para ação como várias palavras (como &quot;Bet Now&quot; em vez de &quot;BetNow&quot;) em bulksheets. |
| [!UICONTROL Call To Action Language] | O idioma para as opções do call to action. Consulte a [Referência de API para obter uma lista de idiomas possíveis](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | O URL da página de aterrissagem para o qual os usuários do mecanismo de pesquisa são levados quando clicam em seu anúncio, incluindo quaisquer parâmetros de acréscimo configurados para a campanha ou conta. URLs base/final no nível de palavra-chave substituem aqueles no nível de anúncio e superior.<br><br>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Destination URL] | (Incluído em bulksheets gerados para fins de informação; não publicado no mecanismo de pesquisa) Para contas com URLs de destino, este é o URL que vincula um anúncio a um URL/página inicial base no site do anunciante (às vezes, por meio de outro site que rastreia o clique e redireciona o usuário para a página inicial). Inclui quaisquer parâmetros de acréscimo configurados para a campanha ou conta do Search, Social e Commerce. Se você gerou URLs de rastreamento, eles se baseiam nos parâmetros de rastreamento das configurações da conta e das configurações da campanha. Se você anexou parâmetros específicos do mecanismo de pesquisa, eles podem ser substituídos pelos parâmetros equivalentes para Pesquisa, Social e Commerce.<br><br>Para contas com URLs finais, esta coluna mostra o mesmo valor que a coluna URL Base/URL Final. |
| [!UICONTROL Custom URL Param] | Dados para substituir a variável dinâmica `{custom_code}` quando a variável for incluída nos parâmetros de rastreamento da conta de pesquisa ou nas configurações da campanha. Para inserir o valor personalizado no URL de rastreamento, você deve fazer upload do arquivo de bulksheet usando a opção Gerar URLs de rastreamento. |
| [!UICONTROL Creative Type] | O formato do anúncio: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (anúncios de compras), ou <i>[!UICONTROL Responsive Search Ad]</i>, ou <i>[!UICONTROL Text ad]</i>. O padrão para novos anúncios é <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | A primeira data em que as ofertas podem ser feitas para o grupo de anúncios, no fuso horário do anunciante e em um dos seguintes formatos: m/d/aaaa, m/d/aaa, m-d-aaaa ou m-d-aa. Para um novo grupo de anúncios, o padrão é a data atual. |
| [!UICONTROL Ad Group End Date] | A última data em que as ofertas podem ser feitas para o grupo de anúncios, no fuso horário do anunciante e em um dos seguintes formatos: m/d/aaaa, m/d/aaa, m-d-aaaa ou m-d-aa. Para um novo grupo de anúncios, o padrão é [em branco] (isto é, sem data final). |
| [!UICONTROL Tracking Template] | (Opcional) O modelo de rastreamento do, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora o URL final em um parâmetro. O modelo de rastreamento no nível mais granular (com a palavra-chave como o mais granular) substitui os valores em todos os níveis mais altos.<br><br>Para o controle de conversão do Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce adiciona automaticamente o código de redirecionamento e rastreamento quando você salva o registro.<br><br>Para redirecionamentos e rastreamento de terceiros, insira um valor.<br><br>Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte a documentação [!DNL Microsoft Advertising].<br><br> Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Landing Page Suffix] | Quaisquer parâmetros a serem anexados ao final dos URLs finais para rastrear informações. Exemplo: `param2=value1&param3=value2`<br><br>Consulte &quot;[Formatos de rastreamento de cliques para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)&quot;.<br><br>Sufixos finais de URL em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor [!DNL Microsoft Advertising]. |
| Pesquisar status da rede | Se os anúncios do grupo de anúncios devem ser colocados em vários elementos da Rede de pesquisa:<ul><li><i>Todos:</i> para colocar anúncios em todas as redes de pesquisa do Bing e parceiros de pesquisa sindicalizados.</li><li><i>OwnedAndOperatedOnly:</i>Para colocar anúncios apenas no Bing e no Yahoo! Web sites.</li><li><i>SyndicatedSearchOnly:</i> Para colocar anúncios apenas no Bing e no Yahoo! parceiros de pesquisa sindicalizados.</li><li><i>Desativado:</i> Para colocar anúncios somente na Rede de Conteúdo (não na Rede de Pesquisa).</li></ul> Para novos grupos de anúncios, o padrão é Ativado. |
| [!UICONTROL Content Network Status] | Obsoleto |
| [!UICONTROL Languages] | O idioma de destino dos anúncios no grupo de anúncios: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] ou [!UICONTROL Swedish]. O padrão para novas campanhas é [!UICONTROL English].<br><br>Essa configuração determina os países e regiões em que seu anúncio pode ser exibido. Escolha um idioma compatível com as metas de localização da campanha. |
| [!UICONTROL Budget Type] | Se o orçamento é <i>[!UICONTROL Daily]</i> (padrão) ou <i>[!UICONTROL Monthly]</i>.<br><br>Observação: se você atribuir a campanha a um portfólio otimizado, esse valor será automaticamente definido como [!UICONTROL Daily]. |
| [!UICONTROL Device] | Um tipo de dispositivo para o qual são feitos ajustes de oferta no nível da campanha ou do grupo de anúncios: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | O ajuste de oferta para um tipo de destino especificado. Por exemplo, se a oferta no nível da palavra-chave for de 1 USD e o ajuste de oferta para smartphones for de 50%, a oferta do smartphone será de 1,50 USD. Por padrão, todos os públicos-alvo são licitados no nível de palavra-chave. As porcentagens válidas podem incluir:<ul><li>Smartphones e tablets: -100 (para não licitar o tipo de dispositivo) e de -90 a 900</li><li>Desktop: de 0 a 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Os tipos de dispositivo nos quais você prefere exibir o anúncio ou sitelink: <i>[!UICONTROL All]</i> (padrão) ou <i>[!UICONTROL Mobile]</i>. Quando Mobile é especificado, a rede tenta exibir o anúncio ou o sitelink para usuários de dispositivos móveis em vez de usuários de desktop ou tablet. Caso contrário, a rede exibirá o anúncio ou o sitelink em qualquer tipo de dispositivo. <b>Observação:</b> a rede não garante que exibirá o anúncio no tipo de dispositivo preferencial. |
| [!UICONTROL Param2] | A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, descrição ou URL base do anúncio contiver a cadeia de caracteres de substituição dinâmica `{Param2}`. O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres). Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Param3] | A cadeia de caracteres a ser usada como valor de substituição se a URL base da palavra-chave ou o título, descrição ou URL base do anúncio contiver a cadeia de caracteres de substituição dinâmica `{Param3}`. O comprimento máximo é de 70 caracteres, mas esteja ciente do comprimento máximo dos elementos de anúncio em que ele é usado (por exemplo, a combinação do Título 1 e do Título 2 pode ter no máximo 76 caracteres). Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Link Name] | O texto do sitelink. Ele deve ser exclusivo dentro da campanha. Se você especificar Descrição1 e Descrição2, o texto do sitelink pode incluir até 25 caracteres de byte único ou 12 de byte duplo; caso contrário, o texto do sitelink pode incluir até 35 caracteres de byte único ou 17 de byte duplo.<br><br>[!DNL Microsoft Advertising] pode exibir dois, quatro ou seis sitelinks aprimorados com descrições, ou quatro ou seis sitelinks em uma única linha sem descrições, com um anúncio.<br><br>Você pode criar novos sitelinks aprimorados somente em campanhas com sitelinks aprimorados existentes ou sem sitelinks. |
| [!UICONTROL Campaign Status] | O status de exibição da campanha: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente campanhas existentes). O padrão para novas campanhas é [!UICONTROL Active]. Para excluir uma campanha ativa ou pausada, insira o valor `Deleted`. |
| [!UICONTROL Ad Group Status] | O status de exibição do grupo de anúncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente grupos de anúncios existentes). O padrão para novos grupos de anúncios é [!UICONTROL Active]. Para excluir um grupo de anúncios ativo ou pausado, insira o valor `Deleted`. |
| [!UICONTROL Keyword Status] | O status de exibição da palavra-chave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente palavras-chave existentes). O padrão para novas palavras-chave é [!UICONTROL Active]. Para excluir uma palavra-chave ativa ou pausada, insira o valor `Deleted`. <b>Observação:</b> se você criar URLs de rastreamento para uma palavra-chave com vários tipos de correspondência, o status da palavra-chave para cada tipo de correspondência deverá ser o mesmo. |
| [!UICONTROL Placement Status] | Obsoleto |
| [!UICONTROL Ad Status] | O status de exibição do anúncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (somente anúncios existentes), <i>[!UICONTROL Disapproved]</i> (não editável) ou <i>[!UICONTROL Paused]</i>. O padrão para novos anúncios é [!UICONTROL Active]. Para excluir um anúncio ativo ou pausado, insira o valor `Deleted`. |
| [!UICONTROL Target Status] | O status de um destino de pesquisa dinâmica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente destinos existentes). O padrão para novos destinos é [!UICONTROL Active]. Para excluir um destino ativo ou pausado, insira o valor `Deleted`. |
| [!UICONTROL Sitelink Status] | O status de exibição do sitelink: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (somente sitelinks existentes). O padrão para novos sitelinks é [!UICONTROL Active]. Para excluir um sitelink ativo, insira o valor `Deleted`. |
| [!UICONTROL Location Status] | O status do destino do local: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (somente locais existentes). O padrão para novos locais é [!UICONTROL Active]. Para excluir um local ativo, insira o valor `Deleted`. |
| [!UICONTROL Product Group Status] | O status de exibição do grupo de produtos: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (somente grupos de produtos existentes). O padrão para novos grupos de produtos é [!UICONTROL Active]. Para excluir um grupo de produtos ativo, insira o valor `Deleted`. |
| [!UICONTROL Device Target Status] | O status do destino do dispositivo no nível da campanha ou do grupo de anúncios: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Para novas campanhas e grupos de anúncios, o padrão é [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | O status do destino RLSA no nível da campanha ou do grupo de anúncios ou exclusão (somente Google Ads): <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (somente destinos existentes). O padrão para novos destinos ou exclusões é [!UICONTROL Active]. Para excluir um destino ou exclusão ativa, insira o valor `Deleted`. |
| \[Classificação de rótulo específica do anunciante\] | (Nomeado para uma classificação de rótulo específica do anunciante, como &quot;Cor&quot; para uma classificação de rótulo chamada Cor) Um valor para a classificação especificada associada à entidade. Você pode incluir apenas um valor por classificação por entidade (como &quot;vermelho&quot; para a classificação de rótulo &quot;Cor&quot; para a Campanha A). O comprimento máximo é de 100 caracteres e o valor pode incluir caracteres ASCII e não ASCII.<br><br>As classificações de rótulo e seus valores de rótulo são aplicados a todos os componentes filhos; novos componentes adicionados posteriormente são associados automaticamente ao rótulo. As classificações de etiquetas para grupos de produtos são aplicadas ao nível de unidade (mais granular).<br><br>Nem o nome de classificação nem o valor de classificação fazem distinção entre maiúsculas e minúsculas. |
| [!UICONTROL Constraints] | Uma restrição atribuída à entidade. Você pode atribuir somente uma restrição por entidade.<br><b>>As restrições são herdadas por entidades filhas, portanto, não é necessário inserir valores para entidades filhas, a menos que você queira substituir os valores herdados. |
| [!UICONTROL Campaign ID] | A ID exclusiva que identifica uma campanha existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a campanha. |
| [!UICONTROL Ad Group ID] | O identificador exclusivo que identifica um grupo de anúncios existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o grupo de anúncios. |
| [!UICONTROL Placement ID] | Obsoleto |
| [!UICONTROL Keyword ID] | A ID exclusiva que identifica uma palavra-chave existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera a palavra-chave, a menos que a linha inclua a) colunas de propriedade suficientes para identificar a palavra-chave ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>A ID exclusiva que identifica um anúncio existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Para anúncios de pesquisa responsivos, a ID do anúncio ou a ID do AMO é necessária para editar ou excluir dados de anúncios. Para todos os outros tipos de entidade, a ID do AMO é necessária somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade de anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade do anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado.</p><p><b>Observação:</b> se você editar a) as colunas de propriedade do anúncio, exceto o Status de um anúncio existente, ou b) os dados de um anúncio de pesquisa responsivo e não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID], então um novo anúncio será criado e o anúncio existente não será alterado. </p> |
| [!UICONTROL Sitelink ID] | A ID exclusiva que identifica um sitelink existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente ao alterar ou excluir o sitelink, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o sitelink ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; No entanto, se você não incluir [!UICONTROL Sitelink ID] nem [!UICONTROL AMO ID] e as colunas de propriedade corresponderem a vários sitelinks, o status de apenas um dos sitelinks será alterado.</p><p><b>Observação:</b> se você editar as colunas de propriedade do sitelink, exceto o Status de um sitelink existente, e não incluir o [!UICONTROL Sitelink ID] nem o [!UICONTROL AMO ID], um novo sitelink será criado e o sitelink existente não será alterado. |
| [!UICONTROL Product Group ID] | A ID exclusiva que identifica um grupo de produtos existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente ao alterar ou excluir o grupo de produtos, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o grupo de produtos ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| ID do local | O identificador [!DNL Microsoft Advertising] exclusivo do destino do local. Para baixar uma lista de locais, faça logon no portal do desenvolvedor [!DNL Microsoft Advertising] usando suas credenciais de conta publicitária [!DNL Microsoft Advertising]. Necessário somente quando você altera ou exclui o destino do local, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL Target ID] | A ID exclusiva que identifica um direcionamento automático existente. Necessário somente quando você altera ou exclui o direcionamento automático, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL RLSA Target ID] | A ID exclusiva que identifica um público-alvo RLSA existente no nível da campanha ou do grupo de anúncios. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera ou exclui o destino ou a exclusão, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL AMO ID] | (Em bulksheets gerados) Um identificador exclusivo gerado pela Adobe para uma entidade sincronizada. Para anúncios de pesquisa responsivos, a ID do AMO é necessária para editar ou excluir anúncios, a menos que você inclua a ID do anúncio. Para editar dados para todos os outros tipos de entidade com uma ID AMO, a ID AMO é necessária para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |
| [!UICONTROL EF Error Message] | (Incluído nos bulksheets gerados para fins informativos) Espaço reservado para exibir mensagens de erro da rede de publicidade relacionadas aos dados na linha; as mensagens de erro estão incluídas nos arquivos [!UICONTROL EF Errors]. Este valor não é postado na rede de publicidade. |
| [!UICONTROL SE Error Message] | (Incluído nos bulksheets gerados para fins informativos) Espaço reservado para exibir mensagens de erro da rede de publicidade relacionadas aos dados na linha; as mensagens de erro estão incluídas nos arquivos [!UICONTROL SE Errors]. Este valor não é postado na rede de publicidade. |
| [!UICONTROL Exemption Request] | (Incluído nos bulksheets gerados para fins de informação) Espaço reservado para exibir os nomes e o texto de qualquer política de publicidade da Google que um anúncio viola. |
| [!UICONTROL Retail Hash] | (Incluído para fins de informação em bulksheets gerados usando o Gerenciamento avançado de campanha) Um código de hash alfanumérico (como f9639f40cdf56524b541e5dacf55a991) que indica que o item foi gerado usando a visualização Avançado (ACM). |

[^1]: [!DNL Excel] converte números grandes em notação científica (como 2.12E+09 para 2115585666) quando abre o arquivo. Para exibir dígitos na notação padrão, selecione qualquer célula na coluna e clique dentro da barra de fórmulas.

## Campos necessários para criar, editar ou excluir cada componente da conta {#bulksheet-fields-per-component-microsoft}

As seções a seguir incluem os campos relevantes para entidades de conta específicas.

>[!NOTE]
>
>Quando um campo não é aplicável a uma ação, qualquer valor inserido no campo é ignorado.

### Campos de campanha

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório. |
| [!UICONTROL Campaign Budget] | Obrigatório para criar uma campanha. |
| [!UICONTROL Channel Type] | Obrigatório para criar uma campanha. |
| [!UICONTROL Delivery Method] | Opcional |
| [!UICONTROL Campaign Priority] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Has EU Political Ads] | Obrigatório para criar uma campanha. |
| [!UICONTROL Merchant ID] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Sales Country] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Product Scope Filter] | (Campanhas de compras) Opcional |
| [!UICONTROL DSA Domain Name] | Obrigatório para criar uma campanha do tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; ou b) &quot;[!UICONTROL Search]&quot; quando o elemento [!DNL ExperimentId] não está definido) |
| [!UICONTROL DSA Domain Language] | Obrigatório para criar uma campanha do tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; ou b) &quot;[!UICONTROL Search]&quot; quando o elemento [!DNL ExperimentId] não está definido) |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Landing Page Suffix] | <p>Opcional |
| [!UICONTROL Budget Type] | Obrigatório para criar uma campanha. |
| [!UICONTROL Device] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Campaign Status] | Necessário apenas para excluir uma campanha. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Obrigatório somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a campanha. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Group Type] | Obrigatório para criar um grupo de anúncios. |
| [!UICONTROL Audience Target Method] | Obrigatório somente para criar grupos de anúncios de público-alvo. |
| [!UICONTROL Ad Group Start Date] | Opcional |
| [!UICONTROL Ad Group End Date] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Search Network Status] | (Campanhas somente na rede de pesquisa) Opcional |
| [!UICONTROL Languages] | Opcional |
| [!UICONTROL Device] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Status] | Obrigatório apenas para excluir um grupo de anúncios. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Ad Group ID] | Obrigatório somente quando você altera o nome do grupo de anúncios, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o grupo de anúncios. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de palavra-chave

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Keyword] | Obrigatório |
| [!UICONTROL Match Type] | Um valor para o tipo de correspondência ou ID de palavra-chave é necessário para editar ou excluir uma palavra-chave com vários tipos de correspondência. |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Param1] | Opcional |
| [!UICONTROL Param2] | Opcional |
| [!UICONTROL Keyword Status] | Necessário somente para excluir uma palavra-chave. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Keyword ID] | Obrigatório somente ao editar ou excluir a palavra-chave, a menos que a linha inclua a) colunas de propriedade suficientes para identificar a palavra-chave ou b) um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de anúncio de pesquisa dinâmica

>[!NOTE]
>
>Criar suporte não está disponível.

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obrigatório para editar a descrição. <b>Observação:</b> para este tipo de anúncio, a alteração da cópia do anúncio exclui o anúncio existente e cria um novo. |
| [!UICONTROL Display Path 1] | Obrigatório para editar o campo. |
| [!UICONTROL Display Path 2] | Obrigatório para editar o campo. |
| [!UICONTROL Creative Type] | Obrigatório para criar ou editar o status de um anúncio de produto. |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a&amp;rpar; colunas de propriedade de anúncio suficientes para identificar o anúncio ou b&amp;rpar; e &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de anúncio de produto (compras)

Para obter mais informações sobre como criar anúncios de compras, consulte &quot;[Implementar [!DNL Microsoft Advertising] campanhas de compras](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html)&quot;.

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Promotion Line] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Obrigatório para criar ou editar o status de um anúncio de produto. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade do anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de anúncios responsivos (multimídia)

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Para anúncios responsivos, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] são necessários para criar anúncios, e todos os outros campos de título de anúncio são opcionais. Para excluir o valor existente de um campo não obrigatório, use o valor `[delete]` (incluindo os colchetes). <b>Observação:</b> para este tipo de anúncio, a alteração da cópia do anúncio exclui o anúncio existente e cria um novo. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] são necessários para criar anúncios, e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] são opcionais. <b>Observação:</b> para este tipo de anúncio, a alteração da cópia do anúncio exclui o anúncio existente e cria um novo. |
| [!UICONTROL Business Name] | Obrigatório para criar ou excluir um anúncio. |
| [!UICONTROL Call To Action] | Obrigatório para criar um anúncio. |
| [!UICONTROL Call To Action Language] | Obrigatório para criar um anúncio. |
| [!UICONTROL Base URL/Final URL] | Obrigatório para criar um anúncio. |
| [!UICONTROL Creative Type] | Opcional. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade do anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de anúncio de pesquisa responsivos

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Responsive Search Ad]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Para anúncios de pesquisa responsivos, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] são necessários para criar um anúncio, e todos os outros campos de título de anúncio são opcionais. Para excluir o valor existente de um campo não obrigatório, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Para anúncios de pesquisa responsivos, [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] são necessários para criar um anúncio, e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] são opcionais. Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Opcional |
| [!UICONTROL Display Path 1] | Opcional |
| [!UICONTROL Display Path 2] | Opcional |
| [!UICONTROL Base URL/Final URL] | Obrigatório para criar um anúncio. |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório para editar ou excluir anúncios, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir anúncios, a menos que você inclua a ID do anúncio. |

### Campos de anúncio de texto

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

>[!NOTE]
>
>Anúncios de texto expandidos foram descontinuados. Só é possível excluir anúncios de texto existentes.

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Somente leitura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Somente leitura |
| [!UICONTROL Display URL] | Somente leitura |
| [!UICONTROL Display Path 1] | Somente leitura |
| [!UICONTROL Display Path 2] | Somente leitura |
| [!UICONTROL Base URL/Final URL] | Somente leitura |
| [!UICONTROL Custom URL Param] | Somente leitura |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Tracking Template] | Somente leitura |
| [!UICONTROL Creative Preferred Devices] | Somente leitura |
| [!UICONTROL Ad Status] | Obrigatório |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID do anúncio.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino da pesquisa dinâmica (direcionamento automático)

>[!NOTE]
>
>Criar suporte não está disponível.

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Auto Target Expression] | Obrigatório. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Target Status] | Obrigatório para excluir um público alvo |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Target ID] | Necessário somente quando você altera ou exclui o direcionamento automático, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de grupo de produtos de compras

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Match Type] | Obrigatório para criar um grupo de produtos. |
| [!UICONTROL Max CPC] | Obrigatório para criar um grupo de produtos. |
| [!UICONTROL Parent Product Groupings] | Obrigatório |
| [!UICONTROL Product Grouping] | Obrigatório |
| [!UICONTROL Partition Type] | Obrigatório para criar um grupo de produtos. |
| [!UICONTROL Base URL/Final URL] | Obrigatório |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Product Group Status] | Necessário apenas para excluir um grupo de produtos. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Product Group ID] | Obrigatório somente quando você altera ou exclui o grupo de produtos, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o grupo de produtos ou b) um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de sitelink no nível da campanha

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| Linha de Descrição 1 | Opcional |
| [!UICONTROL Description Line 2] | Opcional |
| [!UICONTROL Start Date] | Opcional |
| [!UICONTROL End Date] | Opcional |
| [!UICONTROL Base URL/Final URL] | Obrigatório |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Link Name] | Obrigatório |
| [!UICONTROL Sitelink Status] | Necessário somente para excluir um sitelink. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Sitelink ID] | Necessário somente ao alterar ou excluir o sitelink, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o sitelink ou b) um &quot;[!UICONTROL AMO ID]&quot;. No entanto, se você não incluir [!UICONTROL Sitelink ID] nem [!UICONTROL AMO ID] e as colunas de propriedade corresponderem a vários sitelinks, o status de apenas um dos sitelinks será alterado.<br><br><b>Observação:</b> se você editar as colunas de propriedade do sitelink, exceto o Status de um sitelink existente, e não incluir o [!UICONTROL Sitelink ID] nem o [!UICONTROL AMO ID], um novo sitelink será criado e o sitelink existente não será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino da localização

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Location] | Obrigatório |
| [!UICONTROL Location Type] | Obrigatório para criar um público alvo |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Location Status] | Necessário apenas para excluir um destino de local. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da campanha.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino do dispositivo no nível da campanha e do grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Device] | Obrigatório para excluir um destino de dispositivo. |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Obrigatório para destinos de dispositivo de nível de grupo de anúncios. Não aplicável para alvos de dispositivo no nível da campanha. |
| [!UICONTROL Device Target Status] | Necessário apenas para excluir um destino de dispositivo. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicável somente para alvos de dispositivo de nível de grupo de anúncios. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID de destino do dispositivo.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino RLSA no nível da campanha e do grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-microsoft)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório para públicos-alvo em nível de grupo de anúncios. Não aplicável para públicos-alvo no nível da campanha. |
| [!UICONTROL Audience] | Obrigatório para criar um novo público alvo. |
| [!UICONTROL Target Type] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL RLSA Target Status] | Obrigatório para excluir um destino. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicável somente para alvos de nível de grupo de anúncios. |
| [!UICONTROL RLSA Target ID] | Necessário somente quando você altera ou exclui o destino, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID de Destino RLSA.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

>[!MORELIKETHIS]
>
>* [Apêndice - Erros de bulksheet](../bulksheet-errors.md)
>* [Operações que você pode executar em bulksheets](bulksheet-operations.md)
>* [Formatos de arquivo de bulksheet com suporte](bulksheet-file-formats.md)
>* [Baixar/Criar um arquivo de bulksheet](../bulksheet-download.md)
>* [Formatos de rastreamento de cliques para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Carregar um arquivo de bulksheet ou arquivo de erro corrigido](../bulksheet-upload.md)
