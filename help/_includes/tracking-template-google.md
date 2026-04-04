---
source-git-commit: 287e8bd0c2a3c3aedbf5f1f9551823b0c4586a57
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---
# Campo Modelo de rastreamento para [!DNL Google Ads] entidades

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou a URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e também incorpora a URL da página final/de aterrissagem em um parâmetro [!DNL ValueTrack]. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Para o rastreamento de conversão do Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, o Search, Social e Commerce prefixa automaticamente seu próprio redirecionamento e código de rastreamento quando você salva o registro.

* Para obter os parâmetros compatíveis para incorporar a URL final, consulte a [[!DNL Google Ads] documentação dos [!DNL ValueTrack] formatos](https://support.google.com/google-ads/answer/6305348) compatíveis. (Vá para os parâmetros &quot;Somente modelo de rastreamento&quot; na seção sobre &quot;Parâmetros [!DNL ValueTrack] disponíveis&quot;.)

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como {lpurl}?matchtype={matchtype}&amp;device={device}.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

>[!NOTE]
>
>* Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta da Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.
