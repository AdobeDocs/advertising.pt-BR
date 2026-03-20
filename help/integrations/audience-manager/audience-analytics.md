---
title: '[!DNL Adobe] [!DNL Audience Analytics] para clientes do Adobe Advertising'
description: Saiba como usar o  [!DNL Adobe] [!DNL Audience Analytics] para casos de uso de publicidade
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] para clientes do Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) é uma integração entre o Adobe Audience Manager e o Adobe Analytics que permite aos clientes do Audience Manager enviar segmentos para o [!DNL Analytics] para obter insights avançados sobre a atividade do site.

Os clientes da Adobe Advertising podem se beneficiar usando o [!DNL Audience Analytics]. A integração permite:

* Envie dados de exposição do Adobe Advertising diretamente para [!DNL Analytics] para determinar o impacto da atividade superior do funnel na atividade downstream do site.

* Determine os canais de marketing e os pontos de entrada do site a partir dos anúncios de exposição superiores da funnel.

* Organize a integração com [!DNL Analytics for Advertising] para incorporar segmentos demográficos de terceiros do [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) com dados do [!DNL Analytics for Advertising] para obter mais informações sobre perfis de usuário.

  O [!DNL Audience Marketplace] fornece acesso a feeds de dados de terceiros com modelos de assinatura de &quot;Ativação&quot;, que permitem aos compradores enviar dados para um destino. Se os dados forem usados em um destino [!DNL Analytics], as taxas de ativação não serão aplicadas.

* (Anunciantes com o Advertising DSP) Adicione segmentos de exposição adicionais para obter insights holísticos de gerenciamento de jornadas.

  O Advertising DSP pode enviar dados de exposição para o Audience Manager como sinais acionáveis por meio da implementação de pixels de rastreamento de impressão Adobe Experience Platform ou Audience Manager. O encaminhamento dos mesmos dados para [!DNL Analytics] habilita a análise de dados avançada. Consulte &quot;[Visão geral do envio de dados de exposição de mídia do DSP para o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

Para obter mais informações sobre [!DNL Audience Analytics], incluindo seus pré-requisitos e fluxo de trabalho, consulte &quot;[visão geral do Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemplos de como usar os dados do [!DNL Audience Analytics] com os dados do Adobe Advertising

A seguir estão exemplos de como você pode usar os dados combinados dentro de [!DNL Analytics] [!DNL Analysis Workspace].

### Veja o impacto da atividade superior do funnel na atividade downstream

Use segmentos de exposição do Audience Manager para ver o impacto da atividade superior do site do funnel na atividade downstream do site. Inclua IDs de macro do Adobe Advertising ou de terceiros nos pixels de rastreamento para rastrear o impacto em um nível detalhado, desde o nível da campanha até o nível do site no qual o usuário foi exposto.

Principais benefícios:

* Rastreie a exposição por tipos de funnel/anúncio e use o [!DNL Audience Analytics] para determinar as taxas de entrada e a sobreposição com a próxima fase da jornada do cliente.

* Determine o impacto da atividade superior do funnel na atividade downstream do site.

* Conecte dados de [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] para determinar uma jornada holística ao site.

<!-- (which includes the user's last exposure event) -->

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Veja o impacto da atividade superior do funnel na atividade downstream do site](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Usar dados de segmento de terceiros do [!DNL Audience Analytics] para análise de perfil de usuário

Use segmentos do Audience Manager de terceiros para obter uma análise mais avançada de como os usuários estão interagindo com seu site. Você pode usar as informações para determinar novos públicos de terceiros para os quais ativar mídia, com base em como os perfis dos segmentos de terceiros se envolvem com indicadores-chave de desempenho para os sites das campanhas de mídia.

>[!TIP]
> Use as dimensões `Audiences ID` e `Audiences Name` do Audience Manager em [!DNL Analytics], como qualquer outra dimensão que [!DNL Analytics] coleta.

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Usando segmentos de terceiros para enriquecer a análise do perfil do usuário](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrações do Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
