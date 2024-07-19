---
title: Gerar uma tag de rastreamento de conversão de Adobe Advertising
description: Saiba como criar uma tag de conversão de Adobe Advertising para rastrear seus eventos de conversão.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Gerar uma tag de rastreamento de conversão de Adobe Advertising

*Anunciantes somente com rastreamento de conversão de Adobe Advertising*

Crie uma tag de conversão separada para cada conjunto de métricas que deseja rastrear e forneça as tags ao anunciante ou à agência uma lista de páginas da Web nas quais inserir cada uma.

>[!NOTE]
>
>Este recurso não adiciona marcas de imagem nem [!DNL JavaScript] marcas às páginas da Web do anunciante. As tags devem ser adicionadas de acordo com o procedimento normal do anunciante para atualização de páginas da Web.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique as [configurações da marca de conversão](#conversion-tag-settings).

1. Gere a tag:

   * Se o site usar HTTP, clique em **[!UICONTROL Generate Conversion Tag]**.

   * Se o site for executado em um servidor seguro (HTTPS), clique em **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie a tag da caixa de diálogo e cole-a nas páginas da Web apropriadas, conforme necessário.

>[!NOTE]
>
>Cada métrica na nova marca de conversão é listada automaticamente em [!UICONTROL Admin] > [!UICONTROL Conversions], mesmo que não esteja implementada ou que as páginas da Web em que está não tenham recebido nenhum clique. Esse comportamento é diferente do comportamento das métricas em tags criadas manualmente ou em outro lugar, que não são listadas em [!UICONTROL Admin] > [!UICONTROL Conversions] até que uma das páginas da Web em que está tenha recebido um clique. No entanto, em todos os casos, cada métrica é inicialmente excluída dos objetivos de portfólio, relatórios e exibições até que você as disponibilize explicitamente. No entanto, antes de adicionar as métricas aos objetivos do portfólio, considere primeiro disponibilizar as métricas e adicioná-las aos relatórios para verificar quando recebem cliques.

## Configurações de tag de conversão de Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** O tipo de marca a ser criada:

* *[!UICONTROL Image]:* Para criar uma marca de imagem para exibir uma imagem transparente de 1 pixel x 1 pixel (pixel), que é invisível para os usuários finais, na página da Web. A prática recomendada é usar tags de imagem somente quando o site tiver uma política contra o uso de tags da JavaScript.

* *[!UICONTROL JavaScript]:* Para criar uma marca JavaScript.

Para obter mais informações sobre as diferenças entre os tipos de marcas, consulte &quot;[Perguntas frequentes sobre a conversão de Adobe Advertising e as marcas de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Uma ou mais métricas de conversão serão rastreadas quando um usuário final visualizar uma página contendo a marca de conversão. Para adicionar uma métrica à lista, digite o nome da métrica no campo &quot;[!UICONTROL Add new property]&quot; e clique em **[!UICONTROL Add]**.

Quando várias métricas são rastreadas, elas são unidas por um E comercial (`&`) na marca, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>As métricas adicionadas a esta lista não são salvas em nenhum lugar nem integradas à lista [!UICONTROL Conversions] do cliente na guia [!UICONTROL Admin]. No entanto, as métricas são adicionadas automaticamente à lista [!UICONTROL Conversions] do cliente quando o Adobe Advertising realmente reúne dados para uma métrica, o que acontece quando a tag de conversão é implementada em uma página e um usuário final conclui uma transação que abre essa página.

**[!UICONTROL Include unique transaction IDs]:** (Opcional) Inclui uma propriedade de ID de transação (`ev_transid=<transid>`) na marca. A opção é selecionada por padrão.

Ao selecionar essa opção, o anunciante deverá gerar um valor exclusivo para `<transid>` (por exemplo, uma ID de pedido real) quando a transação for concluída e passá-lo de volta para o Adobe Advertising, como `ev_transid=0123`. O Adobe Advertising usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e o mesmo valor de propriedade. A ID da transação não pode conter símbolos de E comercial (`&`), que são reservados como separadores de parâmetro. A ID da transação está incluída em [o [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que você pode usar para validar dados em Search, Social e Commerce com os dados do anunciante.

Se os dados não incluírem um identificador exclusivo por transação, o Adobe Advertising ainda gerará um com base no tempo da transação.

>[!NOTE]
>
>Se você enviar [feeds de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md) com dados de conversão para conversões offline, deverá enviar a ID de transação (`ev_transid`) da parte online da transação nos dados de feed das partes offline da transação.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** (somente marcas [!DNL JavaScript]) Qual versão da marca [!DNL JavaScript] criar: *[!UICONTROL v2]* (padrão) ou *[!UICONTROL v3]*.

Consulte &quot;[Perguntas frequentes sobre a conversão de Adobe Advertising e as tags de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; para obter mais informações sobre as diferenças.

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão de Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Sobre as ferramentas para criar e decodificar marcas de rastreamento](tracking-tools-about.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [A marca de mapeamento de conversão do Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Sobre o gerenciamento das métricas de conversão de um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
