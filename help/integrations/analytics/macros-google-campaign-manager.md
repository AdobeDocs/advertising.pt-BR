---
title: Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade
description: Saiba por que e como adicionar [!DNL Analytics for Advertising] macros para o seu [!DNL Google Campaign Manager 360] tags de publicidade
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 703cda43e96dfa9d80bbce2d64192fc461d5dbae
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] Macros para [!DNL Google Campaign Manager 360] Tags de publicidade

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

*Aplicável somente ao DSP do anúncio*

Se você usar tags de publicidade de [!DNL Google Campaign Manager 360] para seus anúncios de DSP, anexe [!DNL Analytics for Advertising] parâmetros para os URLs da sua landing page usando o [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Os parâmetros registram a ID AMO (`s_kwcid`) e `ef_id` parâmetros da string de consulta no URL da página inicial, permitindo que o Adobe Advertising envie dados de cliques dos anúncios para a Adobe Analytics.

Usar macros para [!DNL Campaign Manager 360] exibição e anúncios de vídeo para os seguintes tipos de [!DNL Analytics for Advertising] implementações:

* **Anunciantes com o [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado em seus sites**: o código JavaScript já registra a ID do AMO (`s_kwcid`) e `ef_id` parâmetros da sequência de consulta. No entanto, o uso de macros estende o rastreamento para incluir conversões baseadas em cliques quando não há suporte para cookies de terceiros. A prática recomendada é adicionar as macros nas seções a seguir às tags de anúncio para capturar dados de click-through adicionais que não são capturados pelo código JavaScript.

>[!NOTE]
>
>O código JavaScript é uma solução para rastreamento de cliques somente enquanto os cookies ainda estão disponíveis. Quando os cookies forem descontinuados, será necessário implementar as seguintes macros.

* **Anunciantes cujos sites não usam o [!DNL Analytics for Advertising] Código JavaScript e, em vez disso, dependem de [!DNL Analytics] encaminhamento pelo lado do servidor somente para dados de click-through** (sem dados de view-through): as seguintes macros são necessárias para relatar a atividade de cliques no site orientada por anúncios comprados pelo Adobe Advertising.

## Anexe as macros ao seu [!DNL Google Campaign Manager 360] Anúncios

Dentro de [!DNL Google Campaign Manager 360], anexe ao seguinte parâmetro ao URL da página inicial de cada exibição e anúncio de vídeo: `%pamo=!;`

Você pode especificar o URL da página de aterrissagem de várias maneiras. As instruções para cada opção estão incluídas nas subseções a seguir.

Veja a seguir um exemplo do URL da página inicial formatado com o sufixo.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Se o URL da página de aterrissagem incluir um símbolo de hash (#), o que não é comum, insira o `amo` antes do símbolo de hash.
>* Se nenhum outro parâmetro for incluído após a variável `amo` e adicione um parâmetro (por exemplo, &amp;a=b) depois dele. Exemplo:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurar o sufixo do URL da página inicial no nível do anunciante

1. Consulte a [instruções para abrir as propriedades do anunciante](https://support.google.com/campaignmanager/answer/2829344).
1. No [!UICONTROL Landing page URL suffix] configurações, incluir `%pamo!;` no [!UICONTROL URL suffix] campo.

### Configurar o sufixo do URL da página inicial no nível da campanha

1. Consulte a [instruções para abrir as propriedades da campanha](https://support.google.com/campaignmanager/answer/2838056#set).
1. No [!UICONTROL Landing page URL suffix] configurações, incluir `%pamo!;` no [!UICONTROL URL suffix] campo.

### Configurar o sufixo do URL da página inicial de nível criativo

1. Abra as propriedades criativas.
1. No [!UICONTROL Click tags] configuração, incluir `%pamo!;` no [!UICONTROL Landing page] para a tag de clique.

## Como [!DNL Analytics for Advertising] Macros são expandidas no DSP

No DSP, ao criar um anúncio que inclui a variável [!DNL Analytics for Advertising] parâmetro (`amo`), o `ef_id` e `s_kwcid` as macros são anexadas automaticamente ao URL de clique. A prática recomendada é verificar a tag no DSP para garantir que a `ef_id` e `s_kwcid` macros estão presentes.

Veja a seguir um exemplo de [!DNL Google Campaign Manager 360] [tag ins](https://support.google.com/campaignmanager/answer/6080468) como aparece no DSP.

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

Quando um usuário clica no anúncio, [!DNL Google Campaign Manager 360] visualiza `%pamo` no sufixo do URL e insere dinamicamente o valor de `amo` no URL.

>[!MORELIKETHIS]
>
>* [Visão geral do [!DNL Analytics for Advertising]](overview.md)
>* [IDs de Adobe Advertising usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros para [!DNL Flashtalking] Tags de publicidade](macros-flashtalking.md)
