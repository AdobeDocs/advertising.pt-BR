---
title: Status dos dados gerados a partir dos feeds
description: Saiba mais sobre os status dos dados gerados a partir dos feeds de dados de inventário.
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status dos dados gerados a partir dos feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (somente excluir ações) e [!DNL Yandex] somente contas*

Cada componente pode ter um dos seguintes status:

* *[!UICONTROL New]:* O componente não existe na rede de anúncios e não foi postado na rede de anúncios, e você ainda pode editar suas configurações, se necessário, clicando no nome do componente. Quando estiver pronto para publicar os dados, clique em **[!UICONTROL Post to SE]** e especifique os dados a serem enviados.

* *[!UICONTROL Posted]:* (Somente campanhas e grupos de anúncios) A campanha ou grupo de anúncios foi parcialmente publicado na rede de anúncios, mas alguns componentes não foram publicados devido a erros. O status de validação de cada palavra-chave e anúncio mostra quais informações precisam ser corrigidas. Você pode editar as configurações do componente, se necessário, clicando no nome do componente.

* *[!UICONTROL Active]:* O componente já está ativo na rede de anúncios, e você não pode editar suas configurações aqui. Os componentes ativos podem incluir subcomponentes que são [!UICONTROL New], que podem ser publicados se os dados forem válidos.

* *[!UICONTROL Paused]:* O componente já está pausado na rede de anúncios e você não pode editar suas configurações aqui. Os componentes pausados podem incluir subcomponentes que são [!UICONTROL New], que podem ser publicados se os dados forem válidos.

* *[!UICONTROL Deleted]:* O componente já foi excluído na rede de publicidade e você não pode editar suas configurações aqui. Os componentes excluídos podem incluir subcomponentes que [!UICONTROL New], que podem ser publicados se os dados forem válidos.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Publicar dados de campanha gerados a partir de feeds para redes de anúncios](propagated-data-post.md)
>* [Interromper um trabalho de lançamento para dados de feed de estoque](stop-job.md)
