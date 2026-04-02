---
title: Importar segmentos autenticados manualmente de  [!DNL LiveRamp]
description: Saiba como ativar públicos autenticados por meio do  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 0%

---

# Importar segmentos autenticados manualmente de [!DNL LiveRamp]

*recurso do Beta*

Você pode enviar segmentos [!DNL LiveRamp] autenticados manualmente para a DSP usando o painel [!DNL LiveRamp] [!DNL Connect]. Você pode usar segmentos importados para direcionamento de posicionamento. Para segmentos primários, as taxas são de US$ 0,15 por impressão de anúncio de exibição entregue e US$ 0,25 por impressão de anúncio de vídeo entregue.

O mapeamento de segmentos e o upload de cada trabalho de importação podem levar até sete dias.

<!--
Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Conclua as seguintes etapas no painel [!DNL Connect]:

   1. Ativar o bloco de destino **[!DNL AAC API 1P Onboarding]**.

   1. Definir somente [!DNL Identifier Settings] a **[!DNL Ramp ID]**.

      ![Configurações do identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Se você ainda quiser receber identificadores baseados em cookies, crie um segundo bloco de destino [!DNL AAC API 1P Onboarding] com &quot;[!DNL Cookies]&quot;, &quot;[!DNL IDFA]&quot; e &quot;[!DNL AAID]&quot; selecionados.

   1. Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público-alvo a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se toda a contagem de segmentos foi importada.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo de ID universal](source-manage.md)
>* [conexão com o Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
