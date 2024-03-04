---
title: Lançar bulksheets ou arquivos de erro corrigidos
description: Saiba como publicar arquivos de bulksheet em redes de anúncios.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: f68b2eb267391972eed94e4fec3ea386fbf206c6
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Lançar bulksheets ou arquivos de erro corrigidos

Você pode publicar arquivos de bulksheet ou arquivos de erro corrigidos nas contas relevantes para [redes de publicidade suportadas](bulksheet-about.md#bulksheet-functionality-by-network). Se o arquivo estiver no formato ZIP, não será necessário descompactá-lo primeiro.

Os arquivos de bulksheet e de erro são excluídos automaticamente 30 dias após serem carregados ou gerados.

>[!NOTE]
>Também é possível publicar um arquivo de bulksheet ou arquivo de erro ao fazer upload do arquivo.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Marque a caixa de seleção ao lado de cada arquivo a ser postado.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Post]**.

1. Na caixa de diálogo, insira ou selecione informações na caixa de diálogo [[!UICONTROL Post Bulksheet] configurações](#bulksheet-post-settings)e clique em **[!UICONTROL Post]**.

   As mesmas configurações se aplicam a todos os arquivos publicados.

Quando a tarefa for iniciada, o status e a data de publicação agendada para a linha serão alterados no [!UICONTROL Bulksheets] exibição. Quando o arquivo for postado, uma notificação por email será enviada com um link para o arquivo. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. No entanto, se algum dos dados não puder ser publicado, um arquivo de erro será listado no [!UICONTROL Bulksheets] e uma notificação por email é enviada com um link para o arquivo de erro.

>[!NOTE]
>
>* Grandes quantidades de dados demoram mais para serem postadas. É possível acompanhar o progresso do arquivo no [!UICONTROL Progress] na [!UICONTROL Bulksheets] exibição.
>* Todos os dados publicados estão sujeitos ao processo editorial da rede.
* Antes da publicação do arquivo de bulksheet, você pode cancelar a publicação.

## Configurações de publicação para bulksheets e arquivos de erro corrigidos {#bulksheet-post-settings}

| Parâmetro | Descrição |
|----|----|
| [!UICONTROL Account (Search Engine)] | A conta da rede de publicidade para a qual os dados são publicados. Se você publicar vários arquivos simultaneamente ou um arquivo que se aplique a várias contas, o valor será <i>Várias contas selecionadas</i>.<br><br>A primeira letra do nome da rede de publicidade está entre parênteses após o nome da conta (como &quot;Acme Realty (G)&quot; de [!DNL Google Ads] conta). |
| [!UICONTROL Scheduling] | Quando publicar o arquivo na rede de anúncios especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (o padrão): começa a postar os dados imediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Começa a postar os dados na data e hora especificadas; o padrão é amanhã às 02:00 (2:00). Para alterar a data, insira uma data no formato DD/MM/AAAA ou D/M/AAAA ou clique em ![Calendário](assets/calendar.png "Calendário") para abrir o calendário e [selecionar uma data](/advertising.en/help/search-social-commerce/campaign-management/bulksheets/assets/calendar.png). Para alterar a hora, insira a hora no formato HH/MM ou H/M ou selecione uma hora (em intervalos de 15 minutos) na lista.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se incluir modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para todas as palavras-chave, anúncios, posicionamentos, sitelinks e [!DNL Google Ads] grupos de produtos no lançamento: <i>[!UICONTROL Yes]</i> (o padrão) ou <i>[!UICONTROL No]</i>. Não importa se as unidades de oferta estão em um portfólio.<br><br>Se você selecionar <i>[!UICONTROL Yes]</i>, os URLs são gerados de acordo com os parâmetros no [!UICONTROL Tracking Methods] seção das configurações relevantes da conta ou das configurações da campanha. Por padrão, se existirem URLs de rastreamento, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavras-chave, o texto do anúncio ou os parâmetros de rastreamento das contas relevantes tivessem sido alterados).<br><br>Se você selecionar <i>[!UICONTROL No]</i>, você ainda poderá gerar URLs de rastreamento posteriormente postando manualmente o arquivo carregado.<br><br><b>Nota:</b> Se o anunciante usar o rastreamento de conversão de Adobe Advertising e o URL de base tiver sido alterado, você deverá gerar novos URLs de rastreamento, a menos que a conta esteja configurada para gerar e carregar automaticamente URLs de rastreamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite alterações de orçamento em campanhas em portfólios otimizados com base em dados publicados. Por padrão, essa opção não está selecionada. Se você selecionar essa opção, quaisquer alterações de orçamento de campanha especificadas serão aplicáveis até que o recurso de otimização determine que o orçamento deve ser realocado (geralmente no próximo ciclo de ofertas).<br><br><b>Nota:</b> Quaisquer alterações de orçamento resultantes dos dados publicados para campanhas em portfólios não otimizados ocorrem quando o arquivo é publicado. As alterações aparecem nas exibições de gerenciamento de campanha no dia seguinte. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando os componentes da campanha incluídos estão em um portfólio otimizado, esse recurso substitui a estratégia de otimização e permite alterações de oferta com base nos dados na bulksheet até uma data final especificada. Se você selecionar essa opção, especifique uma data de término entre 1 e 7 dias na **[!UICONTROL Hold bulksheet bids until]** campo. |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Baixar/criar um arquivo de bulksheet](bulksheet-download.md)
>* [Fazer upload de bulksheets ou arquivos de erro corrigidos](bulksheet-upload.md)
>* [Validar páginas de aterrissagem em arquivos de bulksheet](bulksheet-validate-landing-pages.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)
