---
title: Sobre extensões do sitelink
description: Saiba mais sobre extensões do sitelink.
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/lOrTOUXOFT7cvY5cEilRiROSfIbmcI9v8vU2MVZlg7U
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 0%

---

# Sobre extensões do sitelink

*[!DNL Google Ads]e [!DNL Microsoft Advertising] somente*

Um sitelink é um link de texto extra em uma lista de anúncios de texto. Use sitelinks para levar os usuários diretamente para páginas específicas do site. A rede de anúncios determina quais sitelinks serão exibidos com um anúncio, com base na relevância do sitelink para o anúncio. Opcionalmente, é possível incluir texto descritivo para cada sitelink, que pode ser incluído no anúncio. A rede de publicidade pode exibir automaticamente uma cópia de publicidade dos anúncios existentes na conta com o sitelink quando a cópia de publicidade for altamente relevante para o sitelink. [!DNL Google Ads] pode mostrar de 2 a 6 sitelinks em um anúncio de desktop e até quatro sitelinks em um anúncio móvel. [!DNL Microsoft Advertising] pode mostrar dois, quatro ou seis sitelinks com descrições ou 4-6 sitelinks sem descrições.

O texto e as configurações de sitelink compartilhados são criados, incluindo datas durante as quais os sitelinks podem ser exibidos com anúncios, no nível da conta.

## As visualizações [!UICONTROL Sitelinks] e [!UICONTROL Associations]

A biblioteca [!UICONTROL Extensions] > [!UICONTROL Sitelinks] em [!UICONTROL Campaigns] > [!UICONTROL Campaigns] lista todos os sitelinks no nível da conta e você pode criar e gerenciar seus sitelinks compartilhados lá. Consulte a ajuda da rede de publicidade para obter o número máximo de extensões de anúncios por [[!DNL Google Ads] conta](https://support.google.com/google-ads/answer/6372658) e por [[!DNL Microsoft Advertising] conta](https://help.ads.microsoft.com/#apex/3/en/52001). Os links do site na biblioteca não são usados com seus anúncios até que você os atribua às entidades da conta.

Na exibição [!UICONTROL Extensions] > [!UICONTROL Associations], é possível atribuir qualquer um dos sitelinks como extensões possíveis a todos os anúncios no nível de conta (somente [!DNL Google Ads]), nível de campanha ou nível de grupo de anúncios (somente [!DNL Google Ads]).

## Dados de desempenho para sitelinks

Search, Social e Commerce mapeia os cliques em uma extensão de anúncio e a conversão resultante para a palavra-chave associada ao anúncio no qual a extensão está incluída. Dados de custo ou clique inexistentes no nível da extensão estão disponíveis em Search, Social e Commerce. No entanto, em [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), você pode saber se uma transação resultou de um sitelink (em vez do próprio anúncio) quando o valor na coluna Tipo de link está listado como `sl:<Sitelink text>`, como sl:See Ofertas atuais.

Em [!DNL Google Ads] e [!DNL Microsoft Advertising], você pode ver os dados de custo e clique na guia [!DNL Ad Extensions].

>[!MORELIKETHIS]
>
>* [Gerenciar extensões compartilhadas do sitelink](sitelink-extension-manage.md)
>* [Associar extensões compartilhadas do sitelink a campanhas ou grupos de anúncios](sitelink-extension-associate.md)
