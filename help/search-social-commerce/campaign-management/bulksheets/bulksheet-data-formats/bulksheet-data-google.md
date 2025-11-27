---
title: Dados de bulksheet necessários para  [!DNL Google Ads] contas
description: Referencie os campos de cabeçalho e de dados necessários em bulksheets para contas do  [!DNL Google Ads] .
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '7859'
ht-degree: 0%

---

# Apêndice - Dados de bulksheet necessários para contas do [!DNL Google Ads]

Para criar e atualizar dados de campanha do [!DNL Google Ads] em massa, você pode usar os arquivos de bulksheet do Search, Social e Commerce formatados especificamente para contas do [!DNL Google Ads]. Você pode a) [gerar arquivos de planilha em massa para contas existentes](../bulksheet-download.md) no formato de arquivo necessário ou b) criá-los manualmente (consulte &quot;[Formatos de Arquivo de Planilha em Massa com Suporte](bulksheet-file-formats.md)&quot; para obter informações gerais sobre os formatos de arquivo com suporte).

Cada bulksheet deve incluir os campos de cabeçalho e os campos de dados correspondentes necessários para as [operações específicas que você deseja executar](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (como criar um anúncio). Quando um campo não é obrigatório, você pode omiti-lo das linhas de cabeçalho e dados. Todas as colunas personalizadas são excluídas ao fazer upload do arquivo de planilha em massa.

A seguir há uma tabela de todos os campos de dados disponíveis e tabelas adicionais indicando quais campos são necessários para adicionar, editar ou excluir dados de entidades individuais (como campanhas e palavras-chave).

## Todos os campos de dados disponíveis {#bulksheet-fields-all-google}

A tabela a seguir descreve todos os campos de dados disponíveis.

Para os campos de dados relevantes para entidades de conta, consulte &quot;[Campos necessários para criar, editar ou excluir cada componente de conta](#bulksheet-fields-per-component-google).&quot;

>[!NOTE]
>
>* Os valores em todas as colunas de texto fazem distinção entre maiúsculas e minúsculas.
>* Ao criar um novo registro e não incluir valores para todos os campos de dados obrigatórios, alguns desses campos recebem os valores padrão especificados.
>* Para campos que não são especificados abaixo, o valor padrão para a rede de publicidade é usado.
>* Para obter uma lista de linhas de bulksheet disponíveis na caixa de diálogo [!UICONTROL Download Bulksheet], consulte &quot;[Linhas de bulksheet por rede de anúncios](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).&quot;

| Campo | Descrição |
| ---- | ---- |
| [!UICONTROL Platform] | (Incluído nos bulksheets gerados para fins de informação) A plataforma de anúncios. Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Acct Name] | O nome exclusivo que identifica uma conta de rede de anúncios. Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | O nome exclusivo que identifica uma campanha para uma conta. |
| [!UICONTROL Campaign Budget] | Um limite de gastos diário para a campanha, com ou sem símbolos e pontuação monetários. Este valor substitui mas não pode exceder o orçamento da conta. |
| [!UICONTROL Delivery Method] | <p>A rapidez com que os anúncios da campanha são mostrados todos os dias:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (o padrão para novas campanhas): para espalhar suas impressões de anúncios ao longo do dia.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (obsoleto em outubro de 2019) Para exibir seus anúncios com a maior frequência possível até que seu orçamento seja atingido. Como resultado, seus anúncios podem não aparecer no final do dia.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Os canais nos quais colocar anúncios. Especifique uma ou mais opções:</p><ul><li><p><i>[!UICONTROL Search]</i> (o padrão para novas campanhas): Para colocar anúncios na rede de pesquisa [!DNL Google Ads] (incluindo sites de pesquisa e pesquisa de parceiros [!DNL Google Ads]) e, opcionalmente, também na rede de exibição [!DNL Google Ads]. <b>Observação:</b> campanhas direcionadas à rede de pesquisa e à rede de exibição não podem ser adicionadas a um portfólio para otimização de lances.</p></li><li><p><i>[!UICONTROL Display]</i>: Para colocar anúncios somente na rede de exibição [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i>: Para colocar anúncios de compras na rede de compras [!DNL Google Ads] (em países selecionados) e na rede de pesquisa [!DNL Google Ads] (incluindo sites de pesquisa e pesquisa de parceiros [!DNL Google Ads]). Para criar anúncios de compras, você deve ter produtos em uma conta do [!DNL Google Merchant Center] e [permitir que o Search, Social e Commerce baixe dados da conta](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Consulte &quot;[Implementar [!DNL Google Ads] campanhas de compras](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; para obter mais informações sobre o processo de criação de anúncios de compras.</p></li></ul> |
| [!UICONTROL Networks] | <p>Onde colocar os anúncios. Especifique uma ou mais opções:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: listagens de pesquisa patrocinadas somente na Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: listagens de pesquisa patrocinadas nos parceiros de pesquisa da Google.</p></li><li><p><i>[!UICONTROL Content]</i>: Para fazer ofertas para exibir listagens de rede.</p></li><li><p><i>[!UICONTROL All]</i> (o padrão para novas campanhas): Segmenta a Pesquisa da Google, os Parceiros de Pesquisa e o Conteúdo.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Somente Rede de pesquisa; aplicável somente a anúncios de pesquisa dinâmica expandidos) O domínio raiz (como example.com) ou subdomínio (como shoes.example.com) do site cujo conteúdo a rede de publicidade usa para direcionar seus anúncios de pesquisa dinâmica.<br><br><b>Notas:</b></p><ul><li><p>A Pesquisa dinâmica expandida anuncia o conteúdo do site de destino em vez de palavras-chave.</p></li><li><p>Seu domínio deve ser indexado pelo índice de pesquisa orgânica da rede de publicidade para ser direcionado.</p></li><li><p>Se você não especificar um domínio, deverá criar destinos de pesquisa dinâmica, que direcionem todas as páginas do seu site ou um subconjunto delas, para cada grupo de anúncios.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Somente rede de pesquisa; aplicável somente a anúncios de pesquisa dinâmica expandidos) O idioma para o domínio do site especificado. <b>Observação:</b> se o domínio contiver páginas em vários idiomas e você quiser direcionar todas elas, crie uma campanha separada para cada idioma. |
| [!UICONTROL GDN Custom Bid Level] | (Campanhas que direcionam apenas a rede de exibição) Como licitar: por <i>[!UICONTROL Ad Group]</i> (padrão), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (site) ou <i>[!UICONTROL None]</i> (para redefinir o valor existente). Outras dimensões (<i>Idade</i>, <i>Gênero</i>, <i>Interesse e Lista</i>, <i>Tópico</i> e <i>Vertical</i>) estão disponíveis na interface [!DNL Google Ads]. Se você tiver usado a interface [!DNL Google Ads] para configurar ofertas por outra dimensão, esse valor será exibido, mas você não poderá selecionar ou inserir essas dimensões aqui.</p><p><b>Nota:</b></p><ul><li><p>Ao fazer uma oferta por palavra-chave, crie modelos de rastreamento no nível da palavra-chave. Da mesma forma, ao fazer uma oferta por posicionamento, crie modelos de rastreamento no nível de posicionamento. Para todas as outras dimensões, crie modelos de rastreamento no nível do anúncio.</p></li><li><p>Quando você faz uma oferta por uma dimensão não compatível (Idade, Gênero, Interesse e Lista ou Tópico), o Search, Social e Commerce não otimiza ofertas para a dimensão e todas as atribuições são aplicadas ao grupo de publicidade.</p></li><li><p>Anúncios na rede de pesquisa sempre usam ofertas de palavra-chave.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Somente campanhas de compras) A prioridade com a qual a campanha é usada quando várias campanhas anunciam o mesmo produto: <i>[!UICONTROL Low]</i> (o padrão para novas campanhas), <i>[!UICONTROL Medium]</i> ou <i>[!UICONTROL High]</i>.</p><p>Quando o mesmo produto é incluído em mais de uma campanha, a rede de publicidade usa a prioridade de campanha primeiro para determinar qual campanha (e ofertas associadas) está qualificada para o leilão de anúncios. Quando todas as campanhas têm a mesma prioridade, a campanha com a maior oferta é qualificada. |
| [!UICONTROL Merchant ID] | (Campanhas de compras e campanhas de público vinculadas somente a um feed de comerciante) A ID do cliente da conta do comerciante cujos produtos são usados para a campanha. |
| [!UICONTROL Sales Country] | (Somente campanhas de compras; somente leitura para campanhas existentes) O país no qual os produtos da campanha são vendidos. Como os produtos são associados aos países de destino, essa configuração determina quais produtos são anunciados na campanha. |
| [!UICONTROL Product Scope Filter] | (Campanhas usando apenas a rede de compras [!DNL Google Ads]) Os produtos em sua conta [!DNL Google Merchant Center] para os quais anúncios de compras podem ser criados para a campanha. É possível inserir até sete dimensões de produto e combinações de atributo nas quais filtrar seus produtos, usando o formato dimension=attribute. Separe vários filtros com um delimitador &quot;>&quot;. Para obter uma lista de dimensões de produto disponíveis, consulte &quot;[Filtros de produto da campanha de compras](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.</p><p>Exemplo: &quot;CategoriaL1=animais>>CategoriaL2=suprimentos para animais de estimação>>Marca=Suprimentos para animais de estimação da Acme&quot;</p><p>Para excluir os valores existentes, use o valor <code>[excluir]</code> (incluindo os colchetes).</p> |
| [!UICONTROL Languages] | <p>(Somente redes Search e Display) Os idiomas de destino dos anúncios na campanha.</p><p>Se você não inserir um valor para esse campo ou para o campo [!UICONTROL Geo Targeting] para uma nova campanha, a moeda especificada para a conta determinará os idiomas padrão, exceto que campanhas com moedas que não são mapeadas para idiomas específicos (por exemplo, EUR) são direcionadas para todos os idiomas. Se você não inserir um valor para este campo, mas inserir um valor no campo [!UICONTROL Geo Targeting] para uma nova campanha, o padrão será <i>[!UICONTROL All]</i>. Se você deixar esse campo em branco para uma campanha existente, o valor existente será retido.</p><p>Para direcionar todos os idiomas, digite <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Para direcionar idiomas específicos, insira valores separados por ponto-e-vírgula usando <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] nomes de idioma</a> (como <i>inglês;japonês</i>, que são substituídos pelos códigos numéricos corretos) ou códigos numéricos (como <i>1000;1005</i>). Os valores não diferenciam maiúsculas de minúsculas.</p> |
| [!UICONTROL Location] | Uma localização geográfica na qual colocar anúncios, ou para a qual excluir anúncios, para a campanha. Se você não inserir valores para esse campo ou para o campo Languages para uma nova campanha, a moeda especificada para a conta determinará os locais padrão, exceto que campanhas com moedas que não estão mapeadas para locais específicos (por exemplo, EUR) serão direcionadas para todos os locais. Se você não inserir um valor para este campo, mas inserir um valor no campo [!UICONTROL Languages] para uma nova campanha, o padrão será <i>[!UICONTROL All]</i>. Se você deixar esse campo em branco para uma campanha existente, o valor existente será retido.</p><p>Para direcionar um local específico, use um dos [[!DNL Google Ads] nomes de local](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (que são substituídos pelo código numérico correto) ou códigos de local:</p><ul><li><p>Países/territórios: insira os nomes do país/território (como <i>Estados Unidos;Japão</i>) ou os códigos numéricos (como <i>2840;2392</i>).</p></li><li><p>Estados/províncias/regiões: insira os nomes de estado/província/região com as abreviações de país/território relacionadas (como <i>Tóquio, JP;Nova York, US</i>) ou os códigos numéricos (como <i>20636;21167</i>).</p></li><li><p>Cidades fora dos EUA: insira o nome da cidade, o nome do estado/província/região e as abreviações do país/território (como <i>Adachi, Tóquio, JP;Kita, Tóquio, JP</i>) ou os códigos numéricos (como <i>1028850;1009293</i>)</p></li><li><p>Áreas metropolitanas dos EUA: insira os nomes das cidades, os nomes dos estados e as abreviações dos países (como <i>Buffalo NY, US;New York NY, US</i>) ou os códigos numéricos (como <i>514;501</i>).</p></li></ul><p>Para excluir um local, preceda o nome do local ou o código com um sinal de menos (`-`), como <i>-Japão</i>.</p><p><b>Observação:</b> os valores não diferenciam maiúsculas de minúsculas.</p> |
| [!UICONTROL Location Type] | (Quando você inclui um Local) O [tipo de local](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Um tipo de dispositivo para o qual são feitos ajustes de oferta no nível da campanha ou do grupo de anúncios: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Quando você inclui um destino [!UICONTROL Location], [!UICONTROL Device] ou [!UICONTROL RLSA]) Se ajusta lances para anúncios em um local específico, em um tipo de dispositivo específico ou com um destino de público específico:</p><ul><li><p>Para usar o lance de nível de palavra-chave (0% de diferença), digite 0. Para novos targets, você também pode deixar em branco.</p></li><li><p>Para usar um lance diferente para essa meta, informe a porcentagem pela qual aumentar ou diminuir lances.</p></li><ul><li><p>Para destinos de localização e RLSA, as porcentagens válidas incluem de -90 a 900.</p></li><li><p>Para ajustes de oferta de dispositivos, as porcentagens válidas incluem:</p></li><ul><li><p>(Campanhas)-100 (para não oferecer anúncios no tipo de dispositivo) ou de -90 a 900.</p></li><li><p>(Grupos de anúncios) -100 para smartphones e tablets (para não licitar o tipo de dispositivo) e de -90 a 900 para todos os tipos de dispositivo.</p></li></ul></ul><li><p>(Campanhas e grupos de anúncios existentes) Para usar o ajuste de oferta existente, deixe em branco.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Incluído nos bulksheets gerados para fins de informação) O ajuste de oferta somente leitura que a Adobe recomenda para o target de localização no nível da campanha ou uma RLSA. É calculado somente quando a campanha está em um portfólio com um objetivo que usa métricas de conversão ponderadas (não o objetivo [!UICONTROL Maximize Clicks]) e a campanha contém pelo menos dois destinos de localização ou RLSAs com pelo menos cinco cliques ou US$ 5 em custo nos últimos 90 dias.</p><p>Se quiser editar manualmente um destino de local ou RLSA para usar o valor recomendado, aguarde pelo menos duas semanas depois de criar o destino de local ou RLSA para permitir coleta de dados suficiente e não altere o valor mais de uma vez por semana. |
| [!UICONTROL Device Targets] | <p>(Somente tipos de campanha herdados) Os dispositivos nos quais o anúncio pode ser exibido: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> ou <i>[!UICONTROL Tablets]</i>. Para novas campanhas, o padrão é <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Somente tipos de campanha herdados; aplicável quando os Destinos do Dispositivo incluem &quot;Smartphones&quot; ou &quot;Tablets&quot;) Os sistemas operacionais nos quais o anúncio pode ser exibido: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> ou <i>[!UICONTROL Palm]</i>. Para novas campanhas, o padrão é <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Somente tipos de campanha herdados; aplicável quando [!UICONTROL Device Targets] inclui &quot;[!UICONTROL All]&quot; ou &quot;[!UICONTROL Smartphones]&quot;) Operadoras de celular às quais os smartphones podem estar conectados: <i>[!UICONTROL All]</i>, ou uma ou mais operadoras indicadas por &lt;c<i>código da operadora</i>>,&lt;<i>código do país</i>> (como T-Mobile,US) usando a lista de <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">operadoras disponíveis e códigos para [!DNL Google Ads]</a>. Separe várias operadoras com ponto e vírgula (como T-Mobile, EUA;T-Mobile, GB). Para novas campanhas, o padrão é <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>O nome exclusivo que identifica um grupo de anúncios. O comprimento máximo é de 255 caracteres; caracteres em branco à direita não são salvos (por exemplo, &quot;Grupo de anúncios 1 &quot; é salvo como &quot;Grupo de anúncios 1&quot;). Este campo não se aplica a sitelinks no nível da campanha ou destinos de dispositivo no nível da campanha.</p> |
| [!UICONTROL Ad Group Type] | <p>O tipo de grupo de anúncios: <i>[!UICONTROL Demand Gen]</i> (somente para campanhas de geração de demanda), <i>[!UICONTROL Display]</i> (para campanhas de exibição), <i>[!UICONTROL Search Dynamic]</i> (para anúncios de pesquisa dinâmicos expandidos), <i>[!UICONTROL Search Standard]</i> (para anúncios de pesquisa), <i>[!UICONTROL Shopping Product]</i> (para anúncios de produtos de compras), <i>[!UICONTROL Shopping Showcase]</i> (criação e edição sem suporte) ou <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Somente campanhas CPC) O custo máximo por clique (CPC), que é a quantidade mais alta a ser paga por um clique de anúncio na rede de anúncios, com ou sem símbolos monetários e pontuação. Você pode definir valores para grupos de anúncios e palavras-chave, grupos de produtos e alvos de pesquisa dinâmica. O padrão para uma nova palavra-chave é herdada do nível do grupo de anúncios. Para grupos de produtos, é possível definir valores para a camada mais baixa do grupo de produtos; o padrão para uma nova camada é herdado da camada principal.</p><p>Para grupos de produtos existentes e alvos de pesquisa dinâmica em portfólios otimizados, as atualizações são eficazes por apenas um dia e são substituídas durante o próximo ciclo de otimização.</p> |
| [!UICONTROL Max Content CPC] | <p>(Somente campanhas CPC) O custo máximo de conteúdo por clique (CPC), que é a quantidade mais alta a ser paga por um clique de anúncio em um site da rede de exibição, com ou sem símbolos e pontuação monetários. Você pode definir e editar valores no nível do grupo de anúncios em campanhas que não são direcionadas para posicionamento.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campanhas somente na rede de pesquisa e campanhas [!DNL Gmail] existentes somente leitura na rede de exibição) Se:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: para mostrar anúncios somente a usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios.</p><p>No entanto, você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, definindo ofertas mais altas para esses públicos-alvo.</p></li></ul> |
| [!UICONTROL Keyword] | A sequência de palavras-chave. O comprimento máximo é de 80 caracteres e não pode exceder 10 palavras, e pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [ ] ' + . / :`</p><p><b>Nota:</b></p><ul><li><p>Para excluir uma palavra-chave no nível do grupo de anúncios ou da campanha, defina o [!UICONTROL Match Type] como <i>[!UICONTROL Negative]</i>. Se a linha incluir o nome do grupo de anúncios, a palavra-chave será excluída do grupo de anúncios. Se a linha não incluir o nome do grupo de anúncios, a palavra-chave será excluída para toda a campanha.</p></li><li><p>Alterar uma palavra-chave [!DNL Google Ads] ou um tipo de correspondência exclui a palavra-chave existente e cria uma nova.</p></li></ul> |
| [!UICONTROL Placement] | (Campanhas que usam somente a correspondência de conteúdo) Um posicionamento na rede de exibição na qual seus anúncios podem ser exibidos. Especifique uma das seguintes opções:</p><ul><li><p>Site da Web: insira um URL válido. Pode ser um domínio de nível superior, subdomínio de primeiro nível ou domínio com um único nome de diretório. O URL não pode incluir um ponto de interrogação (?). Exemplos:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Uma posição de anúncio em uma página específica: Use o formato `<URL> >> <location,sublocation>` (como `finance.google.com >> Company pages,Top right`).</p></li><li><p>Uma categoria de tópico: Use a sintaxe `<category::<category> > <subcategory>` e assim por diante (como `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Observação:</b> para excluir um posicionamento no nível do grupo de anúncios ou da campanha, defina [!UICONTROL Match Type] como <i>[!UICONTROL Negative]</i>. Se a linha incluir o nome do grupo de anúncios, o posicionamento será excluído para o grupo de anúncios. Se a linha não incluir o nome do grupo de anúncios, o posicionamento será excluído para toda a campanha.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Obrigatório quando a configuração da campanha para &quot;[!UICONTROL Use my website contents to target my ads]&quot; não está habilitada; opcional caso contrário) Alvos de pesquisa dinâmica para o grupo de anúncios.</p><p>Para todos os destinos, use um asterisco (*).</p><p>Para direcionar até três critérios de pesquisa dinâmica, use o formato `<category>=<target>`, onde `<category>` pode incluir qualquer uma das categorias abaixo. Unir vários destinos para uma categoria individual com &quot;\[espaço em branco\] e \[espaço em branco\]&quot; e unir várias categorias com &quot;[espaço em branco] e [espaço em branco]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: para mostrar anúncios de pesquisa dinâmica expandidos para páginas indexadas com uma categoria de conteúdo [!DNL Google Ads] específica.</p></li><li><p><i>[!UICONTROL URL]</i>: Para mostrar anúncios de pesquisa dinâmica expandidos para páginas indexadas com uma URL específica, onde o valor pode ser incluído em qualquer lugar dentro da URL.</p></li><li><p><i>[!UICONTROL Page Title]</i>: para mostrar anúncios de pesquisa dinâmica expandidos para páginas indexadas com texto específico no título da página.</p></li><li><p><i>[!UICONTROL Page Content]</i>: para mostrar anúncios de pesquisa dinâmica expandidos para páginas indexadas com conteúdo específico.</p></li></ul><p>Exemplo: url=shoes.example.com e page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | A hierarquia de qualquer grupo de produtos principal.<br><br>Exemplo: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>O grupo de produtos (como &quot;brand=acme&quot; ou &quot;All Products&quot;).</p><p><b>Nota:</b></p><ul><li><p>Quando um grupo de produtos especificado não existe na hierarquia [!UICONTROL Parent Product Groupings], o Search, Social e Commerce cria todas as partes da hierarquia necessárias.</p></li><li><p>O Search, Social e Commerce cria automaticamente um grupo &quot;[!UICONTROL All Products]&quot; ao criar um grupo de anúncios em uma campanha de compras [!DNL Google Ads] com uma oferta padrão definida para a oferta padrão do grupo de anúncios. O Search, Social e Commerce cria automaticamente um grupo &quot;[!UICONTROL Everything Else]&quot; com a oferta padrão do grupo de anúncios em cada nível da hierarquia do grupo de produtos. Você ainda pode criar explicitamente esses grupos padrão e excluí-los ou alterar seus lances.</p></li><li><p>Cada grupo de publicidade pode incluir até oito camadas de grupos de produtos, incluindo &quot;[!UICONTROL All Products]&quot; e sete outras camadas.</p></li></ul> |
| [!UICONTROL Partition Type] | O tipo de partição do grupo de produtos: <i>subdivisão</i> (quando tem grupos de produtos filho) ou <i>unidade</i> (quando não tem grupos de produtos filho). |
| [!UICONTROL Match Type] | <p>Para grupos de produtos ou destinos de pesquisa dinâmica: a opção de correspondência de palavras-chave para o destino de pesquisa dinâmica ou grupo de produtos: <i>[!UICONTROL Dynamic Ad Target]</i> (o padrão para novos destinos de pesquisa dinâmica), <i>[!UICONTROL Product Group]</i> (o padrão para novos grupos de produtos) ou <i>[!UICONTROL Negative Product Group]</i> (para excluir um grupo de produtos).</p><p>Para palavras-chave: A opção de correspondência de palavras-chave para a palavra-chave: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> ou <i>[!UICONTROL Negative]</i> (para excluir uma palavra-chave ou um posicionamento na rede de exibição); os grupos de produtos usados com anúncios de compras têm um tipo de correspondência de <i>[!UICONTROL Product Group]</i>. Se você usar <i>[!UICONTROL Negative]</i>, também deverá incluir o tipo de correspondência a ser excluído (por exemplo, &quot;Frase negativa&quot;).</p><p>Para novas palavras-chave, o padrão é <i>[!UICONTROL Broad]</i>. Um valor para o tipo de correspondência ou ID de palavra-chave é necessário somente para editar uma palavra-chave com vários tipos de correspondência.</p><p><b>Nota:</b></p><ul><li><p>Os tipos de correspondência não se aplicam a anúncios de pesquisa dinâmica expandidos, que não usam palavras-chave.</p></li><li><p>Alterar o tipo de correspondência de uma palavra-chave [!DNL Google Ads] exclui a palavra-chave existente e cria uma nova.</p></li><li><p>Para o Modificador de correspondência ampla, escolha &quot;Amplo&quot; e insira um + antes de qualquer palavra-chave na palavra-chave para a qual as variantes próximas são necessárias (como &quot;+vermelho +sapatos&quot; para exigir variantes próximas de &quot;vermelho&quot; e &quot;sapatos&quot;). <b>Observação:</b> os modificadores de correspondência ampla agora têm o mesmo comportamento de correspondência que a correspondência de frases para alguns idiomas e você não pode criar novas palavras-chave do modificador de correspondência ampla desde julho de 2021. Consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/7042511) para obter mais informações.</p> |
| [!UICONTROL First Page Bid] | (Incluído em bulksheets gerados para fins de informação) A oferta necessária para colocar um anúncio na primeira página dos resultados da pesquisa. Este valor não é postado na rede de publicidade. |
| [!UICONTROL Quality Score] | (Incluída em bulksheets gerados para fins de informação) A pontuação de qualidade atual que o mecanismo de pesquisa atribuiu à palavra-chave. Este valor não é publicado na rede de publicidade.) |
| [!UICONTROL Creative Preferred Devices] | (Anúncios de texto, anúncios de pesquisa dinâmicos expandidos e sitelinks aprimorados; opcional) Os tipos de dispositivo nos quais você prefere exibir o anúncio: <i>[!UICONTROL All]</i> (padrão) ou <i>[!UICONTROL Mobile]</i>. Quando <i>[!UICONTROL Mobile]</i> é especificado, a rede tenta exibir o anúncio para usuários de dispositivos móveis em vez de usuários de desktop ou tablet. Caso contrário, a rede exibirá o anúncio em qualquer tipo de dispositivo.</p><p><b>Nota:</b></p><ul><li><p>Somente usuários administradores e [!DNL Adobe] gerentes de conta podem editar esta configuração.</p></li><li><p>A rede não garante que exibirá o anúncio no tipo de dispositivo preferido.</p></li><li><p>Os novos sitelinks aprimorados podem ser criados apenas em campanhas com sitelinks aprimorados existentes ou sem sitelinks.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Somente anúncios de texto expandidos e anúncios de pesquisa responsivos) Os títulos de um anúncio, cada um separado por uma barra vertical (&amp;vert;). O comprimento máximo para cada campo de título de anúncio é de 30 caracteres ou 15 caracteres de byte duplo, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).</p><p>Para anúncios de pesquisa responsivos, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] são obrigatórios, e todos os outros campos de título de anúncio são opcionais. Para excluir o valor existente de um campo não obrigatório, use o valor <code>[excluir]</code> (incluindo os colchetes).</p><p>Para anúncios de pesquisa responsivos, insira um personalizador de anúncios usando o seguinte formato: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, como <code>{CUSTOMIZER.Discount:10%}</code></p><p>Não é possível criar ou editar, mas você pode excluir anúncios de texto expandidos, que [!DNL Google Ads] descontinuou em junho de 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Somente anúncios de pesquisa responsivos; opcional) Uma posição na qual fixar o título do anúncio correspondente: `[null]` (sem valor, o que torna o título do anúncio qualificado para todas as posições), <i>1</i>, <i>2</i> ou <i>3</i>. Por exemplo, se [!UICONTROL Ad Title Position] tiver um valor de 1, o Título do anúncio aparecerá somente na Posição 1. Por padrão, todos os títulos de anúncios são nulos (sem valores).</p><p>Para excluir o valor existente, use o valor <code>[excluir]</code> (incluindo os colchetes).</p><p><b>Observação:</b> você pode fixar vários títulos de anúncios na mesma posição. A rede de anúncios usa um dos títulos de anúncios fixados na posição. Os títulos fixados na posição 3 podem não ser mostrados com o anúncio.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Anúncios de pesquisa dinâmicos expandidos, anúncios de texto expandidos e anúncios de pesquisa responsivos apenas) O corpo de um anúncio. O comprimento máximo para cada campo de descrição é de 90 caracteres ou 45 caracteres de byte duplo, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).</p><p>Para anúncios de pesquisa responsivos, insira um personalizador de anúncios usando o seguinte formato: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, como `{CUSTOMIZER.Discount:10%}`</p><p>Para anúncios de pesquisa dinâmica expandidos, use somente [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2]. <b>Observação:</b> para este tipo de anúncio, a alteração da cópia do anúncio exclui o anúncio existente e cria um novo.</p><p>Não é possível criar ou editar, mas você pode excluir anúncios de texto expandidos, que [!DNL Google Ads] descontinuou em junho de 2022.</p><p>Para anúncios de pesquisa responsivos, [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] são obrigatórios, e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] são opcionais. Para excluir o valor existente, use o valor <code>[excluir]</code> (incluindo os colchetes).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Somente anúncios de pesquisa responsivos; opcional) Uma posição na qual fixar a descrição correspondente: `[null]` (nenhum valor, o que torna a descrição qualificada para todas as posições), <i>1</i>, <i>2</i> ou <i>3</i>. Por exemplo, se [!UICONTROL Description 1 Position] tiver um valor de 1, então [!UICONTROL Description 1] aparecerá somente na Posição 1. Por padrão, nenhuma descrição é fixada a uma posição.</p><p>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes).</p><p><b>Observação:</b> você pode fixar várias descrições na mesma posição. A rede de anúncios usa uma das descrições fixadas na posição. As descrições fixadas na posição 2 podem não ser mostradas com o anúncio. |
| [!UICONTROL Display URL] | O URL incluído no anúncio.<br><br>Para anúncios de pesquisa dinâmica expandidos, [!DNL Google Ads] gera esse valor dinamicamente a partir do domínio do site, e você não precisa inserir um valor.<br><br>Para anúncios de pesquisa responsivos, não é necessário inserir um valor. O URL de exibição é extraído automaticamente do domínio no URL final. Opcionalmente, é possível personalizar o URL usando os campos Caminho 1 e Caminho 2.<br><br>Não é possível criar ou editar, mas você pode excluir anúncios de texto expandidos, que [!DNL Google Ads] descontinuou em junho de 2022.<br><br><b>Observação:</b> (Contas com URLs finais) os nomes de domínio na URL de exibição e na URL final devem corresponder.</p> |
| [!UICONTROL Display Path 1] | <p>(Anúncios de texto expandidos<span> e anúncios de pesquisa responsivos</span> somente)</p><p>(Opcional) Texto adicionado ao URL de exibição que é extraído automaticamente do URL final. Ele é precedido no URL por uma barra (/). Um caminho não pode conter caracteres de barra (/) ou de nova linha (\n). O comprimento máximo é de 15 caracteres ou 7 caracteres de byte duplo.</p><p>Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`</p><p>Por exemplo, se [!UICONTROL Display Path 1] for &quot;ofertas&quot;, a URL de exibição será &lt;<i>URL de exibição</i>>/ofertas, como www.example.com/deals.</p><p>Não é possível criar ou editar, mas você pode excluir anúncios de texto expandidos, que [!DNL Google Ads] descontinuou em junho de 2022.</p> |
| [!UICONTROL Display Path 2] | Um segundo caminho de exibição; consulte a entrada para [!UICONTROL Display Path 1].<br><br>Exemplo: se [!UICONTROL Display Path 1] for &quot;ofertas&quot; e [!UICONTROL Display Path 2] for &quot;local&quot;, a URL de exibição será &lt;<i>URL de exibição</i>>/ofertas/local, como www.example.com/deals/local.</p><p>Não é possível criar ou editar, mas você pode excluir anúncios de texto expandidos, que [!DNL Google Ads] descontinuou em junho de 2022.</p> |
| [!UICONTROL Promotion Line] | (Somente anúncios de listagem de produtos) Uma linha de promoção opcional a ser incluída na listagem de produtos nos resultados da pesquisa. O comprimento máximo é de 45 caracteres.</p><p>A linha de promoção pode aparecer em locais diferentes relacionados ao anúncio (como abaixo do anúncio), dependendo de onde o anúncio aparece na página. |
| [!UICONTROL Link Name] | <p>O texto do sitelink. Pode incluir até 25 caracteres.</p><p>Para novos sitelinks, você deve incluir o nome da campanha na linha do sitelink. Para sitelinks de nível de grupo de anúncios, você também deve incluir o nome do grupo de anúncios.</p><p><b>Observação:</b> texto existente de 35 caracteres ainda é exibido em anúncios em computadores e tablets, mas não em dispositivos móveis.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Somente anúncios de instalação de aplicativo existentes) O sistema operacional no qual o aplicativo móvel é executado: <i>Android™</i> ou <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Somente anúncios de instalação de aplicativo existentes) <p>A ID do aplicativo ou o nome do pacote. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Somente anúncios de instalação de aplicativo existentes) O nome do aplicativo. |
| [!UICONTROL Start Date] | <p>(Somente sitelinks aprimorados) A primeira data em que podem ser feitas ofertas para o sitelink, no fuso horário do anunciante e em um dos seguintes formatos: <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i> ou <i>m-d-yyy</i>. O padrão para novos sitelinks aprimorados é o dia atual.</p><p><b>Observação:</b> novos sitelinks aprimorados podem ser criados apenas em campanhas com sitelinks aprimorados existentes ou sem sitelinks.</p> |
| [!UICONTROL End Date] | <p>(Somente sitelinks aprimorados) A última data em que podem ser feitas ofertas para o sitelink, no fuso horário do anunciante e em um dos seguintes formatos:  <i>d/m/yyyy</i>, <i>d/m/yyy</i>, <i>d-m-yyyy</i> ou <i>d-m-yyy</i>. O padrão é nenhum (sem data final).</p><p><b>Observação:</b> novos sitelinks aprimorados podem ser criados apenas em campanhas com sitelinks aprimorados existentes ou sem sitelinks.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Somente anúncios de instalação de aplicativo existentes)</p><p>(Opcional) Impede [!DNL Google Ads] de exibir o anúncio para os usuários do tablet. Os valores podem incluir <i>sim</i> e <i>não</i>. |
| [!UICONTROL Landing Page Suffix] | Quaisquer parâmetros a serem anexados ao final dos URLs finais para rastrear informações. Exemplo: `param2=value1&param3=value2`<br><br>Consulte &quot;[Formatos de rastreamento de cliques para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)&quot;.<br><br>Sufixos finais de URL em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | O modelo de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e incorpora a URL final em um parâmetro [!DNL ValueTrack]. O modelo de rastreamento no nível mais granular (com a palavra-chave como o mais granular) substitui os valores em todos os níveis mais altos.<br><br>Para o controle de conversão do Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce adiciona automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.<br><br>Para redirecionamentos e rastreamento de terceiros, insira um valor. Para obter uma lista de parâmetros [!DNL ValueTrack] para indicar URLs finais em modelos de rastreamento, consulte os parâmetros &quot;Somente modelo de rastreamento&quot; na seção sobre &quot;Parâmetros [!DNL ValueTrack] disponíveis&quot; na [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/2375447).<br><br>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Base URL/Final URL] | O URL da página de aterrissagem para o qual os usuários do mecanismo de pesquisa são levados quando clicam em seu anúncio, incluindo quaisquer parâmetros de acréscimo configurados para a campanha ou conta. URLs base/final no nível de palavra-chave substituem aqueles no nível de anúncio e superior.<br><br>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Destination URL] | (Incluído em bulksheets gerados para fins de informação; não publicado no mecanismo de pesquisa) Para contas com URLs de destino, este é o URL que vincula um anúncio a um URL/página inicial base no site do anunciante (às vezes, por meio de outro site que rastreia o clique e redireciona o usuário para a página inicial). Inclui quaisquer parâmetros de acréscimo configurados para a campanha ou conta do Search, Social e Commerce. Se você gerou URLs de rastreamento, eles se baseiam nos parâmetros de rastreamento das configurações da conta e das configurações da campanha. Se você anexou parâmetros específicos do mecanismo de pesquisa, eles podem ser substituídos pelos parâmetros equivalentes para Pesquisa, Social e Commerce.<br><br>Para contas com URLs finais, esta coluna mostra o mesmo valor que a coluna URL Base/URL Final. |
| [!UICONTROL Custom URL Param] | Dados para substituir a variável dinâmica `{custom_code}` quando a variável for incluída nos parâmetros de rastreamento da conta de pesquisa ou nas configurações da campanha. Para inserir o valor personalizado no URL de rastreamento, você deve fazer upload do arquivo de bulksheet usando a opção Gerar URLs de rastreamento. |
| [!UICONTROL Creative Type] | O formato do anúncio: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (anúncios do carrossel de várias imagens), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> e <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (tipo de anúncio obsoleto), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (obsoleto), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (anúncios de compras) ou <i>[!UICONTROL Responsive search ad]</i>. O padrão para novos anúncios é <i>[!UICONTROL Text ad]</i>.<br><br>Obrigatório para criar ou editar o status de um anúncio de produto. |
| [!UICONTROL Param1] | <p>O valor numérico do parâmetro de anúncio `{param1}`, que pode ser incluído na cópia do anúncio ou na URL de exibição para qualquer anúncio no arquivo de bulksheet. O comprimento máximo é de 25 caracteres e você pode incluir os seguintes caracteres não numéricos:</p><ul><li><p>O valor pode ser precedido ou anexado com um símbolo ou código de moeda. Por exemplo, `£2.000,00` e `2000GBP` são válidos.</p></li><li><p>O valor pode incluir uma vírgula (`,`) ou ponto (`.`) como separador, com um ponto opcional (`.`) ou vírgula (`,`) para valores fracionais. Por exemplo, `1,000.00` e `2.000,10` são válidos.</p></li><li><p>O valor pode ser prefixado ou anexado com um sinal de porcentagem (`%`), sinal de adição (`+`) ou sinal de subtração (`- `). Por exemplo, `20%`, `208+` e `-42.32` são válidos.</p></li><li><p>Dois números podem ser incorporados com uma barra. Por exemplo, `4/1` e `0.95/0.45` são válidos.</p></li></ul><p>Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes).</p> |
| [!UICONTROL Param2] | O valor numérico do parâmetro de anúncio `{param2}`, que pode ser incluído na cópia do anúncio ou na URL de exibição para qualquer anúncio no arquivo de bulksheet. Consulte a entrada para Param1 para obter mais informações. |
| [!UICONTROL Audience] | A lista de remarketing para o público-alvo ou público-alvo excluído da campanha ou do grupo de publicidade. Especifique se é um target ou uma exclusão no campo &quot;Target Type&quot;. |
| [!UICONTROL Target Type] | (Quando um Público-alvo é especificado) Se o público-alvo especificado é uma <i>Inclusão</i> (destino) ou <i>Exclusão</i>. |
| [!UICONTROL Campaign Status] | O status de exibição da campanha: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (não editável) ou <i>[!UICONTROL Deleted]</i> (somente campanhas existentes). O padrão para novas campanhas é <i>[!UICONTROL Active]</i>. Para excluir uma campanha ativa ou pausada, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | O status de exibição do grupo de anúncios: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente grupos de anúncios existentes). O padrão para novos grupos de anúncios é [!UICONTROL Active]. Para excluir um grupo de anúncios ativo ou pausado, insira o valor `Deleted`. |
| [!UICONTROL Keyword Status] | O status de exibição da palavra-chave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente palavras-chave existentes). O padrão para novas palavras-chave é [!UICONTROL Active]. Para excluir uma palavra-chave ativa ou pausada, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | O status de exibição do anúncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (somente anúncios existentes), <i>[!UICONTROL Disapproved]</i> (não editável) ou <i>[!UICONTROL Paused]</i>. O padrão para novos anúncios é [!UICONTROL Active]. Para excluir um anúncio ativo ou pausado, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | O status do posicionamento do site: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente anúncios existentes). O padrão para novos sites é <i>Ativo.</i> Para excluir um posicionamento ativo ou pausado, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | O status de um destino de pesquisa dinâmica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (somente destinos existentes). O padrão para novos destinos é <i>Ativo.</i> Para excluir um destino ativo ou pausado, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | O status de exibição do grupo de produtos: <i>[!UICONTROL Active]</i> <span>ou</span> <i>[!UICONTROL Deleted]</i> (somente grupos de produtos existentes). O padrão para novos grupos de produtos é <i>[!UICONTROL Active]</i>. Para excluir um grupo de produtos ativo, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | O status de exibição do sitelink: <i>Ativo ou Excluído</i> (somente sitelinks existentes). O padrão para novos sitelinks é <i>[!UICONTROL Active]</i>. Para excluir um sitelink ativo, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | O status do destino do local: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (somente locais existentes). O padrão para novos locais é [!UICONTROL Active]. Para excluir um local ativo, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | O status do destino ou exclusão RLSA no nível da campanha ou do grupo de anúncios: <i>[!UICONTROL Active]</i> ou [!UICONTROL Deleted]</i> (somente destinos existentes). O padrão para novos destinos ou exclusões é <i>[!UICONTROL Active]</i>. Para excluir um destino ou exclusão ativa, insira o valor <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>O status do destino do dispositivo no nível da campanha ou do grupo de anúncios: <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Para novas campanhas e grupos de anúncios, o padrão é <i>[!UICONTROL Active]</i>.</p> |
| \[Classificação de rótulo específica do anunciante\] | (Nomeado para uma classificação de rótulo específica do anunciante, como &quot;Cor&quot; para uma classificação de rótulo chamada Cor) Um valor para a classificação especificada associada à entidade. Você pode incluir apenas um valor por classificação por entidade (como &quot;vermelho&quot; para a classificação de rótulo &quot;Cor&quot; para a Campanha A). O comprimento máximo é de 100 caracteres e o valor pode incluir caracteres ASCII e não ASCII.<br><br>As classificações de rótulo e seus valores de rótulo são aplicados a todos os componentes filhos; novos componentes adicionados posteriormente são associados automaticamente ao rótulo. As classificações de etiquetas para grupos de produtos são aplicadas ao nível de unidade (mais granular).<br><br>Nem o nome de classificação nem o valor de classificação fazem distinção entre maiúsculas e minúsculas. |
| [!UICONTROL Constraints] | Uma restrição atribuída à entidade. Você pode atribuir somente uma restrição por entidade.<br><b>>As restrições são herdadas por entidades filhas, portanto, não é necessário inserir valores para entidades filhas, a menos que você queira substituir os valores herdados. |
| [!UICONTROL Campaign ID] | A ID exclusiva que identifica uma campanha existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a campanha. |
| [!UICONTROL Ad Group ID] | O identificador exclusivo que identifica um grupo de anúncios existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o grupo de anúncios. |
| [!UICONTROL Keyword ID] | A ID exclusiva que identifica uma palavra-chave existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera a palavra-chave, a menos que a linha inclua a) colunas de propriedade suficientes para identificar a palavra-chave ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>A ID exclusiva que identifica um anúncio existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Para anúncios de pesquisa responsivos, a ID do anúncio ou a ID do AMO é necessária para editar ou excluir dados de anúncios. Para todos os outros tipos de entidade, a ID do anúncio é necessária somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade do anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado.</p><p><b>Observação:</b> se você editar a) as colunas de propriedade do anúncio, exceto o Status de um anúncio existente, ou b) os dados de um anúncio de pesquisa responsivo e não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID], então um novo anúncio será criado e o anúncio existente não será alterado.</p> |
| [!UICONTROL Placement ID] | A ID exclusiva que identifica o posicionamento de um site. Obrigatório somente ao alterar ou excluir o posicionamento, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o posicionamento ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | A ID exclusiva que identifica um direcionamento automático existente. Necessário somente quando você altera ou exclui o direcionamento automático, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL Product Group ID] | A ID exclusiva que identifica um grupo de produtos existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente ao alterar ou excluir o grupo de produtos, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o grupo de produtos ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | A ID exclusiva que identifica um sitelink existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente ao alterar ou excluir o sitelink, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o sitelink ou b) um &quot;[!UICONTROL AMO ID]&quot;.&quot; No entanto, se você não incluir [!UICONTROL Sitelink ID] nem [!UICONTROL AMO ID] e as colunas de propriedade corresponderem a vários sitelinks, o status de apenas um dos sitelinks será alterado.</p><p><b>Observação:</b> se você editar as colunas de propriedade do sitelink, exceto o Status de um sitelink existente, e não incluir o [!UICONTROL Sitelink ID] nem o [!UICONTROL AMO ID], um novo sitelink será criado e o sitelink existente não será alterado. |
| [!UICONTROL RLSA Target ID] | A ID exclusiva que identifica um destino ou exclusão de RLSA em nível de campanha ou grupo de anúncios existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera ou exclui o destino ou a exclusão, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL Device Target ID] | <p>A ID exclusiva que identifica um direcionamento ou exclusão de dispositivo existente no nível da campanha ou do grupo de anúncios. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Necessário somente quando você altera ou exclui o destino, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino.</p> |
| [!UICONTROL AMO ID] | (Em bulksheets gerados) Um identificador exclusivo gerado pela Adobe para uma entidade sincronizada. Para anúncios de pesquisa responsivos, a ID do AMO é necessária para editar ou excluir anúncios, a menos que você inclua a ID do anúncio. Para editar dados para todos os outros tipos de entidade com uma ID AMO, a ID AMO é necessária para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |
| [!UICONTROL EF Error Message] | (Incluído nos bulksheets gerados para fins informativos) Espaço reservado para exibir mensagens de erro da rede de publicidade relacionadas aos dados na linha; as mensagens de erro estão incluídas nos arquivos [!UICONTROL EF Errors]. Este valor não é postado na rede de publicidade. |
| [!UICONTROL SE Error Message] | (Incluído nos bulksheets gerados para fins informativos) Espaço reservado para exibir mensagens de erro da rede de publicidade relacionadas aos dados na linha; as mensagens de erro estão incluídas nos arquivos [!UICONTROL SE Errors]. Este valor não é postado na rede de publicidade. |
| [!UICONTROL Exemption Request] | (Incluído nos bulksheets gerados para fins de informação) Espaço reservado para exibir os nomes e o texto de qualquer política de publicidade que um anúncio viola.[!DNL Google Ads] |
| [!UICONTROL Retail Hash] | (Incluído para fins de informação em bulksheets gerados usando o Gerenciamento avançado de campanha) Um código de hash alfanumérico (como f9639f40cdf56524b541e5dacf55a991) que indica que o item foi gerado usando a visualização Avançado (ACM). |

[^1]: [!DNL Excel] converte números grandes em notação científica (como 2.12E+09 para 2115585666) quando abre o arquivo. Para exibir dígitos na notação padrão, selecione qualquer célula na coluna e clique dentro da barra de fórmulas.

## Campos necessários para criar, editar ou excluir cada componente da conta {#bulksheet-fields-per-component-google}

As seções a seguir incluem os campos relevantes para entidades de conta específicas.

>[!NOTE]
>
>Quando um campo não é aplicável a uma ação, qualquer valor inserido no campo é ignorado.

### Campos de campanha

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Campaign Budget] | Obrigatório para criar uma campanha. |
| [!UICONTROL Delivery Method] | Obrigatório para criar uma campanha. |
| [!UICONTROL Channel Type] | Obrigatório para criar uma campanha. |
| [!UICONTROL Networks] | Obrigatório para criar uma campanha. |
| [!UICONTROL DSA Domain Name] | Obrigatório para criar uma campanha com anúncios de pesquisa dinâmica na rede de pesquisa. |
| [!UICONTROL DSA Domain Language] | Obrigatório para criar uma campanha com anúncios de pesquisa dinâmica na rede de pesquisa. |
| [!UICONTROL Campaign Priority] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Merchant ID] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Sales Country] | Obrigatório para criar uma campanha de compras. |
| [!UICONTROL Product Scope Filter] | (Campanhas de compras) Opcional |
| [!UICONTROL Languages] | Opcional |
| [!UICONTROL Device Targets] | Opcional |
| [!UICONTROL Device Targets (Google Adwords)] | Opcional |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Opcional |
| [!UICONTROL Audience Target Method] | n/d |
| [!UICONTROL Landing Page Suffix] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Campaign Status] | Necessário apenas para excluir uma campanha. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Obrigatório somente quando você altera o nome da campanha, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a campanha. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Networks] | n/d |
| [!UICONTROL GDN Custom Bid Level] | Opcional |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Group Type] | Obrigatório para criar um grupo de anúncios. |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Max Content CPC] | Opcional |
| [!UICONTROL Audience Target Method] | Obrigatório |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Ad Group Status] | Obrigatório apenas para excluir um grupo de anúncios. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Ad Group ID] | Obrigatório somente quando você altera o nome do grupo de anúncios, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o grupo de anúncios. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de palavra-chave

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Keyword] | Obrigatório |
| [!UICONTROL Match Type] | Um valor para o tipo de correspondência ou ID de palavra-chave é necessário para editar ou excluir uma palavra-chave com vários tipos de correspondência. |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Param1] | Opcional |
| [!UICONTROL Param2] | Opcional |
| [!UICONTROL Keyword Status] | Necessário somente para excluir uma palavra-chave. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Keyword ID] | Obrigatório somente ao editar ou excluir a palavra-chave, a menos que a linha inclua a) colunas de propriedade suficientes para identificar a palavra-chave ou b) um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de posicionamento

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Opcional |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Opcional |
| [!UICONTROL Placement] | Obrigatório |
| [!UICONTROL Match Type] | Obrigatório |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Placement Status] | Necessário somente para excluir um posicionamento. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Placement ID] | Obrigatório somente ao editar ou excluir o posicionamento, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o posicionamento ou b) um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Anúncio de pesquisa dinâmica expandido

Este tipo de anúncio agora é chamado de &quot;anúncio de pesquisa dinâmica&quot; em [!DNL Google Ads]. Para obter mais informações sobre como criar anúncios de pesquisa dinâmica, consulte &quot;[Implementar [!DNL Google Ads] anúncios de pesquisa dinâmica](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html)&quot;.

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obrigatório para criar um anúncio ou editar a descrição. <b>Observação:</b> para este tipo de anúncio, a alteração da cópia do anúncio exclui o anúncio existente e cria um novo. |
| [!UICONTROL Display URL] | Obrigatório |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Creative Type] | Obrigatório para criar ou editar o status de um anúncio de produto. |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade do anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Lista de produtos/campos de anúncios de compras

Para obter mais informações sobre como criar anúncios de compras, consulte &quot;[Implementar [!DNL Google Ads] campanhas de compras](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html)&quot;.

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Promotion Line] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Opcional |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Obrigatório para criar ou editar o status de um anúncio de produto. |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a) colunas de propriedade do anúncio suficientes para identificar o anúncio ou b) um &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de anúncio de pesquisa responsivos

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Responsive Search Ad]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Para anúncios de pesquisa responsivos, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] são necessários para criar um anúncio, e todos os outros campos de título de anúncio são opcionais. Para excluir o valor existente de um campo não obrigatório, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Opcional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Para anúncios de pesquisa responsivos, [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] são necessários para criar um anúncio, e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] são opcionais. Para excluir o valor existente, use o valor `[delete]` (incluindo os colchetes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Opcional |
| [!UICONTROL Display Path 1] | Opcional |
| [!UICONTROL Display Path 2] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Obrigatório para criar um anúncio. |
| [!UICONTROL Custom URL Param] | Opcional |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório para excluir um anúncio. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório para editar ou excluir anúncios, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir anúncios, a menos que você inclua a ID do anúncio. |

### Campos de anúncio de texto

Para este tipo de anúncio, use a linha &quot;[!UICONTROL Creative (except RSA)]&quot; na caixa de diálogo [!UICONTROL Download Bulksheet].

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

>[!NOTE]
>
>Anúncios de texto expandidos foram descontinuados em junho de 2022. Só é possível excluir anúncios de texto existentes.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Creative Preferred Devices] | Somente leitura |
| [!UICONTROL Ad Title], Título do anúncio 2-3 | Somente leitura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Somente leitura |
| [!UICONTROL Display URL] | Somente leitura |
| [!UICONTROL Display Path 1] | Somente leitura |
| [!UICONTROL Display Path 2] | Somente leitura |
| [!UICONTROL Tracking Template] | Somente leitura |
| [!UICONTROL Base URL/Final URL] | Somente leitura |
| [!UICONTROL Custom URL Param] | Somente leitura |
| [!UICONTROL Creative Type] | Opcional |
| [!UICONTROL Ad Status] | Obrigatório |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Ad ID] | Obrigatório somente quando você altera o status do anúncio, a menos que a linha inclua a&amp;rpar; colunas de propriedade de anúncio suficientes para identificar o anúncio ou b&amp;rpar; e &quot;[!UICONTROL AMO ID].&quot; No entanto, se você não incluir [!UICONTROL Ad ID] nem [!UICONTROL AMO ID] e as colunas de propriedade de anúncio corresponderem a vários anúncios, o status de apenas um dos anúncios será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino da pesquisa dinâmica (direcionamento automático)

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Max CPC] | Opcional |
| [!UICONTROL Auto Target Expression] | Necessário apenas quando a configuração da campanha para &quot;[!UICONTROL Use my website contents to target my ads]&quot; não está habilitada. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Target Status] | Obrigatório para excluir um público alvo |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Target ID] | Necessário somente quando você altera ou exclui o direcionamento automático, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de grupo de produtos de compras

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório |
| [!UICONTROL Max CPC] | Obrigatório para criar um grupo de produtos. |
| [!UICONTROL Parent Product Groupings] | Obrigatório |
| [!UICONTROL Product Grouping] | Obrigatório |
| [!UICONTROL Partition Type] | Obrigatório para criar um grupo de produtos. |
| [!UICONTROL Match Type] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Obrigatório |
| [!UICONTROL Product Group Status] | Necessário apenas para excluir um grupo de produtos. |
| \[Classificação de rótulo específica do anunciante\] | Opcional |
| [!UICONTROL Constraints] | Opcional |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Product Group ID] | Obrigatório somente quando você altera ou exclui o grupo de produtos, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o grupo de produtos ou b) um &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de sitelink no nível da campanha e do grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Ad Group Name] | Obrigatório para sitelinks de nível de grupo de anúncios. Não aplicável para sitelinks no nível da campanha. |
| [!UICONTROL Creative Preferred Devices] | Opcional |
| [!UICONTROL Link Name] | Obrigatório |
| [!UICONTROL Start Date] | Opcional |
| [!UICONTROL End Date] | Opcional |
| [!UICONTROL Tracking Template] | Opcional |
| [!UICONTROL Base URL/Final URL] | Obrigatório |
| [!UICONTROL Sitelink Status] | Necessário somente para excluir um sitelink. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional |
| [!UICONTROL Sitelink ID] | Necessário somente ao alterar ou excluir o sitelink, a menos que a linha inclua a) colunas de propriedade suficientes para identificar o sitelink ou b) um &quot;[!UICONTROL AMO ID]&quot;. No entanto, se você não incluir [!UICONTROL Sitelink ID] nem [!UICONTROL AMO ID] e as colunas de propriedade corresponderem a vários sitelinks, o status de apenas um dos sitelinks será alterado.<br><br><b>Observação:</b> se você editar as colunas de propriedade do sitelink, exceto [!UICONTROL Status] para um sitelink existente, e não incluir o [!UICONTROL Sitelink ID] nem o [!UICONTROL AMO ID], um novo sitelink será criado e o sitelink existente não será alterado. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Destino da localização

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Location] | Obrigatório |
| [!UICONTROL Location Type] | Opcional |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Location Status] | Necessário apenas para excluir um destino de local. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL AMO ID] | É necessário editar ou excluir os dados, a menos que você inclua o [!UICONTROL Campaign ID].<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino do dispositivo no nível da campanha e do grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Device] | Necessário para criar ou editar um destino de dispositivo. |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Obrigatório para destinos de dispositivo de nível de grupo de anúncios. Não aplicável para alvos de dispositivo no nível da campanha. |
| [!UICONTROL Device Target Status] | Necessário apenas para excluir um destino de dispositivo. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicável somente para alvos de dispositivo de nível de grupo de anúncios. |
| [!UICONTROL Device Target ID] | Necessário somente quando você altera ou exclui o destino, a menos que a linha inclua um &quot;[!UICONTROL AMO ID]&quot; para o destino. |
| [!UICONTROL AMO ID] | Obrigatório para editar ou excluir os dados, a menos que você inclua a ID de destino do dispositivo.<br><br>O Search, Social e Commerce usa o valor para determinar a identidade correta a ser editada, mas não publica a ID na rede de anúncios. |

### Campos de destino/exclusão RLSA no nível da campanha e do grupo de anúncios

Para obter uma descrição de cada campo de dados, consulte &quot;[Todos os campos de dados disponíveis](#bulksheet-fields-all-google)&quot;.

| Campo | Obrigatório? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obrigatório, a menos que cada linha inclua um &quot;[!UICONTROL AMO ID]&quot; para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório |
| [!UICONTROL Bid Adjustment] | Opcional |
| [!UICONTROL Ad Group Name] | Obrigatório para públicos-alvo e exclusões em nível de grupo de anúncios. Não aplicável para metas e exclusões no nível da campanha. |
| [!UICONTROL Audience] | Necessário para criar um novo público-alvo ou exclusão. |
| [!UICONTROL Target Type] | Necessário para criar um novo público-alvo ou exclusão. |
| [!UICONTROL RLSA Target Status] | Necessário apenas para excluir um target ou exclusão. |
| [!UICONTROL Campaign ID] | Opcional |
| [!UICONTROL Ad Group ID] | Opcional; aplicável somente para exclusões e públicos-alvo no nível do grupo de anúncios. |
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
