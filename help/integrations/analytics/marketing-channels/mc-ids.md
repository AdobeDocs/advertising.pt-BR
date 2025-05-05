---
title: Usando IDs de Adobe Advertising para criar  [!DNL Marketing Channels] Regras
description: Saiba como usar IDs de Adobe Advertising para criar regras de processamento para  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Usando IDs de Adobe Advertising para criar Regras de Processamento do [!DNL Marketing Channels]

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

Você pode usar Adobe Advertising IDs ([AMO ID e EF ID](../ids.md)) para configurar [!DNL Marketing Channels] regras de processamento no Adobe Analytics. Use IDs de Adobe Advertising para regras específicas para suas campanhas de Adobe Advertising.

## A ID do AMO nas Regras de processamento

A ID do AMO é o código de rastreamento primário usado para reportar dados de Adobe Advertising em [!DNL Analytics]. A ID do AMO é uma concatenação de valores dinâmicos gerenciados pelo Adobe para fornecer relatórios granulares no [!DNL Analytics]. Ele está armazenado em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=pt-BR) ou em uma dimensão rVar (AMO ID). A ID do AMO pode ser definida em [!DNL Analytics] de duas maneiras:

* Rastreamento de click-through: o Adobe Advertising define o parâmetro da sequência de consulta `s_kwcid` em um link e o [!DNL Analytics] seleciona o parâmetro da URL da página de aterrissagem quando ocorre um click-through.
* Rastreamento de view-through (Somente [!DNL DSP]): o Último Serviço de Evento detecta uma view-through no lado do servidor e envia a ID do AMO para [!DNL Analytics]. Nesse caso, a URL não contém um parâmetro `s_kwcid`.

Os valores dinâmicos nas IDs do AMO indicam o canal de marketing que foi rastreado:

* O prefixo na ID do AMO pode ser usado para identificar o canal de nível superior em [!DNL Marketing Channels].

* As frases de caracteres no corpo da ID do AMO indicam um tipo de campanha mais específico.

* O sufixo &quot;vt&quot; está presente para o tráfego de view-through [!DNL DSP] e pode ser usado para criar canais de click-through e view-through [!DNL DSP] separados.

O restante da ID do AMO pode ser ignorado.

| [!UICONTROL AMO ID] | Canal | Lógica da regra |
|--------|---------|--------------------|
| !ctv (sufixo) | [!UICONTROL DSP Connected TV View-through] | Termina com |
| !d! (corpo) | [!UICONTROL Display Network] | Contém |
| !g! (corpo) | [!UICONTROL Google Search] | Contém |
| !s! (corpo) | [!UICONTROL Search Partner] | Contém |
| !u! (corpo) | [!UICONTROL Smart Shopping Campaign] | Contém |
| !ytv! (corpo) | [!UICONTROL YouTube Video Ad] | Contém |
| !sim! (corpo) | [!UICONTROL YouTube Search Ad] | Contém |
| !vp! (corpo) | [!UICONTROL Google Video Partners] | Contém |
| !vt (sufixo) | [!UICONTROL DSP View-through] | Termina com |
| AL! (prefixo) | [!UICONTROL Paid Search] | Começa com |
| AC! (prefixo) | [!UICONTROL DSP] | Começa com |

### Exemplos de regras de processamento que usam a ID do AMO

A regra de processamento [!DNL Marketing Channels] para o canal [!UICONTROL Paid Search] pode ter esta aparência:

![Exemplo de uma regra [!UICONTROL Paid Search]](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

A regra de processamento [!DNL Marketing Channels] para o canal [!UICONTROL YouTube Video Ads] pode ter esta aparência:

![Exemplo de uma regra [!UICONTROL YouTube Video Ads]](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Certifique-se de executar as regras em ordem de especificidade. Se as duas regras acima fossem executadas em ordem, o tráfego de anúncio de vídeo [!DNL YouTube] ficaria no canal [!UICONTROL Paid Search], pois a ID do AMO começaria com &quot;AL!&quot; e contêm &quot;!ytv!&quot;.

## A ID EF nas Regras de Processamento

A EF ID do AMO (EF ID) é o segundo código de rastreamento usado na integração do [!DNL Analytics for Advertising]. Seu objetivo principal é rastrear e transmitir dados do evento [!DNL Analytics] para o Adobe Advertising. Sempre que ocorrer um click-through ou um view-through, é gerado um único ID EF, mesmo que seja exatamente o mesmo anúncio para o mesmo visitante. A ID de EF não é usada na interface do usuário de relatórios [!DNL Analytics] porque geralmente excede os 500k valores únicos por limite de variável em [!DNL Analytics], tornando-a inutilizável para relatórios. As métricas e os metadados de Adobe Advertising não são aplicados à ID EF; são aplicados apenas à ID AMO. A granularidade adicional do rastreamento é necessária para a otimização da campanha no Adobe Advertising, portanto, ambas as IDs são necessárias.

Embora a dimensão EF ID não seja usada diretamente nos relatórios [!DNL Analytics], a EF ID pode ser útil na criação de canais de marketing. O sufixo da ID EF indica o canal (exibição ou pesquisa) e se a visita foi orientada por um click-through ou um view-through. O delimitador na EF ID é um sinal de dois pontos, em vez do ponto de exclamação na AMO ID.

| Sufixo da ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemplos de Regras de Processamento que Utilizam a EF ID

#### Exibir Regra de Click-through

Crie um canal de marketing click-through de exibição ao capturar somente click-throughs. Como a ID do AMO é a mesma para click-throughs e view-throughs, essa regra usa a variável EF ID e o parâmetro de sequência de consulta `ef_id`.

Às vezes, os click-throughs são rastreados pelo URL (o padrão). Em outros casos, os click-throughs são rastreados pelo Último Serviço de Evento no lado do servidor e, portanto, a URL não contém o parâmetro `ef_id`. A regra, portanto, verifica as condições em que a variável EF ID ou o parâmetro de cadeia de caracteres de consulta `ef_id` termina com &quot;:d&quot;. Use o operador &quot;`Any`&quot; porque você deseja que essa regra seja acionada para qualquer uma das condições.

![Exemplo de uma regra de click-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Exibir Regra de View-through

Para criar um canal de view-through de Exibição, crie uma regra em que a ID de EF termine com &quot;:i&quot;. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui o `ef_id` ou `s_kwcid` na URL, portanto, a regra requer apenas uma condição.

![Exemplo de uma regra de view-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por que os dados de canal podem variar entre Adobe Advertising e  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] com Dados Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para Relatórios de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=pt-BR)
>* [IDs de Adobe Advertising Usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
