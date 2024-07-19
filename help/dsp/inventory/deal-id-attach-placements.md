---
title: Especificar disposições e anúncios para um acordo privado
description: Saiba como usar uma negociação privada com posicionamentos e anúncios adicionais.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Especificar disposições e anúncios para um acordo privado

Para ofertas não garantidas, você pode especificar a oferta como um destino de inventário para novos posicionamentos na exibição [!UICONTROL Placements].

Para ofertas programáticas garantidas (PG), você pode criar inserções com anúncios especificados da exibição [!UICONTROL Deals].

Você também pode [anexar anúncios a inserções](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associadas a ofertas PG e não garantidas a qualquer momento.

## Especificar uma Negociação Não Garantida como um Destino de Inventário para uma Colocação

* [Criar um posicionamento a partir da [!UICONTROL Placements] exibição](/help/dsp/campaign-management/placements/placement-create.md). Nas configurações de [!UICONTROL Inventory Targeting], selecione a oferta privada.

## Anexar inserções e anúncios a um contrato de PG

1. No menu principal, clique em **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Na linha de negócios, clique em **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Nas configurações de [!UICONTROL Ad & Campaign Selection], selecione os anúncios a serem usados para o posicionamento:

       1. Selecione o anunciante, a campanha e o tipo de anúncio. Opcionalmente, selecione um status de anúncio pelo qual filtrar os anúncios.
       
       1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio a ser usado para a negociação.
       
       1. Clique em **[!UICONTROL Apply]**.
   
   1. Na tela de configurações de posicionamento:

      1. Insira o nome da disposição.

      1. (Opcional) Edite as [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição da oferta padrão, que é preenchida automaticamente com o valor CPM da oferta; a alteração do intervalo de datas; ou a anexação de mais anúncios.

      A negociação é direcionada automaticamente na seção Metas de Inventário. Todas as outras opções de direcionamento são inaplicáveis.

      1. Clique em **[!UICONTROL Create placement]**.

O posicionamento começa a ser executado depois que o editor ativa a ID de contrato PG.

>[!NOTE]
>
> Você não precisa enviar a tag de negócios ao editor para verificação.

>[!MORELIKETHIS]
>
>* [Sobre Inventário Privado](private-inventory-about.md)
>* [Listar os Posicionamentos e Anúncios de um Contrato Privado](/help/dsp/inventory/private-deal-view-placements.md)
>* [Criar manualmente os detalhes da ID do contrato](deal-id-create.md)
>* [Configurações manuais de ID do contrato](deal-id-settings.md)
>* [Configurar um contrato programático garantido](programmatic-guaranteed-set-up.md)
