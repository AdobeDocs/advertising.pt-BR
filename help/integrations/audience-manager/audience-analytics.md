---
title: '''[!DNL Adobe] [!DNL Audience Analytics] para clientes da Adobe Advertising'
description: Saiba como usar o [!DNL Adobe] [!DNL Audience Analytics] para casos de uso de publicidade
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] para clientes da Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) é uma integração entre o Adobe Audience Manager e o Adobe Analytics que permite que os clientes do Audience Manager enviem segmentos para [!DNL Analytics] para obter insights enriquecidos sobre a atividade do site.

Os clientes da Adobe Advertising podem se beneficiar usando [!DNL Audience Analytics]. A integração permite:

* Enviar dados de exposição de publicidade do Adobe diretamente para [!DNL Analytics] para determinar o impacto da atividade superior do funil na atividade downstream do site.

* Determine os canais de marketing e pontos de entrada do site a partir de anúncios de exposição superior no funil.

* Criar camadas de integração com o [!DNL Analytics for Advertising] incorporar segmentos demográficos de terceiros do [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) com [!DNL Analytics for Advertising] para obter mais informações sobre perfis de usuário.

   [!DNL Audience Marketplace] O fornece acesso a feeds de dados de terceiros com modelos de assinatura &quot;Ativation&quot;, que permitem aos compradores enviar dados para um destino. Se os dados forem utilizados em um [!DNL Analytics] destino e, em seguida, as taxas de ativação não serão aplicadas.

* (Anunciantes com DSP publicitário) Adicione segmentos de exposição adicionais para obter insights holísticos de gerenciamento de jornadas.

   O DSP publicitário pode enviar dados de exposição para o Audience Manager como sinais acionáveis por meio da implementação de pixels Adobe Experience Platform ou Audience Manager de rastreamento de impressão. Encaminhamento dos mesmos dados para [!DNL Analytics] permite a análise avançada de dados. Consulte &quot;[Visão geral da integração de dados de mídia de publicidade do Adobe com o Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obter mais informações.

Para obter mais informações sobre [!DNL Audience Analytics], incluindo os pré-requisitos e o fluxo de trabalho, consulte &quot;[visão geral do Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemplos de como usar [!DNL Audience Analytics] Dados com dados de publicidade do Adobe

A seguir estão exemplos de como é possível usar os dados combinados em [!DNL Analytics] [!DNL Analysis Workspace].

### Veja o impacto da atividade de funil superior na atividade de downstream

Use segmentos de exposição de Audience Manager para ver o impacto da atividade superior do site de funil na atividade downstream do site. Inclua anúncios de Adobe ou IDs de macro de terceiros nos pixels de rastreamento para rastrear o impacto em um nível detalhado, desde o nível da campanha até o nível do site no qual o usuário foi exposto.

Principais benefícios:

* Rastrear a exposição por tipos de funil/anúncio e uso [!DNL Audience Analytics] para determinar as taxas de entrada e a sobreposição com a próxima fase da jornada do cliente.

* Determine o impacto da atividade superior do funil na atividade downstream do site.

* Conectar [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] dados <!-- (which includes the user's last exposure event) --> para determinar uma jornada integral ao site.

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Veja o impacto da atividade de funil superior na atividade downstream do site](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Uso [!DNL Audience Analytics] Dados de segmento de terceiros para análise do perfil do usuário

Use segmentos de Audience Manager de terceiros para obter uma análise mais avançada de como os usuários estão interagindo com o seu site. Você pode usar as informações para determinar novos públicos de terceiros para os quais ativar mídia, com base em como os perfis dos segmentos de terceiros se envolvem com indicadores-chave de desempenho para os sites das campanhas de mídia.

>[!TIP]
> Usar o Audience Manager `Audiences ID` e `Audiences Name` dimensões em todo o [!DNL Analytics], como qualquer outra dimensão que [!DNL Analytics] coleta.

Veja a seguir exemplos de relatórios que você pode criar em [!DNL Analysis Workspace].

![Utilização de segmentos de terceiros para enriquecer a análise do perfil do usuário](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrações de publicidade do Adobe com o Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

