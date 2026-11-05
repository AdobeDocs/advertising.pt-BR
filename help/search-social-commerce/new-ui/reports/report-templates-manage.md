---
title: (Nova interface do usuário) Gerenciar modelos de relatório
description: Saiba como criar, exibir, editar e excluir modelos de relatório reutilizáveis para relatórios agendados e por demanda.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# (Nova interface do usuário) Gerenciar modelos de relatório

Os modelos de relatório são layouts predefinidos de relatório que podem ser reutilizados na maioria dos relatórios gerados. A utilização de modelos poupa tempo se você quiser usar parâmetros não padrão, executar variações do mesmo relatório ou executar o mesmo relatório de acordo com uma programação regular. Os modelos salvos estão disponíveis na guia **[!UICONTROL Templates]** em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

É possível manter até 100 modelos por vez.

A visualização dos dados requer a permissão [!UICONTROL View Scheduled Reports]. Criar, duplicar, editar, executar e excluir modelos, bem como copiar dados de linha, requer a permissão [!UICONTROL Edit Scheduled Reports]. Você pode editar somente os modelos criados.

## Ações disponíveis

* [Criar um modelo de relatório](#template-create) como um novo modelo ou com base em um modelo existente.

* [Exiba as configurações de um modelo de relatório sem alterar o original](#template-view).

* [Editar um modelo de relatório](#template-edit), incluindo seu agendamento.

* [Executar relatórios sob demanda para modelos especificados](#template-run).

* [Excluir modelos de relatório](#template-delete).

* [Copie todos os dados nas linhas selecionadas para a área de transferência](#copy-to-clipboard).

## Criar um modelo de relatório {#template-create}

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Siga um destes procedimentos:

   * Para criar um novo modelo, clique em **[!UICONTROL Create Template]**. No painel **[!UICONTROL Create a New Template]**, selecione a categoria de relatório e o tipo de relatório e clique em **[!UICONTROL Proceed]**.

   * Para criar um modelo baseado em um modelo existente, mantenha o cursor sobre a linha de modelo e clique em ![Configurações de Modelo](/help/search-social-commerce/assets/settings-new.png "Configurações de Modelo") **[!UICONTROL Template Settings]** ou **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Insira um **[!UICONTROL Report Name]** exclusivo para o modelo e verifique se **[!UICONTROL Save as Template]** está habilitado.

   A configuração é habilitada por padrão quando você começa com **[!UICONTROL Create Template]**. Se você desabilitá-lo, a ação final será alterada para **[!UICONTROL Run Report]**, o que gerará um relatório em vez de salvar um modelo.

1. Defina as configurações de relatório para [relatórios básicos e avançados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [relatórios de assistência](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [relatórios de precisão de modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) ou [relatórios especializados](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Clique em **[!UICONTROL Next]** para mover entre as seções de configurações.

1. (Opcional) Para gerar relatórios automaticamente, defina o **[!UICONTROL Frequency]** e as configurações de entrega no **[!UICONTROL Scheduling]**.

1. Clique em **[!UICONTROL Create]**.

Você também pode salvar um modelo enquanto [cria um relatório a partir da guia Relatórios Mais Recentes](/help/search-social-commerce/new-ui/reports/management/report-manage.md), habilitando **[!UICONTROL Save as Template]** antes de enviar as configurações do relatório.

## Exibir as configurações de um modelo de relatório {#template-view}

Para inspecionar as configurações sem alterar o modelo original, abra uma duplicata. Isso requer a permissão [!UICONTROL Edit Scheduled Reports]. Abrir a duplicata não salva um novo modelo.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre a linha do modelo e clique em ![Configurações do Modelo](/help/search-social-commerce/assets/settings-new.png "Configurações do Modelo") **[!UICONTROL Template Settings]**.

1. Revise as configurações do relatório.

1. Clique em **[!UICONTROL Cancel]** quando terminar. Se for solicitado que você descarte a instalação, clique em **[!UICONTROL Discard]**.

Para salvar uma cópia, siga o [procedimento de criação do modelo](#template-create).

## Editar um modelo de relatório {#template-edit}

É possível alterar as configurações e o agendamento de qualquer modelo criado. As alterações se aplicam aos relatórios gerados a partir do modelo no futuro.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Marque a caixa de seleção ao lado de um modelo criado.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

   [!UICONTROL Edit] não está disponível quando vários modelos são selecionados ou o modelo selecionado foi criado por outro usuário.

1. Alterar as configurações do relatório. Para adicionar, alterar ou remover um agendamento, edite **[!UICONTROL Frequency]** em **[!UICONTROL Scheduling]**.

   Selecione uma frequência diária, semanal ou mensal para os relatórios agendados. Para remover um agendamento recorrente, selecione **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** e **[!UICONTROL Type]** são somente leitura ao editar um modelo existente. Você não precisa habilitar [!UICONTROL Save as Template] novamente.

1. Clique em **[!UICONTROL Save]**.

## Executar relatórios sob demanda para modelos especificados {#template-run}

É possível executar relatórios para um ou mais modelos a qualquer momento.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Siga um destes procedimentos:

   * (Para executar um único modelo):

     1. Abra o menu da linha de modelo e selecione **[!UICONTROL Run]**.

     1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

   * (Para executar um ou mais templates):

     1. Marque a caixa de seleção ao lado de cada modelo que deseja executar.

     1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Run]**.

     1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

Você também pode executar um modelo ao editá-lo clicando em **[!UICONTROL Run Report]** e depois em **[!UICONTROL Confirm]**. Salve as alterações primeiro; essa ação executa o modelo salvo.

## Excluir modelos de relatório {#template-delete}

É possível excluir qualquer modelo de relatório disponível. Quando você exclui um modelo que inclui um agendamento, esse relatório não é gerado no futuro.

1. No menu principal, clique em **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. Siga um destes procedimentos:

   * (Para excluir um único modelo):

     1. Abra o menu da linha de modelo e selecione **[!UICONTROL Delete]**.

     1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

   * (Para excluir um ou mais templates):

     1. Marque a caixa de seleção ao lado de cada modelo que deseja excluir.

     1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete]**.

     1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## Copiar todos os dados nas linhas selecionadas para a área de transferência {#copy-to-clipboard}

Copie as informações visíveis nas linhas selecionadas, de acordo com os filtros e colunas aplicados visíveis na exibição. As informações são salvas como valores separados por tabulação (TSV).

1. Marque a caixa de seleção ao lado de cada linha cujos dados você deseja copiar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Copy]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.
