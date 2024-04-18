---
title: Gerenciar multiplicadores de oferta para disposições
description: Saiba como criar e editar multiplicadores de oferta para destinos de posicionamento especificados.
feature: DSP Placements
source-git-commit: be52d56554f40babae1da683d436b821ef190e09
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 3%

---

# Gerenciar multiplicadores de oferta para disposições

Você pode alterar os multiplicadores de oferta de seus alvos de disposição existentes usando esse recurso. É possível gerenciar os multiplicadores de oferta para uma disposição de cada vez.<!-- remove that line once we can edit multiple -->

Para alterar os destinos selecionados para suas disposições, consulte &quot;[Editar uma disposição](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Mover para cada [guia específico do público-alvo](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e [!UICONTROL Brand Safety]) e edite os valores existentes para os destinos de posicionamento. A maioria das categorias de público alvo lista subcategorias à esquerda. Clique em uma subcategoria para gerenciar os multiplicadores de oferta dessa subcategoria, quando aplicável.

   Por padrão, o multiplicador de oferta de uma meta é 1,00, o que significa que a oferta não é ajustada para essa meta. Os valores podem variar de 0,10 a 10,00. Por exemplo, um modificador de lance de 0,5 diminui um lance de USD 6 para USD 3 (0,5 x 6). Os modificadores de oferta nunca aumentam a oferta para mais do que a oferta máxima.

   Quando um leilão é qualificado para vários modificadores de lance, todos os modificadores de lance aplicáveis são multiplicados.

   É possível definir multiplicadores de oferta (com valores diferentes de 1,00) para uma [número limitado de targets](#bid-multiplier-limits-by-target).

1. No canto superior direito, clique em **[!UICONTROL Save]**.

## Tipos de Alvo Qualificados para Multiplicadores de Lance {#bid-multiplier-by-target}

Você pode configurar modificadores de lances somente para alvos incluídos, não alvos excluídos.

* **Destinos geográficos**: geografia (países, estados e cidades), códigos postais e DMAs

* **Metas de estoque**: fontes e feeds para inventário público e [!UICONTROL On Demand] inventário

* **Destinos do site:** sites/aplicativos direcionados (mas não excluídos), categorias de site

* **Públicos-alvo:** segmentos, dayparts e tópicos

* **destinos do ads.txt:** (Ao recusar o ads.txt, que permite comprar inventário de todos os vendedores) somente vendedores do ads.txt, vendedores diretos do ads.txt e vendedores do ads.txt mais sites sem ads.txt <!-- bid multipliers for the different subsets of inventory -->

## Número Máximo de Multiplicadores de Oferta por Tipo de Meta {#bid-multiplier-limits-by-target}

É possível definir multiplicadores de oferta (com valores diferentes de 1,00) para um número limitado de públicos-alvos. Por exemplo, você pode definir multiplicadores de lance para até 20 metas de país. O número máximo de alvos para cada tipo de alvo que pode ter multiplicadores de lance está listado abaixo.

| Categoria | Parâmetro | Número máximo |
| -------- | --------- | ----- |
| Geo | País | 20 |
| Geo | Estado | 100 |
| Geo | Cidade | 100 |
| Geo | Metro | 100 |
| Geo | Códigos postais | 100 |
| Inventário | Origens | 100 |
| Inventário | Feeds | 100 |
| Sites | Categoria do site | 100 |
| Sites | Sites/Aplicativos | 100 |
| Público-alvo | Segmentos | 500 |
| Público-alvo | Temas | 100 |
| Segurança da marca | Ads.txt | N/D |

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de posicionamento](placement-about.md)
>* [Editar uma disposição](placement-edit.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
