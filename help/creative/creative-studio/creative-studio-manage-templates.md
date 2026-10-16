---
title: Gerenciar modelos de anúncios no Creative Studio
description: Saiba como criar, importar, organizar e gerenciar modelos de anúncios no Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8fa8d6c66228d3a0af1de2514dd016d8f50262e8
workflow-type: tm+mt
source-wordcount: '3702'
ht-degree: 1%
---
# Gerenciar modelos de anúncios em [!UICONTROL Creative Studio]

Crie, importe e gerencie modelos de exibição e anúncio de vídeo para uso em sessões de geração de anúncios.

## A visualização [!UICONTROL Creative Studio] > [!UICONTROL Templates]

A guia **[!UICONTROL Templates]** fornece ações rápidas para criar ou importar novos modelos de anúncios.

A guia [!UICONTROL Templates] também lista seus modelos de anúncios existentes na parte inferior da página <!-- Only in the Templates tab --> como [cartões individuais (o padrão) ou como tabelas/listas](/help/creative/introduction/customize-data-views.md). A lista de modelos de anúncio inclui guias para [!UICONTROL All], [!UICONTROL System Templates] (que a equipe de conta da Adobe carrega na sua conta) e [!UICONTROL User Templates]. Por padrão, são exibidos modelos de anúncio para todos os anunciantes. Para exibir apenas os modelos de anúncios de um anunciante específico, selecione na lista de anunciantes na parte superior da página.

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Ações disponíveis

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Criação:

* [Gerar um modelo de anúncio usando IA](#template-generate)

* [Criar um modelo de anúncio manualmente](#template-create)

* [Importar modelos de anúncios do HTML5](#templates-import)

Ações em seus modelos existentes:

* [Gerar variações de anúncios a partir de um modelo de anúncio de exibição](#ad-variations-generate)

* [Editar um modelo de anúncio](#template-edit)

* [Adicionar ou remover rótulos de um modelo de anúncio](#template-labels)

* [Pré-visualizar um modelo de anúncio](#template-preview)

* [Baixar um modelo de anúncio](#template-download)

* [Adicionar ou remover um modelo de anúncio como favorito](#template-favorite)

* [Excluir um modelo de anúncio](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Gerar um modelo de anúncio usando IA {#template-generate}

*recurso do Beta*

Use a IA em [!UICONTROL Creative Studio] para converter uma imagem de anúncio de exibição estática existente em um modelo de anúncio de exibição editável. Um assistente de três etapas ajuda a gerar e revisar o modelo, solicitar alterações usando a linguagem natural e abrir o editor de modelo para fazer alterações manuais e salvar o modelo.

### Pré-requisitos

Você precisa de um anúncio de imagem estática em uma Biblioteca da Creative. Esse fluxo de trabalho seleciona anúncios das bibliotecas; ele não carrega uma nova imagem diretamente na caixa de diálogo de geração.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Etapa 1: Gerar e revisar o modelo

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. (Opcional) Selecione um anunciante na lista de anunciante na parte superior da página para exibir as bibliotecas desse anunciante.

1. Na caixa **[!UICONTROL Use AI to Generate a New Display Ad Template]**, clique em **[!UICONTROL Generate]**.

1. Na caixa de diálogo **[!UICONTROL Generate New Ad Template]**, selecione **[!UICONTROL Generate from Existing Standard Ad Image]** se ainda não estiver selecionado.

1. Selecione a biblioteca que contém o anúncio de imagem na lista **[!UICONTROL Ad Library]**.

1. Mantenha o cursor sobre o cartão de anúncio da imagem e clique em **[!UICONTROL Use this Standard Ad]**.

   A geração começa automaticamente, usando a largura e a altura do anúncio selecionado.

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Revise e refine o modelo gerado](#template-review).

### Etapa 2: revisar e refinar o modelo {#template-review}

1. Aguarde a conclusão da geração e revise a visualização do modelo e o painel **[!UICONTROL Layers]**, quando disponíveis.

   Verifique o texto, as imagens e o layout antes de usar o modelo. As camadas mostradas aqui são para revisão; faça alterações manuais no editor de modelo.

1. (Opcional) Solicitar alterações no modelo gerado:

   1. No campo **[!UICONTROL Ask the AI for any changes]**, descreva as alterações desejadas. Por exemplo, digite `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Clique em **[!UICONTROL Regenerate]**.

   1. Revise a visualização atualizada. Repita conforme necessário.

1. Quando estiver pronto para continuar, clique em **[!UICONTROL Use this Ad Template]**.

   O modelo gerado é aberto no editor de modelo de exibição.

### Etapa 3: editar e salvar o modelo {#template-save}

>[!TIP]
>
> O assistente de IA usa uma biblioteca de fontes de código aberto para encontrar uma correspondência próxima para a fonte em seu anúncio. Para usar sua própria fonte, carregue-a na guia [!UICONTROL Assets] ou no editor de modelo e substitua a fonte gerada no editor.
>
> Para obter melhores resultados, substitua o logotipo gerado pela IA pelo seu logotipo original com pixel perfeito no editor de modelos.

1. No editor de modelos, revise os elementos gerados e faça as alterações restantes usando os [controles do editor de modelos](#template-controls).

1. Clique em **[!UICONTROL Save]**.

1. Na caixa de diálogo **[!UICONTROL Update Template]**, insira ou atualize a **[!UICONTROL Template name]**, selecione a **[!UICONTROL Advertiser]** e, opcionalmente, adicione marcas.

1. Clique em **[!UICONTROL Update]** para salvar o modelo e retornar à exibição **[!UICONTROL Templates]**.

   Para salvar uma cópia separada, clique em **[!UICONTROL Save As New]**.

Você pode usar o modelo para [gerar variações de anúncios](#ad-variations-generate).

### Se você não puder gerar um template {#troubleshooting}

| Problema | O que fazer |
| --- | --- |
| Nenhuma biblioteca ou anúncio de imagem é listado ao gerar de uma imagem | Verifique o anunciante selecionado e **[!UICONTROL Ad Library]**. Se a biblioteca não tiver imagens de anúncio padrão, selecione outra biblioteca contendo um anúncio de imagem estática existente. |
| A geração baseada em imagem falha ou a imagem não pode ser convertida | Revise a mensagem exibida, clique em **[!UICONTROL Back to library]**, selecione uma imagem e tente novamente. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## Criar um modelo de anúncio manualmente {#template-create}

Crie um modelo de exibição ou vídeo em branco usando o editor de modelo.

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Na caixa **[!UICONTROL Create New Ad Template]**, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Display Ad Template]** ou **[!UICONTROL Video Ad Template]**.

1. (Exibir anúncios) Selecione o tamanho do modelo de anúncio e clique em **[!UICONTROL Continue]**.

1. Defina as configurações do modelo usando os [controles no editor de modelo](#template-controls).

1. (Opcional) Para baixar uma cópia do modelo conforme definido, clique em **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

1. Salve o template:

   1. Siga um destes procedimentos:

      * Clique em **[!UICONTROL Save]**.

      * Para salvar o modelo como rascunho, clique em **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Insira o **[!UICONTROL Template name]**, selecione o **[!UICONTROL Advertiser]**, opcionalmente selecione marcas existentes ou adicione novas marcas ao modelo e clique em **[!UICONTROL Save]**.

## Importar modelos de anúncios do HTML5 {#templates-import}

Faça upload de um ou mais modelos HTML5 pré-criados que são empacotados como arquivos ZIP. Os modelos são validados na importação; a importação falha se o HTML exceder 200.000 caracteres, o CSS exceder 60.000 caracteres, o modelo contiver mais de 5.000 elementos DOM ou o modelo incluir tags de script não compatíveis.

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Selecione o anunciante na parte superior da página.

1. Clique na guia **[!UICONTROL Templates]**.

1. Na caixa **[!UICONTROL Upload HTML5 Templates]**, clique em **[!UICONTROL Upload]** e selecione **[!UICONTROL Display Ad Template]** ou **[!UICONTROL Video Ad Template]**.

1. Selecione um ou mais arquivos ZIP do dispositivo ou da rede.

1. No diálogo **[!UICONTROL Import Templates]**:

   1. Selecione um **[!UICONTROL Advertiser]**.

      Se você já tiver selecionado um anunciante específico na parte superior da página, esse anunciante será pré-selecionado.

   1. (Opcional) Para cada arquivo, edite o **[!UICONTROL Template Name]**.

      O nome do arquivo é usado por padrão.

   1. (Opcional) Para adicionar mais arquivos, clique em **[!UICONTROL Add more]** e selecione arquivos ZIP adicionais. Especifique o **[!UICONTROL Template Name]** para cada arquivo adicional.

1. Clique em **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>Se a importação falhar, simplifique o modelo ou entre em contato com a equipe de conta da Adobe.

## Editar um modelo de anúncio {#template-edit}

*Exibir modelos de anúncio somente.*

>[!IMPORTANT]
>
>O agente de IA não pode alterar o layout do modelo, as posições dos elementos, o espaçamento ou a tipografia. Faça alterações estruturais no editor de modelo antes de gerar o conteúdo.

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão do modelo ou a linha da tabela e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Edite o layout ou os elementos do modelo usando os [controles no editor de modelo](#template-controls).

1. (Opcional) Para baixar uma cópia do modelo conforme definido, clique em **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   O arquivo é baixado de acordo com o procedimento normal do navegador.

1. Salve o template:

   * Clique em **[!UICONTROL Save]**.

   * Para salvar o modelo como rascunho, clique em **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Insira o **[!UICONTROL Template name]**, selecione o **[!UICONTROL Advertiser]**, opcionalmente selecione marcas existentes ou adicione novas marcas ao modelo e clique em **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Gerar variações de anúncios a partir de um modelo de anúncio de exibição {#ad-variations-generate}

*Exibir modelos de anúncio somente.*

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão do modelo ou a linha da tabela e clique em **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   O [!UICONTROL Ad Variations Generator] é aberto com o modelo pré-carregado.

1. Use a interface de bate-papo do AI para gerar e refinar conteúdo de anúncios. Consulte &quot;[Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)&quot; para obter o fluxo de trabalho completo.

## Adicionar ou remover rótulos de um modelo de anúncio {#template-labels}

*Exibir modelos de anúncio somente.*

Os rótulos ajudam a organizar e filtrar modelos de usuário. Não é possível adicionar rótulos aos modelos do sistema.

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão do modelo ou a linha da tabela e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. No diálogo **[!UICONTROL Edit Labels]**:

   * Para adicionar um rótulo, selecione um rótulo existente ou insira um nome no campo de entrada e clique em **[!UICONTROL Add Tag]**.

   * Para remover um rótulo, clique em **[!UICONTROL X]** ao lado da marca de rótulo.

1. Clique em **[!UICONTROL Save]**.

## Pré-visualizar um modelo de anúncio {#template-preview}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão de modelo.

1. Siga um destes procedimentos:

   * (Exibição de cartão) Clique no ícone **[!UICONTROL Preview template]** ou clique em **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Modo de exibição Tabela) Clique em **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

1. Para modelos de vídeo, clique em ![Reproduzir](/help/creative/assets/play.png "Reproduzir").

## Baixar um modelo de anúncio {#template-download}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão do modelo ou a linha da tabela e clique em **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   O modelo é baixado como um arquivo ZIP de acordo com o procedimento normal do navegador.

## Adicionar ou remover um modelo de anúncio como favorito {#template-favorite}

*Somente exibição de cartão*

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão de modelo.

1. Siga um destes procedimentos:

   * Para adicionar um modelo como favorito, clique em ![Favorito](/help/creative/assets/favorite-null.png "Favorito").

   * Para remover um modelo como favorito, clique em ![Favorito](/help/creative/assets/favorite.png "Favorito").

## Excluir um modelo de anúncio {#template-delete}

1. No menu principal, clique em **[!UICONTROL Creative Studio].**

1. Clique na guia **[!UICONTROL Templates]**.

1. Mantenha o cursor sobre o cartão do modelo ou a linha da tabela e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Controles do editor de modelo {#template-controls}

Os editores de modelo de vídeo e exibição fornecem uma barra de ferramentas acima da tela para desfazer alterações e ajustar a exibição, painéis à esquerda para adicionar ativos e elementos e um painel [!UICONTROL Layers] à direita para gerenciar camadas. As ferramentas para editar elementos selecionados e controlar o tempo e a reprodução diferem entre os modelos de exibição e de vídeo.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Desfazer alterações e ajustar a visualização da tela de desenho

A barra de ferramentas de ações gerais fica acima da tela de edição no editor de modelo de anúncio e é dividida em duas partes (esquerda e direita).

#### Exibir modelos de anúncio

| Controle | Descrição |
| --- | --- |
| **[!UICONTROL Undo]** | Desfaz a última ação. |
| ![Refazer](/help/creative/assets/cs-icon-redo.png "Refazer") **[!UICONTROL Redo]** | Refaz a última ação desfeita. |
| **[!UICONTROL Links]** | Abre um painel para gerenciar os URLs de click-through anexados aos elementos no modelo. |
| Controles de zoom | Clique em **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** para ajustar a ampliação da tela (10%-150%, em incrementos de 10%). Clique no rótulo do nível de zoom — que mostra **[!UICONTROL Auto]** quando a tela se ajusta automaticamente ou uma porcentagem quando definida manualmente — para abrir um menu com opções: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| Tamanho do anúncio | Mostra as dimensões atuais do anúncio (por exemplo, 300 × 250). Clique para abrir o seletor de tamanho, que oferece seis tamanhos padrão de IAB comumente usados como cartões, além de uma lista suspensa com todos os 19 tamanhos de anúncio de exibição de IAB padrão. O tamanho padrão para novos modelos é 300 × 250 (Retângulo Medium). |
| ![Abrir painel Camadas](/help/creative/assets/layers-panel-open.png "Abrir painel Camadas") | Abre o painel [!UICONTROL Layers]. Aparece somente quando o painel [!UICONTROL Layers] é fechado. |

#### Modelos de anúncio de vídeo

| Controle | Descrição |
| --- | --- |
| **[!UICONTROL Undo]** / ![Refazer](/help/creative/assets/cs-icon-redo.png "Refazer") **[!UICONTROL Redo]** | Desfaz ou refaz a última ação. |
| Controles de zoom | Clique em **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** para ajustar a ampliação da tela de desenho. Clique no nível de zoom para abrir um menu com opções: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| ![Abrir painel Camadas](/help/creative/assets/layers-panel-open.png "Abrir painel Camadas") | Abre o painel [!UICONTROL Layers]. Aparece somente quando o painel [!UICONTROL Layers] é fechado. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Adicionar ativos e elementos

O painel esquerdo permite adicionar ativos e elementos de anúncios ao modelo. Clique em um ícone para abrir seu painel de conteúdo; clique no mesmo ícone novamente para fechá-lo.

#### Exibir modelos de anúncio

| Ícone | Descrição |
| --- | --- |
| **[!UICONTROL Search]** | Pesquise em todos os tipos de ativos na biblioteca. |
| **[!UICONTROL Upload]** | Fazer upload de imagens ou arquivos de fontes no editor para uso no modelo atual. Você pode carregar até 20 arquivos de cada vez. |
| **[!UICONTROL Templates]** | Procure modelos de anúncios na biblioteca do Creative Studio para usar como uma camada base ou elemento de referência. |
| **[!UICONTROL My Assets]** | Navegue por todos os ativos carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Images]** | Procure somente os ativos de imagem carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Text]** | Adicione um elemento de texto à tela, incluindo qualquer fonte personalizada que você tenha carregado. |
| **[!UICONTROL Elements]** | Adicionar elementos de formas e layout, como botões e retângulos. |

Você pode arrastar um item de qualquer painel diretamente para a tela ou clicar nele para colocá-lo na posição padrão.

#### Modelos de anúncio de vídeo

| Ícone | Descrição |
| --- | --- |
| **[!UICONTROL Search]** | Pesquise em todos os tipos de ativos na biblioteca. |
| **[!UICONTROL Upload]** | Fazer upload de arquivos de imagem, vídeo, áudio ou fonte (TTF, OTF, WOFF, WOFF2) no editor para uso no modelo atual. Você pode carregar até 20 arquivos de cada vez. |
| **[!UICONTROL Templates]** | Procure modelos de anúncios na biblioteca do Creative Studio. |
| **[!UICONTROL My Assets]** | Navegue por todos os ativos carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Images]** | Procure somente os ativos de imagem carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Video]** | Procure somente os ativos de vídeo carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Audio]** | Procure somente os ativos de áudio carregados na guia do Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Text]** | Adicione um elemento de texto à tela, incluindo qualquer fonte personalizada que você tenha carregado. |
| **[!UICONTROL Elements]** | Adicionar formas e elementos de vetor. |

Você pode arrastar um item de qualquer painel diretamente para a tela ou clicar nele para colocá-lo na posição padrão.

### Editar elementos selecionados

Clique em um elemento na tela de edição para selecioná-lo. Dependendo do tipo de modelo, uma ou mais barras de ferramentas são exibidas com controles para esse elemento.

Os controles variam de acordo com o tipo de elemento.

<!-- From inspectorbar.ts -->

#### Exibir barra de ferramentas de edição do modelo

| Controle | Tipos de elemento | Descrição |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Todos | Abre um painel para editar o nome da camada; marca a camada como dinâmica (trocável durante a geração do anúncio); e define um URL de click-through (somente links). Abaixo disso, escolha um estado **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** para estilizar o elemento para esse estado de interação, em seguida, ajuste o estilo — tipografia (somente texto e links), decorações (preenchimento, borda, raio do canto), dimensões, posição — com base no tipo de elemento. |
| **[!UICONTROL Effects]** | Todos | Abre um painel no qual você escolhe um estado **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** para aplicar efeitos a esse estado de interação e ajusta as seções **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** e **[!UICONTROL Cursor]**. Os elementos de texto também incluem uma seção **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Todos | Abre um painel para definir a hora de entrada e saída da camada na linha do tempo e para configurar as predefinições **[!UICONTROL Entrance Animation]**, **[!UICONTROL Loop Animation]** e **[!UICONTROL Exit Animation]** com duração e atenuação. Inclui ações **[!UICONTROL Copy]**, **[!UICONTROL Paste]** e **[!UICONTROL Reset]**. |
| **[!UICONTROL Crop]** | Imagens | Abre uma barra de ferramentas para recortar a imagem. Selecione uma predefinição de **[!UICONTROL Aspect Ratio]** (ou **[!UICONTROL Free]**) e clique em **[!UICONTROL Apply]** ou **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Todos | Abre um menu com **[!UICONTROL Move]** opções (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** opções (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**) e, para elementos que não sejam de imagem, **[!UICONTROL Layer Level Alignment]** opções (as mesmas seis opções de alinhamento, mais **[!UICONTROL Fit to Content]**). |

#### Barra de ferramentas de edição do modelo de vídeo

| Controle | Tipos de elemento | Descrição |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Formas | Define opções específicas da forma. |
| Controles de recorte | Imagens | Ajuste o tipo de recorte, o deslocamento e a suavização. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Vários elementos selecionados ou um grupo | Agrupa os elementos selecionados ou desagrupa um grupo selecionado. |
| **[!UICONTROL Combine]** | Formas compatíveis | Combina formas selecionadas em uma única forma. |
| **[!UICONTROL Audio replace]** | Áudio e vídeo | Substitui a faixa de áudio por um arquivo da biblioteca de ativos. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Texto | Ajusta a família da fonte, peso, tamanho, alinhamento horizontal e outras configurações avançadas de tipografia. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Imagens e vídeo | Define a imagem de preenchimento ou a fonte de vídeo do elemento. |
| **[!UICONTROL Trim]** | Vídeo e áudio | Abre o modo de corte para definir os pontos inicial e final do clipe. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Vídeo e áudio | Ajusta o nível de áudio. |
| ![Velocidade de reprodução](/help/creative/assets/speed.png "Velocidade de reprodução") ([!UICONTROL Playback speed]) | Vídeo e áudio | Ajusta a taxa de reprodução. |
| ![Cortar](/help/creative/assets/crop.png "Cortar") ([!UICONTROL Crop]) | Todos | Corta o elemento em uma área personalizada. |
| Controles de rotação e inversão | Todos | Girar ou inverter o elemento selecionado. |
| ![Traço](/help/creative/assets/stroke.png "Traço") ([!UICONTROL Stroke]) | Todos | Define a cor e a largura da borda. |
| **[!UICONTROL Text Background]** | Texto | Adiciona uma cor de fundo atrás do texto. |
| **[!UICONTROL Animations]** | Todos | Adiciona ou edita animações de entrada, saída ou loop. |
| **[!UICONTROL Style]** | Todos | Abre um menu com as opções **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** e **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Todos | Adiciona ou edita uma sombra projetada. |
| **[!UICONTROL Opacity]** | Todos | Define o nível de transparência do elemento. |
| **[!UICONTROL Position]** | Todos | Ajusta o tamanho, posição e rotação do elemento numericamente. |
| ![Painel de edição](/help/creative/assets/cs-template-video-editing-panel.png "Painel de edição") | Todos | Abre ou fecha um [painel de edição](#detailed-element-properties-for-video-templates) para o elemento selecionado com mais recursos de edição. |

#### Propriedades detalhadas de elementos para modelos de vídeo

No editor de modelo de vídeo, clique em ![Painel de edição](/help/creative/assets/cs-template-video-editing-panel.png "Painel de edição") na barra de ferramentas para abrir um painel de edição para o elemento selecionado com mais recursos de edição. O painel de edição aparece à esquerda da tela de desenho e é separado do painel [!UICONTROL Layers], que lista as camadas no modelo.

##### Elementos individuais

Quando você seleciona uma única imagem, vídeo, forma ou elemento de texto, o painel de edição mostra as seções aplicáveis abaixo.

| Seção do painel | Ferramenta | Controles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alinhamento e posicionamento da camada | Alinha a camada selecionada à esquerda, no centro horizontal, à direita, na parte superior, no centro vertical ou na parte inferior. O menu de organização altera sua ordem de empilhamento da frente para trás. Esses controles posicionam a própria camada; eles não justificam o texto dentro da camada. |
| | [!UICONTROL Rotate & Flip] | Insira um ângulo de rotação em graus. Use ![Inverter horizontal](/help/creative/assets/cs-template-video-flip.png "Inverter horizontal") para espelhar a camada horizontalmente ou ![Inverter vertical](/help/creative/assets/cs-template-video-flip-vertical.png "Inverter vertical") para espelhá-la verticalmente. |
| | ![Opacidade](/help/creative/assets/cs-template-video-opacity.png "Opacidade") [!UICONTROL Opacity] | Torna a camada selecionada mais ou menos transparente. |
| | ![Modo de mesclagem](/help/creative/assets/cs-template-video-blend-mode.png "Modo de mesclagem") [!UICONTROL Blend Mode] | Altera a forma como as cores da camada selecionada se combinam com as camadas atrás dela. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Abre controles adicionais para a posição e as dimensões da camada. A disponibilidade depende das permissões de transformação da camada selecionada. |
| [!UICONTROL Shape] | ![Opções de forma](/help/creative/assets/cs-template-video-shape-options.png "Opções de forma") [!UICONTROL Shape] e propriedades específicas da forma | Altera a forma e suas propriedades disponíveis, como pontos, lados, diâmetro interno, largura da linha ou raio do canto. Os controles dependem da forma selecionada. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Insere o modo de edição de vetor para editar o caminho da forma, quando disponível. |
| [!UICONTROL Character] | ![Tipo](/help/creative/assets/cs-template-video-typeface.png "Tipo"), ![Estilo do texto](/help/creative/assets/cs-template-video-text-style.png "Estilo do texto"), ![Negrito](/help/creative/assets/cs-template-video-text-bold.png "Negrito") negrito, ![Itálico](/help/creative/assets/cs-template-video-text-italic.png "Itálico") itálico e ![Tamanho da fonte](/help/creative/assets/cs-template-video-font-size.png "Tamanho da fonte") | (Camadas de texto) Altera a família, o estilo e o tamanho da fonte do texto selecionado. |
| | ![Alinhar à esquerda](/help/creative/assets/cs-template-video-text-align-l.png "Alinhar à esquerda") / ![Alinhar ao centro](/help/creative/assets/cs-template-video-text-align-c.png "Alinhar ao centro") / ![Alinhar à direita](/help/creative/assets/cs-template-video-text-align-r.png "Alinhar à direita") Alinhamento de texto | (Camadas de texto) Alinha o texto dentro de seu quadro à esquerda, no centro ou à direita, ou detecta o alinhamento automaticamente. |
| | ![Configurações avançadas de texto](/help/creative/assets/cs-template-video-advanced-text.png "Configurações avançadas de texto") Configurações avançadas de texto | (Camadas de texto) Abre configurações de tipografia adicionais. |
| [!UICONTROL Fill] | ![Preencher](/help/creative/assets/cs-template-video-fill.png "Preencher") controles de preenchimento | Altera a cor, a imagem ou o preenchimento de vídeo da camada selecionada. Os controles refletem o tipo de preenchimento atual e abrem suas configurações. Para texto, altera a cor do texto. |
| [!UICONTROL Stroke] | Controles de Traço ![Traço](/help/creative/assets/cs-template-video-stroke.png "Traço") | Habilita ou desabilita a estrutura de tópicos e altera sua cor, largura, estilo e posicionamento. Controles adicionais são exibidos quando o traçado é ativado. |
| [!UICONTROL Text Background] | ![Plano de fundo do texto](/help/creative/assets/cs-template-video-text-bg.png "Plano de fundo do texto") controles de plano de fundo | (Camadas de texto) Adiciona ou altera o plano de fundo atrás do texto. |
| [!UICONTROL Animations] | ![Animação](/help/creative/assets/cs-template-video-animation.png "Animação") [!UICONTROL Presets] | Abre predefinições de animação para a camada selecionada, incluindo animações de entrada, saída e loop. |
| [!UICONTROL Appearance] | ![Ajustes](/help/creative/assets/cs-template-video-adjustments.png "Ajustes") [!UICONTROL Adjustments] | Altera as propriedades visuais da camada selecionada. |
| | ![Filtro](/help/creative/assets/cs-template-video-filter.png "Filtro") [!UICONTROL Filter] | Aplica um filtro visual à camada selecionada. |
| | ![Efeitos](/help/creative/assets/cs-template-video-effects.png "Efeitos") [!UICONTROL Effect] | Aplica um efeito à camada selecionada. |
| | ![Desfoque](/help/creative/assets/cs-template-video-blur.png "Desfoque") [!UICONTROL Blur] | Aplica um desfoque à camada selecionada. |
| | ![Sombra](/help/creative/assets/cs-template-video-shadow.png "Sombra") [!UICONTROL Shadow] | Adiciona ou altera a sombra da camada selecionada. |

##### Várias seleções e elementos especializados

Quando você seleciona vários elementos, um grupo, um elemento de recorte ou um clipe de áudio, o painel de edição mostra as seções específicas de seleção abaixo. Vários elementos, grupos e recortes também retêm a seção [!UICONTROL Layer].

| Seção do painel | Ferramenta | Controles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alinhamento e posicionamento da camada | Alinha vários elementos selecionados para um grupo. O menu de organização altera a ordem de empilhamento da frente para trás. |
| | [!UICONTROL Rotate & Flip] | Gira ou inverte os elementos ou grupos selecionados. |
| | ![Opacidade](/help/creative/assets/cs-template-video-opacity.png "Opacidade") [!UICONTROL Opacity] | Torna os elementos ou grupos selecionados mais ou menos transparentes. |
| | ![Modo de mesclagem](/help/creative/assets/cs-template-video-blend-mode.png "Modo de mesclagem") [!UICONTROL Blend Mode] | Altera a forma como as cores dos elementos selecionados ou do grupo são combinadas com as camadas atrás deles. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Abre controles para a posição e as dimensões do grupo ou dos elementos selecionados. Os controles disponíveis dependem dos elementos selecionados. |
| [!UICONTROL Selection] | ![Grupo](/help/creative/assets/cs-template-video-group.png "Grupo") Grupo / ![Desagrupar](/help/creative/assets/cs-template-video-ungroup.png "Desagrupar") Desagrupar | Aparece abaixo de [!UICONTROL Layer] para várias camadas selecionadas ou um grupo selecionado. Agrupa as camadas selecionadas para que possam ser gerenciadas juntas ou separa um grupo em camadas individuais. |
| [!UICONTROL Settings] | ![Recorte do recorte](/help/creative/assets/cs-template-video-cutout-clip.png "Recorte do recorte") / ![Sobreposição do recorte](/help/creative/assets/cs-template-video-cutout-overlay.png "Sobreposição do recorte") controles de recorte | (Camadas de recorte) Aparece abaixo de [!UICONTROL Layer]. Seleciona o tipo de recorte e ajusta a suavização de borda e deslocamento. |
| [!UICONTROL Audio Properties] | ![Aparar](/help/creative/assets/cs-template-video-trim.png "Aparar") Aparar, ![Volume](/help/creative/assets/cs-template-video-volume.png "Volume") volume e ![Velocidade de reprodução](/help/creative/assets/cs-template-video-playback-speed.png "Velocidade de reprodução") velocidade de reprodução | (Camadas de áudio) Define os pontos inicial e final do clipe, o nível de áudio e a velocidade de reprodução. |

#### Editar elementos diretamente na tela

##### Exibir modelos de anúncio

| Ação | Descrição |
| --- | --- |
| **[!UICONTROL Replace]** | (Somente elementos de imagem) Abre o painel Imagens para que você possa substituir a imagem por uma de sua biblioteca de ativos. |
| ![Avançar](/help/creative/assets/cs-icon-move-forward.png "Avançar") **[!UICONTROL Move forward]** | Move o elemento um passo à frente na ordem de empilhamento (em direção à frente). |
| ![Retroceder](/help/creative/assets/cs-icon-move-backward.png "Retroceder") **[!UICONTROL Move backward]** | Move o elemento um passo para trás na ordem de empilhamento (para trás). |
| ![Duplicado](/help/creative/assets/cs-icon-duplicate.png "Duplicado") **[!UICONTROL Duplicate]** | Cria uma cópia do elemento. |
| ![Excluir](/help/creative/assets/cs-icon-delete.png "Excluir") **[!UICONTROL Delete]** | Remove o elemento da tela de desenho. |
| Alça de rotação | Clique e arraste a alça acima de um elemento selecionado para girá-lo. Segure **[!UICONTROL Shift]** ao arrastar para ajustar a rotação a incrementos de 15 graus. |

Você também pode clicar e arrastar um elemento selecionado para reposicioná-lo, e clicar e arrastar as alças ao redor dele para redimensioná-lo.

##### Modelos de anúncio de vídeo

| Ação | Descrição |
| --- | --- |
| **[!UICONTROL Edit text]** | (Somente elementos de texto) Alterna para o modo de edição de texto, para que você possa digitar e formatar o texto diretamente na tela de desenho. No modo de edição de texto, um menu secundário fornece **[!UICONTROL Text color]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]** e **[!UICONTROL Text variables]** (espaços reservados para modelos). |
| **[!UICONTROL Replace]** | (Somente elementos de imagem) Abre a biblioteca de ativos para que você possa trocar a imagem. |
| **[!UICONTROL Bring forward]** | Move o elemento um passo à frente na ordem de empilhamento. |
| **[!UICONTROL Send backward]** | Move o elemento uma etapa para trás na ordem de empilhamento. |
| **[!UICONTROL Duplicate]** | Cria uma cópia do elemento. |
| **[!UICONTROL Delete]** | Remove o elemento da tela de desenho. |
| **... >[!UICONTROL Flip horizontal]** | Inverte o elemento horizontalmente 180 graus. |
| **... >[!UICONTROL Flip vertical]** | Inverte o elemento verticalmente 180 graus. |
| **... >[!UICONTROL Copy Element]** | Copia o elemento para a área de transferência da tela. |
| **... >[!UICONTROL Pastes Element]** | Cola o elemento copiado. |

Você também pode clicar e arrastar um elemento selecionado para reposicioná-lo, e clicar e arrastar as alças ao redor dele para redimensioná-lo.

### Controlar tempo e reprodução

Os editores de vídeo e exibição exibem um painel de linha do tempo na parte inferior da tela.

#### Exibir modelos de anúncio

A linha do tempo mostra uma faixa para cada camada na tela de desenho, abrangendo o intervalo de tempo em que a camada fica visível com base no tempo de animação de entrada e saída. Arraste a alça de início ou fim de uma faixa para ajustar o tempo de entrada ou saída, ou arraste uma faixa para reordenar as camadas. Clique na régua ou arraste o indicador de reprodução para mover-se para um ponto no tempo.

A barra de ferramentas da linha do tempo inclui um campo **[!UICONTROL Duration]** (0-60 segundos), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, uma exibição de tempo atual/duração total, um botão de alternância de loop, controles de zoom **[!UICONTROL Timeline Scale]**, um botão **[!UICONTROL Fit View]** e um botão de alternância de recolher/expandir.

#### Modelos de anúncio de vídeo

A linha do tempo mostra todos os clipes de vídeo e áudio no modelo. Use a linha do tempo para revisar como os clipes são organizados no tempo e para aparar os clipes arrastando suas alças de início e fim. Não é possível adicionar um novo clipe diretamente na linha do tempo; em vez disso, adicione-o a partir do painel esquerdo ou da tela e ele aparecerá como um clipe na linha do tempo.

### Gerenciar camadas

O painel [!UICONTROL Layers] no lado direito da tela lista todos os elementos no modelo e permite gerenciar a ordem, a visibilidade e as propriedades. Para modelos de exibição, clique em **[!UICONTROL Open Layers]** na barra de ferramentas da tela para abri-la. Para modelos de vídeo, o painel é aberto por padrão.

Clique em qualquer camada para selecionar o elemento correspondente na tela de desenho.

**Guias (exibir somente modelos de anúncios)**

Os modelos de exibição têm duas guias na parte superior do painel [!UICONTROL Layers]:

* **[!UICONTROL Dynamic]** — Lista apenas as camadas que podem ser trocadas durante a geração do anúncio, como imagens e texto que o agente de IA pode substituir. Essa é a exibição padrão para gerar variações de anúncios.
* **[!UICONTROL All]** — Mostra a hierarquia completa da camada para o modelo, incluindo contêineres estruturais. Use essa exibição para inspecionar ou reorganizar como os elementos são aninhados.

Os modelos de vídeo mostram todas as camadas em uma única lista sem guias.

**Ações por camada**

Mantenha o cursor sobre uma camada para ver as ações a seguir.

| Ação | Descrição |
| --- | --- |
| ![Renomear camada](/help/creative/assets/edit.png "Renomear camada") **[!UICONTROL Rename layer]** | Permite inserir um novo nome de camada no painel. |
| ![Camada de bloqueio](/help/creative/assets/cs-icon-lock.png "Camada de bloqueio") **[!UICONTROL Lock layer]** / ![Desbloquear camada](/help/creative/assets/cs-icon-unlock.png "Desbloquear camada") **[!UICONTROL Unlock layer]** | Impede ou permite que a camada seja movida, editada ou reordenada. |
| ![Ocultar camada](/help/creative/assets/cs-icon-hidden.png "Ocultar camada") **[!UICONTROL Hide layer]** / ![Mostrar camada](/help/creative/assets/cs-icon-visible.png "Mostrar camada") **[!UICONTROL Show layer]** | Oculta ou mostra a camada na tela de desenho. As camadas ocultas são preservadas no modelo, mas não aparecem quando ele é renderizado. |
| ![Arrastar para reordenar](/help/creative/assets/cs-icon-drag.png "Arrastar para reordenar") Arrastar para reordenar | (Exibir somente modelos de anúncio) Arraste o ícone de reordenação para alterar a posição da camada na ordem de empilhamento. A camada deve ser desbloqueada para reordená-la. |

**Rodapé do painel**

| Ação | Descrição |
| --- | --- |
| ![Duplicar camada selecionada](/help/creative/assets/cs-icon-duplicate.png "Duplicar camada selecionada") **[!UICONTROL Duplicate selected layer]** | Cria uma cópia da camada selecionada. |
| ![Excluir camada selecionada](/help/creative/assets/cs-icon-delete.png "Excluir camada selecionada") **[!UICONTROL Delete selected layer]** | Exclui a camada selecionada. |
| **[!UICONTROL Group selected layers]** (somente modelos de vídeo) | Agrupa duas ou mais camadas selecionadas em um único grupo. Aparece somente quando duas ou mais camadas são selecionadas. É possível desagrupar camadas agrupadas ou remover camadas individuais do grupo usando os controles na linha do grupo. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

>[!MORELIKETHIS]
>
>* [Sobre o Creative Studio no Advertising Creative](creative-studio-about.md)
>* [Gerenciar ativos no Creative Studio](creative-studio-manage-assets.md)
>* [Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gerenciar criações dinâmicas no Creative Studio](creative-studio-manage-dynamic-ads.md)
