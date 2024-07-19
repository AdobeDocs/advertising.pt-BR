---
title: Por que os dados de canal podem variar entre Adobe Advertising e  [!DNL Marketing Channels]
description: Saiba por que os dados de canal rastreados pela ID do AMO podem variar dos dados de canal rastreados pelo  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Por que os dados de canal podem variar entre Adobe Advertising e [!DNL Marketing Channels]

*Anunciantes com uma Integração Adobe Advertising-Adobe Analytics Somente*

Uma pergunta comum dos usuários que estão aprendendo sobre a integração do Adobe Advertising e dos conjuntos de dados [!DNL Marketing Channels] é &quot;O que causa a variação nos dados entre a ID do AMO e [!DNL Marketing Channels]?&quot; Ou, às vezes, &quot;Por que os dados são quebrados? Preciso que todas as métricas correspondam aos relatórios.&quot; Felizmente, as discrepâncias não indicam que os dados estão &quot;quebrados&quot;, e as discrepâncias são esperadas e até desejadas. Vamos analisar por que a integração foi projetada dessa maneira.

Os dois conjuntos de dados têm casos de uso principais diferentes:

* [!DNL Marketing Channels]: o principal caso de uso para [!DNL Marketing Channels] é comparar dados entre vários canais com um modelo de atribuição comum. Os analistas podem usar a dimensão [!UICONTROL Marketing Channel] para obter mais informações sobre como os canais estão interagindo entre si. Esse insight pode ajudar a alimentar decisões de nível macro sobre como investir em cada canal e pode levar a insights sobre como os visitantes de cada canal interagem com o site.

  A dimensão [!DNL Analytics] [!UICONTROL Marketing Channel], portanto, está configurada para capturar e rastrear todos os canais. O [!DNL Marketing Channels] também pode ser configurado para capturar view-throughs e click-throughs do Advertising DSP, e isso em relação aos outros canais de marketing.

* ID do AMO do Adobe Advertising: o principal caso de uso dos dados da ID do AMO do Adobe Advertising é para alimentar os algoritmos de lances avançados alimentados pelo [!DNL Adobe Sensei]. Os algoritmos fazem automaticamente milhares de decisões de lances de nível micro feitas diariamente para maximizar os gastos com publicidade e atingir as metas da campanha [!DNL DSP] ou do portfólio [!DNL Search, Social, & Commerce]. Quanto mais dados de conversão os algoritmos puderem conectar campanhas ao, melhor os algoritmos poderão tomar essas decisões de lance.

  Para coletar esses dados, a integração do [!DNL Analytics for Advertising] passa IDs AMO brutas que podem ser traduzidas como códigos de rastreamento de click-through e view-through na dimensão da ID AMO do Adobe Analytics — que é armazenada como uma variável personalizada (eVar) ou uma variável reservada (rVar). Os click-throughs para outros canais não estão definidos na dimensão da ID do AMO, portanto, a dimensão da ID do AMO não pode rastrear a entrada desses outros canais. O resultado é que a ID do AMO persiste através de [!DNL Marketing Channels] pontos de entrada.

Para obter mais informações sobre possíveis variações de dados entre dados rastreados por Adobe Advertising e dados rastreados por [!DNL Analytics], consulte &quot;[Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variações de Dados Esperadas Entre [!DNL Analytics] e Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Usando IDs de Adobe Advertising para Criar [!DNL Marketing Channels] Regras de Processamento](mc-ids.md)
>* [Usando [!DNL Analytics Marketing Channels] com Dados Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para Relatórios de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
