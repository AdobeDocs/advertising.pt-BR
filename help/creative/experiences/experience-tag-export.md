---
title: Exportar e implementar uma tag de experiência de anúncio para uma experiência ao vivo
description: Saiba como exportar uma tag de experiência de anúncio e, opcionalmente, carregá-la em uma campanha do Advertising DSP.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: c05c5d22f4763cd6c1425b5ab3b0bf11b78b0aee
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Exportar e implementar uma tag de experiência de anúncio para uma experiência ao vivo

*Beta fechado*

Quando uma marca de anúncio para um tamanho criativo específico estiver disponível para uma experiência do [live](experience-about.md#experience-statuses), você poderá gerar e copiar a marca nos formatos JavaScript e iframe para implementação no Advertising DSP ou em outros DSPs. As tags da DSP incluem todas as macros necessárias para o DSP.

Como opção, os anunciantes com o Advertising DSP podem fazer upload de tags diretamente em uma campanha do Advertising DSP como anúncios.

>[!NOTE]
>
>* Ao criar uma experiência com direcionamento de árvore decisória, o [!DNL Creative] cria automaticamente uma tag de anúncio para cada tamanho criativo aplicável.
>* Ao criar uma experiência sem definição de metas da árvore decisória, você deve [criar manualmente uma tag de anúncio](experience-tag-create-manually.md) para cada tamanho criativo aplicável.
>* As tags de experiência são dinâmicas. Não é necessário atualizar as tags se você editar uma experiência.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**

1. Mantenha o cursor sobre a linha da marca de anúncio aplicável e clique em ![Exportar marcas de anúncio](/help/creative/assets/export.png "Exportar marcas de anúncio") **[!UICONTROL Export ad tags]** ou **[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Opcional) Na guia [!UICONTROL Macros], especifique até cinco macros personalizadas para serem incluídas na tag. Para cada macro a ser incluída:

   1. Marque uma caixa de seleção.<!-- Explain more -->

   1. Insira a macro personalizada.<!-- Explain more -->

1. Clique em **[!UICONTROL Next]** no canto superior direito ou clique em **[!UICONTROL Generate ad tags]** no menu esquerdo.

1. Selecione o tipo de marca: ** *JavaScript<!-- sic -->* **&#x200B; ou &#x200B;** *IFRAME* ** <!-- sic -->.

1. Na lista [!UICONTROL Destinations], selecione onde você criará anúncios para a experiência.

   * *Genérico:* Para anúncios criados em outros DSPs. **Observação:** talvez seja necessário incluir manualmente [macros adicionais](/help/creative/creative-macros.md), conforme necessário.

   * *Adobe Advertising:* Para anúncios criados no Advertising DSP.

   * *DCM do Google:* Para anúncios criados em [!DNL Google Campaign Manager 360]. **Observação:** talvez seja necessário incluir manualmente [macros adicionais](/help/creative/creative-macros.md), conforme necessário.

1. Clique em **[!UICONTROL Generate tags]**.

1. Copie ou baixe as tags:

   * Para copiar uma marca para um único tamanho de anúncio, expanda a linha de marcas, mantenha o cursor sobre a linha e clique em ![Copiar](/help/creative/assets/copy.png "Copiar") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Para baixar todas as marcas geradas como um arquivo no local de download padrão do seu navegador, clique em ![Baixar marcas](/help/creative/assets/download.png "Baixar marcas").

   É possível abrir o arquivo em um editor de texto para copiar cada tag. Para marcas JavaScript, a marca está entre `<script></script>` e `<noscript></noscript>`. Para marcas iframe, a marca está entre `<iframe></iframe>` marcas.

1. Implemente as tags para a DSP relevante:

   * Para DSPs diferentes do Advertising DSP, forneça as tags a quem quer que crie os anúncios na DSP.

   * Para o Advertising DSP:

      1. Clique em **[!UICONTROL Next]** no canto superior direito ou clique em **[!UICONTROL DSP link]** no menu esquerdo.

      1. Selecione a campanha na qual deseja fazer upload da tag de publicidade.

      1. Clique em **[!UICONTROL Assign Tags]**.

         O DSP abre para a visualização [!UICONTROL Ads] da campanha selecionada.

      1. Na exibição [!UICONTROL Create ads], revise as marcas de anúncio, selecione cada marca para a qual deseja criar um anúncio e clique em **[!UICONTROL Create]**.

         A exibição [!UICONTROL Ads] agora inclui os novos anúncios, que têm os mesmos nomes que as marcas de anúncio em [!DNL Creative]. Você pode [anexar os anúncios a qualquer posicionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) na campanha.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Crie manualmente uma marca de anúncio para um tamanho criativo aplicável](experience-tag-create-manually.md)
>* [Atribuir criações a uma marca de anúncio para experiências sem direcionamento](experience-tag-assign-creatives.md)
>* [Renomear uma marca de anúncio](experience-tag-rename.md)
