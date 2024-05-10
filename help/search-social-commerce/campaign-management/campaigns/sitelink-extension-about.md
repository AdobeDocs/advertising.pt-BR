---
title: Sobre extensões do sitelink
description: Saiba mais sobre extensões do sitelink.
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Sobre extensões do sitelink

*[!DNL Google Ads]e [!DNL Microsoft Advertising] somente*

Um sitelink é um link de texto extra em uma lista de anúncios de texto. Use sitelinks para levar os usuários diretamente para páginas específicas do site. A rede de anúncios determina quais sitelinks serão exibidos com um anúncio, com base na relevância do sitelink para o anúncio. Opcionalmente, é possível incluir texto descritivo para cada sitelink, que pode ser incluído no anúncio. A rede de publicidade pode exibir automaticamente uma cópia de publicidade dos anúncios existentes na conta com o sitelink quando a cópia de publicidade for altamente relevante para o sitelink. [!DNL Google Ads] pode mostrar de 2 a 6 sitelinks em um anúncio de desktop e até quatro sitelinks em um anúncio móvel. [!DNL Microsoft Advertising] pode mostrar dois, quatro ou seis sitelinks com descrições ou de 4 a 6 sitelinks sem descrições.

O texto e as configurações de sitelink compartilhados são criados, incluindo datas durante as quais os sitelinks podem ser exibidos com anúncios, no nível da conta.

## A variável [!UICONTROL Sitelinks] e [!UICONTROL Associations] visualizações

A variável [!UICONTROL Extensions] > [!UICONTROL Sitelinks] biblioteca em [!UICONTROL Campaigns] > [!UICONTROL Campaigns] O lista todos os sitelinks no nível de conta, e você pode criar e gerenciar seus sitelinks compartilhados lá. Consulte a ajuda da rede de publicidade para obter o número máximo de extensões de anúncios por [[!DNL Google Ads] account](https://support.google.com/google-ads/answer/6372658) e por [[!DNL Microsoft Advertising] account](https://help.ads.microsoft.com/#apex/3/en/52001). Os links do site na biblioteca não são usados com seus anúncios até que você os atribua às entidades da conta.

No [!UICONTROL Extensions] > [!UICONTROL Associations] , é possível atribuir qualquer um dos sitelinks como extensões possíveis a todos os anúncios no nível da conta ([!DNL Google Ads] somente ), nível de campanha ou nível de grupo de publicidade ([!DNL Google Ads] somente).

## Dados de desempenho para sitelinks

Search, Social e Commerce mapeia os cliques em uma extensão de anúncio e a conversão resultante para a palavra-chave associada ao anúncio no qual a extensão está incluída. Dados de custo ou clique inexistentes no nível da extensão estão disponíveis em Pesquisa, Social e Comércio. No entanto, em [o [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), é possível saber se uma transação resultou de um link de site (em vez do próprio anúncio) quando o valor na coluna Tipo de link é listado como `sl:<Sitelink text>`, como sl:Consulte Ofertas atuais.

Entrada [!DNL Google Ads] e [!DNL Microsoft Advertising], você pode ver os dados de custo e clique no link [!DNL Ad Extensions] guia.

>[!MORELIKETHIS]
>
>* [Gerenciar extensões compartilhadas do sitelink](sitelink-extension-manage.md)
>* [Associar extensões compartilhadas do sitelink a campanhas ou grupos de anúncios](sitelink-extension-associate.md)
