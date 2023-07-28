---
title: Implementar [!DNL Google Ads] campanhas de desempenho máximo do
description: Saiba mais sobre o fluxo de trabalho para configuração [!DNL Google Ads] desempenho máximo de campanhas.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] campanhas de desempenho máximo do

Entrada [!DNL Google Ads] desempenho máximo de campanhas, você não configura grupos de anúncios, anúncios ou palavras-chave. Em vez disso, nas configurações da campanha, você especifica um ou mais grupos de ativos, que incluem títulos, descrições e imagens, logotipos e [!DNL YouTube videos]. [!DNL Google Ads] combina automaticamente os ativos para veicular anúncios com base no canal (como [!DNL YouTube], [!DNL Gmail]ou [!DNL Search]).

Você pode visualizar suas campanhas de desempenho máximo existentes, com dados de desempenho no formato de tabela e gráfico de tendências, no [!DNL Campaigns] view; os dados não estão disponíveis em níveis inferiores. Os dados de desempenho no nível de campanha também estão disponíveis nos relatórios e no Adobe Analytics (para anunciantes com uma [Integração do Analytics](/help/integrations/analytics/overview.md). Para exibir dados de desempenho para campanhas de desempenho máximo no [!DNL Analytics], a campanha deve usar o [código de rastreamento s_kwcid atualizado](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) (que rastreia a ID da campanha e a ID do grupo de publicidade).

>[!NOTE]
>
>* Você deve carregar manualmente todos os arquivos de imagem. Links para [!DNL Google Merchant Center] os feeds de produto do não são compatíveis.
>* Somente as configurações necessárias estão disponíveis. Para configurações opcionais, faça logon na [!DNL Google Ads] editor.
>* Não há suporte disponível para a listagem de grupos. Para gerenciar e exibir dados de grupos de listagem, efetue logon na [!DNL Google Ads] editor.

## Etapas para configurar [!DNL Google Ads] campanhas de desempenho máximo do

Você pode configurar campanhas de desempenho máximo do individualmente na [!UICONTROL Campaigns] > [!UICONTROL Campaigns] exibição.

1. [Criar uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) com tipo de campanha **[!UICONTROL Performance Max]**.

   Especifique a [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], e [!UICONTROL URL Options]. Opcionalmente, informe [!UICONTROL Negative Keywords], insira [!UICONTROL Negative Websites]e/ou substituir o [!UICONTROL Campaign Tracking] opções.

1. Criar grupos de ativos e fazer upload de ativos para a campanha:

   1. Na parte inferior das configurações da campanha, clique em **[!UICONTROL Manage Asset Groups]**.

   1. Especifique as configurações para o primeiro grupo de ativos e faça upload das imagens, logotipos e vídeos opcionais para o grupo de ativos.

      Consulte [descrições das configurações do grupo de ativos](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) para compreender os requisitos e as especificações.

   1. Adicione grupos de ativos adicionais, conforme necessário.

1. Clique em **[!UICONTROL Post]**.

1. (Opcional) Adicione a campanha a um portfólio híbrido para otimização.
