---
title: (Nova interface do usuário) Baixar/criar um arquivo de bulksheet
description: Saiba como criar arquivos de bulksheet baixando dados de conta para suas redes de anúncios na nova interface do Search, Social e Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f916f47a40729ff39ac1456e3b3ad93e1045e9a9
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# (Nova interface do usuário) Baixar/criar um arquivo de bulksheet

Você pode criar bulksheets usando configurações personalizadas para uma ou mais contas em uma ou mais [redes de anúncios com suporte](about.md#bulksheet-functionality-by-network). Os bulksheets incluem dados no Search, Social e Commerce.

Para campanhas sincronizadas, você pode, opcionalmente, sincronizar com a rede de anúncios antes de baixar os dados para garantir que as alterações de dados recentes no lado da rede de anúncios sejam incluídas. Para todas as redes de anúncios, é possível gerar novos URLs de rastreamento de cliques para incluir no arquivo.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Na barra de ferramentas, clique em **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Especifique as [configurações de bulksheet](#bulksheet-settings):

   1. Na guia **[!UICONTROL Selections]**, selecione as contas, campanhas ou grupos de anúncios para incluir e configurar as opções de bulksheet.

   1. (Opcional) Clique na guia **[!UICONTROL Rows and Columns]**, especifique os componentes da conta e os status dos componentes que deseja incluir linhas na planilha e especifique as colunas a serem incluídas para cada componente selecionado.

      Para obter uma lista de linhas de bulksheet disponíveis, consulte &quot;[Linhas de bulksheet por rede de anúncios](#bulksheet-rows-by-ad-network).&quot;

   1. (Opcional) Clique na guia **[!UICONTROL Filters]** e especifique os critérios para as campanhas específicas, grupos de anúncios, anúncios/criações, palavras-chave, disposições e outras entidades a serem incluídas na bulksheet.

1. Clique em **[!UICONTROL Download]**.

Quando a tarefa for iniciada, a janela exibirá uma notificação, mas permanecerá aberta para que você possa continuar criando bulksheets adicionais, se necessário. Quando o arquivo é criado, você recebe uma notificação por email com um link para o arquivo; dependendo da quantidade de dados que está sendo compilada, a notificação pode levar vários minutos ou mais. Se a geração do arquivo falhar, um arquivo de erro será listado na exibição Bulksheets e você receberá uma notificação por email com um link para o arquivo de erro.

## Configurações de bulksheet {#bulksheet-settings}

### Guia Seleções {#bulksheet-selections-settings}

**\[Seleção de conta, campanha e grupo de anúncios\]**

Expanda a rede e a hierarquia de conta e marque a caixa de seleção ao lado de cada conta, campanha ou grupo de anúncios cujos dados serão incluídos na bulksheet:

* Para incluir todos os grupos de campanhas e anúncios de uma conta, marque a caixa de seleção ao lado do nome da conta.

* Para incluir campanhas específicas, expanda a conta e marque a caixa de seleção ao lado de cada campanha a ser incluída. Para incluir grupos de anúncios específicos, expanda ainda mais uma campanha e marque a caixa de seleção ao lado de cada grupo de anúncios.

>[!NOTE]
>
>* Uma única planilha pode ser aplicada a várias contas em várias redes de anúncios. As colunas específicas da rede de anúncios são rotuladas em bulksheets com o nome da rede de anúncios (como &quot;Operadoras de celular (Google Ads)&quot;).
>* Para ver o tipo de componente que um item é, mantenha o cursor sobre ele.
>* Por padrão, somente as contas ativas e ativadas e seus componentes ativos são listados.

**[!UICONTROL Generate Tracking URLs]:** (Opcional) Inclui modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento, ou URLs de destino com códigos de rastreamento inseridos em contas com URLs de destino, para palavras-chave, anúncios, posicionamentos, sitelinks e grupos de produtos [!DNL Google Ads] na planilha em massa. Por padrão, essa opção está selecionada.

Quando essa opção é selecionada, as URLs são geradas de acordo com os parâmetros na seção [!UICONTROL Campaign Tracking] das configurações da conta ou das configurações da campanha. Por padrão, se os URLs de rastreamento já existirem, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto do anúncio ou os parâmetros de rastreamento da conta tenham sido alterados).

>[!NOTE]
>
>* Se o anunciante usar o rastreamento de conversão do Adobe Advertising e a conta relevante não estiver configurada para gerar e carregar automaticamente URLs de rastreamento, você deverá gerar novos URLs de rastreamento quando os URLs de base tiverem sido alterados.
>* Se você não selecionar essa opção, ainda poderá gerar URLs de rastreamento posteriormente ao fazer upload ou publicar o arquivo.

**[!UICONTROL Perform pre-sync]:** (Opcional) Instrui o Search, Social e Commerce a sincronizar seus arquivos com as campanhas especificadas para garantir que todos os dados sejam iguais. Por padrão, essa opção não está selecionada.

>[!NOTE]
>
>O Search, Social e Commerce sincroniza automaticamente com a rede de anúncios uma vez por dia, sempre que detecta uma nova campanha na rede de anúncios e sempre que você altera os dados da campanha no Search, Social e Commerce. Selecione essa opção se você achar que alterações recentes nos dados da campanha ou da conta foram feitas diretamente na rede de anúncios ou usando o editor de desktop da rede de anúncios. A criação de bulksheet demora mais ao selecionar essa opção.

**[!UICONTROL Bulksheet Name]:** O nome da nova bulksheet e o tipo de arquivo. Por padrão, o arquivo é criado no formato de valores separados por tabulação e é nomeado como uma das seguintes opções:

* (Para todas as contas de uma rede de anúncios) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Para uma única conta) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Para várias contas) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

Você pode renomear o arquivo. O nome não pode incluir os seguintes caracteres: `# % & * | \ : " < > . ? /`

Opcionalmente, altere o tipo de arquivo. As opções incluem *[!UICONTROL .tsv]* (para valores separados por tabulação), *[!UICONTROL .txt (unicode)]* (para texto ASCII compatível com Unicode), *[!UICONTROL .csv]* (para valores separados por vírgula) ou *[!UICONTROL .zip]* (para formato ZIP compactado, que é descompactado em um arquivo TSV).

>[!TIP]
>
>Para bulksheets que incluem caracteres internacionais, use o formato TSV ou TXT.

### Guia Linhas e Colunas {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** As entidades e seus status correspondentes a serem incluídos como linhas de dados na planilha em massa, com uma linha por entrada. Por exemplo, se você incluir campanhas ativas, a bulksheet incluirá uma linha por campanha ativa. Somente as entidades selecionadas com os status selecionados são incluídas. Os padrões são pré-selecionados com base na rede de anúncios especificada. Por padrão, somente as instâncias ativas das entidades selecionadas são incluídas.

Para adicionar ou remover entidades, marque ou desmarque as caixas de seleção ao lado das entidades. Para adicionar ou remover os status de uma entidade, clique no menu de status ao lado da entidade e marque ou desmarque as caixas de seleção dos status aplicáveis.

Para obter uma lista de linhas disponíveis por rede de anúncios, consulte &quot;[Linhas de bulksheet por rede de anúncios](#bulksheet-rows-by-ad-network).&quot;

**[!UICONTROL Cascading Status Hierarchy]:** Filtra entidades filho para aquelas com os status de entidade pai especificados, usando uma operação AND. Por exemplo, se você selecionar &quot;Campanha ativa&quot;, &quot;Grupo de anúncios ativo&quot; e &quot;Palavra-chave ativa&quot;, a planilha eletrônica incluirá somente palavras-chave ativas em grupos de anúncios ativos em campanhas ativas.

Se você não selecionar essa opção, o status principal não será considerado, e o filtro usará uma operação OR. Por exemplo, se você selecionar &quot;Campanha ativa&quot;, &quot;AdGroup ativo&quot; e &quot;Palavra-chave ativa&quot;, a bulksheet incluirá todas as campanhas ativas, todos os grupos de anúncios ativos, independentemente do status da campanha pai, e todas as palavras-chave ativas, independentemente do status da campanha pai e do grupo de anúncios.

**[!UICONTROL Bulksheet Columns]:** As colunas a serem incluídas no arquivo de bulksheet baixado:

* *[!UICONTROL AMO ID]:* (Obrigatório se &quot;[!UICONTROL SE ID]&quot; não estiver selecionado) Inclui um identificador exclusivo gerado por [!DNL Adobe] para cada entidade/linha. Search, Social, &amp; Commerce usa o valor para determinar a identidade correta para editar, mas não o publica na rede de anúncios. Posteriormente, você poderá editar dados para a entidade usando o [!UICONTROL AMO ID] como identificador, em vez da ID da entidade e das IDs da entidade pai.

* *[!UICONTROL SE ID]:* (Obrigatório se &quot;[!UICONTROL AMO ID]&quot; não estiver selecionado) Inclui o identificador exclusivo da rede de publicidade para cada coluna incluída e suas entidades pai. Posteriormente, se você editar dados para qualquer entidade que use [!UICONTROL SE ID] como identificador, também deverá incluir linhas para as entidades pai (incluindo seus valores [!UICONTROL SE ID]).

* *[!UICONTROL Platform]:* Inclui uma coluna [!UICONTROL Platform] no início de cada linha para indicar a plataforma de anúncio (como &quot;Baidu&quot;).

* *[!UICONTROL Acct Name]:* (Obrigatório se &quot;[!UICONTROL AMO ID]&quot; não estiver selecionado) Inclui o nome da conta da rede de publicidade para cada entidade/linha.

* \[Colunas específicas da entidade\]: Para incluir todas, nenhuma ou somente colunas selecionadas relevantes para cada entidade selecionada em [!UICONTROL Bulksheet Rows], clique em ![Ponta de seta para a direita](/help/search-social-commerce/assets/compressed-item.png "ao lado do nome da entidade para expandi-la e marque ou desmarque as caixas de seleção de colunas individuais. ")Por padrão, todas as colunas relevantes são incluídas para cada linha de entidade selecionada.

>[!TIP]
>
>Certifique-se de incluir colunas adequadas para identificar o item em cada linha do arquivo de bulksheet. Por exemplo, se você incluir linhas de palavra-chave pelo seletor [!UICONTROL Bulksheet Rows], mas excluir todas as colunas relacionadas a palavras-chave, a bulksheet resultante incluirá uma linha para cada instância de palavra-chave sem como identificar qual instância de palavra-chave pertence a uma linha específica. Nesse caso, você não pode usar o bulksheet para atualizar dados, a menos que adicione manualmente a coluna e os valores de ID apropriados.

### Guia Filtros {#bulksheet-filters-settings}

Critérios para campanhas específicas, grupos de anúncios, anúncios/criações, palavras-chave e/ou posicionamentos para incluir na bulksheet:

1. Selecione um parâmetro (nome ou ID da entidade; ou qualquer elemento de uma criação, palavra-chave ou disposição), selecione um operador e insira o valor aplicável.

   Por exemplo, para retornar apenas anúncios com &quot;sapatos&quot; no título de uma conta [!DNL Google Ads], selecione *[!UICONTROL Headline]*, selecione *[!UICONTROL contains]* e digite `shoes` no campo de entrada.

1. (Para aplicar filtros adicionais) Para cada filtro adicional, clique em **[!UICONTROL +Add Filter]**, selecione **[!UICONTROL AND]** ou **[!UICONTROL OR]**, selecione um elemento de anúncio ou palavra-chave e um operador e insira o valor aplicável.

## Linhas de bulksheet por rede de anúncios {#bulksheet-rows-by-ad-network}

| Linha de Bulksheet | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | [!DNL Yandex] | Notas |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | — |
| [!UICONTROL Adgroup] | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | Sim | — |
| [!UICONTROL Creative] *ou* [!UICONTROL Creative (except RSA)] | Sim | Sim | Sim | — | — | Sim | Sim | Sim | Sim | ([!DNL Google Ads]) Use para todos os tipos de anúncios, exceto anúncios de pesquisa responsivos, que estão disponíveis na linha [!UICONTROL Responsive Search Ad]. |
| [!UICONTROL Responsive Search Ad] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sim | Sim | Sim | Sim | Sim | — | Sim | Sim | Sim | Use somente para palavras-chave não negativas. Para ver palavras-chave negativas criadas no nível da campanha ou do grupo de anúncios, use a linha [!UICONTROL Campaign Negative Keyword] ou [!UICONTROL Adgroup Negative Keyword], quando disponível. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Sim | — | — | — | — | — |
| [!UICONTROL Placement] | — | Sim | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sim | Sim | — | — | — | — | — | — | Use para direcionamentos de pesquisa dinâmica para um grupo de publicidade. |
| [!UICONTROL Shopping Product Group] | — | Sim | Sim | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sim | Sim | — | — | — | — | Sim | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sim | Sim | Sim | — | — | — | Sim | Sim | — | Use somente para palavras-chave negativas criadas no nível da campanha ou do grupo de anúncios. Para ver palavras-chave não negativas, use a linha [!UICONTROL Keyword] quando disponível. |
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

Para obter detalhes sobre as colunas obrigatórias e opcionais para cada rede de anúncios, consulte os artigos de formato de dados do bulksheet específico da rede de anúncios:

* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Baidu]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Google Ads]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Microsoft Advertising]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Naver]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Yahoo! Display Network]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Yahoo! Japan Ads]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Dados de bulksheet obrigatórios e opcionais para  [!DNL Yandex]  contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Sobre o gerenciamento de dados de campanha usando bulksheets](about.md)
>* [(Nova interface do usuário) Carregar um bulksheet ou arquivo de erro corrigido](upload.md)
>* [(Nova interface do usuário) Postar bulksheets ou arquivos de erro corrigidos](post.md)
>* [(Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet](validate-landing-pages.md)
