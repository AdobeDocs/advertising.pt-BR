---
title: Opções de rastreamento de conversão para o Search, Social e Commerce
description: Saiba mais sobre as opções de rastreamento de conversão para o Search, Social e Commerce.
exl-id: 098efaf8-6ffb-4811-8b20-41c7c85df812
feature: Search Tracking
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Opções de rastreamento de conversão para o Search, Social e Commerce

Search, Social e Commerce podem usar dados de conversão que são rastreados das seguintes maneiras:

* **Conversões rastreadas por Adobe Advertising:** O anunciante insere uma tag de rastreamento de conversão de Adobe Advertising em cada página de conversão. A tag envia os dados de conversão para um servidor de rastreamento. Você pode usar o pixel de terceiros herdado ou o pixel de terceiros mais recente. Consulte &quot;[Comparação de cada método de rastreamento de conversão](#conversion-tracking-comparison).&quot;

* **Conversões do Adobe Analytics:** O anunciante usa o rastreamento de Adobe Analytics para todas as conversões. Essa opção requer uma integração Adobe Advertising-Adobe Analytics. Consulte &quot;[Rastreamento de conversão do Adobe Analytics](conversion-tracking-analytics.md)&quot; para obter mais informações.

* **[!DNL Google Analytics]conversões:** O anunciante usa o [!DNL Google Analytics] para rastrear todas as conversões. Consulte &quot;[[!DNL Google Ads] dados de conversão no Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; para obter mais informações sobre as conversões sincronizadas automaticamente.

* **Conversões rastreadas pelo anunciante:** (Somente para clientes Search, Social e Commerce) O anunciante fornece aos clientes Search, Social e Commerce um arquivo de feed com qualquer combinação de dados de conversão online e offline. Consulte &quot;[Rastreamento de conversão usando um feed de ID EF](feed-efid.md)&quot; e &quot;[Rastreamento de conversão usando um feed de ID de transação](feed-transaction-id.md).&quot;

## Comparação de cada método de rastreamento de conversão {#conversion-tracking-comparison}

À medida que as políticas de cookies do navegador se tornam mais rigorosas, é importante entender seus recursos de rastreamento atuais e identificar suas melhores opções a longo prazo.

| Método de rastreamento | Descrição | Limitação | Benefícios | Recomendado? |
|----|----|----|----|----|
| Adobe Analytics | Anunciantes com [Adobe Analytics para publicidade](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importar automaticamente seus [!DNL Analytics] eventos padrão e personalizados para o Adobe Advertising para relatórios e otimização. | <ul><li>[!DNL Safari] O permite somente uma retrospectiva de conversão de sete dias, que é redefinida em visitas repetidas do site durante a janela de retrospectiva.</li><li> Espere limitações semelhantes no [!DNL Chrome] em 2024.</li></ul> | <ul><li>Integração perfeita com o [!DNL Analytics]</li> <li>Consulte dados de pesquisa paga em [!DNL Analytics] Analysis Workspace</li><li>Benefícios além da pesquisa paga</li></ul> | Sim |
| Pixel de Adobe Advertising herdado | Os anunciantes adicionam imagem de Adobe Advertising herdada ou pixels JavaScript às suas páginas de conversão. O pixel é acionado quando um usuário que clicou em um anúncio chega à página. Esse método depende de cookies de terceiros. | <ul><li>[!DNL Safari] O bloqueia todo o rastreamento de conversão usando este método.</li><li>Espere limitações semelhantes no [!DNL Chrome] em 2024.</li></ul> | O pixel já está implementado. No entanto, você ainda deve [implementar a tag de mapeamento ITP adicional](itp-conversion-mapping-tag.md).<br><br>Recomendação: alterne para o pixel primário. | Não |
| Adobe Advertising Pixel próprio | Os anunciantes fazem o seguinte: <ul><li>Implemente a biblioteca JavaScript do para o [Serviço da Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) em todo o site.</li><li>Adicione o Adobe Advertising [Tags JavaScript com mapeamento ITP](itp-conversion-mapping-tag.md) para qualquer página que possa ser uma página de aterrissagem a partir de um clique de pesquisa (idealmente, em todas as páginas, já que as páginas de aterrissagem podem mudar com o tempo). A tag permite que o Adobe Advertising rastreie um evento de conversão que ocorre em uma página que converte números grandes em notação científica na página de aterrissagem.</li><li>Adicione o Adobe Advertising [Tag de rastreamento de conversão do JavaScript v3](format-conversion-tag-jsv3.md) para páginas de conversão.</li></ul> | <ul><li>[!DNL Safari] O permite somente uma retrospectiva de conversão de sete dias, que é redefinida em visitas repetidas do site durante a janela de retrospectiva.</li><li>Espere limitações semelhantes no [!DNL Chrome] em 2022.</li></ul> | [!DNL Safari] rastreia conversões durante a retrospectiva de sete dias. Como a pesquisa é redefinida em visitas repetidas ao site durante a janela de pesquisa, a limitação não afeta todas [!DNL Safari] usuários. | Não |
| Feed EFID | As contas de pesquisa do anunciante são configuradas para gerar URLs de destino/URLs finais com IDs exclusivas de Adobe Advertising (tokens). Quando um usuário clica em um anúncio, o Adobe Advertising cria uma ID exclusiva (`EFID`) e o exibe no final do URL final. O sistema cliente do anunciante captura a EFID como um identificador exclusivo para conversões que resultam do clique e a envia para o Adobe Advertising em um feed de receita que inclui a EFID, a data da transação e a propriedade de conversão. O Adobe Advertising usa o EFID para corresponder a conversão ao clique original. | <ul><li>O anunciante deve ter uma maneira de capturar a EFID e enviar feeds automatizados para o Adobe Advertising diariamente.</li><li>As conversões podem ser rastreadas por até 180 dias (por Adobe Advertising) ou de acordo com os limites do sistema do anunciante.</li></ul> | <ul><li>Esse método usa dados de conversão primários, de modo que não é afetado pelas limitações de cookies de terceiros.</li><li>As conversões online e offline podem ser enviadas em um feed.</li><li>Não são necessárias alterações de código ou tags para o site.</li></ul> | Sim |
| Feed de ID de transação [feed combo] | Os anunciantes adicionam pixels de Adobe Advertising que incluem um parâmetro para uma ID de transação exclusiva (`ev_transid=&lt;transid&gt;`) para suas páginas da Web, e o Adobe Advertising captura a ID de transação exclusiva criada quando o pixel é acionado. O sistema cliente do anunciante também captura as [!UICONTROL Transaction ID] e envia Adobe Advertising a feed de receita para conversões offline com correspondência [!UICONTROL Transaction ID] valores | <ul><li>Se o anunciante estiver usando o pixel herdado, que [!DNL Safari] for impedida de disparar, a ID não será capturada para uso em dados offline.</li><li>O feed não é automatizado.</li></ul> | <ul><li>Se você implementar o pixel primário, a variável [!UICONTROL Transaction ID] é capturado em [!DNL Safari].</li><li>Fornece rastreamento de eventos de conversão offline/aprovados.</li></ul> | Não |
| Conversões do Google | Conversões rastreadas com [!DNL Google Analytics] as tags são importadas automaticamente para o Adobe Advertising por meio de uma conexão de API. Cada nome de conversão tem um `&quot;GGL_&quot;` prefixo. | <ul><li>O Google normalmente não rastreia dados offline.</li><li>As conversões da Microsoft® Advertising não estão incluídas.</li></ul> | O Google usa o aprendizado de máquina para extrapolar&quot;[conversões modeladas](https://support.google.com/google-ads/answer/10081327).&quot; | Não |

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Sobre as tags de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Rastreamento de conversão do Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Rastreamento de conversão usando um feed de ID EF](/help/search-social-commerce/tracking/feed-efid.md)
>* [Rastreamento de conversão usando um feed de ID de transação](/help/search-social-commerce/tracking/feed-transaction-id.md)
