---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Campo Modelo de rastreamento para o Yahoo! Entidades de anúncios do Japão

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da página de aterrissagem e também incorpora o URL da página final/de aterrissagem em um parâmetro. Usar o parâmetro `!{lpurl}` para indicar o URL da landing page. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

Para rastreamento de conversão de anúncio de Adobe, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.

>[!NOTE]
>
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* É possível atualizar os modelos de rastreamento em qualquer nível sem reenviar os anúncios para aprovação.

