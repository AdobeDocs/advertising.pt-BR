---
title: Executar ou executar novamente uma simulação personalizada
description: Saiba como executar ou executar novamente uma simulação personalizada de um portfólio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# Executar ou executar novamente uma simulação personalizada

*recurso do Beta*

Você pode gerar uma simulação personalizada para um portfólio [otimizado ou ativo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status). Você também pode selecionar uma simulação na lista para executar uma nova simulação para o mesmo portfólio ou executar simulações novamente com as configurações existentes.

Criar uma simulação personalizada requer a permissão [!UICONTROL Create Simulation]. A seleção de um portfólio requer a permissão [!UICONTROL View Portfolios].

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] e [!UICONTROL Account Manager] usuários podem ver simulações criadas por outros usuários. Todos os outros usuários podem ver somente as simulações personalizadas que criam.

## Criar uma nova simulação {#simulation-create}

Você pode começar no modo de exibição [!UICONTROL Simulations] ou [executar uma simulação personalizada no modo de exibição [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. No menu principal, clique em **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Limpe todas as linhas de simulação selecionadas e clique em **[!UICONTROL Run Simulation]**.

1. Selecione o portfólio:

   1. Clique em **[!UICONTROL Select Portfolio]**.

   1. Selecione o portfólio.

      Para pesquisar portfólios que incluem uma sequência de texto específica, comece inserindo a sequência de texto no campo de pesquisa. Os valores não diferenciam maiúsculas de minúsculas.

   1. Clique em **[!UICONTROL Proceed]**.

1. Especifique as [configurações personalizadas da simulação](#custom-simulation-settings):

   1. (Opcional) Para alterar o portfólio usado para a simulação, clique em **[!UICONTROL Change Portfolio]** ao lado do nome do portfólio, selecione o portfólio e clique em **[!UICONTROL Proceed]**.

   1. Na guia [!UICONTROL Basic Settings]:

      1. Digite um **[!UICONTROL Simulation Name]** exclusivo.

      1. (Opcional) Altere os parâmetros básicos da simulação.

   1. (Opcional) Na guia [!UICONTROL Advanced Settings], altere os parâmetros avançados da simulação.

   Os parâmetros existentes para o portfólio selecionado são especificados por padrão. Alterar os valores mostrará os resultados que diferentes parâmetros produziriam sem alterar os parâmetros existentes do portfólio.

1. Clique em **[!UICONTROL Next]**.

1. Revise as configurações e edite as configurações conforme necessário.

1. Clique em **[!UICONTROL Submit & Run]**.

A solicitação é enviada e a exibição [!UICONTROL Simulations] é aberta. Quando o relatório de simulação estiver disponível, você e qualquer outro destinatário de email especificado receberão uma notificação com um link de download. Você também pode [baixar a simulação da [!UICONTROL Simulations] exibição](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Executar uma simulação novamente com as configurações existentes {#rerun-a-simulation-with-the-existing-settings}

É possível executar novamente até 10 simulações de cada vez com as configurações existentes. Simulações com status [!UICONTROL Queued] ou [!UICONTROL In Progress] não podem ser executadas novamente. Se sua seleção incluir essas simulações, elas serão ignoradas e as simulações restantes serão enviadas.

1. No menu principal, clique em **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Marque as caixas de seleção ao lado das simulações que deseja executar novamente.

1. Na barra de ferramentas acima da tabela de dados ou na barra de ferramentas de ações em massa, clique em **[!UICONTROL Re-Run Simulation]**.

A solicitação é enviada e a exibição é atualizada.

## Executar uma nova simulação para um portfólio na lista {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Selecionar uma simulação antes de clicar em [!UICONTROL Run Simulation] seleciona seu portfólio para uma nova simulação. O formulário usa as configurações atuais do portfólio, não as configurações da simulação selecionada. Esta ação não edita a simulação existente.

1. No menu principal, clique em **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Marque a caixa de seleção ao lado de uma simulação para o portfólio que você deseja usar.

   Se você selecionar várias simulações, elas deverão usar o mesmo portfólio. O portfólio deve estar ativo ou otimizado.

1. Acima da tabela de dados, clique em **[!UICONTROL Run Simulation]**.

1. Especifique as [configurações personalizadas da simulação](#custom-simulation-settings), incluindo uma **[!UICONTROL Simulation Name]** exclusiva. Altere os parâmetros nas guias **[!UICONTROL Basic Settings]** e **[!UICONTROL Advanced Settings]** conforme necessário.

1. Clique em **[!UICONTROL Next]**.

1. Revise as configurações e edite as configurações conforme necessário.

1. Clique em **[!UICONTROL Submit & Run]**.

A solicitação é enviada e a exibição [!UICONTROL Simulations] é aberta. Você pode [baixar a simulação](simulation-download.md) depois que ela for concluída com êxito.

## Configurações personalizadas de simulação {#custom-simulation-settings}

Para obter mais informações sobre as configurações personalizadas da simulação, consulte o Guia de otimização, disponível em Pesquisa, Social e Commerce.

>[!MORELIKETHIS]
>
>* [Sobre simulações](simulation-about.md)
>* [Exibir detalhes da simulação](simulation-view.md)
>* [Baixar simulações](simulation-download.md)
