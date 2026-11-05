---
title: Gerenciar extensões de chamada compartilhadas do Google Ads
description: Saiba como criar, editar e excluir extensões de chamada compartilhadas do Google Ads.
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
source-wordcount: '685'
ht-degree: 0%
---
# Gerenciar [!DNL Google Ads] extensões de chamada compartilhadas

*[!DNL Google Ads]somente contas*

Uma extensão de chamada é um texto informativo sobre um produto, serviço ou promoção que seu site oferece, exibido com um anúncio de texto. A rede de publicidade pode mostrar de 2 a 4 chamadas com um anúncio.

Você cria texto explicativo e configurações compartilhados no nível da conta para uma [conta sincronizada do Google Ads](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). As chamadas na biblioteca não são usadas com anúncios até que você as associe a uma campanha ou grupo de anúncios compatível na rede de pesquisa.

Para que seus anúncios possam ser exibidos com chamadas, atribua pelo menos duas chamadas por campanha ou grupo de publicidade. As chamadas no nível do grupo de anúncios substituem as chamadas no nível da campanha.

## Sobre as visualizações [!UICONTROL Callouts] e [!UICONTROL Associations] {#callout-view-about}

Em **[!UICONTROL Library]>[!UICONTROL Extensions]**, a guia **[!UICONTROL Callouts]** lista suas chamadas compartilhadas no nível da conta. A guia **[!UICONTROL Associations]** lista as associações entre extensões e entidades de conta.

A exibição dessas guias requer a permissão [!UICONTROL View Extensions]. Criar, editar e excluir chamadas e criar ou excluir associações requer a permissão [!UICONTROL Edit Extensions].

Consulte a [documentação do Google Ads sobre limites de conta](https://support.google.com/google-ads/answer/6372658) para obter o número máximo de extensões por conta.

### Ações disponíveis

* [Criar uma chamada compartilhada](#callout-create)

* [Editar configurações de texto explicativo compartilhadas](#callout-edit)

* [Excluir chamadas compartilhadas](#callout-delete)

* [Associar chamadas compartilhadas a campanhas e grupos de publicidade](ad-extension-association-manage.md#callout-associate)

* [Excluir associações de extensão](ad-extension-association-manage.md#association-delete)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

## Criar uma chamada compartilhada {#callout-create}

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Callouts]**.

1. Clique em **[!UICONTROL Create Callout]**.

1. Em **[!UICONTROL Basic Settings]**, selecione [!DNL Google Ads] e a conta.

1. Insira as [configurações de texto explicativo compartilhado](#shared-callout-settings).

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as configurações. Para alterar uma configuração, clique em **[!UICONTROL Edit]** na seção aplicável.

1. Clique em **[!UICONTROL Create]**.

Depois de criar a chamada, [associe-a a uma campanha ou grupo de publicidade](ad-extension-association-manage.md#callout-associate).

## Editar configurações de texto explicativo compartilhadas {#callout-edit}

É possível editar uma chamada compartilhada de cada vez. Você não pode alterar a data de início após criá-la.

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Callouts]**.

1. Marque a caixa de seleção ao lado de uma chamada.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite as [configurações de texto explicativo compartilhado](#shared-callout-settings).

1. Clique em **[!UICONTROL Review and Save]**, revise as configurações e clique em **[!UICONTROL Update]**.

## Excluir chamadas compartilhadas {#callout-delete}

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Callouts]**.

1. Marque a caixa de seleção ao lado de cada texto explicativo compartilhado a ser excluído.

   Para obter informações sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

Para remover uma associação sem excluir o texto explicativo compartilhado da biblioteca, [exclua a associação](ad-extension-association-manage.md#association-delete).

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Configurações de texto explicativo compartilhado {#shared-callout-settings}

Para obter mais políticas e motivos para a desaprovação de chamada, consulte os [requisitos de chamada do Google Ads](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** O texto a ser exibido. Pode incluir até 25 caracteres de byte único ou 12 caracteres de byte duplo. Ele não pode incluir pontos de exclamação ou pontuação no início do texto.

**[!UICONTROL Start Date]:** (Opcional; somente criação) A primeira data em que a chamada pode ser exibida. O padrão é o dia atual. Para especificar uma data futura, insira-a no formato MM/DD/AAAA ou use o seletor de datas. A data de início é somente leitura para chamadas existentes.

**[!UICONTROL End Date]:** (Opcional) A última data em que a chamada pode ser exibida. Por padrão, a chamada pode ser exibida indefinidamente. Para especificar uma data final, insira-a no formato MM/DD/AAAA ou use o seletor de datas.

**[!UICONTROL Mobile Preference]:** (Opcional) Permite que o [!DNL Google Ads] tente exibir a extensão para usuários de dispositivos móveis, em vez de usuários de desktop ou tablet. Caso contrário, a extensão poderá ser exibida em qualquer tipo de dispositivo. [!DNL Google Ads] não garante que exibirá a extensão no tipo de dispositivo preferencial.

## Dados de desempenho para chamadas de retorno {#callout-performance}

Os mapas de Pesquisa, Social e Commerce clicam em uma extensão de anúncio e as conversões resultantes na palavra-chave associada ao anúncio no qual a extensão aparece. Os dados de custo e clique no nível da extensão não estão disponíveis em Search, Social e Commerce.

Você pode visualizar o custo de nível de extensão e clicar em dados na interface [!DNL Google Ads].

>[!MORELIKETHIS]
>
>* [Gerenciar extensões compartilhadas do sitelink](sitelink-extension-manage.md)
>* [Gerenciar associações de extensão de anúncios](ad-extension-association-manage.md)
