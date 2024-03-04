---
title: Publicar dados de campanha gerados a partir de feeds para redes de anúncios
description: Saiba como publicar dados gerados a partir de feeds de dados de inventário em redes de anúncios.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Publicar dados de campanha gerados a partir de feeds para redes de anúncios

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Você pode publicar dados de campanha gerados a partir de um feed à medida que propaga os dados por meio dos modelos associados ou como um processo separado. Depois de publicar os dados, todos os dados propagados existentes serão removidos da [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] listas.

Para uma publicação bem-sucedida, todos os grupos de anúncios devem ser atribuídos a campanhas, todas as palavras-chave e anúncios devem ser atribuídos a grupos de anúncios e todas as informações necessárias devem ser incluídas sem violações de duração.

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview],&quot; depois [publicar o arquivo de bulksheet gerado](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (nomeado como &quot;`<feed file name>_<template name>`&quot;) no [!UICONTROL Bulksheets] exibição.

  Se você não tiver [validar suas páginas de aterrissagem](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), você poderá fazer isso antes de publicar o arquivo.

* Se você usou a opção para &quot;[!UICONTROL Propagate only]&quot;, será possível publicar os dados gerados para os componentes com a [[!UICONTROL New] status](propagated-data-status.md) em uma exibição de hierarquia de campanha no [!UICONTROL Templates] guia.

  >[!NOTE]
  >
  >Os componentes ativos ou excluídos podem incluir subcomponentes novos, e os subcomponentes podem ser publicados se os dados forem válidos.

  >[!TIP]
  >
  >Se você não validou suas páginas de aterrissagem anteriormente e deseja fazer isso, [propagar dados e visualizá-los](feed-data-propagate.md) do [!UICONTROL Bulksheets] exibir em vez de postá-lo na rede de publicidade. Você pode então [validar os URLs](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) antes de publicar manualmente o arquivo na rede de publicidade.

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abre para o [!UICONTROL Templates] guia.

   1. Marque a caixa de seleção ao lado do modelo.

   1. Na barra de ferramentas, clique em **[!UICONTROL Post]**.

   1. Nas configurações de lançamento, insira ou selecione informações nos campos e clique em **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Quais componentes da conta são lançados.

      * **[!UICONTROL Scheduling]:** Quando publicar o arquivo:

         * *[!UICONTROL Post to search engine now]* (o padrão): cria um arquivo de planilha em massa a partir dos dados de feed propagados e começa a publicá-los imediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Cria um arquivo de bulksheet e o publica posteriormente. Especifique o seguinte:

            * **[!UICONTROL Start Time]:** Uma data e hora futuras em que o arquivo de bulksheet deverá ser publicado na rede de anúncios. Por padrão, o arquivo é enviado às 00:00 (12:00) do dia seguinte. **Nota:** Para arquivos grandes que exigem processamento mais longo, os dados publicados não estão disponíveis imediatamente nas visualizações de gerenciamento de campanha ou no gerenciador de anúncios da rede.

            * **[!UICONTROL End Time]:** Uma data e hora futuras em que os anúncios publicados poderão ser pausados ou excluídos com base no [configuração de dados de feed](feed-settings-manage.md#feed-data-settings) para &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Por padrão, a hora de término é às 00:00 (12:00), 30 dias a partir de hoje. Selecionar **[!UICONTROL None]** para manter os dados ativos indefinidamente (ou até que você propague novos dados para o modelo), ou especifique uma data e hora.

              Para especificar uma data, use o formato DD/MM/AAAA ou D/M/AAAA ou clique em [Calendário](/help/search-social-commerce/assets/calendar.png "Calendário") para abrir o calendário e [selecionar uma data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para alterar uma hora, insira a hora no formato de 24 horas HH/MM ou H/M ou selecione uma hora (em intervalos de 30 minutos) na lista.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Cria um arquivo de planilha em massa disponível no [!UICONTROL Search] > [!UICONTROL Bulksheets] exibição. É possível postar o arquivo a partir daí.

           Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

      * **[!UICONTROL Generate Tracking URLs]:** Se devem ser incluídos URLs de rastreamento para palavras-chave e variações de anúncios no arquivo de bulksheet: *[!UICONTROL Yes]* (o padrão) ou *[!UICONTROL No]*.

        Se você selecionar *[!UICONTROL Yes]*, os URLs são gerados a partir dos URLs de base para as palavras-chave e anúncios de acordo com a [!UICONTROL Tracking Methods] parâmetros no [configurações da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) ou, se estiver mapeando dados para campanhas existentes, para o [!UICONTROL Tracking Methods] parâmetros no existente [configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Se existirem URLs de rastreamento para os itens relevantes, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto criativo ou os parâmetros de rastreamento da conta tenham sido alterados).

      * **[!UICONTROL Bulksheet Name]:** O nome do arquivo de bulksheet que será criado a partir dos dados de feed propagados. Por padrão, o arquivo é nomeado como `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Você pode renomear o arquivo da maneira que desejar, mas ele deve terminar com uma das seguintes extensões de arquivo: `.tsv` (para valores separados por tabulação), `.txt` (para texto ASCII), `.csv` (para valores separados por vírgula) ou `.zip` (para um arquivo TSV compactado). Para dados que incluam caracteres internacionais, use o formato TSV ou TXT.

        O arquivo publicado está disponível no [!UICONTROL Bulksheets] exibir por 30 dias, independentemente de você publicá-lo ou não na rede de publicidade.

O &quot;[!UICONTROL Last Prop. Status]&quot;A coluna mostra o status do trabalho para os modelos aplicáveis.

Quando a bulksheet é criada, ela é listada no [!UICONTROL Bulksheets] exibição. Quando o arquivo for postado, uma notificação por email será enviada com um link para o arquivo. No entanto, se não for possível publicar todos ou alguns dados, um arquivo de erro será listado no [!UICONTROL Bulksheets] e uma notificação por email é enviada com um link para o arquivo de erro.

>[!NOTE]
>
>* Independentemente da opção de agendamento selecionada, os dados especificados serão removidos da [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] listas.
>* Grandes quantidades de dados demoram mais para serem processadas. Você pode acompanhar o progresso do arquivo durante o processo.
>* Todos os dados publicados estão sujeitos ao processo editorial da rede.
>* Antes de um arquivo de bulksheet ser publicado, você pode [cancelar o lançamento](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Interromper um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status dos dados gerados a partir dos feeds](propagated-data-status.md)
