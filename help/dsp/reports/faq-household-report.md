---
title: Perguntas frequentes sobre relatórios domésticos
description: Saiba mais sobre alcance, frequência e dados de conversão domésticos, incluindo como os relatórios domésticos são diferentes de outros relatórios e solução de problemas.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: ae6028d7dc9b35906e4abcd727b84b169e5594b1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Perguntas frequentes sobre relatórios domésticos

## A variável [!UICONTROL Household Reach & Frequency] Relatório

### Como estão [!UICONTROL Household Reach & Frequency] relatórios diferentes de outros relatórios personalizados?

A variável [!UICONTROL Household Reach & Frequency] O relatório mede o alcance, a impressão e a frequência em várias dimensões em um nível doméstico com base no endereço IP. Os outros relatórios personalizados são gerados no nível do dispositivo ou do cookie.

Por exemplo, mesmo que uma impressão seja transmitida a três dispositivos em uma família, a métrica Casa única atingida é uma.

#### Dimension compatíveis

A variável [!UICONTROL Household Reach & Frequency] O relatório suporta a [seguintes dimensões](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (que não fornece acesso a métricas de sobreposição), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; e posicionamento criado pelo usuário &quot;[!UICONTROL Tags].&quot; |

#### Métricas suportadas

A variável [métricas disponíveis](/help/dsp/reports/report-columns.md) incluem:

* Métricas de sobreposição: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], e [!UICONTROL Unique Household (Overlap)].

  Métricas de sobreposição são os valores que ocorrem apenas para a dimensão ou combinação de dimensões relatada, e não para outras dimensões. <!-- For example, it might show the ?? -->

* Métricas que não se sobrepõem: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], e [!UICONTROL Unique Household Reached]

Métricas de conversão e metas personalizadas não são compatíveis.

### Qual é a diferença entre as métricas de sobreposição e não sobreposição?

A figura a seguir mostra três métricas (Família única atingida, Família incremental atingida e Família incremental (sobreposição)) para três campanhas (A, B e C).

![Ilustração de métricas de sobreposição de residências](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustração de métricas de sobreposição de residências")

* Unique Household Reached (Total) fornece a Unique Household atingida por cada uma das campanhas ou a área total de cada um dos círculos. Na figura, Agregado único alcançado por A = Agregado incremental alcançado por A + (A+B) + (A+C) + (A+B+C)

* Domicílio Incremental Alcançado é o Domicílio Único que foi alcançado apenas por uma campanha. Na figura, Família Incremental Alcançada por A, B, C são a Família Incremental Alcançada por A, B, C respectivamente.

* Família Incremental (Sobreposição) é a Família Exclusiva atingida pela campanha ou combinação de campanhas. Na figura, o agregado incremental alcançado por A, C é A+C.

### Fluxo de trabalho (WRK)

Siga as etapas normais para [criar um relatório personalizado](report-create.md).

A variável [!UICONTROL Household Reach & Frequency] O relatório pode incluir apenas uma dimensão. Também pode incluir a) métricas de sobreposição por qualquer dimensão, exceto por sites/aplicativos ou b) métricas de não sobreposição, mas não ambas.

### Quais são algumas limitações do [!UICONTROL Household Reach & Frequency] relatório?

Relatórios com interseções de saída de métricas de sobreposição de até três valores. Por exemplo, se você usar a métrica [!UICONTROL Unique Household (Overlap)] para 10 colocações, você pode ver as famílias únicas atingidas por colocações individuais, famílias comuns atingidas por uma combinação de duas colocações e famílias comuns atingidas por combinações de três colocações. Não é possível ver famílias comuns atingidas por quatro ou mais posicionamentos.

Para dimensões diferentes de campanha, pacote ou posicionamento, o relatório suporta até 10 valores em cada dimensão. Por exemplo, para gerar um [!UICONTROL Unique Household Reached] relatório para o [!UICONTROL Audience] , o número de públicos-alvo únicos deve ser menor ou igual a 10. Se você incluir mais de 10 públicos-alvo exclusivos, será gerado um relatório em branco.

### Por que os valores de frequência e alcance único são diferentes entre meus [!UICONTROL Custom] relatórios e a [!UICONTROL Household Reach & Frequency] relatório?

Essas métricas no [!UICONTROL Household] relatórios são calculados usando a contagem real de endereços IP, enquanto as métricas no [!UICONTROL Custom] relatar o uso de números estimados calculados usando modelos. No entanto, a discrepância deve ser inferior a 10%.

### Como configurar o relatório para o [!UICONTROL Placement Tags] dimensão?

Para criar tags para o posicionamento, [abrir as configurações de posicionamento](/help/dsp/campaign-management/placements/placement-edit.md) e insira valores na variável [Campo Tags de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

Quando um posicionamento inclui várias tags, o relatório considera a string inteira como uma tag. O relatório inclui uma linha para cada sequência exclusiva.

## A variável [!UICONTROL Household Conversions] Relatório

### Quais são os tipos de métodos de atribuição compatíveis com o [!UICONTROL Household Conversions] relatório?

Há suporte para dois tipos de métodos de atribuição:

* Exclusivo: conta o número de vezes que um valor de dimensão (como um dispositivo ou um posicionamento) estava no caminho para conversão.

* MTA (Atribuição multitoque): distribui o crédito de cada conversão com base na frequência de ocorrência do valor da dimensão (como um dispositivo ou posicionamento) no caminho para a conversão. Por exemplo, se houvesse um total de 10 impressões antes da conversão, com 8 no CTV e 2 no Mobile, então 80% do crédito (0,8) é dado para telas de CTV e 0,2 para o Mobile.

### Como os relatórios de conversão doméstica diferem dos relatórios de view-through de CTV no Adobe Analytics?

Dados de view-through de CTV no [!DNL Analytics] é ativado [!DNL Analytics] e os dados de conversão da família usam os dados coletados pelo rastreamento de conversão do Adobe Advertising. Além disso, a lógica de atribuição do DSP no [!DNL Analytics] O usa somente o último evento, mas os relatórios de conversão da família são compatíveis com dois métodos de atribuição diferentes: exclusivo e MTA.

### Posso exibir dados de view-through de CTV em ambos [!DNL Analytics for Advertising] e nos relatórios personalizados?

Anunciantes sem [!DNL Analytics for Advertising] O pode usar somente o Relatório de Conversão de Famílias para emissão de relatórios de conversão de famílias.

Se sua organização tiver [!DNL Analytics for Advertising], use os dois tipos de relatórios juntos. Embora os relatórios de view-through de CTV sejam adequados para uma análise mais ampla do canal, comportamento do site e assim por diante, os relatórios personalizados fornecem uma visualização granular (com dados divididos por tipo de mídia, editores e assim por diante) para indicar os fatores que impulsionam as taxas de conversão.

## [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] Relatórios versus dados de [!DNL Advanced Measurement Services]

Para a comunicação avançada de informações sobre o alcance e a frequência ou conversões [[!DNL Strategic Advertising Consulting] equipe](/help/dsp/introduction/advanced-measurement-services.md) O pode fornecer relatórios altamente personalizáveis juntamente com recomendações estratégicas holísticas. Para obter mais informações sobre [!DNL Advanced Measurement Services], entre em contato com a equipe de conta do Adobe.

### Se eu já estiver usando [!DNL Advanced Measurement Services], por que devo usar o [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] relatórios?

A variável [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] Os relatórios do permitem que os clientes obtenham métricas de alcance, frequência e conversão de nível doméstico, respectivamente, de forma independente e em tempo real.

### Posso usar as duas opções [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] relatórios e [!DNL Advanced Measurement Services]?

O caso de uso ideal é usar as duas [!UICONTROL Household] relatório e a [!DNL Advanced Measurement Services] serviços de relatórios e consultoria em conjunto. Considere o [!UICONTROL Household] relatar como transacional, destinado a informar otimizações diárias e [!DNL Advanced Measurement Services] como mais estratégico, destinado a informar aprendizados e vantagens holísticas vinculados a objetivos de negócios abrangentes.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Configurações do relatório personalizado](/help/dsp/reports/report-settings.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
