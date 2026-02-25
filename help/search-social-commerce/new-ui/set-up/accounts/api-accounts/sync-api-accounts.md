---
title: (Nova interface) Sincronizar manualmente os dados de rede do e do
description: Saiba como acionar manualmente a sincronização da estrutura da campanha e das entidades da campanha para redes de anúncios compatíveis na nova interface do usuário.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nova interface do usuário) Sincronizar manualmente os dados de rede do e do por meio da conexão da API

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] e apenas contas [!DNL Baidu] existentes*

A sincronização é o processo pelo qual a Pesquisa, o Social e a Commerce reúnem informações atualizadas para cada conta de rede de anúncios conectada de anunciante em [redes de anúncios compatíveis](/help/search-social-commerce/introduction/supported-inventory.md). Esses dados incluem a estrutura de campanha e as entidades de campanha do anunciante, incluindo a maioria dos atributos gerenciados ou relatados em Pesquisa, Social e Commerce. Ela não inclui dados de cliques, nem lances e modificadores de lances inseridos fora da Pesquisa, Social e Commerce, que são coletados separadamente.

O Search, Social e Commerce sincroniza automaticamente (sincroniza) com suas contas de rede de anúncios uma vez por dia e também sempre que detecta uma nova campanha em uma de suas redes de anúncios. Além disso, envia imediatamente todas as alterações nos dados da campanha feitas no Search, Social e Commerce para a rede de anúncios.

Você pode solicitar manualmente a sincronização de todas as campanhas ativas e pausadas em contas especificadas<!--Not available as of 2/23:  or in specific active and paused campaigns -->. Essa tarefa reúne entidades na rede de anúncios que são novas ou alteradas.

Para campanhas com a opção &quot;[!UICONTROL Auto Update]&quot;, a operação de sincronização também gera e publica códigos de rastreamento que estão ausentes ou precisam ser alterados nos modelos de rastreamento ou nas URLs de destino. Os URLs são gerados de acordo com os parâmetros nas configurações de rastreamento das configurações da conta ou da campanha. Se existirem URLs de rastreamento para os itens relevantes, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto criativo ou os parâmetros de rastreamento da conta tenham sido alterados).

>[!NOTE]
>
>Sempre que você [criar um bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), poderá, opcionalmente, sincronizar com a rede de anúncios antes da criação do bulksheet.

## Sincronizar campanhas em uma conta de rede de anúncios

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Marque a caixa de seleção ao lado do nome da conta.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

Você pode seguir o status do trabalho de sincronização na exibição [!UICONTROL Workspace]. O trabalho pode levar
uma hora ou mais para aparecer.

>[!MORELIKETHIS]
>
>* [Baixar/Criar um arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
