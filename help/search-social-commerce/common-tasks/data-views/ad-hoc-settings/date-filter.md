---
title: Filtrar dados por intervalo de datas
description: Saiba como usar o filtro de intervalo de datas global.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Filtrar dados por intervalo de datas

<!-- The same in new UI and legacy CM views -->

O mesmo filtro de intervalo de datas global é aplicado à maioria das visualizações de dados, em todos os anunciantes, exceto para exibições padrão e personalizadas para as quais você salvou intervalos de datas específicos. O intervalo de datas padrão do sistema para exibições de gerenciamento de campanha é &quot;Ontem&quot;.

Suas configurações de intervalo de datas são salvas em um cookie específico do navegador, de modo que quaisquer alterações no filtro de intervalo de datas são usadas para todos os anunciantes sempre que você entrar usando o mesmo aplicativo do navegador, até alterar o filtro ou excluir o cookie. Cada aplicativo de navegador usado armazena configurações de filtro de intervalo de datas em um cookie diferente.

Quando você salva um intervalo de datas específico para uma exibição padrão ou personalizada, esse intervalo é aplicado sempre que a exibição é aplicada, independentemente do aplicativo do navegador usado.

>[!NOTE]
>
>* Você pode exibir dados dos 13 meses anteriores, mas qualquer exibição personalizada existente pode incluir dados apenas dos 180 dias anteriores.
>* Para exibir dados anteriores, vá para a [[!UICONTROL Reports] exibição](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) e execute um relatório básico.
>* Você também pode salvar um intervalo de datas para uma [exibição padrão ou personalizada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Alterar o filtro de data global nas visualizações de campanha

1. Acima de qualquer tabela de dados em Pesquisar \> Campanhas \> Campanhas, clique no intervalo de datas atual.

1. No campo **[!UICONTROL Date Range]**, especifique o intervalo:

   * Para um intervalo predefinido: selecione na lista de incrementos de tempo comuns, variando de *[!UICONTROL Today]* a *[!UICONTROL Last 180 Days]*. O padrão é *[!UICONTROL Yesterday]*.

   * Para um intervalo específico: Selecione **[!UICONTROL Custom Date Range]** e especifique a data inicial e a data final.

     Insira as datas no formato MM/DD/AAAA ou MM-DD-AAAA ou clique em ![Ícone do calendário](/help/search-social-commerce/assets/calendar.png "Ícone do calendário") ao lado de cada campo para abrir o calendário e selecionar uma data.

1. (Opcional) Comparar dados para o intervalo de datas especificado com dados para um segundo intervalo de datas:

   1. Mova o controle deslizante **[!UICONTROL Comparison]** para a posição &quot;ligado&quot;.

      Ao selecionar essa opção, duas colunas adicionais são adicionadas para cada coluna de dados regular. Por exemplo, em vez de incluir apenas uma coluna para &quot;[!UICONTROL Impressions]&quot;, a tabela inclui colunas para &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; e &quot;[!UICONTROL Impressions Diff]&quot;.  Se exportar os dados, as mesmas colunas serão grafadas como &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; e &quot;[!UICONTROL Impressions Difference]&quot;.

   1. Especifique o segundo intervalo de datas.

   1. Escolha como expressar a diferença entre os dados nos dois intervalos de datas selecionados na coluna &quot;\[_Data field_\] Difference&quot;:

      * *[!UICONTROL Variance]* (padrão): mostra a diferença como um valor numérico.

      * *[!UICONTROL % Change]:* Mostra a diferença como uma porcentagem.

1. Clique em **[!UICONTROL Apply]**.
