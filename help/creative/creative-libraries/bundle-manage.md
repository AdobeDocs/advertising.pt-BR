---
title: Gerenciar pacotes criativos
description: Saiba mais sobre xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 95e17af996cb3171667ef3cd5ac662f08112691b
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 0%

---

# Gerenciar pacotes criativos

*Beta fechado*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Pacotes são grupos de criadores que podem ser adicionados a uma experiência como uma unidade. Depois de criar um contêiner de pacote, é possível anexar criações ao pacote. Os pacotes de exibição padrão podem conter apenas anúncios de exibição padrão, os pacotes de vídeo padrão podem conter apenas anúncios de vídeo padrão e os pacotes de exibição dinâmicos podem conter apenas anúncios de exibição dinâmicos. Você pode substituir as páginas de aterrissagem, tags de rastreamento de impressão e tags de rastreamento de cliques para todas as criações em um pacote atribuído a uma experiência da árvore de decisão de experiência, sem afetar as criações básicas.

[!DNL Creative] gira pelas criações no pacote conforme especificado para cada experiência à qual o pacote é atribuído. Opcionalmente, você pode permitir que o [!DNL Creative] otimize os elementos de anúncios para qualquer experiência baseada em desempenho usando a rotação de anúncios algorítmica, que é viabilizada pelo Adobe Sensei.

Para habilitar a otimização de elementos de anúncio em pacotes em uma experiência de anúncio, cada pacote pode incluir apenas uma de cada combinação \[creative size ou duration + language\]. Por exemplo, se um pacote incluir um criativo de 250x250 com um idioma padrão de &quot;Francês&quot;, você não poderá adicionar um segundo criativo de 250x250 com um idioma padrão de &quot;Francês&quot;. Se você tiver vários elementos de criação do mesmo tamanho no mesmo idioma, adicione-os separadamente à experiência.

As criações anexadas aos pacotes ainda estão disponíveis como criações individuais. É possível adicionar um único criativo a vários pacotes. Se você editar qualquer configuração de um criativo que está anexado a um pacote, as alterações serão propagadas para o pacote. No entanto, qualquer página de aterrissagem personalizada, tag de rastreamento de impressão e tag de rastreamento de cliques configuradas para o criativo em uma experiência são sempre usadas para a experiência.

<!-- multiselect only to duplicate and delete -->

## Criar um pacote para uma biblioteca criativa

Você pode anexar um criativo a vários pacotes.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Na parte superior direita, clique em **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Insira um **[!UICONTROL Bundle Name]** exclusivo e o **[!UICONTROL Bundle Type]:** *Vídeo Padrão* (para criações de vídeo padrão), *Vídeo Dinâmico* (para criações de vídeo dinâmico), *Vídeo Padrão* (para criações de vídeo padrão).

1. Clique em **[!UICONTROL Create]**.

## Listar os elementos de criação em um pacote

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Clique no cartão ou na linha do pacote para exibir todas as criações no pacote.

## Pacotes duplicados

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Selecione os pacotes a serem duplicados:

   * Para duplicar um único pacote:

      * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome do pacote e em **[!UICONTROL Duplicate]**.

      * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Duplicate]**.

   * Para duplicar um ou mais pacotes, marque a caixa de seleção para cada pacote que deseja duplicar. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Duplicate].**

     Para selecionar todas as linhas, marque a caixa de seleção global no canto superior esquerdo.

   Os novos conjuntos são nomeados como `<original name> (copy) # 1` (ou o próximo número na sequência). Por exemplo, se você fizer duas duplicatas de &quot;Pacote de teste&quot;, elas serão nomeadas como &quot;Pacote de teste (cópia) nº 1&quot; e &quot;Pacote de teste (cópia) nº 2&quot;.

## Editar um nome de pacote

As alterações no nome de um pacote são propagadas em todas as experiências associadas.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Selecione o pacote:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da biblioteca e em **[!UICONTROL Edit]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Edit]**.

1. Edite o **[!UICONTROL Bundle Name]**.

   O [!UICONTROL Bundle Name] deve ser exclusivo.

1. Clique em **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Anexar criações a um pacote

Você pode anexar criações de vídeo padrão existentes a um pacote de exibição padrão, criações de vídeo padrão a pacotes de vídeo padrão e criações de exibição dinâmica a um pacote dinâmico. Anexar um criativo a um pacote disponibiliza o criativo em todas as experiências às quais o pacote é atribuído. Cada pacote pode incluir apenas uma de cada combinação \[creative size ou duration + language\].

>[!NOTE]
>
>Você também pode [anexar criações a pacotes a partir das exibições de Anúncios padrão e Anúncios dinâmicos](creative-attach-detach-bundles.md).

### Anexar criações a um pacote da lista Pacotes

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Selecione o pacote:

   * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome do pacote e em **[!UICONTROL Attach Creatives]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Attach Creatives]**.

   Cada criativo qualificado para o tipo de pacote está listado no quadro correto. As criações que já estão anexadas ao pacote são listadas, mas não podem ser selecionadas.

1. (Opcional) Alterne entre a exibição de tabela padrão e uma exibição de cartão dos pacotes disponíveis clicando em ![Exibição de cartão](/help/creative/assets/card-view-button.png "Exibição de cartão") para abrir a exibição de cartão ou ![Exibição em tabela/lista](/help/creative/assets/table-view-button.png "Visualização em tabela") para retornar à exibição de tabela.

1. No quadro direito, marque a caixa de seleção ao lado de cada criativo a ser anexado ao pacote e clique em **[!UICONTROL Attach Creative to Bundle]**.

### Anexar criações a um pacote da lista criativa do pacote

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Clique no cartão ou na linha do pacote para exibir todas as criações no pacote.

1. No canto superior direito, clique em **[!UICONTROL Attach Creatives]**.

1. No painel direito, marque a caixa de seleção de cada criativo que deseja anexar.

1. Clique em **[!UICONTROL Attach Creatives to Bundle]**.

## Desanexar criações de um pacote {#bundle-detach-creatives}

Desconectar um criativo de um pacote remove a associação entre os dois, para que o criativo não seja mais usado para experiências que direcionam o pacote.

Desanexar um criativo do pacote não exclui o criativo da guia Criativos na biblioteca criativa.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Clique no cartão ou na linha do pacote para exibir todas as criações no pacote.

1. Selecione as criações para desanexar do pacote:

   * Para desanexar um único criativo:

      * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome criativo e, em seguida, clique em **[!UICONTROL Detach]**.

      * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Detach]**.

   * Para desanexar uma ou mais criações, marque a caixa de seleção de cada criação que deseja desanexar. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Detach]**.

     Para selecionar todas as linhas, marque a caixa de seleção global no canto superior esquerdo.

## Visualizar um único criativo em um pacote

Você pode visualizar um criativo como os visualizadores o verão, incluindo hiperlinks.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Clique no cartão ou na linha do pacote para exibir todas as criações no pacote.

1. Selecione o criativo:

   * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome criativo e, em seguida, clique em **[!UICONTROL Preview]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Preview]**.

1. (Opcional) Para redimensionar a imagem na tela, selecione uma opção na lista **[!UICONTROL Zoom]**, de 10% a 100% do tamanho da imagem.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Opcional) Para abrir a landing page do criativo, clique no criativo.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Para baixar o criativo, clique em ![Baixar](/help/creative/assets/download.png "Baixar").

   O arquivo é baixado de acordo com o procedimento normal do navegador.

## Visualizar todos os elementos de criação em um pacote

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Selecione o pacote:

   * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome do pacote e em **[!UICONTROL Preview]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Preview]**.

1. (Opcional) Para filtrar as criações por idioma, selecione uma opção na lista **[!UICONTROL Language]** e clique em **[!UICONTROL Preview]** no canto superior direito da visualização.

1. (Opcional) Para filtrar as criações por tamanho, selecione uma opção na lista **[!UICONTROL Size]** e clique em **[!UICONTROL Preview]** no canto superior direito da visualização.

1. (Opcional) Para redimensionar as imagens dentro da tela, selecione uma opção na lista **[!UICONTROL Zoom]**, de 10% a 100% do tamanho da imagem.

1. (Opcional) Para abrir a landing page de um criativo, clique no criativo.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Para compartilhar uma URL de demonstração para que outras pessoas sem login no [!DNL Creative] possam visualizar os elementos de criação:

   1. Clique em ![Compartilhar](/help/creative/assets/share.png "Compartilhar") no canto superior direito da visualização.

   1. Na caixa de diálogo [!UICONTROL Share Demo URL], clique em **[!UICONTROL Copy]** para copiar a URL para a área de transferência e compartilhá-la com outra pessoa.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Excluir pacotes

Você pode excluir pacotes que não estão atribuídos a uma experiência [live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses). Se um pacote for atribuído a uma experiência ao vivo, [remova o pacote da árvore decisória](/help/creative/experiences/experience-target-node-delete.md) para a experiência antes de continuar.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Clique na guia **[!UICONTROL Bundles]**.

1. Selecione os pacotes a serem excluídos:

   * Para excluir um único pacote:

      * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome do pacote e em **[!UICONTROL Delete]**.

      * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Delete]**.

   * Para excluir um ou mais pacotes, marque a caixa de seleção para cada pacote que deseja excluir. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Delete].**

     Para selecionar todas as linhas, marque a caixa de seleção global no canto superior esquerdo.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Atribuir e cancelar atribuição de pacotes criativos a um nó final em uma experiência](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Visualizar um criativo](/help/creative/creative-libraries/creative-preview.md)
>* [Adicionar criações padrão a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Gerenciar bibliotecas criativas](/help/creative/creative-libraries/creative-library-manage.md)
>* [Sobre suas bibliotecas criativas](/help/creative/creative-libraries/creative-libraries-about.md)
