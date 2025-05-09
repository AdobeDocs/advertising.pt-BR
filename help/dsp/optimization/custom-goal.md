---
title: Metas personalizadas
description: Saiba mais sobre as metas personalizadas para definir seus eventos de sucesso em pacotes otimizados para o CPA mais baixo ou o ROAS mais alto.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Metas personalizadas

As metas personalizadas definem os eventos de sucesso que um anunciante precisa para atender aos seus objetivos de negócios. Cada pacote que usa a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve incluir uma meta personalizada para ajudar a alcançar a meta de otimização geral. Você pode criar metas personalizadas como *objetivos* em [!DNL Advertising Search, Social, & Commerce]. O nome de cada objetivo do DSP deve receber o prefixo &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Cada meta personalizada (objetivo) consiste em uma ou mais métricas de conversão e os pesos relativos dessas métricas. As métricas de conversão disponíveis incluem todas as métricas rastreadas usando o pixel de conversão do Adobe Advertising e por meio do Adobe Analytics. Somente os pesos não móveis são considerados para metas personalizadas do DSP, mas são usados para todos os tipos de anúncios.

Por exemplo, suponha que três métricas de conversão sejam relevantes para um pacote específico em uma de suas campanhas: &quot;Download do PDF&quot; avaliado em 20 USD, &quot;Inscrição em email&quot; avaliado em 30 USD e &quot;Confirmação de pedido&quot; avaliado em 40 USD. Se você quiser atribuir peso de acordo com o valor monetário único da ação do cliente, os pesos relativos das métricas serão 1, 1,5 e 2.

Depois de [criar uma meta personalizada](#custom-goal-create), você pode [atribuí-la a um pacote](/help/dsp/campaign-management/packages/package-settings.md) para otimização de relatórios e algoritmos usando o Adobe Sensei.

As recomendações de peso são geradas automaticamente para métricas atribuídas pelo DSP em objetivos e podem aplicar todas as recomendações de peso com um clique. Todas as alterações de peso nos objetivos com o prefixo &quot;ADSP_&quot; são aplicadas de forma algorítmica no DSP dentro de dois dias. Para obter mais informações sobre recomendações de peso, consulte o capítulo do Guia de otimização em &quot;(Beta) Novos objetivos&quot;, que está disponível no Search, Social e Commerce.

## Criar uma meta personalizada {#custom-goal-create}

Para criar uma meta personalizada, a conta do DSP deve estar vinculada a uma conta do [!DNL Search, Social, & Commerce] com a mesma ID de organização da Adobe Experience Cloud, nas configurações de cliente do [!DNL Search, Social, & Commerce]. Se sua conta do DSP não estiver vinculada a uma conta do [!DNL Search, Social, & Commerce], entre em contato com a equipe de conta da Adobe.

1. Entre no [!DNL Advertising Search, Social, & Commerce] em (usuários na América do Norte) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (todos os outros usuários) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Verifique se as métricas que você deseja incluir em sua meta foram rastreadas, estão disponíveis no produto e incluem um nome de exibição:

   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Localize a métrica e verifique se **[!UICONTROL Show in UI and Reports]** está habilitado para a métrica.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventos personalizados seguem esta convenção de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid`

   1. Se a métrica não tiver um valor na coluna **[!UICONTROL Display Name]**, clique na célula, digite o nome de exibição e clique em **[!UICONTROL Apply].**

1. Criar a meta personalizada como um *objetivo*:

   1. No menu principal, clique em **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Na barra de ferramentas, clique em ![Criar](/help/dsp/assets/create-search-ui.png "Criar").

   1. Insira as configurações do objetivo, incluindo as métricas associadas e seus pesos numéricos relativos para dispositivos não móveis, e salve o objetivo. Considere o seguinte:

      * Para objetivos usados para pacotes do Advertising DSP, o nome do objetivo deve ter o prefixo &quot;ADSP_&quot; como &quot;ADSP_Registrations&quot;. O prefixo não diferencia maiúsculas de minúsculas.

      * Incluir somente métricas atribuídas ao DSP. Qualquer métrica atribuída à Pesquisa, Social e Commerce ou a qualquer outra rede de anúncios é ignorada.

      * Pelo menos uma métrica deve ter o tipo de métrica *[!UICONTROL Goal]*.

      * O DSP usa os pesos não móveis para todos os anúncios. Quaisquer pesos móveis especificados são ignorados.

      >[!NOTE]
      >
      >* [!DNL Analytics] eventos personalizados seguem esta convenção de nomenclatura: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemplo: `custom_event_16_examplersid`
      >* [!DNL Analytics] dimensões e segmentos não estão disponíveis para otimização do Adobe Advertising.

      >[!TIP]
      >
      >Para obter o desempenho ideal, as métricas combinadas na meta personalizada (objetivo) devem totalizar pelo menos dez conversões por dia. Caso contrário, a prática recomendada é adicionar outras métricas de conversão de suporte, como páginas de produtos ou inícios de aplicativos, ao objetivo. Consulte [Práticas recomendadas para criar uma meta personalizada](#custom-goal-best-practices) para obter diretrizes.

Nas configurações de pacote do DSP para pacotes que usam a meta de otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, o nome do objetivo agora está incluído na lista [!UICONTROL Custom Goals]. Quando você seleciona o objetivo como meta personalizada para um pacote, a lista [!UICONTROL Conversion Metric] inclui todas as métricas de meta para o objetivo.

## Práticas recomendadas para a criação de uma meta personalizada {#custom-goal-best-practices}

### Metas personalizadas com uma única métrica

Os exemplos a seguir mostram como você pode configurar metas que têm como alvo uma única métrica de conversão.

#### Exemplo de uma Campanha com a Meta de Otimização &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Se a meta da campanha for receita ([!UICONTROL Highest Return on Ad Spend (ROAS)]) e a receita de todos os tipos de dispositivos for igualmente importante para você, inclua a métrica &quot;[!UICONTROL Revenue]&quot; com um peso não móvel de um (1); o peso móvel será ignorado. Selecione o tipo de métrica *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Um peso não móvel de um (1) equivale a um valor de um (1) para cada US$ 1 da receita rastreada para anúncios de exibição em qualquer dispositivo. Por exemplo, uma conversão de $250 com um peso não móvel de um (1) é relatada como $250 para conversões. Se for atribuído um peso não móvel de 0,5 à métrica de conversão, a conversão de US$ 250 será relatada como US$ 125 no Adobe Advertising (conversão de US$ 250 * 0,5 [!UICONTROL Non-mobile Weight] = US$ 125).

#### Exemplo de uma Campanha com a Meta de Otimização &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Se a meta da campanha for o custo mais baixo por aquisição (CPA) e exigir apenas um evento bem-sucedido (como &quot;Envio de aplicativo&quot;), inclua essa métrica e especifique o tipo de métrica como *[!UICONTROL Goal]*. A prática recomendada é definir o peso não móvel como um (1); o peso móvel é ignorado.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Um peso não móvel de um (1) equivale a um valor de um (1) para cada conversão rastreada para anúncios de exibição em qualquer dispositivo. Por exemplo, se 10 conversões de Envio de aplicativo forem rastreadas, 10 conversões de Envio de aplicativo serão relatadas. No entanto, se for atribuído um peso não móvel de 0,5 à métrica de conversão, as 10 conversões serão relatadas como cinco (5) no Adobe Advertising (10 conversões * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Metas personalizadas com várias métricas

Há dois cenários nos quais você usaria várias métricas em uma meta personalizada:

* Sua meta de campanha tem vários eventos de sucesso. Por exemplo, talvez você esteja anunciando mais de uma ação no site (Download do PDF, Fale Conosco e Cadastro por email) e todas as ações contribuem para sua meta de CPA. Se o objetivo incluir as três métricas separadas, cada uma com pesos não móveis de um (1), o algoritmo [!DNL Adobe Sensei] tratará cada uma das métricas e tipos de dispositivos de usuário com igual importância. Se as diferentes métricas tiverem custos ou importância variáveis, você ajustará seus pesos relativos de acordo.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* A única métrica de conversão em sua meta personalizada não está atingindo o mínimo de 10 conversões por dia necessárias para o desempenho otimizado. Isso pode ocorrer devido ao gasto diário mínimo do pacote ou a um número limitado de conversões naturais. Adicionar métricas de suporte adicionais à meta personalizada pode ajudar você a alcançar o limite de 10 conversões por dia. Dez eventos de suporte podem ajudar um pacote a atingir o limite de 10 dias, mesmo quando cada um de seus pesos estiver abaixo de um (1). Mas talvez não seja necessário adicionar tantos eventos.

  Ao adicionar métricas de suporte a uma meta personalizada, avalie-as de acordo com sua importância relativa para o evento bem-sucedido principal e lembre-se da quantidade de pontos de dados. Isso permite que o algoritmo do Adobe Sensei equilibre várias métricas e otimize em direção à sua meta.

  O exemplo de objetivo a seguir inclui três métricas, cada uma com um peso não móvel diferente: Envio de aplicativo = 1, Início do aplicativo = 0.1 e Página de aterrissagem do anunciante = 0.01. Isso significa que cada conversão de envio de aplicativo tem o mesmo valor para sua empresa como uma média de 10 conversões de início de aplicativo e 100 conversões de página de aterrissagem de anunciante.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Se, em vez disso, você ponderar as visitas à página de aterrissagem igualmente aos envios de aplicativos, a quantidade naturalmente maior de visitas à página de aterrissagem poderá sobrecarregar sua meta e inclinar as visitas à página de aterrissagem.<!--reword-->

>[!MORELIKETHIS]
>
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como a DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
