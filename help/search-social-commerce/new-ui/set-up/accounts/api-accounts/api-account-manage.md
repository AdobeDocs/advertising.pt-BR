---
title: (Nova interface do usuário) Gerenciar contas de rede de anúncios
description: Saiba como configurar e gerenciar detalhes da conta na nova interface para uma rede de anúncios sincronizada por meio da API da rede de anúncios.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar contas de rede de anúncios por meio da conexão de API

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*recurso do Beta*

<!-- Move out info about Naver into a separate page -->

A seguir estão instruções para gerenciar contas de rede de anúncios que o Search, Social e Commerce sincroniza usando a API da rede de anúncios.

<!-- Move out info about Naver into a separate page -->

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Criar detalhes da conta de rede de publicidade {#create-account}

Para habilitar a sincronização de uma conta, você deve criar um registro de conta correspondente contendo as credenciais de acesso e as opções de rastreamento da conta e com o status *habilitado*.

>[!NOTE]
>
>Para criar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Clique em **[!UICONTROL Create Account]**.

1. Clique no nome da rede de publicidade e clique em **[!UICONTROL Next]**.

1. (Todas as redes de anúncios, exceto [!DNL Yandex]) Faça logon na rede de anúncios usando as credenciais do anunciante. Selecione a opção &quot;Rastreamento de conta para esta conta&quot;. Em seguida, no canto superior direito, clique em **[!UICONTROL Next]**.

1. Especifique as [configurações da conta](#account-settings-api):

   1. Na guia **[!UICONTROL Select Accounts]**, especifique as configurações gerais da conta. Para contas do [!DNL Yandex], especifique as credenciais da conta.

   1. Clique na guia **[!UICONTROL Setup Tracking]** e insira as configurações de rastreamento.

   1. (Anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e selecione todos os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

1. Clique em **[!UICONTROL Save]**.

   Os dados recentes de custos e cliques de todas as campanhas na conta são atualizados na Pesquisa, no Social e no Commerce por hora. Por padrão, os dados estão disponíveis nos últimos 5 a 10 dias, dependendo da rede de anúncios. No entanto, quando necessário, a equipe de lançamento do projeto pode recuperar dados dos últimos 60 dias.

## Editar detalhes da conta de rede de publicidade {#edit-account}

Para autenticar novamente as configurações da conta para atualizar a conexão ou as permissões de atualização, habilite ou desabilite a atividade em uma conta, altere os parâmetros de rastreamento padrão em uma conta ou altere os conjuntos de relatórios [!DNL Analytics] a serem usados para rastreamento e relatórios, e edite os detalhes da conta.

>[!NOTE]
>
>Para editar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

1. Edite as [configurações da conta](#account-settings-api):

   1. (Opcional) Na guia **[!UICONTROL Account Details]**, edite os detalhes da conta.

   1. (Opcional) Clique na guia **[!UICONTROL Setup Tracking]** e edite as configurações de rastreamento.

   1. (Opcional; anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md)) Clique na guia **[!UICONTROL Set up Adobe Analytics]** e edite os conjuntos de relatórios [!DNL Analytics] para usar no rastreamento e na atividade de campanha de relatórios.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Clique em **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devem sincronizar os novos dados da conta com os da rede de anúncios. Isso acontece automaticamente uma vez por dia ou com mais frequência quando o Search, o Social e o Commerce detectam alterações na rede de anúncios.

## Autenticar novamente uma conta de rede de publicidade {#reauthenticate}

Para atualizar a conexão de rede de publicidade ou as permissões de atualização da conta, autentique novamente a conta.

1. (Se você estiver conectado a outra conta para a mesma rede de anúncios no mesmo aplicativo do navegador) Faça logout de qualquer conta diferente da do anunciante.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

1. Na guia **[!UICONTROL Account Details]**, clique em **[!UICONTROL Re authenticate]** e faça logon na rede de publicidade usando as credenciais do anunciante.

1. Clique em **[!UICONTROL Save]**.

## Ativar ou desativar contas de rede de publicidade {#enable-disable-account}

Quando você habilita uma conta de rede de publicidade, o Search, Social e Commerce sincroniza dados de campanha com a conta (quando suportado) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios. Quando você desativa uma conta de rede de publicidade, o Search, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as visualizações e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está desativada. Posteriormente, é possível reativar a conta para retomar a atividade com ela.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Da exibição [!UICONTROL Accounts]):

      * (Para habilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Activate]** na barra de ferramentas de ações em massa.

      * (Para desabilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Pause]** na barra de ferramentas de ações em massa.

   * (Nas configurações da conta):

      1. Selecione a conta de uma das seguintes maneiras:

         * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

         * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

      1. Na guia **[!UICONTROL Account Details]**, desative o **[!UICONTROL Account enabled]**.

      1. Clique em **[!UICONTROL Save]**.

## Adicionar configurações de conta de rede {#account-settings-api}

As configurações da conta variam de acordo com a rede de anúncios. Talvez você não veja todas as configurações abaixo.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Guia [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, peça à sua Equipe de conta da Adobe para atualizar o mapeamento.

**[!DNL [Contas de Rede de Anúncios]]:** (Visível enquanto você está criando uma conta) A conta de rede de anúncios a ser sincronizada.

**[Detalhes do Logon]:** (somente contas do Yandex) As credenciais de conta a serem usadas:

* **[!UICONTROL Login]:** O nome ou ID de logon para habilitar o acesso à API para a conta.

* **[!UICONTROL Password]:** A senha da conta.

* **[!UICONTROL Access Key]:** A chave de acesso para a conta de desenvolvedor a ser usada.

* **[!UICONTROL Application ID]:** O token de desenvolvedor a ser usado para a conta. O mesmo token é usado para todas as contas [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) A ID numérica da campanha usada para pagar todas as campanhas de publicidade na conta.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) O token de desenvolvedor a ser usado para chamadas de API relacionadas a finanças, como para realocar dinheiro da carteira entre as campanhas do anunciante, conforme necessário para otimização de portfólio.

**[!UICONTROL Network Account ID]:** (Todas as redes de anúncios, exceto [!DNL Yandex] A ID de conta atribuída pela rede de anúncios.

>[!NOTE]
>
>Contas de gerente de rede de publicidade não são suportadas aqui. Para identificar uma conta de gerente para [!DNL Microsoft Advertising], use o campo ID da Conta Principal ou Conta MCC, respectivamente. Para [configurar credenciais para uma [!DNL Google Ads] conta de gerente](/help/search-social-commerce/admin/manager-accounts.md), vá para [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (Somente leitura) A abreviação da moeda usada na conta. Esse valor é preenchido automaticamente com a moeda configurada para a conta na rede de publicidade depois que você salva o registro.

**[!UICONTROL Time Zone]:** O fuso horário do anunciante. Esse valor é preenchido automaticamente com o fuso horário configurado para a conta Search, Social, &amp; Commerce do anunciante depois de salvar o registro.

**[!UICONTROL Login]:** (Somente leitura) A conta de usuário usada para fazer logon na conta.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** O Search, Social e Commerce sincroniza dados de campanha com a conta (quando há suporte) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.

## Guia [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Se o rastreamento deve ser habilitado ou não, use o serviço de rastreamento de conversão do Adobe Advertising. Esse método gera IDs exclusivas de rastreamento de cliques e redireciona os usuários para o servidor do Adobe Advertising para fins de rastreamento antes de enviá-los para a página inicial do cliente. Esse método tem opções de rastreamento padrão que você pode personalizar opcionalmente e também pode especificar parâmetros para anexar a cada URL.

Para habilitar este recurso, ative **[Habilitar o rastreamento]**.

>[!NOTE]
>
>* Se você alterar essa configuração, deverá gerar novamente as URLs de rastreamento da conta.
>* As opções de rastreamento no nível da campanha substituem as configurações no nível da conta.

**[!UICONTROL Tracking Type]:** (quando o rastreamento de Search, Social e Commerce está habilitado) O método de redirecionamento de usuários finais para a URL final ou de destino. A opção selecionada é aplicável a todas as unidades de oferta na conta ou campanha. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante, e a configuração padrão no nível da campanha é herdada das configurações da conta.

* *[!UICONTROL Standard]:* Para redirecionar o usuário final para a URL especificada.

* *[!UICONTROL Token]:* Para redirecionar o usuário final para a URL e também gravar a ID de Pesquisa, Social e Commerce para o clique (`ef_id`) como um parâmetro de sequência de consulta, que é usado como um token. Escolha esta opção se for relatar transações offline, se quiser que o Search, Social e Commerce troquem dados com o Adobe Analytics ou se quiser rastrear todas as conversões que ocorrem nos navegadores [!DNL Apple Safari].

>[!NOTE]
>
>* Se você alternar de [!UICONTROL Standard] para [!UICONTROL Token], ou vice-versa, será necessário regenerar as URLs de rastreamento da conta.
>* Você pode substituir a configuração no nível da conta no nível da campanha.

**[!UICONTROL Auto Update]:** (Quando o rastreamento de Pesquisa, Social e Commerce está habilitado) Padroniza as URLs de rastreamento para compatibilidade entre navegadores e servidores. O Search, Social e Commerce faz o upload do seguinte automaticamente para a rede de publicidade durante a próxima sincronização: (a) Parâmetros de rastreamento de Search, Social e Commerce para modelos de rastreamento e os mesmos parâmetros anexados aos URLs finais ou (b) novos URLs de destino incorporados ao código de rastreamento do Search, Social e Commerce. Para anunciantes com uma [integração Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=pt-BR) e uma configuração de ID AMO do lado do servidor (s_kwcid), o carregamento também inclui [parâmetros de ID do AMO](/help/integrations/analytics/ids.md#amo-id) para suas contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising]. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante. Você pode substituir a configuração no nível da conta no nível da campanha.

Os URLs de rastreamento são atualizados diariamente apenas para entidades que estão fora de sincronia (ou seja, novas entidades que foram adicionadas e entidades existentes cujas propriedades foram alteradas). Portanto, se você alterar essa configuração de desativado para ativado para um anunciante/conta/campanha existente, os URLs de rastreamento não serão atualizados para entidades existentes que já estão em sincronia. Para adicionar rastreamento aos URLs de entidades existentes em sincronia, entre em contato com a equipe de conta da Adobe e solicite um processo de sincronização manual e único. O processo de upload automático lidará com alterações futuras.

**[!UICONTROL URL Encoding]:** (Quando o rastreamento Search, Social, &amp; Commerce está habilitado; contas somente com URLs de destino) Codifica a URL base dentro da barra de endereços do navegador do usuário final (como `%3D` em vez de `=`):

**[!UICONTROL Tracking Level]:** (Quando o rastreamento de Pesquisa, Social e &amp; Commerce está habilitado; disponível nos níveis de conta e campanha; não aplicável a redes de anúncios habilitadas para rastreamento paralelo) O nível no qual os cliques e as receitas devem ser rastreados adicionando um redirecionamento (quando relevante) e anexando parâmetros às URLs relevantes:

* *[!UICONTROL Keyword]:* Para rastrear dados somente no nível da palavra-chave. Não disponível para [!DNL Yandex].

* *[!UICONTROL Ad]:* Para rastrear dados somente no nível do anúncio. Não disponível para [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* Para rastrear dados nos níveis de palavra-chave e anúncio. Não disponível para [!DNL Naver] e [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** contas ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente; opcional) Quaisquer parâmetros a serem anexados ao final das URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear.

Exemplo: `param1=value1&param2=value2`

As contas que usam o rastreamento de cliques do Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para Google) no sufixo. Contas com uma integração do Adobe Analytics devem usar o parâmetro de ID AMO (começando com `s_kwcid`). Se a conta tiver uma implementação de ID do AMO do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte os [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Este campo não é atualizado pela configuração de rastreamento [!UICONTROL Auto Update].
>* Os sufixos de URL finais nos níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.

**URL de Acompanhamento de Conta**: ([!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] contas somente; opcional) O modelo de rastreamento padrão para a conta, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e também incorpora a URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

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

## Guia [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes com [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md); opcional) Um ou mais conjuntos de relatórios do Analytics para os quais Search, Social e Commerce enviam dados coletados da rede de publicidade, incluindo classificações de entidade e dados de cliques da conta. Esse recurso está disponível somente para redes de anúncios compatíveis.

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve ser habilitada. Além disso, a conta [!DNL Analytics] do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com a equipe de conta da Adobe.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de anúncios](../ad-network-account-about.md)
>* [Gerenciar contas do centro de comércio](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Atualize o código de rastreamento s_kwcid de uma  [!DNL Google Ads] conta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
