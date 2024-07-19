---
title: Gerenciar multiplicadores de oferta para disposições
description: Saiba como criar e editar multiplicadores de oferta para seus alvos de posicionamento.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Gerenciar multiplicadores de oferta para disposições

Você pode criar e gerenciar multiplicadores de oferta, pelos quais uma oferta calculada de forma algorítmica é multiplicada para aumentar ou diminuir a oferta, para seus destinos de posicionamento existentes de [tipos de destino qualificados](#bid-multiplier-by-target). Você pode editar manualmente os valores do multiplicador de oferta para uma disposição ou fazer upload de uma planilha com valores para uma ou mais disposições.

Por padrão, o multiplicador de oferta para uma meta é 1,00, o que significa que a oferta não é ajustada para essa meta. Os valores podem variar de 0,10 a 10,00. Por exemplo, um multiplicador de oferta de 0,5 diminui uma oferta de US$ 6 para US$ 3 (0,5 x 6). Quando um leilão é qualificado para vários modificadores de lances, todos os multiplicadores de lances aplicáveis são multiplicados. Por exemplo, se a Califórnia tiver um multiplicador de oferta de 2 e São Francisco tiver um multiplicador de oferta de 3, o multiplicador de oferta final para os anúncios executados em São Francisco será 6.

>[!NOTE]
>
>Os multiplicadores de lance nunca aumentam o lance para mais do que o lance máximo.

Você pode definir multiplicadores de oferta (com valores diferentes de 1,00) para um [número limitado de targets](#bid-multiplier-limits-by-target).

Esse recurso funciona com seus destinos de posicionamento existentes. Para alterar os destinos selecionados para seus posicionamentos, consulte &quot;[Editar Posicionamentos](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Gerenciar os Multiplicadores de Oferta para uma Única Colocação

Você pode editar valores manualmente ou fazer upload de uma planilha para uma única disposição.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajustar os multiplicadores de oferta para alvos elegíveis:

   * Para ajustar manualmente os valores do multiplicador de oferta, mova para cada [guia específica de destino](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] e [!UICONTROL Brand Safety]) e edite os valores existentes para os destinos de posicionamento.

     A maioria das categorias de público alvo lista subcategorias à esquerda. Clique em uma subcategoria para gerenciar multiplicadores de oferta para essa subcategoria, conforme aplicável.

   * Para fazer upload de um arquivo CSV com valores de multiplicador de oferta para substituir todos os valores existentes:

      1. Clique em **[!UICONTROL CSV File Edit]** no canto superior direito.

      1. a) clique em **[!UICONTROL Download Template]** e edite o arquivo ou b) edite um modelo baixado anteriormente. Salve o arquivo editado em seu dispositivo ou rede.

         As planilhas baixadas incluem uma planilha para cada tipo de destino (como País, Origens e Categoria do Site). Somente multiplicadores de oferta existentes com valores &lt; 1.0 ou > 1.0 são incluídos.

         * Para adicionar um multiplicador de lance para um target existente, informe o target usando a mesma sintaxe visível na interface do usuário e o valor do multiplicador de lance correspondente.

         * Para remover um modificador de oferta, defina o valor do multiplicador de oferta como 1,0 ou exclua todas as informações da linha.

         ![Exemplo de linha em um arquivo de planilha do multiplicador de oferta](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemplo de linha em um arquivo de planilha do multiplicador de oferta")

      1. Clique em **[!UICONTROL Next]** para mover para a seção [!UICONTROL Upload File] e a) arraste e solte o arquivo editado na caixa ou b) clique dentro da caixa para selecionar o arquivo do seu dispositivo ou rede.

      1. Verifique os dados carregados na seção [!UICONTROL Review & Submit] e clique em **[!UICONTROL Save]**.

## Fazer upload de multiplicadores de oferta para uma ou mais disposições

Faça upload de uma planilha para aplicar os mesmos valores a todas as disposições selecionadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada disposição cujos multiplicadores de oferta você deseja gerenciar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Faça upload de um arquivo CSV com valores de multiplicador de oferta para substituir todos os valores existentes para todos os posicionamentos selecionados.

   1. a) clique em **[!UICONTROL Download Template]** e edite o arquivo ou b) edite um modelo baixado anteriormente. Salve o arquivo editado em seu dispositivo ou rede.

      As planilhas baixadas incluem uma planilha para cada tipo de destino (como País, Origens e Categoria do Site). Somente multiplicadores de oferta existentes com valores &lt; 1.0 ou > 1.0 são incluídos.

      * Para adicionar um multiplicador de lance para um target existente, informe o target usando a mesma sintaxe visível na interface do usuário e o valor do multiplicador de lance correspondente.

      * Para remover um modificador de oferta, defina o valor do multiplicador de oferta como 1,0 ou exclua todas as informações da linha.

      ![Exemplo de linha em um arquivo de planilha do multiplicador de oferta](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemplo de linha em um arquivo de planilha do multiplicador de oferta")

   1. Clique em **[!UICONTROL Next]** para mover para a seção [!UICONTROL Upload File] e a) arraste e solte o arquivo editado na caixa ou b) clique dentro da caixa para selecionar o arquivo do seu dispositivo ou rede.

   1. Verifique os dados carregados na seção [!UICONTROL Review & Submit] e clique em **[!UICONTROL Save]**.

## Tipos de Alvo Qualificados para Multiplicadores de Lance {#bid-multiplier-by-target}

Você pode configurar modificadores de lances somente para alvos incluídos, não alvos excluídos.

* **Geo targets**: geografia (países, estados e cidades), códigos postais e DMAs

* **Destinos de estoque**: fontes e feeds para inventário público e inventário [!UICONTROL On Demand]

* **Destinos de site:** sites/aplicativos direcionados (mas não excluídos), categorias de site

* **Públicos-alvo:** segmentos, dayparts e tópicos

* **destinos do ads.txt:** (Quando você recusa o ads.txt, o que permite comprar o inventário de todos os vendedores) somente vendedores do ads.txt, vendedores diretos do ads.txt e vendedores do ads.txt mais sites sem ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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
>* [Sobre o Gerenciamento de Posicionamento](placement-about.md)
>* [Editar posicionamentos](placement-edit.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
