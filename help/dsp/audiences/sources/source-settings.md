---
title: Configurações do Audience Source
description: Saiba mais sobre as configurações para fontes de público-alvo.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Configurações do Audience Source

*recurso do Beta*

**[!UICONTROL Data Visibility Level]:** Se os segmentos estão disponíveis para um único anunciante com acesso à conta (*[!UICONTROL Advertiser]*) ou para todos os anunciantes com acesso à conta *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (somente visibilidade no nível do anunciante) O anunciante para o qual os segmentos estão disponíveis. Selecione um na lista de anunciantes com acesso à conta.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] fontes somente) A ID da organização da Adobe Experience Cloud para a conta [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Os tipos de ID para os quais você converterá suas informações de identificação pessoal (PII). Se você selecionar vários tipos, o segmento gerado será preenchido com valores para cada tipo de ID selecionado (como [!DNL RampID] e [!DNL Unified ID2.0] para cada endereço de email). Os encargos de dados são aplicados de acordo.

Para [!DNL RampID] e [!DNL Unified ID2.0], o fornecedor pesquisa cada endereço de email para ver se uma ID já existe e traduz o endereço para uma ID correspondente quando disponível. Se não houver uma ID para o endereço, ela criará uma nova ID.

>[!NOTE]
>
>Você pode direcionar somente um tipo de ID em uma única inserção. Para testar o desempenho por tipo de ID, [crie um posicionamento separado](/help/dsp/campaign-management/placements/placement-create.md) para cada tipo de ID no segmento.

* *[!DNL RampID]:* Para converter PII em [!DNL RampID]. Você pode usar [!DNL RampIDs] para redirecionar usuários de logon e para [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) medição.

* *[!DNL Unified ID2.0](Beta):* Para converter PII em uma ID [Unified ID 2.0](https://unifiedid.com) para redirecionar usuários de logon.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Os termos do contrato de serviço para converter PII em IDs universais. Você ou outro usuário na conta do DSP deve aceitar os termos uma vez antes de converter os dados em um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta do Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **>**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Somente leitura; gerada automaticamente) A chave de origem que você pode usar para criar uma conexão de destino na plataforma de dados do cliente para enviar públicos para a Advertising DSP. Você pode copiar o valor para a área de transferência para colar nas configurações de conexão de destino ou em um arquivo.

>[!MORELIKETHIS]
>
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Sobre fontes de público-alvo primárias](source-about.md)
>* [Importar manualmente os segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
