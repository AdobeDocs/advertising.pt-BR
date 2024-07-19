---
title: Implementar  [!DNL Google Ads] campanhas de desempenho máximo
description: Saiba mais sobre o fluxo de trabalho para configurar  [!DNL Google Ads] campanhas de desempenho máximo.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementar campanhas de desempenho máximo de [!DNL Google Ads]

Em [!DNL Google Ads] campanhas de desempenho máximo, você não configura grupos de anúncios, anúncios ou palavras-chave. Em vez disso, nas configurações da campanha, você especifica um ou mais grupos de ativos, que incluem títulos, descrições e imagens, logotipos e [!DNL YouTube videos] carregados. O [!DNL Google Ads] combina automaticamente os ativos para veicular anúncios com base no canal (como [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

Você pode visualizar suas campanhas de desempenho máximo existentes, com dados de desempenho em formato de tabela e gráfico de tendências, na visualização [!DNL Campaigns]. Os dados não estão disponíveis em níveis inferiores. Os dados de desempenho no nível de campanha também estão disponíveis nos relatórios e no Adobe Analytics (para anunciantes com uma [integração com o Analytics](/help/integrations/analytics/overview.md). Para exibir dados de desempenho para campanhas de desempenho máximo em [!DNL Analytics], a campanha deve usar o [código de rastreamento de ID do AMO atualizado](/help/integrations/analytics/ids.md#amo-id-formats) (que rastreia a ID da campanha e a ID do grupo de anúncios).

>[!NOTE]
>
>* Você deve carregar manualmente todos os arquivos de imagem. Os links para feeds de produto do [!DNL Google Merchant Center] não são compatíveis.
>* Somente as configurações necessárias estão disponíveis. Para configurações opcionais, faça logon no editor [!DNL Google Ads].
>* Não há suporte disponível para a listagem de grupos. Para gerenciar e exibir dados de grupos de listagem, faça logon no editor do [!DNL Google Ads].

## Etapas para configurar campanhas de desempenho máximo de [!DNL Google Ads]

Você pode configurar campanhas de desempenho máximo individualmente na exibição [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

1. [Crie uma campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) com o tipo de campanha **[!UICONTROL Performance Max]**.

   Especifique os [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] e [!UICONTROL URL Options]. Opcionalmente, insira [!UICONTROL Negative Keywords], insira [!UICONTROL Negative Websites] e/ou substitua as opções [!UICONTROL Campaign Tracking].

1. Criar grupos de ativos e fazer upload de ativos para a campanha:

   1. Na parte inferior das configurações da campanha, clique em **[!UICONTROL Manage Asset Groups]**.

   1. Especifique as configurações para o primeiro grupo de ativos e faça upload das imagens, logotipos e vídeos opcionais para o grupo de ativos.

      Consulte [descrições das configurações do grupo de ativos](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) para entender os requisitos e as especificações.

   1. Adicione grupos de ativos adicionais, conforme necessário.

1. Clique em **[!UICONTROL Post]**.

1. (Opcional) Adicione a campanha a um portfólio híbrido para otimização.
