---
title: Duplicar disposições
description: Saiba como duplicar um ou mais posicionamentos.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Duplicar disposições

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique uma ou mais disposições para criar disposições com configurações semelhantes. Você pode:

* Fazer várias duplicações de inserções
* Duplicar inserções nos anunciantes e campanhas originais ou em diferentes anúncios
* (Para inserções duplicadas nas campanhas originais) Opcionalmente, duplique os anúncios originais
* Modificar o status e as datas de voo das novas inserções

Consulte &quot;[O que não está duplicado](#placement-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Siga um destes procedimentos:

   * Para duplicar um posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** ao lado do nome do pacote.

   * Para duplicar vários posicionamentos:

      1. Marque a caixa de seleção ao lado de cada posicionamento a ser duplicado.

      1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de posicionamento:

   1. (Inserções únicas) Insira o novo nome de inserção.

   1. No menu **[!UICONTROL Choose Package (Required)]**, selecione o pacote pai ou **[!UICONTROL No package]*.

   1. (Opcional) Altere as configurações padrão.

   As configurações se aplicam a todos os posicionamentos selecionados.

   Por padrão, as novas inserções são para o tipo de anúncio original, são atribuídas aos anunciantes e campanhas originais, têm programações de voo que começam no dia atual, são pausadas e não incluem os anúncios originais.

   Ao criar vários posicionamentos, os novos nomes de posicionamento são anexados com um número, em sequência, usando a convenção &lt;*original_placement_name #N*>, como &quot;Meu Posicionamento #2&quot;.

1. Clique em **[!UICONTROL Submit]**.

## O que não está duplicado {#placement-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações de experimento
* (Se você alterar as datas de veiculação) Programação de anúncios personalizada
* (Se você não anexar anúncios) Peso e agendamento personalizados de anúncios
* Posicionamentos padrão para ofertas programáticas garantidas (PG) e posicionamentos para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Destinos geográficos
   * Pixels de evento
   * Anúncios
   * Segmentos no nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] (que substituem os segmentos no nível do anunciante)

## Práticas recomendadas para configurar as novas disposições

>[!TIP]
>
>* Use bulksheets para [fazer alterações em vários componentes da campanha de uma só vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use folhas de marcas de publicidade para [carregar vários anúncios de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause as novas disposições até estar pronto para ativá-las.

* Considere o seguinte e edite as novas configurações de posicionamento conforme necessário:

   * A conta tem financiamento suficiente para acomodar os novos orçamentos de posicionamento?

   * Os novos posicionamentos precisam de orçamentos diferentes dos posicionamentos anteriores?

   * Faça upload de criações, incluindo qualquer ponderação e agendamento de anúncio personalizado necessário, e anexe-as aos posicionamentos.

   * Anexe pixels do evento, conforme necessário, aos posicionamentos e anúncios.

   * Inclua destinos geográficos e segmentos no nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety], conforme necessário, nos posicionamentos.

   * Para ofertas programáticas garantidas, use novas IDs de negócios e crie inserções padrão.

   * Crie novos posicionamentos para [!UICONTROL Simple Ad Serving] ofertas, conforme necessário.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Posicionamento](placement-about.md)
>* [Criar um posicionamento](placement-create.md)
>* [Editar posicionamentos](placement-edit.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
