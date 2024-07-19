---
title: Validar páginas de aterrissagem em arquivos de bulksheet
description: Saiba como validar os URLs de destino em um arquivo de bulksheet de uma única conta.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validar páginas de aterrissagem em arquivos de bulksheet

*Contas somente com URLs de destino*

Você pode validar as landing pages em todos os URLs de destino em um arquivo de bulksheet de conta única. Você pode especificar quaisquer frases e URLs que indiquem uma página inválida e, opcionalmente, reportar redirecionamentos de página de aterrissagem como erros. O Search, Social e Commerce verifica as condições especificadas e as páginas de aterrissagem ausentes (que resultam em erros HTTP 404 ou &quot;Não encontrado&quot;).

Ao encontrar erros, o Search, Social e Commerce cria um arquivo de erro de bulksheet que inclui todas as linhas na bulksheet original e mensagens de erro para todas as linhas com uma página de aterrissagem inválida. Os erros são anotados na coluna [!UICONTROL EF Errors]. A convenção de nome de arquivo é `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Posteriormente, você pode baixar o arquivo, corrigir os erros, fazer upload do arquivo corrigido e publicar o arquivo corrigido na conta de rede de publicidade.

>[!NOTE]
>
>* Esse recurso não valida valores na coluna URL base/URL final.
>* Você pode publicar arquivos de bulksheet enquanto eles estiverem sendo validados ou mesmo se forem encontrados erros.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Marque a caixa de seleção ao lado de cada arquivo a ser validado.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Validate URLs]**.

1. Na caixa de diálogo, insira as informações nos campos e clique em **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Texto no corpo de uma página de aterrissagem que indica que a página é inválida. Para especificar vários valores, insira-os em linhas separadas.

   **[!UICONTROL Enter invalid landing pages(one per line):]** As URLs de páginas inválidas como páginas de aterrissagem. Para especificar vários valores, insira-os em linhas separadas.

   **[!UICONTROL User Agent:]** Como o agente de validação da página de aterrissagem é identificado ao servidor Web no qual a página de aterrissagem reside. O padrão é, que atribui exibições pelo agente a um usuário anônimo [!DNL Mozilla Firefox]. Se o servidor Web bloquear solicitações de usuários anônimos [!DNL Mozilla Firefox], digite o nome de um agente diferente. Por exemplo, para [!DNL Googlebot], digite `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Quando uma página de aterrissagem é redirecionada para outra página (por exemplo, se a página de aterrissagem estiver ausente e o site exibir uma página substituta), a coluna [!UICONTROL ER Errors] no arquivo de erro da página de aterrissagem indica a URL para a qual a página de aterrissagem é redirecionada.

Quando a tarefa for iniciada, uma nova linha será adicionada à [!UICONTROL Bulksheets view]. Quando o arquivo é criado, uma notificação por email é enviada com um link para o arquivo. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. Você pode baixar o arquivo para editá-lo e depois fazer upload dele para publicação ou postar o arquivo como está. No entanto, se a geração do arquivo falhar, um arquivo de erro será listado na página [!UICONTROL Bulksheet Management] e uma notificação será enviada por email com um link para o arquivo de erro.

>[!NOTE]
>
>* Arquivos grandes demoram mais para serem validados.
>* Os arquivos de bulksheet para várias campanhas podem conter até 500.000 linhas de dados. Se você gerar dados para várias campanhas e os dados combinados consistirem em mais de 500.000 linhas, os dados serão divididos por campanha em dois ou mais arquivos chamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` e assim por diante.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Excluir bulksheets e arquivos de erro carregados](bulksheet-delete.md)
>* [Postar bulksheets ou arquivos de erro corrigidos](bulksheet-post.md)
>* [Parar um trabalho de bulksheet em andamento](bulksheet-stop-job.md)
>* [Carregar uma bulksheet ou arquivo de erro corrigido](bulksheet-upload.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)
