---
title: Por que os dados de canal podem variar entre anúncios de Adobe e [!DNL Marketing Channels]
description: Saiba por que os dados do canal rastreados pela AMO ID podem variar dos dados do canal rastreados por [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Por que os dados de canal podem variar entre anúncios de Adobe e [!DNL Marketing Channels]

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

Uma pergunta comum dos usuários sobre a integração do anúncio de Adobe e [!DNL Marketing Channels] conjuntos de dados é &quot;O que causa a variação nos dados entre a ID do AMO e [!DNL Marketing Channels]?&quot; Ou, às vezes, &quot;Por que os dados são quebrados? Preciso que todas as métricas correspondam aos relatórios.&quot; Felizmente, as discrepâncias não indicam que os dados estão &quot;quebrados&quot;, e as discrepâncias são esperadas e até desejadas. Vamos analisar por que a integração foi projetada dessa maneira.

Os dois conjuntos de dados têm casos de uso principais diferentes:

* [!DNL Marketing Channels]: o principal caso de uso do [!DNL Marketing Channels] é comparar dados em vários canais com um modelo de atribuição comum. Os analistas podem usar o [!UICONTROL Marketing Channel] para obter mais insights sobre como os canais estão interagindo entre si. Esse insight pode ajudar a alimentar decisões de nível macro sobre como investir em cada canal e pode levar a insights sobre como os visitantes de cada canal interagem com o site.

   A variável [!DNL Analytics] [!UICONTROL Marketing Channel] portanto, a dimensão está configurada para capturar e rastrear todos os canais. [!DNL Marketing Channels] O também pode ser configurado para capturar view-throughs e click-throughs de DSP de publicidade, e isso em relação aos outros canais de marketing.

* Adobe Advertising AMO ID: o caso de uso principal dos dados da Adobe Advertising AMO ID é para alimentar o avançado [!DNL Adobe Sensei]algoritmos de lance acionados pelo. Os algoritmos fazem automaticamente milhares de decisões de oferta de nível micro feitas diariamente para maximizar os gastos com publicidade e alcançar os objetivos do [!DNL DSP] campanha ou o [!DNL Search, Social, & Commerce] portfólio. Quanto mais dados de conversão os algoritmos puderem conectar campanhas ao, melhor os algoritmos poderão tomar essas decisões de lance.

   Para coletar esses dados, a variável [!DNL Analytics for Advertising] A integração passa IDs AMO brutas que podem ser traduzidas como códigos de rastreamento de click-through e view-through na dimensão ID do AMO do Adobe Analytics — que é armazenada como uma variável personalizada (eVar) ou uma variável reservada (rVar). Os click-throughs para outros canais não estão definidos na dimensão da ID do AMO, portanto, a dimensão da ID do AMO não pode rastrear a entrada desses outros canais. O resultado é que a ID do AMO persiste até [!DNL Marketing Channels] pontos de entrada.

Para obter mais informações sobre possíveis variações de dados entre os dados rastreados pelo Adobe Advertising e [!DNL Analytics]dados rastreados pelo, consulte &quot;[Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Fundamentos da [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de IDs de publicidade do Adobe para criar [!DNL Marketing Channels] Regras de processamento](mc-ids.md)
>* [Usar [!DNL Analytics Marketing Channels] com dados de publicidade do Adobe](mc-ac-data.md)
>* [Vídeo: usar [!DNL Marketing Channels] para Relatórios de publicidade do Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

