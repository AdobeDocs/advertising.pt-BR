---
title: Sobre a automatização do gerenciamento de anúncios usando feeds de inventário
description: Saiba mais sobre o gerenciamento avançado de campanhas, que permite gerenciar automaticamente a estrutura da conta e fornecer anúncios dinâmicos com base em dados sobre o inventário de produtos ou serviços.
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Sobre a automatização do gerenciamento de anúncios usando feeds de inventário

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

A variável [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] o view for advanced campaign management permite criar e atualizar automaticamente a estrutura de conta da rede de publicidade e fornecer anúncios dinâmicos com base em dados sobre o inventário de produtos ou serviços. Você pode fazer upload de novos arquivos com os dados do produto diariamente ou sempre que desejar, ou vincular diretamente a um [!DNL Google] ou [!DNL Microsoft®] conta da central de comércio. Use o recurso para:

* Crie novas campanhas a partir de fontes de dados solicitadas.

* Atualizar dinamicamente o texto e os anúncios de pesquisa responsivos, [!DNL Google Ads] anúncios de compras ou [!DNL Microsoft® Advertising] anúncios de compras sempre que novos dados forem processados, usando variáveis dinâmicas para elementos de dados alteráveis (como preço ou quantidade). Cada vez que os dados são alterados, os anúncios existentes são excluídos e novos são criados.

* Pausar ou remover automaticamente grupos de anúncios, palavras-chave e anúncios quando o estoque cair abaixo de um nível específico, de acordo com uma data final especificada, ou quando um componente existente for omitido dos dados de feed.

Para configurar seus anúncios, crie modelos de feed de inventário contendo variáveis (espaços reservados) e substitua as variáveis por colunas de dados reais de um arquivo carregado ou uma [Conta do centro de comércio da Google ou Microsoft® que é sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). As variáveis também podem incluir grupos de modificadores configurados em um arquivo ou linhas individuais no arquivo para criar vários anúncios, palavras-chave, campanhas ou grupos de anúncios para cada linha aplicável no arquivo de dados. Por exemplo, se você usar uma variável do grupo de modificadores em um título de anúncio e o grupo de modificadores incluir dois modificadores (&quot;para barato&quot; e &quot;com desconto&quot;), dois anúncios separados serão criados para cada produto — um para cada modificador. Para [!DNL Google Ads] e [!DNL Microsoft® Advertising] anúncios de pesquisa dinâmica, você também pode incluir valores para personalizadores de anúncios.

| [!UICONTROL Ad Variation] Seção do modelo | Modificadores no Search, Social e Commerce | Conteúdos do feed | Anúncios resultantes |
|----|----|----|----|
| Título: comprar high-end \{<i>Categoria do produto</i>\} &lt;<i>ListaBarata</i>>.<br><br>Descrição 1: Grande inventário de \{<i>Nome do produto</i>\}.<br><br>Descrição 2: disponível em \{<i>Porcentagem de desconto</i>\}% de desconto. | Valores para o grupo de modificadores &quot;CheapList&quot;:<br><br>&quot;para barato&quot;<br><br>&quot;com desconto&quot; | Categoria do Produto,Nome do Produto,Porcentagem de Desconto<br>eletrônica,iPods,10<br><br>vestuário,Camisas,15<br><br><b>Nota:</b> É possível separar valores com vírgulas ou guias. | <u>Compre eletrônicos de alta qualidade a preços baixos.</u><br>Enorme inventário de tablets. Disponível com desconto de 10%.<br><br><u>Compre eletrônicos de alta qualidade com desconto.</u><br>Enorme inventário de tablets. Disponível com desconto de 10%.<br><br><u>Compre roupas de última geração por mais barato.</u><br>Enorme inventário de camisas. Disponível com 15% de desconto.<br><br><u>Compre roupas sofisticadas com desconto.</u><br>Enorme inventário de camisas. Disponível com 15% de desconto. |

Depois de gerar os anúncios, você pode, opcionalmente, revisá-los e, em seguida, publicá-los na rede de anúncios.

>[!NOTE]
>Para criar ou editar dados da campanha em massa usando arquivos de planilha, consulte &quot;[Sobre o gerenciamento de dados de campanha usando bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

## Fluxo de trabalho para gerenciar dados da campanha usando feeds de inventário

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
>* [Quando os componentes da conta são criados ou excluídos pelos feeds de inventário?](when-are-components-created-deleted.md)
