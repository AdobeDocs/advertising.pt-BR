---
title: Casos de uso
description: Saiba mais sobre casos de uso para compartilhar dados de mídia do Advertising DSP com o Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
TQID: https://experienceleague.adobe.com/bEvS7Wb-Xk0nHAchL60c3AUNm7K4S2p3tBxJ2aWWevA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 730
ht-degree: 0%

---

# Casos de uso para capturar dados de exposição da mídia no Adobe Audience Manager

*Somente anunciantes com o Advertising DSP*

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Audience Manager*

Veja a seguir algumas maneiras de se beneficiar da captura dos dados de exposição da mídia do Advertising DSP <!-- ad impression data? --> no Audience Manager.

## Gerenciamento de recenticidade e frequência

A captura de dados de impressão no Audience Manager permite aprimorar o gerenciamento de frequência criando segmentos de usuários que foram expostos a um anúncio ou campanha específica. Você pode usar esses segmentos para o direcionamento de anúncios se quiser aumentar a frequência ou para a supressão de anúncios se quiser limitar a frequência.

Além disso, com o Audience Manager [!DNL Segment Builder], você pode aplicar [controles de recenticidade e frequência](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a qualquer [característica baseada em regras](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) que contenha sinais acionáveis. Isso permite, por exemplo, limitar o número de vezes que um usuário recebe um anúncio específico em uma campanha de mídia. Leia &quot;[Supressão instantânea entre dispositivos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; para saber como fazer isso.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Mensagens sequenciais

Capturando dados de impressão, você pode criar um segmento de usuários que foram expostos a uma campanha ou anúncio e usar esse segmento para mensagens sequenciais ou supressão. Por exemplo, é possível redirecionar usuários que viram o criativo `123`, mas não clicaram ou converteram ao mostrá-los como criativos `456`.

Para executar este exemplo no Audience Manager, siga estas etapas:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Crie uma característica para capturar os usuários que viram o criativo.

   Por exemplo, para nomear a característica `Creative Trait 123`, use a seguinte regra de característica:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Crie uma característica para capturar usuários que clicam ou convertem.

   Por exemplo, para nomear esta característica `Click and Converter`, use a seguinte regra de característica:

   ```
   d_event == click OR d_event=conv
   ```

1. Crie um segmento chamado `Retarget Users` para popular com usuários que viram o criativo `123`, mas não clicaram nem converteram. Use a seguinte regra de característica:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mapeie o segmento `Retarget Users` para um destino e direcione usuários no destino com a `456` criativa.

## [!DNL Adobe Audience Analytics] e dados de exposição da campanha

Quando os dados de impressão da campanha e cliques estiverem disponíveis no Audience Manager, você poderá criar características e segmentos de usuários que foram expostos a uma campanha ou tática específica ou que interagiram com ela. Com uma [[!DNL Audience Analytics] integração](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=pt-BR), seus segmentos do Audience Manager podem ser sincronizados com o [!DNL Analytics] para análise adicional. Os possíveis casos de uso incluem:

* **Análise de interação entre o DSP e [!DNL Advertising Search, Social, & Commerce] anúncios:** A [[!DNL Analytics for Advertising] integração](/help/integrations/analytics/overview.md) padrão não fornece insights sobre a interação entre o DSP e o [!DNL Search, Social, & Commerce] porque ambos os canais usam IDs AMO que seguem as regras de atribuição da ID AMO, para as quais um clique de pesquisa substitui um view-through. Ao criar um segmento de exposição do DSP no Audience Manager, você pode usar o [!DNL Audience Analytics] para analisar a interação entre o DSP e os anúncios [!DNL Search, Social, & Commerce] no [!DNL Analytics].

* **Análise de frequência:** você pode criar segmentos no Audience Manager com base no número de vezes que um usuário foi exposto a um anúncio ou campanha específica. Em seguida, você pode analisar os diferentes segmentos de exposição no Analytics para ver como o comportamento do usuário muda, dependendo do número de exposições da DSP.

## [!DNL Audience Optimization Reports]

Você pode aproveitar a [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=pt-BR) para identificar oportunidades de desempenho em potencial para segmentos em suas campanhas. Esses relatórios combinam dados de impressão da campanha, cliques e conversão com métricas de segmento para informar otimizações centradas em segmentos e uma combinação eficaz de canais.

### Tipos de relatórios relevantes do Audience Optimization

| Relatório | Descrição |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=pt-BR) | Compara segmentos mapeados e não mapeados por impressões e taxas de conversão. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Relatórios]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Retorne dados sobre impressões, taxas de click-through e conversões para uma grande variedade de dimensões de publicidade. |
| [[!UICONTROL Optimal Frequency] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=pt-BR) | Ajuda a descobrir o equilíbrio ideal entre o número de impressões e conversões fornecidas. Ela permite ajustar o número de impressões a serem exibidas antes de começar a ver retornos decrescentes. |
| [[!UICONTROL Unique User Reach] Relatório](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=pt-BR) | Um gráfico de bolhas, no qual cada bolha é dimensionada em proporção direta ao número de usuários únicos para a dimensão selecionada. |

### Considerações

* Se [!DNL Audience Optimization Reports] usuários tiverem controles de acesso com base em função (RBAC), [!DNL Adobe Customer Care] deverá configurar um mapeamento entre a ID do anunciante e o código de integração da fonte de dados do Audience Manager da organização. Os usuários administradores podem, então, fornecer direitos RBAC a diferentes usuários.

* O relatório de conversão em [!DNL Audience Optimization Reports] requer alguma configuração pelo usuário final. Os usuários devem preencher arquivos de metadados.

* [!DNL Audience Optimization Reports] não dá suporte a alterações nos metadados da campanha (como nome da campanha ou nome de posicionamento).

* Os cliques nos anúncios de pesquisa são incluídos no [!DNL Audience Optimization Reports] somente quando estão correlacionados com impressões. Em outras palavras, os cliques de pesquisa são tratados como conversões após as impressões. Como resultado, muitos cliques de pesquisa podem não ser incluídos em [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Visão geral do envio de dados de exposição de mídia do DSP para o Adobe Audience Manager](overview.md)
>* [Coletar dados de clique e impressão de campanhas do Advertising DSP](collect.md)
