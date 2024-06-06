---
title: Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID
description: Saiba como criar e gerenciar uma fonte para importar públicos da plataforma de dados do cliente e convertê-los em segmentos que contêm IDs universais.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 9411089703ce0b9502c1c2522cce999c3a5fafbf
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID

*Recurso beta*

Crie uma fonte no DSP para cada público-alvo primário na plataforma de dados do cliente que você deseja converter em segmentos que contêm tipos de ID universal especificados. Você pode importar os segmentos para a conta DSP de sua organização ou para uma conta de anunciante. Os encargos de dados são aplicados com base nos tipos de ID universal selecionados. Depois de criar uma origem, etapas adicionais são necessárias para assimilar os públicos-alvo de cada plataforma de dados do cliente. Consulte a nota no final do procedimento para criar uma origem.

Posteriormente, você pode alterar os tipos de ID universal para os quais o público-alvo de origem é traduzido e exibir um log das alterações.

Você também pode excluir uma origem.

## Criar uma fonte de público-alvo

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clique em **[!UICONTROL Add Source]**.

1. No [!UICONTROL Select a Type] selecione a plataforma de dados do cliente:

   * *[!UICONTROL RT-CDP]*: [A variável [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: A variável [[!DNL ActionIQ] plataforma de dados do cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Somente usuários configurados) A variável [[!DNL Tealium] plataforma de dados do cliente](source-about.md).

1. Especifique a [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Insira o restante [configurações de origem](#source-settings).

   Manter uma cópia do [!UICONTROL Source Key] que é gerado. Você precisará do valor mais tarde.

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Depois de criar uma fonte para a plataforma de dados do cliente, será necessário concluir as etapas adicionais. Consulte a [fluxo de trabalho para importar públicos-alvo do [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e a variável [fluxo de trabalho para importar públicos-alvo do [!DNL Tealium]](source-tealium.md).

## Alterar os Tipos de ID para uma Fonte de público-alvo

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Mantenha o cursor sobre a linha de origem e clique em **[!UICONTROL Edit]**.

1. Altere o [IDs selecionadas para a origem](#source-settings).

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

## Configurações de fonte de público {#source-settings}

**[!UICONTROL Data Visibility Level]:** Se os segmentos estão disponíveis para um único anunciante com acesso à conta (*[!UICONTROL Advertiser]*) ou a todos os anunciantes com acesso à conta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Somente visibilidade no nível do anunciante) O anunciante para o qual os segmentos estão disponíveis. Selecione um na lista de anunciantes com acesso à conta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] (somente fontes) A ID da organização da Adobe Experience Cloud para o [!DNL Adobe Experience Platform] conta.

**[!UICONTROL Convert PII to the following IDs]:** Os tipos de ID para os quais você converterá suas informações de identificação pessoal (PII). Se você selecionar vários tipos, o segmento gerado será preenchido com valores para cada tipo de ID selecionado (como [!DNL RampID] e uma [!DNL Unified ID2.0] para cada endereço de email). Os encargos de dados são aplicados de acordo.

Para [!DNL RampID] e [!DNL Unified ID2.0], o fornecedor pesquisa cada endereço de email para ver se uma ID já existe e traduz o endereço para uma ID correspondente, quando disponível. Se não houver uma ID para o endereço, ela criará uma nova ID.

>[!NOTE]
>
>Você pode direcionar somente um tipo de ID em uma única inserção. Para testar o desempenho por tipo de ID, [criar um posicionamento separado](/help/dsp/campaign-management/placements/placement-create.md) para cada tipo de ID no segmento.

* *[!DNL RampID]:* Para converter PII em um [!DNL RampID]. Você pode usar [!DNL RampIDs] para redirecionar usuários de login e para [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) medição.

* *[!DNL Unified ID2.0](Beta)* Para converter PII em um [ID unificada 2.0](https://unifiedid.com) ID para redirecionar usuários conectados.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Os termos do contrato de serviço para converter PII em IDs universais. Você ou outro usuário na conta do DSP deve aceitar os termos uma vez antes de converter os dados em um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta do Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **>**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Somente leitura; gerado automaticamente) A chave de origem que você pode usar para criar uma conexão de destino na plataforma de dados do cliente para encaminhar públicos-alvo para o DSP de publicidade. Você pode copiar o valor para a área de transferência para colar nas configurações de conexão de destino ou em um arquivo.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
