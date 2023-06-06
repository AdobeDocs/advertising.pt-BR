---
title: Reautenticar um [!DNL Google Analytics] fonte de dados
description: Saiba como reautenticar um [!DNL Google Analytics] se você alterar a senha associada ou se o certificado expirar.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Reautenticar um [!DNL Google Analytics] fonte de dados

*Somente administradores de agências, gerentes de conta de agências, gerentes de conta do Adobe e administradores*

Se você alterar a senha da conta de email usada para uma fonte de dados ou se a variável [!DNL OAuth] o certificado da conta expira, todas as conexões abertas com a conta de email são fechadas e você deve reautenticar para retomar a sincronização de dados.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Marque a caixa de seleção ao lado da fonte de dados que você deseja autenticar novamente.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite o [configurações da fonte de dados](data-source-settings.md):

   1. No [!UICONTROL Connect to Google Analytics] faça o seguinte.

      1. (Se necessário) Digite um novo endereço de e-mail a ser usado para acessar os dados desta fonte de dados. O endereço de e-mail deve ser registrado em um [!DNL Google] conta e têm permissões de &quot;Ler e analisar&quot; para a [!DNL Google Analytics] conta. Consulte a [instruções para atribuição de permissões de usuário no [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para garantir que apenas [!DNL Google Analytics] as propriedades e as exibições estão disponíveis no Search, Social e Commerce, faça logon usando um endereço de email que tenha acesso somente a essas propriedades e exibições.
   1. Marque a caixa de seleção para autorizar o Search, Social e Commerce a acessar métricas da conta.

   1. Clique em **[!UICONTROL Re-Authenticate]**.


1. Clique em **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Sobre sincronização [!DNL Google Analytics] métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar um [!DNL Google Analytics] exibir como fonte de dados](data-source-configure.md)
>* [Editar um [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)

