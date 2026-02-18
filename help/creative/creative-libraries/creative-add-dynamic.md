---
title: Adicionar criações dinâmicas a uma biblioteca criativa
description: Saiba como adicionar criações dinâmicas a uma biblioteca criativa.
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
source-git-commit: 8a304eb74549ca1a81257e9f672d311d39987b79
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Adicionar criações dinâmicas a uma biblioteca criativa

Adicione criações dinâmicas às suas [bibliotecas criativas](creative-library-manage.md) para usar com [experiências de anúncio](/help/creative/experiences/experience-about.md) dinâmicas. Você pode criar um único anúncio estático do HTML5 ou anúncios dinâmicos do HTML5 a partir de um único modelo de anúncio. Para anúncios dinâmicos do HTML5, use ativos em catálogos especificados que foram criados a partir de arquivos de feed.

>[!PREREQUISITES]
>
>Antes de adicionar criações dinâmicas a uma biblioteca criativa, você deve concluir outras etapas — incluindo a criação do modelo de anúncio, o upload de ativos e a criação (anúncios dinâmicos do HTML5) de um modelo e catálogo de feed. Consulte &quot;[Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md).&quot;

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## Adicionar criações dinâmicas usando um modelo de anúncio dinâmico do HTML5

1. Siga um destes procedimentos:

   * De uma biblioteca criativa:

      1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

      1. Clique no nome da biblioteca.

      1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

   * De um modelo de publicidade:

      1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

      1. Mantenha o cursor sobre a linha do modelo de anúncio e clique em **[!UICONTROL Create Dynamic Ad]**.

1. Especifique as [configurações de anúncios dinâmicos](/help/creative/creative-libraries/creative-settings-dynamic.md):

   1. Especifique os detalhes básicos do anúncio, incluindo o tipo de criação.

   1. Selecione o modelo de anúncio a ser usado nas criações.

      Use um modelo de anúncio do HTML5 para anúncios de exibição e um modelo de anúncio de vídeo para anúncios de vídeo.

   1. Selecione o catálogo a partir do qual os anúncios serão criados.

   1. Selecione os critérios para os quais as linhas de catálogo devem ser usadas para criar anúncios.

   1. Mapeie cada atributo (campo de anúncio dinâmico) no modelo de anúncio especificado para uma coluna no arquivo de feed especificado (rótulo do catálogo) ou insira valores estáticos.

   1. Clique em **[!UICONTROL Continue]** para visualizar as criações a serem geradas. Você pode executar qualquer um dos seguintes procedimentos na pré-visualização:

      * Para filtrar as criações por catálogo, valor do filtro <!-- explain more--> e tamanho do anúncio, use os filtros acima da área de visualização.

      * Para pesquisar um produto pelo seu identificador exclusivo no campo de pesquisa abaixo da área de pré-visualização.

      * Para alterar as colunas exibidas, clique em ![Filtro de Coluna](/help/creative/assets/custom-columns.png "Filtro de Coluna") abaixo da área de visualização.

      * Para visualizar um criativo específico, marque a caixa de seleção da linha.

      * Alterar o conteúdo:

         * Para editar o valor de uma célula na tabela, clique dentro da célula e edite o valor. Clique fora da célula ou pressione a tecla **[!DNL Enter]** para salvar suas alterações.

         * Para marcar um único produto como o padrão<!--Explain what this means. -->, mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

         * (Quando o anúncio incluir mais de uma oferta) Para marcar vários produtos como padrão, selecione as linhas (até o número de ofertas) e clique em **[!UICONTROL Set as Default]** na barra de ferramentas de ações em massa.

      * Para excluir um produto do catálogo, mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

      * (Quando o anúncio incluir mais de uma oferta) Para excluir vários produtos do catálogo, selecione as linhas (até o número de ofertas) e clique em **[!UICONTROL Delete Row]** na barra de ferramentas de ações em massa.

1. Salve os criativos:

   * Para salvar os anúncios e adicioná-los a um [pacote criativo](/help/creative/creative-libraries/bundle-manage.md) na biblioteca:

      1. Clique em **[!UICONTROL Save and Attach to Bundle]**.

      1. Clique em **[!UICONTROL Save]** para salvar os anúncios.

      1. Selecione os pacotes e clique em **[!UICONTROL Attach Creative to Bundles]**.

   * Para salvar os anúncios e sair da configuração, clique em **[!UICONTROL Save]** e em **[!UICONTROL Save]** novamente.

>[!MORELIKETHIS]
>
>* [Configurações dinâmicas de criação](creative-settings-dynamic.md)
>* [Editar um criativo dinâmico em uma biblioteca criativa](creative-edit-dynamic.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
