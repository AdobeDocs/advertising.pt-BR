---
title: Configurações de fonte de público
description: Saiba mais sobre as configurações para fontes de público-alvo.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Configurações de fonte de público

*Recurso beta*

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
>* [Criar uma fonte de público-alvo para ativar públicos-alvo da Universal ID](source-create.md)
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
