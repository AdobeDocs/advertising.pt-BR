---
title: Soluções entre dispositivos
description: Saiba mais sobre os recursos entre dispositivos.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Soluções entre dispositivos

A integração do Advertising DSP com o [!DNL LiveRamp] permite estender o público-alvo para todos os dispositivos conhecidos de uma pessoa, não apenas para os dispositivos rastreados pela sua marca. A integração também fornece limite de frequência e medição de atribuição em todos os dispositivos.

Ao usar um gráfico de dispositivos com base em pessoas compatível, você pode:

* Combine públicos em canais e dispositivos para fornecer anúncios a pessoas e famílias, em vez de a dispositivos.
* Equilíbrio e exposição por meio da compreensão e limitação de frequência entre indivíduos.
* Estratégias de teste que expõem versus convertem públicos em canais ou dispositivos.

## Benefícios do Gráfico de dispositivos [!DNL LiveRamp]

* Fornece um pool de dados determinístico, incluindo dados offline do cliente

* Fornece cobertura uniforme entre IDs de cookie e IDs de dispositivo móvel

* Inclui dados predominantemente dos Estados Unidos

* É livre para medição de limite de frequência e atribuição

* Com preço de US$ 0,35 CPM para impressões estendidas (impressões fornecidas exclusivamente usando o gráfico de dispositivos [!DNL LiveRamp], em vez de dispositivos encontrados nos segmentos de público-alvo direcionados)

  A taxa é refletida no seu cartão de taxa de conta.

## Gerenciamento de frequência com base em pessoas

O gerenciamento de frequência com base em pessoas permite especificar limites de frequência no nível da pessoa, em vez do nível do dispositivo, para um verdadeiro controle de exposição da mídia.

### Ativar o Gerenciamento de frequência com base em pessoas

* **Campanhas:** ao criar uma nova campanha, você pode especificar uma configuração [!UICONTROL Cross-Device Level]. Habilite &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; e selecione um gráfico de dispositivos. O gráfico de dispositivos especificado é usado para direcionamento entre dispositivos no nível de posicionamento e para gerenciamento de frequência com base em pessoas no nível de campanha, pacote e posicionamento. Os limites de frequência se aplicam a todos os dispositivos conhecidos de uma pessoa.

Para obter mais informações, consulte [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Depois de salvar uma campanha, você não poderá alterar sua configuração [!UICONTROL Cross Device Level].

* **Pacotes:** você pode, opcionalmente, definir limites de frequência adicionais no nível do pacote. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

* **Posicionamentos:** você pode, opcionalmente, definir limites de frequência adicionais no nível de posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

## Direcionamento com base em pessoas

O direcionamento com base em pessoas permite encontrar clientes no desktop e nos dispositivos móveis.

### Ativar o direcionamento com base em pessoas

* **Campanhas:** ao criar uma nova campanha, você pode especificar uma configuração [!UICONTROL Cross-Device Level]. Habilite &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; e selecione um gráfico de dispositivos. O gráfico de dispositivos especificado é usado para direcionamento entre dispositivos no nível de posicionamento e para gerenciamento de frequência com base em pessoas.

Para obter mais informações, consulte [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Posicionamentos:** ao selecionar destinos de público-alvo para um posicionamento em uma campanha com um gráfico de dispositivos especificado, uma opção [!UICONTROL Cross-Device Targeting] permite estender seu direcionamento para todos os dispositivos conhecidos de uma pessoa (de acordo com o gráfico de dispositivos especificado nas configurações da campanha), até mesmo dispositivos que não estão nos segmentos especificados.

### Configurar relatórios para direcionamento com base em pessoas

Você pode incluir as seguintes métricas nos relatórios personalizados:

* **Impressões Estendidas:** (na seção [!UICONTROL Build Your Report] em [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) O volume de impressões incrementais fornecidas por meio do uso de um gráfico de dispositivos (e não encontradas nos segmentos de público originais). Essa métrica também é usada para calcular as taxas aplicáveis associadas ao uso de um gráfico de dispositivos de terceiros.

  Para determinar o custo de suas impressões estendidas durante um período de tempo, execute um relatório personalizado que inclua a coluna [!UICONTROL Extended Impressions] e multiplique o número total de impressões estendidas por US$ 0,00035 (impressões de US$ 0,35/1000).

  O custo agregado também está incluído na coluna [!UICONTROL Billable Other Net Spend] (em [!UICONTROL Metrics] > [!UICONTROL Spend]), embora essa métrica também inclua outras taxas de campanha que você possa ter adicionado.

* **Gráfico de dispositivos:** (na seção [!UICONTROL Build Your Report] em [!UICONTROL Dimensions] > [!UICONTROL Campaign]) O gráfico de dispositivos selecionado para uma campanha, um pacote ou um posicionamento específico.

## Medição de atribuição com base em pessoas

*Anunciantes com Rastreamento de Conversão de Adobe Advertising Somente*

Com a atribuição baseada em pessoas, você pode atribuir conversões que ocorreram em um dispositivo diferente do dispositivo no qual ocorreu a exposição da mídia. A medição de atribuição baseada em pessoas está disponível por DSP, [!DNL Adobe Advertising Creative] e [!DNL Adobe Advertising Search, Social, & Commerce] para anunciantes que implementaram pixels de conversão de Adobe Advertising em seus sites.

### Ativar medição de atribuição com base em pessoas

Se você quiser ativar a medição de atribuição entre dispositivos, entre em contato com a equipe de conta do Adobe.

### Configurar relatórios de conversão para atribuição de conversão entre dispositivos

#### Configurações do relatório de conversão

Quando um gráfico de dispositivos é habilitado para medição de atribuição, o Relatório [!UICONTROL Conversion] inclui uma configuração [!UICONTROL Cross-Device Breakout], que permite incluir até três colunas separadas para cada métrica de conversão, incluindo:

* &lt;*Conversão*>[!UICONTROL (tp)]: inclui o total de conversões (total de pessoas), que inclui tanto conversões de mesmo dispositivo quanto conversões entre dispositivos (se aplicável). No relatório, &quot;[!UICONTROL (tp)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Respostas(le)(tl)(tp)).

* &lt;*Conversion*>[!UICONTROL (sd)]: (opcional) inclui somente conversões para as quais apenas um único dispositivo foi rastreado no caminho de conversão. No relatório, &quot;[!UICONTROL (sd)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Respostas(le)(tl)(sd)).

* &lt;*Conversion*>[!UICONTROL (xd)]: (opcional) inclui somente conversões para as quais mais de um dispositivo foi rastreado no caminho de conversão. No relatório, &quot;[!UICONTROL (xd)]&quot; é anexado ao nome da métrica de conversão, ao tipo de regra e aos tipos de conversão no caminho de conversão (por exemplo, &quot;Respostas(le)(tl)(xd)).

#### Como interpretar o relatório de conversão

Classifique a porcentagem do total de conversões entre dispositivos ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de alto a baixo para entender o que está gerando conversões entre dispositivos acima da média. Você pode usá-lo para informar sua estratégia criativa ou de direcionamento para corresponder o investimento em mensagens e canais ao comportamento do usuário.

* Pacotes — veja quais pacotes geram mais conversões totais e quais têm uma alta porcentagem de conversões entre dispositivos. Isso pode ajudá-lo a entender onde concentrar os gastos.

* Posicionamentos — Compare o desempenho e a atribuição do posicionamento (por exemplo, um anúncio de web móvel pode gerar conversões no desktop). Sem um gráfico de dispositivos para atribuição, você pode perder um impacto do posicionamento da Web móvel nas conversões de desktop ou ele pode ficar enterrado se a maioria dos usuários converter no desktop e não na Web móvel.

* Anúncios — Descubra quais anúncios geram conversões mais altas e quantificam seu valor e impacto em navegadores da Web e ambientes de aplicativos móveis.

* Sites — otimize entre sites em vez de excluir sites manualmente por completo. Se um site direciona conversões entre dispositivos, você pode ver em quais dispositivos esse comportamento ocorre.

* Ofertas — melhore a otimização manual verificando quais ofertas de inventário oferecem conversões entre dispositivos e, em seguida, decidindo se você deve expandir seu direcionamento para incluir mais dispositivos e canais nessas ofertas.

>[!MORELIKETHIS]
>
>* [Configurações do relatório](/help/dsp/reports/report-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
