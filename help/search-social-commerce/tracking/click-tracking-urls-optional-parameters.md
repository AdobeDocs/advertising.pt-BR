---
title: Parâmetros de rastreamento opcionais para URLs de rastreamento de cliques
description: Saiba mais sobre os parâmetros opcionais de rastreamento de pesquisa, redes sociais e comércio e sobre os parâmetros específicos de rastreamento de rede de anúncios que você pode adicionar aos URLs de rastreamento de cliques.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: c743e0dec75578d739a704ef94f96dd7be4f982e
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Parâmetros de rastreamento opcionais para URLs de rastreamento de cliques

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan], e [!DNL Yandex] somente contas*

Em vez de usar apenas os parâmetros de rastreamento padrão para um URL final ou URL de destino, você pode adicionar mais parâmetros para rastrear dados específicos de uma conta de rede de anúncios. Você pode adicionar qualquer combinação dos seguintes parâmetros nas configurações da conta ou nas configurações da campanha:

* Você pode anexar qualquer string de texto estático como parâmetro nos URLs base da conta/campanha.

* Você pode anexar parâmetros específicos da rede de Adobe Advertising e anúncios nos URLs base da conta/campanha para rastrear mais dados:

   * Os parâmetros de Adobe Advertising são semiestáticos. o Adobe Advertising insere um valor de dados quando carrega o URL base para a rede de publicidade. Por exemplo, quando você anexa `campaign={ef_campaign}` para o URL base, o Adobe Advertising substitui `{ef_campaign}` com o nome real da campanha (como &quot;Back-to-school-Campaign&quot;) quando ele carrega o URL.

     **Nota:** Depois que os valores forem inseridos, eles permanecerão estáticos. Se você mover uma palavra-chave ou anúncio para um grupo de publicidade diferente, ou mover o grupo de publicidade para uma campanha diferente, então a variável  {ef_adgroup} ou {ef_campaign} O parâmetro da não é atualizado automaticamente, portanto, você deve gerar manualmente um novo URL de destino ou URL de base (final).

   * Parâmetros específicos da rede de publicidade são dinâmicos, e o mecanismo de pesquisa insere um valor de dados quando o usuário clica em uma publicidade. Por exemplo, quando você anexa `{param1}` ao URL base, a rede de publicidade o substitui pelo {param1} quando um usuário final clica no anúncio.

>[!NOTE]
>
>* Separe vários parâmetros com vírgulas ou &quot;E&quot; comercial (`&`).
>* Os parâmetros a seguir não diferenciam maiúsculas de minúsculas.
>* Os caracteres especiais nos parâmetros anexados são substituídos da seguinte maneira no URL de destino gerado ou no URL de base (final):
>  * `=` é substituída por `%3D`
>  * `?` é substituída por `%26`
>  * um espaço vazio é substituído por `%2B`
>  Por exemplo, quando você anexa o parâmetro `campaign={ef_campaign}` ao URL base http://www.example.com para uma palavra-chave, o URL base para essa palavra-chave é gerado como `http://www.example.com/campaign%3D{ef_campaign}`.

## Parâmetros de rastreamento estático de Pesquisa, Social e Comércio

Você pode usar os parâmetros a seguir para contas em qualquer rede de anúncios e combiná-los com parâmetros para uma rede de anúncios específica, conforme necessário. Alguns desses parâmetros duplicam os parâmetros que são adicionados automaticamente para redes de anúncios específicas quando o método de rastreamento da conta é &quot;[!UICONTROL EF Direct].&quot;

Todos os parâmetros a seguir devem ser especificados como um par de valores chave; você pode incluir vários parâmetros para um par de valores. Por exemplo, para inserir o nome da campanha, use `<your_parameter_name>={ef_campaign}`, como `campaign={ef_campaign}`. Para inserir o tipo de correspondência usando nomes de tipo de correspondência especificados, use `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, como `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Os tipos de correspondência não aplicáveis não aparecem no URL resultante.

| Parâmetro | Descrição |
| ---- | ---- |
| <code>{custom_code}</code> | Para inserir dados da coluna &quot;Parâmetro de URL personalizado&quot; em um arquivo de bulksheet carregado no URL de rastreamento. {custom_code} pode ser usado somente no final do valor de um ou mais pares de valor chave no URL de rastreamento. Exemplos:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Nota:</b> Para inserir o valor personalizado do arquivo de bulksheet no URL de rastreamento, faça upload do arquivo de bulksheet usando a opção &quot;Gerar URLs de rastreamento&quot;. Para obter mais informações sobre o uso de arquivos de bulksheet, consulte &quot;[Sobre o gerenciamento de dados de campanha usando bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| <code>{ef_uniqueid}</code> | Para inserir o identificador exclusivo criado pelo Adobe Advertising. Adicionado automaticamente quando o método de rastreamento é &quot;EF Redirect&quot;. |
| <code>{ef_userid}</code> | Para inserir o identificador de usuário único que o Adobe Advertising atribui ao anunciante. |
| <code>{ef_sid}</code> | Para inserir a ID numérica que o Search, Social e Commerce atribui à rede de publicidade: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft®® Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto) ou <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| <code>{ef_searchengine}</code> | Para inserir o nome da rede de publicidade. |
| <code>{ef_campaign}</code> | Para inserir o nome da campanha. |
| <code>{ef_campaignid}</code> | Para inserir a ID da campanha. <b>Nota:</b> A ID de uma nova campanha só será criada depois que a campanha for postada na rede de publicidade. Se a conta usar o &quot;[!UICONTROL EF Redirect]&quot; e &quot;AutoUpload&quot;, em seguida, o Adobe Advertising insere automaticamente a ID da campanha nos URLs de destino relevantes ou nos URLs finais no dia seguinte. Se a conta não usar o &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot; e quiser inserir a ID da campanha nos URLs de destino relevantes ou URLs finais, você deve criar a campanha; baixar um arquivo de bulksheet para a nova campanha, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e, em seguida, publicar o arquivo na rede de publicidade. |
| <code>{ef_adgroup}</code> | Para inserir o nome do grupo de anúncios. |
| <code>{ef_adgroupid}</code> | Para inserir a ID do grupo de anúncios. <b>Nota:</b> A ID para um novo grupo de publicidade não é criada até que o grupo de publicidade seja postado na rede de publicidade. Se a conta usar o &quot;[!UICONTROL EF Redirect]&quot; e &quot;AutoUpload&quot;, em seguida, o Adobe Advertising insere automaticamente a ID do grupo de anúncios nos URLs de destino relevantes ou URLs finais no dia seguinte. Se a conta não usar o[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot; e quiser inserir a ID do grupo de anúncios nos URLs de destino relevantes ou URLs finais, é necessário criar o grupo de anúncios; baixar um arquivo de bulksheet para o novo grupo de anúncios, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e, em seguida, publicar o arquivo na rede de anúncios. |
| <code>{ef_keyword}</code> | Para inserir a palavra-chave. |
| <code>{ef_keywordid}</code> | Para inserir a ID da palavra-chave. <b>Nota:</b> A ID para uma nova palavra-chave só será criada depois que a palavra-chave for postada na rede de publicidade. Se a conta usar o &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot;, o Adobe Advertising insere automaticamente a ID da palavra-chave nos URLs de destino relevantes ou URLs finais no dia seguinte. Se a conta não usar o &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot; e quiser inserir a ID da palavra-chave nos URLs de destino relevantes ou URLs finais, você deverá criar a palavra-chave; baixar um arquivo de bulksheet para a nova palavra-chave, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e, em seguida, publicar o arquivo na rede de publicidade. |
| <code>{ef_matchtype}</code> | Para inserir o tipo de correspondência de palavra-chave como &quot;Amplo&quot;, &quot;Exato&quot; ou &quot;Frase&quot;. Incluído automaticamente para [!DNL Google Ads] e [!DNL Microsoft® Advertising] com o &quot;[!UICONTROL EF Redirect]&quot;método de rastreamento. |
| <code>{ef_adid}</code> | Para inserir a ID do anúncio. <b>Nota:</b> A ID para um novo anúncio não é criada até que o anúncio seja postado na rede de anúncios. Se a conta usar o &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot; e o Adobe Advertising insere automaticamente a ID do anúncio nos URLs de destino relevantes ou URLs finais no dia seguinte. Se a conta não usar o &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Auto Upload]&quot; e desejar inserir a ID do anúncio nos URLs de destino relevantes ou URLs finais, é necessário criar o anúncio; baixar um arquivo de bulksheet para o novo anúncio, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e, em seguida, publicar o arquivo na rede de publicidade. |

## [!DNL Google Ads] parâmetros de rastreamento dinâmico

Consulte [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft® Advertising] parâmetros de rastreamento dinâmico

Consulte [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Parâmetros de rastreamento dinâmico de anúncios do Japão

Consulte [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] parâmetros de rastreamento dinâmico

Consulte [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
