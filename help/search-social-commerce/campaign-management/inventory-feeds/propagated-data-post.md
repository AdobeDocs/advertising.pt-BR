---
title: Publicar dados de campanha gerados a partir de feeds para redes de anúncios
description: Saiba como publicar dados gerados a partir de feeds de dados de inventário em redes de anúncios.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 2cf15dbab3dc00ec88a41e4f7d8b5b3646b843e8
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Publicar dados de campanha gerados a partir de feeds para redes de anúncios

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Você pode publicar dados de campanha gerados a partir de um feed à medida que propaga os dados por meio dos modelos associados ou como um processo separado. Depois que você postar os dados, todos os dados propagados existentes serão removidos das listas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

Para uma publicação bem-sucedida, todos os grupos de anúncios devem ser atribuídos a campanhas, todas as palavras-chave e anúncios devem ser atribuídos a grupos de anúncios e todas as informações necessárias devem ser incluídas sem violações de duração.

* Se você usou a opção para &quot;[!UICONTROL Propagate and Preview]&quot;, então [poste o arquivo de bulksheet gerado](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (chamado &quot;`<feed file name>_<template name>`&quot;) da exibição [!UICONTROL Bulksheets].

  Se você não [validou suas páginas de aterrissagem](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) anteriormente, poderá fazê-lo antes de postar o arquivo.

* Se você usou a opção para &quot;[!UICONTROL Propagate only]&quot;, poderá postar os dados gerados para componentes com o [[!UICONTROL New] status](propagated-data-status.md) em uma exibição de hierarquia de campanha da guia [!UICONTROL Templates].

  >[!NOTE]
  >
  >Os componentes ativos ou excluídos podem incluir subcomponentes novos, e os subcomponentes podem ser publicados se os dados forem válidos.

  >[!TIP]
  >
  >Se você não validou suas páginas de aterrissagem anteriormente e deseja fazer isso, [propague os dados e visualize-os](feed-data-propagate.md) da exibição [!UICONTROL Bulksheets] em vez de postá-los na rede de publicidade. Você pode [validar as URLs](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) antes de postar manualmente o arquivo na rede de publicidade.

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que abrirá a guia [!UICONTROL Templates].

   1. Marque a caixa de seleção ao lado do modelo.

   1. Na barra de ferramentas, clique em **[!UICONTROL Post]**.

   1. Nas configurações de lançamento, insira ou selecione informações nos campos e clique em **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Quais componentes da conta são lançados.

      * **[!UICONTROL Scheduling]:** Quando postar o arquivo:

         * *[!UICONTROL Post to search engine now]* (padrão): cria um arquivo de planilha em massa a partir dos dados de feed propagados e começa a postá-los imediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Cria um arquivo de bulksheet e o publica mais tarde. Especifique o seguinte:

            * **[!UICONTROL Start Time]:** Uma data e hora futuras nas quais o arquivo de bulksheet deve ser postado na rede de anúncios. Por padrão, o arquivo é enviado às 00:00 (12:00) do dia seguinte. **Observação:** para arquivos grandes que exigem processamento mais longo, os dados postados não estão disponíveis imediatamente nas exibições de gerenciamento de campanhas ou no gerenciador de anúncios da rede.

            * **[!UICONTROL End Time]:** Uma data e hora futuras em que os anúncios postados poderão ser pausados ou excluídos com base na [configuração de dados de feed](feed-settings-manage.md#feed-data-settings) para &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Por padrão, a hora de término é às 00:00 (12:00), 30 dias a partir de hoje. Selecione **[!UICONTROL None]** para manter os dados ativos indefinidamente (ou até que você propague novos dados para o modelo), ou especifique uma data e hora.

              Para especificar uma data, use o formato DD/MM/AAAA ou D/M/AAAA ou clique em ![Calendário](/help/search-social-commerce/assets/calendar.png "Calendário") para abrir o calendário e [selecionar uma data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para alterar uma hora, insira a hora no formato de 24 horas HH/MM ou H/M ou selecione uma hora (em intervalos de 30 minutos) na lista.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Cria um arquivo de planilha em massa disponível na exibição [!UICONTROL Search] > [!UICONTROL Bulksheets]. É possível postar o arquivo a partir daí.

           Quando o arquivo de bulksheet resultante tiver mais de 2 MB, o arquivo estará no formato ZIP. Não é necessário descompactar o arquivo para publicar.

      * **[!UICONTROL Generate Tracking URLs]:** Se devem ser incluídas URLs de rastreamento para palavras-chave e variações de anúncios no arquivo de bulksheet: *[!UICONTROL Yes]* (o padrão) ou *[!UICONTROL No]*.

        Se você selecionar *[!UICONTROL Yes]*, as URLs serão geradas a partir das URLs de base para as palavras-chave e anúncios de acordo com os parâmetros [!UICONTROL Tracking Methods] nas [configurações da conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) ou, se você estiver mapeando dados para campanhas existentes, para os parâmetros [!UICONTROL Tracking Methods] nas [configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) existentes.

        Se existirem URLs de rastreamento para os itens relevantes, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto criativo ou os parâmetros de rastreamento da conta tenham sido alterados).

      * **[!UICONTROL Bulksheet Name]:** O nome do arquivo de bulksheet a ser criado a partir dos dados de feed propagados. Por padrão, o nome do arquivo é `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Você pode renomear o arquivo como desejar, mas ele deve terminar com uma das seguintes extensões de arquivo: `.tsv` (para valores separados por tabulação), `.txt` (para texto ASCII), `.csv` (para valores separados por vírgula) ou `.zip` (para um arquivo TSV compactado). Para dados que incluam caracteres internacionais, use o formato TSV ou TXT.

        O arquivo postado fica disponível no modo de exibição [!UICONTROL Bulksheets] por 30 dias, independentemente de você publicá-lo ou não na rede de publicidade.

A coluna &quot;[!UICONTROL Last Prop. Status]&quot; mostra o status do trabalho para os modelos aplicáveis.

Quando a bulksheet for criada, ela será listada na exibição [!UICONTROL Bulksheets]. Quando o arquivo for postado, uma notificação por email será enviada com um link para o arquivo. No entanto, se todos ou alguns dados não puderem ser postados, um arquivo de erro será listado no modo de exibição [!UICONTROL Bulksheets] e uma notificação será enviada por email com um link para o arquivo de erro.

>[!NOTE]
>
>* Independentemente da opção de agendamento selecionada, os dados especificados são removidos das listas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].
>* Grandes quantidades de dados demoram mais para serem processadas. Você pode acompanhar o progresso do arquivo durante o processo.
>* Todos os dados publicados estão sujeitos ao processo editorial da rede.
>* Antes da publicação de um arquivo de bulksheet, você pode [cancelar o lançamento](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
>* [Status de dados gerados a partir de feeds](propagated-data-status.md)
