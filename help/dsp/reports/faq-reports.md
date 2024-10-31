---
title: Perguntas frequentes sobre relatórios personalizados
description: Saiba mais sobre relatórios personalizados, incluindo relatórios domésticos e relatórios de análise do caminho de conversão.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: cb3eed4629c66283e0de18f7287169ec6e501aaa
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---

# Perguntas frequentes sobre relatórios personalizados

## Relatórios do Agregado

### O Relatório [!UICONTROL Household Reach & Frequency]

#### Qual a diferença entre os relatórios do [!UICONTROL Household Reach & Frequency] e de outros relatórios personalizados?

O relatório [!UICONTROL Household Reach & Frequency] mede o alcance, a impressão e a frequência em várias dimensões em um nível doméstico com base no endereço IP. Os outros relatórios personalizados são gerados no nível do dispositivo ou do cookie.

Por exemplo, mesmo que uma impressão seja transmitida a três dispositivos em uma família, a métrica Casa única atingida é uma.

##### Dimension compatíveis

O relatório [!UICONTROL Household Reach & Frequency] oferece suporte às [seguintes dimensões](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (que não fornece acesso a métricas de sobreposição), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length]&quot; e ao posicionamento criado pelo usuário &quot;[!UICONTROL Tags].&quot; |

##### Métricas suportadas

As [métricas disponíveis](/help/dsp/reports/report-columns.md) incluem:

* Métricas de sobreposição: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] e [!UICONTROL Unique Household (Overlap)].

  Métricas de sobreposição são os valores que ocorrem apenas para a dimensão ou combinação de dimensões relatada, e não para outras dimensões. <!-- For example, it might show the ?? -->

* Métricas não sobrepostas: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] e [!UICONTROL Unique Household Reached]

Métricas de conversão e metas personalizadas não são compatíveis.

#### Qual é a diferença entre as métricas de sobreposição e não sobreposição?

A figura a seguir mostra três métricas (Família única atingida, Família incremental atingida e Família incremental (sobreposição)) para três campanhas (A, B e C).

![Ilustração de métricas de sobreposição doméstica](/help/dsp/assets/household-overlap-metrics-illustration.png "Ilustração de métricas de sobreposição doméstica")

* Unique Household Reached (Total) fornece a Unique Household atingida por cada uma das campanhas ou a área total de cada um dos círculos. Na figura, Agregado único alcançado por A = Agregado incremental alcançado por A + (A+B) + (A+C) + (A+B+C)

* Domicílio Incremental Alcançado é o Domicílio Único que foi alcançado apenas por uma campanha. Na figura, Família Incremental Alcançada por A, B, C são a Família Incremental Alcançada por A, B, C respectivamente.

* Família Incremental (Sobreposição) é a Família Exclusiva atingida pela campanha ou combinação de campanhas. Na figura, o agregado incremental alcançado por A, C é A+C.

#### Fluxo de trabalho (WRK)

Siga as etapas normais para [criar um relatório personalizado](report-create.md).

O relatório [!UICONTROL Household Reach & Frequency] pode incluir apenas uma dimensão. Também pode incluir a) métricas de sobreposição por qualquer dimensão, exceto por sites/aplicativos ou b) métricas de não sobreposição, mas não ambas.

#### Quais são algumas limitações do relatório [!UICONTROL Household Reach & Frequency]?

Relatórios com interseções de saída de métricas de sobreposição de até três valores. Por exemplo, se você usar a métrica [!UICONTROL Unique Household (Overlap)] para 10 posicionamentos, será possível ver os ambientes únicos alcançados por posicionamentos individuais, ambientes comuns alcançados por uma combinação de dois posicionamentos quaisquer e ambientes comuns alcançados por combinações de três posicionamentos quaisquer. Não é possível ver famílias comuns atingidas por quatro ou mais posicionamentos.

Para dimensões diferentes de campanha, pacote ou posicionamento, o relatório suporta até 10 valores em cada dimensão. Por exemplo, para gerar um relatório [!UICONTROL Unique Household Reached] para a dimensão [!UICONTROL Audience], o número de públicos-alvo únicos deve ser menor ou igual a 10. Se você incluir mais de 10 públicos-alvo exclusivos, será gerado um relatório em branco.

#### Por que a frequência e os valores de alcance exclusivos são diferentes entre meus relatórios [!UICONTROL Custom] e o relatório [!UICONTROL Household Reach & Frequency]?

Essas métricas nos relatórios [!UICONTROL Household] são calculadas com a contagem real de endereços IP, enquanto as métricas no relatório [!UICONTROL Custom] usam números estimados calculados com modelos. No entanto, a discrepância deve ser inferior a 10%.

#### Como configurar o relatório para a dimensão [!UICONTROL Placement Tags]?

Para criar marcas para o posicionamento, [abra as configurações de posicionamento](/help/dsp/campaign-management/placements/placement-edit.md) e insira valores no [campo Marcas de Posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

Quando um posicionamento inclui várias tags, o relatório considera a string inteira como uma tag. O relatório inclui uma linha para cada sequência exclusiva.

### O Relatório [!UICONTROL Household Conversions]

#### Quais métodos de atribuição são suportados no relatório [!UICONTROL Household Conversions]?

Há suporte para dois tipos de métodos de atribuição:

* [!UICONTROL Unique]: Conta o número de vezes que um valor de dimensão (como um dispositivo ou posicionamento) estava no caminho para conversão.

* [!UICONTROL Multi-Touch Attribution (MTA)]: distribui o crédito de cada conversão com base na frequência de ocorrência do valor da dimensão (como um dispositivo ou posicionamento) no caminho para a conversão. Por exemplo, se houvesse um total de 10 impressões antes da conversão, com 8 no CTV e 2 no Mobile, então 80% do crédito (0,8) é dado para telas de CTV e 0,2 para o Mobile.

#### Como os relatórios de conversão doméstica diferem dos relatórios de view-through de CTV no Adobe Analytics?

Os dados de view-through de CTV em [!DNL Analytics] são viabilizados pelo rastreamento de [!DNL Analytics], e os dados de conversão doméstica usam os dados coletados pelo rastreamento de conversão de Adobe Advertising. Além disso, a lógica de atribuição do DSP em [!DNL Analytics] usa apenas o último evento, mas os relatórios de conversão doméstica oferecem suporte a dois métodos de atribuição diferentes: Exclusivo e MTA.

#### É possível exibir dados de view-through de CTV em [!DNL Analytics for Advertising] e em relatórios personalizados?

Anunciantes sem [!DNL Analytics for Advertising] podem usar somente o Relatório de Conversão Doméstica para relatórios de conversão doméstica.

Se sua organização tiver o [!DNL Analytics for Advertising], use os dois tipos de relatórios juntos. Embora os relatórios de view-through de CTV sejam adequados para uma análise mais ampla do canal, comportamento do site e assim por diante, os relatórios personalizados fornecem uma visualização granular (com dados divididos por tipo de mídia, editores e assim por diante) para indicar os fatores que impulsionam as taxas de conversão.

### [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] Relatórios vs. Dados de [!DNL Advanced Measurement Services]

Para relatórios avançados sobre alcance e frequência ou conversões domésticos, a [[!DNL Strategic Advertising Consulting] equipe](/help/dsp/introduction/advanced-measurement-services.md) pode fornecer relatórios altamente personalizáveis, juntamente com recomendações estratégicas holísticas. Para obter mais informações sobre [!DNL Advanced Measurement Services], contate a equipe de conta do Adobe.

#### Se eu já estiver usando o [!DNL Advanced Measurement Services], por que devo usar os relatórios [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions]?

Os relatórios [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] capacitam os clientes a obter métricas de alcance, frequência e conversão de nível doméstico, respectivamente, de forma independente e em tempo real.

#### Posso usar os relatórios [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] e o [!DNL Advanced Measurement Services]?

O caso de uso ideal é usar o relatório [!UICONTROL Household] e os serviços de relatórios e consultoria [!DNL Advanced Measurement Services] juntos. Considere o relatório [!UICONTROL Household] como transacional, destinado a informar otimizações diárias, e [!DNL Advanced Measurement Services] como mais estratégico, destinado a informar aprendizados holísticos e vantagens vinculados a objetivos comerciais abrangentes.

## Relatórios de análise de caminho de conversão

### Como o relatório Caminho para conversão se compara aos relatórios criados por [!DNL Advanced Measurement Services] e Adobe Analytics Analysis Workspace?

| | Caminho para o relatório de conversão | Efeito de Halo dos Serviços de Medição Avançados nos Relatórios de Pesquisa | Relatórios no Analysis Workspace |
| --- | --- | --- |---|
| Valor para o cliente | Gerar um relatório personalizado de autoatendimento para entender quais caminhos da jornada de anúncios levaram a mais conversões para aumentar a otimização | Compreender a influência das táticas de TV conectada (CTV) nos cliques de pesquisa | Entenda a influência de seu investimento integral em Adobe Advertising, juntamente com outros canais de marketing, nos cliques de pesquisa |
| Nível da família | Sim | Sim | Não |
| O CTV é compatível? | Sim | Sim | Sim |
| Metodologia de atribuição | O evento de último toque (impressão ou clique) deve estar dentro da janela da pasta de pesquisa. | Únicos | Último contato |
| | Pontos de interação mais de 30 dias antes do evento de último toque são considerados para o caminho de conversão. | (O CTV recebe crédito, independentemente de onde a exposição ao CTV ocorre no caminho para clicar do usuário) | (O CTV recebe crédito se a impressão for o último evento na janela de pesquisa E não houver clique pago de outros formatos antes ou depois da exposição do CTV) |
| Nível de relatório | Granular | Granular | Amplo |
| | (Tipo De Canal, Criativo/Anúncio, Palavra-Chave, Caminhos, Duração, Tempo Para Conversão) | (Tática de CTV, aplicativo/editor de CTV) | (Adobe Advertising e outros canais de marketing) |
| Canais de marketing | DSP + Pesquisa (do Search, Social e Commerce) | DSP + Pesquisa (do Search, Social e Commerce) | Canais de marketing não rastreados pela ID EF de clickthrough do Adobe Advertising (como Pesquisa orgânica, Social orgânico, Email e Afiliado) |
| Métricas de conversão compatíveis | Métricas rastreadas usando o pixel do evento Adobe Advertising (AMO ID) e o rastreamento do Adobe Analytics | Cliques (sem conversões) | Métricas rastreadas usando o rastreamento do Adobe Analytics |

Para obter mais informações sobre o Efeito Halo dos Serviços de Medição Avançados nos Relatórios de Pesquisa, consulte &quot;[Serviços de Medição Avançada](/help/dsp/introduction/advanced-measurement-services.md).&quot;

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Configurações de Relatório Personalizado](/help/dsp/reports/report-settings.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
