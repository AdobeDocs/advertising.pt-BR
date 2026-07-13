---
title: Gerenciar criações dinâmicas no Creative Studio
description: Saiba como criar, editar, duplicar e excluir criações dinâmicas orientadas por catálogo no Adobe Advertising Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# Gerenciar criações dinâmicas em [!UICONTROL Creative Studio]

*recurso do Beta*

A guia **[!UICONTROL Creatives]** no [!UICONTROL Creative Studio] lista suas criações dinâmicas por biblioteca. Aqui, você pode criar novas criações dinâmicas orientadas por catálogo, editar os detalhes e o mapeamento de atributos de criações existentes, exibir logs de alteração, criações duplicadas e excluir criações.

## Criar um criativo dinâmico {#build-dynamic-creative}

Use esse fluxo de trabalho para criar criações dinâmicas orientadas por catálogo. Um assistente guiado de quatro etapas orienta você na seleção de um modelo, na conexão de um catálogo e no mapeamento dos campos do catálogo aos elementos do modelo. Após a configuração, o [!UICONTROL AI Assistant] ajuda a visualizar e verificar a qualidade de cada combinação de anúncios gerada a partir dos dados do catálogo.

As criações dinâmicas diferem dos anúncios padrão de uma maneira-chave: o agente de IA não pode modificar o conteúdo proveniente do catálogo. Ele pode filtrar, analisar e sinalizar problemas, mas, para alterar o conteúdo do anúncio, é necessário atualizar o catálogo de origem.

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

   Se você continuar com o controle de qualidade, a tela mostrará todas as combinações de anúncios geradas no catálogo, exibidas como linhas com uma pré-visualização de cada entrada de catálogo renderizada no modelo.

1. Se você continuar com o controle de qualidade:

   1. Siga um destes procedimentos:

      * Use os controles **[!UICONTROL Zoom in]** e **[!UICONTROL Zoom out]** para ajustar a exibição da tela.

      * Use os controles de paginação (**X-Y de Z**) para paginar por meio de linhas de catálogo.

      * Para editar uma combinação de anúncios:

         1. Mantenha o cursor sobre a linha de catálogo e clique em **[!UICONTROL Edit]**.

         1. Na caixa de diálogo **[!UICONTROL Edit Row]**, atualize os valores do campo.

         1. Clique em **[!UICONTROL Save]**.

        A tela é atualizada para refletir os valores atualizados.

      * Use o painel de chat do **[!UICONTROL AI Assistant]** para analisar e filtrar combinações de catálogo. Digite sua solicitação no campo **[!UICONTROL Ask anything]** ou clique em um dos prompts sugeridos:

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        O agente de IA pode:

         * Filtre a tela para mostrar anúncios que correspondam a um segmento de público-alvo, uma região geográfica, um idioma, uma categoria ou outro campo de catálogo específico.
         * Verifique problemas de qualidade, como saturação de limite de caracteres, estouro ou sangramento de conteúdo, links de imagem quebrados e visibilidade do aviso.
         * Compare as combinações de anúncios para a análise do teste A/B.
         * Organize anúncios em grupos para análise lado a lado.

        O agente de IA não pode modificar o conteúdo de origem em catálogo. Para alterar o conteúdo do anúncio, atualize o catálogo de origem.

   1. Salve **[!UICONTROL Save Dynamic Creative]** no cabeçalho.

   1. Na mensagem de confirmação, clique em **[!UICONTROL Create]**.

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

## Reabra o assistente de controle de qualidade para um criativo dinâmico {#qa-dynamic-creative}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   A tela de controle de qualidade é aberta. Consulte &quot;[Etapa 5: Visualização e controle de qualidade com IA](#qa)&quot; para obter os controles de tela e recursos do assistente de IA disponíveis.

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

