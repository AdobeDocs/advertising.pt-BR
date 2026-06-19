---
title: (Nova interface) Sobre o gerenciamento de dados de campanha usando bulksheets
description: Saiba mais sobre a funcionalidade de bulksheet disponível por rede de anúncios, o fluxo de trabalho de bulksheet e a manipulação de erros na nova interface do usuário do Search, Social e Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 772
ht-degree: 0%

---

# (Nova interface) Sobre o gerenciamento de dados de campanha usando bulksheets

Uma bulksheet é um arquivo que contém dados de campanha em um formato específico e pode ser usado para criar ou modificar rapidamente dados de estrutura de campanha e grupos de anúncios e anúncios de texto. Você pode gerar (baixar) bulksheets com dados para uma ou mais contas, para campanhas e grupos de anúncios específicos ou até mesmo para anúncios de texto, inserções e grupos de produtos específicos. Você pode usar bulksheets para gerenciar grandes conjuntos de dados ou fazer pequenas alterações. Cada rede de publicidade exige diferentes colunas de informações.

Você pode gerar bulksheets com a quantidade de dados que desejar — ou, como opção, criá-los manualmente e carregá-los. Consulte &quot;[Dados obrigatórios e incluídos em bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)&quot; para obter os requisitos de formato de arquivo e &quot;[Operações que você pode executar em bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)&quot; para obter as operações com suporte da rede de anúncios.

Depois de criar um bulksheet, você poderá identificar qualquer página de aterrissagem quebrada que precise ser corrigida ou dados adicionais para adicionar ou editar. É possível editar o arquivo e carregá-lo no Search, Social e Commerce, programando, opcionalmente, que ele seja publicado na rede de publicidade relevante imediatamente ou posteriormente. Também é possível publicar um bulksheet disponível imediatamente ou posteriormente.

Todos os bulksheets, arquivos de erro de validação da página de aterrissagem e outros arquivos de erro são excluídos automaticamente 30 dias após sua criação, a menos que você os exclua anteriormente.

## Funcionalidade por rede de anúncios {#bulksheet-functionality-by-network}

* **Baixar, carregar e postar:** contas [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yandex]

* **Baixar e carregar apenas:** contas [!DNL Naver]

  Você pode carregar dados do [!DNL Naver] para usar no Search, Social e Commerce, mas não pode publicá-los na rede de publicidade. Você também pode baixar os dados existentes (não sincronizados).

* **Baixar somente dados:** contas [!DNL Pinterest], [!DNL Yahoo DSP], [!DNL Yahoo Native]

  Você pode baixar os dados existentes (não sincronizados).

## Visão geral do uso de bulksheets

As etapas padrão para usar bulksheets com contas sincronizadas são as seguintes:

1. [Baixe dados de uma ou mais contas, campanhas ou grupos de anúncios em um arquivo de bulksheet](download.md). Como opção, você pode preencher manualmente um bulksheet específico da rede de anúncios e fazer upload do arquivo.

1. [Validar as páginas de aterrissagem](validate-landing-pages.md) nas URLs base (finais) ou de destino no arquivo.

1. Quando for necessário adicionar dados ou fazer correções:

   1. Exporte o arquivo para sua área de trabalho e edite-o em [!DNL Microsoft Excel].

   1. [Carregue manualmente o arquivo editado](upload.md) para o Search, Social e Commerce.

1. (Para arquivos carregados manualmente) [Poste o arquivo](post.md) na rede de publicidade ao carregá-lo ou posteriormente.

1. (Se necessário) Baixe quaisquer novos arquivos de erro, corrija as linhas e publique novamente o arquivo.

## Gerenciamento de erros no upload e lançamento de dados de campanha

O Search, Social, &amp; Commerce carrega e publica quantas linhas de dados forem possíveis de uma bulksheet de campanha, incluindo os URLs de rastreamento gerados, quando necessário.

Quando ocorrem erros durante uma operação de bulksheet, um dos dois tipos de arquivos de erro a seguir é gerado:

* **[!UICONTROL EF Errors]:** Quando um arquivo ou linhas individuais no arquivo não podem ser carregadas ou processadas, um arquivo de erro chamado `<uploaded file name>_ef_errors.<extension used for the bulksheet>` é criado. Se o problema estiver com linhas individuais, essas linhas serão incluídas, com uma explicação de cada erro para que ele possa ser corrigido.

* **[!UICONTROL SE Errors]:** Quando um arquivo é postado, mas a rede de publicidade não aceita alguns ou todos os dados, um arquivo de erro chamado `<uploaded file name>_se_errors.<extension used for the bulksheet>` é criado. Quando algumas linhas, mas não todas, são aceitas, o arquivo de erro mostra as linhas que não foram publicadas e uma explicação de cada erro para que ele possa ser corrigido. As mensagens de erro são mostradas nas três últimas colunas de cada linha.

>[!NOTE]
>
>Se você postar qualquer anúncio de [!DNL Google Ads] que viole as políticas de publicidade da rede de publicidade, mas possa ser qualificado para isenções, esses anúncios serão automaticamente repostados com solicitações de isenção. Se a solicitação de isenção falhar, as informações sobre a violação serão incluídas no arquivo de erro.

Você pode baixar qualquer tipo de arquivo de erro, fazer correções diretamente nas linhas e, em seguida, fazer upload novamente e publicar o arquivo.

Os arquivos de erro são automaticamente excluídos após 30 dias, a menos que você os exclua anteriormente.

## Informações sobre cada arquivo

Todos os arquivos de dados baixados, arquivos carregados e arquivos de erro estão disponíveis em [!UICONTROL Setup] \> [!UICONTROL Bulksheets].

As informações para cada arquivo incluem o status da tarefa atual e a porcentagem da tarefa que está concluída, a data em que foi criada, (quando aplicável) a data em que foi ou será postada na rede de publicidade especificada, a data de exclusão programada e o nome de logon do usuário que iniciou a tarefa.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Baixar/Criar um arquivo de bulksheet](download.md)
>* [(Nova interface do usuário) Carregar um bulksheet ou arquivo de erro corrigido](upload.md)
>* [(Nova interface do usuário) Postar bulksheets ou arquivos de erro corrigidos](post.md)
>* [(Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet](validate-landing-pages.md)
>* [(Nova interface do usuário) Excluir bulksheets e arquivos de erro carregados](delete.md)
>* [(Nova interface do usuário) Parar um trabalho de bulksheet em andamento](stop-job.md)
