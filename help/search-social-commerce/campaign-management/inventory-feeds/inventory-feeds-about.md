---
title: Sobre a automatização do gerenciamento de anúncios usando feeds de inventário
description: Saiba mais sobre o gerenciamento avançado de campanhas, que permite gerenciar automaticamente a estrutura da conta e fornecer anúncios dinâmicos com base em dados sobre o inventário de produtos ou serviços.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Sobre a automatização do gerenciamento de anúncios usando feeds de inventário

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

A visualização [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] para gerenciamento avançado de campanha permite que você crie e atualize automaticamente a estrutura da conta de rede de anúncios e forneça anúncios dinâmicos com base em dados sobre o inventário de seus produtos ou serviços. Você pode carregar novos arquivos com dados de produtos diariamente ou sempre que desejar, ou vincular diretamente a uma conta de [!DNL Google] ou [!DNL Microsoft] da central de comércio. Use o recurso para:

* Crie novas campanhas a partir de fontes de dados solicitadas.

* Atualize dinamicamente o texto e os anúncios de pesquisa responsivos, [!DNL Google Ads] anúncios de compras ou [!DNL Microsoft Advertising] anúncios de compras sempre que novos dados forem processados, usando variáveis dinâmicas para elementos de dados alteráveis (como preço ou quantidade). Cada vez que os dados são alterados, os anúncios existentes são excluídos e novos são criados.

* Pausar ou remover automaticamente grupos de anúncios, palavras-chave e anúncios quando o estoque cair abaixo de um nível específico, de acordo com uma data final especificada, ou quando um componente existente for omitido dos dados de feed.

Para configurar seus anúncios, crie modelos de feed de estoque contendo variáveis (espaços reservados) e substitua as variáveis por colunas de dados reais de um arquivo carregado ou de uma [conta da central de comerciante do Google ou do Microsoft que esteja sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). As variáveis também podem incluir grupos de modificadores configurados em um arquivo ou linhas individuais no arquivo para criar vários anúncios, palavras-chave, campanhas ou grupos de anúncios para cada linha aplicável no arquivo de dados. Por exemplo, se você usar uma variável do grupo de modificadores em um título de anúncio e o grupo de modificadores incluir dois modificadores (&quot;para barato&quot; e &quot;com desconto&quot;), dois anúncios separados serão criados para cada produto — um para cada modificador. Para os anúncios de pesquisa dinâmica do [!DNL Google Ads] e do [!DNL Microsoft Advertising], você também pode incluir valores para os personalizadores de anúncios.

| Seção do modelo [!UICONTROL Ad Variation] | Modificadores no Search, Social e Commerce | Conteúdos do feed | Anúncios resultantes |
|----|----|----|----|
| Título: Compre produtos avançados \{<i>Categoria do produto</i>\} &lt;<i>CheapList</i>>.<br><br>Descrição 1: enorme inventário de \{<i>Nome do produto</i>\}.<br><br>Descrição 2: Disponível em \{<i>Porcentagem de desconto</i>\}% de desconto. | Valores para o grupo de modificadores &quot;CheapList&quot;:<br><br>&quot;para barato&quot;<br><br>&quot;com desconto&quot; | Categoria do produto,Nome do produto,Porcentagem de desconto<br>eletrônicos,iPods,10<br><br>vestuário,Camisas,15<br><br><b>Observação:</b> é possível separar valores com vírgulas ou guias. | <u>Compre eletrônicos sofisticados por um preço baixo.</u><br>Enorme inventário de tablets. Disponível com desconto de 10%.<br><br><u>Compre eletrônicos sofisticados com desconto.</u><br>Enorme inventário de tablets. Disponível com desconto de 10%.<br><br><u>Compre roupas de alta qualidade a preços acessíveis.</u><br>Enorme inventário de camisas. Disponível com 15% de desconto.<br><br><u>Compre roupas sofisticadas com desconto.</u><br>Enorme inventário de camisas. Disponível com 15% de desconto. |

Depois de gerar os anúncios, você pode, opcionalmente, revisá-los e, em seguida, publicá-los na rede de anúncios.

>[!NOTE]
>Para criar ou editar dados de campanha em massa usando arquivos de planilha, consulte &quot;[Sobre o gerenciamento de dados de campanha usando bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

## Fluxo de trabalho para gerenciar dados da campanha usando feeds de inventário

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Inicialmente, teste pelo menos um arquivo de feed ou conta e, em seguida, você pode automatizar totalmente o processo ou continuar a controlá-lo em cada etapa:

1. (Opcional) Entre em contato com a equipe de conta do Adobe para configurar um diretório FTP para depósito de arquivos de dados.

   Se você usar o diretório FTP, o serviço de feed verificará se há novos arquivos a cada duas horas.

   Caso contrário, você pode carregar arquivos manualmente na exibição [!UICONTROL Advanced (ACM)].

1. Definir [parâmetros para processar dados de feed](feed-settings-manage.md#feed-data-settings).

   Se estiver usando o FTP, inicialmente não publique dados nas redes de anúncios automaticamente. Depois de verificar a saída do primeiro arquivo e ficar satisfeito com os resultados, é possível alterar as configurações.

1. Carregue um arquivo de dados para o diretório FTP, [carregue manualmente um arquivo de dados](feed-files-manage.md) no [!UICONTROL Advanced (ACM) view] ou [habilite o acesso a uma conta da central de comerciante do Google ou do Microsoft](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Para carregar arquivos manualmente, você pode aguardar até criar um modelo que use o arquivo de dados.

1. (Opcional) Crie grupos de [modificadores](modifiers-manage.md) para usar como variáveis em vários campos de dados em modelos de dados de feed.

1. [Crie um ou mais modelos](ad-templates/ad-template-manage.md) que usam as colunas de dados para criar campanhas, grupos de anúncios, palavras-chave e/ou cópias de anúncios para uma conta de rede de anúncios específica.

1. [Propagar dados de feed por meio dos modelos](feed-data-propagate.md), que substitui os nomes de coluna no modelo por dados no arquivo ou na conta. Dependendo das opções do modelo, o Search, Social e Commerce cria uma nova estrutura de conta (campanhas, grupos de anúncios, palavras-chave) para os anúncios usando as configurações padrão ou mapeia os anúncios para a estrutura de conta existente.

1. (Opcional) [Visualize a saída](propagated-data-view.md) nas exibições [!UICONTROL Advanced (ACM)] e, opcionalmente, exiba um resumo das alterações de dados na guia [!UICONTROL Propagations].

1. [Postar os dados](propagated-data-post.md) nas contas de rede de anúncios relevantes.

1. (Se você usar o FTP ou uma conta do centro de comércio para carregar seus dados; opcional) Depois de validar a saída do primeiro arquivo de feed, [edite os parâmetros](feed-settings-manage.md#feed-data-settings) para propagar automaticamente os dados subsequentes por meio dos modelos associados e publicá-los nas redes de anúncios relevantes.

1. (Quando você tiver novos arquivos de dados) Conforme necessário, faça upload de novos arquivos, propague os dados por meio de modelos e publique os dados na rede de anúncios relevante. Opcionalmente, é possível propagar e publicar os dados em uma etapa.

>[!MORELIKETHIS]
>
>* [Quando os componentes da conta são criados ou excluídos pelos feeds de inventário?](when-are-components-created-deleted.md)
