---
title: Métricas e dimensões do Adobe Advertising no Customer Journey Analytics
description: Consulte as métricas e dimensões do Adobe Advertising disponíveis no Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 6e22ead8f91d87cce3f104635e95a2dcab03bc3a
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Métricas e dimensões do Adobe Advertising no Customer Journey Analytics

*Anunciantes com apenas uma integração Adobe Advertising-Customer Journey Analytics*

*recurso do Beta*

O Adobe Advertising transmite métricas e dimensões de tráfego para [!DNL Customer Journey Analytics] diariamente. [!DNL Web SDK] captura click-throughs e view-throughs do Adobe Advertising em tempo real e os transmite para o Customer Journey Analytics.

## Métricas de tráfego do Adobe Advertising

<!-- Verify column names -->

Na tabela a seguir:

* &quot;Nome do campo XDM&quot; é o nome do campo no Adobe Experience Platform.

* &quot;Nome de exibição do campo XDM&quot; indica o nome de exibição no Customer Journey Analytics.

| Nome do campo Adobe Advertising | Nome do campo XDM | Nome de exibição do campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Data | Data | Todos | |
| ID AMO | skwcid | ADOBE ADVERTISING ID | Todos |
| Impressões AMO | adobe_advertising_impressions | Impressões do Adobe Advertising | Todos |
| Cliques AMO | adobe_advertising_clicks | Cliques do Adobe Advertising | Todos |
| Custo AMO | adobe_advertising_cost | Custo do Adobe Advertising | Todos |
| Código de moeda | moeda | Moeda | Todos |
| Visualizações AMO | adobe_advertising_views | Visualizações do Adobe Advertising | Ad Cloud DSP |
| Visualizações do AMO 25% concluídas | adobe_advertising_views_25_pct | Visualizações do Adobe Advertising 25% concluídas | Ad Cloud DSP |
| Visualizações AMO 50% concluídas | adobe_advertising_views_50_pct | Adobe Advertising Views 50% Concluídas | Ad Cloud DSP |
| Visualizações do AMO 75% concluídas | adobe_advertising_views_75_pct | Adobe Advertising Views 75% concluído | Ad Cloud DSP |
| Visualizações do AMO 100% concluídas | adobe_advertising_views_100_pct | Adobe Advertising Views 100% concluídas | Ad Cloud DSP |
| Minutos do AMO Visualizados | adobe_advertising_minutes_viewed | Minutos do Adobe Advertising visualizados | Ad Cloud DSP |
| Impressões para visualização do AMO | adobe_advertising_viewable_impressions | Impressões visíveis do Adobe Advertising | Ad Cloud DSP |
| Impressões não visualizáveis do AMO | adobe_advertising_not_viewable_impressions | Impressões do Adobe Advertising não visualizáveis | Ad Cloud DSP |
| Impressões mensuráveis AMO | adobe_advertising_messurable_impressions | Impressões mensuráveis do Adobe Advertising | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Dimensões do Adobe Advertising

Na tabela a seguir:

* &quot;Nome do campo XDM&quot; é o nome do campo no Adobe Experience Platform.

* &quot;Nome de exibição do campo XDM&quot; indica o nome de exibição no Customer Journey Analytics.

| Nome do campo Adobe Advertising | Nome do campo XDM | Nome de exibição do campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Chave | skwcid | ADOBE ADVERTISING ID |
| Plataforma de publicidade | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Conta | adobe_advertising_account | Conta do Adobe Advertising |
| Campaign | adobe_advertising_campaign | Campanha Adobe Advertising |
| Grupo de publicidade | adobe_advertising_ad_group | Grupo de publicidade do Adobe Advertising |
| Palavra-chave | adobe_advertising_keyword | Palavra-chave do Adobe Advertising |
| Anúncio | adobe_advertising_ad | Anúncio Adobe Advertising |
| Posicionamento | adobe_advertising_placement | Posicionamento do Adobe Advertising |
| Tipo de correspondência | adobe_advertising_match_type | Tipo de correspondência do Adobe Advertising |
| Título do anúncio | adobe_advertising_ad_title | Título do anúncio do Adobe Advertising |
| Descrição do anúncio | adobe_advertising_ad_description | Descrição de anúncio do Adobe Advertising |
| URL de destino do anúncio | adobe_advertising_ad_destination_url | URL de destino do anúncio Adobe Advertising |
| Adicionar URL de exibição | adobe_advertising_ad_display_url | URL de exibição do anúncio do Adobe Advertising |
| Dispositivo | adobe_advertising_device | Dispositivo Adobe Advertising |
| Correspondência de Tipo de Palavra-chave | adobe_advertising_keyword_matchtype | Correspondência de tipo de palavra-chave do Adobe Advertising |
| Rede | adobe_advertising_network | Rede Adobe Advertising |
| Tipo de anúncio | adobe_advertising_ad_type | Tipo de anúncio do Adobe Advertising |
| Destino do produto | adobe_advertising_product_target | Direcionamento de produto do Adobe Advertising |
| Tipo de aterrissagem | adobe_advertising_landing_type | Tipo de aterrissagem do Adobe Advertising |
| Otimização | adobe_advertising_otimization | Otimização do Adobe Advertising |

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* [Pré-requisitos](prerequisites.md)
>* [Adobe Advertising IDs Usadas por [!DNL Customer Journey Analytics]](ids.md)
