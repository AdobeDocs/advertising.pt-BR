---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Trechos

## Campo Modelo de rastreamento para entidades do Google Ads {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da página inicial, e também incorpora o URL da página final/de aterrissagem em uma [!DNL ValueTrack] parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Para rastreamento de conversão de Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

* Para obter os parâmetros compatíveis que incorporam o URL final, consulte a [[!DNL Google Ads] documentação para o suportado [!DNL ValueTrack] formatos](https://support.google.com/google-ads/answer/6305348). (Vá para os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Disponível [!DNL ValueTrack] Parâmetros.&quot;)

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como {lpurl}?matchtype={matchtype}&amp;dispositivo={device}.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

>[!NOTE]
>
>* Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.

## Campo Modelo de rastreamento para [!DNL Microsoft Advertising] entidades {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da página de aterrissagem e também incorpora o URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Para rastreamento de conversão de Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

* Para obter os parâmetros compatíveis que incorporam o URL final, consulte a [[!DNL Microsoft Advertising] documentação sobre parâmetros para indicar o URL final](https://help.ads.microsoft.com/#apex/3/en/56799).

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como {lpurl}?matchtype={matchtype}&amp;dispositivo={device}.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* É possível atualizar os modelos de rastreamento em qualquer nível sem reenviar os anúncios para aprovação.

## Modelo de anúncio de texto - Nota que explica como inserir um parâmetro dinâmico {#inventory-feed-template-insert-dynamic-parameter}

Para inserir um nome de coluna ou grupo de modificadores como um parâmetro dinâmico, clique no campo de entrada e, em seguida, clique em um nome de coluna na lista de colunas ou em uma [nome do modificador](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) na lista Modificadores. Para inserir a variável [!DNL Param1] ou [!DNL Param2] insira o valor `{param1:default text}` ou `{param2:default text}`, onde &quot;texto padrão&quot; é o texto usado se a coluna de parâmetros no arquivo de feed estiver vazia em uma linha de anúncio.

## Modelo de anúncio de texto - Nota explicando como inserir um personalizador de anúncio {#inventory-feed-template-insert-ad-customizer}

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, como `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, como `{CUSTOMIZER.Discount:10%}`
