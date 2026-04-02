---
title: Por que os dados do canal podem variar entre o Adobe Advertising e o  [!DNL Marketing Channels]
description: Saiba por que os dados de canal rastreados pela ID do AMO podem variar dos dados de canal rastreados pelo  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
TQID: https://experienceleague.adobe.com/zzYKrbiwvW9Ysf7baDfKGsETmSvYbXDY7-lIygorXH8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Por que os dados do canal podem variar entre o Adobe Advertising e o [!DNL Marketing Channels]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Uma pergunta comum dos usuários que estão aprendendo sobre a integração do Adobe Advertising e dos conjuntos de dados do [!DNL Marketing Channels] é &quot;O que causa a variação nos dados entre a ID do AMO e o [!DNL Marketing Channels]?&quot; Ou, às vezes, &quot;Por que os dados são quebrados? Preciso que todas as métricas correspondam aos relatórios.&quot; Felizmente, as discrepâncias não indicam que os dados estão &quot;quebrados&quot;, e as discrepâncias são esperadas e até desejadas. Vamos ver por que a integração foi projetada dessa maneira.

Os dois conjuntos de dados têm casos de uso principais diferentes:

* [!DNL Marketing Channels]: o principal caso de uso para [!DNL Marketing Channels] é comparar dados entre vários canais com um modelo de atribuição comum. Os analistas podem usar a dimensão [!UICONTROL Marketing Channel] para obter mais informações sobre como os canais estão interagindo entre si. Este insight pode ajudar a alimentar decisões de nível macro sobre como investir em cada canal e pode levar a insights sobre como os visitantes de cada canal interagem com o site.

  A dimensão [!DNL Analytics] [!UICONTROL Marketing Channel], portanto, está configurada para capturar e rastrear todos os canais. O [!DNL Marketing Channels] também pode ser configurado para capturar view-throughs e click-throughs do Advertising DSP, e isso em relação aos outros canais de marketing.

* Adobe Advertising AMO ID: o principal caso de uso dos dados do Adobe Advertising AMO ID é para alimentar os algoritmos de lances avançados viabilizados pelo [!DNL Adobe AI]. Os algoritmos fazem automaticamente milhares de decisões de lances de nível micro feitas diariamente para maximizar os gastos com publicidade e atingir as metas da campanha [!DNL DSP] ou do portfólio [!DNL Search, Social, & Commerce]. Quanto mais dados de conversão os algoritmos puderem conectar campanhas ao, melhor os algoritmos poderão tomar essas decisões de lance.

  Para coletar esses dados, a integração do [!DNL Analytics for Advertising] passa IDs AMO brutas que podem ser traduzidas como códigos de rastreamento de click-through e view-through na dimensão da ID AMO do Adobe Analytics — que é armazenada como uma variável personalizada (eVar) ou uma variável reservada (rVar). Os click-throughs para outros canais não estão definidos na dimensão da ID do AMO, portanto, a dimensão da ID do AMO não pode rastrear a entrada desses outros canais. O resultado é que a ID do AMO persiste através de [!DNL Marketing Channels] pontos de entrada.

Para obter mais informações sobre possíveis variações de dados entre dados rastreados pelo Adobe Advertising e dados rastreados pelo [!DNL Analytics], consulte &quot;[Variações de dados esperadas entre [!DNL Analytics] e o Adobe Advertising](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Variações de dados esperadas entre [!DNL Analytics] e Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Usando Adobe Advertising IDs para criar [!DNL Marketing Channels] regras de processamento](mc-ids.md)
>* [Usando [!DNL Analytics Marketing Channels] com dados do Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para relatórios do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=pt-BR)
