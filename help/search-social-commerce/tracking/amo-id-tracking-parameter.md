---
title: O parâmetro de rastreamento da ID do AMO (s_kwcid)
description: Saiba mais sobre o parâmetro de rastreamento usado para compartilhar dados do Adobe Advertising com o Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# O parâmetro de rastreamento da ID do AMO (s_kwcid)

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

O Adobe Advertising compartilha dados sobre suas campanhas com a Adobe Analytics usando o parâmetro de acréscimo da ID do AMO, também chamado de `s_kwcid` que consiste em elementos específicos do canal de publicidade e da rede de publicidade.

O parâmetro é adicionado aos URLs de rastreamento de uma das seguintes maneiras:

* (Recomendado) O recurso de inserção do lado do servidor é implementado.

   * Clientes DSP: o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final visualiza um anúncio de exibição com o pixel Adobe Advertising.

   * Clientes de pesquisa, social e comércio:

      * Para [!DNL Google Ads] e [!DNL Microsoft® Advertising] contas com o [!UICONTROL Auto Upload] configuração ativada para a conta ou campanha, o servidor de pixels anexa automaticamente o parâmetro s_kwcid aos sufixos da página de aterrissagem quando um usuário final clica em um anúncio com o pixel Adobe Advertising.

      * Para outras redes de publicidade, ou [!DNL Google Ads] e [!DNL Microsoft® Advertising] contas com o [!UICONTROL Auto Upload] configurando desativado, adicione manualmente o parâmetro aos parâmetros de acréscimo no nível da conta, que o anexam aos URLs base.

* O recurso de inserção do lado do servidor não está implementado:

   * Clientes DSP:

      * Para [!DNL Flashtalking] adicionar tags, insira manualmente macros adicionais de acordo com &quot;[Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Para [!DNL Google Campaign Manager 360] adicionar tags, insira manualmente macros adicionais de acordo com &quot;[Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Clientes de pesquisa, social e comércio:

      * Para ([!DNL Google Ads] e [!DNL Microsoft® Advertising]), adicione manualmente o parâmetro da ID do AMO aos sufixos da sua página de aterrissagem.

      * Para anúncios em todas as outras redes de anúncios, adicione manualmente o parâmetro da ID do AMO aos parâmetros de acréscimo no nível da conta, que o anexam aos URLs base.

Para implementar o recurso de inserção do lado do servidor ou determinar a melhor opção para sua empresa, entre em contato com a equipe de conta da Adobe.

Para obter os formatos de ID do AMO para DSP e Pesquisa, Social e Comércio, consulte &quot;[IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Pesquisa, Social e Comércio) [Gerenciar contas de rede de publicidade](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Pesquisa, Social e Comércio) [Configurações da campanha no Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Pesquisa, Social e Comércio) [Configurações da campanha do Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Pesquisa, Social e Comércio) [Configurações da campanha publicitária da Microsoft®](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Pesquisa, Social e Comércio) [Yahoo! Configurações da campanha de anúncios no Japão](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Pesquisa, Social e Comércio) [Configurações da campanha Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
