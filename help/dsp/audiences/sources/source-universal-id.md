---
title: Ativar segmentos autenticados de parceiros de ID universal
description: Saiba mais sobre como ativar públicos autenticados por meio de uma solução de ID universal.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: e9ff454428d0256402a2ef2fa74f8bd45bd7592f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Ativar segmentos autenticados de parceiros de ID universal

Para ativar públicos autenticados por meio de uma solução de ID universal no DSP do Advertising, os segmentos devem ser traduzidos em [!DNL RampIDs], que são reconhecíveis em um ambiente licitável. Você pode fazer isso das seguintes maneiras:

* Aproveitar a integração do DSP com o [!DNL Adobe Real-Time Customer Data Platform (CDP)] e a variável [!DNL Adobe-LiveRamp Retrieval API].

* Envio manual de segmentos autenticados para DSP do [!DNL LiveRamp] [!DNL Connect] painel.

## Tarefas

1. Para qualquer uma das opções, entre em contato com `adcloud-support@adobe.com` para ativar as seguintes configurações no DSP, que permitirão direcionar segmentos autenticados em campanhas DSP uma vez [todas as etapas do fluxo de trabalho de ativação foram concluídas](source-adobe-rtcdp.md):

   1. [!DNL LiveRamp] [!DNL RampID] configuração da campanha antes do compartilhamento do segmento a partir de [!DNL Real-Time CDP].

   1. O nível da conta &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Usuários compartilham segmentos autenticados manualmente do [!DNL LiveRamp]) Complete as etapas a seguir na [!DNL LiveRamp] [!DNL Connect] painel:

   1. Ativar o bloco de destino **[!DNL AAC API 1P Onboarding]**.

   1. Definir [!DNL Identifier Settings] para **[!DNL Ramp ID]** somente.

      ![Configurações do identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Se você ainda quiser receber identificadores baseados em cookies, crie um segundo [!DNL AAC API 1P Onboarding] bloco de destino com &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selecionado.

## Práticas recomendadas para testes e validação de dados

* **Target [!DNL RampID]Segmentos com base em e segmentos com base em cookies em campanhas separadas.**

   * As configurações de campanha permitem que apenas um identificador seja priorizado.

   * Atualmente, [!DNL RampIDs] não são recuperáveis durante eventos no site. Isso significa que determinadas metas personalizadas, como CPA mais baixo e ROAS, não estão disponíveis com o uso de segmentos autenticados. Use segmentos baseados em cookies somente se você tiver um KPI de desempenho restritivo.

* **Criar uma disposição em ambas as [!DNL RampID] e campanhas baseadas em cookies.**

   * Direcionar os segmentos que são compartilhados a partir do [!DNL LiveRamp] usando o processo de ativação de segmento padrão.

   * Trabalhe com a equipe de suporte do Adobe Advertising para validar a distribuição de dados adequada.

Para saber mais sobre a integração do DSP com o [!DNL LiveRamp], entre em contato `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre a ativação de segmentos autenticados de fontes de público-alvo](source-about.md)
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
