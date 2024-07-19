---
title: Lançar bulksheets ou arquivos de erro corrigidos
description: Saiba como publicar arquivos de bulksheet em redes de anúncios.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Lançar bulksheets ou arquivos de erro corrigidos

Você pode postar arquivos de bulksheet ou arquivos de erro corrigidos nas contas relevantes para [redes de anúncios com suporte](bulksheet-about.md#bulksheet-functionality-by-network). Se o arquivo estiver no formato ZIP, não será necessário descompactá-lo primeiro.

Os arquivos de bulksheet e de erro são excluídos automaticamente 30 dias após serem carregados ou gerados.

>[!NOTE]
>Também é possível publicar um arquivo de bulksheet ou arquivo de erro ao fazer upload do arquivo.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Marque a caixa de seleção ao lado de cada arquivo a ser postado.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Post]**.

1. Na caixa de diálogo, insira ou selecione informações nas [[!UICONTROL Post Bulksheet] configurações](#bulksheet-post-settings) e clique em **[!UICONTROL Post]**.

   As mesmas configurações se aplicam a todos os arquivos publicados.

Quando a tarefa for iniciada, o status e a data de postagem agendada para a linha serão alterados no modo de exibição [!UICONTROL Bulksheets]. Quando o arquivo for postado, uma notificação por email será enviada com um link para o arquivo. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. No entanto, se algum dos dados não puder ser postado, um arquivo de erro será listado no modo de exibição [!UICONTROL Bulksheets] e uma notificação será enviada por email com um link para o arquivo de erro.

>[!NOTE]
>
>* Grandes quantidades de dados demoram mais para serem postadas. Você pode acompanhar o progresso do arquivo na coluna [!UICONTROL Progress] na exibição [!UICONTROL Bulksheets].
>* Todos os dados publicados estão sujeitos ao processo editorial da rede.
* Antes da publicação do arquivo de bulksheet, você pode cancelar a publicação.

## Configurações de publicação para bulksheets e arquivos de erro corrigidos {#bulksheet-post-settings}

| Parâmetro | Descrição |
|----|----|
| [!UICONTROL Account (Search Engine)] | A conta da rede de publicidade para a qual os dados são publicados. Se você postar vários arquivos simultaneamente ou um arquivo que se aplica a várias contas, o valor será <i>Várias Contas Selecionadas</i>.<br><br>A primeira letra do nome da rede de publicidade está entre parênteses após o nome da conta (como &quot;Acme Realty (G)&quot; para uma conta [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Quando publicar o arquivo na rede de anúncios especificada:<ul><li><i>[!UICONTROL Post to ad network now]</i> (o padrão): começa a postar os dados imediatamente.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Começa a postar os dados na data e hora especificadas; o padrão é amanhã às 02:00 (2:00). Para alterar a data, insira uma data no formato DD/MM/AAAA ou D/M/AAAA ou clique em ![Calendário](/help/search-social-commerce/assets/calendar.png "Calendário") para abrir o calendário e [selecione uma data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para alterar a hora, insira a hora no formato HH/MM ou H/M ou selecione uma hora (em intervalos de 15 minutos) na lista.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se incluir modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento, ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para todas as palavras-chave, anúncios, posicionamentos, sitelinks e grupos de produtos [!DNL Google Ads] na postagem: <i>[!UICONTROL Yes]</i> (padrão) ou <i>[!UICONTROL No]</i>. Não importa se as unidades de oferta estão em um portfólio.<br><br>Se você selecionar <i>[!UICONTROL Yes]</i>, as URLs serão geradas de acordo com os parâmetros na seção [!UICONTROL Tracking Methods] das configurações de conta ou de campanha relevantes. Por padrão, se existirem URLs de rastreamento, eles não serão gerados novamente, a menos que novos sejam necessários (como se o tipo de correspondência de palavras-chave, o texto do anúncio ou os parâmetros de rastreamento das contas relevantes tivessem sido alterados).<br><br>Se você selecionar <i>[!UICONTROL No]</i>, ainda será possível gerar URLs de rastreamento posteriormente postando manualmente o arquivo carregado.<br><br><b>Observação:</b> se o anunciante usar o rastreamento de conversão de Adobe Advertising e a URL base tiver sido alterada, você deverá gerar novas URLs de rastreamento, a menos que a conta esteja configurada para gerar e carregar automaticamente as URLs de rastreamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite alterações de orçamento em campanhas em portfólios otimizados com base em dados publicados. Por padrão, essa opção não está selecionada. Se você selecionar essa opção, quaisquer alterações de orçamento de campanha especificadas serão aplicáveis até que o recurso de otimização determine que o orçamento deve ser realocado (geralmente no próximo ciclo de ofertas).<br><br><b>Observação:</b> quaisquer alterações de orçamento resultantes dos dados postados para campanhas em portfólios não otimizados ocorrem quando o arquivo é postado. As alterações aparecem nas exibições de gerenciamento de campanha no dia seguinte. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando os componentes da campanha incluídos estão em um portfólio otimizado, esse recurso substitui a estratégia de otimização e permite alterações de oferta com base nos dados na bulksheet até uma data final especificada. Se você selecionar essa opção, especifique uma data de término entre 1-7 dias no campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](bulksheet-about.md)
>* [Baixar/Criar um arquivo de bulksheet](bulksheet-download.md)
>* [Carregar bulksheets ou arquivos de erro corrigidos](bulksheet-upload.md)
>* [Validar páginas de aterrissagem em arquivos de bulksheet](bulksheet-validate-landing-pages.md)
>* [Exportar um arquivo de bulksheet gerado ou carregado](bulksheet-export.md)
