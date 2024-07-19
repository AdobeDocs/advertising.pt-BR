---
title: Status dos dados gerados a partir dos feeds
description: Saiba mais sobre os status dos dados gerados a partir dos feeds de dados de inventário.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status dos dados gerados a partir dos feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (somente ações de exclusão) e somente contas [!DNL Yandex]*

Cada componente pode ter um dos seguintes status:

* *[!UICONTROL New]:* O componente não existe na rede de anúncios e não foi postado na rede de anúncios, e você ainda poderá editar suas configurações, se necessário, clicando no nome do componente. Quando estiver pronto para publicar os dados, clique em **[!UICONTROL Post to SE]** e especifique os dados a serem enviados.

* *[!UICONTROL Posted]:* (Somente campanhas e grupos de anúncios) A campanha ou o grupo de anúncios foi parcialmente postado na rede de anúncios, mas alguns componentes não foram postados devido a erros. O status de validação de cada palavra-chave e anúncio mostra quais informações precisam ser corrigidas. Você pode editar as configurações do componente, se necessário, clicando no nome do componente.

* *[!UICONTROL Active]:* O componente já está ativo na rede de anúncios, e você não pode editar suas configurações aqui. Os componentes ativos podem incluir subcomponentes que são [!UICONTROL New], que podem ser postados se os dados forem válidos.

* *[!UICONTROL Paused]:* O componente já está pausado na rede de anúncios e você não pode editar suas configurações aqui. Os componentes pausados podem incluir subcomponentes que são [!UICONTROL New], que podem ser postados se os dados forem válidos.

* *[!UICONTROL Deleted]:* O componente já foi excluído na rede de publicidade e você não pode editar suas configurações aqui. Os componentes excluídos podem incluir subcomponentes que são [!UICONTROL New], que podem ser postados se os dados forem válidos.

>[!MORELIKETHIS]
>
>* [Sobre feeds de inventário](inventory-feeds-about.md)
>* [Exibir dados gerados de feeds](propagated-data-view.md)
>* [Editar dados gerados a partir dos feeds](propagated-data-edit.md)
>* [Dados de pós-campanha gerados de feeds para redes de anúncios](propagated-data-post.md)
>* [Parar um trabalho de lançamento para dados de feed de estoque](stop-job.md)
