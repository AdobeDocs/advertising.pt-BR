---
title: Reautenticar uma fonte de dados [!DNL Google Analytics]
description: Saiba como reautenticar uma fonte de dados do [!DNL Google Analytics] se você alterar a senha associada ou se o certificado expirar.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
TQID: 'https://experienceleague.adobe.com/1xjaqEk70Yr2rAcR95CteZ46OTG--xSao09B3CdCvCo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: ''
  - id: 1003789d-7feb-5a2f-a02d-3182fd0ceb8a
    internal-label: Search Admin
  - id: 9bd4e165-792f-5324-bcaa-eee38dc8b8e9
    internal-label: Search Data Sources
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Data sources
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%
---
# Reautenticar uma fonte de dados [!DNL Google Analytics]

*Somente administradores de agências, gerentes de contas de agências, gerentes de contas da Adobe e administradores*

Se você alterar a senha da conta de email usada para uma fonte de dados ou se o certificado [!DNL OAuth] da conta expirar, todas as conexões abertas com a conta de email serão fechadas e você deverá reautenticar para retomar a sincronização de dados.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Marque a caixa de seleção ao lado da fonte de dados que você deseja autenticar novamente.

1. Na barra de ferramentas acima da tabela, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite as [configurações da fonte de dados](data-source-settings.md):

   1. Na seção [!UICONTROL Connect to Google Analytics], faça o seguinte.

      1. (Se necessário) Digite um novo endereço de e-mail a ser usado para acessar os dados desta fonte de dados. O endereço de email deve ser registrado em uma conta [!DNL Google] e ter permissões de &quot;Leitura e Análise&quot; para a conta [!DNL Google Analytics]. Consulte as [instruções para atribuir permissões de usuário em [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para garantir que somente propriedades e exibições específicas do [!DNL Google Analytics] estejam disponíveis no Search, Social e Commerce, entre usando um endereço de email que tenha acesso somente a essas propriedades e exibições.

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
