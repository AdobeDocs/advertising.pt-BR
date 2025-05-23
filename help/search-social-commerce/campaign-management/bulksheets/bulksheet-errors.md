---
title: Erros de bulksheet
description: Faça referência aos possíveis motivos para cada erro de bulksheet.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Erros de bulksheet

O Search, Social e Commerce gera dois tipos de arquivos de erro durante operações de bulksheet:

* **Erros SE:** Quando um arquivo é postado, mas a rede de publicidade não aceita todos os dados, um arquivo de erro chamado `<uploaded file name>_se_errors.<extension used for the bulksheet>` é criado. Quando algumas linhas, mas não todas, são aceitas, o arquivo de erro mostra as linhas que não foram publicadas e uma explicação de cada erro para que você possa corrigi-lo. Os erros estão incluídos na coluna &quot;[!UICONTROL SE Error Message]&quot;.

>[!NOTE]
>
>Se você postar qualquer anúncio [!DNL Google Ads] que viole as políticas de publicidade da rede de publicidade, mas possa ser qualificado para isenções, esses anúncios serão automaticamente repostados com solicitações de isenção. Se a solicitação de isenção falhar, as informações sobre a violação serão incluídas no arquivo de erro.

* **Erros EF:** Quando a operação de bulksheet não pode carregar ou processar um arquivo ou linhas individuais no arquivo, ela cria um arquivo de erro chamado `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Se o problema estiver com linhas individuais, essas linhas serão incluídas,
com uma explicação de cada erro para que você possa corrigi-lo. Os erros estão incluídos na coluna &quot;[!UICONTROL EF Error Message]&quot;.

## [!UICONTROL SE Error] mensagens

Os erros na coluna [!UICONTROL SE Error] vêm diretamente da rede de anúncios.

## [!UICONTROL EF Error] mensagens

Os seguintes erros podem ser incluídos na coluna [!UICONTROL EF Error] em [!UICONTROL EF Errors] arquivos.

### Baixar/Criar erros

| Categoria | Mensagem | Descrição |
|----|----|----|
| Geral | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | A operação falhou completamente devido a um erro sem categoria ou sem tratamento. Se o problema persistir, entre em contato com a equipe da conta do Adobe para investigar a causa. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | O Search, Social e Commerce não pôde sincronizar com a rede de anúncios antes de criar o bulksheet, portanto, nenhum bulksheet foi criado. Se o problema persistir, entre em contato com a equipe de conta da Adobe. |

### Erros de upload

| Categoria | Mensagem | Descrição |
|----|----|----|
| Geral | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | A operação falhou completamente. Se o problema persistir, entre em contato com a equipe de conta da Adobe. |
| Todas as entidades | [!UICONTROL Invalid Fields.] \[campos inválidos e erro\] | Os dados especificados estão ausentes ou são inválidos. |
|  | [!UICONTROL Invalid Reference Given] | A ID da entidade na rede de publicidade ou a ID de uma entidade principal (como a ID da conta) não corresponde a uma entidade no Search, Social e Commerce. Isso pode ocorrer ao editar a ID na bulksheet. |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | A entidade expirou ou foi excluída, e você não pode alterar suas propriedades. A entidade pode ser excluída quando alguém editou manualmente o status. |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | (Novas entidades) Uma nova entidade só pode ser &quot;Ativa&quot; ou &quot;Pausada&quot;. |
|  | [!UICONTROL Duplicate Entries are present] | Várias linhas são incluídas para a mesma entidade, com atributos diferentes em cada linha. Consolidar as alterações em uma linha. |
|  | [!UICONTROL Invalid AMO ID given] | A ID do AMO da linha não existe. Isso pode ocorrer se você editou a ID na bulksheet. |
|  | [!UICONTROL Invalid row given] | A linha não inclui informações suficientes para determinar o tipo de entidade. Edite a linha para incluir todos os campos obrigatórios para o tipo de entidade. |
| Contas | [!UICONTROL Provide Valid Account Details] | (Bulksheets para várias contas) Os identificadores de conta não são incluídos em todas as linhas. Insira valores para qualquer uma das seguintes combinações de colunas para cada linha: a) &quot;[!UICONTROL AMO ID]&quot; ou b) &quot;[!UICONTROL Account Name]&quot; e &quot;[!UICONTROL Platform]&quot;. |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | O Search, Social e Commerce não tem acesso à conta de rede de anúncios, portanto, não é possível criar ou editar dados de campanha. Verifique se as credenciais da conta de pesquisa estão corretas e se a conta está habilitada. |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | (Campanhas de compras) O valor no campo &quot;[!UICONTROL Sales Country]&quot; é inválido. Veja uma lista de países válidos [para [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) e [para [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Todos os componentes da campanha | [!UICONTROL Campaign creation failed] | A campanha pai não foi criada, portanto, esta entidade não foi criada. Verifique se todas as entidades principais contêm todos os campos obrigatórios. |
| Grupo de publicidade | [!UICONTROL Campaign Row missing] | A campanha pai especificada não existe, portanto, o grupo de publicidade não foi criado. Crie a campanha pai em uma nova linha. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Um grupo de anúncios pode conter palavras-chave ou disposições, mas não ambas. Crie grupos de anúncios separados para palavras-chave e disposições. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) O grupo de anúncios não foi criado porque não inclui pelo menos uma palavra-chave. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) O grupo de anúncios não foi criado porque não inclui pelo menos um anúncio. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) O grupo de anúncios não foi criado porque não inclui pelo menos um anúncio. |
| Todos os componentes do grupo de anúncios | [!UICONTROL Adgroup creation failed] | O grupo pai de anúncios não foi criado, portanto, essa entidade não pôde ser criada. Isso pode ocorrer devido a um erro nos campos do grupo de publicidade ou porque a campanha principal falhou. Verifique se todas as entidades principais contêm todos os campos obrigatórios. |
|  | [!UICONTROL Adgroup Row Missing] | O grupo de anúncios pai especificado não existe, portanto, a entidade não pôde ser criada. Crie o grupo pai de anúncios em uma nova linha. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | O campo &quot;[!UICONTROL Tracking Template]&quot; é somente para contas que usam URLs finais/avançadas. Remova o valor até ter migrado a conta para usar URLs finais/avançados. |
| Anúncio | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | (Tipos de anúncio diferentes de texto, texto expandido, produto, instalação de aplicativo e pesquisa dinâmica) Você pode editar somente o status e o URL desse tipo de anúncio. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Cada grupo de anúncios pode incluir até 50 anúncios, e essa planilha abrangente inclui mais de 50. Reduza o número de anúncios. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | O anúncio está em uma entidade pai expirada ou excluída, portanto, não é possível editá-lo. |
| Palavra-chave | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | A campanha ou o grupo de publicidade principal foi excluído ou expirou, portanto, você não pode alterar a entidade. |
| Posicionamento | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | A campanha ou o grupo de publicidade principal foi excluído ou expirou, portanto, você não pode alterar a entidade. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Anúncios do Google) Você pode oferecer somente disposições em campanhas do somente na rede de pesquisa ou somente na rede de conteúdo, mas não em campanhas do direcionadas às redes de pesquisa e conteúdo. |
| Grupo de produtos de compras | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Cada nível do grupo de produtos deve incluir um grupo &quot;[!UICONTROL Everything Else]&quot;. Não é possível excluir manualmente um grupo &quot;[!UICONTROL Everything Else]&quot;; ele é excluído automaticamente quando você exclui todos os outros grupos de produtos no mesmo nível. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | A campanha ou o grupo de publicidade principal foi excluído ou expirou, portanto, você não pode alterar a entidade. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | (Somente [!DNL Yandex]) A mensagem é imprecisa; cada campanha pode incluir até quatro (não dez) sitelinks, e esta bulksheet inclui mais de quatro. Remova alguns sitelinks. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | A campanha pai expirou ou foi excluída, portanto, não é possível editar o sitelink. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Não foi possível criar o sitelink porque o anúncio não foi criado. |
| Destino da localização | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | A campanha ou o grupo de publicidade principal foi excluído ou expirou, portanto, não é possível editar os destinos de localização. |
| Exclusões | [!UICONTROL Other than status is modified] | Você pode editar somente o status de uma exclusão (&quot;[!UICONTROL Active]&quot; ou &quot;[!UICONTROL Deleted]&quot;). |
| Públicos-alvo/públicos-alvo da lista de remarketing do Google | [!UICONTROL Invalid Audience given] | (Somente campanhas do [!DNL Google Ads]) O destino RLSA não corresponde a um RLSA (público-alvo) existente. Corrija os valores nas colunas &quot;[!UICONTROL Audience]&quot; e &quot;[!UICONTROL RLSA Target]&quot;. |

### Publicar erros

Os seguintes erros ocorrem somente em [!UICONTROL EF Errors] arquivos. A maioria dos erros de publicação vem da rede de publicidade e é incluída em um arquivo de erros SE.

| Categoria | Mensagem | Descrição |
|----|----|----|
| Geral | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | A operação falhou completamente. Se o problema persistir, entre em contato com a equipe de conta da Adobe. |
| Todas as entidades | [!UICONTROL Entity] foi postado na rede de publicidade | A entidade foi postada na rede de publicidade, mas não foi sincronizada com o Search, Social e Commerce ao mesmo tempo, portanto, os dados da entidade não estão imediatamente disponíveis no Search, Social e Commerce. O processo de sincronização é acionado automaticamente agora.<br><br>Quando grandes quantidades de dados são sincronizadas, eles podem não estar disponíveis em Search, Social e Commerce por várias horas ou mais. |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | Não foi possível criar a entidade pai, portanto, essa entidade filho não foi criada. |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Baixar/Criar um arquivo de bulksheet](bulksheet-download.md)
>* [Validar páginas de aterrissagem em arquivos de bulksheet](bulksheet-validate-landing-pages.md)
>* [Carregar um arquivo de bulksheet ou arquivo de erro corrigido](bulksheet-upload.md)
>* [Postar bulksheets ou arquivos de erro corrigidos](bulksheet-post.md)
