---
title: Criar uma métrica personalizada
description: Saiba como configurar métricas personalizadas, que são calculadas a partir das métricas padrão.
exl-id: a9ce503a-67ee-477e-8f79-31b4a9c6e51a
feature: Search Common Tasks, Search Custom Metrics
TQID: 'https://experienceleague.adobe.com/g-J8AlulQ20I-vxQrPkPaP-Ap66bBIng0eKDPqhV9U4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: a1695a4d-41fb-5bb6-a22a-9e7a1b3222d7
    internal-label: Search Custom Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 9837cac1a920b1b3b88b04b150cb604832209eaf
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%
---
# Criar uma métrica personalizada

## (Nova interface do usuário) Criar uma métrica personalizada a partir de uma exibição de gerenciamento

*Disponível na maioria das exibições de entidade no menu [!UICONTROL Manage],<!-- [!UICONTROL Plan] > [!UICONTROL Simulations],--> [!UICONTROL Setup] > [!UICONTROL Label Classifications], [!UICONTROL Goals] > [!UICONTROL Objectives] e [!UICONTROL Constraints], e [!UICONTROL Targeting] > [!UICONTROL Placements]*

1. Acima da tabela de dados, siga um destes procedimentos:

   * Clique no nome da exibição aplicada no momento (![Exibição](/help/search-social-commerce/assets/view.png "Exibição")). Mantenha o cursor sobre o nome de qualquer modo de exibição editável e clique em ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") para abrir as configurações de modo.

     A métrica personalizada que você criar ficará disponível em todas as suas exibições.

   * Clique em ![Colunas personalizadas](/help/search-social-commerce/assets/custom-columns-new.png "Colunas personalizadas") para abrir as definições de configuração da coluna.

1. Abaixo da lista de colunas que é aberta, clique em ![Criar métrica personalizada](/help/search-social-commerce/assets/add.png "Criar métrica personalizada") **[!UICONTROL Create Custom Metric]**.

1. Especifique as [configurações de métrica personalizada](custom-metric-settings.md).

1. Clique em **[!UICONTROL Create]**.

## (Nova interface do usuário) Criar uma métrica personalizada a partir das configurações do relatório ou do modelo de relatório {#create-from-report-settings}

1. Nas configurações do relatório ou do modelo de relatório, vá para a etapa **[!UICONTROL Columns]**.

1. Na seção **[!UICONTROL Custom Metrics]**, especifique as configurações de métrica:

   * **[!UICONTROL Custom Metric Name]:** Insira um nome para a métrica.

   * **[!UICONTROL Format]:** Selecione **[!UICONTROL Currency]**, **[!UICONTROL Number to 2 Decimal Places]**, **[!UICONTROL Number to 3 Decimal Places]**, **[!UICONTROL Number w/out Decimal Places]** ou **[!UICONTROL Percentage]**.

   * **[Campo de entrada da fórmula]:** crie a fórmula selecionando métricas de **[!UICONTROL Insert Metric]** e clicando nos botões do operador (`+`, `-`, `*`, `/`, `(` e `)`). Também é possível inserir a fórmula manualmente. Coloque o cursor onde deseja inserir cada métrica ou operador.

1. Clique em **[!UICONTROL Add Metric]**.

   Depois que a métrica é criada com sucesso, a lista de colunas disponíveis é filtrada pelo nome da métrica. A criação da métrica não a inclui automaticamente no relatório.

1. Para incluir a métrica no relatório, selecione-a na lista de colunas disponíveis e clique em ![Seta para a direita](/help/search-social-commerce/assets/arrow-right-customize.png "Seta para a direita") para movê-la para a lista de colunas selecionadas.

## (Interface herdada) Criar uma métrica personalizada de uma exibição de gerenciamento de campanha

1. Acima da tabela de dados, siga um destes procedimentos:

   * Clique no nome da exibição padrão ou personalizada para abrir as configurações de exibição.

   * Clique em ![Colunas personalizadas](/help/search-social-commerce/assets/custom-columns.png "Colunas personalizadas") para abrir as definições de configuração da coluna.

1. Abaixo da lista de colunas que é aberta, clique em ![Criar nova métrica personalizada](/help/search-social-commerce/assets/add.png "Criar nova métrica personalizada") **[!UICONTROL Create New Custom Metric]**.

1. Especifique as [configurações de métrica personalizada](custom-metric-settings.md).

1. Clique em **[!UICONTROL Save]**.

## (Interface herdada) Criar uma métrica personalizada de um relatório ou formulário de modelo de relatório

1. Em um relatório ou formulário de modelo de relatório, vá para a guia **[!UICONTROL Columns]**.

1. Na seção direita, clique em **[!UICONTROL Create]**.

1. Especifique as [configurações de métrica personalizada](custom-metric-settings.md).

1. Clique em **[!UICONTROL Submit]**.

## (Interface herdada) Criar uma métrica personalizada a partir das [!UICONTROL Portfolios] exibições

1. Acima da tabela de dados, clique em ![Editar Exibição Selecionada](/help/search-social-commerce/assets/view-settings.png "Editar Exibição Selecionada").

1. Clique na guia **[!UICONTROL Columns]**.

1. Na seção direita, clique em **[!UICONTROL Create]**.

1. Especifique as [configurações de métrica personalizada](custom-metric-settings.md).

1. Clique em **[!UICONTROL Submit]**.

>[!MORELIKETHIS]
>
>* [Sobre métricas personalizadas](custom-metric-about.md)
>* [Editar uma métrica personalizada](custom-metric-edit.md)
>* [Excluir uma métrica personalizada](custom-metric-delete.md)
>* [Configurações de métrica personalizada](custom-metric-settings.md)
