---
title: Gerenciar extensões compartilhadas do sitelink
description: Saiba como criar, editar e excluir extensões compartilhadas do sitelink.
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
source-wordcount: '1127'
ht-degree: 0%
---
# Gerenciar extensões compartilhadas do sitelink

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

Um sitelink é um link de texto extra em uma lista de anúncios de texto. Use sitelinks para levar os usuários diretamente a páginas específicas do site. A rede de anúncios determina quais sitelinks serão exibidos com base em sua relevância para o anúncio.

Opcionalmente, é possível incluir texto descritivo para cada sitelink. A rede de publicidade também pode exibir uma cópia dos anúncios existentes na conta quando for altamente relevante para o sitelink. [!DNL Google Ads] pode mostrar de 2 a 6 sitelinks em um anúncio de desktop e até quatro em um anúncio móvel. [!DNL Microsoft Advertising] pode mostrar dois, quatro ou seis sitelinks com descrições ou 4-6 sem descrições.

Você cria texto e configurações de sitelink compartilhados no nível da conta para uma [conta de rede de publicidade sincronizada](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Os Sitelinks na biblioteca não são usados com anúncios até que você os associe a entidades de conta.

## Sobre as visualizações [!UICONTROL Sitelinks] e [!UICONTROL Associations] {#sitelink-view-about}

Em **[!UICONTROL Library]>[!UICONTROL Extensions]**, a guia **[!UICONTROL Sitelinks]** lista seus sitelinks compartilhados no nível da conta. A guia **[!UICONTROL Associations]** lista as associações entre extensões e entidades de conta.

A exibição dessas guias requer a permissão [!UICONTROL View Extensions]. Criar, editar e excluir sitelinks e criar ou excluir associações requer a permissão [!UICONTROL Edit Extensions].

Consulte a ajuda da rede de publicidade para obter o número máximo de extensões por [conta do Google Ads](https://support.google.com/google-ads/answer/6372658) e por [conta do Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/52001).

### Ações disponíveis

* [Criar um sitelink compartilhado](#sitelink-create)

* [Editar configurações de sitelink compartilhadas](#sitelink-edit)

* [Excluir sitelinks compartilhados](#sitelink-delete)

* [Associar sitelinks compartilhados a contas, campanhas e grupos de anúncios](ad-extension-association-manage.md#sitelink-associate)

* [Excluir associações de extensão](ad-extension-association-manage.md#association-delete)

* [Copiar todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard)

## Criar um sitelink compartilhado {#sitelink-create}

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Sitelinks]**.

1. Clique em **[!UICONTROL Create Sitelink]**.

1. Em **[!UICONTROL Basic Settings]**, selecione a rede de publicidade e a conta.

1. Insira as [configurações de sitelink compartilhadas](#shared-sitelink-settings).

1. Clique em **[!UICONTROL Review and Save]**.

1. Revise as configurações. Para alterar uma configuração, clique em **[!UICONTROL Edit]** na seção aplicável.

1. Clique em **[!UICONTROL Create]**.

Depois de criar o sitelink, [associe-o a uma conta, campanha ou grupo de anúncios](ad-extension-association-manage.md#sitelink-associate).

## Editar configurações de sitelink compartilhadas {#sitelink-edit}

É possível editar um sitelink compartilhado de cada vez. Você não pode alterar a data de início após criá-la.

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Sitelinks]**.

1. Marque a caixa de seleção ao lado de um sitelink.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

1. Edite as [configurações de sitelink compartilhadas](#shared-sitelink-settings).

1. Clique em **[!UICONTROL Review and Save]**, revise as configurações e clique em **[!UICONTROL Update]**.

Você também pode editar o **[!UICONTROL Base URL]** ou o **[!UICONTROL Tracking Template]** de um sitelink diretamente na tabela de dados clicando em seu valor.

## Excluir sitelinks compartilhados {#sitelink-delete}

1. No menu principal, clique em **[!UICONTROL Library]>[!UICONTROL Extensions]** e depois clique na guia **[!UICONTROL Sitelinks]**.

1. Marque a caixa de seleção ao lado de cada link de site compartilhado a ser excluído.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

Para remover uma associação sem excluir o sitelink compartilhado da biblioteca, [exclua a associação](ad-extension-association-manage.md#association-delete).

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

## Configurações de sitelink compartilhado {#shared-sitelink-settings}

Para obter políticas adicionais e motivos para a desaprovação do sitelink, consulte os [requisitos de sitelink do Google Ads](https://support.google.com/adspolicy/answer/1054210) e os [requisitos de sitelink do Microsoft Advertising](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** O texto a ser exibido para o link. Pode incluir até 25 caracteres de byte único ou 12 caracteres de byte duplo. O texto do link deve ser exclusivo na conta ou campanha.

>[!NOTE]
>
>([!DNL Google Ads]) O texto existente de 35 caracteres é exibido em anúncios em desktops e tablets, mas não em dispositivos móveis.

**[!UICONTROL Status]:** O status de exibição do sitelink: **[!UICONTROL Active]** ou **[!UICONTROL Deleted]** para sitelinks existentes. Os novos sitelinks estão ativos por padrão.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Texto extra que a rede de publicidade pode exibir sob o texto do link. Para incluir uma descrição, informe ambos os campos. Cada uma pode incluir até 35 caracteres de byte único ou 17 caracteres de byte duplo.

**[!UICONTROL Start Date]:** (Opcional; somente criação) A primeira data em que o sitelink pode ser exibido. O padrão é o dia atual. Para especificar uma data futura, insira-a no formato MM/DD/AAAA ou use o seletor de datas. A data de início é somente leitura para sitelinks existentes.

**[!UICONTROL End Date]:** (Opcional) A última data em que o sitelink pode ser exibido. Por padrão, o sitelink pode ser exibido indefinidamente. Para especificar uma data final, insira-a no formato MM/DD/AAAA ou use o seletor de datas.

**[!UICONTROL Mobile Preference]:** (Opcional) Permite que a rede tente exibir a extensão para usuários de dispositivos móveis em vez de usuários de desktop ou tablet. Por padrão, essa opção não está ativada e a extensão pode aparecer em qualquer tipo de dispositivo. A rede não garante que exibirá a extensão no tipo de dispositivo preferencial.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (Opcional) A URL de rastreamento, incluindo redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem, com a URL da página de aterrissagem final incorporada em um parâmetro. Por exemplo, `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

Nesta exibição, os valores inseridos para [!UICONTROL Base URL] e [!UICONTROL Tracking Template] devem começar com `http://` ou `https://` e não podem conter espaços.

* Quando as configurações da campanha incluem **[!UICONTROL EF Redirect]** e **[!UICONTROL Auto Upload]**, o Search, Social e Commerce prefixa automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.

* Para parâmetros que incorporam a URL final, consulte a [documentação do Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/56799) ou os parâmetros &quot;Somente modelo de rastreamento&quot; na [documentação do Google Ads ValueTrack](https://support.google.com/google-ads/answer/6305348).

* Você pode incluir parâmetros de URL e parâmetros personalizados no nível da campanha, separados por &quot;E&quot; comercial (`&`), além de redirecionamentos e rastreamento de terceiros.

* O modelo de rastreamento no nível mais granular substitui os modelos nos níveis mais altos.

>[!NOTE]
>
>* Para contas com URLs finais, o URL base pode conter redirecionamentos dentro do domínio ou subdomínio da página inicial, mas não fora dele. A rede de publicidade extrai o domínio para criar o URL de exibição.
>* ([!DNL Google Ads]) Cada sitelink em uma campanha ou grupo de anúncios deve ter uma página de aterrissagem exclusiva com aproximadamente 80% de conteúdo exclusivo. Não use links para várias âncoras na mesma página como páginas iniciais separadas do sitelink.
>* ([!DNL Google Ads]) A atualização de um modelo de rastreamento no nível do sitelink ou da palavra-chave reenvia os anúncios relevantes para revisão. Atualizá-lo no nível da conta, campanha ou grupo de anúncios não reenvia os anúncios.
>* ([!DNL Microsoft Advertising]) É possível atualizar modelos de rastreamento em qualquer nível sem reenviar anúncios para aprovação.
>* ([!DNL Google Ads]) Evite macros, que não são substituídas por cliques de fontes que habilitam o rastreamento paralelo. Se forem necessárias macros, sua equipe de conta da Adobe trabalhará com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

## Dados de desempenho para sitelinks {#sitelink-performance}

Os mapas de Pesquisa, Social e Commerce clicam em uma extensão de anúncio e as conversões resultantes na palavra-chave associada ao anúncio no qual a extensão aparece. Os dados de custo e clique no nível da extensão não estão disponíveis em Search, Social e Commerce.

Em [!UICONTROL Transaction Report], um valor [!UICONTROL Link Type] de `sl:<Sitelink text>`, como `sl:See Current Offers`, identifica uma transação de um sitelink em vez do próprio anúncio. Consulte &quot;[Relatório de transação](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)&quot;.

Você pode visualizar o custo no nível da extensão e clicar em dados na interface da rede de publicidade.

>[!MORELIKETHIS]
>
>* [Gerenciar extensões de chamada compartilhadas do Google Ads](callout-extension-manage.md)
>* [Gerenciar associações de extensão de anúncios](ad-extension-association-manage.md)
