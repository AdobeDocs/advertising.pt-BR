---
title: Gerar uma tag de rastreamento de conversão de Adobe Advertising
description: Saiba como criar uma tag de conversão de Adobe Advertising para rastrear seus eventos de conversão.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Gerar uma tag de rastreamento de conversão de Adobe Advertising

*Anunciantes com rastreamento de conversão de Adobe Advertising somente*

Crie uma tag de conversão separada para cada conjunto de métricas que deseja rastrear e forneça as tags ao anunciante ou à agência uma lista de páginas da Web nas quais inserir cada uma.

>[!NOTE]
>
>Esse recurso não adiciona tags de imagem ou [!DNL JavaScript] para as páginas da Web do anunciante. As tags devem ser adicionadas de acordo com o procedimento normal do anunciante para atualização de páginas da Web.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Especifique a [configurações da tag de conversão](#conversion-tag-settings).

1. Gere a tag:

   * Se o site usar HTTP, clique em **[!UICONTROL Generate Conversion Tag]**.

   * Se o site for executado em um servidor seguro (HTTPS), clique em **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copie a tag da caixa de diálogo e cole-a nas páginas da Web apropriadas, conforme necessário.

>[!NOTE]
>
>Cada métrica na nova tag de conversão é listada automaticamente em [!UICONTROL Admin] > [!UICONTROL Transaction Properties], mesmo que não esteja implementado ou que as páginas da Web em que está não tenham recebido nenhum clique. Esse comportamento é diferente do comportamento das métricas em tags criadas manualmente ou em outro lugar, que não estão listadas em [!UICONTROL Admin] > [!UICONTROL Transaction Properties] até que uma das páginas da web em que está tenha recebido um clique. No entanto, em todos os casos, cada métrica é inicialmente excluída dos objetivos de portfólio, relatórios e exibições até que você as disponibilize explicitamente. No entanto, antes de adicionar as métricas aos objetivos do portfólio, considere primeiro disponibilizar as métricas e adicioná-las aos relatórios para verificar quando recebem cliques.

## Configurações de tag de conversão de Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** O tipo de tag a ser criada:

* *[!UICONTROL Image]:* Para criar uma tag de imagem para exibir uma imagem transparente de 1 pixel x 1 pixel (pixel), que é invisível para os usuários finais, na página da Web. A prática recomendada é usar tags de imagem somente quando o site tiver uma política contra o uso de tags JavaScript.

* *[!UICONTROL JavaScript]:* Para criar uma tag JavaScript.

Para obter mais informações sobre as diferenças entre os tipos de tag, consulte &quot;[Perguntas frequentes sobre a conversão de Adobe Advertising e as tags de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Uma ou mais métricas de conversão a serem rastreadas quando um usuário final visualizar uma página contendo a tag de conversão. Para adicionar uma métrica à lista, digite o nome da métrica no &quot;[!UICONTROL Add new property]&quot; e clique em **[!UICONTROL Add]**.

Quando várias métricas são rastreadas, elas são unidas por um E comercial (`&`) na tag, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>As métricas adicionadas a esta lista não são salvas em nenhum lugar nem integradas ao do cliente [!UICONTROL Conversions] lista na [!UICONTROL Admin] guia. No entanto, as métricas são adicionadas ao do cliente [!UICONTROL Conversions] lista automaticamente assim que o Adobe Advertising realmente reúne dados para uma métrica, o que acontece quando a tag de conversão é implementada em uma página e um usuário final conclui uma transação que abre essa página.

**[!UICONTROL Include unique transaction IDs]:** (Opcional) Inclui uma propriedade de ID de transação (`ev_transid=<transid>`) na tag. A opção é selecionada por padrão.

Ao selecionar essa opção, o anunciante deve gerar um valor exclusivo para `<transid>` (por exemplo, uma ID de pedido real) quando a transação estiver concluída e passá-la de volta para o Adobe Advertising, como `ev_transid=0123`. O Adobe Advertising usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e o mesmo valor de propriedade. A ID da transação não pode conter símbolos de E comercial (`&`), que são reservados como separadores de parâmetro. A ID da transação está incluída em [o [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que você pode usar para validar dados no Search, Social e Commerce com os dados do anunciante.

Se os dados não incluírem um identificador exclusivo por transação, o Adobe Advertising ainda gerará um com base no tempo da transação.

>[!NOTE]
>
>Se você enviar [feeds de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md) com os dados de conversão para conversões offline, você deve enviar a ID da transação (`ev_transid`) para a parte online da transação nos dados de feed das partes offline da transação.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] (somente tags do ) Qual versão do [!DNL JavaScript] tag a ser criada: *[!UICONTROL v2]* (o padrão) ou *[!UICONTROL v3]*.

Consulte &quot;[Perguntas frequentes sobre a conversão de Adobe Advertising e as tags de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; para obter mais informações sobre as diferenças.

>[!MORELIKETHIS]
>
>* [Sobre as tags de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Sobre as ferramentas para criar e decodificar tags de rastreamento](tracking-tools-about.md)
>* [Perguntas frequentes sobre tags de rastreamento de conversão e exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das tags de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das tags de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [A tag de mapeamento de conversão do JavaScript do Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Sobre o gerenciamento das propriedades de transação de um anunciante](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
