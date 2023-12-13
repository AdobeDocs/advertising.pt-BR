---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Campo Modelo de rastreamento para entidades do Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional; não disponível para todas as entidades) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da aterrissagem e também incorpora o URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Para rastreamento de conversão de Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

* Para obter os parâmetros compatíveis que incorporam o URL final, consulte a [[!DNL Microsoft Advertising] documentação sobre parâmetros para indicar o URL final](https://help.ads.microsoft.com/#apex/3/en/56799).

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como {lpurl}?matchtype={matchtype}&amp;dispositivo={device}.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* É possível atualizar os modelos de rastreamento em qualquer nível sem reenviar os anúncios para aprovação.
