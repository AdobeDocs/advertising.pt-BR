---
title: Criar uma fonte de público-alvo para ativar públicos-alvo primários
description: Saiba como criar uma fonte para importar públicos para sua conta ou uma conta de anunciante.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Criar uma fonte de público-alvo para ativar públicos-alvo primários

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Crie uma fonte no DSP para importar públicos-alvo primários para sua conta DSP ou para uma conta de anunciante.

Para obter as etapas adicionais necessárias para assimilar segmentos de plataformas de dados específicas do cliente, consulte [os workflows de ativação específicos do público](source-about.md)

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clique em **[!UICONTROL Add Source]**.

1. No [!UICONTROL Select a Type] selecione o tipo de origem.

   * *[!UICONTROL RT-CDP]*: [A variável [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: A variável [[!DNL Tealium] plataforma de dados do cliente](source-about.md).

1. Especifique a [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Insira o restante [configurações de origem](source-settings.md).

   Manter uma cópia do [!UICONTROL Source Key] que é gerado. Você precisará do valor mais tarde.

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Após criar uma origem para sua plataforma de dados do cliente, você deve concluir etapas adicionais. Consulte a [fluxo de trabalho de ativação para [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e a variável [fluxo de trabalho de ativação para [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Configurações de fonte de público](source-settings.md)
>* [Sobre a ativação de segmentos autenticados de fontes de público-alvo](source-about.md)
>* [Ativar segmentos autenticados de parceiros de ID universal](source-universal-id.md)<!-- title?-->
>* [Conexão com o Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
