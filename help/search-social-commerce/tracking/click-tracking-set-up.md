---
title: Configurar o rastreamento de cliques com base em cookies
description: Saiba como configurar e validar tags de rastreamento de cliques.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Configurar o rastreamento de cliques com base em cookies

Para que o Search, Social e Commerce rastreie cliques, os seguintes elementos devem ser configurados e validados.

1. (Equipe de conta do Adobe) Configure o anunciante como um cliente pixel.

1. [Especifique as opções de rastreamento corretas para cada uma das contas e campanhas da rede de anúncios do anunciante](#set-up-click-tracking-options).

1. Se necessário, [gerar URLs de rastreamento e carregá-los](#generate-upload-tracking-urls) para alguns elementos da campanha.

1. [Valide o formato de alguns dos URLs de rastreamento de cliques e teste-os para validar se a página de aterrissagem correta é aberta](#validate-tracking-urls).

## Configurar opções de rastreamento para campanhas e contas de rede de anúncios {#set-up-click-tracking-options}

*Gerente de conta da agência, [!DNL Adobe] funções de gerente de conta e administrador de usuário somente*

1. Para cada conta de rede de publicidade, faça o seguinte:

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Mantenha o cursor sobre o nome da conta e clique em ![Ícone do menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Ícone do menu")e selecione **[!UICONTROL Edit]**.

   1. Clique em **[!UICONTROL Set Account Tracking]**.

   1. Para o [!UICONTROL Tracking Type] , selecione **[!UICONTROL EF Redirect]**.

   1. (Para permitir que o Search, Social e Commerce troquem dados com o Adobe Analytics ou rastreiem conversões que ocorrem no [!DNL Apple Safari]) Selecione o [!UICONTROL Redirect Type] opção **[!UICONTROL Token]**.

   1. (Opcional) Ative o botão **[!UICONTROL Auto Upload]** opção para carregar automaticamente novos URLs de rastreamento na rede de publicidade na próxima vez que o Search, Social e Commerce sincronizar com ele. Esse valor é herdado como o padrão para todas as campanhas na conta, mas pode ser substituído no nível da campanha.

1. Para cada campanha, faça o seguinte:

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Mantenha o cursor sobre o nome da campanha, clique em ![Ícone do menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Ícone do menu")e selecione **[!UICONTROL Edit]**.

   1. Clique em **[!UICONTROL Set Campaign Tracking]**. Em seguida, selecione a opção para **[!UICONTROL Override Account Tracking]**.

   1. Para o [!UICONTROL Tracking Type] , selecione **[!UICONTROL EF Redirect]**.

   1. (Para permitir que o Search, Social e Commerce troquem dados com o Adobe Analytics ou rastreiem conversões que ocorrem no [!DNL Apple Safari]) Selecione o [!UICONTROL Redirect Type] opção **[!UICONTROL Token]**.

   1. (Opcional) Ative o botão **[!UICONTROL Auto Upload]** opção para carregar automaticamente novos URLs de rastreamento na rede de publicidade na próxima vez que o Search, Social e Commerce sincronizar com ele. Esse valor é herdado como o padrão para todas as campanhas na conta, mas pode ser substituído no nível da campanha.

## Gerar e carregar URLs de rastreamento {#generate-upload-tracking-urls}

Consulte &quot;[Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### Testar o formato de URLs de rastreamento de cliques {#validate-tracking-urls}

Valide se a landing page correta é aberta para o URL de rastreamento de cliques.

1. Imite um clique de anúncio enviando tráfego para o ambiente de preparo do anunciante:

   1. Em um editor de texto, cole um URL de rastreamento de cliques, altere o URL da página de destino para apontar para a mesma página no ambiente de preparo do anunciante e, em seguida, cole o novo URL na barra de endereços do navegador e pressione a tecla **[!DNL Enter]** chave.

   1. Procure o cookie nos cookies armazenados do seu navegador.

   1. Conclua uma transação no site de preparo e verifique se a página de sucesso aciona o pixel correto. Os parâmetros reais rastreados pelo pixel variam de acordo com o anunciante e o URL de rastreamento. No exemplo a seguir, o anunciante deseja rastrear o número de novos aplicativos e a quantidade de nova receita:

      Para um novo usuário final (com um cookie novo), o seguinte pixel deve ser acionado:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Se o cookie não estiver atualizado, o seguinte pixel deverá ser acionado:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Repita o procedimento para vários URLs de rastreamento de cliques no domínio.

1. Repita a Etapa 1 para cada domínio, usando uma landing page diferente.

1. Se necessário, confirme se o Search, o Social e o Commerce podem ver os pixels das IDs de transações (`ev_transid`) gerado durante o teste.

>[!MORELIKETHIS]
>
>* [Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)

