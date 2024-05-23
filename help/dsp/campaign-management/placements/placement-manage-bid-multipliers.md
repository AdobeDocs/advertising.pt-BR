---
title: Gerenciar multiplicadores de oferta para disposições
description: Saiba como criar e editar multiplicadores de oferta para seus alvos de posicionamento.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: c0dd18a3ce8759214813b7303c590a28febf1b37
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 2%

---

# Gerenciar multiplicadores de oferta para disposições

É possível criar e gerenciar multiplicadores de lance, pelos quais um lance é multiplicado para aumentar ou diminuir o lance, para seus alvos de posicionamento existentes de [tipos de público alvo elegíveis](#bid-multiplier-by-target). Você pode editar manualmente os valores do multiplicador de oferta ou fazer upload de uma planilha com valores.

Por padrão, o multiplicador de oferta para uma meta é 1,00, o que significa que a oferta não é ajustada para essa meta. Os valores podem variar de 0,10 a 10,00. Por exemplo, um modificador de lance de 0,5 diminui um lance de USD 6 para USD 3 (0,5 x 6). Quando um leilão é qualificado para vários modificadores de lance, todos os modificadores de lance aplicáveis são multiplicados. Os modificadores de oferta nunca aumentam a oferta para mais do que a oferta máxima.

É possível definir multiplicadores de oferta (com valores diferentes de 1,00) para uma [número limitado de targets](#bid-multiplier-limits-by-target).

Esse recurso funciona com seus destinos de posicionamento existentes. Para alterar os destinos selecionados para suas disposições, consulte &quot;[Editar disposições](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajustar os multiplicadores de oferta para alvos elegíveis:

   * Para ajustar manualmente os valores do multiplicador de oferta, mova para cada [guia específico do público-alvo](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e [!UICONTROL Brand Safety]) e edite os valores existentes para os destinos de posicionamento.

     A maioria das categorias de público alvo lista subcategorias à esquerda. Clique em uma subcategoria para gerenciar multiplicadores de oferta para essa subcategoria, conforme aplicável.

   * Para fazer upload de um arquivo CSV com valores de multiplicador de oferta para substituir todos os valores existentes:

      1. Clique em **[!UICONTROL CSV File Edit]** no canto superior direito.

      1. a) Clique em **[!UICONTROL Download Template]** e edite o arquivo ou b) edite um template baixado anteriormente. Salve o arquivo editado em seu dispositivo ou rede.

         As planilhas baixadas incluem uma planilha para cada tipo de destino (como País, Origens e Categoria do Site). Somente multiplicadores de oferta existentes com valores &lt; 1.0 ou > 1.0 são incluídos.

         * Para adicionar um multiplicador de lance para um target existente, informe o target usando a mesma sintaxe visível na interface do usuário e o valor do multiplicador de lance correspondente.

         * Para remover um modificador de oferta, defina o valor do multiplicador de oferta como 1,0 ou exclua todas as informações da linha.

         ![Exemplo de linha em um arquivo de planilha do multiplicador de oferta](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemplo de linha em um arquivo de planilha do multiplicador de oferta")

      1. Clique em **[!UICONTROL Next]** para ir para a [!UICONTROL Upload File] e a) arraste e solte o arquivo editado na caixa ou b) clique dentro da caixa para selecionar o arquivo do seu dispositivo ou rede.

      1. Verifique os dados carregados na variável [!UICONTROL Review & Submit] e clique em **[!UICONTROL Save]**.

## Tipos de Alvo Qualificados para Multiplicadores de Lance {#bid-multiplier-by-target}

Você pode configurar modificadores de lances somente para alvos incluídos, não alvos excluídos.

* **Destinos geográficos**: geografia (países, estados e cidades), códigos postais e DMAs

* **Metas de estoque**: fontes e feeds para inventário público e [!UICONTROL On Demand] inventário

* **Destinos do site:** sites/aplicativos direcionados (mas não excluídos), categorias de site

* **Públicos-alvo:** segmentos, dayparts e tópicos

* **destinos do ads.txt:** (Ao recusar o ads.txt, que permite comprar inventário de todos os vendedores) somente vendedores do ads.txt, vendedores diretos do ads.txt e vendedores do ads.txt mais sites sem ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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
>* [Editar disposições](placement-edit.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
