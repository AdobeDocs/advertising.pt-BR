---
title: (Nova interface) Sobre portfólios
description: Saiba mais sobre portfólios.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# (Nova interface) Sobre portfólios

*recurso do Beta*

Você pode gerenciar suas campanhas publicitárias coletivamente usando portfólios (semelhantes a portfólios de investimento). Um portfólio é um conjunto de campanhas de anúncios ou conjuntos de anúncios, incluindo suas palavras-chave e anúncios associados, que são otimizados para um único objetivo comercial. Um objetivo pode incluir várias conversões ponderadas e um único orçamento ou meta de desempenho (como um orçamento mensal ou uma meta de ROI). Como campanhas/conjuntos de anúncios individuais, palavras-chave e anúncios podem ter desempenho diferente entre si (por exemplo, eles podem gastar quantidades diferentes ou atingir ROIs diferentes), o recurso de otimização usa modelos orientados por IA para orientar todo o portfólio a fim de alcançar coletivamente o público-alvo. Todas as campanhas em um portfólio usam a mesma moeda.

Algumas funções de usuário podem criar e configurar portfólios. Dependendo do tipo de portfólio, as configurações do portfólio podem incluir o objetivo do portfólio, as campanhas atribuídas, a estratégia de gastos, as restrições de lances no nível do portfólio e os parâmetros de modelagem e otimização. Quando estiver pronto para Search, Social e Commerce para iniciar a otimização de um portfólio, altere o status para &quot;otimizado&quot;.

Opcionalmente, é possível agrupar portfólios em grupos de portfólios para exibir dados de cliques e receitas compostos para todo o grupo. Crie grupos de portfólios a partir da [interface herdada](/help/search-social-commerce/getting-started/ui-switch.md).

Dependendo da sua função, você poderá gerar simulações de desempenho, que usam modelagem preditiva para identificar o seu ponto de gasto ideal e relatórios detalhados de precisão de previsão.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Suporte de otimização por estratégia de oferta {#optimization-by-bid-strategy}

As campanhas estão qualificadas para otimização com base na campanha ou estratégia de oferta de grupo de anúncios.

>[!NOTE]
>
>As opções &quot;lance inteligente&quot; e &quot;lance automatizado&quot; geralmente são usadas alternadamente, mas não são a mesma coisa. As ofertas inteligentes se referem somente a [!DNL Google Ads] e [!DNL Microsoft Advertising] estratégias de lances automatizadas que usam lances no período do leilão, o que significa que a rede de anúncios otimiza para conversões ou valores de conversão no momento de cada leilão.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Estratégia de oferta | Lance inteligente? | Lance De Nível De Grupo De Produto/Palavra-Chave? | Nível de suporte | Tipo de Objetivo | Unidade de lance | O que o Adobe define? | O que a rede de publicidade define? |
|---|---|---|---|---|---|---|---|
| CPC manual (opção somente [!DNL Google Ads]) | — | Sim | Criar, Editar, Otimizar | Objetivo de uma ou várias propriedades com qualquer valor de peso | Palavra-chave + Tipo de correspondência + Campanha | Lance de palavra-chave, orçamento de campanha, valores de ajuste de oferta | n/d |
| ECPC (CPC avançado) | Sim | Sim | Criar, Editar, Otimizar | Objetivo de uma ou várias propriedades com qualquer valor de peso | Palavra-chave + Tipo de correspondência + Campanha | Lance de palavra-chave, orçamento de campanha | Ajusta ofertas em tempo real |
| Maximizar cliques[^1] | — | — | Criar, Editar, Otimizar | Nenhum; otimiza apenas para cliques | Campaign | Orçamento da campanha | Ajusta o lance em tempo real para maximizar os cliques dentro do orçamento |
| Maximizar conversões<br>(com ou sem TCPA) | Sim | — | Criar, Editar, Otimizar | Objetivo de propriedade única usando um peso de 1 | Campanha ou grupo de publicidade ([!DNL Google Ads])<br>Somente campanha ([!DNL Microsoft Advertising]) | Orçamento da campanha, CPA do Target quando definido<br>TCPA pode ser uma estratégia de oferta independente em [!DNL Microsoft Advertising]) | Ajusta o lance em tempo real para maximizar pedidos/leads dentro do orçamento, atendendo a uma meta de CPA quando o público-alvo é definido |
| Maximizar Valor de Conversão<br>(com ou sem TROAS) | Sim | — | Criar, Editar, Otimizar | Objetivo multipropriedade com qualquer valor de ponderação, ou objetivo de propriedade única com um valor de ponderação maior que 1 (para representar um valor monetário) | Campanha ou grupo de publicidade ([!DNL Google Ads])<br>Somente campanha ([!DNL Microsoft Advertising]) | Orçamento da campanha, ROAS do Target quando definido<br>O TROAS pode ser uma estratégia de oferta independente em [!DNL Microsoft Advertising]) | Ajusta ofertas em tempo real para maximizar a receita/lucro dentro do orçamento, atendendo a uma meta do ROAS quando a meta é definida |
| Compartilhamento de impressão do Target | — | — | Criar, Editar | n/d | n/d | n/d - não pode ser atribuído a um portfólio | Ajusta ofertas em tempo real para atender a uma meta de compartilhamento de impressão |

[^1]: a configuração da estratégia de oferta [!UICONTROL Maximize Clicks] na rede de anúncios não é a mesma que o objetivo de Pesquisa, Social e Commerce [!UICONTROL Maximize Clicks]. Se a estratégia de oferta for [!UICONTROL Maximize Clicks], você deverá atribuí-la somente a um portfólio com otimização no nível da campanha ou do grupo de anúncios, não a um portfólio com otimização no nível da palavra-chave.

## Status do Portfolio {#portfolio-status}

Um portfólio pode ter os seguintes status:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## A visualização [!UICONTROL Portfolios]

A exibição [!UICONTROL Portfolios] lista seus portfólios existentes, com dados de desempenho personalizáveis. Você pode [personalizar as colunas na exibição](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) e filtrar dados para incluir portfólios específicos [da barra de ferramentas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou do [cabeçalho da coluna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Ações disponíveis

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Criar um portfólio](portfolio-create.md)

* [Duplicação de um portfólio](portfolio-duplicate.md)

* [Editar configurações do portfólio](portfolio-edit.md)

* [Editar configurações de portfólio em massa usando arquivos de bulksheet](portfolio-bulksheets.md)

* [Exibir detalhes de desempenho do portfólio](portfolio-details.md)

* [Baixar dados no modo de exibição [!UICONTROL Portfolios]](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Criar um portfólio](portfolio-create.md)
>* [Duplicar um portfólio](portfolio-duplicate.md)
>* [Editar um portfólio](portfolio-edit.md)
>* [Gerenciar relatórios de exibição de dados da [!UICONTROL Portfolios] exibição](portfolio-view-report.md)
