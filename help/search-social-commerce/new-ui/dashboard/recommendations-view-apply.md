---
title: Suporte a recomendações e insights do editor
description: Saiba mais sobre o suporte para exibir e gerenciar recomendações e insights do editor.
feature: Search Recommendations
source-git-commit: 1328e52509e4111bc0e58412ebf3c3b2de0cb291
workflow-type: tm+mt
source-wordcount: '1604'
ht-degree: 0%

---

# Suporte a recomendações e insights do editor

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas*

As recomendações e os insights do [!DNL Google Ads] e do [!DNL Microsoft Advertising] são sugestões da rede de publicidade para ajudar a melhorar o desempenho e a eficiência das suas campanhas:

* Cada recomendação do [!DNL Google Ads] fornece sugestões personalizadas sobre diferentes aspectos de desempenho de uma campanha, desde adicionar um ativo até aumentar o orçamento, com base no histórico de desempenho da conta, nas configurações da campanha e nas tendências do [!DNL Google Ads].

* Cada recomendação e insight de desempenho do [!DNL Microsoft Advertising] sugere alterações para otimizar o desempenho da campanha com base em algoritmos de aprendizado de máquina e práticas recomendadas.

## A visualização [!UICONTROL Recommendations]

Em (nova interface) [!UICONTROL Dashboard] > [!UICONTROL Recommendations] e (interface herdada) [!UICONTROL Insights & Reports] > [!UICONTROL Recommendations & Publisher Insights], você pode:

* Ver as principais características de todas as recomendações compatíveis da que não foram implementadas em uma conta. As informações para cada entrada incluem o tipo de recomendação, a recomendação [!DNL Adobe], as métricas afetadas, a entidade afetada e um link para mais detalhes. Os aumentos previstos para as métricas são destacados em verde.

  ![Interface do usuário do Recommendations](/help/search-social-commerce/assets/recommendations-ui.png "Interface do usuário do Recommendations")

  Os dados são disponibilizados em tempo real quando você abre a visualização. Para atualizar os dados, clique em ![Atualizar](/help/search-social-commerce/assets/refresh.png "Atualizar") na parte inferior esquerda da página.

* Para contas do [!DNL Microsoft Advertising], veja as principais características de cada insight de desempenho gerado nos últimos 30 dias para uma conta do [!DNL Microsoft Advertising]. Os insights fornecem informações semelhantes às recomendações, mas em um formato diferente. Cada insight inclui a data, uma descrição do problema, a entidade afetada, a causa raiz (que pode incluir links para mais detalhes) e a ação sugerida com um link para abrir o editor [!DNL Microsoft Advertising], a partir do qual você pode agir no insight específico.

* Exibir detalhes sobre uma recomendação e aplicá-la diretamente ou descartá-la.

* Exibir um log de cada recomendação que foi aplicada para a conta.

## Tipos de recomendação com suporte para [!DNL Google Ads]

| Categoria de recomendação | Tipo de recomendação | Descrição |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] (agora chamado de &quot;[!DNL Ads and assets]&quot; em [!DNL Google Ads]) | [!UICONTROL Call extension] | Adicionar extensões de chamada a uma campanha |
| | [!UICONTROL Callout extension] | Adicionar extensões de chamada a uma campanha |
|  | [!UICONTROL Improve demand gen ad strength] | Sugestões para melhorar a intensidade do anúncio para um anúncio de geração de demanda |
| | [!UICONTROL Optimize ad rotation] | Usar rotações de anúncios otimizadas |
| | [!UICONTROL Responsive search ad] | Adicione um novo anúncio de pesquisa responsivo |
| | [!UICONTROL Responsive search ad asset] | Adicionar ativos responsivos de publicidade de pesquisa a uma publicidade |
| | [!UICONTROL Responsive search improve ad strength] | Sugestões para melhorar a intensidade do anúncio para uma pesquisa responsiva de anúncio |
| | [!UICONTROL Sitelink extension] | Adicionar extensões do sitelink a uma campanha |
| | [!UICONTROL Text ad] | Adicionar um novo anúncio de texto |
| [!UICONTROL Automated campaigns] | [!UICONTROL DSA to performance max migration] | Migrar anúncios de pesquisa dinâmica para campanhas de desempenho máximo |
| | [!UICONTROL Dynamic image extension opt in] | Habilite extensões de imagem dinâmicas para a conta, o que permite que o aprendizado de máquina do [!DNL Google Ads] anexe automaticamente as imagens mais relevantes da página de aterrissagem do seu anúncio ao seu anúncio |
| | [!UICONTROL Improve performance max ad strength] | Melhore a força do grupo de ativos de uma campanha de desempenho máximo para uma classificação &quot;Excelente&quot; |
| | [!UICONTROL Performance max final URL opt in] | Ativar a expansão final de URL para suas campanhas de desempenho máximo |
| | [!UICONTROL Performance max opt in] | Optar por campanhas de desempenho máximo |
| | [!UICONTROL Upgrade local campaign to performance max] | Atualizar uma campanha local herdada para uma campanha de desempenho máximo |
| | [!UICONTROL Upgrade smart shopping campaign to performance max] | Atualize uma campanha de compras inteligentes herdada para uma campanha de desempenho máximo |
| [!UICONTROL Bidding and budget] | [!UICONTROL Campaign budget] | Orçamento recomendado para uma campanha atualmente limitada pelo orçamento |
| | [!UICONTROL Forecasting campaign budget] | Orçamento recomendado para uma campanha que deve se tornar limitada pelo orçamento no futuro |
| | [!UICONTROL Forecasting set Target CPA] | Definir um CPA de destino para campanhas sem um antes de um evento sazonal previsto para aumentar o tráfego |
| | [!UICONTROL Forecasting set Target ROAS] | Aumente o orçamento antes de um evento sazonal previsto para aumentar o tráfego e altere a estratégia de lances de [!UICONTROL Maximize Conversion Value] para [!UICONTROL Target ROAS] |
| | [!UICONTROL Marginal ROI campaign budget] | Ajustar o orçamento da campanha para aumentar o ROI |
| | [!UICONTROL Maximize clicks opt in] | Alteração na estratégia de lances [!UICONTROL Maximize Clicks] |
| | [!UICONTROL Maximize conversion value opt in] | Alteração na estratégia de lances Maximizar Valor de Conversão |
| | [!UICONTROL Maximize conversions opt in] | Alteração na estratégia de lances [!UICONTROL Maximize Conversions] |
| | [!UICONTROL Move unused budget] | Mover orçamento não utilizado para um orçamento restrito |
| | [!UICONTROL Raise Target CPA bid too low] | Aumente o [!UICONTROL Target CPA] de acordo com o valor recomendado quando ele for muito baixo e houver poucas ou nenhuma conversão |
| | [!UICONTROL Set Target CPA] | Definir um CPA de destino para campanhas sem um |
| | [!UICONTROL Set Target ROAS] | Definir um ROAS de destino para campanhas sem um |
| | [!UICONTROL Target CPA opt in] | Alteração na estratégia de lances [!UICONTROL Target CPA] |
| | [!UICONTROL Target CPA raising] | Gerar o [!UICONTROL Target CPA] com base em [!DNL Google Ads] previsões, que são calculadas a partir de conversões passadas |
| | [!UICONTROL Target ROAS lowering] | Reduza o [!UICONTROL Target ROAS] com base em [!DNL Google Ads] previsões, que são calculadas a partir de conversões anteriores |
| | [!UICONTROL Target ROAS opt in] | Alteração na estratégia de lances [!UICONTROL Target ROAS] |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Display expansion opt in] | Expandir alcance atualizando uma campanha para usar a expansão de exibição |
| | [!UICONTROL Keyword] | Adicionar novas palavras-chave |
|  | [!UICONTROL Refresh customer match list] | Atualize suas listas de correspondência do cliente para mostrar anúncios personalizados para clientes recentes |
| | [!UICONTROL Search partners opt in] | Expandir alcance com [!DNL Google] parceiros de pesquisa |
| | [!UICONTROL Use broad match keyword] | Use uma ampla correspondência para campanhas baseadas em conversão com ofertas totalmente automatizadas baseadas em conversão |

## Tipos de recomendação com suporte para [!DNL Microsoft Advertising]

| Categoria de recomendação | Tipo de recomendação | Descrição |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] | [!UICONTROL Responsive search ad] | Adicione um novo anúncio de pesquisa responsivo |
| [!UICONTROL Bidding and budgets] | [!UICONTROL Campaign budget] | Corrigir campanhas limitadas por orçamento |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Keyword] | Adicionar novas palavras-chave de todas as fontes |

## Exibir recomendações e insights do editor {#recommendations-view}

>[!NOTE]
>
>Embora as recomendações de rede de anúncios e os insights de desempenho ajudem a melhorar o desempenho da campanha, alguns podem não se alinhar às suas metas mais amplas. Como resultado, é melhor consultar a equipe de conta da Adobe antes de implementar qualquer recomendação ou insight.

### (Nova interface do usuário) Exibir as recomendações do editor

1. No menu principal, clique em **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. Na barra de ferramentas, selecione a rede de publicidade e a conta.

   Para contas do [!DNL Microsoft Advertising], a guia [!UICONTROL Recommendations] é aberta por padrão.

1. Na coluna [!UICONTROL Actions] da linha, clique em **[!UICONTROL View]**. Se a recomendação tiver sub-recomendações, clique em **[!UICONTROL View]** ao lado da sub-recomendação.

   Opcionalmente, você pode [aplicar ou ignorar](#recommendations-apply-dismiss) as recomendações da rede de anúncios.

### (Interface herdada) Exibir as recomendações do editor

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. No canto superior direito, selecione a rede de anúncios e a conta.

   Para contas do [!DNL Microsoft Advertising], os [!UICONTROL Recommendations] da conta são listados por padrão.

1. Na coluna [!UICONTROL Actions] da linha, clique em **[!UICONTROL View]**. Se a recomendação tiver sub-recomendações, clique em **[!UICONTROL View]** ao lado da sub-recomendação.

   Opcionalmente, você pode [aplicar ou ignorar](#recommendations-apply-dismiss) as recomendações da rede de anúncios.

### (Nova interface do usuário) Exibir seus insights de desempenho do [!DNL Microsoft Advertising]

1. No menu principal, clique em **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. Na barra de ferramentas, selecione a rede de publicidade e a conta.

1. Clique na guia **[!UICONTROL Insights]** acima da tabela de dados.

1. (Opcional) Quando a coluna [!UICONTROL Actions] da linha inclui uma ou mais ações:

   * Para abrir o editor [!DNL Microsoft Advertising], no qual você pode atuar em uma insight individual, clique em **[!UICONTROL Click here]** ao lado da ação.

   * (Insights com várias ações) Para exibir o texto completo de todas as ações da insight, clique em **[!UICONTROL Read More]**. Para abrir o editor [!DNL Microsoft Advertising], do qual você pode agir em uma insight individual, clique em **[!UICONTROL Click here]** ao lado da ação individual.

   Se você não estiver conectado ao editor [!DNL Microsoft Advertising], será direcionado primeiro à tela de logon.

### (Interface herdada) Visualize seus insights de desempenho do [!DNL Microsoft Advertising]

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. No canto superior direito, selecione a rede de anúncios e a conta.

1. Clique em **[!UICONTROL Insights]** acima da tabela de dados.

1. Quando a coluna [!UICONTROL Actions] da linha incluir uma ação, você poderá, opcionalmente, clicar em **[!UICONTROL Click here]** para abrir o editor [!DNL Microsoft Advertising], a partir do qual poderá atuar na insight.

   Se você não estiver conectado ao editor [!DNL Microsoft Advertising], será direcionado primeiro à tela de logon.

## Aplicar ou ignorar uma recomendação do editor {#recommendations-apply-dismiss}

Aplique uma recomendação quando ela estiver alinhada às suas metas comerciais e ignore uma recomendação quando não estiver.

>[!NOTE]
>
>Embora as recomendações ajudem a melhorar o desempenho da campanha, algumas podem não se alinhar às suas metas mais amplas. Como resultado, é melhor consultar a equipe de conta da Adobe antes de implementar qualquer recomendação.

### (Nova interface do usuário) Aplicar ou ignorar uma recomendação do editor

1. No menu principal, clique em **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. Na barra de ferramentas, selecione a rede de publicidade e a conta.

   Para contas do [!DNL Microsoft Advertising], a guia [!UICONTROL Recommendations] é aberta por padrão.

1. (Opcional) Filtre as recomendações por categoria e tipo.

1. Na coluna [!UICONTROL Actions] da linha de recomendação ou insight, clique em **[!UICONTROL View]**.

1. (Recomendações com recomendações secundárias) Clique em **[!UICONTROL View]** ao lado da recomendação secundária.

1. (Opcional) Siga um destes procedimentos:

   * Para aplicar uma recomendação, clique em **[!UICONTROL Apply]**.

     A aplicação de uma recomendação pode levar de milissegundos a alguns segundos, dependendo do tamanho da recomendação.

   * Para ignorar uma recomendação, clique em **[!UICONTROL Dismiss]**.

### (Interface herdada) Aplicar ou descartar uma recomendação do editor

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. No canto superior direito, selecione a rede de anúncios e a conta.

   Para contas do [!DNL Microsoft Advertising], os [!UICONTROL Recommendations] da conta são listados por padrão.

1. (Opcional) Filtre as recomendações por categoria e tipo.

1. Na coluna [!UICONTROL Actions] da linha de recomendação ou insight, clique em **[!UICONTROL View]**.

1. (Recomendações com recomendações secundárias) Clique em **[!UICONTROL View]** ao lado da recomendação secundária.

1. (Opcional) Siga um destes procedimentos:

   * Para aplicar uma recomendação, clique em **[!UICONTROL Apply]**.

     A aplicação de uma recomendação pode levar de milissegundos a alguns segundos, dependendo do tamanho da recomendação.

   * Para ignorar uma recomendação, clique em **[!UICONTROL Dismiss]**.

## Exibir um log das recomendações do editor para uma conta {#recommendations-log}

Você pode exibir um log de cada recomendação que foi aplicada. As informações incluem a categoria da recomendação, o tipo de recomendação, as entidades afetadas, o usuário que aplicou a recomendação e o carimbo de data e hora.

Recomendações descartadas não estão disponíveis na rede de anúncios.

### (Nova interface do usuário) Exibir um log das recomendações do editor para uma conta

1. No menu principal, clique em **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. Na barra de ferramentas, selecione a rede de publicidade e a conta.

1. Na parte superior direita, clique em ![Logs de recomendação](/help/search-social-commerce/assets/recommendations-log-view-new.png "Logs de recomendação").

### (Interface herdada) Exibir um log das recomendações do editor para uma conta

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. No canto superior direito, selecione a rede de anúncios e a conta.

1. Na parte superior direita, clique em ![Logs de recomendação](/help/search-social-commerce/assets/recommendations-log-view.png "Logs de recomendação").

## Práticas recomendadas para usar as recomendações do editor com portfólios

<!--
 Add info for MS once we have it ..." 

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts*
 
-->

## [!DNL Google Ads] recomendações

| Tipo de recomendação | Descrição | Aplicar recomendações automaticamente com portfólios de pesquisa, social e Commerce? | Comentários |
|--- |--- |--- |--- |
| [!UICONTROL Ads] e extensões (agora chamadas de &quot;Anúncios e ativos&quot; em [!DNL Google Ads]) | Recomendações para adicionar/editar anúncios e ativos | Pode ser aplicado automaticamente, mas os anunciantes devem revisar as recomendações manualmente. | Revisar recomendações é necessário para garantir que anúncios de pesquisa responsivos estejam alinhados com os requisitos do anunciante. |
| [!UICONTROL Automated campaigns] | Recomendações para campanhas automatizadas (campanhas locais e inteligentes) | Não disponível em Search, Social e Commerce. | — |
| [!UICONTROL Bidding and budget] | Oferecer, orçar e direcionar recomendações para melhorar o desempenho | Não aplicar automaticamente para campanhas em portfólios otimizados. | As recomendações atuais podem ser unidimensionais para suas finalidades. Por exemplo, [!DNL Google Ads] recomenda um aumento no CPA de destino, sem preocupação com o orçamento, quando os cliques diminuem para uma campanha. |
| [!UICONTROL Keywords and targeting] | Limpeza de palavra-chave e recomendações de público | Pode ser aplicado automaticamente, mas use a aplicação automática seletivamente. | Use a limpeza de palavras-chave e a remoção de redundâncias em campanhas, mas evite mais automação (como a criação automática de anúncios de pesquisa dinâmicos ou públicos de expansão automática). |
| [!UICONTROL Measurement] | Recomendações para rastreamento e certificação de conversão | Não disponível em Search, Social e Commerce. | Essas recomendações podem afetar o desempenho. Consulte sua equipe de conta da Adobe para discutir os prós e contras de qualquer recomendação antes de aplicá-la. |
| [!UICONTROL Repairs] | Recomendações diversas para melhorar problemas de conta | Não disponível em Search, Social e Commerce. | Revisar periodicamente as recomendações de reparo manualmente em [!DNL Google Ads]. Esse tipo de recomendação é uma boa maneira de identificar anúncios não aprovados, problemas de feed, problemas de rastreamento e assim por diante. |
| [!UICONTROL Other] | Recomendação para usar o aplicativo móvel [!DNL Google Ads] | Não disponível em Search, Social e Commerce. | — |
