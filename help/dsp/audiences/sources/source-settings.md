---
title: Configurações de fonte de público
description: Saiba mais sobre as configurações para fontes de público-alvo.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Configurações de fonte de público

**[!UICONTROL Data Visibility Level]:** Se os segmentos estão disponíveis para um único anunciante com acesso à conta (*[!UICONTROL Advertiser]*) ou a todos os anunciantes com acesso à conta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Somente visibilidade no nível do anunciante) O anunciante para o qual os segmentos estão disponíveis. Selecione um na lista de anunciantes com acesso à conta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] (somente fontes) A ID da organização da Adobe Experience Cloud para o [!DNL Adobe Experience Platform] conta.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] e [!DNL Tealium] (Somente fontes da ) O tipo de ID para a qual você deseja converter suas informações de identificação pessoal (PII). Os encargos de dados são aplicados de acordo.

* *[!DNL RampID]:* Para converter PII em um RampID. Se você escolher *[!DNL RampID]*, seus segmentos são traduzidos em [!DNL RampIDs] automaticamente.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] apenas origens) Para converter PII em um [ID unificada 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Somente leitura; gerado automaticamente) A chave de origem que você pode usar para criar uma conexão de destino na plataforma de dados do cliente para encaminhar públicos-alvo para o DSP de publicidade. Você pode copiar o valor para a área de transferência para colar nas configurações de conexão de destino ou em um arquivo.

>[!MORELIKETHIS]
>
>* [Criar uma fonte de público-alvo para ativar públicos-alvo primários](source-create.md)
>* [Sobre a ativação de segmentos autenticados de fontes de público-alvo](source-about.md)
>* [Ativar segmentos autenticados de parceiros de ID universal](source-universal-id.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
