---
title: Anexar [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] marcas de anúncio
description: Saiba por que e como adicionar  [!DNL Analytics for Advertising] macros às suas [!DNL Google Campaign Manager 360] marcas de anúncio
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 0b95d99a1370a047642f8d1e4bbafe35ad5187f6
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Acrescentar [!DNL Analytics for Advertising] macros a [!DNL Google Campaign Manager 360] marcas de anúncio

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável somente ao Advertising DSP*

Se você usar marcas de anúncio de [!DNL Google Campaign Manager 360] para seus anúncios Advertising DSP, anexe [!DNL Analytics for Advertising] parâmetros às URLs da sua página de aterrissagem usando a macro [`%p` &#x200B;](https://support.google.com/campaignmanager/table/6096962). Os parâmetros registram os parâmetros AMO ID (`s_kwcid`) e `ef_id` da cadeia de caracteres de consulta na URL da página de aterrissagem, permitindo que o Adobe Advertising envie dados de cliques para os anúncios para o Adobe Analytics.

Use macros para exibição e anúncios de vídeo do [!DNL Campaign Manager 360] para os seguintes tipos de implementações do [!DNL Analytics for Advertising]:

* **Anunciantes com o código JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementado em seus sites**: o código JavaScript já registra os parâmetros de cadeia de caracteres de consulta AMO (`s_kwcid`) e `ef_id`. No entanto, o uso de macros estende o rastreamento para incluir conversões baseadas em cliques quando não há suporte para cookies de terceiros. A prática recomendada é adicionar as macros nas seções a seguir às tags de anúncio para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Anunciantes cujos sites não usam o código JavaScript [!DNL Analytics for Advertising] e dependem do encaminhamento pelo lado do servidor [!DNL Analytics] somente para dados de click-through** (sem dados de view-through): as macros a seguir são necessárias para relatar a atividade de clique no site orientada pelos anúncios comprados pelo Adobe Advertising.

## Acrescentar as macros aos seus anúncios do [!DNL Google Campaign Manager 360]

No [!DNL Google Campaign Manager 360], anexe ao seguinte parâmetro à URL da página de aterrissagem para cada exibição e anúncio de vídeo: `%pamo=!;`

Você pode especificar o URL da página de aterrissagem de várias maneiras. As instruções para cada opção estão incluídas nas subseções a seguir.

Veja a seguir um exemplo do URL da página inicial formatado com o sufixo.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Se a URL da página de aterrissagem incluir um símbolo de hash (#), o que não é comum, coloque o parâmetro `amo` antes do símbolo de hash.
>* Se nenhum outro parâmetro for incluído após o parâmetro `amo`, adicione um parâmetro (por exemplo, &amp;a=b) depois dele. Exemplo: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurar o sufixo do URL da página de aterrissagem no nível do anunciante

1. Consulte as [instruções para abrir as propriedades do anunciante](https://support.google.com/campaignmanager/answer/2829344).
1. Nas configurações de [!UICONTROL Landing page URL suffix], inclua `%pamo!;` no campo [!UICONTROL URL suffix].

### Configurar o sufixo do URL da página de aterrissagem no nível da campanha

1. Consulte as [instruções para abrir as propriedades da campanha](https://support.google.com/campaignmanager/answer/2838056#set).
1. Nas configurações de [!UICONTROL Landing page URL suffix], inclua `%pamo!;` no campo [!UICONTROL URL suffix].

### Configurar o sufixo do URL da página de aterrissagem no nível da criação

1. Abra as propriedades criativas.
1. Na configuração [!UICONTROL Click tags], inclua `%pamo!;` na coluna [!UICONTROL Landing page] para a marca de clique.

## Como as macros [!DNL Analytics for Advertising] são expandidas no DSP

No DSP, ao criar um anúncio que inclui o parâmetro [!DNL Analytics for Advertising] (`amo`), as macros `ef_id` e `s_kwcid` são automaticamente anexadas à URL de clique. A prática recomendada é verificar a marca no DSP para garantir que as macros `ef_id` e `s_kwcid` estejam presentes.

Este é um exemplo de uma [!DNL Google Campaign Manager 360] [in tag](https://support.google.com/campaignmanager/answer/6080468) como ela aparece na DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Quando um usuário clica no anúncio, [!DNL Google Campaign Manager 360] vê `%pamo` no sufixo da URL e insere dinamicamente o valor do parâmetro `amo` na URL.

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Acrescentar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Marcas de anúncio](macros-flashtalking.md)
