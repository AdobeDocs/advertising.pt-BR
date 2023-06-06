---
title: Sobre a automatização do gerenciamento de anúncios usando feeds de inventário
description: Saiba mais sobre o fluxo de trabalho para gerenciar automaticamente a estrutura da conta e fornecer anúncios dinâmicos com base em dados sobre o inventário de produtos ou serviços.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Fluxo de trabalho para gerenciar dados da campanha usando feeds de inventário

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Inicialmente, teste pelo menos um arquivo de feed ou conta e, em seguida, você pode automatizar totalmente o processo ou continuar a controlá-lo em cada etapa:

1. (Opcional) Entre em contato com a equipe de conta do Adobe para configurar um diretório FTP para depósito de arquivos de dados.

   Se você usar o diretório FTP, o serviço de feed verificará se há novos arquivos a cada duas horas.

   Caso contrário, você poderá fazer upload dos arquivos manualmente no [!UICONTROL Advanced (ACM)] exibição.

1. Definir [parâmetros para processamento de dados de feed](feed-settings-manage.md#feed-data-settings).

   Se estiver usando o FTP, inicialmente não publique dados nas redes de anúncios automaticamente. Depois de verificar a saída do primeiro arquivo e ficar satisfeito com os resultados, é possível alterar as configurações.

1. Fazer upload de um arquivo de dados para o diretório FTP, [fazer upload manual de um arquivo de dados](feed-files-manage.md) no [!UICONTROL Advanced (ACM) view]ou [habilitar o acesso a uma conta de centro de comerciante da Google ou Microsoft®](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Para carregar arquivos manualmente, você pode aguardar até criar um modelo que use o arquivo de dados.

1. (Opcional) Crie grupos de [modificadores](modifiers-manage.md) para usar como variáveis em vários campos de dados em modelos de dados de feed.

1. [Criar um ou mais modelos](ad-templates/ad-template-manage.md) que usam as colunas de dados para criar campanhas, grupos de anúncios, palavras-chave e/ou cópias de anúncios para uma conta de rede de anúncios específica.

1. [Propagar dados do feed por meio dos modelos](feed-data-propagate.md), que substitui os nomes das colunas no modelo pelos dados no arquivo ou na conta. Dependendo das opções do modelo, Search, Social, &amp; Commerce cria uma nova estrutura de conta (campanhas, grupos de anúncios, palavras-chave) para os anúncios usando as configurações padrão ou mapeia os anúncios para a estrutura de conta existente.

1. (Opcional) [Visualizar a saída](propagated-data-view.md) no [!UICONTROL Advanced (ACM)] exibições e, opcionalmente, exibir um resumo das alterações de dados na [!UICONTROL Propagations] guia.

1. [Publicar os dados](propagated-data-post.md) às contas de rede de publicidade relevantes.

1. (Se você usar o FTP ou uma conta da central do comerciante para carregar seus dados; opcional) Depois de validar a saída do primeiro arquivo de feed, [editar os parâmetros](feed-settings-manage.md#feed-data-settings) para propagar automaticamente dados subsequentes por meio dos modelos associados e publicá-los nas redes de anúncios relevantes.

1. (Quando você tiver novos arquivos de dados) Conforme necessário, faça upload de novos arquivos, propague os dados por meio de modelos e publique os dados na rede de anúncios relevante. Opcionalmente, é possível propagar e publicar os dados em uma etapa.

>[!MORELIKETHIS]
>
>* [Sobre a automatização do gerenciamento de anúncios usando feeds de inventário](inventory-feeds-about.md)
>* [Quando os componentes da conta são criados ou excluídos pelos feeds de inventário?](when-are-components-created-deleted.md)

