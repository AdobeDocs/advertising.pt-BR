---
title: Dados de bulksheet necessários para [!DNL Naver] contas
description: Fazer referência aos campos de cabeçalho e campos de dados necessários em bulksheets para [!DNL Naver] contas.
exl-id: bd6e3dab-47b0-428a-825d-bd9c21494fb0
feature: Search Bulksheets
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# Apêndice - Dados de bulksheet necessários para [!DNL Naver] contas

Preencha seu [!DNL Naver] contas na Pesquisa, no Social e no Comércio, gerando um arquivo de bulksheet no [!DNL Naver], e depois carregá-lo em Search, Social e &amp; Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Campos de dados disponíveis

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Campo | Campaign | Grupo de publicidade | Palavra-chave | Descrição |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/d | n/d | n/d | (Incluído nos bulksheets gerados para fins de informação) A plataforma de anúncios. Obrigatório, a menos que cada linha inclua uma ID AMO para a entidade. |
| [!UICONTROL Acct Name] | Obrigatório/Opcional | Obrigatório/Opcional | Obrigatório/Opcional | O nome exclusivo que identifica uma conta de rede de anúncios. Obrigatório, a menos que cada linha inclua uma ID AMO para a entidade. |
| [!UICONTROL Campaign Name] | Obrigatório | Obrigatório | Obrigatório | O nome exclusivo que identifica uma campanha para uma conta. |
| [!UICONTROL Ad Group Name] | n/d | Obrigatório | Obrigatório | O nome exclusivo que identifica um grupo de anúncios. |
| [!UICONTROL Keyword] | n/d | n/d | Obrigatório | A sequência de palavras-chave. |
| [!UICONTROL Base URL] | n/d | n/d | Opcional | O URL da página de aterrissagem para o qual os usuários finais são levados quando clicam em seu anúncio, incluindo quaisquer parâmetros de acréscimo configurados para a campanha ou conta.<br><br>URLs base/final no nível de palavra-chave substituem URLs no nível de anúncio e superior. |
| [!UICONTROL Destination URL] | n/d | n/d | n/d | (Incluído em bulksheets gerados para fins de informação; não publicado na rede de publicidade) Para contas com URLs de destino, esse valor é o URL que vincula um anúncio a um URL/página inicial base no site do anunciante (às vezes, por meio de outro site que rastreia o clique e redireciona o usuário para a página inicial). Inclui quaisquer parâmetros de acréscimo configurados para a campanha ou conta do Search, Social e &amp; Commerce. Se você gerou URLs de rastreamento, esse valor se baseia nos parâmetros de rastreamento nas configurações da conta e nas configurações da campanha. Se você anexou parâmetros específicos de rede de publicidade, eles podem ser substituídos pelos parâmetros equivalentes de Pesquisa, Social e Comércio.<br><br>Para contas com URLs finais, essa coluna mostra o mesmo valor que a variável [!UICONTROL Base URL/Final URL column]. |
| \[Classificação de rótulo específica do anunciante\] | Opcional | Opcional | Opcional | (Nomeado para uma classificação de rótulo específica do anunciante, como &quot;Cor&quot; para uma classificação de rótulo chamada Cor) Um valor para a classificação especificada associada à entidade. Você pode incluir apenas um valor por classificação por entidade (como &quot;vermelho&quot; para a classificação de rótulo &quot;Cor&quot; para a Campanha A). O comprimento máximo é de 100 caracteres e o valor pode incluir caracteres ASCII e não ASCII.<br><br>As classificações de rótulo e seus valores de rótulo são aplicados a todos os componentes filhos; novos componentes adicionados posteriormente são associados automaticamente ao rótulo. As classificações de etiquetas para grupos de produtos são aplicadas ao nível de unidade (mais granular).<br><br>O nome da classificação e o valor da classificação não fazem distinção entre maiúsculas e minúsculas. |
| [!UICONTROL Constraints] | Opcional | Opcional | Opcional | Uma restrição atribuída à entidade. Você pode atribuir somente uma restrição por entidade.<br><br>As restrições são herdadas por entidades filhas, portanto, não é necessário inserir valores para entidades filhas, a menos que você queira substituir os valores herdados. |
| [!UICONTROL Campaign Status] | Opcional: criar ou editar<br>Obrigatório: Excluir | n/d | n/d | O status de exibição da campanha: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i> (somente campanhas existentes). O padrão para novas campanhas é <i>[!UICONTROL Active]</i>. Para excluir uma campanha ativa ou pausada, insira o valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | n/d | Opcional: criar ou editar<br>Obrigatório: Excluir | n/d | O status de exibição do grupo de anúncios: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i> (somente grupos de anúncios existentes). O padrão para novos grupos de anúncios é <i>[!UICONTROL Active]</i>. Para excluir um grupo de anúncios ativo ou pausado, digite o valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | n/d | n/d | Opcional: criar ou editar<br>Obrigatório: Excluir | O status de exibição da palavra-chave: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i> (somente palavras-chave existentes). O padrão para novas palavras-chave é <i>[!UICONTROL Active]</i>. Para excluir uma palavra-chave ativa ou pausada, digite o valor &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | n/d: Criar<br>Obrigatório/Opcional: Editar ou excluir | Opcional | Opcional | A ID exclusiva que identifica uma campanha existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Obrigatório somente quando você altera o nome da campanha, a menos que a linha inclua uma ID do AMO para a campanha. |
| [!UICONTROL Ad Group ID] | n/d | n/d: Criar<br>Obrigatório/Opcional: Editar ou excluir | Opcional | O identificador exclusivo que identifica um grupo de anúncios existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Obrigatório somente quando você altera o nome do grupo de anúncios, a menos que a linha inclua uma ID AMO para o grupo de anúncios. |
| [!UICONTROL Keyword ID] | n/d | n/d | n/d: Criar<br>Obrigatório/Opcional: Editar<br>Obrigatório: Excluir | A ID exclusiva que identifica uma palavra-chave existente. Em arquivos CSV e TSV, ele deve ser precedido por uma aspa simples (&#39;).[^1] Obrigatório somente quando você altera o nome da palavra-chave, a menos que a linha inclua a) colunas de propriedade suficientes para identificar a palavra-chave ou b) uma ID AMO. |
| [!UICONTROL AMO ID] | n/d: Criar<br>Opcional: Editar ou excluir | n/d: Criar<br>Opcional: Editar ou excluir | n/d: Criar<br>Opcional: Editar ou excluir | (Em bulksheets gerados) Uma [!DNL Adobe]Identificador exclusivo gerado pelo para uma entidade sincronizada. Para anúncios de pesquisa responsivos, a ID do AMO é necessária para editar ou excluir anúncios, a menos que você inclua a variável [!UICONTROL Ad ID]. Para editar dados para todos os outros tipos de entidade com uma ID AMO, a ID AMO é necessária para editar ou excluir os dados, a menos que você inclua a ID da entidade e a ID da entidade pai.<br><br>Search, Social, &amp; Commerce usa o valor para determinar a identidade correta para editar, mas não publica a ID na rede de anúncios. |
| [!UICONTROL EF Error Message] | n/d | n/d | n/d | (Incluído em bulksheets gerados para fins de informação) Espaço reservado para exibir mensagens de erro do Search, Social e &amp; Commerce referentes aos dados na linha; as mensagens de erro estão incluídas em [!UICONTROL EF Errors] arquivos. Este valor não é postado na rede de publicidade. |
| [!UICONTROL SE Error Message] | n/d | n/d | n/d | (Incluído em bulksheets gerados para fins de informação) Espaço reservado para exibir mensagens de erro da rede de publicidade relacionadas aos dados na linha; as mensagens de erro estão incluídas em [!UICONTROL SE Errors] arquivos. Este valor não é postado na rede de publicidade. |

[^1]: o Excel converte números grandes em notação científica (como 2.12E+09 para 2115585666) quando abre o arquivo. Para exibir dígitos na notação padrão, selecione qualquer célula na coluna e clique dentro da barra de fórmulas.

>[!MORELIKETHIS]
>
>* [Apêndice - Erros de bulksheet](../bulksheet-errors.md)
>* [Operações que você pode executar em bulksheets](bulksheet-operations.md)
>* [Formatos de arquivo de bulksheet compatíveis](bulksheet-file-formats.md)
>* [Baixar/criar um arquivo de bulksheet](../bulksheet-download.md)
>* [Formatos de rastreamento de cliques para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Fazer upload de um arquivo de bulksheet ou arquivo de erro corrigido](../bulksheet-upload.md)
>* [Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
