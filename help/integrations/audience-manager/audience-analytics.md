---
title: '[!DNL Adobe] [!DNL Audience Analytics] para clientes do Adobe Advertising'
description: Saiba como usar o  [!DNL Adobe] [!DNL Audience Analytics] para casos de uso de publicidade
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] para clientes do Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) é uma integração entre o Adobe Audience Manager e o Adobe Analytics que permite que os clientes do Audience Manager enviem segmentos para o [!DNL Analytics] para obter insights avançados sobre a atividade do site.

Os clientes do Adobe Advertising podem se beneficiar usando o [!DNL Audience Analytics]. A integração permite:

* Envie dados de exposição de Adobe Advertising diretamente para [!DNL Analytics] para determinar o impacto da atividade superior de funil na atividade downstream do site.

* Determine os canais de marketing e pontos de entrada do site a partir de anúncios de exposição superior no funil.

* Organize a integração com [!DNL Analytics for Advertising] para incorporar segmentos demográficos de terceiros do [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) com dados do [!DNL Analytics for Advertising] para obter mais informações sobre perfis de usuário.

  O [!DNL Audience Marketplace] fornece acesso a feeds de dados de terceiros com modelos de assinatura de &quot;Ativação&quot;, que permitem aos compradores enviar dados para um destino. Se os dados forem usados em um destino [!DNL Analytics], as taxas de ativação não serão aplicadas.

* (Anunciantes com o Advertising DSP) Adicione segmentos de exposição adicionais para obter insights holísticos de gerenciamento de jornadas.

  O Advertising DSP pode enviar dados de exposição para o Audience Manager como sinais acionáveis por meio da implementação de pixels Adobe Experience Platform ou Audience Manager de rastreamento de impressão. O encaminhamento dos mesmos dados para [!DNL Analytics] habilita a análise de dados avançada. Consulte &quot;[Visão geral da integração de dados de mídia Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

Para obter mais informações sobre [!DNL Audience Analytics], incluindo seus pré-requisitos e fluxo de trabalho, consulte &quot;[visão geral sobre Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemplos de como usar os dados do [!DNL Audience Analytics] com os dados de Adobe Advertising

A seguir estão exemplos de como você pode usar os dados combinados dentro de [!DNL Analytics] [!DNL Analysis Workspace].

### Veja o impacto da atividade de funil superior na atividade de downstream

Use segmentos de exposição de Audience Manager para ver o impacto da atividade superior do site de funil na atividade downstream do site. Inclua IDs de macro de terceiros ou do Adobe Advertising nos pixels de rastreamento para rastrear o impacto em um nível detalhado, desde o nível da campanha até o nível do site no qual o usuário foi exposto.

Principais benefícios:

* Rastreie a exposição por tipos de funil/anúncio e use o [!DNL Audience Analytics] para determinar as taxas de entrada e as sobreposições com a próxima fase da jornada do cliente.

* Determine o impacto da atividade superior do funil na atividade downstream do site.

* Conecte [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] dados <!-- (which includes the user's last exposure event) --> para determinar uma jornada holística ao site.

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Veja o impacto da atividade superior de funil na atividade downstream do site](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Usar dados de segmento de terceiros do [!DNL Audience Analytics] para análise de perfil de usuário

Use segmentos de Audience Manager de terceiros para obter uma análise mais avançada de como os usuários estão interagindo com o seu site. Você pode usar as informações para determinar novos públicos de terceiros para os quais ativar mídia, com base em como os perfis dos segmentos de terceiros se envolvem com indicadores-chave de desempenho para os sites das campanhas de mídia.

>[!TIP]
> Use as dimensões Audience Manager `Audiences ID` e `Audiences Name` em [!DNL Analytics], como qualquer outra dimensão que [!DNL Analytics] coleta.

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Usando segmentos de terceiros para enriquecer a análise do perfil do usuário](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrações de Adobe Advertising com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
