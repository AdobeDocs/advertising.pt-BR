---
title: Gerenciar multiplicadores de oferta para disposições
description: Saiba como criar e editar multiplicadores de oferta para destinos de posicionamento especificados.
feature: DSP Placements
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Gerenciar multiplicadores de oferta para disposições


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Você pode alterar os multiplicadores de oferta de seus alvos de disposição existentes usando esse recurso.

Para alterar os destinos selecionados para suas disposições, consulte &quot;[Editar disposições](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Gerenciar os multiplicadores de oferta para uma ou mais disposições

Para todas as disposições selecionadas, você pode editar os valores manualmente ou fazer upload de uma planilha com valores.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada disposição cujos multiplicadores de oferta você deseja gerenciar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajuste os multiplicadores de oferta para o target elegível manualmente ou fazendo upload de um arquivo CSV com valores de destino:

   * Para ajustar manualmente os valores do multiplicador de oferta, vá para cada guia específica de destino ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e[!UICONTROL Brand Safety]) e edite os valores existentes para os destinos de posicionamento.

   As mesmas alterações se aplicam a todos os posicionamentos selecionados.

   * Para fazer upload de um arquivo CSV com valores de multiplicador de oferta que substituirão os valores existentes:

     >[!NOTE]
     >
     >Se você deixar um campo vazio, todos os valores para esse tipo de target serão excluídos.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Clique em **[!UICONTROL CSV Edit]** no canto superior direito.

      1. a) Clique em **[!UICONTROL Download Template]** e edite os valores do multiplicador de oferta ou b) edite um template baixado anteriormente. Salve o arquivo editado em seu dispositivo ou rede.

      1. a) arraste e solte o arquivo editado na caixa ou b) clique dentro da caixa para selecionar o arquivo do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Upload]**.

   Por padrão, o multiplicador de oferta de uma meta é 1,00, o que significa que a oferta não é ajustada para essa meta. Os valores podem variar de 0,10 a 10,00. Por exemplo, um modificador de lance de 0,5 diminui um lance de USD 6 para USD 3 (0,5 x 6). É possível definir multiplicadores de oferta (com valores diferentes de 1,00) para uma [número limitado de targets](#bid-multiplier-limits-by-target).

   Quando um leilão é qualificado para vários modificadores de lance, todos os modificadores de lance aplicáveis são multiplicados.

   Os modificadores de oferta nunca aumentam a oferta para mais do que a oferta máxima.

1. Clique em **[!UICONTROL Save]**.

-->

## Fazer Upload de uma Planilha para Gerenciar os Multiplicadores de Oferta para uma Única Colocação<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

As alterações no arquivo carregado substituem os valores existentes do multiplicador de oferta.<!-- what if you delete a row? -->

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. a) Clique em **[!UICONTROL Download Template]** e edite os valores do multiplicador de oferta ou b) edite um template baixado anteriormente. Salve o arquivo editado em seu dispositivo ou rede.

   Por padrão, o multiplicador de oferta de uma meta é 1,00, o que significa que a oferta não é ajustada para essa meta. Os valores podem variar de 0,10 a 10,00. Por exemplo, um modificador de lance de 0,5 diminui um lance de USD 6 para USD 3 (0,5 x 6). É possível definir multiplicadores de oferta (com valores diferentes de 1,00) para uma [número limitado de targets](#bid-multiplier-limits-by-target).

   Quando um leilão é qualificado para vários modificadores de lance, todos os modificadores de lance aplicáveis são multiplicados.

   Os modificadores de oferta nunca aumentam a oferta para mais do que a oferta máxima.

1. a) arraste e solte o arquivo editado na caixa ou b) clique dentro da caixa para selecionar o arquivo do seu dispositivo ou rede.

1. Clique em **[!UICONTROL Upload]**.

1. Clique em **[!UICONTROL Save]**.

## Tipos de Alvo Qualificados para Multiplicadores de Lance {#bid-multiplier-by-target}

não duplicado aqui

## Número Máximo de Multiplicadores de Oferta por Tipo de Meta {#bid-multiplier-limits-by-target}

não duplicado aqui

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
