---
title: Sobre metas personalizadas
description: Saiba mais sobre as metas personalizadas para definir seus eventos de sucesso em pacotes otimizados para o CPA mais baixo ou o ROAS mais alto.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Sobre metas personalizadas

As metas personalizadas definem os eventos de sucesso que um anunciante precisa para atender aos seus objetivos de negócios. Cada pacote que usa uma meta de otimização que termina com &quot;[!UICONTROL - Custom Goal]&quot; (como &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;) deve incluir uma meta personalizada que ajudará a alcançar a meta de otimização geral. Você pode criar metas personalizadas como *objetivos* in [!DNL Advertising Search, Social, & Commerce].

![metas personalizadas](/help/dsp/assets/objective-goals.png)

Cada meta personalizada consiste em uma ou mais métricas de conversão e os pesos relativos dessas métricas. As métricas de conversão disponíveis incluem todas as métricas rastreadas usando o pixel de conversão de Adobe Advertising e por meio do Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensões e segmentos não estão disponíveis para otimização de Adobe Advertising.
>* Para usar os eventos do Analytics no DSP, trabalhe com a equipe de conta do Adobe para configurar uma integração no nível do anunciante.
>* [!DNL Analytics] os eventos personalizados seguem esta convenção de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid`

Por exemplo, suponha que três métricas de conversão sejam relevantes para um pacote específico em uma de suas campanhas: &quot;Download de PDF&quot; com valor de 20 USD, &quot;Inscrição em email&quot; com valor de 30 USD e &quot;Confirmação de pedido&quot; com valor de 40 USD. Se você quiser atribuir peso de acordo com o valor monetário único da ação do cliente, os pesos relativos das propriedades serão 1, 2 e 1,5.

Consulte a [práticas recomendadas para criar metas personalizadas](custom-goal-best-practices.md) para obter dicas sobre como configurar suas metas personalizadas.

Uma vez que [criar uma meta personalizada](custom-goal-create.md), você pode [atribuir a um pacote](/help/dsp/campaign-management/packages/package-settings.md) para otimização de relatórios e algorítmicos usando o Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Criar uma meta personalizada](custom-goal-create.md)
>* [Práticas recomendadas para a criação de uma meta personalizada](custom-goal-best-practices.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
