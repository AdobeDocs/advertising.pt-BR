---
title: Gerenciar criações dinâmicas no Creative Studio
description: Saiba como criar, verificar a qualidade, editar, duplicar e excluir criações dinâmicas orientadas por catálogo no Adobe Advertising Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b9a68528b3c622aae44a46bca9b3bb747019bc95
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# Gerenciar criações dinâmicas em [!UICONTROL Creative Studio]

A guia **[!UICONTROL Creatives]** no [!UICONTROL Creative Studio] lista suas criações dinâmicas por biblioteca. Aqui, você pode criar novas criações dinâmicas orientadas por catálogo, criações de verificação de qualidade com IA, editar os detalhes e o mapeamento de atributos de criações existentes, exibir logs de alteração, criações duplicadas e excluir criações.

## Criar um criativo dinâmico {#build-dynamic-creative}

Use esse fluxo de trabalho para criar criações dinâmicas orientadas por catálogo. Um assistente guiado de quatro etapas orienta você na seleção de um modelo, na conexão de um catálogo e no mapeamento dos campos do catálogo aos elementos do modelo. Após a configuração, o [!UICONTROL AI Assistant] ajuda a visualizar e verificar a qualidade de cada combinação de anúncios gerada a partir dos dados do catálogo.

As criações dinâmicas diferem dos anúncios padrão de uma maneira-chave: o agente de IA não pode modificar o conteúdo proveniente do catálogo. Ele pode filtrar, analisar e sinalizar problemas, mas para alterar o conteúdo do anúncio, você deve atualizar os valores do catálogo manualmente, na tela de QA ou no catálogo de origem.

### Pré-requisitos

* Pelo menos um modelo de anúncio de exibição criado pelo usuário (não um modelo do sistema) deve existir em sua biblioteca de modelos.
* Um catálogo de produtos ou conteúdo (feed) está disponível em sua conta.

### Etapa 1: Abrir o assistente do [!UICONTROL Build Dynamic Creative] {#open-wizard}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL Build]** no cartão de ação rápida **[!UICONTROL Build dynamic creatives from catalog data]**.

   A caixa de diálogo de quatro etapas **[!UICONTROL Build Dynamic Creative]** é aberta.

### Etapa 2: Selecionar um modelo {#select-template}

>[!NOTE]
>
>A galeria de modelos lista somente os modelos de anúncios de exibição criados. Os modelos de sistema e de anúncio de vídeo não estão disponíveis como ponto de partida para criações dinâmicas.

1. Na galeria de modelos, clique em um modelo para selecioná-lo.

   O botão **[!UICONTROL Next]** estará desabilitado até que um modelo seja selecionado.

1. Clique em **[!UICONTROL Use this template]**.

### Etapa 3: Selecionar um catálogo {#select-catalog}

1. Defina as configurações de criação:

   * **[!UICONTROL Ad Library]:** Selecione a biblioteca criativa na qual salvar o criativo.
   * **[!UICONTROL Dynamic creative name]:** Insira um nome para a criação dinâmica.
   * **[!UICONTROL Number of cards]:** Insira o número de ofertas de catálogo a serem incluídas em cada combinação de anúncios (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (Opcional) Quando habilitado, as criações salvas são anexadas a um conjunto. Selecione um pacote na biblioteca.

1. Selecione um ou mais catálogos:

   1. (Opcional) Use **[!UICONTROL Catalog template]** para filtrar a lista de catálogos para uma família de modelos específica. Para baixar opcionalmente o arquivo de modelo para revisá-lo, clique em **[!UICONTROL Download feed template]**.

   1. Procure e selecione catálogos na lista. Todos os catálogos selecionados devem pertencer à mesma família de modelo de catálogo; um aviso será exibido se você tentar misturar famílias.

   1. (Opcional) Para carregar um novo arquivo de catálogo, arraste e solte o arquivo na área de carregamento ou clique em **[!UICONTROL Browse Files]**. Formatos compatíveis: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP e MP4. Tamanho máximo do arquivo: 25 MB. É possível fazer upload de um arquivo por vez. Os catálogos carregados aparecem na lista de chips rotulada **(carregado)**.

1. Clique em **[!UICONTROL Continue]**.

### Etapa 4: Mapear campos de catálogo para elementos de modelo {#attribute-mapping}

Mapeie cada campo de catálogo para o elemento correspondente no modelo. Por exemplo, mapeie o campo de nome de produto do catálogo para o elemento de título do modelo e o campo de imagem do produto para o elemento de imagem do plano de fundo.

1. Em **[!UICONTROL Targeting]**, selecione pelo menos uma fonte de dados para personalizar a criação: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** ou **[!UICONTROL Audience Segment]**.

1. Para cada elemento de template, selecione o campo de catálogo correspondente na lista suspensa.

1. Clique em **[!UICONTROL Continue]**.

### Etapa 5: Pré-visualização e QA com IA {#qa}

1. Escolha se deseja *[!UICONTROL Save Dynamic Creative & Skip QA]* ou *[!UICONTROL Continue to QA]*.

   Se você continuar com o controle de qualidade, a tela **[!UICONTROL Dynamic Creative QA]** será aberta com uma tela de visualização e o painel de chat **[!UICONTROL AI Assistant]**.

1. Se você continuar com o controle de qualidade, siga os procedimentos em &quot;[Verificação de qualidade de uma criação dinâmica](#qa-dynamic-creative)&quot; para [analisar e filtrar anúncios](#analyze-ads), [revisar visualizações e alertas](#review-previews) e, opcionalmente, [corrigir valores de catálogo](#correct-catalog-values). Quando terminar, [salve o criativo dinâmico](#save-or-exit).

## Editar um criativo dinâmico {#edit-dynamic-creative}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

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

## Verificação de qualidade de um criativo dinâmico {#qa-dynamic-creative}

Use o assistente de controle de qualidade para analisar linhas do catálogo em relação ao modelo de um criativo dinâmico, visualizar os anúncios resultantes e identificar possíveis problemas de conteúdo. Você pode filtrar e agrupar anúncios usando o **[!UICONTROL AI Assistant]**, revisar alertas de catálogo e corrigir manualmente os valores do catálogo antes de publicar as alterações.

>[!NOTE]
>
>Você pode verificar a qualidade das criações dinâmicas de [!UICONTROL Creative Studio] ou [!UICONTROL Creative Libraries]. Embora os rótulos de menu sejam diferentes, ambos os pontos de entrada abrem a mesma tela **[!UICONTROL Dynamic Creative QA]** com a mesma funcionalidade. A análise depende da criação, do catálogo e da solicitação selecionados. Consulte &quot;[Verificação de qualidade de um criativo dinâmico de Bibliotecas Creative](/help/creative/creative-libraries/creative-edit-dynamic.md#qa-dynamic-creative)&quot; para o outro ponto de entrada.

O assistente de controle de qualidade está disponível para criações de exibição dinâmica, não criações padrão ou criações de vídeo dinâmico.

### Abrir o assistente de controle de qualidade {#open-qa-agent}

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, localize o criativo dinâmico em sua biblioteca criativa abaixo da seção [!UICONTROL Generate or Build Creatives].

1. Mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

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

* Para salvar o criativo dinâmico e publicar qualquer edição de catálogo:

  1. Clique em **[!UICONTROL Save Dynamic Creative]** no cabeçalho.

  1. Confirme o salvamento:

     * Para um novo criativo, na caixa de diálogo de confirmação **[!UICONTROL Create Dynamic Creative]**, clique em **[!UICONTROL Create]**.
     * Para um criativo existente, na caixa de diálogo de confirmação **[!UICONTROL Update Dynamic Creative]**, clique em **[!UICONTROL Update]**.

     Você retorna para [!UICONTROL Creative Studio].

* Para sair sem publicar edições de catálogo pendentes, clique em **[!UICONTROL Cancel]** no cabeçalho da página.

## Exibir o log de alterações para um criativo dinâmico {#view-change-log}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Duplicar um criativo dinâmico {#duplicate-dynamic-creative}

Duplique um criativo dinâmico para adicionar um novo criativo com as mesmas configurações à biblioteca. Posteriormente, é possível renomear o novo criativo e editar as configurações, conforme necessário.

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   O nome do novo criativo é `<original name> (copy)`.

## Excluir um criativo dinâmico {#delete-dynamic-creative}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre o Creative Studio no Advertising Creative](creative-studio-about.md)
>* [Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gerenciar modelos no Creative Studio](creative-studio-manage-templates.md)
