---
title: Implementar [!DNL Naver] contas somente de rastreamento
description: Saiba como configurar campanhas de rastreamento para suas contas do  [!DNL Naver] , de modo que você possa acompanhar, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implementar contas somente de rastreamento do [!DNL Naver]

*[!DNL Naver]somente contas*

Você pode criar campanhas de rastreamento para suas contas do [!DNL Naver] de modo que possa acompanhar, relatar e visualizar o desempenho dos anúncios comprados diretamente da rede de anúncios. O Search, Social e Commerce não sincroniza dados com a rede de publicidade, carrega o rastreamento automaticamente ou faz ofertas para a conta.

As campanhas de rastreamento replicam suas campanhas, grupos de anúncios e palavras-chave existentes. Depois de criar a estrutura de conta em Search, Social e Commerce e adicionar o rastreamento às campanhas originais na rede de anúncios, você pode fazer upload das métricas diárias de tráfego na rede para suas palavras-chave ou anúncios. Search, Social e Commerce podem atribuir suas conversões a seus anúncios e palavras-chave.

Você pode rastrear métricas de desempenho em todas as suas campanhas e para qualquer campanha individual, grupo de publicidade ou palavra-chave/anúncio. Você também pode incluir informações sobre eles nos relatórios mais básicos, avançados e de assistência, juntamente com dados de outras redes de anúncios. O suporte para exportar as métricas para o Adobe Analytics não está disponível, mas o Search, Social e Commerce pode sincronizar [métricas que você está rastreando [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) com o Search, Social e Commerce.

>[!NOTE]
>
>Não é possível adicionar campanhas de rastreamento a um portfólio para otimização.

1. Crie campanhas de rastreamento em Search, Social e Commerce:

   1. Criar [detalhes de conta de rede fictícios](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Se você tiver várias contas em uma única rede de anúncios, consolide-as em uma conta na exibição [!UICONTROL Accounts].

      [!DNL Naver] não fornece suporte de API para carregar parâmetros de rastreamento para a rede de publicidade. No entanto, você pode gerar parâmetros de rastreamento usando bulksheets e adicioná-los manualmente na rede de anúncios (por Etapa 2). Para gerar os parâmetros de rastreamento, você deve usar o método de rastreamento &quot;[!UICONTROL EF Redirect]&quot;. Opcionalmente, você pode adicionar os parâmetros de acréscimo desejados.

      O Search, Social e Commerce inclui automaticamente o parâmetro `ev_cl={ef_uniqueid}` em todas as URLs de rastreamento geradas nos bulksheets da conta. Esse identificador exclusivo é usado para corresponder os dados da campanha com os dados de qualquer custo e clique que você fizer upload.

   1. Configurar campanhas para rastrear:

      1. Na rede de anúncios, crie um arquivo de bulksheet contendo todas as entidades, e suas entidades principais necessárias, que você deseja que o Search, Social e Commerce rastreie para a conta.

         É possível incluir dados sobre palavras-chave, incluindo as campanhas principais e grupos de anúncios.

      1. Edite o arquivo de bulksheet, se necessário, para que ele siga o formato de bulksheet [de Pesquisa, Social e Commerce necessário para [!DNL Naver] contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. Em Pesquisar, Social e Commerce, [carregue o arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Observação: o Search, Social e Commerce não publica os dados na conta de rede de anúncios.

1. Configurar o rastreamento para as campanhas:

   1. Em Pesquisar, Social e Commerce, [baixe um novo arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) usando a opção para &quot;[!UICONTROL Generate Tracking URLs].&quot;

   O uso da opção &quot;[!UICONTROL Generate Tracking URLs]&quot; preenche o campo [!UICONTROL Destination URL] para cada palavra-chave com o código de rastreamento Search, Social e Commerce prefixado ao valor [!UICONTROL Base URL].

   Veja a seguir um exemplo do URL de destino com rastreamento:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copie os valores [!UICONTROL Destination URL] no arquivo de bulksheet baixado para as configurações de palavra-chave relevantes na rede.

      Você pode adicionar os URLs às entidades relevantes fazendo upload do arquivo para a rede no editor da rede de anúncios. Nesse caso, talvez seja necessário remover algumas colunas, de acordo com os requisitos de dados da rede. Caso contrário, você deve inserir os URLs manualmente na rede.

1. Baixe periodicamente dados de cliques e custos agregados diariamente da rede de anúncios para as palavras-chave ou anúncios de marca no nível do grupo de anúncios que você está rastreando e, em seguida, [carregue os dados de cliques e custos](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) para Search, Social e Commerce no [formato necessário](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Inclua a hierarquia de conta completa e qualquer métrica que desejar incluir. Search, Social e Commerce corresponde os dados carregados aos dados em campanhas existentes.

1. (Opcional) Se você usar as tags de serviço de rastreamento de conversão de Adobe Advertising nas páginas da Web para rastrear conversões que não são rastreadas na rede de anúncios, envie arquivos de feed que contêm dados de conversão agregados diariamente para adicionar às campanhas de rastreamento.

   Para obter mais informações, entre em contato com a equipe de conta da Adobe.

Todos os dados de rastreamento carregados estão disponíveis em [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] nos modos de exibição [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Keywords]. Ele também está disponível para relatórios na visualização [!UICONTROL Insights & Reports].

>[!MORELIKETHIS]
>
>* [Apêndice - Dados de bulksheet necessários para [!DNL Naver] contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Carregar métricas de tráfego e conversão para [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Requisitos de dados de métrica para [!DNL Naver] contas somente rastreamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formatos de rastreamento de cliques para [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
