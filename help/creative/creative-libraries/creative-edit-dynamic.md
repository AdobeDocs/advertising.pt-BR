---
title: Editar e verificar a qualidade de criações dinâmicas
description: Saiba como editar configurações de criação dinâmicas e verificar a qualidade do conteúdo do catálogo em uma biblioteca criativa.
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
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# Editar e verificar a qualidade de criações dinâmicas

Edite as configurações de criação para alterar a configuração da criação, como nome, catálogos e mapeamento de atributos. Use o QA Agent para revisar os anúncios resultantes e corrigir os valores do catálogo.

## Editar configurações de criação {#edit-creative-settings}

### Da nova interface {#from-the-new-ui}

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

### Da interface herdada {#from-the-legacy-ui}

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

## Verificação de qualidade de um criativo dinâmico (somente nova interface do usuário) {#qa-dynamic-creative}

Use o Agente de controle de qualidade na nova interface do usuário para analisar linhas de catálogo em relação a um modelo do criativo dinâmico, visualizar os anúncios resultantes e identificar possíveis problemas de conteúdo. Você pode filtrar e agrupar anúncios usando o **[!UICONTROL AI Assistant]**, revisar alertas de catálogo e corrigir manualmente os valores do catálogo antes de publicar as alterações.

>[!NOTE]
>
>Você pode verificar a qualidade das criações dinâmicas de [!UICONTROL Creative Libraries] ou [!UICONTROL Creative Studio]. Consulte &quot;[Verificação de qualidade de um criativo dinâmico do Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)&quot; para o outro ponto de entrada.

O agente de controle de qualidade está disponível somente para criações de exibição dinâmicas com base em modelos dinâmicos, não criações padrão ou criações de vídeo dinâmicas.

### Abra o Agente de controle de qualidade {#open-qa-agent}

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Abra a biblioteca de uma das seguintes maneiras:

   * Clique no nome da biblioteca.
   * Ao lado do nome da biblioteca, clique em **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL ...]** ao lado do nome criativo dinâmico e clique em **[!UICONTROL QA Agent]**.

   A tela **[!UICONTROL Dynamic Creative QA]** é aberta com uma tela de visualização e o painel de chat **[!UICONTROL AI Assistant]**.

1. Se o criativo usar vários catálogos, selecione o catálogo a ser revisado de **[!UICONTROL Catalog]** no cabeçalho.

   O assistente analisa o catálogo selecionado. O seletor de catálogo é desativado quando o criativo usa apenas um catálogo.

### Analisar e filtrar anúncios com IA {#analyze-ads}

1. No painel **[!UICONTROL AI Assistant]**, digite uma solicitação em **[!UICONTROL Ask anything]** e pressione **[!UICONTROL Enter]**, ou clique em um dos prompts sugeridos:

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   O assistente responde no painel de bate-papo e exibe linhas de catálogo correspondentes como visualizações de anúncios na tela. Até que você envie uma solicitação, a tela solicita que você peça ao assistente para analisar o catálogo.

1. Continue refinando a revisão com solicitações de acompanhamento. O assistente pode ajudá-lo a:

   * Filtre anúncios por segmento de público, idioma, geografia ou código postal.
   * Verifique os comprimentos de caracteres usando um limite especificado.
   * Verifique se há erros de feed, conteúdo ausente e conteúdo suspeito.
   * Revisar status da tradução.
   * Comparar variantes de teste A/B.
   * Anúncios de grupo para análise, como por produto ou problema.

   Verifique as respostas do assistente e inspecione as visualizações antes de salvar as alterações.

### Revisar visualizações e alertas {#review-previews}

* Use a barra de ferramentas da tela para:

  * Ajuste o zoom.
  * Alternar entre **[!UICONTROL Thumbnail view]** e **[!UICONTROL Actual size]**.
  * Clique em **[!UICONTROL Replay animations]** para repetir as visualizações.
  * Selecione o número de linhas por página, selecione um número de página ou use **[!UICONTROL Previous page]** e **[!UICONTROL Next page]**.

* Quando os grupos de assistentes resultarem, clique no link para exibir todas as criações em um grupo. Use **[!UICONTROL Back to groups]** para retornar aos resultados agrupados ou **[!UICONTROL Catalog Rows]** para sair da exibição agrupada.

* Quando uma visualização mostrar **[!UICONTROL Issues detected]**, mantenha o cursor sobre o indicador para exibir os detalhes do problema.

* Quando os alertas do catálogo estiverem disponíveis, clique em **[!UICONTROL View Alerts]**. A caixa de diálogo **[!UICONTROL Alerts]** lista o catálogo, o número de linha, a coluna e a mensagem de erro para cada problema. Clique em **[!UICONTROL Close]** para retornar à tela.

### Corrigir valores do catálogo {#correct-catalog-values}

Você pode editar manualmente os valores do catálogo por meio de uma visualização de anúncio sem sair da tela de controle de qualidade.

1. Na visualização que você deseja corrigir, clique em **[!UICONTROL Edit]**.

1. Na caixa de diálogo de edição, selecione as colunas a serem alteradas em **[!UICONTROL Catalog columns to edit]**. Para localizar uma coluna, use **[!UICONTROL Search columns]**.

1. Em **[!UICONTROL Columns content]**, atualize os valores de campo selecionados.

1. Clique em **[!UICONTROL Update]**.

   A visualização é atualizada para refletir os valores atualizados. As alterações no catálogo não são publicadas até que você salve a criação dinâmica.

>[!IMPORTANT]
>
>Essas edições atualizam os dados do catálogo, não apenas a pré-visualização do anúncio. Revise os valores antes de publicá-los.

### Salvar alterações ou sair {#save-or-exit}

* Para salvar o criativo dinâmico existente e publicar qualquer edição de catálogo:

  1. Clique em **[!UICONTROL Save Dynamic Creative]** no cabeçalho.

  1. No diálogo de confirmação **[!UICONTROL Update Dynamic Creative]**, clique em **[!UICONTROL Update]**.

     Você retorna à biblioteca criativa.

* Para sair sem publicar edições de catálogo pendentes, clique em **[!UICONTROL Cancel]** no cabeçalho da página.

>[!MORELIKETHIS]
>
>* [Configurações dinâmicas de criação](creative-settings-dynamic.md)
>* [Adicionar criações dinâmicas a uma biblioteca criativa](creative-add-dynamic.md)
>* [Exibir o log de alterações para um criativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
