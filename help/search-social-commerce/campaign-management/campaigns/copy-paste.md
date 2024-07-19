---
title: Criar e editar dados da campanha em massa usando copiar e colar
description: Saiba como gerenciar dados do Campaign em massa usando o recurso copiar e colar.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Criar e editar dados da campanha em massa usando copiar e colar

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e contas [!DNL Baidu] existentes apenas*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] visualizações*

Você pode copiar até 10.000 linhas das exibições [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] e colá-las em [!DNL Microsoft Excel] ou em outro editor para editar quaisquer campos que não sejam ID. Em seguida, você pode copiar as linhas [!DNL Excel] e colá-las como dados separados por tabulação de volta na exibição para fazer as alterações. O recurso usa a área de transferência do computador.

Você pode usar esse recurso para editar objetos de campanha existentes (com campos de ID) e para criar novos objetos de campanha sem campos de ID.

## Copiar linhas de dados

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Marque a caixa de seleção ao lado de cada linha que você deseja copiar.

   É possível copiar até 10.000 linhas.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e em **[!UICONTROL Copy]**.

   Como alternativa, você pode usar o comando de teclado &quot;copiar&quot; dos seus sistemas operacionais, como **[!DNL Ctrl+C]** para [!DNL Microsoft Windows] ou **[!DNL Command-C]** para [!DNL Apple Mac].

1. Na caixa de diálogo [!UICONTROL Copy to Clipboard], clique em **[!UICONTROL Continue]**. Quando os dados estiverem prontos para cópia, clique em **[!UICONTROL Copy]**.

1. Cole as linhas em [!DNL Excel] ou outro editor.

## Editar e criar linhas de dados

1. Edite os dados de acordo com os seguintes requisitos:

   * Os dados colados devem incluir uma linha de cabeçalho e os valores de objeto de campanha necessários; consulte as colunas de bulksheet necessárias para [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Rede de Exibição](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japão](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md) e [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). A ordem das colunas não importa.

      * Para objetos existentes que você deseja editar, é necessário incluir todas as colunas de ID relevantes, nomes de entidade e o atributo a ser editado. Não edite a ID numérica do objeto.

      * Para novos objetos de campanha, inclua todos os nomes e atributos de entidade relevantes, mas não inclua IDs de objeto (que são geradas automaticamente). Por exemplo, se você criar um novo anúncio, deixe o campo [!UICONTROL Ad ID] em branco. A rede de publicidade cria automaticamente uma ID quando você publica o objeto.

   * O valor em qualquer coluna não obrigatória pode ser nulo (em branco), mas cada linha deve ter o mesmo número de valores separados por tabulação.

1. Salve os dados como valores separados por tabulação.

## Colar linhas de dados nas exibições de gerenciamento de campanha

>[!NOTE]
>
>Se as linhas coladas contiverem dados idênticos aos das entidades existentes ou que dupliquem uma entidade existente, os dados duplicados serão ignorados.

1. Em [!DNL Excel] ou outro editor, copie as linhas relevantes separadas por tabulação.

1. No menu principal Search, Social, &amp; Commerce, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Abrir o modo de exibição no qual os dados serão colados (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Na barra de ferramentas acima da tabela de dados, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e em **[!UICONTROL Paste]**.

   Como alternativa, você pode usar o comando de teclado &quot;colar&quot; de seus sistemas operacionais, como o **[!DNL Ctrl+V]** para [!DNL Microsoft Windows] ou o **[!DNL Command-V]** para [!DNL Apple Mac].

1. Cole os dados na caixa de entrada e clique em **[!UICONTROL Process]**.

1. (Opcional) Insira detalhes adicionais:

   * (Se **[!UICONTROL Additional Details]** estiver compactado) Clique em ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para expandir os detalhes.

   * Digite um **[!UICONTROL Job Name]** opcional e/ou **[!UICONTROL Job Description]** opcional.

1. Clique em **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Editar configurações diretamente em uma linha](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Gerenciar campanhas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Gerenciar grupos de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Gerenciar palavras-chave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Gerenciar anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
