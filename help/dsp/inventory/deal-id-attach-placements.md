---
title: Especificar posicionamentos e anúncios para um negócio privado
description: Saiba como usar uma negociação privada com posicionamentos e anúncios adicionais.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
TQID: https://experienceleague.adobe.com/ZCFqnc6cQLEqahDoElttE7DzeZCR3IRx2lkyyb3BPMs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3b9845e85cd91cdece195593b43cbaf851368f9e
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Especificar posicionamentos e anúncios para um negócio privado

Para ofertas não garantidas, você pode especificar a oferta como um destino de inventário para novos posicionamentos na exibição [!UICONTROL Placements].

Para ofertas programáticas garantidas (PG), você pode criar inserções com anúncios especificados da exibição [!UICONTROL Deals].

Você também pode [anexar anúncios a inserções](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associadas a ofertas PG e não garantidas a qualquer momento.

## Especificar uma negociação não garantida como um destino de estoque para uma inserção

* [Criar um posicionamento a partir da [!UICONTROL Placements] exibição](/help/dsp/campaign-management/placements/placement-create.md). Nas configurações de [!UICONTROL Inventory Targeting], selecione a oferta privada.

## Anexar posicionamentos e anúncios a um contrato PG

1. No menu principal, clique em **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Na linha de negócios, clique em **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Nas configurações de [!UICONTROL Ad & Campaign Selection], selecione os anúncios a serem usados para o posicionamento:

   1. Selecione o anunciante, a campanha e o tipo de anúncio. Opcionalmente, selecione um status de anúncio pelo qual filtrar os anúncios.

   1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio a ser usado para a negociação.

   1. Clique em **[!UICONTROL Apply]**.

1. Na tela de configurações de posicionamento:

   1. Insira o nome da disposição.

   1. (Opcional) Edite as [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição da oferta padrão, que é automaticamente preenchida com o valor de CPM da oferta, a alteração do intervalo de datas ou a anexação de mais anúncios.

      A negociação é direcionada automaticamente na seção Metas de Inventário. Todas as outras opções de direcionamento são inaplicáveis.

   1. Clique em **[!UICONTROL Create placement]**.

O posicionamento começa a ser executado depois que o editor ativa a ID de contrato PG.

>[!NOTE]
>
> Você não precisa enviar a tag de negócios ao editor para verificação.

>[!MORELIKETHIS]
>
>* [Sobre o inventário privado](private-inventory-about.md)
>* [Listar os posicionamentos e anúncios de uma negociação privada](/help/dsp/inventory/private-deal-view-placements.md)
>* [Criar manualmente os detalhes da ID de negócios](deal-id-create.md)
>* [Configurações manuais de ID de negócios](deal-id-settings.md)
>* [Configurar um contrato programático garantido](programmatic-guaranteed-set-up.md)
