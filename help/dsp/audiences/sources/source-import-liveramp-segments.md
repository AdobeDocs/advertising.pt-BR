---
title: Importar segmentos autenticados manualmente do [!DNL LiveRamp]
description: Saiba mais sobre como ativar públicos autenticados por meio do [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Importar segmentos autenticados manualmente do [!DNL LiveRamp]

*Recurso beta*

Você pode enviar manualmente arquivos [!DNL LiveRamp] segmentos para DSP usando o [!DNL LiveRamp] [!DNL Connect] painel. Você pode usar segmentos importados para direcionamento de posicionamento. Para segmentos primários, as taxas são de US$ 0,15 por impressão de anúncio de exibição entregue e US$ 0,25 por impressão de anúncio de vídeo entregue.

O mapeamento de segmentos e o upload de cada trabalho de importação podem levar até sete dias.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Complete as etapas a seguir na [!DNL Connect] painel:

   1. Ativar o bloco de destino **[!DNL AAC API 1P Onboarding]**.

   1. Definir [!DNL Identifier Settings] para **[!DNL Ramp ID]** somente.

      ![Configurações do identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Se você ainda quiser receber identificadores baseados em cookies, crie um segundo [!DNL AAC API 1P Onboarding] bloco de destino com &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selecionado.

   1. Verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que toda a contagem de segmentos foi importada.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
