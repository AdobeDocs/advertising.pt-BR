---
title: O parâmetro de rastreamento da ID do AMO (s_kwcid)
description: Saiba mais sobre o parâmetro de rastreamento usado para compartilhar dados do Adobe Advertising com o Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# O parâmetro de rastreamento da ID do AMO (s_kwcid)

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

O Adobe Advertising compartilha dados sobre suas campanhas com a Adobe Analytics usando o parâmetro de acréscimo da ID do AMO, também chamado de `s_kwcid` que consiste em elementos específicos do canal de publicidade e da rede de publicidade.

<!-- add everything below to IDs page -->

O parâmetro é adicionado aos URLs de rastreamento de uma das seguintes maneiras:

* (Recomendado) O recurso de inserção do lado do servidor é implementado.

  Para [!DNL Google Ads] e [!DNL Microsoft Advertising] contas com o [!UICONTROL Auto Upload] configuração ativada para a conta ou campanha, o servidor de pixels anexa automaticamente o parâmetro da ID do AMO aos sufixos da página de aterrissagem quando um usuário final clica em um anúncio <!-- click a search ad or views a display ad --> com o pixel Adobe Advertising.

  Para outras redes de publicidade, ou [!DNL Google Ads] e [!DNL Microsoft Advertising] contas com o [!UICONTROL Auto Upload] configuração desativada, adicione manualmente o parâmetro da ID do AMO aos parâmetros de acréscimo no nível da conta, que o anexam aos URLs base.

* <!-- (Search, Social, & Commerce only) -->O recurso de inserção do lado do servidor não está implementado e você precisa adicionar manualmente o parâmetro da ID do AMO ao seu ([!DNL Google Ads] e [!DNL Microsoft Advertising]) sufixos de página de aterrissagem ou (outras redes de anúncios) parâmetros de acréscimo no nível da conta.

Para implementar o recurso de inserção do lado do servidor ou determinar a melhor opção para sua empresa, entre em contato com a equipe de conta da Adobe.

Para obter os formatos de ID do AMO para DSP e Pesquisa, Social e Comércio, consulte &quot;[IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Gerenciar contas de rede de publicidade](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Configurações da campanha no Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Configurações da campanha do Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Configurações da campanha de publicidade do Microsoft](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Configurações da campanha de anúncios no Japão](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Configurações da campanha Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
