---
title: Replicar [!DNL Google Ads] campanhas no [!DNL Microsoft® Advertising]
description: Saiba como exportar suas campanhas sincronizadas em um [!DNL Google Ads] diretamente em uma conta sincronizada [!DNL Microsoft® Advertising] conta.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 877333330df84ff5c8bd7ee1bfc837de492877fb
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Replicar [!DNL Google Ads] campanhas no [!DNL Microsoft® Advertising]

Você pode exportar suas campanhas sincronizadas em um [!DNL Google Ads] diretamente em uma conta sincronizada [!DNL Microsoft® Advertising] conta como campanhas CPC (eCPC) avançadas. Os lances e orçamentos de campanha existentes são dimensionados. O rastreamento existente de Pesquisa, Social e Comércio não é importado.

Você pode replicar os seguintes tipos de campanhas e sua estrutura de campanha:

* [!DNL Google Ads] pesquisar e exibir campanhas em [!DNL Microsoft® Advertising] pesquisar e exibir campanhas.

* [!DNL Google Display Network] campanhas do, incluindo imagens de anúncios, em [!DNL Microsoft® Advertising] campanhas de público na Microsoft® Audience Network.

  Se quiser replicar campanhas de exibição baseadas em feed de compras, primeiro replique suas [!DNL Google Merchant Center] ofertas de produtos para [!DNL Microsoft® Merchant Center]. Ao replicar as campanhas, selecione a variável [!DNL Microsoft® Merchant Center] armazene nas Opções de importação para vincular a loja às suas campanhas de público-alvo com base em feed.

* [!DNL Google Ads] desempenho máximo de campanhas, incluindo anúncios de inventário locais, em [!DNL Microsoft® Advertising] desempenho máximo de campanhas.

Você pode optar por atualizar as campanhas uma vez; diariamente, semanalmente ou mensalmente; ou de acordo com [!DNL Microsoft® Advertising]do calendário recomendado. Opcionalmente, é possível configurar notificações sempre que um trabalho de importação for executado ou quando ocorrerem erros ou alterações. Depois de importar suas campanhas para o [!DNL Microsoft® Advertising], você pode verificar o status do seu trabalho de importação, revisar logs de erro, executar um trabalho de importação manualmente e editar, pausar, habilitar ou excluir o cronograma de importação.

Nem todas as informações da campanha são replicadas e talvez seja necessário adicionar algumas informações às [!DNL Microsoft® Advertising] campanhas. Para obter mais informações sobre quais dados são importados, consulte [!DNL Microsoft® Advertising] ajuda sobre &quot;[O que é importado do [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Como o rastreamento de Pesquisa, Social e Comércio não é importado, você também deve adicionar o rastreamento dentro da [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) configurações.

## Replicar [!DNL Google Ads] campanhas

>[!NOTE]
>
>Se você quiser replicar campanhas de exibição baseadas em feed de compras, primeiro [replique seu [!DNL Google Merchant Center] ofertas de produto no [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Ao replicar as campanhas, selecione a variável [!DNL Microsoft® Merchant Center] armazene nas opções de importação para vincular a loja às suas campanhas de público-alvo baseadas em feed.

Consulte [do que é importado [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. No menu principal Pesquisar, Social e Comércio, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Clique em **[!UICONTROL +Import]**.

1. Especifique a [configurações de importação](#campaign-import-settings):

   1. No **[!UICONTROL Select accounts]** seção:

      1. Selecione as contas de origem e de destino.

      1. Clique em **[!UICONTROL Get Credential Id from MSA]**.

      1. Fazer logon no destino [!DNL Microsoft Advertising] conta, copie a ID da credencial que é exibida e cole o valor no campo **[!UICONTROL Credential ID]** campo.

   1. No **[!UICONTROL Select campaigns & ad groups]** especifique as campanhas e os grupos de anúncios a serem importados.

   1. No **[!UICONTROL Customize your import]** especifique os tipos de item a serem importados.

   1. No **[!UICONTROL Set schedule]** especifique quando executar o trabalho de importação.

1. Clique em **[!UICONTROL Post]**.

1. (Opcional) Adicione o rastreamento de Pesquisa, Social e Comércio na [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de publicidade](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) configurações.

## Editar configurações de programação para um trabalho de importação de campanha

Consulte [do que é importado [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Marque a caixa de seleção ao lado do trabalho de importação e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. No **[!UICONTROL Set schedule]** especifique a [configurações de programação](#campaign-import-settings).

1. Clique em **[!UICONTROL Post]**.

## Exibir seus trabalhos de importação de campanha

Você pode listar todos os trabalhos de importação, incluindo a origem [!DNL Google Ads] conta, o target [!DNL Microsoft® Advertising] conta, o horário ou agendamento de importação e o usuário que criou o job. Quando você executa um trabalho de importação várias vezes, incluindo durante importações programadas regularmente, cada ocorrência é listada como um trabalho separado.

* Siga um destes procedimentos:

   * No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Por padrão, a exibição é aberta para a variável [!UICONTROL List of Import Jobs] guia.

   * No [[!UICONTROL Import Logs] guia](#campaign-import-log), clique no link **[!UICONTROL List of Import Jobs]** guia.

## Executar um trabalho de importação de campanha

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Marque a caixa de seleção ao lado do trabalho de importação.

1. Clique em ![Executar agora](/help/search-social-commerce/assets/run.png "Executar agora").

## Exibir logs para seus trabalhos de importação de campanha {#campaign-import-log}

Você pode listar todos os trabalhos de importação concluídos ou com falha, incluindo a hora de início, a origem [!DNL Google Ads] conta, o target [!DNL Microsoft® Advertising] , o usuário que criou o trabalho, o número de operações bem-sucedidas e com falha e quaisquer endereços de email que receberam notificações para cada trabalho. Você pode ver mais detalhes sobre as alterações no público alvo [!DNL Microsoft® Advertising] conta que ocorreu para cada trabalho, incluindo o número de itens adicionados, sincronizados, excluídos e que produziram erros para cada nível de entidade (como campanha ou palavra-chave) na conta.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Clique em **[!UICONTROL Import Logs]** guia.

1. (Opcional) Para exibir detalhes de qualquer trabalho de importação, clique no valor na [!UICONTROL Summary] coluna.

## Configurações do trabalho de importação da campanha {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** O sincronizado [!DNL Google Ads] conta da qual os dados do campaign são exportados.

**[!UICONTROL Credential ID]:** Uma ID que [!DNL Microsoft® Advertising] O usa o para representar sua [!DNL Google Ads] credenciais.

Geração automática de [!DNL Microsoft® Advertising] as credenciais para importação não estão disponíveis devido a [!DNL Microsoft® Advertising] limitações. Entre em contato com a equipe de conta do Adobe, que gerará as credenciais e fornecerá a ID.

**[!UICONTROL Target Microsoft® Ads account]:** O sincronizado [!DNL Microsoft® Advertising] conta para a qual os dados da campanha são importados.

### [!UICONTROL Select campaigns & ad groups]

**\[Dados a importar\]:** Especifique os dados a serem importados:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar dados de todas as campanhas que já existem e campanhas que não existem no [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para selecionar campanhas específicas e grupos de anúncios.

   * Para expandir uma campanha em seus grupos de anúncios secundários, clique em **[!UICONTROL >]** após o nome da campanha.

   * Para selecionar uma campanha ou grupo de anúncios, selecione o item para que apareça uma marca de seleção.

   * Para remover uma campanha ou grupo de anúncios:

      * No [!UICONTROL Campaigns] ou [!UICONTROL Adgroups] , desmarque a campanha ou o grupo de anúncios para que a marca de seleção desapareça.

      * No [!UICONTROL Selected] clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar o que importar, lances e orçamentos, entre outras opções.

**[!UICONTROL What to import]:** Define os itens a serem importados. As opções para importar categorias de item são selecionadas por padrão, com todos os tipos de itens selecionados. Para incluir apenas tipos de item específicos, clique em **[!UICONTROL Show advanced options]** e altere os tipos de item para incluir.

**[!UICONTROL Bids and budgets]:** Define as configurações de oferta e orçamento a serem importadas, atualizadas e personalizadas.

**[!UICONTROL Other options]:** Define como lidar com URLs de página de aterrissagem importados, modelos de rastreamento e outras opções de campanha, publicidade e direcionamento.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** O nome do trabalho de importação.

**[!UICONTROL When]:** Quando importar as campanhas especificadas: *Automático* (para permitir [!DNL Microsoft® Advertising] definir um cronograma para otimizar suas campanhas), *[!UICONTROL Now]* (para executar o job ao publicar as configurações do job), *[!UICONTROL Once]* em um horário especificado, *[!UICONTROL Daily]* em um horário especificado, *[!UICONTROL Weekly]* em um horário especificado, ou *[!UICONTROL Monthly]* em um horário especificado.

**[!UICONTROL Receive email notifications]:** Se e quando enviar notificações por email sobre trabalhos de importação para os endereços de email no campo Enviar relatórios para.

**[!UICONTROL Send reports to]:** Endereços de email para receber notificações sobre trabalhos de importação. Separe vários endereços com vírgulas (`,`).
