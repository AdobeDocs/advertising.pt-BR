---
title: Perguntas frequentes sobre o [!UICONTROL Household] Relatório
description: Saiba mais sobre o [!UICONTROL Household] , incluindo como é diferente de outros relatórios e solução de problemas.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Perguntas frequentes sobre o [!UICONTROL Household] Relatório

## Como [!UICONTROL Household] relatórios de alcance e frequência diferentes de outros relatórios personalizados?

O [!UICONTROL Household] As medidas de relatório atingem, impressões e frequência em várias dimensões em um nível de residência com base no endereço IP. Os outros relatórios personalizados são gerados no nível do dispositivo ou do cookie.

Por exemplo, mesmo que uma impressão seja veiculada em três dispositivos em uma residência, a métrica Alcançado único da casa é uma.

### Dimension compatíveis

O [!UICONTROL Household] O relatório suporta [seguintes dimensões](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot;[!UICONTROL Package],&quot;[!UICONTROL Placement],&quot;[!UICONTROL Site/Apps]&quot; (que não fornece acesso a métricas de sobreposição), &quot;[!UICONTROL Media Type],&quot;[!UICONTROL Feed Type],&quot;[!UICONTROL Device],&quot;[!UICONTROL Publisher],&quot;[!UICONTROL Audience],&quot;[!UICONTROL Creative Length],&quot; e inserção criada pelo usuário &quot;[!UICONTROL Tags].&quot; |

### Métricas suportadas

O [métricas disponíveis](/help/dsp/reports/report-columns.md) incluem:

* Métricas de sobreposição: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]e [!UICONTROL Unique Household (Overlap)].

   Métricas de sobreposição são os valores que ocorrem apenas para a dimensão reportada ou combinação de dimensões, e não para outras dimensões. <!-- For example, it might show the ?? -->

* Métricas de não sobreposição: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]e [!UICONTROL Unique Household Reached]

Métricas de conversão e metas personalizadas não são compatíveis.

## Qual é a diferença entre as métricas de sobreposição e não sobreposição?

A figura a seguir mostra três métricas (Alcançado único da casa, Alcançado Incremental da casa e Família Incremental (Sobreposição)) para três campanhas (A, B e C).

![Ilustração das métricas de sobreposição de residências](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustração das métricas de sobreposição de residências")

* Alcançado único da casa (Total) fornece a família exclusiva alcançada por cada campanha ou a área total de cada círculo. Na figura, agregado familiar único atingido por A = agregado familiar incremental atingido por A + (A+B) + (A+C) + (A+B+C)

* O Lado a Lado Incremental Alcançado é o Lar Único que foi alcançado apenas por uma campanha. Na figura, a Família Incremental Alcançada por A, B, C é a Família Incremental Alcançada por A, B, C, respectivamente.

* A Família Incremental (Sobreposição) é a Família Única alcançada pela campanha ou combinação de campanhas. Na figura, a Casa Incremental Alcançada por A, C é A+C.

## Fluxo de trabalho (WRK)

Siga as etapas normais para [criar um relatório personalizado](report-create.md).

O [!UICONTROL Household] relatório pode incluir apenas uma dimensão. Também pode incluir a) métricas de sobreposição por qualquer dimensão, exceto por Site/Aplicativos ou b) métricas de não sobreposição, mas não ambas.

## Quais são algumas limitações da [!UICONTROL Household] relatório? 

Relatórios com métricas de sobreposição fazem interseções de saída de até três valores. Por exemplo, se você usar a métrica [!UICONTROL Unique Household (Overlap)] em 10 disposições, é possível ver as famílias únicas atingidas por disposições individuais, as famílias comuns atingidas por uma combinação de quaisquer duas disposições e as famílias comuns atingidas por combinações de três posições. Você não pode ver famílias comuns atingidas por quatro ou mais disposições.

Para dimensões diferentes de campanha, pacote ou disposição, o relatório suporta até 10 valores em cada dimensão. Por exemplo, para gerar uma [!UICONTROL Unique Household Reached] relatório para o [!UICONTROL Audience] , o número de públicos-alvo únicos deve ser menor ou igual a 10. Se você incluir mais de 10 públicos-alvo únicos, um relatório em branco será gerado.

## Por que a frequência e os valores de alcance únicos são diferentes entre meus [!UICONTROL Custom] e [!UICONTROL Household] relatório?

Essas métricas na [!UICONTROL Household] os relatórios são calculados usando a contagem real de endereços IP, enquanto as métricas na variável [!UICONTROL Custom] use números estimados calculados usando modelos. No entanto, a discrepância deve ser inferior a 10%.

## Como configurar o relatório para a variável [!UICONTROL Placement Tags] dimensão?

Para criar tags para a disposição, [abra as configurações de posicionamento](/help/dsp/campaign-management/placements/placement-edit.md) e insira valores no [Campo Tags de disposição](/help/dsp/campaign-management/placements/placement-settings.md).
 
Quando uma disposição inclui várias tags, o relatório considera a cadeia de caracteres inteira como uma tag. O relatório inclui uma linha para cada string exclusiva.

## [!UICONTROL Household] Relatório x dados de [!DNL Advanced Measurement Services]

Para a comunicação avançada sobre o alcance e a frequência com base nas famílias, a [[!DNL Strategic Advertising Consulting] equipe](/help/dsp/introduction/advanced-measurement-services.md) O pode fornecer relatórios altamente personalizáveis junto com recomendações estratégicas holísticas. Para obter mais informações sobre [!DNL Advanced Measurement Services], entre em contato com a equipe de conta do Adobe.

### Se eu já estiver usando [!DNL Advanced Measurement Services], por que devo usar o [!UICONTROL Household] relatório?

O [!UICONTROL Household] O relatório permite que os clientes puxem métricas de alcance e frequência do nível doméstico de forma autônoma em tempo real.

### Posso usar as duas [!UICONTROL Household] relatório e [!DNL Advanced Measurement Services]? 

O caso de uso ideal é usar a variável [!UICONTROL Household] relatório e [!DNL Advanced Measurement Services] serviços de informação e consultoria em conjunto. Considere a [!UICONTROL Household] como transacional, destinado a informar otimizações diárias, e [!DNL Advanced Measurement Services] como mais estratégico, pretendia informar aprendizagens holísticas e tomar medidas associadas a objetivos empresariais abrangentes.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Configurações personalizadas de relatório](/help/dsp/reports/report-settings.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)

