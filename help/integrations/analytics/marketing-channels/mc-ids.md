---
title: Uso de IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras
description: Saiba como usar IDs de Adobe Advertising para criar regras de processamento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Uso de IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras de processamento

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

Você pode usar IDs de Adobe Advertising ([ID AMO e ID EF](../ids.md)) para configurar [!DNL Marketing Channels] regras de processamento no Adobe Analytics. Use IDs de Adobe Advertising para regras específicas para suas campanhas de Adobe Advertising.

## A ID do AMO nas Regras de processamento

A ID do AMO é o código de rastreamento principal usado para relatar dados de publicidade de Adobe no [!DNL Analytics]. A ID do AMO é uma concatenação de valores dinâmicos gerenciados pelo Adobe para fornecer relatórios granulares no [!DNL Analytics]. Ele é armazenado em um [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (ID do AMO). A ID do AMO pode ser definida em [!DNL Analytics] de duas formas:

* Rastreamento de click-through: o Adobe Advertising define o `s_kwcid` parâmetro da sequência de consulta em um link e [!DNL Analytics] O seleciona o parâmetro no URL da página inicial quando ocorre um click-through.
* Rastreamento de view-through ([!DNL DSP] Somente ): o Último serviço de evento detecta um view-through no lado do servidor e envia a ID do AMO para [!DNL Analytics]. Nesse caso, o URL não contém um `s_kwcid` parâmetro.

Os valores dinâmicos nas IDs do AMO indicam o canal de marketing que foi rastreado:

* O prefixo na ID do AMO pode ser usado para identificar o canal de nível superior no [!DNL Marketing Channels].

* As frases de caracteres no corpo da ID do AMO indicam um tipo de campanha mais específico.

* O sufixo &quot;vt&quot; está presente para [!DNL DSP] tráfego de view-through e pode ser usado para criar click-through e view-through separados [!DNL DSP] canais.

O restante da ID do AMO pode ser ignorado.

| [!UICONTROL AMO ID] | Canal | Lógica da regra |
|--------|---------|--------------------|
| AL! (prefixo) | [!UICONTROL Paid Search] | Começa com |
| AC! (prefixo) | [!UICONTROL DSP] | Começa com |
| !g! (corpo) | [!UICONTROL Google Search] | Contém |
| !s! (corpo) | [!UICONTROL Search Partner] | Contém |
| !d! (corpo) | [!UICONTROL Display Network] | Contém |
| !u! (corpo) | [!UICONTROL Smart Shopping Campaign] | Contém |
| !ytv! (corpo) | [!UICONTROL YouTube Video Ad] | Contém |
| !sim! (corpo) | [!UICONTROL YouTube Search Ad] | Contém |
| !vp! (corpo) | [!UICONTROL Google Video Partners] | Contém |
| !vt (sufixo) | [!UICONTROL DSP View-through] | Termina com |

### Exemplos de regras de processamento que usam a ID do AMO

A variável [!DNL Marketing Channels] regra de processamento para o [!UICONTROL Paid Search] o canal pode ter esta aparência:

![Exemplo de a [!UICONTROL Paid Search] regra](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

A variável [!DNL Marketing Channels] regra de processamento para o [!UICONTROL YouTube Video Ads] o canal pode ter esta aparência:

![Exemplo de a [!UICONTROL YouTube Video Ads] regra](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Certifique-se de executar as regras em ordem de especificidade. Se as duas regras acima forem executadas em ordem, a variável [!DNL YouTube] o tráfego de anúncio de vídeo se enquadra no [!UICONTROL Paid Search] canal porque a ID do AMO começaria com &quot;AL!&quot; e contêm &quot;!ytv!&quot;.

## A ID EF nas Regras de Processamento

A EF ID do AMO (EF ID) é o segundo código de rastreamento usado no [!DNL Analytics for Advertising] integração. Seu objetivo principal é rastrear e transmitir [!DNL Analytics] dados do evento na Adobe Advertising. Sempre que ocorrer um click-through ou um view-through, é gerado um único ID EF, mesmo que seja exatamente o mesmo anúncio para o mesmo visitante. A ID EF não é utilizada na variável [!DNL Analytics] interface de usuário de relatórios porque geralmente excede o limite de 500.000 valores únicos por variável em [!DNL Analytics], tornando-o inutilizável para relatórios. As métricas e os metadados de Adobe Advertising não são aplicados à ID EF; são aplicados apenas à ID AMO. A granularidade adicional do rastreamento é necessária para a otimização da campanha no Adobe Advertising, portanto, ambas as IDs são necessárias.

Embora a dimensão EF ID não seja usada diretamente no [!DNL Analytics] relatório, a EF ID pode ser útil na criação de canais de marketing. O sufixo da ID EF indica o canal (exibição ou pesquisa) e se a visita foi orientada por um click-through ou um view-through. O delimitador na EF ID é um sinal de dois pontos, em vez do ponto de exclamação na AMO ID.

| Sufixo da ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemplos de Regras de Processamento que Utilizam a EF ID

#### Exibir Regra de Click-through

Crie um canal de marketing click-through de exibição ao capturar somente click-throughs. Como a ID do AMO é a mesma para click-throughs e view-throughs, esta regra usa a variável ID do EF e a variável `ef_id` parâmetro da sequência de consulta.

Às vezes, os click-throughs são rastreados pelo URL (o padrão). Em outros casos, os click-throughs são rastreados por meio do Último serviço de evento no lado do servidor e, portanto, o URL não contém o `ef_id` parâmetro. A regra verifica, portanto, as condições em que a variável EF ID ou o `ef_id` o parâmetro da sequência de consulta termina com &quot;:d&quot;. Use o &quot;`Any`&quot; porque você deseja que essa regra seja acionada para qualquer condição.

![Exemplo de uma regra de click-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Exibir Regra de View-through

Para criar um canal de view-through de Exibição, crie uma regra em que a ID de EF termine com &quot;:i&quot;. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui a variável `ef_id` ou `s_kwcid` no URL, para que a regra exija apenas uma condição.

![Exemplo de uma regra view-through de exibição](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Fundamentos da [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por que os dados de canal podem variar entre anúncios de Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usar [!DNL Analytics Marketing Channels] com dados de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: usar [!DNL Marketing Channels] para Relatórios de publicidade do Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [IDs de publicidade do Adobe usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
