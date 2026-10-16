---
title: Gerar um modelo de anúncio a partir de uma imagem usando IA
description: Saiba como usar a IA no Creative Studio para converter uma imagem de anúncio de exibição estática existente em um modelo de anúncio editável.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# Gerar um modelo de anúncio a partir de uma imagem usando IA

*recurso do Beta*

Use a IA em [!UICONTROL Creative Studio] para converter uma imagem de anúncio de exibição estática existente em um modelo de anúncio de exibição editável. Revise o modelo gerado, solicite alterações usando a linguagem natural e abra o editor de modelo para fazer alterações manuais e salvar o modelo.

## Antes de começar

Você precisa de um anúncio de imagem estática existente em uma Biblioteca da Creative. Esse fluxo de trabalho seleciona anúncios das bibliotecas; ele não carrega uma nova imagem diretamente na caixa de diálogo de geração.

## Gerar e revisar o modelo {#template-generate}

1. No menu principal, clique em **[!UICONTROL Creative Studio]**.

1. Clique na guia **[!UICONTROL Templates]**.

1. (Opcional) Selecione um anunciante na lista de anunciante na parte superior da página para exibir as bibliotecas desse anunciante.

1. Na caixa **[!UICONTROL Use AI to Generate a New Display Ad Template]**, clique em **[!UICONTROL Generate]**.

1. Na caixa de diálogo **[!UICONTROL Generate New Ad Template]**, selecione **[!UICONTROL Generate from Existing Standard Ad Image]** se ainda não estiver selecionado.

1. Selecione a biblioteca que contém o anúncio de imagem na lista **[!UICONTROL Ad Library]**.

1. Mantenha o cursor sobre o cartão de anúncio da imagem e clique em **[!UICONTROL Use this Standard Ad]**.

   A geração começa automaticamente, usando a largura e a altura do anúncio selecionado.

1. Aguarde a conclusão da geração e revise a visualização do modelo e o painel **[!UICONTROL Layers]**, quando disponíveis.

   Verifique o texto, as imagens e o layout antes de usar o modelo. As camadas mostradas aqui são para revisão; faça alterações manuais no editor de modelo.

1. (Opcional) Solicitar alterações no modelo gerado:

   1. No campo **[!UICONTROL Ask the AI for any changes]**, descreva as alterações desejadas. Por exemplo, digite `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Clique em **[!UICONTROL Regenerate]**.

   1. Revise a visualização atualizada. Repita conforme necessário.

1. Quando estiver pronto para continuar, clique em **[!UICONTROL Use this Ad Template]**.

   O modelo gerado é aberto no editor de modelo de exibição.

## Editar e salvar o modelo {#template-save}

1. No editor de modelos, revise os elementos gerados e faça as alterações restantes usando os [controles do editor de modelos](creative-studio-manage-templates.md#template-controls).

1. Clique em **[!UICONTROL Save]**.

1. Na caixa de diálogo **[!UICONTROL Update Template]**, insira ou atualize a **[!UICONTROL Template name]**, selecione a **[!UICONTROL Advertiser]** e, opcionalmente, adicione marcas.

1. Clique em **[!UICONTROL Update]** para salvar o modelo e retornar à exibição **[!UICONTROL Templates]**.

   Para salvar uma cópia separada, clique em **[!UICONTROL Save As New]**.

Você pode usar o modelo para [gerar variações de anúncios](creative-studio-manage-templates.md#ad-variations-generate).

## Se você não puder gerar um template {#troubleshooting}

* **Não há bibliotecas ou anúncios de imagem listados:** Verifique o anunciante selecionado e **[!UICONTROL Ad Library]**. Se a biblioteca não tiver imagens de anúncio padrão, selecione outra biblioteca contendo um anúncio de imagem estática existente.

* **A geração falhou ou a imagem não pode ser convertida:** Revise a mensagem exibida, clique em **[!UICONTROL Back to library]** e selecione um anúncio de imagem para tentar novamente.

>[!MORELIKETHIS]
>
>* [Gerenciar modelos de anúncios no Creative Studio](creative-studio-manage-templates.md)
>* [Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)