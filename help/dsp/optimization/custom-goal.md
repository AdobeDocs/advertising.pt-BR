---
title: Práticas recomendadas para metas personalizadas
description: Saiba mais sobre as práticas recomendadas para definir metas personalizadas para pacotes otimizados para o CPA mais baixo ou para o ROAS mais alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# Práticas recomendadas para metas personalizadas

As metas personalizadas definem os eventos de sucesso que um anunciante precisa para atender aos seus objetivos de negócios. Cada pacote que usa a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve incluir uma meta personalizada para ajudar a alcançar a meta de otimização geral. Você pode criar metas personalizadas como *[objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)*.

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Cada meta personalizada (objetivo) consiste em uma ou mais métricas de conversão a serem rastreadas e otimizadas e nos pesos relativos dessas métricas. Você pode [atribuir uma meta personalizada a um pacote](/help/dsp/campaign-management/packages/package-settings.md) para otimização de relatórios e algoritmos usando o [!DNL Adobe AI].

Para criar e gerenciar metas personalizadas, consulte &quot;[Gerenciar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)&quot;.

## Metas personalizadas com uma única métrica

Os exemplos a seguir mostram como você pode configurar metas que têm como alvo uma única métrica de conversão.

### Exemplo de campanha com a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Se a meta da campanha for receita ([!UICONTROL Highest Return on Ad Spend (ROAS)]) e a receita de todos os tipos de dispositivos for igualmente importante para você, inclua a métrica &quot;[!UICONTROL Revenue]&quot; com um peso de um (1). Selecione o tipo de métrica *[!UICONTROL Goal]*.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Um peso de um (1) equivale a um valor de um (1) para cada US$ 1 da receita rastreada para anúncios de exibição em qualquer dispositivo. Por exemplo, uma conversão de $250 com um peso de um (1) é relatada como $250 para conversões. Se um peso de 0,5 for atribuído à métrica de conversão, a conversão de US$ 250 será relatada como US$ 125 no Adobe Advertising (conversão de US$ 250 * 0,5 [!UICONTROL weight] = US$ 125).

### Exemplo de campanha com a meta de otimização &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Se a meta da campanha for o custo mais baixo por aquisição (CPA) e exigir apenas um evento bem-sucedido (como &quot;Envio de aplicativo&quot;), inclua essa métrica e especifique o tipo de métrica como *[!UICONTROL Goal]*. A prática recomendada é definir o peso como um (1).

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Um peso de um (1) equivale a um valor de um (1) para cada conversão rastreada para anúncios de exibição em qualquer dispositivo. Por exemplo, se 10 conversões de Envio de aplicativo forem rastreadas, 10 conversões de Envio de aplicativo serão relatadas. No entanto, se for atribuído um peso de 0,5 à métrica de conversão, as 10 conversões serão relatadas como cinco (5) no Adobe Advertising (10 conversões * 0,5 [!UICONTROL weight] = 5).

## Metas personalizadas com várias métricas

Há dois cenários nos quais você usaria várias métricas em uma meta personalizada:

* Sua meta de campanha tem vários eventos de sucesso. Por exemplo, talvez você esteja anunciando mais de uma ação no site (Download do PDF, Fale Conosco e Cadastro por email) e todas as ações contribuem para sua meta de CPA. Se o objetivo incluir as três métricas separadas, cada uma com pesos de um (1), o algoritmo [!DNL Adobe AI] tratará cada uma das métricas e tipos de dispositivo do usuário com importância igual. Se as diferentes métricas tiverem custos ou importância variáveis, ajuste seus pesos relativos de acordo.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* A única métrica de conversão em sua meta personalizada não está atingindo o mínimo de 10 conversões por dia necessárias para o desempenho otimizado. Um número menor de conversões pode ocorrer devido ao gasto diário mínimo do pacote ou a um número limitado de conversões naturais. Adicionar métricas de suporte adicionais à meta personalizada pode ajudar você a alcançar o limite de 10 conversões por dia. Dez eventos de suporte podem ajudar um pacote a atingir o limite de 10 dias, mesmo quando cada um de seus pesos estiver abaixo de um (1). Mas talvez não seja necessário adicionar tantos eventos.

  Ao adicionar métricas de suporte a uma meta personalizada, avalie-as de acordo com sua importância relativa para o evento bem-sucedido principal e lembre-se da quantidade de pontos de dados. Isso permite que o algoritmo [!DNL Adobe AI] equilibre várias métricas e otimize em direção à sua meta.

  O exemplo de objetivo a seguir inclui três métricas, cada uma com um peso diferente: Envio de aplicativo = 1, Início do aplicativo = 0.1 e Página de aterrissagem do anunciante = 0.01. Isso significa que cada conversão de envio de aplicativo tem o mesmo valor para sua empresa como uma média de 10 conversões de início de aplicativo e 100 conversões de página de aterrissagem de anunciante.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Se, em vez disso, você ponderasse as visitas de página de aterrissagem igualmente aos envios de aplicativos, a quantidade naturalmente maior de visitas de página de aterrissagem poderia sobrecarregar sua meta e distorcer a otimização em direção às visitas de página de aterrissagem.

>[!MORELIKETHIS]
>
>* [Gerenciar objetivos personalizados](/help/dsp/admin/custom-objectives-manage.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Como a DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
