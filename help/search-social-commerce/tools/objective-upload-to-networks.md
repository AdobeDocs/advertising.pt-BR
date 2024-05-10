---
title: Habilitar carregamento de objetivos para redes de anúncios
description: Saiba como fazer upload de objetivos para seus portfólios híbridos no [!DNL Google Ads] e [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Habilitar carregamento de objetivos para redes de anúncios

*Anunciantes com [!DNL Google Ads] e [!DNL Microsoft Advertising] somente contas*

*Anunciantes habilitados somente para otimização híbrida*

Search, Social e Commerce podem fazer upload dos objetivos dos portfólios de uma conta de anunciante para o [!DNL Google Ads] e [!DNL Microsoft Advertising] para que você possa usá-los para otimização híbrida. Os objetivos carregados estão disponíveis como ações de conversão para metas de conversão personalizadas no nível da conta e da campanha.

Habilitar essa opção aciona automaticamente um upload para objetivos em portfólios que contêm campanhas com estratégias de oferta inteligente. O Search, Social e Commerce cria uma conversão na rede de anúncios para cada objetivo aplicável. A conversão representa todas as métricas de conversão ponderadas no objetivo. Cada conversão tem um dos seguintes nomes:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  onde `<network_ID>` é a ID numérica que o Search, Social e Commerce usa para a rede de publicidade, `<objective_id>` é a ID numérica do objetivo e `<network_account_ID>` é a ID numérica da conta da rede de publicidade ou da conta de gerente.

* (Formato antigo que será descontinuado no futuro) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  onde `<portfolio_id>` é a ID numérica do portfólio e `<se_acctid/conversion_manager_se_acctid>` é a ID numérica da conta da rede de publicidade ou da conta de gerente.

  Sua equipe de conta do Adobe trabalhará com você para migrar os nomes de ação de conversão existentes na rede de anúncios antes que o formato antigo seja descontinuado. Durante o período de migração, os uploads de formato antigo e novo serão executados em paralelo. A modelagem e a otimização não são afetadas porque as novas ações de conversão aparecem inicialmente com o status &quot;secundário&quot; (não otimizado) e com 90 dias de dados de preenchimento retroativo.

Carrega para [!DNL Google Ads] ocorrem diariamente às 06:00 no fuso horário do anunciante. Carrega para [!DNL Microsoft Advertising] ocorrem diariamente às 9h no fuso horário do anunciante.

>[!IMPORTANT]
>
>As conversões rastreadas pelo Google Ads e pela tag de rastreamento de evento universal (UET) da Microsoft Advertising não são recarregadas nas redes de publicidade. Se você incluí-los em um objetivo, adicione-os às metas da campanha no editor da rede de publicidade.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao lado de **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes com [!DNL Google Ads] contas que fazem negócios no Espaço Econômico Europeu (EEA) ou Reino Unido (UK); opcional) Se você coletou consentimento de usuários do EEA e do UK para carregar seus dados para fins de publicidade, marque a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clique em **[!UICONTROL Save]**.

1. (Se suas conversões forem rastreadas no nível de uma conta de gerente) [Adicionar credenciais para sua conta de gerente](/help/search-social-commerce/admin/manager-accounts.md) em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

Após a conclusão do upload diário, é possível verificar se as ações de conversão aparecem na rede de anúncios.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento das métricas de conversão de um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Fazer upload de métricas de conversão para [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
