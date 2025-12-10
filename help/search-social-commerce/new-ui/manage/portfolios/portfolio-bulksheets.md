---
title: Editar configurações de portfólio em massa usando arquivos de bulksheet
description: Saiba como editar as configurações de vários portfólios usando um arquivo de bulksheet.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 14f85e5ff5655be045fa4a2280edc1fe01978029
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Editar configurações de portfólio em massa usando arquivos de bulksheet

*recurso do Beta*

Um bulksheet de portfólio é um arquivo que contém configurações de portfólio em um formato específico e pode ser usado para revisar e modificar rapidamente as configurações. Você pode gerar (baixar) bulksheets com configurações para um ou mais portfólios. O arquivo foi baixado como uma pasta de trabalho [!DNL Excel] com duas planilhas (formato XLSX). A pasta de trabalho inclui:

* Uma planilha [!UICONTROL Instructions] somente leitura com informações sobre a edição dos campos.

* Uma guia [!UICONTROL Portfolio Settings Edit], com uma linha por portfólio incluído. Opcionalmente, é possível editar os campos conforme necessário, salvar o arquivo localmente e, em seguida, [carregar o arquivo editado](#portfolio-bulksheet-upload) para Search, Social e Commerce. Os campos editáveis são realçados em cores.

## Baixar um arquivo de bulksheet com configurações de portfólio

1. Marque a caixa de seleção ao lado de cada portfólio a ser incluído na planilha em massa.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Insira o nome do arquivo de bulksheet a ser criado e clique em **[!UICONTROL Export Now]**.

   O arquivo é salvo na pasta de downloads padrão do navegador.

## Fazer upload de um arquivo de bulksheet com configurações atualizadas do portfólio {#portfolio-bulksheet-upload}

O arquivo deve estar no formato XLSX.

1. Na barra de ferramentas acima da tabela de dados, clique em **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**. &lt;!— Deve ser &quot;Importar configurações do Portfolio&quot; — &quot;Detalhes&quot; podem ser muito vagos e sugerem que podem incluir algo diferente. —>

1. Na caixa de diálogo [!UICONTROL Import Portfolio Details File]:<!-- reword if we change the name of the operation -->

   1. Arraste e solte um arquivo na caixa ou clique em **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->para selecionar um arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Import]**.

Você pode verificar o status do carregamento usando o botão [!UICONTROL Global Sync Status] (![Status de Sincronização Global](/help/search-social-commerce/assets/global-sync-status.png "Status de Sincronização Global")) ao lado do seletor de intervalo de datas.<!-- icon similar to Refresh -->. Se qualquer uma das alterações não tiver sido bem-sucedida, você poderá baixar um arquivo de erro mostrando o que falhou.

As notificações também são adicionadas à Central de Notificações, e você pode abrir o painel Notificações no ícone ![Notificações](/help/search-social-commerce/assets/notifications-new.png "Notificações") ao lado do botão [!UICONTROL Global Sync Status] (![Status da sincronização global](/help/search-social-commerce/assets/global-sync-status.png "Status da sincronização global")).

## Requisitos em matéria de dados para os ficheiros de bulksheet carregados

Todos os arquivos de bulksheet devem incluir a coluna [!UICONTROL Portfolio ID], e cada linha de dados deve incluir um valor para que [!UICONTROL Portfolio ID] seja acionável. Para obter mais informações sobre os requisitos de dados, consulte a guia [!UICONTROL Instructions] no arquivo de bulksheet baixado.

Para obter explicações sobre as colunas de configuração do portfólio na guia [!UICONTROL Portfolio Settings Edit], consulte o Guia de Otimização, que está disponível no Search, Social e Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Editar um portfólio](portfolio-edit.md)
>* [Criar um portfólio](portfolio-create.md)
>* [(Nova Interface do Usuário) Sobre portfólios](portfolio-about.md)
