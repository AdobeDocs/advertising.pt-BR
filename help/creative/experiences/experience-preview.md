---
title: Visualizar uma experiência
description: Saiba como visualizar as criações em uma experiência de anúncio.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Visualizar uma experiência

Você pode visualizar as criações com um tamanho de anúncio específico que os visualizadores do público-alvo verão para uma experiência, incluindo todos os hiperlinks. Para experiências com direcionamento de árvore de decisão, é possível visualizar um único criativo, os criativos de uma ramificação específica (tipo de destino) ou todos os criativos na experiência. Para experiências sem definição de metas da árvore de decisão, você pode visualizar um único criativo. <!-- verify -->

* Quando você visualiza todas as criações da experiência ou de uma ramificação específica, todas as criações aplicáveis são exibidas.

* Ao visualizar uma única criação e várias criações que se encaixam nos critérios, o criativo que você vê sempre que atualiza a visualização é baseado nas configurações de rotação do anúncio para a experiência:

   * Para a rotação de anúncios algorítmicos, o criativo é selecionado com base na meta de otimização.

   * Para a rotação de anúncios programada, é exibida a primeira criação no agendamento. Você pode continuar atualizando a visualização para continuar pela sequência.

   * Para uma rotação de anúncios ponderada, o criativo é selecionado com base nos pesos especificados (como uma chance de 80% de a Creative A ser exibida e uma chance de 20% de a Creative B ser exibida) cada vez.

## Pré-visualizar criações em uma experiência com direcionamento de árvore de decisão

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir experiências específicas.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Preview]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Preview]**.

1. Selecione quais criações serão visualizadas:

   * Para visualizar um único criativo:

      1. Clique em **[!UICONTROL Creative]**.

      1. Selecione o tamanho do anúncio.

      1. Na seção [!UICONTROL Decision Tree Targeting], selecione o destino criativo.

   * Para visualizar as criações de uma ramificação específica:

      1. Clique em **[!UICONTROL Particular branch]**.

      1. Selecione o tamanho do anúncio.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Selecione o público-alvo criativo.

   * Para visualizar todas as criações na experiência, clique em **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Opcional) Para incluir o nome do criativo, o tipo e o tamanho do criativo, as URLs de clique ou de URLs da página de aterrissagem e os atributos flexíveis abaixo de cada criativo, selecione **[!UICONTROL Display Creative Metadata]**.

1. Clique em **[!UICONTROL Preview]**.

1. (Visualizar apenas por criativo; opcional) Na barra de ferramentas, clique em **[!UICONTROL Refresh]** para visualizar os elementos de criação adicionais que possam ser exibidos, de acordo com as configurações de rotação de anúncios.<!-- I don't see this as of 2/3 -->

1. (Opcional) Para copiar uma URL de demonstração da experiência para compartilhar com outras pessoas sem login no [!DNL Creative]:

   1. No canto superior direito da visualização, clique em ![Compartilhar](/help/creative/assets/share.png "Compartilhar").

   1. Na caixa de diálogo [!UICONTROL Share Demo URL], clique em **[!UICONTROL Copy]** para copiar a URL para a área de transferência e compartilhá-la com outra pessoa.

## Visualizar criações em uma experiência sem direcionamento de árvore de decisão

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir experiências específicas.

1. Siga um destes procedimentos:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Preview]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Preview]**.

1. (Opcional) Limite a lista de criativos selecionando um tamanho de criação específico.

   Por padrão, criações de todos os tamanhos são listadas.

1. Clique no nome de uma tag de publicidade para expandir a linha e visualizar as criações.

1. (Opcional) Para acessar a landing page de um criativo, clique no criativo.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Para copiar uma URL de demonstração da experiência para compartilhar com outras pessoas sem login no [!DNL Creative]:

   1. No canto superior direito da visualização, clique em ![Compartilhar](/help/creative/assets/share.png "Compartilhar").

   1. Na caixa de diálogo [!UICONTROL Share Demo URL], clique em **[!UICONTROL Copy]** para copiar a URL para a área de transferência e compartilhá-la com outra pessoa.

>[!MORELIKETHIS]
>
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Criar uma experiência sem definição de metas da árvore de decisão](/help/creative/experiences/experience-create-no-targeting.md)
