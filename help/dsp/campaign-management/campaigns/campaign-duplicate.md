---
title: Duplicar uma campanha
description: Saiba como duplicar uma campanha.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Duplicar uma campanha

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique uma campanha para criar uma nova campanha com configurações semelhantes. Você pode:

* Duplique a campanha para o anunciante original ou para uma campanha diferente

* Opcionalmente, duplicar os pacotes e posicionamentos originais

* Modificar as datas de voo da nova campanha

Consulte &quot;[O que não está duplicado](#campaign-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Ao lado do nome da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de campanha:

   1. Insira o novo nome da campanha e a data de término da veiculação.

   1. (Opcional) Altere as configurações padrão.

      Por padrão, a nova campanha é atribuída ao anunciante original, tem uma programação de voo que começa no dia atual e inclui os pacotes e disposições originais.

1. Clique em **[!UICONTROL Submit]**.

## O que não está duplicado {#campaign-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações de experimento
* Orçamentos mínimos no nível de posicionamento
* (Se você alterar as datas de veiculação) Programação de anúncios personalizada
* (Se você não anexar anúncios) Peso e agendamento personalizados de anúncios
* Posicionamentos padrão para ofertas programáticas garantidas (PG) e posicionamentos para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Destinos geográficos
   * Pixels de evento
   * Anúncios
   * Segmentos no nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] (que substituem os segmentos no nível do anunciante)

## Práticas recomendadas para configurar a nova campanha

>[!TIP]
>
>* Use bulksheets para [fazer alterações em vários componentes da campanha de uma só vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use folhas de marcas de publicidade para [carregar vários anúncios de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause a nova campanha até estar pronto para ativá-la.

* Considere o seguinte e edite a nova campanha conforme necessário:

   * A conta tem financiamento suficiente para acomodar o novo orçamento de campanha?

   * A nova campanha precisa de um orçamento diferente do orçamento da campanha anterior?

   * Os orçamentos mínimos são necessários para qualquer um dos posicionamentos?

   * Faça upload de criações, incluindo qualquer ponderação e agendamento de anúncio personalizado necessário, e anexe-as aos posicionamentos.

   * Anexe pixels do evento, conforme necessário, aos posicionamentos e anúncios.

   * Inclua destinos geográficos e segmentos de nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] conforme necessário para posicionamentos.

   * Para ofertas programáticas garantidas, use novas IDs de negócios e crie inserções padrão.

   * Crie novos posicionamentos para [!UICONTROL Simple Ad Serving] ofertas, conforme necessário.

* Para campanhas de desempenho (ou seja, campanhas com pacotes que usam metas de otimização personalizadas), use a [[!UICONTROL Linked Package for Optimization Learnings Carryover] configuração](/help/dsp/campaign-management/packages/package-settings.md) de cada pacote para usar os dados do histórico da campanha anterior como entrada para otimizar o pacote.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de campanhas](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)
>* [Exibir o Log de Alterações de uma Campanha](campaign-change-log.md)
>* [Configurações da campanha](campaign-settings.md)
