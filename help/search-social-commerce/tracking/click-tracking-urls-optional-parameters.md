---
title: Parâmetros de rastreamento opcionais para URLs de rastreamento de cliques
description: Saiba mais sobre os parâmetros opcionais de rastreamento de pesquisa, redes sociais e comércio e sobre os parâmetros específicos de rastreamento de rede de anúncios que você pode adicionar aos URLs de rastreamento de cliques.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Parâmetros de rastreamento opcionais para URLs de rastreamento de cliques

*Google Ads, Microsoft Advertising e Yahoo! Somente contas do Japão*

Em vez de usar apenas os parâmetros de rastreamento padrão para um URL final ou URL de destino, você pode adicionar mais parâmetros para rastrear dados específicos de uma conta de rede de anúncios. Você pode adicionar qualquer combinação dos seguintes parâmetros nas configurações da conta ou nas configurações da campanha:

* Você pode anexar qualquer string de texto estático como parâmetro nos URLs base da conta/campanha.

* Você pode anexar parâmetros específicos de rede de anúncio e publicidade do Adobe nos URLs base da conta/campanha para rastrear mais dados:

   * Os parâmetros de publicidade de Adobe são semiestáticos. O Adobe Advertising insere um valor de dados quando faz upload do URL base para a rede de publicidade. Por exemplo, quando você anexa `campaign={ef_campaign}` para o URL base, a Adobe Advertising substitui `{ef_campaign}` com o nome real da campanha (como &quot;Back-to-school-Campaign&quot;) quando ele carrega o URL.

      **Nota:** Depois que os valores forem inseridos, eles permanecerão estáticos. Se você mover uma palavra-chave ou um anúncio para um grupo de anúncios diferente, ou mover o grupo de anúncios para uma campanha diferente, o parâmetro {ef_adgroup} ou {ef_campaign} não será atualizado automaticamente, portanto, você deve gerar manualmente um novo URL de destino ou URL de base (final).

   * Parâmetros específicos da rede de publicidade são dinâmicos, e o mecanismo de pesquisa insere um valor de dados quando o usuário clica em uma publicidade. Por exemplo, quando você anexa `{param1}` ao URL base, a rede de anúncios o substitui pelo valor real {param1} quando um usuário final clica no anúncio.

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
| {custom_code}</code> | Para inserir dados da coluna &quot;Parâmetro de URL personalizado&quot; em um arquivo de bulksheet carregado no URL de rastreamento. {custom_code} pode ser usado somente no final do valor de um ou mais pares de valor chave no URL de rastreamento. Exemplos: a={custom_code}</code>; a={ef_campaign}{custom_code}</code>; a={ef_campaign}{custom_code}&amp;b={custom_code}</code><br><br><b>Nota:</b> Para inserir o valor personalizado do arquivo de bulksheet no URL de rastreamento, faça upload do arquivo de bulksheet usando a opção &quot;Gerar URLs de rastreamento&quot;. Para obter mais informações sobre o uso de arquivos de bulksheet, consulte &quot;[Sobre o gerenciamento de dados de campanha usando bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| {ef_uniqueid}</code> | Para inserir o identificador exclusivo criado pela Adobe Advertising. Adicionado automaticamente quando o método de rastreamento é &quot;EF Redirect&quot;. |
| {ef_userid}</code> | Para inserir a ID de usuário exclusiva que a Adobe Advertising atribui ao anunciante. |
| {ef_sid}</code> | Para inserir a ID numérica que o Search, Social e Commerce atribui à rede de publicidade: <i>[!UICONTROL 3]</i> para [!DNL Google Ads], <i>[!UICONTROL 10]</i> para [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> para [!DNL Meta], <i>[!UICONTROL 86]</i> para [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> para [!DNL Naver], <i>[!UICONTROL 88]</i> para [!DNL Baidu], <i>[!UICONTROL 90]</i> para [!DNL Yandex], <i>[!UICONTROL 94]</i> para [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> para [!DNL Yahoo Native] (obsoleto) ou <i>[!UICONTROL 106]</i> para [!DNL Pinterest] (obsoleto). |
| {ef_searchengine}</code> | Para inserir o nome da rede de publicidade. |
| {ef_campaign}</code> | Para inserir o nome da campanha. |
| {ef_campaign}</code> | Para inserir a ID da campanha. <b>Nota:</b> A ID de uma nova campanha só será criada depois que a campanha for postada na rede de publicidade. Se a conta usar as opções &quot;EF Redirect&quot; e &quot;AutoUpload&quot;, a Adobe Advertising inserirá automaticamente a ID da campanha nos URLs de destino relevantes ou nos URLs finais no dia seguinte. Se a conta não usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e você quiser inserir a ID da campanha nos URLs de destino relevantes ou URLs finais, crie a campanha; baixe um arquivo de bulksheet para a nova campanha, usando a opção para &quot;Gerar URLs de rastreamento&quot;; e depois publique o arquivo na rede de publicidade. |
| {ef_adgroup}</code> | Para inserir o nome do grupo de anúncios. |
| {ef_adgroupid}</code> | Para inserir a ID do grupo de anúncios. <b>Nota:</b> A ID para um novo grupo de publicidade não é criada até que o grupo de publicidade seja postado na rede de publicidade. Se a conta usar as opções &quot;EF Redirect&quot; e &quot;AutoUpload&quot;, a Adobe Advertising inserirá automaticamente a ID do grupo de publicidade nos URLs de destino relevantes ou nos URLs finais no dia seguinte. Se a conta não usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e você quiser inserir a ID do grupo de anúncios nos URLs de destino relevantes ou URLs finais, será necessário criar o grupo de anúncios; baixar um arquivo de bulksheet para o novo grupo de anúncios, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e depois publicar o arquivo na rede de anúncios. |
| {ef_keyword}</code> | Para inserir a palavra-chave. |
| {ef_keywordid}</code> | Para inserir a ID da palavra-chave. <b>Nota:</b> A ID para uma nova palavra-chave só será criada depois que a palavra-chave for postada na rede de publicidade. Se a conta usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot;, a Adobe Advertising inserirá automaticamente a ID de palavra-chave nos URLs de destino relevantes ou nos URLs finais no dia seguinte. Se a conta não usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e você quiser inserir a ID da palavra-chave nos URLs de destino relevantes ou URLs finais, então você deve criar a palavra-chave; baixar um arquivo de bulksheet para a nova palavra-chave, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e, em seguida, publicar o arquivo na rede de publicidade. |
| {ef_matchtype}</code> | Para inserir o tipo de correspondência de palavra-chave como &quot;Amplo&quot;, &quot;Exato&quot; ou &quot;Frase&quot;. Incluído automaticamente para o Google Ads e Microsoft Advertising com o método de rastreamento &quot;EF Redirect&quot;. |
| {ef_adid}</code> | Para inserir a ID do anúncio. <b>Nota:</b> A ID para um novo anúncio não é criada até que o anúncio seja postado na rede de anúncios. Se a conta usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot;, a Adobe Advertising inserirá automaticamente a ID do anúncio nos URLs de destino relevantes ou nos URLs finais no dia seguinte. Se a conta não usar as opções &quot;EF Redirect&quot; e &quot;Auto Upload&quot; e você quiser inserir o ID do anúncio nos URLs de destino relevantes ou URLs finais, então você deve criar o anúncio, baixar um arquivo de bulksheet para o novo anúncio, usando a opção para &quot;Gerar URLs de rastreamento;&quot; e depois publicar o arquivo na rede de publicidade. |

## Parâmetros de rastreamento dinâmico do Google Ads

Consulte [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Parâmetros de rastreamento dinâmico da Microsoft Advertising

Consulte [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Parâmetros de rastreamento dinâmico nativos do Yahoo

Consulte [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Parâmetros de rastreamento dinâmico de anúncios do Japão

Consulte [https://help.marketing.yahoo.co.jp/en/?p=115](https://help.marketing.yahoo.co.jp/en/?p=115).

## Parâmetros de rastreamento dinâmico do Yandex

Consulte [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Sobre formatos de URL de rastreamento de cliques para o serviço de rastreamento de conversão do Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
