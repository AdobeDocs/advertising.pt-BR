---
title: Gerenciar contas de rede de publicidade
description: Saiba como configurar e gerenciar detalhes de uma conta de rede de anúncios.
exl-id: fd8b38bd-24d0-488c-9e57-a516f5ae67ac
feature: Search Campaign Management
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '2086'
ht-degree: 0%

---

# Gerenciar contas de rede de publicidade

Veja a seguir instruções para criar e editar detalhes de conta de rede de anúncios, atualizar a [!DNL oAuth] token para uma conta e desativando contas.

## Criar detalhes da conta de rede de publicidade {#create-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Para habilitar a sincronização ou o rastreamento de uma conta, você deve criar um registro de conta correspondente contendo as credenciais de acesso e as opções de rastreamento da conta e com o status *ativo*. Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Para criar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Especifique a [configurações da conta](#account-settings):

   1. Clique no nome da rede de publicidade e clique em **[!UICONTROL Next]**.

   1. No **[!UICONTROL Account Details]** insira os detalhes da conta.

      Para redes de anúncios que usam o tipo de autorização de logon &quot;[!UICONTROL oAuth],&quot; permitir que o Search, Social e Commerce acessem a conta usando o [Protocolo de autorização OAuth](https://oauth.net/2/):

      1. Insira o **[!UICONTROL Login]** para a conta, opcionalmente informe a senha e, em seguida, clique em **[!UICONTROL Authenticate]**.

         A prática recomendada é usar o logon para acessar a conta pela API. Digite a senha quando quiser criptografá-la e salvá-la, para que a equipe da conta do Adobe possa atualizar os tokens conforme necessário.

      1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta de anúncios do anunciante. A prática recomendada é usar as credenciais para o acesso da API à conta.

      1. Na tela de solicitação de permissão/acesso, clique no botão para confirmar a permissão.

      1. Copie a string de autenticação na janela pop-up que é aberta e cole a string na **[!UICONTROL oAuth Token]** campo.

      1. Especifique os detalhes restantes da conta.

   1. Clique em **[!UICONTROL Set Account Tracking]** e insira as configurações de rastreamento.

1. Clique em **[!UICONTROL Post]**.

   Os dados recentes de custo e clique para todas as campanhas na conta estão disponíveis em Pesquisa, Social e Comércio em cerca de 24 horas. Por padrão, os dados estão disponíveis nos últimos 5 a 10 dias, dependendo da rede de anúncios. No entanto, quando necessário, a equipe de lançamento do projeto pode recuperar dados dos últimos 60 dias.

## Editar detalhes da conta de rede de publicidade {#edit-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Se as credenciais da conta forem alteradas, você desejará alterar os parâmetros de rastreamento padrão em uma conta, ou ativar ou desativar a atividade em uma conta e, em seguida, editar os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta e clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais")e selecione **[!UICONTROL Edit]**.

1. Edite o [configurações da conta](#account-settings):

   1. (Opcional) Edite os detalhes da conta.

   1. (Opcional) Clique em **[!UICONTROL Set Account Tracking]** e edite as configurações de rastreamento.

1. Clique em **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >A Search, Social e Commerce precisa sincronizar os novos dados da conta com os da rede de anúncios. Isso acontece automaticamente uma vez por dia ou com mais frequência quando o Search, Social e Commerce detecta alterações na rede de anúncios.

## Atualizar tokens de acesso oAuth para contas de pesquisa {#refresh-oauth-tokens}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Se as opções Pesquisar, Social e Comércio acessarem a conta usando o [Protocolo de autorização OAuth](https://oauth.net/2/) e as credenciais da conta forem alteradas, ou se for necessário acesso adicional para oferecer suporte a novos recursos no Search, Social e Commerce, você deverá obter um novo token de acesso para a conta.

Sua equipe de conta do Adobe informará se novos recursos exigirem um novo token.

1. (Se você estiver conectado a outra conta para a mesma rede de anúncios no mesmo aplicativo do navegador) Faça logout de qualquer conta diferente da do anunciante.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta e clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais")e selecione **[!UICONTROL Edit]**.

1. Obter um novo token de acesso:

   1. Clique em **[!UICONTROL Get oAuth Token]**.

   1. (Se você não tiver feito logon na conta do anunciante) Faça logon na conta de anúncios do anunciante. A prática recomendada é usar as credenciais para o acesso da API à conta.

   1. Na tela de solicitação de permissão/acesso, clique no botão para confirmar a permissão.

   1. Copie a string de autenticação na janela pop-up que é aberta e cole a string na **[!UICONTROL oAuth Token]** campo.

1. Clique em **[!UICONTROL Post]**.

## Ativar ou desativar contas de rede de publicidade {#enable-disable-account}

*Somente funções de gerente de conta da agência, gerente de conta do Adobe e administrador de usuário*

Quando você habilita uma conta de rede de publicidade, o Search, Social e Commerce sincroniza dados de campanha com a conta (quando há suporte) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.Quando você desabilita uma conta de rede de publicidade, o Search, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as visualizações e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está desativada. Posteriormente, é possível reativar a conta para retomar a atividade com ela.

1. No menu principal, clique em **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. No submenu, clique em **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Para alterar o status para uma única conta) Mantenha o cursor sobre o nome da conta, clique em ![Mais](/help/search-social-commerce/assets/more-filters.png "Mais")e selecione **[!UICONTROL Edit]**. Altere o **[!UICONTROL Status]** para *Ativado* ou *Desabilitado* e clique em **[!UICONTROL Post]**.

   * (Para alterar o status de uma ou mais contas) Faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada conta.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Na barra de ferramentas acima da tabela de dados, clique em ![Ícone Ativar](/help/search-social-commerce/assets/activate.png "Ícone Ativar") para habilitar a conta ou ![Ícone Desativar](/help/search-social-commerce/assets/disable.png "Ícone Desativar") para desativar a conta.

## Adicionar configurações de conta de rede {#account-settings}

>[!NOTE]
>
>Somente gerente de conta da agência, [!DNL Adobe] o gerente de conta e os usuários administradores podem definir as configurações da conta.

### Detalhes da conta

**[!UICONTROL SE Account ID]:** (Todas as contas exceto [!DNL Naver] e [!DNL Yandex] contas; editável somente para novas contas) A ID da conta atribuída pela rede de publicidade.

>[!NOTE]
>
>Contas de gerente de rede de publicidade não são suportadas aqui. Para identificar uma conta de gerente para [!DNL Microsoft Advertising] ou [!DNL Yandex], use o campo ID de conta Principal ou Conta MCC, respectivamente. Para [configurar credenciais para um [!DNL Google Ads] conta do gerente](/help/search-social-commerce/admin/manager-accounts.md), vá para [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, notifique a Equipe de conta do Adobe para que ela possa atualizar o mapeamento.

**[!UICONTROL Login Details]: \[Tipo de logon\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] somente) Se autorizar logons na conta usando:

* *[!UICONTROL oAuth]* (o padrão): Para usar a variável [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

* *[!UICONTROL Password]:* Para usar a senha do cliente.

Para [!DNL Microsoft Advertising] contas, somente [!DNL oAuth]logons autorizados podem ser usados.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Todas as redes de publicidade, exceto [!DNL Naver]) O nome de logon ou a ID para habilitar o acesso da API à conta.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-habilitado e todas as outras redes, exceto para [!DNL Baidu], [!DNL Meta], e [!DNL Yandex]) O token da conta para autorizar logons usando o [[!DNL OAuth] protocolo de autorização](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Todas as redes de publicidade, exceto [!DNL Naver]) A senha da conta. Para contas habilitadas com senha em [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], e [!DNL Yandex], esse campo é obrigatório. Para [!DNL oAuth]Contas habilitadas para, esse campo é opcional; use-o quando desejar criptografar e salvar a senha para que o gerente de conta possa atualizar tokens conforme necessário.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] e [!DNL Yandex] contas somente) A chave de acesso da conta de desenvolvedor a ser usada.

**[!UICONTROL Currency]:** A abreviação da moeda usada na conta. Este campo é editável para novos [!DNL Naver] contas. Para todas as outras redes de pesquisa, o valor é preenchido automaticamente com a moeda configurada para a conta na rede de publicidade depois que você salva o registro.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente contas do; opcional) Quaisquer parâmetros a serem anexados ao final dos URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear.

Exemplo: `param1=value1&param2=value2`

As contas que usam o rastreamento de cliques do Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para Google) no sufixo. As contas com uma integração do Adobe Analytics devem usar o parâmetro da ID do AMO (começando com `s_kwcid`). Se a conta tiver uma implementação de ID do AMO do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte a [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Este campo não é atualizado pelo [!UICONTROL Auto Upload] configuração de rastreamento.
>* Os sufixos de URL finais nos níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.

**Fuso Horário:** (Todas as redes de anúncios, exceto [!DNL Baidu] e [!DNL Yahoo! Display Network]) O fuso horário do anunciante. Este campo é editável e opcional para novos [!DNL Naver] contas. Para todas as outras redes de pesquisa, o valor é preenchido automaticamente com o fuso horário configurado para a conta de Pesquisa, Social e Comércio do anunciante depois de salvar o registro.

**Status:** O status da conta em Pesquisa, Social e Comércio:

* *Ativado:* Search, Social e Commerce sincroniza dados de campanha com a conta (quando suportado) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.
* *Desabilitado:* Search, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as exibições e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está pausada. Posteriormente, você pode reativar a conta para retomar a atividade com ela.

**Modelo de rastreamento** - ([!DNL Google Ads], [!DNL Microsoft Advertising], e [!DNL Yahoo! Japan Ads] somente contas; opcional) o modelo de rastreamento padrão para a conta, que especifica todos os redirecionamentos e parâmetros de rastreamento de domínio fora da página de aterrissagem, e também incorpora o URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

* Para incorporar o URL final:

   * ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente) Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte o ([!DNL Microsoft Advertising] somente) [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] somente) os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Disponível [!DNL ValueTrack] Parâmetros&quot; na [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] somente) Usar o parâmetro `!{lpurl}` para indicar o URL da landing page.

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

* Quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

>[!NOTE]
>
>* Para [!DNL Google Ads], evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] contas somente) A ID de uma conta de agência/gerenciamento associada à conta.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] contas somente; opcional) Uma conta de agência/administração associada à conta. Para remover uma associação existente, selecione &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] contas somente) O token do desenvolvedor a ser usado para a conta. O mesmo token é usado para todos [!DNL Yandex] contas.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] contas com a configuração Conta compartilhada desativada somente; opcional) a ID numérica da campanha que será usada para pagar todas as campanhas de publicidade na conta.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] contas com a configuração Conta compartilhada desativada somente; opcional) O token do desenvolvedor a ser usado para chamadas de API relacionadas a finanças, como para realocar dinheiro da carteira entre as campanhas do anunciante, conforme necessário para otimização de portfólio.

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

**[!UICONTROL Track Product Group]:** (Para [!UICONTROL EF Redirect] somente) Não implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Formato S_kwcid** - (Existente [!DNL Google Ads] contas para anunciantes com uma integração Adobe Advertising-Adobe Analytics e para as quais a ID do AMO (s_kwcid) ainda não foi migrada)

Essa conta usa o formato herdado para o código de rastreamento da ID do AMO, o que permite que o Adobe Advertising compartilhe dados sobre a conta com a Adobe Analytics. A variável [formato mais recente](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) inclui parâmetros para a ID da campanha e a ID do grupo de anúncios, que são necessários para relatar com precisão os níveis da campanha e do grupo de anúncios para [!DNL Google Ads] desempenho máximo de campanhas e rascunhos e campanhas de experimentos no Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Se essa conta precisar de relatórios nos níveis de campanha e grupo de publicidade, clique no link [!UICONTROL Edit] (lápis) e **[!UICONTROL Migrate to new s_kwcid format]** para alterar para o novo formato. Para contas que não incluem esses tipos de campanha, a migração para o novo formato é opcional, mas recomendada.

Para obter instruções completas, consulte &quot;[Atualizar o código de rastreamento da ID do AMO para um [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Nomes dos conjuntos de relatórios** - (Para redirecionamento EF somente com token; anunciantes com integração Adobe Advertising-Adobe Analytics; opcional) Um ou mais conjuntos de relatórios do Analytics para os quais o Search, Social e Commerce envia dados coletados da rede de anúncios, incluindo classificações de entidade e dados de cliques da conta. Esse recurso está disponível somente para redes de anúncios compatíveis.

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; deve ser ativado. Além disso, a conta do Analytics do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com o Gerente de conta do Adobe.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de publicidade](ad-network-account-about.md)
>* [Gerenciar contas do centro de comércio](merchant-account-manage.md)
>* [Atualize o código de rastreamento s_kwcid de uma [!DNL Google Ads] account](update-amo-id-google.md)
