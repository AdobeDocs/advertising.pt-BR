---
title: Perguntas frequentes sobre o [!UICONTROL Household] Relatório
description: Saiba mais sobre o [!UICONTROL Household] relatório, incluindo como ele é diferente de outros relatórios e solução de problemas.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Perguntas frequentes sobre o [!UICONTROL Household] Relatório

## Como estão [!UICONTROL Household] relatórios de alcance e frequência diferentes de outros relatórios personalizados?

A variável [!UICONTROL Household] O relatório mede o alcance, a impressão e a frequência em várias dimensões em um nível doméstico com base no endereço IP. Os outros relatórios personalizados são gerados no nível do dispositivo ou do cookie.

Por exemplo, mesmo que uma impressão seja transmitida a três dispositivos em uma família, a métrica Casa única atingida é uma.

### Dimension compatíveis

A variável [!UICONTROL Household] O relatório suporta a [seguintes dimensões](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (que não fornece acesso a métricas de sobreposição), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; e posicionamento criado pelo usuário &quot;[!UICONTROL Tags].&quot; |

### Métricas suportadas

A variável [métricas disponíveis](/help/dsp/reports/report-columns.md) incluem:

* Métricas de sobreposição: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], e [!UICONTROL Unique Household (Overlap)].

   Métricas de sobreposição são os valores que ocorrem apenas para a dimensão ou combinação de dimensões relatada, e não para outras dimensões. <!-- For example, it might show the ?? -->

* Métricas que não se sobrepõem: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], e [!UICONTROL Unique Household Reached]

Métricas de conversão e metas personalizadas não são compatíveis.

## Qual é a diferença entre as métricas de sobreposição e não sobreposição?

A figura a seguir mostra três métricas (Família única atingida, Família incremental atingida e Família incremental (sobreposição)) para três campanhas (A, B e C).

![Ilustração de métricas de sobreposição de residências](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustração de métricas de sobreposição de residências")

* Unique Household Reached (Total) fornece a Unique Household atingida por cada uma das campanhas ou a área total de cada um dos círculos. Na figura, Agregado único alcançado por A = Agregado incremental alcançado por A + (A+B) + (A+C) + (A+B+C)

* Domicílio Incremental Alcançado é o Domicílio Único que foi alcançado apenas por uma campanha. Na figura, Família Incremental Alcançada por A, B, C são a Família Incremental Alcançada por A, B, C respectivamente.

* Família Incremental (Sobreposição) é a Família Exclusiva atingida pela campanha ou combinação de campanhas. Na figura, o agregado incremental alcançado por A, C é A+C.

## Fluxo de trabalho (WRK)

Siga as etapas normais para [criar um relatório personalizado](report-create.md).

A variável [!UICONTROL Household] O relatório pode incluir apenas uma dimensão. Também pode incluir a) métricas de sobreposição por qualquer dimensão, exceto por sites/aplicativos ou b) métricas de não sobreposição, mas não ambas.

## Quais são algumas limitações do [!UICONTROL Household] relatório? 

Relatórios com interseções de saída de métricas de sobreposição de até três valores. Por exemplo, se você usar a métrica [!UICONTROL Unique Household (Overlap)] para 10 colocações, você pode ver as famílias únicas atingidas por colocações individuais, famílias comuns atingidas por uma combinação de duas colocações e famílias comuns atingidas por combinações de três colocações. Não é possível ver famílias comuns atingidas por quatro ou mais posicionamentos.

Para dimensões diferentes de campanha, pacote ou posicionamento, o relatório suporta até 10 valores em cada dimensão. Por exemplo, para gerar um [!UICONTROL Unique Household Reached] relatório para o [!UICONTROL Audience] , o número de públicos-alvo únicos deve ser menor ou igual a 10. Se você incluir mais de 10 públicos-alvo exclusivos, será gerado um relatório em branco.

## Por que os valores de frequência e alcance único são diferentes entre meus [!UICONTROL Custom] relatórios e a [!UICONTROL Household] relatório?

Essas métricas no [!UICONTROL Household] relatórios são calculados usando a contagem real de endereços IP, enquanto as métricas no [!UICONTROL Custom] relatar o uso de números estimados calculados usando modelos. No entanto, a discrepância deve ser inferior a 10%.

## Como configurar o relatório para o [!UICONTROL Placement Tags] dimensão?

Para criar tags para o posicionamento, [abrir as configurações de posicionamento](/help/dsp/campaign-management/placements/placement-edit.md) e insira valores na variável [Campo Tags de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).
 
Quando um posicionamento inclui várias tags, o relatório considera a string inteira como uma tag. O relatório inclui uma linha para cada sequência exclusiva.

## [!UICONTROL Household] Relatório versus dados de [!DNL Advanced Measurement Services]

Para a comunicação avançada de informações sobre o alcance e a frequência [[!DNL Strategic Advertising Consulting] equipe](/help/dsp/introduction/advanced-measurement-services.md) O pode fornecer relatórios altamente personalizáveis juntamente com recomendações estratégicas holísticas. Para obter mais informações sobre [!DNL Advanced Measurement Services], entre em contato com a equipe de conta do Adobe.

### Se eu já estiver usando [!DNL Advanced Measurement Services], por que devo usar o [!UICONTROL Household] relatório?

A variável [!UICONTROL Household] O relatório do permite que os clientes obtenham métricas de alcance e frequência em nível doméstico de forma independente e em tempo real.

### Posso usar as duas opções [!UICONTROL Household] relatório e [!DNL Advanced Measurement Services]? 

O caso de uso ideal é usar as duas [!UICONTROL Household] relatório e a [!DNL Advanced Measurement Services] serviços de relatórios e consultoria em conjunto. Considere o [!UICONTROL Household] relatar como transacional, destinado a informar otimizações diárias e [!DNL Advanced Measurement Services] como mais estratégico, destinado a informar aprendizados e vantagens holísticas vinculados a objetivos de negócios abrangentes.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Configurações do relatório personalizado](/help/dsp/reports/report-settings.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)

