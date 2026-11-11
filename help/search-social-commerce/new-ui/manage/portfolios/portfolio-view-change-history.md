---
title: (Nova interface do usuário) Visualização do histórico de alterações de um portfólio e do histórico de alterações de ofertas
description: Saiba como visualizar alterações de portfólio e histórico de alterações de oferta, alterar intervalos de datas, filtrar alterações de portfólio e gerar, baixar e excluir relatórios de histórico no Adobe Advertising Search, Social e Commerce.
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# (Nova interface do usuário) Visualização do histórico de alterações de um portfólio e do histórico de alterações de ofertas

*recurso do Beta*

Você pode exibir um log de alterações feitas no portfólio durante qualquer intervalo de datas. As ações registradas incluem a criação do portfólio, todas as alterações nas configurações do portfólio, todas as campanhas atribuídas ou não atribuídas ao portfólio, todas as restrições aplicadas ou removidas das unidades de oferta no portfólio, todas as restrições nas unidades de oferta no portfólio que expiraram e outras ações que afetam o portfólio.

A caixa de diálogo [!UICONTROL Change History] inclui uma guia [!UICONTROL Portfolio Change History] para alterações de portfólio e uma guia [!UICONTROL Portfolio Bid Change History] para histórico de ofertas. Por padrão, ambas as guias mostram os últimos 180 dias, terminando ontem.

Você pode filtrar alterações de portfólio por categoria e alterar o intervalo de datas para qualquer guia. Você também pode baixar os dados em um arquivo de planilha.

## Exibir o histórico de alterações de um portfólio {#portfolio-change-history}

As informações para cada alteração incluem [!UICONTROL Change Date], [!UICONTROL Changed By], [!UICONTROL Change Type] e [!UICONTROL Description]. As alterações são listadas da mais recente para a mais antiga.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenha o cursor sobre a linha do portfólio e clique em **[!UICONTROL ...]>[!UICONTROL Change History]**.

1. Na caixa de diálogo [!UICONTROL Change History], exiba a guia **[!UICONTROL Portfolio Change History]**.

1. (Opcional) Altere as informações exibidas:

   * Clique em ![Calendário](/help/search-social-commerce/assets/calendar-new.png "Calendário") para alterar o intervalo de datas do relatório.

   * Clique em ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro") para filtrar os dados por categoria: [!UICONTROL All], [!UICONTROL Objective], [!UICONTROL Campaign], [!UICONTROL Target], [!UICONTROL Constraints], [!UICONTROL Optimization Levers] ou [!UICONTROL Others].

## Exibir o histórico de alterações de oferta de um portfólio {#portfolio-bid-change-history}

1. [Abra o histórico de alterações do portfólio](#portfolio-change-history).

1. Clique na guia **[!UICONTROL Portfolio Bid Change History]**.

1. (Opcional) Clique em ![Calendário](/help/search-social-commerce/assets/calendar-new.png "Calendário") para alterar o intervalo de datas.

1. (Opcional) Clique no cabeçalho da coluna de data para classificar a lista por data em ordem crescente ou decrescente.

Para exibir o histórico de uma unidade de oferta individual, [abra os detalhes da unidade de oferta nos detalhes de desempenho do portfólio](portfolio-details.md#bid-unit-history). Você também pode [abrir o histórico de unidade de oferta da [!UICONTROL Keywords] exibição](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history) quando a coluna [!UICONTROL Bid Unit ID] estiver disponível.

## Gerenciar relatórios para históricos de alterações do portfólio

Você pode baixar informações adicionais sobre o histórico de alterações de um portfólio para um arquivo no formato de pasta de trabalho [!DNL Microsoft Excel] (arquivo XLSX). O relatório inclui a ID de alteração numérica, os valores antigos e novos, o tipo de alteração (como &quot;adicionado&quot; ou &quot;modificado&quot;), o tipo de ação (como &quot;Orçamento&quot; ou &quot;Nome da Portfolio&quot;) e o subtipo, quando aplicável, a hora e o nome do usuário.

Você também pode gerar, baixar e excluir relatórios na guia [!UICONTROL Portfolio Bid Change History]. As configurações do relatório são intituladas [!UICONTROL Portfolio History] para alterações de portfólio e [!UICONTROL Portfolio Bid History] para histórico de lances.

### Gerar um relatório com as linhas de dados filtradas

1. [Abra o histórico de alterações do portfólio](#portfolio-change-history) e clique na guia cujos dados você deseja baixar.

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Nas configurações de [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], aceite o nome de relatório padrão ou insira um nome de relatório exclusivo e clique em **[!UICONTROL Generate]**.

   Por padrão, o nome do relatório inclui o tipo de histórico e a data e hora no formato `YYYYMMDD_HHmm`, como &quot;portfolioChangeHistory_20260402_1326&quot;. Se o nome já existir, um sufixo numérico será adicionado.

   O arquivo foi adicionado à lista [!UICONTROL Recently Generated].

1. (Opcional) Para baixar o arquivo após sua conclusão, clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Baixar um relatório concluído

1. [Abra o histórico de alterações do portfólio](#portfolio-change-history) e clique na guia da qual você gerou o relatório.

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Na lista [!UICONTROL Recently Generated] nas configurações [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], clique em ![Baixar](/help/search-social-commerce/assets/download.png "Baixar") ao lado do nome do arquivo.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

### Excluir um relatório concluído

1. [Abra o histórico de alterações do portfólio](#portfolio-change-history) e clique na guia da qual você gerou o relatório.

1. Na parte superior direita, clique em ![Baixar relatório](/help/search-social-commerce/assets/download.png "Baixar relatório").

1. Na lista [!UICONTROL Recently Generated] nas configurações [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir") ao lado do nome do arquivo.

>[!MORELIKETHIS]
>
>* [Criar um portfólio](portfolio-create.md)
>* [(Nova interface do usuário) Editar um portfólio](portfolio-edit.md)
>* [(Nova interface do usuário) Exibir detalhes de desempenho do portfólio](portfolio-details.md)
>* [(Nova interface do usuário) Baixar dados na [!UICONTROL Portfolios] exibição](portfolio-view-report.md)
>* [Sobre portfólios](portfolio-about.md)
