---
title: Sobre o gerenciamento de dados de campanha usando bulksheets
description: Saiba mais sobre a funcionalidade de bulksheet disponível pela rede de anúncios, o fluxo de trabalho de bulksheet e a manipulação de erros.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Sobre o gerenciamento de dados de campanha usando bulksheets

Uma bulksheet é um arquivo que contém dados de campanha em um formato específico e pode ser usado para criar ou modificar rapidamente dados de estrutura de campanha e grupos de anúncios e anúncios de texto. Você pode gerar (baixar) bulksheets com dados para uma ou mais contas, para campanhas e grupos de anúncios específicos ou até mesmo para anúncios de texto, inserções e grupos de produtos específicos. Você pode usar bulksheets para gerenciar grandes conjuntos de dados ou fazer pequenas alterações. Cada rede de publicidade exige diferentes colunas de informações.

Você pode gerar bulksheets com a quantidade de dados que desejar — ou, como opção, criá-los manualmente e carregá-los (consulte o capítulo em &quot;Dados obrigatórios/incluídos em Bulksheets&quot;).

Depois de criar um bulksheet, você poderá identificar qualquer página de aterrissagem quebrada que precise ser corrigida ou dados adicionais para adicionar ou editar. É possível editar o arquivo e carregá-lo no Search, Social e &amp; Commerce, programando, opcionalmente, que ele seja publicado na rede de publicidade relevante imediatamente ou posteriormente. Também é possível publicar um bulksheet disponível imediatamente ou posteriormente.

Opcionalmente, é possível fazer upload de arquivos de bulksheet para uma conta FTP especificada para recuperação e contabilização automática. O diretório é examinado a cada hora e novos arquivos são publicados na rede de pesquisa na ordem em que são recebidos.

Todos os bulksheets, arquivos de erro de validação da página de aterrissagem e outros arquivos de erro são excluídos automaticamente 30 dias após sua criação, a menos que você os exclua anteriormente.

## Funcionalidade por rede de anúncios

* **Baixar, carregar e publicar:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], e [!DNL Yandex] contas

* **Somente download e upload:** [!DNL Naver] contas

   Você pode fazer upload [!DNL Naver] dados para uso no Search, Social e Commerce, mas não podem publicá-los na rede de anúncios. Você também pode baixar os dados existentes (não sincronizados).

* **Baixar somente dados:**  [!DNL Pinterest], [!DNL Yahoo Native], e [!DNL Yahoo! Display Network] contas

   Você pode baixar os dados existentes (não sincronizados).

## Visão geral do uso de bulksheets

As etapas padrão do uso de bulksheets para contas sincronizadas são as seguintes:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Baixar dados de uma ou mais contas, campanhas ou grupos de anúncios em um arquivo de bulksheet](bulksheet-download.md). Como opção, você pode preencher manualmente um bulksheet específico da rede de anúncios e fazer upload do arquivo.

1. [Validar as páginas de destino](bulksheet-validate-landing-pages.md) nos URLs base (finais) ou nos URLs de destino no arquivo.

1. Quando for necessário adicionar dados ou fazer correções:

   1. [Exportar o arquivo](bulksheet-export.md) na sua área de trabalho e edite-a no [!DNL Microsoft® Excel].

   1. [Carregar manualmente o arquivo editado](bulksheet-upload.md) para Pesquisar, Social e Comércio ou [fazer upload do arquivo para uma conta FTP especificada](bulksheet-ftp-account.md) para lançamento automático.

1. (Para arquivos carregados manualmente) [Publicar o arquivo](bulksheet-post.md) à rede de publicidade ao carregá-la ou posteriormente.

1. (Se necessário) Baixe quaisquer novos arquivos de erro, corrija as linhas e publique novamente o arquivo.

## Gerenciamento de erros no upload e lançamento de dados de campanha

O Search, Social, &amp; Commerce carrega e publica quantas linhas de dados forem possíveis de uma planilha de campanha em massa, incluindo os URLs de rastreamento gerados, quando necessário.

Quando ocorrem erros durante a operação de bulksheet, um dos dois seguintes tipos de arquivos de erro é gerado:

* **[!UICONTROL EF Errors]:**  Quando um arquivo ou linhas individuais no arquivo não podem ser carregadas ou processadas, um arquivo de erro chamado `<uploaded file name>_ef_errors.<extension used for the bulksheet>` é criado. Se o problema estiver com linhas individuais, essas linhas serão incluídas, com uma explicação de cada erro para que ele possa ser corrigido.

* **[!UICONTROL SE Errors]:**  Quando um arquivo é postado, mas a rede de publicidade não aceita alguns ou todos os dados, um arquivo de erro chamado `<uploaded file name>_se_errors.<extension used for the bulksheet>` é criado. Quando algumas linhas, mas não todas, são aceitas, o arquivo de erro mostra as linhas que não foram publicadas e uma explicação de cada erro para que ele possa ser corrigido. As mensagens de erro são mostradas nas três últimas colunas de cada linha.

>[!NOTE]
>
>Se você postar algum [!DNL Google Ads] anúncios que violam as políticas de publicidade da rede de publicidade, mas podem ser qualificados para isenções, esses anúncios são automaticamente republicados com solicitações de isenção. Se a solicitação de isenção falhar, as informações sobre a violação serão incluídas no arquivo de erro.

Você pode baixar qualquer tipo de arquivo de erro, fazer correções diretamente nas linhas e, em seguida, fazer upload novamente e publicar o arquivo.

Os arquivos de erro são automaticamente excluídos após 30 dias, a menos que você os exclua anteriormente.

## Informações sobre cada arquivo

Todos os arquivos de dados baixados, arquivos carregados e arquivos de erro estão disponíveis no [!UICONTROL Search] > [!UICONTROL Bulksheets].

As informações para cada arquivo incluem o status da tarefa atual e a porcentagem da tarefa que está concluída, a data em que foi criada, (quando aplicável) a data em que foi ou será postada na rede de publicidade especificada, a data de exclusão programada e o nome de logon do usuário que iniciou a tarefa.

>[!MORELIKETHIS]
>
>* [Baixar/criar um arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Fazer upload de uma bulksheet ou arquivo de erro corrigido](bulksheet-upload.md)
>* [Lançar bulksheets ou arquivos de erro corrigidos](bulksheet-post.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)

