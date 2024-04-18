---
title: Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade
description: Saiba por que e como adicionar [!DNL Analytics for Advertising] macros para o seu [!DNL Flashtalking] tags de publicidade
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: ca8260e643f24787f7918249906f3f38f3bbef6d
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável somente ao DSP do anúncio*

Se você usar tags de publicidade de [!DNL Flashtalking] para seus anúncios de DSP de publicidade, anexe os parâmetros do Analytics for Advertising aos URLs da página de aterrissagem. Os parâmetros registram a ID AMO (`s_kwcid`) e `ef_id` parâmetros da string de consulta no URL da página inicial, permitindo que o Adobe Advertising envie dados de cliques dos anúncios para a Adobe Analytics.

Usar macros para [!DNL Flashtalking] exibição e anúncios de vídeo para os seguintes tipos de [!DNL Analytics for Advertising] implementações:

* **Anunciantes com o [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado em seus sites**: o código JavaScript já registra a ID do AMO (`s_kwcid`) e `ef_id` parâmetros da sequência de consulta. No entanto, o uso de macros estende o rastreamento para incluir conversões baseadas em cliques quando não há suporte para cookies de terceiros. A prática recomendada é adicionar as macros nas seções a seguir às tags de anúncio para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Anunciantes cujos sites não usam o [!DNL Analytics for Advertising] Código JavaScript e, em vez disso, dependem de [!DNL Analytics] encaminhamento pelo lado do servidor somente para dados de click-through** (sem dados de view-through): as seguintes macros são necessárias para relatar a atividade de cliques no site orientada por anúncios comprados pelo Adobe Advertising.

## Exibir tags de anúncio

No prazo de [!DNL Flashtalking] adicionar configurações de tag, anexe a seguinte macro ao final do URL de click-through no `Clicktag` campo:

```
[ftqs:[AdobeAMO]]
```

É a primeira ou única sequência de consulta após o URL base, em seguida, separe-a do URL base com um `?`. Se o URL base incluirá várias cadeias de caracteres de consulta, comece a primeira com uma `?` e cada string subsequente com um `&`.

Exemplos:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Tags de anúncio de vídeo

No prazo de [!DNL Flashtalking] adicionar configurações de tag, anexe a seguinte macro ao final do URL de click-through no `Clicktag` campo:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

É a primeira ou única sequência de consulta após o URL base, em seguida, separe-a do URL base com um `?`. Se o URL base incluirá várias cadeias de caracteres de consulta, comece a primeira com uma `?` e cada string subsequente com um `&`.

Exemplos:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade](/help/integrations/analytics/macros-google-campaign-manager.md)
