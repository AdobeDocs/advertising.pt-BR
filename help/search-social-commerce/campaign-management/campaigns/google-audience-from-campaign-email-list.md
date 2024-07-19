---
title: Criar um público-alvo de correspondência do cliente  [!DNL Google Ads]  a partir de uma lista de email do Adobe Campaign
description: Saiba como criar um público-alvo de correspondência do cliente  [!DNL Google Ads]  de uma lista de email existente do Adobe Campaign.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Criar um público-alvo de correspondência do cliente [!DNL Google Ads] a partir de uma lista de email do Adobe Campaign

*[!DNL Google Ads]contas qualificadas somente para correspondência de cliente*

Você pode criar um público-alvo de correspondência do cliente [!DNL Google Ads] a partir de uma lista de email no Adobe Campaign configurando um link de conta e um fluxo de trabalho no [!DNL Campaign].

Para fazer isso, você precisa acessar sua instância [!DNL Campaign] e um arquivo XML que contém o fluxo de trabalho necessário, que a equipe de conta do Adobe fornecerá. As instruções podem variar para diferentes versões do [!DNL Campaign]. Se necessário, sua equipe de conta do Adobe pode ajudá-lo a configurar o fluxo de trabalho no [!DNL Campaign].

1. Obtenha credenciais para uma conta SFTP fornecida pela Advertising Search, Social e Commerce.

1. Em [!DNL Campaign], configure a entrega da lista de email para o Advertising Search, Social e Commerce:

   1. Crie uma [conta externa](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) para vincular à sua conta SFTP fornecida pela Search, Social e Commerce:

      1. No menu esquerdo, vá para **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Clique em ![Criar Conta](/help/search-social-commerce/assets/campaign-create-account.png "Criar Conta").

      1. Insira um rótulo para a conta e selecione **[!UICONTROL SFTP]** como o tipo de conta.

      1. Insira a URL e o número da porta do servidor SFTP [!DNL Adobe] e o nome, o nome de usuário e a senha da pasta do anunciante.

      1. Clique em **[!UICONTROL Save]**.

   1. Em [!DNL Campaign Client], instale o pacote de dados que inclui o fluxo de trabalho necessário para enviar dados de email:

      1. Na barra de menus, vá para **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Selecione **[!UICONTROL Install a package from a file]** e clique em **[!UICONTROL Next]**.

      1. Localize o arquivo de pacote de dados (`AMO_Workflow.xml`) no dispositivo ou na rede e clique em **[!UICONTROL Next]**.

      1. Clique em **[!UICONTROL Start]** e aguarde a instalação do fluxo de trabalho.

   1. Edite o fluxo de trabalho instalado para editar opcionalmente os filtros da consulta de dados e para identificar o novo nome do público-alvo e a conta SFTP externa:

      1. Vá para **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** e abra o pacote.

      1. (Opcional) Edite qualquer um dos filtros para os dados:

         * No workflow, dê um duplo clique na atividade de query (como ForkTransition 1).

         * Edite as expressões de filtro.

         * Clique em **[!UICONTROL Finish]**.

      1. Nomeie o segmento:

         * No fluxo de trabalho, clique duas vezes na atividade **[!UICONTROL Data extraction (File)]**.

         * Na guia **[!UICONTROL Data extraction (File)]**, no campo **[!UICONTROL File name]**, digite o nome do segmento com a extensão &quot;`.added`&quot; (como PaidSubscribers.aded).

           O nome do segmento ainda não deve existir. O nome do segmento diferencia maiúsculas de minúsculas, deve consistir em caracteres ASCII, mas não pode incluir sublinhados (`_`).

           No entanto, se você quiser adicionar o segmento a uma conta específica do [!DNL Google Ad], anexe o nome do segmento com um sublinhado e a [!UICONTROL User SE Account ID] (Pesquisa, Social e ID da Commerce para a conta do [!DNL Google Ads], não a ID da conta da rede):

           `_<User SE Account ID>`

           Exemplo: Paid_Subscribers_1234.Added

           >[!NOTE]
           >
           >Essa é uma exceção à regra que proíbe sublinhados no nome do arquivo.

           Caso contrário, o segmento será adicionado a todas as contas do [!DNL Google Ads] que o Search, Social e Commerce está sincronizando para o anunciante.

         * Deixe a opção para **[!UICONTROL Generate an outbound transition]** selecionada.

         * Clique em **[!UICONTROL Ok]**.

      1. Especifique a conta externa para a qual enviar os dados:

         * No fluxo de trabalho, clique duas vezes na atividade **[!UICONTROL File Transfer]**.

         * Na guia **[!UICONTROL File Transfer]**, na seção **[!UICONTROL Remote server]**, selecione a opção para **[!UICONTROL Use an external account]**.

         * No campo **[!UICONTROL External account]**, selecione o rótulo para a conta externa que você criou na Etapa 2.

         * No campo **[!UICONTROL Server folder]**, selecione o valor do campo [!UICONTROL Account] para a conta externa.

         * (Opcional) Na guia **[!UICONTROL Schedule]**, especifique um agendamento diferente para a transferência de arquivos.

           Por padrão, o workflow é executado às 00:00 (meia-noite), o que garante que todos os registros sejam processados. Para minimizar a latência, agende o workflow para ser executado até as 18:00.

         * Clique em **[!UICONTROL Ok]**.

Search, Social, &amp; Commerce verifica o diretório a cada 30 minutos (às NN:30 e NN:59 no fuso horário do anunciante) e move todos os arquivos encontrados para outro local, em seguida, cria automaticamente um público-alvo dos dados e o envia para o Google às 22:00 (22:00). O Search, Social e Commerce continua a verificar atualizações (adições e subtrações) na lista de email a cada 30 minutos e atualiza o público-alvo no [!DNL Google Ads] de acordo às 22h diariamente.

>[!NOTE]
>
>* Se você fizer upload de mais de uma versão de um arquivo entre ciclos de processamento, o arquivo mais recente será usado.
>
>* O Search, Social e Commerce não armazena os dados do cliente de suas listas de email usadas para criar ou editar um público-alvo do [!DNL Google Ads].
>
>* [!DNL Google Ads] pode demorar um pouco para processar atualizações para um público-alvo.
>
>* Consulte [[!DNL Google Ads] documentação sobre como a correspondência entre clientes funciona e limitações](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](audience-about.md)
>* [Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](google-audience-from-adobe-audience.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)
