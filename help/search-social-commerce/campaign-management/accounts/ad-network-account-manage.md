---
title: Gerenciar contas de rede de publicidade
description: Saiba como configurar e gerenciar detalhes de uma conta de rede de anúncios.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Gerenciar contas de rede de publicidade

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Veja a seguir instruções para criar e editar detalhes de contas de rede de anúncios, atualizar o token [!DNL oAuth] para uma conta e desabilitar contas.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Criar detalhes da conta de rede de publicidade {#create-account}

*Somente funções de gerente de conta de agência, gerente de conta da Adobe e administrador de usuário*

Para habilitar a sincronização ou o rastreamento de uma conta, você deve criar um registro de conta correspondente contendo as credenciais de acesso e as opções de rastreamento da conta e com o status *ativo*.

>[!NOTE]
>
>* Suporte indisponível para novas contas do [!DNL Baidu].
>* Para criar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Especifique as [configurações da conta](#account-settings):

   1. Clique no nome da rede de publicidade e clique em **[!UICONTROL Next]**.

   1. Na seção **[!UICONTROL Account Details]**, insira os detalhes da conta.

      Para redes de anúncios que usam o tipo de autorização de logon &quot;[!UICONTROL oAuth]&quot;, permita que o Search, Social e Commerce acesse a conta usando o [protocolo de autorização OAuth](https://oauth.net/2/):

      1. Insira o valor **[!UICONTROL Login]** para a conta, opcionalmente insira a senha e clique em **[!UICONTROL Authenticate]**.

         A prática recomendada é usar o logon para acessar a conta pela API. Digite a senha quando quiser criptografá-la e salvá-la, para que a equipe de conta da Adobe possa atualizar os tokens conforme necessário.

      1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta de anúncios do anunciante. A prática recomendada é usar as credenciais para o acesso da API à conta.

      1. Na tela de solicitação de permissão/acesso, clique no botão para confirmar a permissão.

      1. Copie a cadeia de caracteres de autenticação na janela pop-up que é aberta e cole-a no campo **[!UICONTROL oAuth Token]**.

      1. Especifique os detalhes restantes da conta.

   1. Clique em **[!UICONTROL Set Account Tracking]** e insira as configurações de rastreamento.

1. Clique em **[!UICONTROL Post]**.

   Os dados recentes de custos e cliques de todas as campanhas na conta do estão disponíveis em Pesquisa, Social e Commerce em cerca de 24 horas. Por padrão, os dados estão disponíveis nos últimos 5 a 10 dias, dependendo da rede de anúncios. No entanto, quando necessário, a equipe de lançamento do projeto pode recuperar dados dos últimos 60 dias.

## Editar detalhes da conta de rede de publicidade {#edit-account}

*Somente funções de gerente de conta de agência, gerente de conta da Adobe e administrador de usuário*

Se as credenciais da conta forem alteradas, você desejará alterar os parâmetros de rastreamento padrão em uma conta, ou ativar ou desativar a atividade em uma conta e, em seguida, editar os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta, clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais") e selecione **[!UICONTROL Edit]**.

1. Edite as [configurações da conta](#account-settings):

   1. (Opcional) Edite os detalhes da conta.

   1. (Opcional) Clique em **[!UICONTROL Set Account Tracking]** e edite as configurações de rastreamento.

1. Clique em **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devem sincronizar os novos dados da conta com os da rede de anúncios. Isso acontece automaticamente uma vez por dia ou com mais frequência quando o Search, o Social e o Commerce detectam alterações na rede de anúncios.

## Atualizar tokens de acesso oAuth para contas de pesquisa {#refresh-oauth-tokens}

*Somente funções de gerente de conta de agência, gerente de conta da Adobe e administrador de usuário*

Se o Search, Social e Commerce acessar a conta usando o [protocolo de autorização OAuth](https://oauth.net/2/) e as credenciais da conta forem alteradas, ou se for necessário acesso adicional para oferecer suporte a novos recursos no Search, Social e Commerce, você deverá obter um novo token de acesso para a conta.

A equipe de conta da Adobe informará se novos recursos exigirem um novo token.

1. (Se você estiver conectado a outra conta para a mesma rede de anúncios no mesmo aplicativo do navegador) Faça logout de qualquer conta diferente da do anunciante.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta, clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais") e selecione **[!UICONTROL Edit]**.

1. Obter um novo token de acesso:

   1. Clique em **[!UICONTROL Get oAuth Token]**.

   1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta de anúncios do anunciante. A prática recomendada é usar as credenciais para o acesso da API à conta.

   1. Na tela de solicitação de permissão/acesso, clique no botão para confirmar a permissão.

   1. Copie a cadeia de caracteres de autenticação na janela pop-up que é aberta e cole-a no campo **[!UICONTROL oAuth Token]**.

1. Clique em **[!UICONTROL Post]**.

## Ativar ou desativar contas de rede de publicidade {#enable-disable-account}

*Somente funções de gerente de conta de agência, gerente de conta da Adobe e administrador de usuário*

Quando você habilita uma conta de rede de publicidade, o Search, Social e Commerce sincroniza dados de campanha com a conta (quando suportado) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.Quando você desabilita uma conta de rede de publicidade, o Search, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as visualizações e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está desativada. Posteriormente, é possível reativar a conta para retomar a atividade com ela.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Para alterar o status para uma única conta) Mantenha o cursor sobre o nome da conta, clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais") e selecione **[!UICONTROL Edit]**. Altere o **[!UICONTROL Status]** para *Habilitado* ou *Desabilitado* e clique em **[!UICONTROL Post]**.

   * (Para alterar o status de uma ou mais contas) Faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada conta.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Na barra de ferramentas acima da tabela de dados, clique em ![Ícone Ativar](/help/search-social-commerce/assets/activate.png "Ícone Ativar") para habilitar a conta ou ![Ícone Desativar](/help/search-social-commerce/assets/disable.png "Ícone Desativar") para desabilitá-la.

## Adicionar configurações de conta de rede {#account-settings}

>[!NOTE]
>
>Somente o gerente de conta da agência, o gerente de conta [!DNL Adobe] e os usuários administradores podem definir as configurações de conta.

### Detalhes da conta

**[!UICONTROL SE Account ID]:** (Todas as contas exceto as contas [!DNL Naver] e [!DNL Yandex]; editáveis somente para novas contas) A ID da conta atribuída pela rede de publicidade.

>[!NOTE]
>
>Contas de gerente de rede de publicidade não são suportadas aqui. Para identificar uma conta de gerente para [!DNL Microsoft Advertising] ou [!DNL Yandex], use o campo ID da Conta Principal ou Conta MCC, respectivamente. Para [configurar credenciais para uma [!DNL Google Ads] conta de gerente](/help/search-social-commerce/admin/manager-accounts.md), vá para [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, notifique a Equipe de conta da Adobe para que ela possa atualizar o mapeamento.

**[!UICONTROL Login Details]: \[Tipo de Logon\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] somente) Se autorizar logons na conta usando:

* *[!UICONTROL oAuth]* (o padrão): Para usar o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

* *[!UICONTROL Password]:* Para usar a senha do cliente.

Para contas do [!DNL Microsoft Advertising], somente logons autorizados do [!DNL oAuth] podem ser usados.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Todas as redes de anúncios, exceto [!DNL Naver]) O nome de logon ou a ID para habilitar o acesso à API para a conta.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-habilitado e todas as outras redes, exceto [!DNL Meta] e [!DNL Yandex]) O token da conta para autorizar logons usando o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Todas as redes de anúncios, exceto [!DNL Naver]) A senha da conta. Para contas habilitadas com senha em [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] e [!DNL Yandex], este campo é obrigatório. Para contas habilitadas para [!DNL oAuth], este campo é opcional; use-o quando quiser criptografar e salvar a senha para que o gerente de conta possa atualizar os tokens conforme necessário.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** (somente contas [!DNL Yandex]) A chave de acesso para a conta de desenvolvedor a ser usada.

**[!UICONTROL Currency]:** A abreviação da moeda usada na conta. Este campo é editável para novas contas [!DNL Naver]. Para todas as outras redes de pesquisa, o valor é preenchido automaticamente com a moeda configurada para a conta na rede de publicidade depois que você salva o registro.

**[!UICONTROL Landing Page Suffix]** contas ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente; opcional) Quaisquer parâmetros a serem anexados ao final das URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear.

Exemplo: `param1=value1&param2=value2`

As contas que usam o rastreamento de cliques do Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para Google) no sufixo. Contas com uma integração do Adobe Analytics devem usar o parâmetro de ID AMO (começando com `s_kwcid`). Se a conta tiver uma implementação de ID do AMO do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte os [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Este campo não é atualizado pela configuração de rastreamento [!UICONTROL Auto Upload].
>* Os sufixos de URL finais nos níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.

**Fuso Horário:** (Todas as redes de anúncios, exceto [!DNL Baidu] e [!DNL Yahoo! Display Network]) O fuso horário do anunciante. Este campo é editável e opcional para novas contas do [!DNL Naver]. Para todas as outras redes de pesquisa, o valor é preenchido automaticamente com o fuso horário configurado para a conta Search, Social, &amp; Commerce do anunciante depois de salvar o registro.

**Status:** O status da conta em Search, Social e Commerce:

* *Habilitado:* o Search, Social e Commerce sincroniza dados de campanha com a conta (quando há suporte) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.
* *Desabilitado:* Pesquisa, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as exibições e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está pausada. Posteriormente, você pode reativar a conta para retomar a atividade com ela.

**Modelo de Rastreamento** - ([!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] contas apenas; opcional) O modelo de rastreamento padrão para a conta, que especifica todos os redirecionamentos de domínio fora da aterrissagem e parâmetros de rastreamento, e também incorpora a URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

* Para incorporar o URL final:

   * ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente) Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte a [!DNL Microsoft Advertising]documentação[[!DNL Microsoft Advertising]  (](https://help.ads.microsoft.com/#apex/3/en/56799) somente) ou os parâmetros &quot;Somente modelo de rastreamento&quot; ([!DNL Google Ads] somente) na seção sobre &quot;Parâmetros [!DNL ValueTrack] disponíveis&quot; na [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] somente) Use o parâmetro `!{lpurl}` para indicar a URL da página de aterrissagem.

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

* Quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce prefixa automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.

>[!NOTE]
>
>* Para [!DNL Google Ads], evite usar macros, que não são substituídas por cliques de fontes que habilitam o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta da Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.

**[!UICONTROL Master Account ID]:** (somente contas [!DNL Microsoft Advertising]) a identificação de uma conta de agência/administração associada à conta.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] contas somente; opcional) uma conta de agência/administração associada à conta. Para remover uma associação existente, selecione &quot;[!UICONTROL No MCC Account]&quot;.

**[!UICONTROL Application ID]:** (somente contas [!DNL Yandex]) O token de desenvolvedor a ser usado para a conta. O mesmo token é usado para todas as contas [!DNL Yandex].

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) A ID numérica da campanha usada para pagar todas as campanhas de publicidade na conta.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) O token de desenvolvedor a ser usado para chamadas de API relacionadas a finanças, como para realocar dinheiro da carteira entre as campanhas do anunciante, conforme necessário para otimização de portfólio.

### Rastreamento de conta

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Somente para [!UICONTROL EF Redirect]) Não implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Formato S_kwcid:** (Contas [!DNL Google Ads] existentes para anunciantes com uma integração Adobe Advertising-Adobe Analytics e para as quais a ID do AMO (s_kwcid) ainda não foi migrada)

Essa conta usa o formato herdado para o código de rastreamento da ID do AMO, o que permite que a Adobe Advertising compartilhe dados sobre a conta com a Adobe Analytics. O [formato mais recente](/help/integrations/analytics/ids.md#amo-id-formats) inclui parâmetros para a ID da campanha e a ID do grupo de anúncios, que são necessários para relatar com precisão os níveis da campanha e do grupo de anúncios para o desempenho máximo de [!DNL Google Ads] campanhas e rascunhos e campanhas de experimentos no Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Se a conta precisar gerar relatórios nos níveis de campanha e grupo de anúncios, clique no ícone [!UICONTROL Edit] (lápis) e em **[!UICONTROL Migrate to new s_kwcid format]** para alterar para o novo formato. Para contas que não incluem esses tipos de campanha, a migração para o novo formato é opcional, mas recomendada.

Para obter instruções completas, consulte &quot;[Atualizar o código de rastreamento da ID do AMO para uma [!DNL Google Ads] conta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Nomes dos Conjuntos de Relatórios:** (Para EF Redirect com token somente; anunciantes com uma integração Adobe Advertising-Adobe Analytics; opcional) Um ou mais conjuntos de relatórios do Analytics para os quais o Search, o Social e o Commerce enviam dados coletados da rede de anúncios, incluindo classificações de entidade e dados de cliques da conta. Esse recurso está disponível somente para redes de anúncios compatíveis.

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve ser habilitada. Além disso, a conta do Analytics do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com a equipe de conta da Adobe.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de anúncios](ad-network-account-about.md)
>* [Gerenciar contas do centro de comércio](merchant-account-manage.md)
>* [Atualize o código de rastreamento s_kwcid de uma  [!DNL Google Ads] conta](update-amo-id-google.md)
