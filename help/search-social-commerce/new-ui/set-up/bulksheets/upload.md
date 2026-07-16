---
title: (Nova interface do usuário) Fazer upload de uma bulksheet ou arquivo de erro corrigido
description: Saiba como fazer upload manual de um arquivo de bulksheet ou arquivo de erro de validação de página de aterrissagem corrigido na nova interface do Search, Social e Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# (Nova interface do usuário) Fazer upload de uma bulksheet ou arquivo de erro corrigido

Você pode carregar arquivos de bulksheet, arquivos de erro de validação de página de aterrissagem corrigidos e outros arquivos de erro corrigidos de seu dispositivo ou rede para [redes de anúncios com suporte](about.md#bulksheet-functionality-by-network). Quaisquer colunas personalizadas no arquivo são excluídas ao fazer upload do arquivo.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Na barra de ferramentas, clique em **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Insira ou selecione informações nas [[!UICONTROL Upload Bulksheet] configurações](#bulksheet-upload-settings).

1. Clique em **[!UICONTROL Upload]**.

Quando a tarefa for iniciada, o arquivo será listado no modo de exibição [!UICONTROL Bulksheets]. Quando as notificações por email de bulksheets estão [habilitadas dentro de [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), uma notificação por email é enviada com um link para o arquivo quando o trabalho é concluído. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. Se a geração do arquivo falhar, um arquivo de erro será listado na exibição [!UICONTROL Bulksheets] e uma notificação será enviada por email com um link para o arquivo de erro.

>[!NOTE]
>
>Se você postar os dados do bulksheet na rede de anúncios, poderá seguir o progresso do arquivo na coluna [!UICONTROL Progress] na exibição [!UICONTROL Bulksheets]. Grandes quantidades de dados demoram mais para serem postadas.

## Fazer upload de configurações para bulksheets e arquivos de erro corrigidos {#bulksheet-upload-settings}

| Parâmetro | Descrição |
|----|----|
| [!UICONTROL File to Upload] | O arquivo a ser carregado. Especifique o arquivo clicando em **[!UICONTROL Choose File]** para localizá-lo no dispositivo ou na rede.<br><br>Os arquivos de bulksheet podem ter até 2,5 GB (cerca de 2,5 milhões de linhas) e devem ter uma das seguintes extensões de arquivo: *[!UICONTROL .tsv]* (para valores separados por tabulação), *[!UICONTROL .txt]* (para texto ASCII compatível com Unicode), *[!UICONTROL .csv]* (para valores separados por vírgula) ou *[!UICONTROL .zip]* (para formato ZIP compactado, que é descompactado em um arquivo TSV). O nome do arquivo não pode incluir os seguintes caracteres: `# % & * \| \ : " < > . ? /`<br><br>**Dica:** Para dados que incluem caracteres internacionais, use arquivos no formato TSV ou TXT. |
| [!UICONTROL Single Account] | Se o arquivo se aplica a uma conta: *[!UICONTROL Yes]* (para uma conta) ou *[!UICONTROL No]* (para várias contas). |
| [!UICONTROL Account (Search Engine)] | (Quando o arquivo se aplica a uma única conta) A conta na qual os dados serão carregados. |
| [!UICONTROL Search Engine] | (Quando o arquivo se aplica a várias contas) A rede de publicidade para a qual carregar os dados.<br><br>**Observação:** alterações de oferta para palavras-chave em portfólios otimizados não são suportadas com bulksheets de várias contas. |
| [!UICONTROL Scheduling] | Quando ou se publicar o arquivo na rede de publicidade especificada:<ul><li>*[!UICONTROL Post to search engine now]* (o padrão): começa a postar os dados imediatamente.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Começa a postar os dados na data e hora especificadas; o padrão é amanhã às 02:00 (2h). Para alterar a data, insira uma data no formato DD/MM/AAAA ou clique no ícone do calendário para abrir o calendário e selecionar uma data. Para alterar a hora, selecione uma hora (em intervalos de 15 minutos) na lista.</li><li>*[!UICONTROL Preview only]:* Faz upload do arquivo para Search, Social, &amp; Commerce sem postar os dados na rede de publicidade; você ainda pode postar o arquivo mais tarde. Quando o arquivo de bulksheet tem mais de 10 MB, mas tem menos de 2 GB, ele está no formato ZIP; não é necessário descompactar o arquivo para publicá-lo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se incluir modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento, ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para todas as palavras-chave, anúncios, posicionamentos, sitelinks e grupos de produtos [!DNL Google Ads] na postagem: *[!UICONTROL Yes]* (padrão) ou *[!UICONTROL No]*. Não importa se as unidades de oferta estão em um portfólio.<br><br>Se você selecionar *[!UICONTROL Yes]*, as URLs serão geradas de acordo com os parâmetros na seção [!UICONTROL Tracking Methods] das configurações de conta ou de campanha relevantes. Por padrão, se existirem URLs de rastreamento, elas não serão geradas novamente, a menos que novas sejam necessárias (como se o tipo de correspondência de palavra-chave, o texto do anúncio ou os parâmetros de rastreamento das contas relevantes tenham sido alterados).<br><br>Se você selecionar *[!UICONTROL No]*, ainda será possível gerar URLs de rastreamento posteriormente postando manualmente o arquivo carregado.<br><br>**Observação:** Se o anunciante usar o rastreamento de conversão do Adobe Advertising e a URL base tiver sido alterada, você deverá gerar novas URLs de rastreamento, a menos que a conta esteja configurada para gerar e carregar automaticamente URLs de rastreamento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponível quando [!UICONTROL Generate Tracking URLs] é *[!UICONTROL Yes]*) Substitui qualquer rastreamento de Adobe Advertising existente nas URLs do arquivo carregado por um rastreamento recém-gerado. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite alterações de orçamento em campanhas em portfólios otimizados com base em dados publicados. Por padrão, essa opção não está selecionada. Se você selecionar esta opção, todas as alterações de orçamento de campanha especificadas serão aplicáveis até que o recurso de otimização determine que o orçamento deve ser realocado (geralmente no próximo ciclo de ofertas).<br><br>**Observação:** todas as alterações de orçamento resultantes dos dados lançados para campanhas em portfólios não otimizados ocorrem quando o arquivo é lançado. As alterações aparecem nas exibições de gerenciamento de campanha no dia seguinte. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando os componentes da campanha incluídos estão em um portfólio otimizado, esse recurso substitui a estratégia de otimização e permite alterações de oferta com base nos dados na bulksheet até uma data final especificada. Se você selecionar essa opção, especifique uma data de término entre 1-7 dias distante no campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Sobre o gerenciamento de dados de campanha usando bulksheets](about.md)
>* [(Nova interface do usuário) Baixar/Criar um arquivo de bulksheet](download.md)
>* [(Nova interface do usuário) Postar bulksheets ou arquivos de erro corrigidos](post.md)
>* [(Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet](validate-landing-pages.md)
