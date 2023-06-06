---
title: "Atualize o código de rastreamento do s\_kwcid para um [!DNL Google Ads] account"
description: Saiba como alternar para o código de rastreamento s\_kwcid mais recente para um [!DNL Google Ads] conta.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Atualize o código de rastreamento do s\_kwcid de um [!DNL Google Ads] account

*Anunciantes com uma integração Adobe Advertising-Adobe Analytics somente*

*[!DNL Google Ads]somente contas*

O formato legado do código de rastreamento s\_kwcid para o existente [!DNL Google Ads] contas do não são compatíveis com alguns recursos no Analytics, como relatórios nos níveis de campanha e grupo de anúncios para [!DNL Google Ads] desempenho máximo de campanhas, campanhas de rascunhos e experimentos e outros casos de uso em que a mesma combinação de tipo anúncio+palavra-chave+correspondência existe em várias campanhas.

O formato mais recente inclui parâmetros para a ID da campanha e a ID do grupo de publicidade:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

É possível alterar para o novo formato de qualquer uma ou todas as contas existentes, individualmente. Se você não tiver campanhas de desempenho máximo ou campanhas de rascunhos e experimentos, a migração para o novo formato é opcional.

Todos os novos [!DNL Google Ads] as contas do usam automaticamente o novo formato s\_ kwcid.

>[!NOTE]
>
>Depois de migrar uma conta, todos os dados de clique, custo e impressão são relatados corretamente após a alteração, mas os click-throughs ocorridos antes da migração ainda são atribuídos aos dados de conversão com base no formato s\_kwcid antigo.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Mantenha o cursor sobre o nome da conta e clique em ![ícone de seta suspensa](/help/search-social-commerce/assets/arrow-dropdown-menu.png)e selecione **[!UICONTROL Edit]**.
1. Clique em **[!UICONTROL Set Account Tracking]**.
1. Comece a migração:

   1. Ao lado de **[!UICONTROL S_KWCID FORMAT]** , clique em **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Clique em **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Na mensagem de confirmação, marque a caixa de seleção e clique em **[!UICONTROL Continue]**.
   1. Nas configurações da conta, clique em **[!UICONTROL Post]**.

   Os metadados das campanhas são atualizados no Analytics em alguns dias. O rastreamento continua ininterrupto, portanto, nenhum dado é perdido, mas os relatórios podem não refletir os novos códigos de rastreamento até que o Analytics receba todos os metadados.

   >[!NOTE]
   >
   >Todos os click-throughs ocorridos antes da migração ainda relatarão dados de conversão com base no formato antigo.

1. Depois de iniciar a migração, atualize as configurações de Sufixo da página inicial (chamado de &quot;sufixo de URL final&quot; em algumas redes de anúncios), conforme necessário:

   * Quando o recurso &quot;Upload automático&quot; está ativado nas configurações de rastreamento, o Search, Social e Commerce atualiza automaticamente o código de rastreamento no Sufixo da landing page dessa conta e suas campanhas. Você não precisa fazer nada.
   * Quando o recurso &quot;Carregamento automático&quot; não estiver ativado e você não usar o s-kwcid do lado do servidor, será necessário atualizar manualmente o parâmetro s\_kwcid nas configurações de Sufixo da página de aterrissagem. Você pode alterar os sufixos no nível da conta e da campanha manualmente nas configurações da conta e da campanha ou fazendo upload das alterações em uma bulksheet. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o [!DNL Google Ads] editor.
   * Se você incluir o s\_kwcid na configuração de URL base para qualquer componente da campanha, mova-o para a configuração relevante Sufixo da página inicial.

1. (Recomendado) Verifique os dados desta conta no Analytics antes de migrar contas adicionais.

>[!MORELIKETHIS]
>
>* [Gerenciar contas de rede de publicidade](ad-network-account-manage.md)
>* [O parâmetro de rastreamento s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Visão geral do [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html)

