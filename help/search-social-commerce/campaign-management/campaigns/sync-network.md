---
title: Sincronizar manualmente os dados da rede
description: Saiba como acionar manualmente a sincronização da estrutura da campanha e das entidades da campanha para redes de anúncios compatíveis.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Sincronizar manualmente os dados da rede

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising] (antigo [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], e [!DNL Yandex] somente contas*

A sincronização é o processo pelo qual o Search, Social e Commerce coleta informações atualizadas para cada conta de rede de anúncios de anunciante no [redes de publicidade suportadas](/help/search-social-commerce/introduction/supported-inventory.md). Esses dados incluem a estrutura de campanha e as entidades de campanha do anunciante, incluindo a maioria de seus atributos gerenciados ou relatados em Pesquisa, Social e Comércio. Ela não inclui dados de cliques, nem ofertas e modificadores de ofertas inseridos fora da Pesquisa, Social e Comércio, que são coletados separadamente.

O Search, Social e Commerce sincroniza automaticamente (sincroniza) com suas contas de rede de anúncios uma vez por dia e sempre que detecta uma nova campanha em uma de suas redes de anúncios. Além disso, ele envia imediatamente todas as alterações nos dados da campanha feitas no Search, Social e Commerce para a rede de anúncios.

Você pode solicitar manualmente a sincronização de todas as campanhas ativas e pausadas em contas especificadas ou em campanhas ativas e pausadas específicas. Essa tarefa reúne entidades na rede de anúncios que são novas ou alteradas.

Para campanhas com &quot;[!UICONTROL Auto Upload]&quot;, a operação de sincronização também gera e publica códigos de rastreamento que estão ausentes ou precisam ser alterados nos modelos de rastreamento ou URLs de destino. Os URLs são gerados de acordo com os parâmetros nas configurações de rastreamento das configurações da conta ou da campanha. Se existirem URLs de rastreamento para os itens relevantes, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavra-chave, o texto criativo ou os parâmetros de rastreamento da conta tenham sido alterados).

>[!NOTE]
>
>Sempre que você [criar uma bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), você pode, opcionalmente, sincronizar com a rede de anúncios antes da criação do bulksheet.

1. No menu principal, clique em **[!UICONTROL Search]>[!UICONTROL Campaigns]**. No submenu, selecione **[!UICONTROL Accounts]** para sincronizar todas as campanhas em contas específicas ou **[!UICONTROL Campaigns]** para sincronizar campanhas específicas.

1. (Opcional) Filtre a lista para incluir contas ou campanhas específicas.

1. Marque a caixa de seleção ao lado de cada conta ou campanha que você deseja sincronizar. Você pode sincronizar até 50 campanhas por vez. Se você sincronizar mais de cinco contas por vez, a tarefa será dividida em lotes de até cinco contas cada.

1. Clique em **![Mais](/help/search-social-commerce/assets/more.png "Mais")** na barra de ferramentas e selecione **[!UICONTROL Sync]**.

Você pode seguir o status do trabalho de sincronização no [!UICONTROL Workspace] exibição. A tarefa pode levar uma hora ou mais para ser exibida.

>[!MORELIKETHIS]
>
>* [Baixar/criar um arquivo de bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)

