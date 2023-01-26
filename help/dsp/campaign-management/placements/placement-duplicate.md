---
title: Duplicação de disposições
description: Saiba como duplicar uma ou mais disposições.
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Duplicação de disposições

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique uma ou mais disposições para criar disposições com configurações semelhantes. É possível:

* Fazer várias duplicatas de disposições
* Duplicação de disposições nos anunciantes e campanhas originais ou em campanhas diferentes
* (Para disposições duplicadas nas campanhas originais) Duplique opcionalmente os anúncios originais
* Modificar o status e as datas de voo das novas disposições

Consulte &quot;[O que não é duplicado](#placement-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Siga um destes procedimentos:

   * Para duplicar uma disposição, clique em  **[!UICONTROL ...]>[!UICONTROL Duplicate]** ao lado do nome do pacote.

   * Para duplicar várias disposições:

      1. Marque a caixa de seleção ao lado de cada disposição para duplicar.

      1. Na barra de ferramentas das ações em massa, clique em **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de posicionamento:

   1. (Disposições únicas) Insira o novo nome da disposição.

   1. No **[!UICONTROL Choose Package (Required)]** selecione o pacote principal ou **[!UICONTROL No package]*.

   1. (Opcional) Altere as configurações padrão.

   As configurações se aplicam a todas as disposições selecionadas.

   Por padrão, as novas disposições são para o tipo de anúncio original, são atribuídas aos anunciantes e campanhas originais, têm programações de voo que começam no dia atual, são pausadas e não incluem os anúncios originais.

   Quando você cria várias disposições, os novos nomes de disposições são anexados com um número, em sequência, usando a convenção &lt;*original_placement_name #N*>, como &quot;Minha disposição nº 2&quot;.

1. Clique em **[!UICONTROL Submit]**.

## O que não é duplicado {#placement-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações do experimento
* (Se você alterar as datas de voo) Programação de anúncio personalizada
* (Se você não anexar anúncios) Peso de anúncio personalizado e agendamento
* Disposições por defeito para ofertas programáticas garantidas (PG) e disposições para [!UICONTROL Simple Ad Serving] negociações
* (Se você copiar disposições para uma campanha diferente):
   * Meta geográfica
   * pixels do evento
   * Anúncios
   * Nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] segmentos (que substituem os segmentos no nível do anunciante)

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de disposição](placement-about.md)
>* [Criar uma disposição](placement-create.md)
>* [Editar uma disposição](placement-edit.md)
>* [Exibir o log de alterações para uma disposição](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)

