---
title: Implementar [!DNL Naver] contas somente de rastreamento
description: Saiba como configurar campanhas de rastreamento para o seu [!DNL Naver] contas para que possa rastrear, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios.
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementar [!DNL Naver] contas somente de rastreamento

*[!DNL Naver]somente contas*

Você pode criar campanhas de rastreamento para seu [!DNL Naver] contas para que possa rastrear, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios. Search, Social e Commerce não sincronizam dados com a rede de anúncios, fazem upload do rastreamento automaticamente ou lançam ofertas para a conta.

As campanhas de rastreamento replicam suas campanhas, grupos de anúncios e palavras-chave existentes. Depois de criar a estrutura de conta em Pesquisa, Social e Comércio e adicionar o rastreamento às campanhas originais na rede de anúncios, você pode fazer upload das métricas diárias de tráfego da rede para suas palavras-chave ou anúncios. Search, Social e Commerce podem atribuir suas conversões a seus anúncios e palavras-chave.

Você pode rastrear métricas de desempenho em todas as suas campanhas e para qualquer campanha individual, grupo de publicidade ou palavra-chave/anúncio. Você também pode incluir informações sobre eles nos relatórios mais básicos, avançados e de assistência, juntamente com dados de outras redes de anúncios. O suporte para exportar as métricas para o Adobe Analytics não está disponível, mas Search, Social e Commerce podem sincronizar [métricas que você está rastreando [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) em Pesquisa, Social e Comércio.

>[!NOTE]
>
>Não é possível adicionar campanhas de rastreamento a um portfólio para otimização.

1. Crie campanhas de rastreamento em Pesquisa, Social e Comércio:

   1. Criar [detalhes da conta de rede fictícia](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Se você tiver várias contas em uma única rede de anúncios, consolide-as em uma conta no [!UICONTROL Accounts] exibição.

      [!DNL Naver] O não oferece suporte à API para carregar parâmetros de rastreamento na rede de anúncios. No entanto, você pode gerar parâmetros de rastreamento usando bulksheets e adicioná-los manualmente na rede de anúncios (por Etapa 2). Para gerar os parâmetros de rastreamento, você deve usar o &quot;[!UICONTROL EF Redirect]&quot;método de rastreamento. Opcionalmente, você pode adicionar os parâmetros de acréscimo desejados.

      Search, Social e Commerce incluem automaticamente o parâmetro `ev_cl={ef_uniqueid}` em qualquer URL de rastreamento gerado em bulksheets para a conta. Esse identificador exclusivo é usado para corresponder os dados da campanha com os dados de qualquer custo e clique que você fizer upload.

   1. Configurar campanhas para rastrear:

      1. Na rede de anúncios, crie um arquivo de bulksheet contendo todas as entidades, e suas entidades principais necessárias, que você deseja que o Search, Social e Commerce rastreie para a conta.

         É possível incluir dados sobre palavras-chave, incluindo as campanhas principais e grupos de anúncios.

      1. Edite o arquivo de bulksheet, se necessário, para que ele siga as etapas Pesquisa, Social e Comércio [formato de bulksheet obrigatório para [!DNL Naver] contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. Em Pesquisa, Social e Comércio, [fazer upload do arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Observação: o Search, Social e Commerce não publica os dados na conta da rede de publicidade.

1. Configurar o rastreamento para as campanhas:

   1. Em Pesquisa, Social e Comércio, [baixar um novo arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) usando a opção para &quot;[!UICONTROL Generate Tracking URLs].&quot;
   Usar o &quot;[!UICONTROL Generate Tracking URLs]A opção &quot; preenche o [!UICONTROL Destination URL] para cada palavra-chave com o código de rastreamento de Pesquisa, Social e Comércio prefixado à variável [!UICONTROL Base URL] valor.

   Veja a seguir um exemplo do URL de destino com rastreamento:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copie o [!UICONTROL Destination URL] no arquivo de bulksheet baixado para as configurações de palavra-chave relevantes na rede.

      Você pode adicionar os URLs às entidades relevantes fazendo upload do arquivo para a rede no editor da rede de anúncios. Nesse caso, talvez seja necessário remover algumas colunas, de acordo com os requisitos de dados da rede. Caso contrário, você deve inserir os URLs manualmente na rede.


1. Baixe periodicamente dados de cliques e custos agregados diariamente da rede de anúncios para as palavras-chave ou anúncios de marca no nível do grupo de anúncios que você está rastreando e, em seguida, [fazer upload dos dados de clique e custo](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) para Pesquisar, Social e Comércio na [formato obrigatório](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Inclua a hierarquia de conta completa e qualquer métrica que desejar incluir. Search, Social e Commerce faz a correspondência dos dados carregados com os dados em campanhas existentes.

1. (Opcional) Se você usar as tags de serviço de rastreamento de conversão do Adobe Advertising em suas páginas da Web para rastrear conversões que não são rastreadas na rede de anúncios, envie arquivos de feed que contêm dados de conversão agregados diariamente para adicionar às campanhas de rastreamento.

   Para obter mais informações, entre em contato com a equipe de conta da Adobe.

Todos os dados de rastreamento carregados estão disponíveis no [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] no prazo de [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], e [!UICONTROL Keywords] exibições. Também está disponível para relatórios no [!UICONTROL Insights & Reports] exibição.

>[!MORELIKETHIS]
>
>* [Apêndice - Dados de bulksheet necessários para [!DNL Naver] contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Fazer upload de métricas de tráfego e conversão para o [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Requisitos de dados métricos para [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formatos de rastreamento de cliques para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

