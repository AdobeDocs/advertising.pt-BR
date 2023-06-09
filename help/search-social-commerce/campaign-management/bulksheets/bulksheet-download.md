---
title: Baixar/criar um arquivo de bulksheet
description: Saiba como criar arquivos de bulksheet baixando dados de conta para suas redes de anúncios.
source-git-commit: 5d76794c06bbdd563a1ce0f01d219ccd8a3da0b6
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---

# Baixar/criar um arquivo de bulksheet

Você pode criar bulksheets usando configurações personalizadas para uma ou mais contas em uma ou mais [redes de publicidade suportadas](bulksheet-about.md#bulksheet-functionality-by-network). Os bulksheets incluem dados no Search, Social e Commerce.

Para campanhas sincronizadas, você pode, opcionalmente, sincronizar com a rede de anúncios antes de baixar os dados para garantir que as alterações de dados recentes no lado da rede de anúncios sejam incluídas. Para todas as redes de anúncios, é possível gerar novos URLs de rastreamento de cliques para incluir no arquivo.

>[!NOTE]
>
>Também é possível [criar um arquivo de bulksheet com base nas colunas visíveis em uma visualização de gerenciamento de campanha](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. No menu principal, clique em **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Na barra de ferramentas, clique em **[!UICONTROL Download Bulksheet]**.

1. Especifique a [configurações de bulksheet](#bulksheet-download-settings):

1. No **[!UICONTROL Selections]** insira ou selecione informações nos campos.

1. (Opcional) Clique no link **[!UICONTROL Rows and Columns]** especifique os componentes da conta e os status dos componentes que deseja incluir linhas na bulksheet e, em seguida, especifique as colunas a serem incluídas para cada componente selecionado.

   Para obter uma lista de linhas de bulksheet disponíveis, consulte &quot;[Linhas de bulksheet por rede de anúncios](#bulksheet-rows-by-ad-network).&quot;

1. (Opcional) Clique no link **[!UICONTROL Filters]** e indique os critérios para campanhas, grupos de anúncios, anúncios/criações, palavras-chave, disposições e outras entidades específicas a serem incluídas na bulksheet:

   1. Selecione um parâmetro (nome ou ID da entidade; ou qualquer elemento de um anúncio, palavra-chave ou posicionamento), selecione um operador e insira o valor aplicável. Por exemplo, para retornar apenas anúncios com &quot;sapatos&quot; no título de um [!DNL Google Ads] conta, selecione *Título*, selecione *[!UICONTROL contains]* e insira `shoes` no campo de entrada.

   1. (Para aplicar filtros adicionais) Para cada filtro adicional, clique em **[!UICONTROL +Add Filter]**, selecione **[!UICONTROL AND]** ou **[!UICONTROL OR]**, selecione um elemento de anúncio ou palavra-chave e um operador e insira o valor aplicável.

1. Clique em **[!UICONTROL Download]**.

Quando a tarefa for iniciada, a janela exibirá uma notificação, mas permanecerá aberta para que você possa continuar criando bulksheets adicionais, se desejar. Quaisquer filtros e exclusões especificados aplicáveis a quaisquer novas contas selecionadas são retidos. Quando a tarefa for iniciada, o arquivo será listado na exibição Bulksheets. Quando o arquivo é criado, você recebe uma notificação por email com um link para o arquivo; dependendo da quantidade de dados que está sendo compilada, a notificação pode levar vários minutos ou mais. No entanto, se a geração de arquivo falhar, um arquivo de erro será listado na exibição Bulksheets e você receberá uma notificação por email com um link para o arquivo de erro.

## Configurações de download de bulksheet {#bulksheet-download-settings}

| Guia | Parâmetro | Descrição |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | As contas, campanhas ou grupos de anúncios nos quais os dados serão carregados:<ul><li>Para selecionar uma conta e todas as campanhas e grupos de anúncios, marque a caixa de seleção ao lado do nome da conta e clique em >> para movê-la para a [!UICONTROL Selected Filters] coluna.</li><li>Para selecionar campanhas individuais ou grupos de anúncios, clique em próximo à conta para expandi-la (se necessário). Clique em próximo à campanha para expandi-la, marque a caixa de seleção ao lado do nome da campanha ou do grupo de anúncios e clique em >> para movê-la para a [!UICONTROL Selected Filters] coluna. Por exemplo, para obter dados somente para a Campanha 1 na Conta 1, expanda Conta 1, marque a caixa de seleção ao lado de Campanha 1 e mova-a para a [!UICONTROL Selected Filters] coluna.</li></ul><b>Notas:</b><ul><li>Uma única planilha em massa pode ser aplicada a várias contas em várias redes de anúncios. As colunas específicas da rede de anúncios são rotuladas em bulksheets com o nome da rede de anúncios (como &quot;Operadoras de celular (Google Ads)&quot;).</li><li>Para ver que tipo de componente é qualquer item, mantenha o cursor sobre ele.</li><li>Para campanhas do, a primeira letra do nome da rede de publicidade está entre parênteses após o nome da conta (como &quot;Acme Realty (G)&quot; para uma [!DNL Google Ads] conta).</li><li>Por padrão, somente as contas ativas e ativadas e seus componentes ativos são listados. Para exibir componentes pausados e excluídos, clique em ![Seta para baixo](/help/search-social-commerce/assets/arrow-down-expand.png "Seta para baixo") ao lado de [!UICONTROL Show] e selecione **[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Opcional) Inclui modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para palavras-chave, anúncios, posicionamentos, sitelinks e [!DNL Google Ads] grupos de produtos na bulksheet. Por padrão, essa opção está selecionada.<br><br>Quando essa opção é selecionada, os URLs são gerados de acordo com os parâmetros na [!UICONTROL Campaign Tracking] seção das configurações da conta ou das configurações da campanha. Por padrão, se os URLs de rastreamento já existirem, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto do anúncio ou os parâmetros de rastreamento da conta tenham sido alterados).<br><br><b>Notas:</b><ul><li>Se o anunciante usar o rastreamento de conversão de Adobe Advertising e a conta relevante não estiver configurada para gerar e carregar automaticamente URLs de rastreamento, você deverá gerar novos URLs de rastreamento quando os URLs de base tiverem sido alterados.</li><li>Se você não selecionar essa opção, ainda poderá gerar URLs de rastreamento posteriormente ao fazer upload ou publicar o arquivo.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Opcional) Instrui o Search, Social e Commerce a sincronizar seus arquivos com as campanhas especificadas para garantir que todos os dados sejam os mesmos. Por padrão, essa opção não está selecionada.<br><b>Nota:</b> O Search, Social e Commerce sincroniza automaticamente com a rede de anúncios uma vez por dia, sempre que detecta uma nova campanha na rede de anúncios e sempre que você altera os dados da campanha no Search, Social e Commerce. Selecione essa opção se você achar que alterações recentes nos dados da campanha ou da conta foram feitas diretamente na rede de anúncios ou usando o editor de desktop da rede de anúncios. A criação de bulksheet demora mais ao selecionar essa opção. |
| | [!UICONTROL Bulksheet Name] | O nome da nova bulksheet e o tipo de arquivo. Por padrão, o arquivo é criado no formato de valores separados por tabulação e é nomeado como uma das seguintes opções:<ul><li>(para todas as contas da rede de anúncios) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(para contas únicas) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(para várias contas) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>Você pode renomear o arquivo. O nome não pode incluir os seguintes caracteres: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>Opcionalmente, altere o tipo de arquivo. As opções incluem *[!UICONTROL .tsv]* (para valores separados por tabulação), *[!UICONTROL .txt]* (para texto ASCII compatível com Unicode), *[!UICONTROL .csv]* (para valores separados por vírgula) ou *[!UICONTROL .zip]* (para formato ZIP compactado, que é descompactado em um arquivo TSV).<br><br><b>Dica:</b> Para bulksheets que incluem caracteres internacionais, use o formato TSV ou TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | As entidades e seus status correspondentes a serem incluídos na planilha, com uma linha de dados por entrada. Por exemplo, se você incluir campanhas ativas, a bulksheet incluirá uma linha por campanha ativa. Somente as entidades selecionadas com os status selecionados são incluídas. Os padrões são pré-selecionados com base na rede de anúncios especificada. Por padrão, somente as instâncias ativas das entidades selecionadas são incluídas. Para obter uma lista de linhas de bulksheet disponíveis, consulte &quot;[Linhas de bulksheet por rede de anúncios](#bulksheet-rows-by-ad-network).&quot;<br><br>Para adicionar ou remover entidades, marque ou desmarque as caixas de seleção ao lado das entidades, respectivamente. Para adicionar ou remover os status de uma entidade, clique em ao lado do menu de status e marque ou desmarque as caixas de seleção ao lado das entidades, respectivamente. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtra o escopo de entidades filhas para aquelas com os status de entidade pai especificados, usando uma operação AND. Por exemplo, se você selecionar &quot;Campanha ativa&quot;, &quot;Grupo de anúncios ativo&quot; e &quot;Palavra-chave ativa&quot;, a planilha eletrônica incluirá somente palavras-chave ativas em grupos de anúncios ativos em campanhas ativas.<br><br>Se você não selecionar essa opção, o status principal não será considerado, e o filtro usará uma operação OR. Por exemplo, se você selecionar &quot;Campanha ativa&quot;, &quot;AdGroup ativo&quot; e &quot;Palavra-chave ativa&quot;, a bulksheet incluirá todas as campanhas ativas, todos os grupos de anúncios ativos, independentemente do status da campanha principal, e todas as palavras-chave ativas, independentemente do status da campanha principal e do grupo de anúncios. |
| | [!UICONTROL Bulksheet Columns] | As colunas a serem incluídas no arquivo de bulksheet baixado:&lt;ul><li><li>*[!UICONTROL AMO ID]*: (obrigatório se &quot;[!UICONTROL SE ID]&quot; não está selecionado) Inclui um [!DNL Adobe]identificador exclusivo gerado pelo para cada entidade/linha. Search, Social, &amp; Commerce usa o valor para determinar a identidade correta para editar, mas não o publica na rede de anúncios. Posteriormente, você poderá editar os dados da entidade usando o [!UICONTROL AMO ID] como o identificador, em vez da ID da entidade e das IDs da entidade pai.</li><li>*[!UICONTROL SE ID]*: (obrigatório se &quot;[!UICONTROL AMO ID]&quot; não está selecionado) Inclui o identificador exclusivo da rede de publicidade para cada coluna incluída e suas entidades pai. Posteriormente, se você editar dados de qualquer entidade usando o [!UICONTROL SE ID] como identificador, você também deve incluir linhas para as entidades pai (incluindo suas [!UICONTROL SE ID] valores).</li><li>*[!UICONTROL Platform]*: inclui um [!UICONTROL Platform column] no início de cada linha para indicar a plataforma de publicidade (como &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (obrigatório se &quot;[!UICONTROL AMO ID]&quot; não está selecionado) Inclui o nome da conta da rede de publicidade para cada entidade/linha.</li><li>\[Colunas a serem incluídas\]: Para incluir todas, nenhuma ou somente colunas selecionadas relevantes para cada entidade selecionada na [!UICONTROL Bulksheet Rows] seção. Para ver as colunas individuais relevantes para uma entidade, clique em ![Ponta de seta para a direita](/help/search-social-commerce/assets/compressed-item.png "Ponta de seta para a direita") ao lado do nome da entidade. Por padrão, todas as colunas relevantes são incluídas para cada linha de entidade selecionada. Desmarque a caixa de seleção ao lado de qualquer entidade ou ao lado de qualquer coluna individual para excluí-la da bulksheet.</li></ul><br><br><b>Dica:</b> Certifique-se de incluir colunas adequadas para identificar o item em cada linha do arquivo de bulksheet. Por exemplo, digamos que você inclua linhas de palavra-chave de acordo com [!UICONTROL Bulksheet Rows] mas você exclui todas as colunas relacionadas a palavras-chave. A bulksheet resultante inclui uma linha para cada ocorrência de palavra-chave. No entanto, como nenhuma coluna relacionada a palavras-chave é incluída, nem mesmo a ID AMO ou SE ID, você não pode identificar qual instância de palavra-chave pertence a uma linha específica e não pode usar a bulksheet para atualizar dados, a menos que adicione manualmente a coluna e os valores de ID apropriados. |
| [!UICONTROL Filters] | | Critérios para campanhas específicas, grupos de anúncios, anúncios/criações, palavras-chave e/ou posicionamentos para incluir na bulksheet:<ol><li>Selecione um parâmetro (nome ou ID da entidade; ou qualquer elemento de uma criação, palavra-chave ou disposição), selecione um operador e insira o valor aplicável.<br><br>Por exemplo, para retornar apenas anúncios com &quot;sapatos&quot; no título de um [!DNL Google Ads] conta, selecione *[!UICONTROL Headline]*, selecione *[!UICONTROL contains]* e insira `shoes` no campo de entrada.</li><li>(Para aplicar filtros adicionais) Para cada filtro adicional, clique em **[!UICONTROL +Add Filter]**, selecione **[!UICONTROL AND]** ou **[!UICONTROL OR]**, selecione um elemento de anúncio ou palavra-chave e um operador e insira o valor aplicável.</li></ul> |

## Linhas de bulksheet por rede de anúncios {#bulksheet-rows-by-ad-network}

| Linha de Bulksheet | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Notas |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | — |
| [!UICONTROL Adgroup] | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | — |
| [!UICONTROL Creative] *ou* [!UICONTROL Creative (except RSA)] | Sim | Sim | Sim | — | — | Sim | Sim | Sim | Sim | ([!DNL Google  Ads]) Usar para todos os tipos de anúncios, exceto para anúncios de pesquisa responsivos, que estão disponíveis na [!UICONTROL Responsive Search Ad] linha. |
| [!UICONTROL Responsive Search Ad] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sim | Sim | Sim | Sim | Sim | — | Sim | Sim | Sim | Use somente para palavras-chave não negativas. Para ver palavras-chave negativas criadas no nível da campanha ou do grupo de anúncios, use o [!UICONTROL Campaign Negative Keyword] ou [!UICONTROL Adgroup Negative Keyword] linha quando disponível. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Sim | — | — | — | — | — |
| [!UICONTROL Placement] | — | Sim | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sim | Sim | — | — | — | — | — | — | Use para direcionamentos de pesquisa dinâmica para um grupo de publicidade. |
| [!UICONTROL Shopping Product Group] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sim | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sim | Sim | Sim | — | — | — | Sim | Sim | — | Use somente para palavras-chave negativas criadas no nível da campanha ou do grupo de anúncios. Para ver palavras-chave não negativas, use o [!UICONTROL Keyword] linha quando disponível. |
| [!UICONTROL Campaign Negative Website] | — | Sim | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Adgroup Site Link] | — | Sim | — | — | — | — | — | Sim | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Sim | — |
| [!UICONTROL Adgroup Negative Keyword] | Sim | Sim | Sim | — | — | — | Sim | Sim | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Sim | Sim | Sim | — | — | — | Sim | Sim | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Campaign Device Target] | — | Sim | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Adgroup Device Target] | — | Sim | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Sim | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Sim | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Lançar bulksheets ou arquivos de erro corrigidos](bulksheet-post.md)
>* [Validar páginas de aterrissagem em arquivos de bulksheet](bulksheet-validate-landing-pages.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)
