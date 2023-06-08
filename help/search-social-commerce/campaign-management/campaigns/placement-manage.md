---
title: Gerenciar [!DNL Google Ads] disposições
description: Saiba como criar e gerenciar posicionamentos licitáveis para [!DNL Google Ads] grupos de publicidade.
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Gerenciar [!DNL Google Ads] disposições

*[!DNL Google Ads]somente contas*

Você pode criar e editar disposições para grupos de anúncios em [tipos de campanha compatíveis](/help/search-social-commerce/introduction/supported-inventory.md) que direcionem a rede de exibição em um [conta de rede de publicidade sincronizada](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Criar [!DNL Google Ads] disposições

>[!TIP]
>
>Para criar vários posicionamentos de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade, a conta, a campanha e o grupo de publicidade e clique em **[!UICONTROL Continue]**.

1. Configure o [configurações de posicionamento](#placement-settings).

1. Clique em **[!UICONTROL Post]**.

## Editar [!DNL Google Ads] disposições

>[!TIP]
>
>Para editar vários posicionamentos de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Marque a caixa de seleção ao lado de cada linha a ser editada.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") .

1. Edite o [configurações de posicionamento](#placement-settings).

   Para várias disposições, as alterações são aplicadas a todas as disposições selecionadas. Para alguns campos alfanuméricos, você pode alterar os valores existentes para um valor especificado, substituir uma string existente por uma string especificada, adicionar um prefixo especificado ao início de cada valor ou anexar um sufixo ao final de cada valor. Para alguns campos monetários, você pode alterar valores existentes para um valor especificado ou aumentar ou diminuir o valor em uma porcentagem ou quantia monetária especificada, com um limite.

1. Salve os dados:

   * (Inserções únicas) Clique em **[!UICONTROL Post]**.

   * (Vários posicionamentos) Clique em **[!UICONTROL Post Now]**.

## Configurações de posicionamento {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites da rede de conteúdo nos quais seu anúncio pode aparecer. Insira um URL válido, como www.example.com, example.com ou www.example.com/shoes/kids. Para especificar várias cadeias de caracteres, separe-as com vírgulas ou insira-as em linhas separadas. O URL não pode incluir um ponto de interrogação (`?`). **Nota:** Você pode [excluir posicionamentos de sites](placement-negative-create.md) do [!UICONTROL Placements] > [!UICONTROL Negatives] exibir e nas configurações do grupo de anúncios e da campanha.

**[!UICONTROL Status]:** O status de exibição do posicionamento: *Ativo* (para permitir lances; o padrão), *Pausado* (para desativar licitação) ou *Excluído* (para excluir a disposição; somente disposições existentes).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Opcional) O custo máximo por clique (CPC) ou custo por mil impressões visualizáveis (vCPM) para o anúncio baseado em posicionamento, dependendo da estratégia de oferta da campanha. Esse valor substitui a oferta de nível de grupo de anúncios.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Sobre posicionamentos](placement-about.md)
>* [Criar posicionamentos negativos](placement-negative-create.md)
>* [Alterar o status de disposições e disposições negativas](placement-status-edit.md)
