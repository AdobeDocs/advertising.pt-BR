---
title: Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente
description: Saiba como criar e editar [!DNL Google Ads] e [!DNL Microsoft Advertising] públicos-alvo de correspondência do cliente de suas listas de dados do cliente.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Gerenciar públicos-alvo de correspondência do cliente [!DNL Google Ads] e [!DNL Microsoft Advertising] usando listas de dados do cliente

Você pode criar [!DNL Google Ads] e [!DNL Microsoft Advertising] públicos-alvo de correspondência do cliente a partir de suas listas de dados do cliente. Você também pode atualizar qualquer público-alvo de correspondência do cliente [!DNL Google Ads] ou [!DNL Microsoft Advertising], exceto para [!DNL Google Ads] públicos-alvo criados de um público-alvo [!DNL Adobe].

## Criar um público-alvo de correspondência do cliente a partir de uma lista de dados do cliente

Contas de *[!DNL Google Ads]e [!DNL Microsoft Advertising] qualificadas somente para correspondência de cliente*

Você pode criar uma lista baseada em dados de cliente do [!DNL Google Ads] ou do [!DNL Microsoft Advertising] a partir de um arquivo de dados gerado pelo seu sistema de CRM (relacionamento com o cliente).

Para contas do [!DNL Microsoft Advertising], o arquivo pode incluir endereços de email. Para contas do [!DNL Google Ads], o arquivo pode incluir endereços de email, endereços para correspondência ou números de telefone, IDs de usuário ou IDs de dispositivo móvel do seu CRM.

>[!NOTE]
>
>O Search, Social e Commerce não armazena dados de clientes que você carrega ou que sejam dos [!DNL Adobe] segmentos usados para criar ou editar um público-alvo do [!DNL Google Ads] ou do [!DNL Microsoft Advertising].

1. Gere um arquivo com os dados do cliente no formato necessário.

   O nome e o sobrenome, os endereços de email e os números de telefone devem ser atribuídos a hash usando o algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para [!DNL Google Ads] públicos-alvo, consulte a documentação de [!DNL Google Ads] em &quot;[Diretrizes de formatação para carregar dados com hash](https://support.google.com/google-ads/answer/7476159)&quot; para obter uma lista de campos e requisitos de informações de contato permitidos. Para públicos-alvo de [!DNL Microsoft Advertising], consulte a documentação de [!DNL Microsoft Advertising] em [preparando listas de correspondência de clientes](https://help.ads.microsoft.com/#apex/ads/en/56921. Opcionalmente, você pode baixar um modelo [!DNL Microsoft Excel] para obter informações de contato.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Especifique as informações do público:

   1. No menu [!UICONTROL Data Source], selecione **[!UICONTROL Customer List]**.

   1. Insira o **[!UICONTROL Audience Name]**.

   1. Faça upload do arquivo:

      1. Selecione o [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, ou *[!UICONTROL Mobile Device IDs]*.

         A opção IDs de usuário está disponível somente para [!DNL Google Ads] anunciantes nos EUA que optaram por [segmentos de ID de usuário](https://support.google.com/google-ads/answer/9199250)

      1. (Somente listas de ID de dispositivo móvel) Selecione o **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* ou *[!UICONTROL iOS]*) e insira o **[!UICONTROL App ID]**.

         A ID do aplicativo é um identificador exclusivo que o sistema operacional móvel usa para permitir que o aplicativo se conecte à Google Play ou à Apple App Store:

         * ([!DNL Android™] aplicativos) O nome do pacote [!DNL Android™] em [!DNL Google Play], identificado por &quot;`id=<package_name>`.&quot;

           Por exemplo, em https://play.google.com/store/apps/details?id=com.example.game, o nome do pacote é com.example.game.

         * ([!DNL iOS] aplicativos) A ID do aplicativo em [!DNL iTunes App Store], identificada por &quot;`<idNNNNNNNNN>`&quot; no final da URL. Ele também está disponível no [!DNL iOS Developer Console].

           Por exemplo, em https://itunes.apple.com/us/app/id284882215, a ID é id284882215.

         Sua equipe de desenvolvimento tem acesso ao [!UICONTROL App ID] para a plataforma relevante.

      1. No campo [!UICONTROL Select File], clique em **[!UICONTROL Choose File]** e selecione o arquivo na rede ou no dispositivo.

      1. Marque a caixa de seleção para indicar que você concorda com os termos do [!DNL Adobe] e com as políticas de privacidade de rede de anúncios.

      1. (Anunciantes criando [!DNL Google Ads] públicos-alvo que fazem negócios no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido); opcional) Se você coletou o consentimento de usuários do EEE e Reino Unido para carregar seus dados para fins de publicidade, marque a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignora quaisquer dados para usuários da EEA e UK com um status de consentimento não especificado. Isso pode levar a discrepância de dados e problemas de desempenho.

      1. Clique em **[!UICONTROL Upload File]**.

   1. Especifique o número de **[!UICONTROL Membership Days]**, que é o número de dias que um cookie do usuário permanece no público-alvo.

   Use o período de tempo durante o qual você espera que seu anúncio seja relevante para o usuário. As listas de clientes não expiram, a menos que você insira um valor.

1. Clique em **[!UICONTROL Post]**.

>[!NOTE]
>
>* A rede de publicidade pode levar até 24 horas para processar o arquivo.
>* Consulte [[!DNL Google Ads] documentação sobre como a correspondência entre clientes funciona e limitações](https://support.google.com/displayvideo/answer/9539301).

## Editar um público-alvo de correspondência do cliente usando uma lista de dados do cliente

Você pode atualizar qualquer público-alvo de correspondência do cliente [!DNL Google Ads] ou [!DNL Microsoft Advertising], exceto para [!DNL Google Ads] públicos-alvo criados de um público-alvo [!DNL Adobe]. É possível carregar dados para adicionar, excluir ou substituir todos os dados existentes do público-alvo.

Os dados devem ser do mesmo tipo da lista original de clientes (endereços de email, endereços de correspondência, números de telefone, IDs de usuário ou IDs de dispositivo móvel para um aplicativo específico em um sistema operacional móvel específico).

1. Gere um arquivo com os dados do cliente no formato necessário para o tipo de dados existente.

O nome e o sobrenome, os endereços de email e os números de telefone devem ser atribuídos a hash usando o algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para [!DNL Google Ads] públicos-alvo, consulte a documentação de [!DNL Google Ads] em &quot;[Diretrizes de formatação para carregar dados com hash](https://support.google.com/google-ads/answer/7476159)&quot; para obter uma lista de campos e requisitos de informações de contato permitidos. Para públicos-alvo de [!DNL Microsoft Advertising], consulte a documentação de [!DNL Microsoft Advertising] em [preparando listas de correspondência de clientes](https://help.ads.microsoft.com/#apex/ads/en/56921. Opcionalmente, você pode baixar um modelo [!DNL Microsoft Excel] para obter informações de contato.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Marque a caixa de seleção ao lado do público-alvo para editar.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png).

1. Selecione a ação: *[!UICONTROL Add]* (para adicionar os dados carregados aos dados existentes, a menos que já existam), *[!UICONTROL Delete]* (para excluir os dados carregados dos dados existentes, quando eles já existirem) ou *[!UICONTROL Replace]* (para excluir todos os dados existentes e substituí-los pelos dados carregados).

1. Faça upload do arquivo:

   1. No campo [!UICONTROL Select File], clique em **[!UICONTROL Choose File]** e selecione o arquivo na rede ou no dispositivo.

   1. Marque a caixa de seleção para indicar que você concorda com os termos do [!DNL Adobe] e com as políticas de privacidade de rede de anúncios.

   1. Clique em **[!UICONTROL Upload File]**.

1. Clique em **[!UICONTROL Post]**.

>[!NOTE]
>
>A rede de anúncios pode levar algum tempo para processar atualizações para um público-alvo.

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](audience-about.md)
>* [Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](google-audience-from-adobe-audience.md)
>* [Criar um [!DNL Google Ads] público-alvo de correspondência do cliente a partir de uma lista de emails do Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)
