---
title: Suporte para ativação de IDs universais
description: Saiba mais sobre o suporte para importar segmentos de ID universal, criar segmentos personalizados para rastrear IDs universais e converter outros identificadores de usuário em seus segmentos primários para IDs universais para direcionamento sem cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
TQID: https://experienceleague.adobe.com/A4fMoTW9gHD1i9Gdg1FALrBlz0XxMqhHOp9YO6kf3BQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 1610
ht-degree: 0%

---

# Suporte para ativação de IDs universais

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

O DSP oferece suporte a IDs universais com base em pessoas para direcionamento em dispositivos únicos (não entre dispositivos) sem cookies em formatos digitais compatíveis com o DSP.

* Você pode enviar manualmente seu [[!DNL LiveRamp] [!DNL RampIDs]] autenticado diretamente para a DSP usando o painel [!DNL LiveRamp] [!DNL Connect]. Consulte &quot;[Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* A DSP pode assimilar seus segmentos primários criados em sua CDP (Plataforma de Dados do Cliente) e convertê-los em [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] IDs. Para obter mais informações sobre as plataformas de dados do cliente e os tipos de identificadores de usuário compatíveis, os recursos disponíveis para cada tipo de ID universal compatível e os fluxos de trabalho relacionados, consulte &quot;[Sobre Fontes de Público-Alvo Primárias](/help/dsp/audiences/sources/source-about.md).&quot;

* Os anunciantes na Austrália podem importar segmentos primários que contêm [!DNL AdFixus] IDs universais usando uma fonte de público-alvo [!UICONTROL AdFixus ID]. O DSP não converte entre [!DNL AdFixus] IDs e outros tipos de ID universal. Consulte &quot;[Importar segmentos primários de [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)&quot;.

* Você pode criar segmentos personalizados que rastreiam usuários associados a IDs universais de ID5 que estão expostos a anúncios de dispositivos móveis e desktop e que visitam páginas da Web específicas. A ID5 usa um modelo probabilístico para atribuir uma ID derivada de vários sinais do usuário e do navegador. Para obter instruções, consulte &quot;[Criar e implementar um segmento personalizado](/help/dsp/audiences/custom-segment-create.md).&quot;

* Segmentos de terceiros de alguns fornecedores podem incluir IDs universais automaticamente, além de usuários rastreados por cookies ou IDs de dispositivo. Por exemplo, os segmentos de [!DNL Eyeota] podem incluir IDs ID5 automaticamente e os segmentos de [!DNL Lotame] podem incluir IDs UID2.0. Os detalhes do segmento incluem o tamanho de cada tipo. A taxa de uso normal para cada segmento, que é declarada ao lado do nome do segmento, se aplica; nenhuma taxa adicional é cobrada para as IDs ID5.

## Relatório por tipo de ID universal

* **Relatórios personalizados:** dados de custo, impressão, clique, conversão e frequência por tipo de ID universal estão disponíveis em relatórios personalizados.

* **[!DNL Analytics]relatórios:** Os anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) que implementaram todas as etapas necessárias podem ver conversões de viewthrough por tipo de ID universal em [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Para atribuição de conversão adequada, verifique se as URLs de clickthrough para seus anúncios incluem a [EF ID e a AMO ID](/help/integrations/analytics/ids.md).

* **Detalhes do segmento:** Para todos os tipos de segmento, os detalhes do segmento incluem o tamanho do público-alvo por tipo de ID universal e pelo tipo de dispositivo rastreado por cookies ou IDs de dispositivo.

## Como direcionar um público de ID universal em seus posicionamentos

>[!NOTE]
>
>Você não pode alterar os tipos de ID direcionados em uma inserção ao vivo. Se necessário, é possível duplicar um posicionamento dinâmico e alterar os tipos de ID direcionados no novo posicionamento.

Em um posicionamento novo, agendado ou pausado, faça o seguinte:

1. Na seção [!UICONTROL Geo-Targeting], especifique as áreas geográficas para direcionamento. Cada parceiro de ID universal permite o direcionamento de usuários somente em áreas geográficas específicas, e somente os tipos de ID qualificados estão disponíveis nas configurações de [!UICONTROL Targeting].

1. Na seção [!UICONTROL Audience Targeting], faça o seguinte:

   1. Na configuração [!UICONTROL Included Audiences], selecione o segmento para o qual os dados do usuário foram convertidos em IDs universais (como [!DNL RampIDs] ou [!DNL UID2] IDs) ou que contém [!DNL AdFixus] IDs importadas.

      Você pode incluir segmentos adicionais, se desejar.

   1. Nas configurações de [!UICONTROL Targeting]:

      1. Selecione o tipo de ID universal a ser direcionado.

         A configuração inclui as opções &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID]&quot;, que podem incluir as subopções &quot;[!UICONTROL AdFixus],&quot; &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; e &quot;[!UICONTROL Unified ID2.0].&quot; Os destinos geográficos selecionados determinam as subopções disponíveis.

         Você pode selecionar &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID]&quot;, mas pode selecionar apenas um tipo de ID universal por posicionamento. Ao selecionar IDs herdadas e IDs universais, a preferência de lances é dada às IDs universais.

      1. (Se necessário) Aceite os termos do contrato de serviço para usar IDs universais.

         Antes de converter os dados em um novo tipo de ID, um usuário na conta da DSP deve aceitar os termos do contrato de serviço. Os termos devem ser aceitos apenas uma vez por tipo de ID, por conta.

Consulte &quot;[Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Práticas recomendadas para teste e validação de dados para segmentos baseados em [!DNL RampID] e segmentos baseados em ID5

Use as seguintes práticas recomendadas para segmentos baseados em [!DNL RampID] e segmentos baseados em ID5, para os quais a medição de Adobe Analytics está disponível.

* Cerca de 24 horas depois de ativar um segmento, verifique a contagem de IDs convertidas para o segmento em [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se a contagem de ID for inesperada, entre em contato com a equipe de conta da Adobe.

  Consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot; para obter mais informações sobre como as contagens de segmentos podem variar.

* Não altere seus pacotes e posicionamentos existentes. No entanto, se você não tiver um orçamento incremental para testar as IDs universais, reduza os orçamentos originais para financiar os testes.

* Copie os pacotes e posicionamentos originais, ajuste os orçamentos com base no tamanho do teste, altere os públicos para usar segmentos baseados em [!DNL RampID] (para usuários autenticados) ou segmentos baseados em ID5 (para usuários não autenticados) e verifique se os novos pacotes e posicionamentos gastam seus orçamentos completos.

   * Para comparar o desempenho de segmentos com base em ID universal com o desempenho de inserções direcionadas a outros identificadores de público-alvo, como cookies ou IDs de publicidade móvel, crie uma campanha com uma inserção separada com base em ID universal e uma inserção herdada com base em ID.

     Para um teste de redirecionamento completo, direcione RampIDs para usuários autenticados e ID5s para usuários não autenticados.

     A comparação primária não deve ser a obtenção do melhor desempenho. Em vez disso, determine quais IDs estão sendo bem dimensionadas, o que pode informar sua otimização e alocações de orçamento posteriormente. O objetivo de longo prazo é compensar a perda de impressões e o tráfego do site quando os cookies forem descontinuados.

   * Para comparar o alcance total do navegador, selecione segmentos baseados em ID universal e ID herdada na mesma disposição. Use as mesmas configurações de campanha que o caso de uso anterior, exceto que não é necessário dividir o orçamento da campanha.

     A preferência de lance é fornecida para IDs universais, mas as IDs herdadas recebem lances quando as IDs universais não estão disponíveis. Compare o alcance em navegadores diferentes (incluindo Chrome, Safari e Mozilla).

     >[!NOTE]
     >
     >O limite de frequência se aplica a uma ID individual. Quando um usuário tem vários tipos de ID, você pode alcançar esse usuário mais do que o esperado.

* Lembre-se de que o alcance para segmentos de público-alvo autenticados é naturalmente menor do que o alcance para segmentos baseados em cookies, e que o uso de opções adicionais de direcionamento diminui ainda mais o alcance. Seja criterioso em usar o direcionamento granular, especialmente ao unir vários targets com instruções AND.

## Variações de dados entre IDs de email e IDs universais {#universal-ids-data-variances}

Esta seção se aplica somente às IDs de email traduzidas para IDs universais.

### Níveis aceitáveis de variação

A taxa de conversão de endereços de email com hash para IDs universais deve ser maior que 90%; a taxa de conversão para [!DNL RampIDs] em particular deve ser de 95% se todos os endereços de email com hash forem exclusivos. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para pelo menos 95 [!DNL RampIDs] ou mais de 90 outros tipos de IDs universais. Uma taxa de tradução mais baixa pode indicar um problema. Consulte &quot;[Causas de variação]&#x200B;(#universal-ids-data-variances-causes&quot; para obter possíveis explicações.

Para [!DNL RampIDs], entre em contato com a equipe de conta da Adobe para obter mais investigação se as taxas de tradução forem inferiores a 70%.

### Causas de variação {#universal-ids-data-variances-causes}

* Todos os segmentos:

  A contagem de segmento para dispositivo usa um modelo probabilístico, que tem uma variação de erro de +/- 5%. Isso significa que pode superestimar ou subestimar o contagem de público-alvo em 5%.

* IDs de email com hash traduzidas para [!DNL RampIDs]:

   * Quando vários perfis usam a mesma ID de email, a contagem de segmentos do DSP pode ser inferior à contagem de perfis na plataforma de dados do cliente. Por exemplo, no Adobe Photoshop, é possível criar uma conta da empresa e uma conta pessoal usando uma única ID de email. Mas se ambos os perfis pertencerem à mesma pessoa, eles serão mapeados para uma ID de email e correspondentemente para uma [!DNL RampID].

   * Um [!DNL RampID] pode ser atualizado para um novo valor. Se [!DNL LiveRamp] não reconhecer uma ID de email ou não puder mapeá-la para um [!DNL RampID] existente em seu banco de dados, ele atribuirá um novo [!DNL RampID] à ID de email. Futuramente, quando puderem mapear a ID de email para outro [!DNL RampID] ou puderem coletar mais informações sobre a mesma ID de email, eles atualizarão o [!DNL RampID] para um novo valor. [!DNL LiveRamp] refere-se a esta ação como atualização de um [!DNL RampID] &quot;derivado&quot; para um [!DNL RampID] &quot;mantido&quot;. No entanto, o DSP não obtém mapeamentos entre [!DNL RampIDs] derivados e mantidos e, portanto, não pode remover a versão anterior da RampID do segmento do DSP. Nesse caso, a contagem de segmentos pode ser maior que a contagem de perfis.

     Exemplo: um usuário faz logon no site do [!DNL Adobe] e visita a página do Photoshop. Se [!DNL LiveRamp] não tiver nenhuma informação existente sobre a ID de e-mail, ele atribuirá a ela um [!DNL RampID] derivado, digamos D123. Quinze dias depois, o usuário visita a mesma página, mas [!DNL LiveRamp] atualizou o [!DNL RampID] durante esses 15 dias e reatribuiu o [!DNL RampID] ao M123. Embora o segmento &quot;Entusiasta da Photoshop&quot; da plataforma de dados do cliente tenha apenas uma ID de email para o usuário, o segmento do DSP tem duas RampIDs: D123 e M123.

## Solução de problemas

Se você não vir as contagens de usuários ou se os tamanhos de público-alvo estiverem baixos, verifique o seguinte:

* Se você usa [!DNL Flashtalking] ou [!DNL Google Campaign Manager 360] anúncios, verifique se as URLs de clickthrough dos seus anúncios estão anexadas com as macros corretas. Consulte as macros para [[!DNL Flashtalking] anúncios](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] anúncios](/help/integrations/analytics/macros-google-campaign-manager.md).

* (Para [!DNL RampIDs] e [!DNL UID 2.0] IDs) Verifique se o código correto e específico do parceiro de ID universal está implementado em seu site para corresponder a eventos no site e exposições de anúncios. Trabalhe com seu representante do [!DNL LiveRamp] ou do [!DNL ID5], conforme necessário.

* (Para [!DNL RampIDs] e [!DNL UID 2.0] IDs) Verifique se a sua [fonte de dados do DSP está configurada corretamente](/help/dsp/audiences/sources/source-manage.md#source-settings) e se as contagens de usuários estão preenchidas para os segmentos de público-alvo gerados.

* (Para [!DNL AdFixus] IDs) Verifique se a origem [!UICONTROL AdFixus ID] está configurada corretamente e se [!DNL AdFixus] está transmitindo segmentos.

* Se o alcance for menor do que o esperado, verifique se a lógica do segmento de público-alvo não é muito granular.

* Verifique se as configurações de campanha, pacote e posicionamento estão corretas.

Se você não conseguir resolver o problema, entre em contato com a equipe de conta da Adobe.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo de ID universal](/help/dsp/audiences/sources/source-manage.md)
>* [Criar e implementar um segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar segmentos autenticados manualmente de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Importar segmentos primários de [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [Sobre o gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
