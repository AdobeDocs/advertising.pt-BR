---
title: (Nova interface do usuário) Publicar bulksheets ou arquivos de erro corrigidos
description: Saiba como publicar arquivos de bulksheet em suas redes de anúncios na nova interface do Search, Social e Commerce.
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
source-git-commit: 739034010787c2016720bef37fb75dc8efbae58b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# (Nova interface do usuário) Publicar bulksheets ou arquivos de erro corrigidos

Você pode postar arquivos de bulksheet ou arquivos de erro corrigidos nas contas relevantes para [redes de anúncios com suporte](about.md#bulksheet-functionality-by-network). Se o arquivo estiver no formato ZIP, não será necessário descompactá-lo primeiro.

Os arquivos de bulksheet e de erro são excluídos automaticamente 30 dias após serem carregados ou gerados.

>[!NOTE]
>
>Também é possível publicar um arquivo de bulksheet ou arquivo de erro ao fazer upload do arquivo.

1. No menu principal, clique em **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Marque a caixa de seleção ao lado de cada arquivo a ser postado.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Post]**.

1. Insira ou selecione informações nas [[!UICONTROL Post Bulksheet] configurações](#bulksheet-post-settings) e clique em **[!UICONTROL Post]**.

   As mesmas configurações se aplicam a todos os arquivos publicados.

Quando a tarefa for iniciada, o status e a data de postagem agendada para a linha serão atualizados no modo de exibição [!UICONTROL Bulksheets]. Quando as notificações por email de bulksheets estão [habilitadas dentro de [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), uma notificação por email com um link para o arquivo é enviada quando o arquivo é postado. Dependendo da quantidade de dados compilados, a notificação por email pode levar vários minutos ou mais. Se algum dos dados não puder ser postado, um arquivo de erro será listado no modo de exibição [!UICONTROL Bulksheets] e uma notificação será enviada por email com um link para o arquivo de erro.

>[!NOTE]
>
>* Grandes quantidades de dados demoram mais para serem postadas. Você pode acompanhar o progresso do arquivo na coluna [!UICONTROL Progress] na exibição [!UICONTROL Bulksheets].
>* Todos os dados publicados estão sujeitos ao processo editorial da rede.
>* Antes da publicação do arquivo de bulksheet, você pode cancelar a publicação.

## Configurações de publicação para bulksheets e arquivos de erro corrigidos {#bulksheet-post-settings}

| Parâmetro | Descrição |
|----|----|
| [!UICONTROL Account (Search Engine)] | A conta da rede de publicidade para a qual os dados são publicados. Se você postar vários arquivos simultaneamente ou um arquivo que se aplica a várias contas, o valor será *Várias Contas Selecionadas*.<br><br>A primeira letra do nome da rede de publicidade está entre parênteses após o nome da conta (como &quot;Acme Realty (G)&quot; para uma conta [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Quando publicar o arquivo na rede de anúncios especificada:<ul><li>*[!UICONTROL Post to ad network now]* (o padrão): começa a postar os dados imediatamente.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Começa a postar os dados na data e hora especificadas; o padrão é amanhã às 02:00 (2h). Para alterar a data, insira uma data no formato DD/MM/AAAA ou clique no ícone do calendário para abrir o calendário e selecionar uma data. Para alterar a hora, selecione uma hora (em intervalos de 15 minutos) na lista.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se incluir modelos de rastreamento e sufixos de página de aterrissagem (para redes de anúncios aplicáveis) em contas com modelos de rastreamento, ou URLs de destino com códigos de rastreamento incorporados em contas com URLs de destino, para todas as palavras-chave, anúncios, posicionamentos, sitelinks e grupos de produtos [!DNL Google Ads] na postagem: *[!UICONTROL Yes]* (padrão) ou *[!UICONTROL No]*. Não importa se as unidades de oferta estão em um portfólio.<br><br>Se você selecionar *[!UICONTROL Yes]*, as URLs serão geradas de acordo com os parâmetros na seção [!UICONTROL Tracking Methods] das configurações de conta ou de campanha relevantes. Por padrão, se existirem URLs de rastreamento, elas não serão geradas novamente, a menos que novas sejam necessárias (como se o tipo de correspondência de palavra-chave, o texto do anúncio ou os parâmetros de rastreamento das contas relevantes tenham sido alterados).<br><br>Se você selecionar *[!UICONTROL No]*, ainda será possível gerar URLs de rastreamento posteriormente postando manualmente o arquivo carregado.<br><br>**Observação:** Se o anunciante usar o rastreamento de conversão do Adobe Advertising e a URL base tiver sido alterada, você deverá gerar novas URLs de rastreamento, a menos que a conta esteja configurada para gerar e carregar automaticamente URLs de rastreamento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponível quando [!UICONTROL Generate Tracking URLs] é *[!UICONTROL Yes]*) Substitui qualquer rastreamento de Adobe Advertising existente nas URLs do arquivo carregado por um rastreamento recém-gerado. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permite alterações de orçamento em campanhas em portfólios otimizados com base em dados publicados. Por padrão, essa opção não está selecionada. Se você selecionar esta opção, todas as alterações de orçamento de campanha especificadas serão aplicáveis até que o recurso de otimização determine que o orçamento deve ser realocado (geralmente no próximo ciclo de ofertas).<br><br>**Observação:** todas as alterações de orçamento resultantes dos dados lançados para campanhas em portfólios não otimizados ocorrem quando o arquivo é lançado. As alterações aparecem nas exibições de gerenciamento de campanha no dia seguinte. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando os componentes da campanha incluídos estão em um portfólio otimizado, esse recurso substitui a estratégia de otimização e permite alterações de oferta com base nos dados na bulksheet até uma data final especificada. Se você selecionar essa opção, especifique uma data de término entre 1-7 dias no campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Sobre o gerenciamento de dados de campanha usando bulksheets](about.md)
>* [(Nova interface do usuário) Baixar/Criar um arquivo de bulksheet](download.md)
>* [(Nova interface do usuário) Carregar um bulksheet ou arquivo de erro corrigido](upload.md)
>* [(Nova interface do usuário) Validar páginas de aterrissagem em arquivos de bulksheet](validate-landing-pages.md)
>* [(Nova interface do usuário) Excluir bulksheets e arquivos de erro carregados](delete.md)
