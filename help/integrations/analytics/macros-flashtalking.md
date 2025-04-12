---
title: Acrescentar  [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio
description: Saiba por que e como adicionar  [!DNL Analytics for Advertising] macros às suas [!DNL Flashtalking] marcas de anúncio
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: bbb5feaf96a9be28e112544e34f11fc8f7015946
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Organizações sem uma parceria direta somente com [!DNL Flashtalking]*

*Aplicável somente ao Advertising DSP*

Se você usar as marcas de anúncio de [!DNL Flashtalking] para seus anúncios do Advertising DSP, deverá anexar parâmetros de rastreamento às URLs da sua página de aterrissagem. Para usar a parceria do Advertising DSP com [!DNL Flashtalking], anexe os parâmetros do Analytics for Advertising às URLs da sua página de aterrissagem. Os parâmetros registram os parâmetros AMO ID (`s_kwcid`) e `ef_id` da cadeia de caracteres de consulta na URL da página de aterrissagem, permitindo que o Adobe Advertising envie dados de cliques para os anúncios para o Adobe Analytics.

>[!NOTE]
>
>Se sua organização tiver uma parceria direta com [!DNL Flashtalking], esse procedimento não será necessário para você. Em vez disso, faça logon na conta do [!DNL Flashtalking] e siga a documentação de suporte do [!DNL Flashtalking] para coletar dados de clique usando macros de passagem de dados em `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Use macros para exibição e anúncios de vídeo do [!DNL Flashtalking] para os seguintes tipos de implementações do [!DNL Analytics for Advertising]:

* **Anunciantes com o código JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementado em seus sites**: o código JavaScript já registra os parâmetros de cadeia de caracteres de consulta AMO (`s_kwcid`) e `ef_id`. No entanto, o uso de macros estende o rastreamento para incluir conversões baseadas em cliques quando não há suporte para cookies de terceiros. A prática recomendada é adicionar as macros nas seções a seguir às tags de anúncio para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

  >[!NOTE]
  >
  >O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Anunciantes cujos sites não usam o código JavaScript [!DNL Analytics for Advertising] e dependem do encaminhamento pelo lado do servidor [!DNL Analytics] somente para dados de click-through** (sem dados de view-through): as macros a seguir são necessárias para relatar a atividade de clique no site orientada pelos anúncios comprados pelo Adobe Advertising.

## Exibir tags de anúncio

Nas configurações da tag de anúncio do [!DNL Flashtalking], anexe a seguinte macro ao final da URL de click-through no campo `Clicktag`:

```
[ftqs:[AdobeAMO]]
```

Se for a primeira ou única sequência de consulta após a URL base, separe-a da URL base com um `?`. Se a URL base incluir várias cadeias de caracteres de consulta, comece a primeira cadeia de caracteres com um `?` e cada cadeia de caracteres subsequente com um `&`.

Exemplos:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Tags de anúncio de vídeo

Nas configurações da tag de anúncio do [!DNL Flashtalking], anexe a seguinte macro ao final da URL de click-through no campo `Clicktag`:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Se for a primeira ou única sequência de consulta após a URL base, separe-a da URL base com um `?`. Se a URL base incluir várias cadeias de caracteres de consulta, comece a primeira cadeia de caracteres com um `?` e cada cadeia de caracteres subsequente com um `&`.

Exemplos:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs Usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Marcas de anúncio](/help/integrations/analytics/macros-google-campaign-manager.md)

