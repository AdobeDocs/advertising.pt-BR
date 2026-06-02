---
title: (Nova interface) Replicar campanhas do Google Ads no Microsoft Advertising
description: Saiba como exportar suas campanhas sincronizadas em uma conta do Google Ads diretamente para uma conta sincronizada do Microsoft Advertising.
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# (Nova interface do usuário) Replicar campanhas [!DNL Google Ads] em [!DNL Microsoft Advertising]

*recurso do Beta*

Você pode exportar suas campanhas sincronizadas em uma conta do [!DNL Google Ads] diretamente para uma conta do [!DNL Microsoft Advertising] sincronizada como campanhas CPC (eCPC) aprimoradas. Os lances e orçamentos de campanha existentes são dimensionados. O rastreamento existente de Pesquisa, Social e Commerce não é importado.

Você pode replicar os seguintes tipos de campanhas e sua estrutura de campanha:

* [!DNL Google Ads] campanhas de pesquisa e exibição em [!DNL Microsoft Advertising] campanhas de pesquisa e exibição.

* [!DNL Google Display Network] campanhas, incluindo imagens de anúncios, em [!DNL Microsoft Advertising] campanhas de público-alvo na Microsoft Audience Network.

  Se você quiser replicar campanhas de exibição baseadas em feed de compras, primeiro replique suas ofertas de produtos do [!DNL Google Merchant Center] para o [!DNL Microsoft Merchant Center]. Ao replicar as campanhas, selecione o armazenamento [!DNL Microsoft Merchant Center] nas opções de importação para vincular o armazenamento às suas campanhas de público baseadas em feed.

* [!DNL Google Ads] campanhas de desempenho máximo, incluindo anúncios de inventário locais, em [!DNL Microsoft Advertising] campanhas de desempenho máximo.

Você pode optar por atualizar as campanhas uma vez; diariamente, semanalmente ou mensalmente; ou de acordo com a programação recomendada de [!DNL Microsoft Advertising]. Opcionalmente, é possível configurar notificações sempre que um trabalho de importação for executado ou quando ocorrerem erros ou alterações. Depois de importar suas campanhas para o [!DNL Microsoft Advertising], você pode verificar o status do seu trabalho de importação, revisar possíveis logs de erro, executar manualmente um trabalho de importação e editar, pausar, habilitar ou excluir o cronograma de importação.

Nem todas as informações da campanha são replicadas e talvez seja necessário adicionar algumas informações às campanhas do [!DNL Microsoft Advertising]. Para obter mais informações sobre quais dados são importados, consulte a ajuda do [!DNL Microsoft Advertising] em &quot;[O que é importado do [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}.&quot; Como o rastreamento de Search, Social e Commerce não é importado, você também deve adicionar rastreamento nas configurações de [conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [anúncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Replicar [!DNL Google Ads] campanhas

>[!NOTE]
>
>Se você deseja replicar as campanhas de exibição baseadas em feed de compras, primeiro [replique suas [!DNL Google Merchant Center] ofertas de produtos em [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}. Ao replicar as campanhas, selecione o armazenamento [!DNL Microsoft Merchant Center] nas opções de importação para vincular o armazenamento às suas campanhas de público baseadas em feed.

Consulte [o que é importado de [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Clique em **[!UICONTROL Import Campaigns]**.

1. Especifique as [configurações de importação](#campaign-import-settings):

   1. Na etapa **[!UICONTROL Select accounts]**:

      1. Insira um nome para o trabalho de importação no campo **[!UICONTROL Import Name]**.

      1. Selecione a conta de origem [!DNL Google Ads] e a conta de destino [!DNL Microsoft Advertising].

      1. Insira seu **[!UICONTROL Credential ID]**. Entre em contato com a equipe de conta da Adobe se você não tiver uma ID de credencial — a geração automática não está disponível devido às limitações de [!DNL Microsoft Advertising].

      1. Clique em **[!UICONTROL Next]**.

   1. Na etapa **[!UICONTROL Select campaigns & ad groups]**, especifique as campanhas e os grupos de anúncios a serem importados e clique em **[!UICONTROL Next]**.

   1. Na etapa **[!UICONTROL Customize your import]**, especifique opcionalmente os tipos de item, as configurações de oferta e orçamento e outras opções para importar e clique em **[!UICONTROL Next]**.

   1. Na etapa **[!UICONTROL Set schedule]**, especifique quando executar o trabalho de importação e como receber notificações.

1. Revise suas seleções no resumo e clique em **[!UICONTROL Start Import]**.

1. (Opcional) Adicione o rastreamento de Search, Social e Commerce às configurações de [conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [anúncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Editar configurações de programação para um trabalho de importação de campanha

Consulte [o que é importado de [!DNL Google Ads] campanhas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Clique na guia **[!UICONTROL Jobs]**.

1. Clique no nome do trabalho de importação e clique em **[!UICONTROL Edit]**.

1. Na etapa **[!UICONTROL Set schedule]**, especifique as [configurações de agendamento](#campaign-import-settings).

1. Clique em **[!UICONTROL Save]**.

## Exibir seus trabalhos de importação de campanha

Você pode listar todos os trabalhos de importação, incluindo a conta de origem [!DNL Google Ads], a conta de destino [!DNL Microsoft Advertising], o horário ou agendamento de importação e o usuário que criou o trabalho. Quando você executa um trabalho de importação várias vezes, incluindo durante importações programadas regularmente, cada ocorrência é listada como um trabalho separado.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

   O modo de exibição abre a guia **[!UICONTROL Jobs]** por padrão.

## Executar um trabalho de importação de campanha

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Clique na guia **[!UICONTROL Jobs]**.

1. Selecione a caixa ao lado do trabalho de importação e clique em **[!UICONTROL Run Now]**.

## Exibir logs para seus trabalhos de importação de campanha {#campaign-import-log}

Você pode listar todos os trabalhos de importação concluídos ou com falha, incluindo a hora de início, a conta de origem [!DNL Google Ads], a conta de destino [!DNL Microsoft Advertising], o usuário que criou o trabalho, o número de operações com êxito e com falha e quaisquer endereços de email que receberam notificações para cada trabalho. Você pode ver mais detalhes sobre as alterações na conta de destino [!DNL Microsoft Advertising] que ocorreram para cada trabalho, incluindo o número de itens adicionados, sincronizados, excluídos e que produziram erros para cada nível de entidade (como campanha ou palavra-chave) na conta.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Clique na guia **[!UICONTROL Logs]**.

1. (Opcional) Para exibir detalhes de qualquer trabalho de importação, clique no valor na coluna [!UICONTROL Summary].

## Configurações do trabalho de importação da campanha {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]:** Um nome para identificar o trabalho de importação.

**[!UICONTROL Source Google Ads account]:** A conta [!DNL Google Ads] sincronizada da qual os dados de campanha são exportados.

**[!UICONTROL Target Microsoft Ads account]:** A conta [!DNL Microsoft Advertising] sincronizada na qual os dados da campanha são importados.

**[!UICONTROL Credential ID]:** Uma ID que [!DNL Microsoft Advertising] usa para representar suas credenciais do [!DNL Google Ads]. A geração automática de credenciais [!DNL Microsoft Advertising] para importação não está disponível devido às limitações de [!DNL Microsoft Advertising]. Entre em contato com a equipe de conta da Adobe, que gerará as credenciais e fornecerá a ID.

### [!UICONTROL Select campaigns & ad groups]

**\[Dados a importar\]:** Os dados a importar:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar dados para todas as campanhas que já existem e as que não existem em [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para selecionar campanhas e grupos de anúncios específicos.

   * Para expandir uma campanha em seus grupos de anúncios secundários, clique em **[!UICONTROL >]** depois do nome da campanha.

   * Para selecionar uma campanha ou grupo de anúncios, selecione o item para que apareça uma marca de seleção.

   * Para remover uma campanha ou grupo de anúncios, desmarque o item ou clique no ícone excluir na coluna [!UICONTROL Selected].

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar o que importar, ofertas e orçamentos, entre outras opções.

**[!UICONTROL What to import]:** Define os itens a serem importados. As opções para importar categorias de item são selecionadas por padrão, com todos os tipos de item selecionados. Para incluir apenas tipos de item específicos, clique em **[!UICONTROL Show advanced options]** e altere os tipos de item para incluir. Opcionalmente, também é possível associar uma ID de tag UET a qualquer lista de remarketing ou público que não tenha sido importado anteriormente para o [!DNL Microsoft Advertising].

**[!UICONTROL Bids and budgets]:** Define as configurações de oferta e orçamento a serem importadas, atualizadas e personalizadas, incluindo as opções para aumentar ou diminuir ofertas e orçamentos em uma porcentagem especificada para [!DNL Microsoft Advertising].

**[!UICONTROL Other options]:** Define como lidar com URLs de páginas de aterrissagem importadas, modelos de rastreamento e outras opções de campanha, anúncios e direcionamento, incluindo opções para localizar e substituir texto e inserir sufixos.

### [!UICONTROL Set schedule]

**[!UICONTROL When]:** Quando importar as campanhas especificadas: *Automático* (para permitir que [!DNL Microsoft Advertising] defina um agendamento para otimizar suas campanhas), *[!UICONTROL Now]* (para executar o trabalho ao postar as configurações de trabalho), *[!UICONTROL Once]* em um horário especificado, *[!UICONTROL Daily]* em um horário especificado, *[!UICONTROL Weekly]* em um horário especificado ou *[!UICONTROL Monthly]* em um horário especificado.

**[!UICONTROL Receive email notifications]:** Se e quando enviar notificações por email sobre trabalhos de importação para os endereços no campo [!UICONTROL Send reports to]: *[!UICONTROL No emails]*, *[!UICONTROL Only if there are changes or errors]* (o padrão), *[!UICONTROL Only if there are errors]* ou *[!UICONTROL Every time this import runs]*.

**[!UICONTROL Send reports to]:** Endereços de email para receber notificações sobre trabalhos de importação. Separe vários endereços com vírgulas (`,`).

>[!MORELIKETHIS]
>
>* [Gerenciar contas de rede de publicidade](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
