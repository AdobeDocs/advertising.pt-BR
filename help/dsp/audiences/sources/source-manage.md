---
title: Criar e gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID
description: Saiba como criar e gerenciar uma fonte para importar públicos da plataforma de dados do cliente e convertê-los em segmentos que contêm IDs universais.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Criar uma fonte de público-alvo para ativar públicos-alvo da Universal ID

*Recurso beta*

Crie uma fonte no DSP para cada público-alvo primário na plataforma de dados do cliente que você deseja converter em segmentos que contêm tipos de ID universal especificados. Você pode importar os segmentos para a conta DSP de sua organização ou para uma conta de anunciante. Os encargos de dados são aplicados com base nos tipos de ID universal selecionados.

Etapas adicionais são necessárias para assimilar os públicos-alvo de cada plataforma de dados do cliente. Consulte a nota no final do procedimento.

## Criar uma fonte de público-alvo

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

## Alterar os Tipos de ID para uma Fonte de público-alvo

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL Edit]**.

1. Altere o [IDs selecionadas para a origem](source-settings.md).

1. Clique em **[!UICONTROL Save]**.

## Excluir uma fonte de público-alvo

Excluir uma origem remove os segmentos convertidos pela origem.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Exibir o log de alterações de uma origem de público-alvo

Você pode exibir detalhes sobre alterações em um registro de origem de público-alvo e, opcionalmente, anexar observações ao log.

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL Change log]**.

1. (Opcional) Para anexar uma nota ao log de alterações:

   1. Mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL Add Notes]**.

   1. Insira a nota e clique em **[!UICONTROL Save]**.

      O comprimento máximo é de 256 caracteres.

1. (Opcional) Para abrir o log em uma tela de detalhes maior, mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL View Details]**.

>[!MORELIKETHIS]
>
>* [Configurações de fonte de público](source-settings.md)
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Conexão com o Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
