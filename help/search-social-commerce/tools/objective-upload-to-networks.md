---
title: Ativar o upload de objetivos para redes publicidade
description: Aprenda a upload objetivos para seus portfólios híbridos [!DNL Google Ads]  [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Ativar o upload de objetivos para redes publicidade

*Anunciantes somente com [!DNL Google Ads] e [!DNL Microsoft Advertising] contas*

*Anunciantes habilitados somente para otimização híbrida*

Search, Social &amp; Comércio podem upload os objetivos dos portfólios de uma anunciante conta para [!DNL Google Ads] [!DNL Microsoft Advertising] que você possa usá-los para otimização híbrida. Seus objetivos carregados estão disponíveis como ações conversão para metas de conversão personalizados de nível conta e campanha.

Ativar essa opção aciona automaticamente uma upload para objetivos em portfólios que contêm campanhas com estratégias de lance inteligente. Search, Social &amp; Comércio cria uma conversão na rede de publicidade para cada objetivo aplicável. A conversão representa todas as métricas de conversão ponderadas no objetivo. Cada conversão tem um dos seguintes nomes:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  onde `<network_ID>` é a ID numérico que Search, Social &amp; Comércio usa para o rede de publicidade, `<objective_id>` é a ID numérico objetivo e `<network_account_ID>` é a ID numérico para o rede de publicidade conta ou gerenciador conta.

* (Formato antigo que será descontinuado no futuro) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  onde `<portfolio_id>` é a ID do numérico portfólio e `<se_acctid/conversion_manager_se_acctid>` é a ID numérico do rede de publicidade conta ou conta do gerenciador.

  Sua equipe de conta Adobe Systems trabalhará com você para migrar os nomes de ação existentes conversão dentro da rede de publicidade antes que o formato antigo seja descontinuado. Durante o período de migração, os uploads antigos e novos do formato serão executados em paralelo. A modelagem e a otimização não são afetadas porque as novas ações do conversão aparecem inicialmente com status &quot;secundária&quot; (não otimizada) e com 90 dias de dados preenchimento retroativo.

Faz uploads para [!DNL Google Ads] que ocorram diariamente às 06:00 no fuso horário do anunciante. Os uploads [!DNL Microsoft Advertising] ocorrem diariamente às 09:00 no fuso horário do anunciante.

>[!IMPORTANT]
>
>As conversões rastreadas pelo Google Ads e pela Microsoft Advertising universal evento rastreamento (UET) tag não são recargadas para as redes publicidade. Se você as incluir em um objetivo, adicione-as às campanha metas dentro das editor do rede de publicidade.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. No menu principal, clique **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao **[!UICONTROL Enable Objective Upload]** lado de .

1. (Anunciantes com [!DNL Google Ads] contas que fazem negócios na Área Econômica Europeia (EEA) ou Reino Unido (Reino Unido); opcional) Se você coletou o consentimento de usuários da EEA e do Reino Unido para upload seus dados para fins de publicidade, selecione a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clique **[!UICONTROL Save]** em .

1. (Se suas conversões forem rastreadas em um nível de conta do gerenciador) [Adicione credenciais para os conta](/help/search-social-commerce/admin/manager-accounts.md) do gerente em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verifique se cada objetivo - nomeado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - aparece dentro de dois dias na rede de publicidade.

   [!DNL Google Ads] No editor, procure suas [ações](https://support.google.com/google-ads/answer/11461796) de conversão. [!DNL Microsoft Advertising] No editor, procure seus [objetivos conversão](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Se necessário, atualize a intervalo de datas para incluir a data do upload.

## Solução de problemas de objetivos ausentes

Se o objetivo - nomeado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` - para um de seus portfólios não aparecer na rede de publicidade, verifique o seguinte:

* ([!DNL Google Ads]) Verifique se as conversões devem ser carregadas no conta ou no nível do gerenciador. Se eles devem ser enviados por upload no nível do gerenciador:

   * Verifique se as credenciais do conta do [!DNL Google Ads] gerenciador são fornecidas em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Se necessário, [adicione as credenciais para o gerenciador conta](/help/search-social-commerce/admin/manager-accounts.md).

   * Verifique se a rede de publicidade conta já inclui o mesmo nome métrica. Se o fizer, renomeie a métrica para que as propriedade de nível de gerenciador corretas possam ser criadas.

* Verifique se a opção &quot;híbrida&quot; da portfólio está selecionada e se o objetivo tem receita válidos.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento das métricas conversão de uma anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Fazer upload conversão métricas para [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
