---
title: Fazer upload de uma bulksheet ou arquivo de erro corrigido
description: Saiba como carregar manualmente um arquivo de bulksheet ou arquivo de erro de validação de página de aterrissagem corrigido.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Fazer upload de uma bulksheet ou arquivo de erro corrigido

Você pode carregar arquivos de bulksheet, arquivos de erro de validação de página de aterrissagem corrigidos e outros arquivos de erro corrigidos de seu dispositivo ou rede para [redes de anúncios com suporte](bulksheet-about.md#bulksheet-functionality-by-network). Quaisquer colunas personalizadas no arquivo são excluídas ao fazer upload do arquivo.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Upload Bulksheet]**.

1. Insira ou selecione informações nas [[!UICONTROL Upload Bulksheet] configurações](#bulksheet-upload-settings).

1. Clique em **[!UICONTROL Apply]**.

Quando a tarefa for iniciada, o arquivo será listado no modo de exibição [!UICONTROL Bulksheets]. Quando o arquivo estiver concluído, uma notificação por email será enviada com um link para o arquivo. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. No entanto, se a geração do arquivo falhar, um arquivo de erro será listado na exibição [!UICONTROL Bulksheets], e uma notificação por email será enviada com um link para o arquivo de erro.

>[!NOTE]
>
>Se você postar os dados do bulksheet na rede de anúncios, poderá seguir o progresso do arquivo na coluna [!UICONTROL Progress] na exibição [!UICONTROL Bulksheets]. Grandes quantidades de dados demoram mais para serem postadas.

## Fazer upload de configurações para bulksheets e arquivos de erro corrigidos {#bulksheet-upload-settings}

| Parâmetro | Descrição |
|----|----|
| [!UICONTROL File to Upload] | O arquivo a ser carregado. Especifique o arquivo inserindo o caminho completo e o nome do arquivo ou clicando em <b>[!UICONTROL Browse]</b> para localizar o arquivo no dispositivo ou na rede.<br><br>Os arquivos de bulksheet podem ter até 2,5 GB (cerca de 2,5 milhões de linhas) e devem ter uma das seguintes extensões de arquivo: <i>[!UICONTROL .tsv]</i> (para valores separados por tabulação), <i>[!UICONTROL .txt]</i> (para texto ASCII compatível com Unicode), <i>[!UICONTROL .csv]</i> (para valores separados por vírgula) ou <i>[!UICONTROL .zip]</i> (para formato ZIP compactado, que é descompactado em um arquivo TSV). O nome do arquivo não pode incluir os seguintes caracteres: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Dica:</b> Para dados que incluem caracteres internacionais, use arquivos no formato TSV ou TXT. |
| [!UICONTROL Single Account] | Se o arquivo se aplica a uma conta: <i>[!UICONTROL Yes]</i> (para uma conta) ou <i>[!UICONTROL No]</i> (para várias contas). |
| [!UICONTROL Account (Search Engine)] | (Quando o arquivo se aplica a uma única conta) A conta na qual os dados serão carregados. |
| [!UICONTROL Search Engine] | (Quando o arquivo se aplica a várias contas) A rede de publicidade na qual os dados serão carregados. |
| [!UICONTROL Scheduling] | Quando ou se publicar o arquivo na rede de publicidade especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (o padrão): começa a postar os dados imediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Começa a postar os dados na data e hora especificadas; o padrão é amanhã às 02:00 (2:00). Para alterar a data, insira uma data no formato DD/MM/AAAA ou D/M/AAAA ou clique em ![Calendário](/help/search-social-commerce/assets/calendar.png "Calendário") para abrir o calendário e [selecione uma data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para alterar a hora, insira a hora no formato HH/MM ou H/M ou selecione uma hora (em intervalos de 15 minutos) na lista.</li><li><i>[!UICONTROL Preview only]:</i> Para carregar o arquivo para Search, Social, &amp; Commerce sem postar os dados na rede de publicidade; você ainda pode postar o arquivo mais tarde. Quando o arquivo de bulksheet tem mais de 10 MB, mas tem menos de 2 GB, ele está no formato ZIP; não é necessário descompactar o arquivo para publicá-lo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se incluir modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento, ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para todas as palavras-chave, anúncios, posicionamentos, sitelinks e grupos de produtos [!DNL Google Ads] na postagem: <i>[!UICONTROL Yes]</i> (padrão) ou <i>[!UICONTROL No]</i>. Não importa se as unidades de oferta estão em um portfólio.<br><br>Se você selecionar <i>[!UICONTROL Yes]</i>, as URLs serão geradas de acordo com os parâmetros na seção [!UICONTROL Tracking Methods] das configurações de conta ou de campanha relevantes. Por padrão, se existirem URLs de rastreamento, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavras-chave, o texto do anúncio ou os parâmetros de rastreamento das contas relevantes tivessem sido alterados).<br><br>Se você selecionar <i>[!UICONTROL No]</i>, ainda será possível gerar URLs de rastreamento posteriormente postando manualmente o arquivo carregado.<br><br><b>Observação:</b> se o anunciante usar o rastreamento de conversão do Adobe Advertising e a URL base tiver sido alterada, você deverá gerar novas URLs de rastreamento, a menos que a conta esteja configurada para gerar e carregar automaticamente as URLs de rastreamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite alterações de orçamento em campanhas em portfólios otimizados com base em dados publicados. Por padrão, essa opção não está selecionada. Se você selecionar essa opção, quaisquer alterações de orçamento de campanha especificadas serão aplicáveis até que o recurso de otimização determine que o orçamento deve ser realocado (geralmente no próximo ciclo de ofertas).<br><br><b>Observação:</b> quaisquer alterações de orçamento resultantes dos dados postados para campanhas em portfólios não otimizados ocorrem quando o arquivo é postado. As alterações aparecem nas exibições de gerenciamento de campanha no dia seguinte. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando os componentes da campanha incluídos estão em um portfólio otimizado, esse recurso substitui a estratégia de otimização e permite alterações de oferta com base nos dados na bulksheet até uma data final especificada. Se você selecionar essa opção, especifique uma data de término entre 1-7 dias no campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Baixar/Criar um arquivo de bulksheet](bulksheet-download.md)
>* [Postar bulksheets ou arquivos de erro corrigidos](bulksheet-post.md)
>* [Validar páginas de aterrissagem em arquivos de bulksheet](bulksheet-validate-landing-pages.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)
