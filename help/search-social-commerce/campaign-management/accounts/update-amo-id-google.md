---
title: Atualizar o código de rastreamento da ID do AMO (s_kwcid) para uma conta  [!DNL Google Ads]
description: Saiba como alternar para o código de rastreamento de ID do AMO mais recente para uma conta do  [!DNL Google Ads] .
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Atualizar o código de rastreamento da ID do AMO (s_kwcid) para uma conta [!DNL Google Ads]

*Somente anunciantes com integração Adobe Advertising-Adobe Analytics*

*[!DNL Google Ads]somente contas*

O formato herdado (anterior a outubro de 2019) do [código de rastreamento da ID do AMO](/help/integrations/analytics/ids.md#amo-id-formats) para contas [!DNL Google Ads] existentes não oferece suporte a alguns recursos no Analytics, como relatórios nos níveis de campanha e grupo de anúncios para campanhas de desempenho máximo do [!DNL Google Ads], campanhas de rascunhos e experimentos e outros casos de uso nos quais a mesma combinação de tipo anúncio+palavra-chave+correspondência existe em várias campanhas.

O formato atual inclui parâmetros para a ID da campanha e a ID do grupo de publicidade:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

É possível alterar para o formato atual de qualquer uma ou todas as contas existentes, individualmente. Se você não tiver campanhas de desempenho máximo ou campanhas de rascunhos e experimentos, a migração para o novo formato é opcional.

Todas as novas contas do [!DNL Google Ads] usam automaticamente o formato de ID AMO atual.

>[!NOTE]
>
>Depois de migrar uma conta, todos os dados de clique, custo e impressão são relatados corretamente após a alteração, mas todos os click-throughs ocorridos antes da migração ainda são atribuídos aos dados de conversão com base no formato antigo da ID do AMO.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta, clique em ![ícone de seta suspensa](/help/search-social-commerce/assets/arrow-dropdown-menu.png) e selecione **[!UICONTROL Edit]**.

1. Clique em **[!UICONTROL Set Account Tracking]**.

1. Comece a migração:

   1. Ao lado de **[!UICONTROL S_KWCID FORMAT]** , clique em **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Clique em **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Na mensagem de confirmação, marque a caixa de seleção e clique em **[!UICONTROL Continue]**.

   1. Nas configurações da conta, clique em **[!UICONTROL Post]**.

   Os metadados das campanhas são atualizados em [!DNL Analytics] dentro de alguns dias. O rastreamento continua sem interrupções, portanto, nenhum dado é perdido, mas os relatórios podem não refletir os novos códigos de rastreamento até que [!DNL Analytics] receba todos os metadados.

   >[!NOTE]
   >
   >Todos os click-throughs ocorridos antes da migração ainda relatam dados de conversão com base no formato antigo.

1. Depois de iniciar a migração, atualize as configurações de Sufixo da página inicial (chamado de &quot;sufixo de URL final&quot; em algumas redes de anúncios), conforme necessário:

   * Quando o recurso [!UICONTROL Auto Upload] está habilitado nas configurações de rastreamento, o Search, Social e Commerce atualiza automaticamente o código de rastreamento no Sufixo da página de aterrissagem desta conta e suas campanhas. Você não precisa fazer nada.

   * Quando o recurso [!UICONTROL Auto Upload] não estiver habilitado e você não usar o [recurso de ID do AMO do lado do servidor](/help/integrations/analytics/ids.md#amo-id-formats), será necessário atualizar manualmente o parâmetro de ID do AMO nas configurações de Sufixo da página de aterrissagem. Você pode alterar os sufixos no nível da conta e da campanha manualmente nas configurações da conta e da campanha ou fazendo upload das alterações em uma bulksheet. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor [!DNL Google Ads].

   * Se você incluir a ID do AMO na configuração de URL base para qualquer componente da campanha, mova-a para a configuração relevante Sufixo da página inicial.

1. (Recomendado) Verifique os dados desta conta no [!DNL Analytics] antes de migrar contas adicionais.

>[!MORELIKETHIS]
>
>* [Gerenciar contas de rede de publicidade](ad-network-account-manage.md)
>* [IDs de Adobe Advertising Usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Visão Geral de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
