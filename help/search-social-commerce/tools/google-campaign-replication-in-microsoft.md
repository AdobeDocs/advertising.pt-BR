---
title: Replicar [!DNL Google Ads] campanhas em [!DNL Microsoft Advertising]
description: Saiba como exportar suas campanhas sincronizadas em uma conta do  [!DNL Google Ads] diretamente para uma conta do  [!DNL Microsoft Advertising] sincronizada.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replicar [!DNL Google Ads] campanhas em [!DNL Microsoft Advertising]

Você pode exportar suas campanhas sincronizadas em uma conta do [!DNL Google Ads] diretamente para uma conta do [!DNL Microsoft Advertising] sincronizada como campanhas CPC (eCPC) aprimoradas. Os lances e orçamentos de campanha existentes são dimensionados. O rastreamento existente de Pesquisa, Social e Commerce não é importado.

Você pode replicar os seguintes tipos de campanhas e sua estrutura de campanha:

* [!DNL Google Ads] campanhas de pesquisa e exibição em [!DNL Microsoft Advertising] campanhas de pesquisa e exibição.

* [!DNL Google Display Network] campanhas, incluindo imagens de anúncios, em [!DNL Microsoft Advertising] campanhas de público-alvo na Microsoft Audience Network.

  Se você quiser replicar campanhas de exibição baseadas em feed de compras, primeiro replique suas ofertas de produtos do [!DNL Google Merchant Center] para o [!DNL Microsoft Merchant Center]. Ao replicar as campanhas, selecione o armazenamento [!DNL Microsoft Merchant Center] nas Opções de Importação para vincular o armazenamento às suas campanhas de público-alvo baseadas em feed.

* [!DNL Google Ads] campanhas de desempenho máximo, incluindo anúncios de inventário locais, em [!DNL Microsoft Advertising] campanhas de desempenho máximo.

Você pode optar por atualizar as campanhas uma vez; diariamente, semanalmente ou mensalmente; ou de acordo com a programação recomendada de [!DNL Microsoft Advertising]. Opcionalmente, é possível configurar notificações sempre que um trabalho de importação for executado ou quando ocorrerem erros ou alterações. Depois de importar suas campanhas para o [!DNL Microsoft Advertising], você pode verificar o status do seu trabalho de importação, revisar possíveis logs de erro, executar manualmente um trabalho de importação e editar, pausar, habilitar ou excluir o cronograma de importação.

Nem todas as informações da campanha são replicadas e talvez seja necessário adicionar algumas informações às campanhas do [!DNL Microsoft Advertising]. Para obter mais informações sobre quais dados são importados, consulte a ajuda do [!DNL Microsoft Advertising] em &quot;[O que é importado do [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Como o rastreamento de Search, Social e Commerce não é importado, você também deve adicionar rastreamento nas configurações de [conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [anúncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Replicar [!DNL Google Ads] campanhas

>[!NOTE]
>
>Se você deseja replicar as campanhas de exibição baseadas em feed de compras, primeiro [replique suas [!DNL Google Merchant Center] ofertas de produtos em [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Ao replicar as campanhas, selecione o armazenamento [!DNL Microsoft Merchant Center] nas opções de importação para vincular o armazenamento às suas campanhas de público baseadas em feed.

Consulte [o que é importado de [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. No menu principal Search, Social, &amp; Commerce, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Clique em **[!UICONTROL +Import]**.

1. Especifique as [configurações de importação](#campaign-import-settings):

   1. Na seção **[!UICONTROL Select accounts]**:

      1. Selecione as contas de origem e de destino.

      1. Clique em **[!UICONTROL Get Credential Id from MSA]**.

      1. Faça logon na conta de destino [!DNL Microsoft Advertising], copie a ID de credencial exibida e cole o valor no campo **[!UICONTROL Credential ID]**.

   1. Na seção **[!UICONTROL Select campaigns & ad groups]**, especifique as campanhas e os grupos de anúncios a serem importados.

   1. Na seção **[!UICONTROL Customize your import]**, especifique os tipos de item a serem importados.

   1. Na seção **[!UICONTROL Set schedule]**, especifique quando executar o trabalho de importação.

1. Clique em **[!UICONTROL Post]**.

1. (Opcional) Adicione o rastreamento de Search, Social e Commerce às configurações de [conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [anúncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Editar configurações de programação para um trabalho de importação de campanha

Consulte [o que é importado de [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Selecione a caixa ao lado do trabalho de importação e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Na seção **[!UICONTROL Set schedule]**, especifique as [configurações de agendamento](#campaign-import-settings).

1. Clique em **[!UICONTROL Post]**.

## Exibir seus trabalhos de importação de campanha

Você pode listar todos os trabalhos de importação, incluindo a conta de origem [!DNL Google Ads], a conta de destino [!DNL Microsoft Advertising], o horário ou agendamento de importação e o usuário que criou o trabalho. Quando você executa um trabalho de importação várias vezes, incluindo durante importações programadas regularmente, cada ocorrência é listada como um trabalho separado.

* Siga um destes procedimentos:

   * No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Por padrão, o modo de exibição é aberto na guia [!UICONTROL List of Import Jobs].

   * Na guia [[!UICONTROL Import Logs] ](#campaign-import-log), clique na guia **[!UICONTROL List of Import Jobs]**.

## Executar um trabalho de importação de campanha

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Marque a caixa de seleção ao lado do trabalho de importação.

1. Clique em ![Executar agora](/help/search-social-commerce/assets/run.png "Executar agora").

## Exibir logs para seus trabalhos de importação de campanha {#campaign-import-log}

Você pode listar todos os trabalhos de importação concluídos ou com falha, incluindo a hora de início, a conta de origem [!DNL Google Ads], a conta de destino [!DNL Microsoft Advertising], o usuário que criou o trabalho, o número de operações com êxito e com falha e quaisquer endereços de email que receberam notificações para cada trabalho. Você pode ver mais detalhes sobre as alterações na conta de destino [!DNL Microsoft Advertising] que ocorreram para cada trabalho, incluindo o número de itens adicionados, sincronizados, excluídos e que produziram erros para cada nível de entidade (como campanha ou palavra-chave) na conta.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Clique na guia **[!UICONTROL Import Logs]**.

1. (Opcional) Para exibir detalhes de qualquer trabalho de importação, clique no valor na coluna [!UICONTROL Summary].

## Configurações do trabalho de importação da campanha {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** A conta [!DNL Google Ads] sincronizada da qual os dados de campanha são exportados.

**[!UICONTROL Credential ID]:** Uma ID que [!DNL Microsoft Advertising] usa para representar suas credenciais do [!DNL Google Ads].

A geração automática de credenciais [!DNL Microsoft Advertising] para importação não está disponível devido às limitações de [!DNL Microsoft Advertising]. Entre em contato com a equipe de conta da Adobe, que gerará as credenciais e fornecerá a ID.

**[!UICONTROL Target Microsoft Ads account]:** A conta [!DNL Microsoft Advertising] sincronizada na qual os dados da campanha são importados.

### [!UICONTROL Select campaigns & ad groups]

**\[Dados a importar\]:** Especifique os dados a importar:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar dados para todas as campanhas que já existem e as que não existem em [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para selecionar campanhas e grupos de anúncios específicos.

   * Para expandir uma campanha em seus grupos de anúncios secundários, clique em **[!UICONTROL >]** depois do nome da campanha.

   * Para selecionar uma campanha ou grupo de anúncios, selecione o item para que apareça uma marca de seleção.

   * Para remover uma campanha ou grupo de anúncios:

      * Na coluna [!UICONTROL Campaigns] ou [!UICONTROL Adgroups], desmarque a campanha ou o grupo de anúncios para que a marca de seleção desapareça.

      * Na coluna [!UICONTROL Selected], clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar o que importar, ofertas e orçamentos, entre outras opções.

**[!UICONTROL What to import]:** Define os itens a serem importados. As opções para importar categorias de item são selecionadas por padrão, com todos os tipos de itens selecionados. Para incluir apenas tipos de item específicos, clique em **[!UICONTROL Show advanced options]** e altere os tipos de item para incluir.

**[!UICONTROL Bids and budgets]:** Define quais configurações de oferta e orçamento importar, atualizar e personalizar.

**[!UICONTROL Other options]:** Define como lidar com URLs de páginas de aterrissagem importadas, modelos de rastreamento e outras opções de campanha, anúncios e direcionamento.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** O nome do trabalho de importação.

**[!UICONTROL When]:** Quando importar as campanhas especificadas: *Automático* (para permitir que [!DNL Microsoft Advertising] defina um agendamento para otimizar suas campanhas), *[!UICONTROL Now]* (para executar o trabalho ao postar as configurações de trabalho), *[!UICONTROL Once]* em um horário especificado, *[!UICONTROL Daily]* em um horário especificado, *[!UICONTROL Weekly]* em um horário especificado ou *[!UICONTROL Monthly]* em um horário especificado.

**[!UICONTROL Receive email notifications]:** Se e quando enviar notificações por email sobre trabalhos de importação para os endereços de email no campo Enviar relatórios para.

**[!UICONTROL Send reports to]:** Endereços de email para receber notificações sobre trabalhos de importação. Separe vários endereços com vírgulas (`,`).
