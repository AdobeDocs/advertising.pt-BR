---
title: Editar um criativo dinâmico em uma biblioteca criativa
description: Saiba como editar um criativo dinâmico em uma biblioteca criativa.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%
---
# Editar um criativo dinâmico em uma biblioteca criativa

## Da nova interface

1. Abra as configurações de criação:

   * De uma biblioteca criativa:

     1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Abra a biblioteca de uma das seguintes maneiras:

        * Clique no nome da biblioteca.

        * Ao lado do nome da biblioteca, clique em **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL ...]**, ao lado do nome criativo, e em **[!UICONTROL Edit]**.

   * De [!UICONTROL Creative Studio]:

     1. No menu principal, clique em **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

     1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

        Um editor de tela cheia é aberto com uma pré-visualização de anúncio à esquerda e um painel de configurações à direita.

1. Edite as configurações criativas usando as guias **[!UICONTROL Details]** e **[!UICONTROL Attribute Mapping]**:

   Guia **[!UICONTROL Details]**:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** e **[!UICONTROL Ad template]** são somente leitura.
   * **[!UICONTROL Dynamic creative name]:** O nome para exibição do criativo.
   * **[!UICONTROL Number of cards]:** O número de ofertas de catálogo incluídas em cada combinação de anúncios (1-50).
   * (Opcional) Em **[!UICONTROL Catalogs]**, atualize a seleção do catálogo:
     * Use **[!UICONTROL Catalog template]** para filtrar os catálogos disponíveis. Para baixar opcionalmente o arquivo de modelo, clique em **[!UICONTROL Download feed template]**.
     * Pesquise e selecione catálogos da lista ou carregue um novo arquivo de catálogo arrastando-o para a área de carregamento ou clicando em **[!UICONTROL Browse Files]** (formatos compatíveis: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; máximo de 25 MB; um arquivo por vez). Os catálogos carregados estão rotulados como **(carregados)** na lista de chips.

     Todos os catálogos devem pertencer à mesma família de modelo de catálogo.

   Guia **[!UICONTROL Attribute Mapping]**:

   * Em **[!UICONTROL Targeting]**, selecione pelo menos uma fonte de dados: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** ou **[!UICONTROL Audience Segment]**.
   * Em **[!UICONTROL Attribute Mapping]**, atualize o mapeamento de cada nome de camada de modelo para o rótulo de coluna de catálogo correspondente.

1. Clique em **[!UICONTROL Update Creative]**.

## Da interface herdada

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique em **[!UICONTROL Switch to classic UI]**.

1. Clique no nome da biblioteca.

1. Mantenha o cursor sobre a linha criativa e clique em **[!UICONTROL Edit]**.

1. Edite as [configurações de anúncios dinâmicos](creative-settings-dynamic.md).

1. Clique em **[!UICONTROL Continue]** para visualizar as criações a serem geradas. Você pode executar qualquer um dos seguintes procedimentos na pré-visualização:

   * Para filtrar as criações por catálogo, valor do filtro <!-- explain more--> e tamanho do anúncio, use os filtros acima da área de visualização.

   * Para pesquisar um produto pelo seu identificador exclusivo no campo de pesquisa abaixo da área de pré-visualização.

   * Para alterar as colunas exibidas, clique em ![Filtro de Coluna](/help/creative/assets/custom-columns.png "Filtro de Coluna") abaixo da área de visualização.

   * Para visualizar um criativo específico, marque a caixa de seleção da linha.

   * Alterar o conteúdo:

     * (Exibir somente anúncios) Para editar o valor de uma célula na tabela, clique dentro da célula e edite o valor. Clique fora da célula ou pressione a tecla **[!DNL Enter]** para salvar suas alterações.

     * Para marcar um único produto como o padrão<!--Explain what this means. -->, mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Quando o anúncio incluir mais de uma oferta) Para marcar vários produtos como padrão, selecione as linhas (até o número de ofertas) e clique em **[!UICONTROL Set as Default]** na barra de ferramentas de ações em massa.

     * Para excluir um produto do catálogo, mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Quando o anúncio incluir mais de uma oferta) Para excluir vários produtos do catálogo, selecione as linhas (até o número de ofertas) e clique em **[!UICONTROL Delete Row]** na barra de ferramentas de ações em massa.

1. Salve os criativos:

   * Para salvar os anúncios e adicioná-los a um [pacote criativo](bundle-manage.md) na biblioteca:

     1. Clique em **[!UICONTROL Save and Attach to Bundle]**.

     1. Clique em **[!UICONTROL Save]** para salvar os anúncios.

     1. Selecione os pacotes e clique em **[!UICONTROL Attach Creative to Bundles]**.

   * Para salvar os anúncios e sair da configuração, clique em **[!UICONTROL Save]** e em **[!UICONTROL Save]** novamente.

>[!MORELIKETHIS]
>
>* [Configurações dinâmicas de criação](creative-settings-dynamic.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](creative-add-dynamic.md)
>* [Exibir o log de alterações para um criativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
