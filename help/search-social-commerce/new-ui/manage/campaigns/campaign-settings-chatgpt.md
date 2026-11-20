---
title: Configurações de campanha de [!DNL ChatGPT Ads]
description: Referencie as configurações de [!DNL ChatGPT Ads] campanhas.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6aa2e40903fd8652c0ac744e3cd4f68c5e74fd48
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%
---
# Configurações de campanha de [!DNL ChatGPT Ads]

*Anúncios em [!DNL ChatGPT] são um recurso piloto de[!DNL OpenAI]*

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign Type]:** Onde colocar anúncios: a única opção é *[!UICONTROL Standard]* para exibir anúncios em [!DNL ChatGPT].

## Guia [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Um nome de campanha exclusivo dentro da conta.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

**[!UICONTROL Objective]:** O objetivo da campanha: *[!UICONTROL Reach]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Conversions]*. O objetivo determina as [opções de lances de grupo de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-chatgpt.md) disponíveis: a licitação CPC de destino é compatível com cliques e a licitação CPA de destino é compatível com conversões. O CPC de destino e a oferta de CPA de destino não estão disponíveis para campanhas de alcance.

**[!UICONTROL Billing event]:** (Novas campanhas com o objetivo [!UICONTROL Conversions]) Se você é cobrado com base em cliques ou impressões. O padrão é cliques. O objetivo determina para que a campanha é otimizada; o evento de faturamento determina como você é cobrado. Você não pode alterar o evento de faturamento depois de salvar a campanha.

**[!UICONTROL Location Targets]:** Localizações geográficas de usuários com suporte para incluir como destinos. Por padrão, todos os locais compatíveis são direcionados. É possível restringir os destinos para incluir (mas não excluir) usuários em qualquer combinação de locais.

* Para direcionar todos os locais, não selecione nenhum local.

* Para incluir um local e seus locais secundários, clique no círculo adjacente.

* Para expandir um local em seus subcomponentes (como regiões, territórios ou cidades), clique no nome do local.

* Para pesquisar um local, insira ou cole pelo menos os três primeiros caracteres do local no campo de entrada.

**[!UICONTROL Budget Type]:** O tipo de orçamento da campanha: *Orçamento diário* ou *Tempo de vida*. Você não pode alterar o tipo de orçamento depois de salvar a campanha.

**[!UICONTROL Budget]:** O orçamento para o tipo de campanha especificado.

**[!UICONTROL Conversion events]:** (Opcional) Qualquer evento de conversão existente configurado em [!DNL ChatGPT Ads] para ser associado à campanha. **Observação:** os dados de desempenho para conversões rastreadas por [!DNL OpenAI] não estão disponíveis em Pesquisa, Social e Commerce. Monitore suas conversões rastreadas por [!DNL OpenAI] em [!DNL ChatGPT Ads Manager].

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar campanhas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
