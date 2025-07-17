---
title: Exportar e implementar uma tag de experiência de anúncio para uma experiência ao vivo
description: Saiba como exportar uma tag de experiência de anúncio e, opcionalmente, carregá-la em uma campanha do Advertising DSP.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: e79becc860143b749ec96134e7b224649686c672
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Exportar e implementar uma tag de experiência de anúncio para uma experiência ao vivo

*Beta fechado*

Quando uma marca de anúncio para um tamanho criativo ou duração de vídeo específico estiver disponível para uma experiência [em tempo real](experience-about.md#experience-statuses), você poderá gerar e copiar a marca nos formatos JavaScript, iframe e vídeo para implementação no Advertising DSP ou em outros DSPs. As tags da DSP incluem todas as macros necessárias para o DSP.

Os anunciantes com o Advertising DSP podem, opcionalmente, fazer upload de tags diretamente em uma campanha do Advertising DSP como anúncios com o tipo de anúncio &quot;exibição padrão&quot; ou &quot;vídeo universal&quot;.

>[!NOTE]
>
>* Quando você cria uma experiência com o direcionamento de árvore decisória, o [!DNL Creative] cria automaticamente uma tag de anúncio para cada tamanho criativo aplicável (criação não relacionada a vídeo) ou duração do vídeo (criação de vídeo).
>* Ao criar uma experiência sem definição de metas da árvore decisória, você deve [criar manualmente uma tag de anúncio](experience-tag-create-manually.md) para cada tamanho criativo aplicável (criações que não sejam de vídeo) ou duração do vídeo (criações de vídeo).
>* As tags de experiência são dinâmicas. Não é necessário atualizar as tags se você editar uma experiência.
>* Certifique-se de que as campanhas em que você implementará uma experiência de anúncio incluam direcionamento compatível com a experiência. O comportamento hierárquico do direcionamento pode variar de acordo com a DSP. No Advertising DSP, o direcionamento no nível do anúncio é aplicado sobre o direcionamento no nível do posicionamento (não em vez dele).

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**.

1. Mantenha o cursor sobre a linha da marca de anúncio aplicável e clique em ![Exportar marcas de anúncio](/help/creative/assets/export.png "Exportar marcas de anúncio") **[!UICONTROL Export ad tags]** ou **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Para experiências de anúncio de vídeo padrão, aguarde até que a coluna [!UICONTROL Tag Status] mostre &quot;[!UICONTROL Ready]&quot;, que indica que todos os vídeos na experiência foram transcodificados. Todas as criações de vídeo são transcodificadas automaticamente pelo DSP, mas você pode [aplicar transcodificação para uma DSP](experience-tag-video-transcoding.md) diferente a qualquer marca de experiência de vídeo e anúncio.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Opcional) Na guia [!UICONTROL Macros], especifique até cinco macros personalizadas para serem incluídas na tag. Para cada macro a ser incluída:

   1. Marque uma caixa de seleção.<!-- Explain more -->

   1. Insira a macro personalizada.<!-- Explain more -->

1. Clique em **[!UICONTROL Next]** no canto superior direito ou clique em **[!UICONTROL Generate ad tags]** no menu esquerdo.

1. Selecione o tipo de tag:

   * (Experiências não relacionadas a vídeo) ** *JavaScript<!-- sic -->* ** ou ** *IFRAME* ** <!-- sic -->.

   * (Experiências de vídeo) ** *Vídeo* **.

1. Na lista [!UICONTROL Destinations], selecione onde você criará anúncios para a experiência.

   * *Genérico:* Para anúncios criados em outros DSPs. **Observação:** talvez seja necessário incluir manualmente [macros adicionais](/help/creative/creative-macros.md), conforme necessário.

   * *Adobe AdCloud:* Para anúncios criados no Advertising DSP.

   * *Google CM360:* Para anúncios criados em [!DNL Google Campaign Manager 360]. **Observação:** talvez seja necessário incluir manualmente [macros adicionais](/help/creative/creative-macros.md), conforme necessário.

1. Clique em **[!UICONTROL Generate tags]**.

1. Copie ou baixe as tags:

   * Para copiar uma marca para um único tamanho de anúncio (anúncios que não sejam de vídeo) ou duração (anúncios de vídeo), expanda a linha da marca, mantenha o cursor sobre a linha e clique em ![Copiar](/help/creative/assets/copy.png "Copiar") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

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
>* [Personalizar opções de transcodificação para uma marca de experiência de anúncio de vídeo](experience-tag-video-transcoding.md)
