---
title: Sobre a ferramenta [!UICONTROL Planner] do DSP
description: Saiba mais sobre a ferramenta de planejamento para prever o alcance exclusivo de inserções de TV conectada (CTV) de acordo com o orçamento e os critérios de direcionamento especificados.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Sobre a ferramenta [!UICONTROL Planner] do DSP

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*recurso do Beta*

A ferramenta de planejamento ajuda você a prever o alcance exclusivo, a nível doméstico, dos posicionamentos de TV conectada (CTV) de acordo com o orçamento especificado e os critérios de direcionamento antes de começar a gastar no inventário. Depois de avaliar vários planos de alcance, você pode implementar o plano que melhor se alinha aos resultados desejados em seus pacotes e disposições.

A ferramenta de planejamento usa dados históricos de lance, impressão e alcance dos últimos 90 dias para estimar o alcance único, a média do CPM, a frequência média e as impressões de uma configuração de plano.

## Previsão do planejador

Cada previsão consiste em uma curva de previsão de orçamento de alcance que mostra a quantidade de alcance que pode ser atingida com as configurações do plano. Mova o cursor sobre a visualização para ver oportunidades de alcance incremental com orçamentos mais altos.

![Previsão do planejador](/help/dsp/assets/planner-forecast.png "Previsão do planejador")

A saída da previsão também inclui uma seção [!UICONTROL Inventory Breakdown] que mostra como diferentes editores contribuem para um alcance único, oferecendo oportunidades de descoberta valiosas.

>[!NOTE]
>
>* A seção [!UICONTROL Inventory Breakdown] exibe dados somente para o inventário privado e [!UICONTROL On Demand].
>* O alcance exclusivo estimado mostrado para dois editores pode estar sobreposto.

## A visualização do planejador

Na exibição [!UICONTROL Planner], você pode exibir seus planos de alcance de CTV existentes e criar novos.

Também é possível editar, duplicar, exportar, arquivar ou gerar novamente a previsão para qualquer plano.

## Perguntas frequentes

+++A ferramenta de planejamento oferece suporte a quais tipos de inventário?

A ferramenta de planejamento oferece suporte a todos os tipos de inventário, incluindo programático garantido (PG), mercado privado (PMP), [!UICONTROL On Demand] e público. Para gerar previsões precisas, inclua ofertas com pelo menos 50.000 impressões nos últimos sete dias.

+++

+++Por que vejo &quot;[!UICONTROL Unable to generate forecast]&quot;?

Um dos motivos mais comuns para esse erro é um orçamento insuficiente ou oferta máxima. Para obter os melhores resultados, use um orçamento mínimo de US$ 5000. Se o tipo de mídia [!UICONTROL Connected TV] for selecionado, insira um lance máximo de no mínimo US$ 10.

Além disso, verifique se os editores ou ofertas incluídos estão ativos e têm atividade de impressão recente.

+++

+++Construí uma disposição com base na previsão, mas ela não atingiu a quantidade de alcance único indicado pela previsão de alcance. Por quê? 

A previsão de alcance é apenas uma estimativa e espera-se que os resultados reais variem devido a vários fatores que mudam com frequência, como sazonalidade, competitividade de oferta e oferta e demanda. Não é esperado que seja totalmente preciso, mas é mais útil para insights direcionais sobre estratégias de campanha que podem potencialmente gerar os melhores resultados.

+++

+++O planejador pode gerar diferentes resultados de previsão com as mesmas configurações de entrada?

O planejador gera previsões com base nos últimos dados observados, de modo que a saída prevista pode variar em momentos diferentes, mesmo que as configurações do plano permaneçam as mesmas. Considere gerar várias previsões para o mesmo plano e exportar os resultados para cada uma.

+++

+++Posso salvar a saída da previsão do planejador?

Sim, você pode exportar uma previsão para uma planilha do [!DNL Microsoft Excel] clicando em **[!UICONTROL ...]** > **[!UICONTROL Export]** no canto superior direito. A planilha captura as informações exibidas na curva de orçamento de alcance usando duas colunas de dados: [!UICONTROL Budget] e [!UICONTROL Reach].

+++

>[!MORELIKETHIS]
>
>* [Sobre a ferramenta [!UICONTROL Planner] do DSP](planner-about.md)
>* [Criar um plano de alcance de TV conectado](planner-create.md)
>* [Duplicar um plano de alcance de TV conectado](planner-duplicate.md)
>* [Editar um plano de alcance de TV conectado](planner-edit.md)
>* [Exportar um plano de alcance de TV conectado](planner-export.md)
>* [Regenerar a previsão para um plano de alcance de TV conectado](planner-forecast.md)
>* [Arquivar um plano de alcance de TV conectado](planner-archive.md)
>* [Configurações para planos de alcance de TV conectados](planner-settings.md)
