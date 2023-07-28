---
title: Filtrar dados por intervalo de datas
description: Saiba como usar o filtro de intervalo de datas global.
exl-id: e67e843a-1a73-4ab1-9ef7-c97afeb999f6
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Filtrar dados por intervalo de datas

O mesmo filtro de intervalo de datas global é aplicado à maioria das visualizações de dados da campanha, em todos os anunciantes, exceto para exibições padrão e personalizadas para as quais você salvou intervalos de datas específicos. O intervalo de datas padrão do sistema para exibições de gerenciamento de campanha é &quot;Ontem&quot;.

Suas configurações de intervalo de datas são salvas em um cookie específico do navegador, de modo que quaisquer alterações no filtro de intervalo de datas são usadas para todos os anunciantes sempre que você fizer logon usando o mesmo aplicativo do navegador, até alterar o filtro ou excluir o cookie. Cada aplicativo de navegador usado armazenará as configurações de filtro de intervalo de datas em um cookie diferente.

Quando você salva um intervalo de datas específico para uma exibição padrão ou personalizada, esse intervalo é aplicado sempre que a exibição é aplicada, independentemente do aplicativo do navegador usado.

>[!NOTE]
>
>* Você pode exibir dados dos 13 meses anteriores, mas qualquer exibição personalizada existente pode incluir dados apenas dos 180 dias anteriores.
>* Para visualizar dados anteriores, acesse o [[!UICONTROL Reports] exibir](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) e executar um relatório básico.
>* Também é possível salvar um intervalo de datas para uma [modo de exibição padrão ou personalizado](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Alterar o filtro de data global nas visualizações de campanha

1. Acima de qualquer tabela de dados em Pesquisar \> Campanhas \> Campanhas, clique no intervalo de datas atual.

1. No **[!UICONTROL Date Range]** especifique o intervalo:

   * Para um intervalo predefinido: selecione na lista de incrementos de tempo comuns, que vão de *[!UICONTROL Today]* para *[!UICONTROL Last 180 Days]*. O padrão é *[!UICONTROL Yesterday]*.

   * Para um intervalo específico: Selecione **[!UICONTROL Custom Date Range]** e especifique a data de início e a data de término.

     Insira as datas no formato MM/DD/AAAA ou MM-DD-AAAA ou clique em ![Ícone de calendário](/help/search-social-commerce/assets/calendar.png "Ícone de calendário") ao lado de cada campo para abrir o calendário e selecionar uma data.

1. (Opcional) Comparar dados para o intervalo de datas especificado com dados para um segundo intervalo de datas:

   1. Mova as **[!UICONTROL Comparison]** controle deslizante para *[!UICONTROL On]*.

      Ao selecionar essa opção, duas colunas adicionais são adicionadas para cada coluna de dados regular. Por exemplo, em vez de incluir apenas uma coluna para &quot;[!UICONTROL Impressions],&quot; a tabela inclui colunas para &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot; e &quot;[!UICONTROL Impressions Diff].&quot;  Se exportar os dados, as mesmas colunas serão grafadas como &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; e &quot;[!UICONTROL Impressions Difference].&quot;

   1. Especifique o segundo intervalo de datas.

   1. Escolha como expressar a diferença entre os dados nos dois intervalos de datas selecionados no campo &quot;\[_Campo de dados_\] coluna &quot;Diferença&quot;:

      * *[!UICONTROL Variance]* (o padrão): mostra a diferença como um valor numérico.

      * *[!UICONTROL % Change]:*  Mostra a diferença como uma porcentagem.

1. Clique em **[!UICONTROL Apply]**.
