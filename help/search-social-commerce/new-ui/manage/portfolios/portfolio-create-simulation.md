---
title: Executar e baixar simulações da exibição [!UICONTROL Portfolios]
description: Saiba como executar uma simulação personalizada e baixar simulações semanais na exibição Portfólios.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: 3e70998ad9547cecc0f3581d6cfd917051d549db
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---
# Executar e baixar simulações da exibição [!UICONTROL Portfolios]

*recurso do Beta*

Você pode executar uma simulação personalizada para um único portfólio [otimizado ou ativo](portfolio-about.md#portfolio-status) e baixar simulações semanais automatizadas para até 100 portfólios da exibição [!UICONTROL Portfolios].

Executar uma simulação personalizada requer a permissão [!UICONTROL Create Simulation]. Baixar simulações semanais requer a permissão [!UICONTROL View Simulation].

>[!NOTE]
>
>Você também pode [criar ou executar novamente uma simulação personalizada a partir da [!UICONTROL Simulations] exibição](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md).

## Executar uma simulação personalizada {#run-simulation}

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha do portfólio. Ao lado do nome do portfólio, clique em **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

   * Marque a caixa de seleção ao lado do portfólio. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL More]>[!UICONTROL Run Simulation]**.

1. Especifique as [configurações personalizadas da simulação](#custom-simulation-settings):

   1. Na guia **[!UICONTROL Basic Settings]**, insira um **[!UICONTROL Simulation Name]** exclusivo e altere os parâmetros básicos conforme necessário.

   1. (Opcional) Na guia **[!UICONTROL Advanced Settings]**, altere os parâmetros avançados.

   As configurações atuais do portfólio selecionado são usadas como padrão. Alterar as configurações de simulação não altera as configurações do portfólio.

1. Clique em **[!UICONTROL Next]**.

1. Revise as configurações e faça as alterações necessárias.

1. Clique em **[!UICONTROL Submit & Run]**.

A solicitação é enviada e a exibição [!UICONTROL Simulations] é aberta. Você pode [baixar a simulação](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md) depois que ela for concluída com êxito.

## Baixar simulações semanais {#download-simulations}

Você pode baixar simulações semanais para uma data de execução de cada vez como uma pasta de trabalho [!DNL Microsoft Excel] (arquivo XLSX). Somente portfólios ativos e otimizados com relatórios de simulação disponíveis para essa data são incluídos.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Marque a caixa de seleção ao lado de cada portfólio cuja simulação semanal você deseja baixar. Selecione até 100 portfólios.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL More]>[!UICONTROL Download Simulation]**.

1. Em **[!UICONTROL Weekly Simulation]**, selecione uma data de execução.

   A data disponível mais recente é selecionada por padrão. Se os relatórios não estiverem disponíveis para alguns portfólios selecionados, a caixa de diálogo mostrará quantos portfólios serão excluídos. Selecione outra data, se necessário. Não é possível baixar um relatório quando nenhum portfólio selecionado tem uma simulação disponível para essa data.

1. Clique no botão de download, cujo rótulo inclui o número de portfólios com relatórios disponíveis (por exemplo, **[!UICONTROL Download 2 portfolios]**).

   O arquivo é baixado de acordo com o procedimento normal do navegador. A mensagem de conclusão indica quantos portfólios foram incluídos.

Para baixar simulações personalizadas ou selecionar simulações semanais individuais, use a [[!UICONTROL Simulations] exibição](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md).

## Configurações personalizadas de simulação {#custom-simulation-settings}

Para obter mais informações sobre as configurações personalizadas da simulação, consulte o Guia de otimização, disponível em Pesquisa, Social e Commerce.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Exibir detalhes de desempenho do portfólio](portfolio-details.md)
>* [Sobre portfólios](portfolio-about.md)
>* [Executar ou executar novamente uma simulação personalizada](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [Baixar simulações](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
