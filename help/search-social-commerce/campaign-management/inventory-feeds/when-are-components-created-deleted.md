---
title: Quando os componentes da conta são criados ou excluídos pelos feeds de inventário?
description: Saiba quais situações criam e excluem componentes da conta ao lançar feeds de inventário.
exl-id: 93b31996-15dd-4215-ae9d-39327910f712
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Quando os componentes da conta são criados ou excluídos pelos feeds de inventário?

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Quando um arquivo de feed de inventário é propagado por meio de um modelo, os componentes da conta são criados e excluídos da seguinte maneira.

>[!NOTE]
>
>Anúncios duplicados nunca são criados em um grupo de anúncios.

| Cenário | Exemplo | Ação |
|----|----|----|
| Os dados do feed incluem um novo valor para uma coluna usada em um nome de campanha, nome de grupo de anúncios, palavra-chave ou grupo de produtos. | Arquivos anteriores:<br>Campaign=Hats<br>Campaign=Luvas<br><br>Novo arquivo:<br>Campaign=Sapatos | Uma nova campanha, grupo de publicidade, palavra-chave ou grupo de produtos será criada se não existir na rede de publicidade. |
| Os dados do feed contêm um novo valor para uma coluna usada em um anúncio. | Arquivo anterior: um anúncio incluía price=20<br><br>Novo arquivo: Para o mesmo anúncio, price=10 | Quando a cópia de anúncio de [!DNL Microsoft® Advertising] anúncios de texto expandidos, [!DNL Yahoo! Japan ads]ou [!DNL Yandex] anúncios é alterado, o anúncio existente é excluído e um novo é criado.<br><br>Quando o texto do anúncio é alterado para outros tipos de anúncio ou quando a coluna aplicável é usada para um [!DNL Google Ads] parâmetro de publicidade ({param1} ou {param2}) em um anúncio, o anúncio existente será atualizado. |
| As configurações do modelo para a campanha, grupo de publicidade, palavra-chave ou grupo de produtos foram alteradas desde a última propagação. | Configuração anterior:Palavra-chave=[Palavra-chave]<br><br>Nova configuração: Palavra-chave=&lt;color>[Palavra-chave] | Uma nova campanha, grupo de publicidade, palavra-chave ou grupo de produtos será criada se não existir na rede de publicidade. |
| As configurações do modelo para um anúncio foram alteradas desde a última propagação. | Configuração anterior: Ad description=&quot;Buy [categoria] agora.&quot;<br><br>Nova configuração: Ad description=&quot;Buy [marca] agora.&quot; | Quando a cópia de anúncio de [!DNL Microsoft® Advertising] anúncios de texto expandidos, [!DNL Yahoo! Japan ads]ou [!DNL Yandex] anúncios é alterado, o anúncio existente é excluído e um novo é criado.<br><br>Quando a cópia de anúncio é alterada para outros tipos de anúncio ou quando a alteração reflete uma alteração na coluna usada para um único [!DNL Google Ads] parâmetro de publicidade ({param1} ou {param2}) em um anúncio, o anúncio existente será atualizado. |
| Os novos dados de feed não incluem uma linha para uma campanha ou grupo de anúncios existente. | n/d | As campanhas e grupos de anúncios existentes permanecem como estão. |
| Os novos dados de feed não incluem uma linha para um grupo de anúncios, anúncio, palavra-chave ou grupo de produtos existente. | n/d | O grupo de anúncios, anúncio, palavra-chave ou grupo de produtos existente permanece como está, está pausado ou foi excluído, de acordo com o [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). |
| Os novos dados de feed de um grupo de produtos principal existente não incluem linhas para seus grupos de produtos secundários existentes. | n/d | O grupo de produtos principal existente permanece como está ou é excluído, de acordo com o [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). <b>Nota:</b> Se as configurações de dados do feed estiverem definidas para pausar itens de linha ausentes, o grupo de produtos principal ainda será excluído porque você não pode pausar grupos de produtos. |
| Os novos dados do feed incluem uma linha para um grupo de anúncios, anúncio, palavra-chave ou grupo de produtos que era a) nos dados anteriores, mas b) foi omitida desde então e foi pausada de acordo com a variável [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). | n/d | O grupo de anúncios, anúncio, palavra-chave ou grupo de produtos existente é reativado, sem perder o histórico ou a pontuação de qualidade. |
| Os novos dados do feed incluem uma linha para um grupo de anúncios, anúncio, palavra-chave ou grupo de produtos que era a) nos dados anteriores, mas b) era omitida desde então e era excluída de acordo com a variável [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). | n/d | Um novo grupo de anúncios, anúncio, palavra-chave ou grupo de produtos é criado. |
| Você desativou a opção de nível de campanha ou grupo de anúncios para &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | A lista de palavras-chave negativas inclui &quot;coupé&quot; e &quot;carro esportivo&quot;.<br><br>O grupo de anúncios já inclui a palavra-chave negativa &quot;SUV&quot;. | Qualquer palavra-chave negativa existente que não esteja na lista permanece como está. |
| Você ativou a opção de nível de campanha ou grupo de anúncios para &quot;[!UICONTROL Delete negative keywords when omitted from list],&quot; e palavras-chave negativas que não estão na lista existem. | A lista de palavras-chave negativas inclui &quot;coupé&quot; e &quot;carro esportivo&quot;.<br><br>O grupo de anúncios já inclui a palavra-chave negativa &quot;SUV&quot;. | Qualquer palavra-chave negativa não especificada criada anteriormente usando o modelo é excluída quando um arquivo de feed é propagado por meio do modelo. No entanto, quaisquer palavras-chave negativas não especificadas criadas usando outros meios (como em bulksheets simples, a variável [!UICONTROL Campaigns] ou no editor de anúncios da rede de publicidade) permanecem como estão. | | A data de término agendada para os componentes de um arquivo de feed publicado ocorre. | n/d | As campanhas existentes permanecem como estão. Os grupos de anúncios, anúncios e palavras-chave existentes permanecem como estão, estão pausados ou são excluídos, de acordo com o [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). |
| O nível de estoque de um item cai abaixo de um mínimo especificado no [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). | Arquivo anterior: stock=10<br><br>Novo arquivo: stock=0 | As campanhas existentes permanecem como estão. Os grupos de anúncios, anúncios, palavras-chave e grupos de produtos existentes estão pausados ou excluídos, de acordo com o [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). |
| O nível de estoque de um item volta acima de um mínimo especificado no [configurações de dados de feed](feed-settings-manage.md#feed-data-settings). | Arquivo anterior: stock=0<br><br> Novo arquivo: stock=10 | Quando os anúncios, palavras-chave ou grupos de produtos existentes são pausados, eles são reativados sem perder o histórico ou a pontuação de qualidade. Quando não existem anúncios, palavras-chave ou grupos de produtos (por exemplo, se eles foram excluídos anteriormente porque o nível do estoque estava abaixo do mínimo), novos são criados. |

>[!MORELIKETHIS]
>
>* [Sobre a automatização do gerenciamento de anúncios usando feeds de inventário](inventory-feeds-about.md)
