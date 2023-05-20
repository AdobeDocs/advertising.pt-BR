---
title: Práticas recomendadas para a criação de uma meta personalizada
description: Conheça as práticas recomendadas para criar metas personalizadas para definir seus eventos de sucesso.
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Práticas recomendadas para a criação de uma meta personalizada

## Metas personalizadas com uma única propriedade

Os exemplos a seguir mostram como você pode configurar metas que se destinam a uma única propriedade (métrica).

### Exemplo de uma campanha com &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; Meta de otimização

Se a meta da campanha for receita ([!UICONTROL Highest ROAS - Custom Goal]), então sua meta personalizada (objetivo) incluirá a &quot;[!UICONTROL Revenue]&quot; com um peso de um (1).

![exemplo de uma meta personalizada de ROAS com uma única propriedade](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de um equivale a um valor de um para cada US$ 1 da receita rastreada.
>
> Por exemplo, uma conversão de $250 com um peso de um é relatada como $250. Se um peso de 0,5 for atribuído à métrica de conversão, a conversão de US$ 250 será relatada como US$ 125 em publicidade em Adobe (conversão de US$ 250 * 0,5) [!UICONTROL Property Weight] = US$ 125).

### Exemplo de uma campanha com &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; Meta de otimização

Se a meta da campanha for o custo mais baixo por aquisição (CPA) e exigir apenas um evento bem-sucedido, você incluirá essa métrica (no exemplo a seguir, &quot;Envio de aplicativo&quot;). A prática recomendada é definir o peso como um (1).

![exemplo de uma meta personalizada de CPA com uma única propriedade](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de um equivale a um valor de um para cada conversão rastreada.
>
> Por exemplo, se 10 conversões de Envio de aplicativo forem rastreadas, 10 conversões de Envio de aplicativo serão relatadas.  Se à métrica de conversão for atribuído um peso de 0,5, as 10 conversões serão relatadas como cinco (5) no Adobe Advertising (10 conversões * 0,5 [!UICONTROL Property Weight] = 5).

## Metas personalizadas com várias propriedades

Há dois cenários nos quais você usaria várias propriedades em uma meta personalizada:

* Sua meta de campanha tem vários eventos de sucesso. Por exemplo, talvez você esteja anunciando mais de uma ação no site e todas estão sendo atribuídas à sua meta de CPA. O exemplo de objetivo a seguir inclui três propriedades separadas (Download de PDF, Fale conosco e Inscrição por email), cada uma com um peso de um (1), que informa ao [!DNL Adobe Sensei] que cada uma das propriedades tem a mesma importância. Se você incluir propriedades com custos ou importância variáveis, será possível ajustar seus pesos relativos de acordo.

   ![exemplo de uma meta personalizada com várias propriedades](/help/dsp/assets/custom-goal-multiple-properties.png)

* A única propriedade na sua meta personalizada não está atingindo o mínimo de 10 conversões por dia necessárias para o desempenho otimizado. Isso pode ocorrer devido ao gasto diário mínimo do pacote ou a um número limitado de conversões naturais. Adicionar outras propriedades de suporte à meta personalizada pode ajudar você a alcançar o limite de 10 conversões por dia. Dez eventos de suporte podem ajudar um pacote a atingir o limite de 10 dias, mesmo quando cada um de seus pesos estiver abaixo de um (1). Mas talvez não seja necessário adicionar tantos eventos.

   Ao adicionar propriedades de suporte a uma meta personalizada, avalie-as de acordo com sua importância relativa para o evento bem-sucedido principal e lembre-se da quantidade de pontos de dados. Isso permite que o algoritmo do Adobe Sensei equilibre várias propriedades e otimize em direção à sua meta.

   O exemplo de objetivo a seguir inclui três propriedades, cada uma com um peso diferente: Envio de aplicativo = 1, Início do aplicativo = 0.1 e Página de aterrissagem do anunciante = 0.01. Isso significa que cada conversão de envio de aplicativo tem o mesmo valor para sua empresa como uma média de 10 conversões de início de aplicativo e 100 conversões de página de aterrissagem de anunciante.

   ![exemplo de uma meta personalizada com várias propriedades](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Se, em vez disso, você ponderasse as visitas de página de aterrissagem igualmente aos envios de aplicativos, a quantidade naturalmente maior de visitas de página de aterrissagem poderia sobrecarregar sua meta e distorcer as visitas de página de aterrissagem.<!--reword-->

>[!MORELIKETHIS]
>
>* [Sobre metas personalizadas](custom-goal-about.md)
>* [Criar uma meta personalizada](custom-goal-create.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)

