---
title: Gerar variações de criações flexíveis do HTML5
description: Saiba como gerar e salvar variações assistidas por IA de criações flexíveis do HTML5 de uma biblioteca criativa.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# Gerar variações de criações flexíveis do HTML5

Use o [!UICONTROL Ad Variations Generator] para criar novas variações de um criativo flexível do HTML5. O assistente de IA gera e refina títulos, CTAs, imagens, cores e muito mais, e pode criar novas variantes de tamanho em uma única sessão. Salve as variações resultantes como novos anúncios padrão na biblioteca criativa.

>[!NOTE]
>
>Você também pode gerar variações de anúncios de [!UICONTROL Creative Studio]. Ambos os pontos de entrada abrem o mesmo [!UICONTROL Ad Variations Generator]. Consulte &quot;[Gerar variações de anúncios para um anúncio padrão no Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)&quot; para o outro ponto de entrada.

## Disponibilidade {#availability}

A ação **[!UICONTROL Generate Variations]** está disponível para criações HTML5 flexíveis, incluindo aquelas baseadas em modelos de sistema, na nova interface do usuário [!UICONTROL Creative Libraries]. Ele não está disponível para outros tipos criativos, incluindo criativos dinâmicos.

A ação é desativada quando o criativo não tem a referência interna do modelo de anúncio principal exigida pelo gerador. Essa referência não é uma configuração que você pode editar; o carregamento ou a substituição de um arquivo na guia **[!UICONTROL Template]** do criativo não a define explicitamente.

## Abra o Gerador de variações de anúncios {#open-generator}

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Abra a biblioteca de uma das seguintes maneiras:

   * Clique no nome da biblioteca.
   * Ao lado do nome da biblioteca, clique em **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Na guia **[!UICONTROL Creatives]**, clique em **[!UICONTROL ...]** ao lado do nome criativo flexível do HTML5 e clique em **[!UICONTROL Generate Variations]**.

   O [!UICONTROL Ad Variations Generator] é aberto com o conteúdo do criativo selecionado. A tela mostra a seção **[!UICONTROL Template Sizes]** com os formatos de anúncio disponíveis do modelo e uma seção **[!UICONTROL Ad Concepts]** onde o conteúdo gerado será exibido.

## Gerar e refinar variações {#generate-variations}

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
      >O assistente de IA pode gerar e modificar textos (títulos, subtítulos, CTAs, cópia do corpo), trocar imagens de fundo, aplicar cores de marca, alternar versões de logotipo e criar novos modelos de tamanho. Não é possível alterar a estrutura do modelo: posições do elemento, layout, espaçamento, preenchimento, família da fonte, tamanho da fonte ou bordas. Faça alterações estruturais no editor de modelos antes de iniciar a sessão. Consulte [Editar um modelo](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

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

## Salvar as variações {#save-variations}

1. Quando estiver satisfeito com os conceitos gerados, clique em **[!UICONTROL Save Standard Ads]** no cabeçalho.

   O botão fica desativado até que exista pelo menos um conceito.

1. Na caixa de diálogo **[!UICONTROL Save Standard Ads]**, revise as configurações a seguir e clique em **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** O anunciante associado à biblioteca de criação de origem. Você não pode alterar esse valor.

   **[!UICONTROL Creative Library]:** A biblioteca de criação de origem na qual os novos anúncios são salvos. Você não pode alterar esse valor.

   **[!UICONTROL Attach to Bundles]:** (Opcional) Quando habilitado, as criações salvas são anexadas a um ou mais conjuntos. Para cada variação de anúncio, selecione um pacote ou insira um novo nome de pacote.

   **\[Configurações para cada anúncio\]:** Para cada variação de anúncio, você pode exibir e, opcionalmente, alterar o **[!UICONTROL Name]**, **[!UICONTROL Language]** e a URL de click-through para cada marca de clique.

   Você retorna à biblioteca criativa.

>[!MORELIKETHIS]
>
>* [Editar criações padrão](creative-edit-standard.md)
>* [Gerenciar anúncios padrão no Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Gerenciar perfis de marca no Advertising Creative](/help/creative/brands/brand-manage.md)
>* [Metadados C2PA em [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
