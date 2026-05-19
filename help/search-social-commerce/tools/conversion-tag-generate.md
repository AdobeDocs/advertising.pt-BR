---
title: Gerar e implementar uma tag de rastreamento de conversão do Adobe Advertising
description: Saiba como criar uma tag de conversão do Adobe Advertising para rastrear seus eventos de conversão.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Gerar e implementar uma tag de rastreamento de conversão do Adobe Advertising

*Somente anunciantes com rastreamento de conversão do Adobe Advertising*

Crie uma tag de conversão separada para cada conjunto de métricas que você deseja rastrear. Você pode gerar tags na Search, Social e Commerce ou usando tags na Adobe Experience Platform (anteriormente conhecida como Adobe Experience Platform Launch) com a extensão do Adobe Advertising.

<!--

## (New UI) Generate and implement a conversion-tracking tag within Search, Social, & Commerce

>[!NOTE]
>
>This feature doesn't add image tags or [!DNL JavaScript] tags to the advertiser's webpages. Provide the tags to the advertiser or agency with a list of webpages on which to insert each. The tags must be added according to the advertiser's normal procedure for updating webpages.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. In the main toolbar, click **[!UICONTROL Conversion Tag]**.

1. Specify the [conversion tag settings](#conversion-tag-settings).

1. Click **[!UICONTROL Generate]**.
   
1. Click **[!UICONTROL Copy]** to copy the tag to your clipboard. Give the tag to the advertiser or agency to implement.

>[!NOTE]
>
>Each metric in the new conversion tag is automatically listed in [!UICONTROL Admin] > [!UICONTROL Conversions], even if it isn't implemented or the webpages that it's on haven't received any clicks. This behavior is different from the behavior of metrics in tags created manually or elsewhere, which aren't listed in [!UICONTROL Admin] > [!UICONTROL Conversions] until one of the webpages that it's on has received a click. In all cases, however, each metric is initially excluded from portfolio objectives, reports, and views until you explicitly make them available. Before you add the metrics to portfolio objectives, consider first making the metrics available and adding them to reports to verify when they receive clicks.

### Adobe Advertising conversion tag settings {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** The type of tag to create:

* *[!UICONTROL JavaScript]:* To create a JavaScript tag.

* *[!UICONTROL Image]:* To create an image tag to display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the webpage. The best practice is to use image tags only when the site has a policy against using JavaScript tags.

For more information about the differences between the tag types, see "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

**[!UICONTROL Include unique transaction IDs]:** (Optional) Includes a transaction ID property (`ev_transid=<transid>`) in the tag. The option is selected by default.

When you select this option, the advertiser must generate a unique value for `<transid>` (for example, an actual order ID) when the transaction is complete and pass it back to Adobe Advertising, such as `ev_transid=0123`. Adobe Advertising uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID can't contain ampersand symbols (`&`), which are reserved as parameter separators. The transaction ID is included in [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), which you can use to validate data within Search, Social, & Commerce with the advertiser's data.

If the data doesn't include a unique ID per transaction, then Adobe Advertising still generates one based on transaction time.

>[!NOTE]
>
>If you send [transaction ID feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) with conversion data for offline conversions, then you must submit the transaction ID (`ev_transid`) for the online part of the transaction in the feed data for offline parts of the transaction.

**[!UICONTROL JS Version]:** ([!DNL JavaScript] tags only) Which version of the [!DNL JavaScript] tag to create: *[!UICONTROL v2]* (the default) or *[!UICONTROL v3]*.

**[!UICONTROL Security]:** The security protocol for your website create: *[!UICONTROL Standard]* (for websites that use HTTP) or *[!UICONTROL Secure]* (for websites that use HTTPs).

**[!UICONTROL Properties]:** One or more conversion metrics to be tracked when an end user views a page containing the conversion tag. To add a metric to the list, enter the metric name in the "[!UICONTROL Property name]" field and click **[!UICONTROL Add]**.

When multiple metrics are tracked, they're joined by an ampersand (`&`) in the tag, such as `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrics added to this list aren't saved anywhere or integrated with the client's [!UICONTROL Conversions] list on the [!UICONTROL Admin] tab. However, metrics are added to the client's [!UICONTROL Conversions] list automatically once Adobe Advertising actually gathers data for a metric, which happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page.

-->
## &#x200B;<!-- (Legacy UI) --> Gerar e implementar uma tag de rastreamento de conversão no Search, Social e Commerce

>[!NOTE]
>
>Este recurso não adiciona marcas de imagem nem [!DNL JavaScript] marcas às páginas da Web do anunciante. Forneça as tags ao anunciante ou à agência uma lista de páginas da Web nas quais inserir cada uma. As tags devem ser adicionadas de acordo com o procedimento normal do anunciante para atualização de páginas da Web.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique as [configurações da marca de conversão](#conversion-tag-settings).

1. Gere a tag:

   * Se o site usar HTTP, clique em **[!UICONTROL Generate Conversion Tag]**.

   * Se o site for executado em um servidor seguro (HTTPS), clique em **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie a tag da caixa de diálogo e cole-a nas páginas da Web apropriadas, conforme necessário.

>[!NOTE]
>
>Cada métrica na nova marca de conversão é listada automaticamente em [!UICONTROL Admin] > [!UICONTROL Conversions], mesmo que não esteja implementada ou que as páginas da Web em que está não tenham recebido nenhum clique. Esse comportamento é diferente do comportamento das métricas em tags criadas manualmente ou em outro lugar, que não são listadas em [!UICONTROL Admin] > [!UICONTROL Conversions] até que uma das páginas da Web em que está tenha recebido um clique. No entanto, em todos os casos, cada métrica é inicialmente excluída dos objetivos de portfólio, relatórios e exibições até que você as disponibilize explicitamente. No entanto, antes de adicionar as métricas aos objetivos do portfólio, considere primeiro disponibilizar as métricas e adicioná-las aos relatórios para verificar quando recebem cliques.

### Configurações da tag de conversão do Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** O tipo de marca a ser criada:

* *[!UICONTROL Image]:* Para criar uma marca de imagem para exibir uma imagem transparente de 1 pixel x 1 pixel (pixel), que é invisível para os usuários finais, na página da Web. A prática recomendada é usar tags de imagem somente quando o site tiver uma política contra o uso de tags da JavaScript.

* *[!UICONTROL JavaScript]:* Para criar uma marca JavaScript.

Para obter mais informações sobre as diferenças entre os tipos de marcas, consulte &quot;[Perguntas frequentes sobre a conversão do Adobe Advertising e as marcas de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Uma ou mais métricas de conversão serão rastreadas quando um usuário final visualizar uma página contendo a marca de conversão. Para adicionar uma métrica à lista, digite o nome da métrica no campo &quot;[!UICONTROL Add new property]&quot; e clique em **[!UICONTROL Add]**.

Quando várias métricas são rastreadas, elas são unidas por um E comercial (`&`) na marca, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>As métricas adicionadas a esta lista não são salvas em nenhum lugar nem integradas à lista [!UICONTROL Conversions] do cliente na guia [!UICONTROL Admin]. No entanto, as métricas são adicionadas automaticamente à lista [!UICONTROL Conversions] do cliente quando a Adobe Advertising realmente reúne dados para uma métrica, o que acontece quando a tag de conversão é implementada em uma página e um usuário final conclui uma transação que abre essa página.

**[!UICONTROL Include unique transaction IDs]:** (Opcional) Inclui uma propriedade de ID de transação (`ev_transid=<transid>`) na marca. A opção é selecionada por padrão.

Ao selecionar essa opção, o anunciante deverá gerar um valor exclusivo para `<transid>` (por exemplo, uma ID de pedido real) quando a transação for concluída e passá-lo de volta para a Adobe Advertising, como `ev_transid=0123`. O Adobe Advertising usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e o mesmo valor de propriedade. A ID da transação não pode conter símbolos de E comercial (`&`), que são reservados como separadores de parâmetro. A ID da transação está incluída em [o [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que você pode usar para validar dados em Search, Social e Commerce com os dados do anunciante.

Se os dados não incluírem um identificador exclusivo por transação, o Adobe Advertising ainda gerará um com base no tempo da transação.

>[!NOTE]
>
>Se você enviar [feeds de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md) com dados de conversão para conversões offline, deverá enviar a ID de transação (`ev_transid`) da parte online da transação nos dados de feed das partes offline da transação.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** (somente marcas [!DNL JavaScript]) Qual versão da marca [!DNL JavaScript] criar: *[!UICONTROL v2]* (padrão) ou *[!UICONTROL v3]*.

Consulte &quot;[Perguntas frequentes sobre a conversão do Adobe Advertising e as tags de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; para obter mais informações sobre as diferenças.

## Implementar tags de rastreamento de conversão usando tags do Adobe Experience Platform e a extensão do Adobe Advertising

Você pode configurar o rastreamento de conversão para o Search, Social e Commerce usando tags na Adobe Experience Platform. As tags estão disponíveis para clientes corporativos do Adobe CX como um recurso incluso de valor agregado.

As seguintes tarefas são necessárias para configurar tags de rastreamento de conversão para o Search, Social e Commerce na interface do usuário da Experience Platform ou na interface da Coleção de dados da Experience Platform. Para obter informações completas e instruções para configurar tags, consulte o Guia de Tags da Experience Platform, começando com &quot;[Visão geral das tags](https://experienceleague.adobe.com/pt-br/docs/experience-platform/tags/home)&quot; e &quot;[Guia de início rápido](https://experienceleague.adobe.com/pt-br/docs/experience-platform/tags/get-started/quick-start).&quot;

>[!PREREQUISITES]
>
>Para instalar a extensão de tag necessária, peça ao administrador da organização acesso aos recursos de Coleção de Dados na interface do usuário, incluindo a permissão `manage_properties`.

1. Na [Interface da Coleção de Dados](https://experience.adobe.com/#/data-collection/), instale a [Extensão](https://experienceleague.adobe.com/pt-br/docs/experience-platform/tags/ui/extensions/overview) do Adobe Advertising:

   1. Na propriedade aplicável, abra o catálogo de extensões e selecione **Adobe Advertising**.

   1. No menu suspenso, selecione **SSC** (para Search, Social e Commerce).

   1. No campo **ID de Usuário do SSC**, digite a ID de usuário numérica para a conta de Pesquisa, Social e Commerce da sua organização.

      Se você não souber sua ID de usuário, entre em contato com a equipe de conta da Adobe.

   1. Clique em **Salvar**.

1. Crie uma nova regra (por exemplo, &quot;form_completes&quot;) para acionar a tag de conversão do Search, Social e Commerce:

   1. Na seção Configuração do evento:

      1. Selecione os seguintes valores:

         **Extensão:** `Core`

         **Tipo de evento:** `Library Loaded (Page Top)`

      1. Clique em **Manter alterações**.

   1. Na seção Configuração de condição:

      1. Especifique os seguintes valores:

         **Tipo lógico:** `Regular`

         **Extensão:** `Core`

         **Tipo de Condição:** `Path Without Query String`

         **Retornará true se o caminho for igual a:** O caminho onde a conversão deve ser rastreada (por exemplo, `/form_complete`).

      1. Clique em **Manter alterações**.

   1. Na seção Configuração de ação:

      1. Especifique os seguintes valores:

         **Extensão:** `Adobe Advertising`

         **Tipo de ação:** `AMO Measurement`

         **Nome da Propriedade de Conversão:** O nome da propriedade de conversão (por exemplo, `form_completes`).

         **Valor:** O valor numérico da propriedade de conversão (por exemplo, `1` para rastrear formulários_completes) ou escolha um [elemento de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/tags/ui/data-elements) existente.

      1. Clique em **Manter alterações**.

   1. Salve a regra.

1. Publique as alterações.

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Sobre as ferramentas para criar e decodificar marcas de rastreamento](tracking-tools-about.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [A marca de mapeamento de conversão do Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Sobre o gerenciamento das métricas de conversão de um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
