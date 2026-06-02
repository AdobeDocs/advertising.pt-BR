---
title: (Nova interface do usuário) Gerar e implementar uma tag de rastreamento de conversão do Adobe Advertising
description: Saiba como criar uma tag de conversão do Adobe Advertising para rastrear seus eventos de conversão.
feature: Search Tools, Search Tracking
source-git-commit: f97a636a55c6cc823f0041e7acd6f48dca769a3e
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# (Nova interface do usuário) Gerar e implementar uma tag de rastreamento de conversão do Adobe Advertising

*Somente anunciantes com rastreamento de conversão do Adobe Advertising*

Crie uma tag de conversão separada para cada conjunto de métricas que você deseja rastrear. Você pode gerar tags na Search, Social e Commerce ou usando tags na Adobe Experience Platform (anteriormente conhecida como Adobe Experience Platform Launch) com a extensão do Adobe Advertising.

## Gerar e implementar uma tag de rastreamento de conversão no Search, Social e Commerce

>[!NOTE]
>
>Este recurso não adiciona marcas de imagem nem [!DNL JavaScript] marcas às páginas da Web do anunciante. Forneça as tags ao anunciante ou à agência uma lista de páginas da Web nas quais inserir cada uma. As tags devem ser adicionadas de acordo com o procedimento normal do anunciante para atualização de páginas da Web.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Na barra de ferramentas principal, clique em **[!UICONTROL Conversion Tag]**.

1. Especifique as [configurações da marca de conversão](#conversion-tag-settings).

1. Clique em **[!UICONTROL Generate]**.

1. Clique em **[!UICONTROL Copy]** para copiar a marca para a área de transferência. Forneça a tag ao anunciante ou à agência para implementar o.

>[!NOTE]
>
>Cada métrica na nova marca de conversão é listada automaticamente em [!UICONTROL Admin] > [!UICONTROL Conversions], mesmo que não esteja implementada ou que as páginas da Web em que está não tenham recebido nenhum clique. Esse comportamento é diferente do comportamento das métricas em tags criadas manualmente ou em outro lugar, que não são listadas em [!UICONTROL Admin] > [!UICONTROL Conversions] até que uma das páginas da Web em que ela está receba um clique. No entanto, em todos os casos, cada métrica é inicialmente excluída dos objetivos de portfólio, relatórios e exibições até que você as disponibilize explicitamente. Antes de adicionar as métricas aos objetivos do portfólio, considere primeiro disponibilizar as métricas e adicioná-las aos relatórios para verificar quando recebem cliques.

### Configurações da tag de conversão do Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** O tipo de marca a ser criada:

* *[!UICONTROL JavaScript]:* Para criar uma marca JavaScript.

* *[!UICONTROL Image]:* Para criar uma marca de imagem para exibir uma imagem transparente de 1 pixel x 1 pixel (pixel), que é invisível para os usuários finais, na página da Web. A prática recomendada é usar tags de imagem somente quando o site tiver uma política contra o uso de tags da JavaScript.

Para obter mais informações sobre as diferenças entre os tipos de marcas, consulte &quot;[Perguntas frequentes sobre a conversão do Adobe Advertising e as marcas de rastreamento de exibição de página](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Include unique transaction IDs]:** (Opcional) Inclui uma propriedade de ID de transação (`ev_transid=<transid>`) na marca. A opção é selecionada por padrão.

Ao selecionar essa opção, o anunciante deverá gerar um valor exclusivo para `<transid>` (por exemplo, uma ID de pedido real) quando a transação for concluída e passá-lo de volta para a Adobe Advertising, como `ev_transid=0123`. O Adobe Advertising usa a ID de transação para eliminar transações duplicadas com a mesma ID de transação e o mesmo valor de propriedade. A ID da transação não pode conter símbolos de E comercial (`&`), que são reservados como separadores de parâmetro. A ID da transação está incluída em [o [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que você pode usar para validar dados em Search, Social e Commerce com os dados do anunciante.

Se os dados não incluírem um identificador exclusivo por transação, o Adobe Advertising ainda gerará um com base no tempo da transação.

>[!NOTE]
>
>Se você enviar [feeds de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md) com dados de conversão para conversões offline, deverá enviar a ID de transação (`ev_transid`) da parte online da transação nos dados de feed das partes offline da transação.

**[!UICONTROL JS Version]:** (somente marcas [!DNL JavaScript]) Qual versão da marca [!DNL JavaScript] criar: *[!UICONTROL v2]* (padrão) ou *[!UICONTROL v3]*.

**[!UICONTROL Security]:** O protocolo de segurança do site cria: *[!UICONTROL Standard]* (para sites que usam HTTP) ou *[!UICONTROL Secure]* (para sites que usam HTTPs).

**[!UICONTROL Properties]:** Uma ou mais métricas de conversão serão rastreadas quando um usuário final visualizar uma página contendo a marca de conversão. Para adicionar uma métrica à lista, digite o nome da métrica no campo &quot;[!UICONTROL Property name]&quot; e clique em **[!UICONTROL Add]**.

Quando várias métricas são rastreadas, elas são unidas por um E comercial (`&`) na marca, como `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>As métricas adicionadas a esta lista não são salvas em nenhum lugar nem integradas à lista [!UICONTROL Conversions] do cliente na guia [!UICONTROL Admin]. No entanto, as métricas são adicionadas automaticamente à lista [!UICONTROL Conversions] do cliente quando a Adobe Advertising realmente reúne dados para uma métrica, o que acontece quando a tag de conversão é implementada em uma página e um usuário final conclui uma transação que abre essa página.

## Implementar tags de rastreamento de conversão usando tags do Adobe Experience Platform e a extensão do Adobe Advertising

Você pode configurar o rastreamento de conversão para o Search, Social e Commerce usando tags na Adobe Experience Platform. As tags estão disponíveis para clientes corporativos do Adobe CX como um recurso incluso de valor agregado.

As seguintes tarefas são necessárias para configurar tags de rastreamento de conversão para o Search, Social e Commerce na interface do usuário da Experience Platform ou na interface da Coleção de dados da Experience Platform. Para obter informações completas e instruções para configurar tags, consulte o Guia de Tags da Experience Platform, começando com &quot;[Visão geral das tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)&quot; e &quot;[Guia de início rápido](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start).&quot;

>[!PREREQUISITES]
>
>Para instalar a extensão de tag necessária, peça ao administrador da organização acesso aos recursos de Coleção de Dados na interface do usuário, incluindo a permissão `manage_properties`.

1. Na [Interface da Coleção de Dados](https://experience.adobe.com/#/data-collection/), instale a [Extensão](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview) do Adobe Advertising:

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

         **Valor:** O valor numérico da propriedade de conversão (por exemplo, `1` para rastrear formulários_completes) ou escolha um [elemento de dados](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) existente.

      1. Clique em **Manter alterações**.

   1. Salve a regra.

1. Publique as alterações.

>[!MORELIKETHIS]
>
>* [Sobre as marcas de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato das marcas de rastreamento de conversão do JavaScript versão 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato das marcas de rastreamento de conversão de imagem](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [A marca de mapeamento de conversão do Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
