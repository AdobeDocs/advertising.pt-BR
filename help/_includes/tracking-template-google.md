---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Campo Modelo de rastreamento para entidades do Google Ads

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da página inicial, e também incorpora o URL da página final/de aterrissagem em uma [!DNL ValueTrack] parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Para rastreamento de conversão de anúncio de Adobe, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

* Para obter os parâmetros compatíveis que incorporam o URL final, consulte a [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] formatos](https://support.google.com/google-ads/answer/6305348). (Vá para os parâmetros &quot;Modelo de rastreamento somente&quot; na seção em &quot;Parâmetros ValueTrack disponíveis&quot;.)

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como {lpurl}?matchtype={matchtype}&amp;device={device}.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

>[!NOTE]
>
>* Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* Se você atualizar um modelo de rastreamento no nível de anúncio, link do site ou palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.

