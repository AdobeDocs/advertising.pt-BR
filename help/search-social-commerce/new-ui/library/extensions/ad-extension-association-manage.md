---
title: Gerenciar associações de extensão de anúncio
description: Saiba como associar sitelinks e chamadas compartilhados a entidades de conta, excluir associações e copiar dados de associação para a área de transferência.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%
---
# Gerenciar associações de extensão de anúncio

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

Uma associação vincula uma extensão de anúncio a uma entidade de conta para que a extensão possa ser usada com seus anúncios. É possível criar associações para sitelinks e chamadas compartilhados e excluir associações existentes, incluindo sitelink, chamada, local e associações de extensão de telefone compatíveis com a rede de anúncios.

Excluir um link de site compartilhado ou uma associação de texto explicativo remove a associação com a entidade selecionada; isso não exclui a extensão compartilhada da biblioteca. Para excluir a extensão compartilhada, use a guia **[!UICONTROL Sitelinks]** ou **[!UICONTROL Callouts]**.

A exibição de associações requer a permissão [!UICONTROL View Extensions]. Criar ou excluir associações requer a permissão [!UICONTROL Edit Extensions].

## Associar sitelinks compartilhados a contas, campanhas e grupos de anúncios {#sitelink-associate}

Você pode atribuir sitelinks compartilhados para uso na rede de pesquisa:

* Para [!DNL Google Ads], atribua sitelinks a contas, campanhas ou grupos de anúncios.

* Para [!DNL Microsoft Advertising], atribua sitelinks a campanhas. Para atribuí-los a contas ou grupos de anúncios, use o gerente de anúncios do [!DNL Microsoft Advertising].

É possível atribuir até 20 sitelinks por conta, campanha ou grupo de anúncios. Mantenha pelo menos seis sitelinks ativos disponíveis para cobertura de desktop e móvel.

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Associations]**.

1. Clique em **[!UICONTROL Create Association]>[!UICONTROL Sitelink Association]**.

1. Na seção **[!UICONTROL Basic Settings]**, selecione a rede de publicidade e a conta.

1. Na seção **[!UICONTROL Sitelinks]**, selecione os sitelinks compartilhados para associar da biblioteca da conta.

1. Na seção **[!UICONTROL Assignment]**, selecione as entidades da conta às quais os sitelinks são atribuídos:

* Selecione cada conta, campanha ou grupo de anúncios aplicável.

* Para exibir as campanhas de uma conta ou os grupos de anúncios de uma campanha, expanda a conta ou a campanha.

* Use os controles de pesquisa da lista para localizar entidades específicas.

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as seleções. Para fazer alterações, clique em **[!UICONTROL Edit]** na seção aplicável.

1. Clique em **[!UICONTROL Create]**.

## Associar chamadas compartilhadas a campanhas e grupos de publicidade {#callout-associate}

*[!DNL Google Ads]somente contas*

Você pode associar chamadas compartilhadas a [campanhas e grupos de anúncios do Google Ads](/help/search-social-commerce/introduction/supported-inventory.md) com suporte na rede de pesquisa. Atribua pelo menos duas chamadas de retorno a cada campanha ou grupo de publicidade.

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Associations]**.

1. Clique em **[!UICONTROL Create Association]>[!UICONTROL Callout Association]**.

1. Na seção **[!UICONTROL Basic Settings]**, selecione [!DNL Google Ads] e a conta.

1. Na seção **[!UICONTROL Callouts]**, selecione as chamadas compartilhadas a serem associadas da biblioteca da conta.

1. Na seção **[!UICONTROL Assignment]**, selecione as campanhas ou grupos de anúncios aos quais as chamadas de retorno são atribuídas:

* Selecione cada campanha ou grupo de anúncios aplicável.

* Para exibir grupos de anúncios de uma campanha, expanda a campanha.

* Use os controles de pesquisa da lista para localizar campanhas ou grupos de anúncios específicos.

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as seleções. Para fazer alterações, clique em **[!UICONTROL Edit]** na seção aplicável.

1. Clique em **[!UICONTROL Create]**.

## Excluir associações {#association-delete}

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Associations]**.

1. (Opcional) Filtre a lista para incluir extensões, campanhas ou grupos de anúncios específicos.

1. Marque a caixa de seleção ao lado de cada associação a ser excluída.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gerenciar extensões compartilhadas do sitelink](sitelink-extension-manage.md)
>* [Gerenciar extensões de chamada compartilhadas do Google Ads](callout-extension-manage.md)
