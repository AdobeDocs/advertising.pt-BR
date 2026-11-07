---
title: (Nova interface do usuário) Gerenciar contas de rede de anúncios
description: Saiba como configurar e gerenciar detalhes da conta na nova interface para uma rede de anúncios sincronizada por meio da API da rede de anúncios.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 0%
---
# (Nova interface do usuário) Gerenciar contas de rede de anúncios por meio da conexão de API

Estas instruções explicam como gerenciar contas de rede de anúncios que o Search, Social e Commerce sincroniza por meio da API, incluindo autenticação, atualização de conexão e verificações de status.

Para criar, editar ou reautenticar contas, é necessário ter permissão para editar contas.

Para obter detalhes sobre a funcionalidade disponível para cada rede de anúncios, consulte &quot;[Inventário Suportado](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Sobre a exibição [!UICONTROL Accounts] {#account-view-about}

A exibição [!UICONTROL Manage] > [!UICONTROL Accounts] lista todas as contas de rede de anúncios na exibição filtrada para a conta de anunciante selecionada. Clique em um nome de conta para abrir a exibição [!UICONTROL Campaigns] filtrada para essa conta.

### Status de autenticação e acesso da conta {#authentication-status}

Os detalhes de autenticação e acesso variam de acordo com a rede de publicidade e as informações disponíveis para a conta. Uma conta habilitada ou autenticada com êxito ainda pode ter permissões ausentes.

As colunas a seguir mostram o status da conta, a autenticação e os detalhes de acesso:

* **[!UICONTROL Status]:** O status operacional da conta, que é separado de sua autenticação e permissões. Uma conta habilitada pode sincronizar dados com a rede de anúncios e usar recursos de gerenciamento e otimização de conta compatíveis. Uma conta desativada interrompe a atividade no Search, Social e Commerce. A exibição do status da conta usa um indicador verde para **[!UICONTROL Enabled]**, um indicador vermelho para **[!UICONTROL Disabled]** e um indicador âmbar para **[!UICONTROL Pending]**. Você pode [habilitar ou desabilitar contas](#enable-disable-account) da exibição ou das configurações da conta.

* **[!UICONTROL Authenticated]:** Se a conta está autenticada:

  * **[!UICONTROL Yes]:** A conta está autenticada.

  * **[!UICONTROL No]:** A conta não está autenticada. Quando um erro de autenticação estiver disponível, mantenha o cursor sobre o ícone de aviso vermelho para exibir o erro.

  * **[!UICONTROL Not Applicable]:** A autenticação não se aplica porque você carrega dados para a conta em vez de se conectar por meio de uma API.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]** ou **[!UICONTROL Expired]:** Um aviso de expiração de token substitui **[!UICONTROL Yes]** quando as informações de expiração estão disponíveis e o token expira em 14 dias ou menos ou já expirou. Clique no ícone de aviso para exibir os detalhes de acesso da conta e [autenticar novamente](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** (somente contas [!DNL Google Ads]) A identificação da conta de gerente associada usada para carregamentos de conversão entre contas. Quando um erro está disponível para a conta do gerente, um ícone de aviso é exibido ao lado da ID. Para visualizar o erro, mantenha o cursor sobre o ícone. As credenciais da conta de gerente são separadas das credenciais da conta da rede de publicidade. Para adicionar ou atualizar credenciais de conta de gerente, use **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. Consulte &quot;[Gerenciar contas de gerente](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)&quot;.

* **[!UICONTROL Access Level]:** O nível de acesso da conta reportada, como **[!UICONTROL Full]**, **[!UICONTROL Limited]**, **[!UICONTROL None]** ou **[!UICONTROL Not Applicable]** quando não há um valor de nível de acesso disponível.

  Quando as permissões estiverem ausentes, clique no ícone de aviso para exibir os detalhes de acesso da conta. A seção **[!UICONTROL Access]** lista permissões como **[!UICONTROL Granted]** ou **[!UICONTROL Missing]**. Quando os detalhes do impacto estiverem disponíveis, a seção **[!UICONTROL Not working]** listará a funcionalidade afetada. Para [autenticar novamente](#reauthenticate) e atualizar permissões, clique em **[!UICONTROL Update Access]**.

### Ações disponíveis

As ações disponíveis dependem das suas permissões e do tipo de conta.

* [Criar detalhes da conta de rede de publicidade](#create-account)

* [Editar detalhes da conta de rede de publicidade](#edit-account)

* [Autenticar novamente uma conta de rede de publicidade](#reauthenticate)

* [Ativar ou desativar contas de rede de publicidade](#enable-disable-account)

* [Sincronizar dados da conta com a rede de publicidade](sync-api-accounts.md)

* [Exibir um gráfico de desempenho na exibição [!UICONTROL Accounts]](#account-performance-graph)

* [Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Accounts]](#account-reports)

## Criar detalhes da conta de rede de publicidade {#create-account}

Para habilitar a sincronização de uma conta, você deve criar um registro de conta correspondente contendo as credenciais de acesso e as opções de rastreamento da conta e com o status *habilitado*.

>[!NOTE]
>
>Para criar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Clique em **[!UICONTROL Create Account]**.

1. Clique no nome da rede de publicidade para abrir a configuração da conta.

1. (Todas as redes de anúncios, exceto [!DNL ChatGPT Ads] e [!DNL Yandex]) Na guia **[!UICONTROL Authenticate]**, conclua o logon na janela pop-up usando as credenciais do anunciante e conceda acesso à conta solicitada.

   A tela de instalação é atualizada automaticamente e exibe **[!UICONTROL Authentication Successful]** quando a autenticação é bem-sucedida. Se precisar reabrir a janela de logon, clique em **[!UICONTROL Open login again]**. Se o navegador bloquear a janela, edite as configurações do navegador para permitir pop-ups para o site.

   Para [!DNL Meta Ads], um aviso identifica as permissões ausentes e seu impacto. Autenticação bem-sucedida não significa necessariamente que todas as permissões solicitadas foram concedidas.

   Clique em **[!UICONTROL Next]** para continuar.

1. Especifique as [configurações da conta](#account-settings-api) em cada guia disponível. Para contas autenticadas em um pop-up, selecione a conta a ser sincronizada de **[!UICONTROL Linked Ad Accounts]** na guia **[!UICONTROL Select Accounts]**.

1. Clique em **[!UICONTROL Save]**.

   Os dados recentes de custos e cliques de todas as campanhas na conta são atualizados na Pesquisa, no Social e no Commerce por hora. Por padrão, os dados estão disponíveis nos últimos 5 a 10 dias, dependendo da rede de anúncios. No entanto, quando necessário, a equipe de lançamento do projeto pode recuperar dados dos últimos 60 dias.

## Editar detalhes da conta de rede de publicidade {#edit-account}

Para habilitar ou desabilitar a atividade em uma conta, alterar os parâmetros de rastreamento padrão em uma conta ou alterar os conjuntos de relatórios [!DNL Analytics] a serem usados para rastreamento e relatórios, edite os detalhes da conta. Para atualizar a conexão ou as permissões de atualização, você pode [autenticar novamente a conta](#reauthenticate) nas configurações da conta ou no modo de exibição [!UICONTROL Accounts].

>[!NOTE]
>
>Para editar uma conta real na rede de publicidade, vá para o site da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Selecione a conta de uma das seguintes maneiras:

   * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

   * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

1. Edite as [configurações da conta](#account-settings-api) nas guias disponíveis.

1. Clique em **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devem sincronizar os novos dados da conta com os da rede de anúncios. Isso acontece automaticamente uma vez por dia ou com mais frequência quando o Search, o Social e o Commerce detectam alterações na rede de anúncios.

## Autenticar novamente uma conta de rede de publicidade {#reauthenticate}

*Para contas que usam autenticação pop-up; não aplicável a [!DNL ChatGPT Ads] ou [!DNL Yandex] contas*

Para atualizar a conexão de rede de publicidade ou as permissões de atualização da conta, autentique novamente a conta.

1. (Se você estiver conectado a outra conta para a mesma rede de anúncios no mesmo aplicativo do navegador) Faça logout de qualquer conta diferente da do anunciante.

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Abra a autenticação de uma das seguintes maneiras:

   * (Quando o valor **[!UICONTROL Authenticated]** da conta for **[!UICONTROL No]**) Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Re authenticate]**, quando disponível.

   * (Quando um aviso de expiração de token for exibido) Clique no ícone de aviso na coluna **[!UICONTROL Authenticated]** e clique em **[!UICONTROL Reauthenticate]**.

   * (Quando as permissões estiverem ausentes) Clique no ícone de aviso na coluna **[!UICONTROL Access Level]** e clique em **[!UICONTROL Update Access]**.

   * (Nas configurações da conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa, ou mantenha o cursor sobre o nome da conta, clique em **...** e clique em **[!UICONTROL Edit]**. Na guia **[!UICONTROL Account Details]**, em **[!UICONTROL Account Authentication]**, clique em **[!UICONTROL Re authenticate]**.

1. Conclua o logon na janela pop-up usando as credenciais do anunciante e conceda acesso à conta solicitada.

   O novo token de acesso é salvo automaticamente quando a reautenticação é bem-sucedida. Se você também alterar outras configurações da conta, clique em **[!UICONTROL Save]** para salvar essas alterações.

   Para [!DNL Meta Ads], uma mensagem de informação identifica todas as permissões que ainda estão ausentes após a reautenticação bem-sucedida. Para identificar a funcionalidade afetada, reveja os [detalhes de acesso](#authentication-status).

## Ativar ou desativar contas de rede de publicidade {#enable-disable-account}

Quando você habilita uma conta de rede de publicidade, o Search, Social e Commerce sincroniza dados de campanha com a conta (quando suportado) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios. Quando você desativa uma conta de rede de publicidade, o Search, Social e Commerce interrompe todas as atividades na conta. Os dados coletados enquanto a conta estava ativa ainda são armazenados, mas as visualizações e os relatórios do gerenciamento de campanhas não incluem dados para o período em que a conta está desativada. Posteriormente, é possível reativar a conta para retomar a atividade com ela.

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Da exibição [!UICONTROL Accounts]):

     * (Para habilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Enable]** na barra de ferramentas de ações em massa.

     * (Para desabilitar a conta) Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Disable]** na barra de ferramentas de ações em massa.

   * (Nas configurações da conta):

     1. Selecione a conta de uma das seguintes maneiras:

        * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

        * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

     1. Na guia **[!UICONTROL Account Details]**, ative **[!UICONTROL Account Enabled]** para habilitar a conta, ou desative-a para desabilitá-la.

     1. Clique em **[!UICONTROL Save]**.

## Exibir um gráfico de desempenho na exibição [!UICONTROL Accounts] {#account-performance-graph}

Abra e configure um gráfico de desempenho com até três métricas totalizadas em contas na exibição filtrada para o intervalo de datas e a moeda especificados.

### Exibir um gráfico de desempenho

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Especifique o intervalo de datas e aplique filtros para as contas cujo desempenho deseja exibir.

1. Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Use **[!UICONTROL Currency]** e **[!UICONTROL Metrics]** para especificar a moeda e até três métricas a serem incluídas no gráfico.

### Ocultar um gráfico de desempenho visível

* Acima da tabela de dados, clique em ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Gerenciar relatórios de visualização de dados da visualização [!UICONTROL Accounts] {#account-reports}

Gere um relatório que inclua as linhas de dados de uma ou mais contas na exibição [!UICONTROL Accounts] e baixe o relatório como um arquivo de planilha do Microsoft Excel (formato XLSX). O relatório inclui as colunas visíveis na exibição para o intervalo de datas especificado.

É possível excluir relatórios concluídos e relatórios que não foram gerados.

### Gerar um relatório com as linhas de dados filtradas

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Especifique o intervalo de datas e aplique filtros para os dados que deseja baixar.

1. Especifique as contas cujos dados você deseja baixar:

   * Para baixar dados de contas específicas, marque as caixas de seleção ao lado das contas.

   * Para baixar dados de todas as contas na exibição filtrada, deixe todas as caixas de seleção desmarcadas.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na caixa de diálogo [!UICONTROL Grid Reports], mantenha o **[!UICONTROL Report Name]** padrão ou insira outro nome e clique em **[!UICONTROL Generate]**.

   O relatório é adicionado à lista **[!UICONTROL Recently Generated]**.

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista **[!UICONTROL Recently Generated]** da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório

1. No menu principal, clique em **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Baixar Relatório](/help/search-social-commerce/assets/download.png "Baixar Relatório") **[!UICONTROL Reports]**.

1. Na lista **[!UICONTROL Recently Generated]** da caixa de diálogo [!UICONTROL Grid Reports], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome de um relatório concluído ou de um relatório que não foi gerado.

1. Confirme a exclusão.

## Adicionar configurações de conta de rede {#account-settings-api}

As configurações da conta variam de acordo com a rede de anúncios. Talvez você não veja todas as configurações abaixo.

### Guia [!UICONTROL Authenticate]

(Visível enquanto você cria uma conta que usa autenticação pop-up) Conecte-se à rede de anúncios usando as credenciais do anunciante. A guia exibe o status da conexão e inclui **[!UICONTROL Open login again]** para reabrir o pop-up de logon.

### Guia [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** O nome a ser exibido para a conta no Search, Social e Commerce.

>[!NOTE]
>
>Se você tiver uma integração Search, Social e Commerce-Adobe Analytics e alterar o nome da conta de pesquisa, peça à sua Equipe de conta da Adobe para atualizar o mapeamento.

**[!UICONTROL Linked Ad Accounts]:** (Visível enquanto você cria uma conta que usa autenticação pop-up) A conta da rede de anúncios a ser sincronizada. Escolha entre as contas publicitárias vinculadas ao logon na rede.

**[Detalhes de Logon]:** (somente contas [!DNL Yandex]) As credenciais de conta a serem usadas:

* **[!UICONTROL Login]:** O nome ou ID de logon para habilitar o acesso à API para a conta.

* **[!UICONTROL Password]:** A senha da conta.

* **[!UICONTROL Access Key]:** A chave de acesso para a conta de desenvolvedor a ser usada.

* **[!UICONTROL Application ID]:** O token de desenvolvedor a ser usado para a conta. O mesmo token é usado para todas as contas [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) A ID numérica da campanha usada para pagar todas as campanhas de publicidade na conta.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] contas com a configuração Conta Compartilhada somente desabilitada; opcional) O token de desenvolvedor para chamadas de API relacionadas a finanças, como realocação de dinheiro entre campanhas de anunciante para otimização de portfólio.

**[!UICONTROL Currency]:** (Somente leitura) A abreviação da moeda usada na conta. Esse valor é preenchido automaticamente com a moeda configurada para a conta na rede de publicidade depois que você salva o registro.

**[!UICONTROL Time Zone]:** O fuso horário do anunciante. Esse valor é preenchido automaticamente com o fuso horário configurado para a conta Search, Social, &amp; Commerce do anunciante depois de salvar o registro.

**[!UICONTROL Login]:** (Somente leitura) A conta de usuário usada para fazer logon na conta.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** O Search, Social e Commerce sincroniza dados de campanha com a conta (quando há suporte) e envia ofertas automatizadas e/ou orçamentos de campanha para campanhas em portfólios.

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]:** (Visível enquanto você está editando uma conta que usa autenticação pop-up) Atualiza a conexão ou atualiza as permissões da conta. O novo token de acesso é salvo automaticamente quando a reautenticação é bem-sucedida.

## Guia [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Habilita ou não o rastreamento usando o serviço de rastreamento de conversão do Adobe Advertising. Esse método gera IDs exclusivas de rastreamento de cliques e redireciona os usuários para o servidor do Adobe Advertising para fins de rastreamento antes de enviá-los para a página inicial do cliente. Esse método tem opções de rastreamento padrão que você pode personalizar opcionalmente e também pode especificar parâmetros para anexar a cada URL.

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

**[!UICONTROL Auto Update]:** (Quando o rastreamento de Pesquisa, Social e Commerce está habilitado) Padroniza as URLs de rastreamento para compatibilidade entre navegadores e servidores. O Search, Social e Commerce faz o upload do seguinte automaticamente para a rede de publicidade durante a próxima sincronização: (a) Parâmetros de rastreamento de Search, Social e Commerce para modelos de rastreamento e os mesmos parâmetros anexados aos URLs finais ou (b) novos URLs de destino incorporados ao código de rastreamento do Search, Social e Commerce. Para anunciantes com uma [integração Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) e uma configuração de ID AMO do lado do servidor (s_kwcid), o carregamento também inclui [parâmetros de ID do AMO](/help/integrations/analytics/ids.md#amo-id) para suas contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising]. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante. Você pode substituir a configuração no nível da conta no nível da campanha.

Os URLs de rastreamento são atualizados diariamente apenas para entidades que estão fora de sincronia (ou seja, novas entidades que foram adicionadas e entidades existentes cujas propriedades foram alteradas). Portanto, se você alterar essa configuração de desativado para ativado para um anunciante/conta/campanha existente, os URLs de rastreamento não serão atualizados para entidades existentes que já estão em sincronia. Para adicionar rastreamento aos URLs de entidades existentes em sincronia, entre em contato com a equipe de conta da Adobe e solicite um processo de sincronização manual e único. O processo de upload automático lida com alterações futuras.

**[!UICONTROL URL Encoding]:** (Quando o rastreamento Search, Social, &amp; Commerce está habilitado; contas somente com URLs de destino) Codifica a URL base dentro da barra de endereços do navegador do usuário final (como `%3D` em vez de `=`):

**[!UICONTROL Tracking Level]:** (Quando o rastreamento Search, Social, &amp; Commerce está habilitado; disponível nos níveis de conta e campanha; não aplicável a redes de anúncios habilitadas para rastreamento paralelo) O nível no qual rastrear cliques e receita adicionando um redirecionamento e anexando parâmetros às URLs relevantes:

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

**URL de Acompanhamento de Conta**: ([!DNL Google Ads], [!DNL LY Ads] e [!DNL Microsoft Advertising] contas somente; opcional) O modelo de rastreamento padrão para a conta, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e também incorpora a URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

* Para incorporar o URL final:

  * ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente) Para obter uma lista de parâmetros para indicar URLs finais em modelos de rastreamento, consulte a [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ([!DNL Microsoft Advertising] somente) ou os parâmetros &quot;Somente modelo de rastreamento&quot; ([!DNL Google Ads] somente) na seção sobre &quot;Parâmetros [!DNL ValueTrack] disponíveis&quot; na [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL LY Ads] somente) Use o parâmetro `!{lpurl}` para indicar a URL da página de aterrissagem.

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

* Quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce prefixa automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.

>[!NOTE]
>
>* Para [!DNL Google Ads], evite usar macros, que não são substituídas por cliques de fontes que habilitam o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta da Adobe trabalhará com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.

## Guia [!UICONTROL Set up Adobe Analytics]

Estas configurações estão disponíveis para anunciantes com uma [[!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md).

**[!UICONTROL Adobe Analytics Report Suite]:** (opcional) um ou mais conjuntos de relatórios do Analytics para os quais Search, Social e Commerce enviam dados coletados da rede de publicidade, incluindo classificações de entidade e dados de cliques da conta. Este recurso está disponível somente para redes de anúncios com suporte.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

Para que os dados apareçam nos conjuntos de relatórios, (a) o recurso de ID AMO do lado do servidor deve ser configurado para a conta ou (b) a configuração no nível do anunciante como &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve ser habilitada. Além disso, a conta [!DNL Analytics] do anunciante deve ser configurada para receber dados do Search, Social e Commerce. Para obter mais informações, entre em contato com a equipe de conta da Adobe.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** ([!DNL Meta Ads] contas; opcional) Anexa o [parâmetro de rastreamento da AMO ID (s_kwcid)](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) a todos os anúncios da campanha. O parâmetro permite que o Adobe Analytics associe conversões com campanhas do Meta Ads no conjunto de relatórios especificado, juntamente com as classificações de entidade e os dados de cliques.

>[!MORELIKETHIS]
>
>* [Sobre contas de rede de anúncios](../ad-network-account-about.md)
>* [Gerenciar contas do centro de comércio](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Atualize o código de rastreamento s_kwcid de uma  [!DNL Google Ads] conta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
