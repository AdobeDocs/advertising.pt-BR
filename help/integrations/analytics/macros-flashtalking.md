---
title: Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade
description: Saiba por que e como adicionar [!DNL Analytics for Advertising] macros para o seu [!DNL Flashtalking] tags de publicidade
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

*Aplicável somente ao DSP do anúncio*

Se você usar tags de publicidade de [!DNL Flashtalking] para seus anúncios de DSP de publicidade, anexe os parâmetros do Analytics for Advertising aos URLs da página de aterrissagem. O registro de parâmetros `s_kwcid` e `ef_id` parâmetros da string de consulta no URL da página inicial, permitindo que a Adobe Advertising envie dados de cliques para os anúncios para a Adobe Analytics.

Usar macros para [!DNL Flashtalking] exibição e anúncios de vídeo para os seguintes tipos de [!DNL Analytics for Advertising] implementações:

* **Anunciantes com o [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado em seus sites**: o código JavaScript já registra o `s_kwcid` e `ef_id` parâmetros da sequência de consulta. No entanto, o uso de macros estende o rastreamento para incluir conversões baseadas em cliques quando não há suporte para cookies de terceiros. A prática recomendada é adicionar as macros nas seções a seguir às tags de anúncio para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Anunciantes cujos sites não usam o [!DNL Analytics for Advertising] Código JavaScript e, em vez disso, dependem de [!DNL Analytics] encaminhamento pelo lado do servidor somente para dados de click-through** (sem nenhum dado de view-through): as seguintes macros são necessárias para relatar a atividade de cliques no site orientada por anúncios comprados pela Adobe Advertising.

## Exibir tags de anúncio

No prazo de [!DNL Flashtalking] adicionar configurações de tag, anexe a seguinte macro ao final do URL de click-through no `Clicktag` campo:

```html
?[ftqs:[AdobeAMO]]
```

Exemplo:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Tags de anúncio de vídeo

No prazo de [!DNL Flashtalking] adicionar configurações de tag, anexe a seguinte macro ao final do URL de click-through no `Clicktag` campo:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exemplo:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [IDs de publicidade do Adobe usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade](/help/integrations/analytics/macros-google-campaign-manager.md)

