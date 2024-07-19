---
title: Reautenticar uma fonte de dados  [!DNL Google Analytics]
description: Saiba como autenticar novamente uma fonte de dados  [!DNL Google Analytics]  se você alterar a senha associada ou se o certificado expirar.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Reautenticar uma fonte de dados [!DNL Google Analytics]

*Somente Administradores de Agência, Gerentes de Conta de Agência, Gerentes de Conta de Adobe e Administradores*

Se você alterar a senha da conta de email usada para uma fonte de dados ou se o certificado [!DNL OAuth] da conta expirar, todas as conexões abertas com a conta de email serão fechadas e você deverá reautenticar para retomar a sincronização de dados.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Marque a caixa de seleção ao lado da fonte de dados que você deseja autenticar novamente.

1. Na barra de ferramentas acima da tabela, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite as [configurações da fonte de dados](data-source-settings.md):

   1. Na seção [!UICONTROL Connect to Google Analytics], faça o seguinte.

      1. (Se necessário) Digite um novo endereço de e-mail a ser usado para acessar os dados desta fonte de dados. O endereço de email deve ser registrado em uma conta [!DNL Google] e ter permissões de &quot;Leitura e Análise&quot; para a conta [!DNL Google Analytics]. Consulte as [instruções para atribuir permissões de usuário em [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para garantir que apenas propriedades e exibições específicas do [!DNL Google Analytics] estejam disponíveis no Search, Social e Commerce, faça logon usando um endereço de email que tenha acesso somente a essas propriedades e exibições.

   1. Marque a caixa de seleção para autorizar o Search, Social e Commerce a acessar as métricas da conta.

   1. Clique em **[!UICONTROL Re-Authenticate]**.

1. Clique em **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Sobre a sincronização [!DNL Google Analytics] de métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar uma [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Configurar uma  [!DNL Google Analytics] exibição como fonte de dados](data-source-configure.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
