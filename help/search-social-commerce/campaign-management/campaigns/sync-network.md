---
title: Sincronizar manualmente os dados da rede
description: Saiba como acionar manualmente a sincronização da estrutura da campanha e das entidades da campanha para redes de anúncios compatíveis.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Sincronizar manualmente os dados da rede

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] e apenas contas [!DNL Baidu] existentes*

A sincronização é o processo pelo qual a Pesquisa, o Social e a Commerce reúnem informações atualizadas para cada conta de rede de anúncios conectada de anunciante em [redes de anúncios compatíveis](/help/search-social-commerce/introduction/supported-inventory.md). Esses dados incluem a estrutura de campanha e as entidades de campanha do anunciante, incluindo a maioria dos atributos gerenciados ou relatados em Pesquisa, Social e Commerce. Ela não inclui dados de cliques, nem lances e modificadores de lances inseridos fora da Pesquisa, Social e Commerce, que são coletados separadamente.

O Search, Social e Commerce sincroniza automaticamente (sincroniza) com suas contas de rede de anúncios uma vez por dia e também sempre que detecta uma nova campanha em uma de suas redes de anúncios. Além disso, envia imediatamente todas as alterações nos dados da campanha feitas no Search, Social e Commerce para a rede de anúncios.

Você pode solicitar manualmente a sincronização de todas as campanhas ativas e pausadas em contas especificadas ou em campanhas ativas e pausadas específicas. Essa tarefa reúne entidades na rede de anúncios que são novas ou alteradas.

Para campanhas com a opção &quot;[!UICONTROL Auto Upload]&quot;, a operação de sincronização também gera e publica códigos de rastreamento que estão ausentes ou precisam ser alterados nos modelos de rastreamento ou nas URLs de destino. Os URLs são gerados de acordo com os parâmetros nas configurações de rastreamento das configurações da conta ou da campanha. Se existirem URLs de rastreamento para os itens relevantes, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto criativo ou os parâmetros de rastreamento da conta tenham sido alterados).

>[!NOTE]
>
>Sempre que você [criar um bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), poderá, opcionalmente, sincronizar com a rede de anúncios antes da criação do bulksheet.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]>[!UICONTROL Campaigns]**. No submenu, selecione **[!UICONTROL Accounts]** para sincronizar todas as campanhas em contas específicas ou **[!UICONTROL Campaigns]** para sincronizar campanhas específicas.

1. (Opcional) Filtre a lista para incluir contas ou campanhas específicas.

1. Marque a caixa de seleção ao lado de cada conta ou campanha que você deseja sincronizar. Você pode sincronizar até 50 campanhas por vez. Se você sincronizar mais de cinco contas por vez, a tarefa será dividida em lotes de até cinco contas cada.

1. Clique em ![**Mais**](/help/search-social-commerce/assets/more.png " Mais") na barra de ferramentas e selecione **[!UICONTROL Sync]**.

Você pode seguir o status do trabalho de sincronização na exibição [!UICONTROL Workspace]. O trabalho pode levar
uma hora ou mais para aparecer.

>[!MORELIKETHIS]
>
>* [Baixar/Criar um arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
