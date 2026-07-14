---
title: Gerenciar anúncios padrão no Creative Studio
description: Saiba como criar, editar, duplicar, baixar e excluir anúncios de exibição padrão na biblioteca de criação do Creative Studio.
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# Gerenciar anúncios padrão em [!UICONTROL Creative Studio]

*recurso do Beta*

A guia **[!UICONTROL Creatives]** em [!UICONTROL Creative Studio] é sua biblioteca de anúncios de exibição padrão gerados de modelos. Aqui é possível criar anúncios usando o [!UICONTROL Ad Variations Generator], editar anúncios salvos, gerar novas variações de um anúncio existente, exibir o log de alterações, duplicar, baixar e excluir.

## Criar anúncios padrão {#create-standard-ads}

Use o [!UICONTROL Ad Variations Generator] para gerar conteúdo de anúncio de exibição a partir de um modelo. O assistente de IA gera e refina títulos, CTAs, imagens, cores e muito mais, e pode criar novas variantes de tamanho em uma única sessão.

>[!NOTE]
>
>A geração de anúncios padrão atualmente suporta apenas modelos de anúncios de exibição. Os modelos de anúncio de vídeo não estão disponíveis como ponto de partida, na guia **[!UICONTROL Creatives]** ou na guia **[!UICONTROL Templates]**.

### Pré-requisitos

Pelo menos um modelo de anúncio de exibição deve existir na biblioteca de modelos.

### Gerar anúncios padrão

1. Abra o [!UICONTROL Ad Variations Generator] de qualquer uma das seguintes maneiras:

   * **Na guia [!UICONTROL Creatives]:**

      1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

      1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL Generate]** no cartão de ação rápida **[!UICONTROL Generate standard ads from templates]**.

      1. Na caixa de diálogo de seleção de modelo, clique em um modelo para selecioná-lo, depois clique em **[!UICONTROL Use this template]**.

   * (Exibir somente anúncios) **Na guia [!UICONTROL Templates]:**

      1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

      1. Clique na guia **[!UICONTROL Templates]**.

      1. Mantenha o cursor sobre um cartão de modelo e clique em **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   O [!UICONTROL Ad Variations Generator] se abre. A tela mostra a seção **[!UICONTROL Template Sizes]** com os formatos de anúncio disponíveis do modelo e uma seção **[!UICONTROL Ad Concepts]** onde o conteúdo gerado será exibido.

1. (Opcional) Para aplicar um perfil de marca aos anúncios, selecione um **[!UICONTROL Brand Profile]** na barra de ferramentas da tela de desenho.

   O assistente de IA usa o logotipo da sua marca, a paleta de cores, as diretrizes de voz, os padrões de imagem e as diretrizes de canal ao gerar o conteúdo.

1. Criar variações de anúncios usando o [!UICONTROL AI Assistant]:

   1. No campo **[!UICONTROL Ask AI to generate ad variations…]**, digite uma solicitação e pressione **[!UICONTROL Enter]**, ou clique em um dos prompts em destaque:

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      A IA gera resultados na tela e os organiza em *conceitos*, cada um representando uma variação de conteúdo distinta. O contador de conceito na seção **[!UICONTROL Ad Concepts]** rastreia quantos conceitos existem (por exemplo, **(2/10)**). São permitidos até 10 conceitos por sessão.

   1. Continue a refinar enviando mensagens de acompanhamento. Exemplos:

      * &quot;Torne toda a cópia mais divertida e menos corporativa.&quot;
      * &quot;Altere o logotipo para a versão branca.&quot;
      * &quot;Defina a CTA como &#39;Comprar Agora&#39; em todos os conceitos.&quot;
      * &quot;Redimensione este anúncio para todos os 6 tamanhos de tela padrão IAB.&quot;
      * &quot;Conceda-me 3 conceitos de título diferentes com uma imagem de plano de fundo correspondente para cada um.&quot;

      >[!NOTE]
      >
      >O assistente de IA pode gerar e modificar textos (títulos, subtítulos, CTAs, cópia do corpo), trocar imagens de fundo, aplicar cores de marca, alternar versões de logotipo e criar novos modelos de tamanho. Não é possível alterar a estrutura do modelo: posições do elemento, layout, espaçamento, preenchimento, família da fonte, tamanho da fonte ou bordas. Faça alterações estruturais no editor de modelos antes de iniciar a sessão. Consulte [Editar um modelo](creative-studio-manage-templates.md#edit-template).

   1. (Opcional) Para incluir uma referência visual em uma solicitação, clique no botão **[!UICONTROL +]** na área de entrada do chat. No diálogo **[!UICONTROL Select from Asset Library]**:

      * Para usar um ativo na biblioteca de ativos, clique no ativo e, em seguida, clique em **[!UICONTROL Add to chat]**. Envie sua mensagem para incluir o ativo como contexto.

      * Para carregar um ou mais ativos, clique em **[!UICONTROL Upload Assets]** e selecione os arquivos no dispositivo ou na rede.

1. (Opcional) Use a barra de ferramentas da tela de desenho para revisar os anúncios gerados:

   * **[!UICONTROL Brand]:** Selecione ou altere o perfil de marca aplicado à sessão.
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]:** Ajuste o nível de zoom da tela.
   * **[!UICONTROL Fit to screen]:** Redefinir o modo de exibição para mostrar todos os tamanhos.
   * **[!UICONTROL Replay animations]:** Reproduzir animações de modelo.

   Quando a IA cria um novo tamanho, **[!UICONTROL Adjust]**, **[!UICONTROL Keep]**, e controles de exclusão são exibidos no novo cartão de tamanho. Clique em **[!UICONTROL Keep]** para aceitar o tamanho como está, clique em **[!UICONTROL Adjust]** para abrir o modelo no editor de exibição, onde você pode fazer alterações estruturais e, em seguida, clique em **[!UICONTROL Update Ad Format]** para salvar ou clique no ícone excluir para remover o novo tamanho.

1. (Opcional) Gerencie conceitos e variações:

   * Para gerenciar um conceito, mantenha o cursor sobre o rótulo do conceito (por exemplo, **[!UICONTROL Concept 3]**), clique em **[!UICONTROL ...]** e selecione uma opção:

      * **[!UICONTROL Add to chat]:** Faz referência ao conceito no próximo prompt.
      * **[!UICONTROL Delete]:** Remove o conceito.

   * Para gerenciar uma variação individual, mantenha o cursor sobre o cartão de variação e clique em **[!UICONTROL ...]** e selecione uma opção:

      * **[!UICONTROL Add to Chat]:** Faz referência à variação no próximo prompt. Você também pode clicar diretamente no corpo do cartão de variação para alternar a menção.
      * **[!UICONTROL Edit Data]:** Abre uma caixa de diálogo onde você pode atualizar a variação **[!UICONTROL Name]** e a URL de click-through para cada marca de clique definida no modelo. Clique em **[!UICONTROL Save]** para aplicar.
      * **[!UICONTROL Delete]:** Remove a variação.

1. Quando estiver satisfeito com os conceitos gerados, clique em **[!UICONTROL Save Standard Ads]** no cabeçalho.

   O botão fica desativado até que exista pelo menos um conceito.

1. Na caixa de diálogo **[!UICONTROL Save Standard Ads]**, especifique as configurações a seguir e clique em **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** (Obrigatório) O anunciante no qual salvar os elementos de criação.

   **[!UICONTROL Creative Library]:** (Obrigatório) A biblioteca criativa na qual salvar as criações. O seletor de biblioteca é ativado depois de selecionar um anunciante.

   **[!UICONTROL Attach to Bundles]:** (Opcional) Quando habilitado, as criações salvas são anexadas a um ou mais conjuntos. Para cada variação de anúncio, selecione um pacote ou insira um novo nome de pacote.

   **\[Configurações para cada anúncio\]:** Para cada variação de anúncio, você pode exibir e, opcionalmente, alterar os **[!UICONTROL Name],** **[!UICONTROL Language],** e **[!UICONTROL click URL].**

## Editar um anúncio padrão {#edit-standard-ad}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Um editor de tela cheia é aberto com uma visualização de anúncio ao vivo à esquerda e um painel de configurações à direita.

1. Edite as configurações de anúncio usando as guias **[!UICONTROL Details]** e **[!UICONTROL Attributes]**:

   Guia **[!UICONTROL Details]**:

   * **[!UICONTROL Creative Name]:** (Obrigatório) O nome de exibição do criativo.
   * **[!UICONTROL Language]:** (Obrigatório) O idioma do conteúdo do anúncio.
   * **[!UICONTROL Creative Size]:** (Somente leitura) As dimensões de anúncio.
   * **Marcas de clique:** Se o modelo definir marcas de clique, cada marca de clique aparecerá como um campo obrigatório rotulado com o nome da marca. Insira o URL de destino de click-through para cada tag.
   * **[!UICONTROL Label]:** Rótulos (opcionais) para organizar criações. Selecione rótulos existentes ou insira uma nova marca e clique em **[!UICONTROL Add tag].**

   Guia **[!UICONTROL Attributes]**:

   A pré-visualização ao vivo é atualizada em tempo real à medida que você edita. A guia **[!UICONTROL Attributes]** não estará disponível enquanto a visualização estiver sendo carregada.

   * **Atributos de texto:** Insira o valor do texto para cada camada de texto editável definida no modelo.
   * **Atributos de imagem:** mostra uma miniatura da imagem atual. Clique em **[!UICONTROL Replace Image]** para carregar um substituto (PNG, JPEG, GIF, WebP ou SVG).

1. Clique em **[!UICONTROL Update Creative]**.

## Gerar variações de anúncios para um anúncio padrão {#generate-ad-variations}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   O [!UICONTROL Ad Variations Generator] abre com o anúncio selecionado pré-carregado.

1. Use a interface de bate-papo do AI para gerar e refinar variações adicionais. Consulte &quot;[Criar anúncios padrão](#create-standard-ads)&quot; para obter o fluxo de trabalho completo.

## Duplicar um anúncio padrão {#duplicate-standard-ad}

Duplique um anúncio padrão para adicionar um novo criativo com as mesmas configurações à biblioteca. Posteriormente, é possível renomear o novo criativo e editar as configurações, conforme necessário.

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   O nome do novo criativo é `<original name> (copy)`.

## Exibir o log de alterações para um anúncio padrão {#view-change-log}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   Uma caixa de diálogo é aberta, mostrando uma tabela de alterações do anúncio.

## Baixar um anúncio padrão {#download-standard-ad}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   O criativo é baixado de acordo com o procedimento normal do navegador.

## Excluir um anúncio padrão {#delete-standard-ad}

>[!NOTE]
>
>Essa ação não pode ser desfeita.

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Na guia **[!UICONTROL Creatives]**, mantenha o cursor sobre o cartão criativo e clique em **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre o Creative Studio no Advertising Creative](creative-studio-about.md)
>* [Gerenciar criações dinâmicas no Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Gerenciar modelos no Creative Studio](creative-studio-manage-templates.md)
>* [Gerenciar perfis de marca no Advertising Creative](/help/creative/brands/brand-manage.md)

