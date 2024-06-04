---
title: Criar uma fonte de público-alvo para ativar públicos-alvo da Universal ID
description: Saiba como criar uma fonte para importar públicos-alvo da plataforma de dados do cliente e convertê-los em segmentos que contêm IDs universais.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Criar uma fonte de público-alvo para ativar públicos-alvo da Universal ID

*Recurso beta*

Crie uma fonte no DSP para cada público-alvo primário na plataforma de dados do cliente que você deseja converter em segmentos que contêm tipos de ID universal especificados. Você pode importar os segmentos para a conta DSP de sua organização ou para uma conta de anunciante. Os encargos de dados são aplicados com base nos tipos de ID universal selecionados.

Etapas adicionais são necessárias para assimilar os públicos-alvo de cada plataforma de dados do cliente. Consulte a nota no final do procedimento.

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clique em **[!UICONTROL Add Source]**.

1. No [!UICONTROL Select a Type] selecione a plataforma de dados do cliente:

   * *[!UICONTROL RT-CDP]*: [A variável [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: A variável [[!DNL ActionIQ] plataforma de dados do cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Somente usuários configurados) A variável [[!DNL Tealium] plataforma de dados do cliente](source-about.md).

1. Especifique a [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Insira o restante [configurações de origem](source-settings.md).

   Manter uma cópia do [!UICONTROL Source Key] que é gerado. Você precisará do valor mais tarde.

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Depois de criar uma fonte para a plataforma de dados do cliente, será necessário concluir as etapas adicionais. Consulte a [fluxo de trabalho para importar públicos-alvo do [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e a variável [fluxo de trabalho para importar públicos-alvo do [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Configurações de fonte de público](source-settings.md)
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Conexão com o Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
