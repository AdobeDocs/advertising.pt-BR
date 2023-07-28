---
title: Criar um [!DNL Google Ads] público-alvo de correspondência do cliente de uma lista de email da Adobe Campaign
description: Saiba como criar um [!DNL Google Ads] o público-alvo de correspondência do cliente de uma lista de email existente do Adobe Campaign.
exl-id: 967580fc-52c3-42f5-8d60-18cb83bc714a
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Criar um [!DNL Google Ads] público-alvo de correspondência do cliente de uma lista de email da Adobe Campaign

*[!DNL Google Ads]contas elegíveis somente para correspondência de cliente*

Você pode criar um [!DNL Google Ads] o público-alvo de correspondência do cliente de uma lista de email no Adobe Campaign configurando um link de conta e um fluxo de trabalho no [!DNL Campaign].

Para isso, você precisa ter acesso aos seus [!DNL Campaign] e um arquivo XML que contém o fluxo de trabalho necessário, que será fornecido pela equipe de conta do Adobe. As instruções podem variar para diferentes versões do [!DNL Campaign]. Se necessário, a equipe da conta do Adobe poderá ajudá-lo a configurar o fluxo de trabalho no [!DNL Campaign].

1. Obtenha credenciais para uma conta SFTP fornecida pelo Advertising Search, Social e Commerce.

1. Entrada [!DNL Campaign], configurar a entrega da lista de email para Advertising Search, Social e Commerce:

   1. Criar um [conta externa](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) para vincular sua conta SFTP fornecida pelo Search, Social e Commerce:

      1. No menu esquerdo, vá para **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Clique em ![Criar conta](/help/search-social-commerce/assets/campaign-create-account.png "Criar conta").

      1. Insira um rótulo para a conta e selecione **[!UICONTROL SFTP]** como o tipo de conta.

      1. Insira o URL e o número da porta para o [!DNL Adobe] Servidor SFTP e o nome da pasta, nome de usuário e senha do anunciante.

      1. Clique em **[!UICONTROL Save]**.

   1. Entrada [!DNL Campaign Client], instale o pacote de dados que inclui o fluxo de trabalho necessário para enviar dados de email:

      1. Na barra de menus, vá para **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Selecionar **[!UICONTROL Install a package from a file]** e clique em **[!UICONTROL Next]**.

      1. Localize o arquivo do pacote de dados (`AMO_Workflow.xml`) no dispositivo ou na rede e clique em **[!UICONTROL Next]**.

      1. Clique em **[!UICONTROL Start]** e aguarde a instalação do workflow.

   1. Edite o fluxo de trabalho instalado para editar opcionalmente os filtros da consulta de dados e para identificar o novo nome do público-alvo e a conta SFTP externa:

      1. Ir para **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** e abra o pacote.

      1. (Opcional) Edite qualquer um dos filtros para os dados:

         * No workflow, dê um duplo clique na atividade de query (como ForkTransition 1).

         * Edite as expressões de filtro.

         * Clique em **[!UICONTROL Finish]**.

      1. Nomeie o segmento:

         * No workflow, dê um duplo clique na atividade **[!UICONTROL Data extraction (File)]**.

         * Em para o **[!UICONTROL Data extraction (File)]** , na guia **[!UICONTROL File name]** insira o nome do segmento com a extensão &quot;`.added`&quot; (como PaidSubscribers.aded).

           O nome do segmento ainda não deve existir. O nome do segmento diferencia maiúsculas de minúsculas, deve consistir em caracteres ASCII, mas não pode incluir sublinhados (`_`).

           No entanto, se você quiser adicionar o segmento a um [!DNL Google Ad] conta e, em seguida, anexe o nome do segmento com um sublinhado e a [!UICONTROL User SE Account ID] (ID de pesquisa, social e comércio para o [!DNL Google Ads] conta, não a ID da conta da rede):

           `_<User SE Account ID>`

           Exemplo: Paid_Subscribers_1234.Added

           >[!NOTE]
           >
           >Essa é uma exceção à regra que proíbe sublinhados no nome do arquivo.

           Caso contrário, o segmento será adicionado a todos [!DNL Google Ads] contas que o Search, Social e Commerce está sincronizando para o anunciante.

         * Deixe a opção para **[!UICONTROL Generate an outbound transition]** selecionado.

         * Clique em **[!UICONTROL Ok]**.

      1. Especifique a conta externa para a qual enviar os dados:

         * No workflow, dê um duplo clique na atividade **[!UICONTROL File Transfer]**.

         * Em para o **[!UICONTROL File Transfer]** , na guia **[!UICONTROL Remote server]** selecione a opção para **[!UICONTROL Use an external account]**.

         * No **[!UICONTROL External account]** selecione o rótulo da conta externa que você criou na Etapa 2.

         * No **[!UICONTROL Server folder]** selecione o valor para a variável [!UICONTROL Account] para a conta externa.

         * (Opcional) No **[!UICONTROL Schedule]** especifique um agendamento diferente para a transferência de arquivos.

           Por padrão, o workflow é executado às 00:00 (meia-noite), o que garante que todos os registros sejam processados. Para minimizar a latência, agende o workflow para ser executado até as 18:00.

         * Clique em **[!UICONTROL Ok]**.

Search, Social, &amp; Commerce verifica o diretório a cada 30 minutos (às NN:30 e NN:59 no fuso horário do anunciante) e move todos os arquivos encontrados para outro local, em seguida, cria automaticamente um público-alvo dos dados e o envia para o Google às 22:00 (22:00). O Search, Social, &amp; Commerce continua a verificar se há atualizações (adições e subtrações) na lista de email a cada 30 minutos e atualiza o público no [!DNL Google Ads] 22:00 por dia.

>[!NOTE]
>
>* Se você fizer upload de mais de uma versão de um arquivo entre ciclos de processamento, o arquivo mais recente será usado.
>
>* O Search, Social e Commerce não armazena os dados do cliente de suas listas de email usadas para criar ou editar um [!DNL Google Ads] público-alvo.
>
>* [!DNL Google Ads] O pode levar algum tempo para processar atualizações para um público-alvo.
>
>* Consulte [[!DNL Google Ads] documentação sobre como a correspondência do cliente funciona e limitações](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Sobre públicos](audience-about.md)
>* [Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos](google-audience-from-adobe-audience.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)
