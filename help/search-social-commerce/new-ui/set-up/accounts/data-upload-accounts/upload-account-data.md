---
title: Carregar dados da conta offline para relatórios e simulações
description: Saiba como carregar dados de conta offline manualmente ou em um bucket do  [!DNL Amazon] [!DNL S3] para suporte a relatórios e simulações. Os arquivos de log acompanham o progresso dos trabalhos de upload.
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Carregar dados da conta offline para relatórios e simulações

*Anunciantes habilitados para carregamentos de dados da conta*

Faça upload do conteúdo da campanha e dos dados de custo offline, cliques e conversão de uma conta sem suporte de API para relatórios e simulações de desempenho.

Você pode acompanhar o progresso de seus trabalhos de carregamento usando o recurso [!UICONTROL Upload Logs]:

* Exiba uma lista de cada arquivo carregado para a conta. As informações sobre cada trabalho de carregamento de arquivo incluem o nome do arquivo, o canal de carregamento (*[!UICONTROL Cloud Storage]* ou *[!UICONTROL Drag & Drop]*), a data e o status da sincronização e os motivos para carregamentos incompletos.

* Baixe um arquivo com as entidades da conta e as métricas relacionadas que foram carregadas para qualquer trabalho. Os arquivos estão no formato CSV (valores separados por vírgula).

## Carregar dados da conta manualmente

É possível preencher uma conta com dados de conteúdo e custo da campanha, clique e conversão fazendo upload manual dos dados em um arquivo.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Da exibição [!UICONTROL Accounts]):

      1. Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Upload]** na barra de ferramentas de ações em massa.

      1. Arraste um arquivo para a caixa ou clique em **[!UICONTROL Browse Files]** e escolha um arquivo do seu dispositivo ou rede.

      1. Clique em **[!UICONTROL Upload Files]**.

   * (Nas configurações da conta):

      1. Selecione a conta de uma das seguintes maneiras:

         * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

         * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

      1. Clique na guia **[!UICONTROL Upload File]**.

      1. Arraste um arquivo para a caixa ou clique em **[!UICONTROL Browse Files]** e escolha um arquivo do seu dispositivo ou rede.

      1. Clique em **[!UICONTROL Save]**.

&#x200B;# Carregar dados da conta para um bucket [!DNL Amazon] [!DNL S3] {#data-upload-s3}

É possível preencher uma conta com dados de conteúdo e custo da campanha, cliques e conversão carregando os dados em uma pasta atribuída pela Search, Social e Commerce em um bucket do [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Entre em contato com a equipe de conta da Adobe para ativar os uploads de dados da conta para sua conta de anunciante do Search, Social e Commerce. A equipe facilitará a criação de uma pasta específica da organização em um bucket do [!DNL S3], e avisará quando ele for concluído.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Recupere o caminho de armazenamento na nuvem [!DNL S3], a ID da chave de acesso e a chave de acesso secreta para sua conta. A mesma ID de chave de acesso e chave de acesso secreta são usadas para todas as contas de upload de dados da organização do <!-- naming convention?-->.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Siga um destes procedimentos:

   * (Da exibição [!UICONTROL Accounts]):

      1. Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Upload]** na barra de ferramentas de ações em massa.

      1. Na caixa [!UICONTROL Cloud Storage Link], clique em **[!UICONTROL Go to the Link]**.

      1. Clique em **[!UICONTROL Show Access Key and Secret]**.

      1. Ao lado do campo [!UICONTROL Storage Link], clique em **[!UICONTROL Copy]** para copiar o link para a área de transferência e armazená-lo em um local seguro.

      1. Da mesma forma, copie e armazene com segurança os valores [!UICONTROL Access Key] e [!UICONTROL Secret Key].

      1. Clique em **[!UICONTROL Done]**.

   * (Nas configurações da conta):

      1. Selecione a conta de uma das seguintes maneiras:

         * Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Edit]**.

         * Marque a caixa de seleção ao lado do nome da conta e clique em **[!UICONTROL Edit]** na barra de ferramentas de ações em massa.

      1. Clique na guia **[!UICONTROL Upload File]**.

      1. Na caixa [!UICONTROL Cloud Storage Link], clique em **[!UICONTROL Go to the Link]**.

      1. Clique em **[!UICONTROL Show Access Key and Secret]**.

      1. Ao lado do campo [!UICONTROL Storage Link], clique em **[!UICONTROL Copy]** para copiar o link para a área de transferência e armazená-lo em um local seguro.

      1. Da mesma forma, copie e armazene com segurança os valores [!UICONTROL Access Key] e [!UICONTROL Secret Key].

      1. Clique em **[!UICONTROL Done]**.

      1. Clique em **[!UICONTROL Save]**.

1. (Uma vez por organização) Configurar o ambiente local do AWS:

   1. Baixe e instale o [!DNL AWS Command Line Interface] (AWS CLI) do seguinte local: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configurar suas credenciais do AWS:

      1. Crie um arquivo de texto sem formatação e nomeie-o como `~/.aws/credentials` (sem uma extensão de arquivo).

      1. Abra o arquivo em qualquer editor de texto e insira a ID da chave de acesso e a chave de acesso secreta da organização da seguinte maneira:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Baixe o relatório de dados da conta na rede de publicidade e salve-o.

1. Na CLI do AWS, execute o comando a seguir para carregar os dados da conta no local da nuvem do [!DNL S3].

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Exemplo: `aws s3 cp filename.txt s3://cloud-location/`

## Exibir um log de arquivos de dados de conta carregados

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Mantenha o cursor sobre o nome da conta, clique em **...** e em **[!UICONTROL Upload Logs]**.

1. (Opcional) Para baixar os dados de um arquivo carregado, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") na coluna [!UICONTROL Download] e baixe o arquivo de acordo com o procedimento normal do seu navegador.

## Dados exigidos

Os dados devem seguir os requisitos de dados da rede de anúncios. Os campos de dados de cada entidade podem variar de acordo com a rede de anúncios.
