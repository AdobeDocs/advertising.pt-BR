---
title: (Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet
description: Saiba como validar os URLs de destino em um arquivo de bulksheet de uma única conta na nova interface do usuário do Search, Social e Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f916f47a40729ff39ac1456e3b3ad93e1045e9a9
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# (Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet

*Contas somente com URLs de destino*

Você pode validar as landing pages em todos os URLs de destino em um arquivo de bulksheet de conta única. Você pode especificar quaisquer frases e URLs que indiquem uma página inválida e, opcionalmente, reportar redirecionamentos de página de aterrissagem como erros. O Search, Social e Commerce verifica as condições especificadas e as páginas de aterrissagem ausentes (que resultam em erros HTTP 404 ou &quot;Não encontrado&quot;).

Ao encontrar erros, o Search, Social e Commerce cria um arquivo de erro de bulksheet que inclui todas as linhas na bulksheet original e mensagens de erro para todas as linhas com páginas de aterrissagem inválidas. Os erros são anotados na coluna [!UICONTROL EF Errors]. A convenção de nome de arquivo é `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Posteriormente, você pode baixar o arquivo, corrigir os erros, fazer upload do arquivo corrigido e publicar o arquivo corrigido na conta de rede de publicidade.

>[!NOTE]
>
>* Esse recurso não valida valores na coluna URL base/URL final.
>* Você pode publicar arquivos de bulksheet enquanto eles estiverem sendo validados ou mesmo se forem encontrados erros.

>[!IMPORTANT]
>
>O suporte para caracteres não ASCII na validação da página de aterrissagem foi temporariamente suspenso. Se os URLs da sua página de aterrissagem contiverem caracteres não ASCII, entre em contato com o suporte técnico para obter assistência.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Marque a caixa de seleção ao lado de cada arquivo a ser validado.

   >[!NOTE]
   >
   >Você pode validar somente bulksheets EF de conta única que não estejam em andamento no momento. Se você selecionar um bulksheet de várias contas ou um bulksheet que está sendo processado no momento, esses arquivos serão excluídos.

1. Na barra de ações, clique em **[!UICONTROL Validate URLs]**.

1. Na caixa de diálogo, insira informações nos campos e clique em **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Texto no corpo de uma página de aterrissagem indicando que a página é inválida. Para especificar vários valores, insira-os em linhas separadas.

   **[!UICONTROL Enter invalid landing pages (one per line):]** As URLs de páginas inválidas como páginas de aterrissagem. Para especificar vários valores, insira-os em linhas separadas.

   **[!UICONTROL User Agent:]** Como o agente de validação da página de aterrissagem é identificado ao servidor Web no qual a página de aterrissagem reside. O padrão é `default`, que atribui exibições pelo agente a um usuário anônimo [!DNL Mozilla Firefox]. Se o servidor Web bloquear solicitações de usuários anônimos [!DNL Mozilla Firefox], digite o nome de um agente diferente. Por exemplo, para [!DNL Googlebot], digite `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Quando uma página de aterrissagem é redirecionada para outra página (por exemplo, se a página de aterrissagem estiver ausente e o site exibir uma página substituta), a coluna [!UICONTROL EF Errors] no arquivo de erro da página de aterrissagem indica a URL para a qual a página de aterrissagem é redirecionada.

Quando a tarefa for iniciada, uma nova linha será adicionada à exibição [!UICONTROL Bulksheets]. Quando as notificações por email de bulksheets estão [habilitadas dentro de [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), uma notificação por email com um link para o arquivo é enviada quando o arquivo é criado. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. Você pode baixar o arquivo para editá-lo e depois fazer upload dele para publicação ou postar o arquivo como está.

>[!NOTE]
>
>* Arquivos grandes demoram mais para serem validados.
>* Os arquivos de bulksheet para várias campanhas podem conter até 500.000 linhas de dados. Se você gerar dados para várias campanhas e os dados combinados consistirem em mais de 500.000 linhas, os dados serão divididos por campanha em dois ou mais arquivos chamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` e assim por diante.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Sobre o gerenciamento de dados de campanha usando bulksheets](about.md)
>* [(Nova interface do usuário) Carregar um bulksheet ou arquivo de erro corrigido](upload.md)
>* [(Nova interface do usuário) Postar bulksheets ou arquivos de erro corrigidos](post.md)
>* [(Nova interface do usuário) Excluir bulksheets e arquivos de erro carregados](delete.md)
>* [(Nova interface do usuário) Parar um trabalho de bulksheet em andamento](stop-job.md)
