---
title: Suporte para ativação de IDs universais
description: Saiba mais sobre o suporte para importar segmentos de ID universal, criar segmentos personalizados para rastrear IDs universais e converter outros identificadores de usuário em seus segmentos primários para IDs universais para direcionamento sem cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: db21fa1ed9daab9070fa1ce7740dd5dbaa0f3a2f
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# Suporte para ativação de IDs universais

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Recurso beta*

O DSP oferece suporte a IDs universais com base em pessoas para direcionamento sem cookies de dispositivo único (não entre dispositivos) em formatos digitais compatíveis com DSP.

* Você pode enviar manualmente os [[!DNL LiveRamp] [!DNL RampIDs]] diretamente ao DSP usando o [!DNL LiveRamp] [!DNL Connect] painel. Consulte &quot;[Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* O DSP pode assimilar seus segmentos primários compostos de IDs de email com hash criadas na CDP (Plataforma de dados do cliente) e convertê-los em [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] IDs. Para obter mais informações sobre as plataformas de dados do cliente compatíveis, os recursos disponíveis para cada tipo de ID universal compatível e os workflows relacionados, consulte &quot;[Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md).&quot;

* Você pode criar segmentos personalizados que rastreiam usuários associados a IDs universais de ID5 que estão expostos a anúncios de dispositivos móveis e desktop e que visitam páginas da Web específicas. A ID5 usa um modelo probabilístico para atribuir uma ID derivada de vários sinais do usuário e do navegador. Para obter instruções, consulte &quot;[Criar e implementar um segmento personalizado](/help/dsp/audiences/custom-segment-create.md).&quot;

* Segmentos de terceiros de alguns fornecedores podem incluir IDs universais automaticamente, além de usuários rastreados por cookies ou IDs de dispositivo. Por exemplo, segmentos de [!DNL Eyeota] pode incluir IDs ID5 automaticamente e segmentos de [!DNL Lotame] pode incluir IDs UID2.0. Os detalhes do segmento incluem o tamanho de cada tipo. A taxa de uso normal para cada segmento, que é declarada ao lado do nome do segmento, se aplica; nenhuma taxa adicional é cobrada para as IDs ID5.

## Relatório por tipo de ID universal

* **Relatórios personalizados:** Os dados de custo, impressão, clique, conversão e frequência por tipo de ID universal estão disponíveis em relatórios personalizados.

* **[!DNL Analytics]relatórios:** Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) que implementaram todas as etapas necessárias podem ver conversões de view-through por tipo de ID universal em [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Para uma atribuição de conversão adequada, verifique se os URLs de clickthrough para seus anúncios incluem o [EF ID e AMO ID](/help/integrations/analytics/ids.md).

* **Detalhes do segmento:** Para todos os tipos de segmento, os detalhes do segmento incluem o tamanho do público-alvo por tipo de ID universal e pelo tipo de dispositivo rastreado por cookies ou IDs de dispositivo.

## Como direcionar um público-alvo da Universal ID em seus posicionamentos

>[!NOTE]
>
>Você não pode alterar os tipos de ID direcionados em uma inserção ao vivo. Se necessário, é possível duplicar um posicionamento dinâmico e alterar os tipos de ID direcionados no novo posicionamento.

Em um posicionamento novo, agendado ou pausado, faça o seguinte:

1. No [!UICONTROL Geo-Targeting] especifique as áreas geográficas para direcionamento. Cada parceiro de ID universal permite o direcionamento de usuários somente em áreas geográficas específicas, e somente os tipos de ID qualificados estão disponíveis no [!UICONTROL Targeting] configurações.

1. No [!UICONTROL Audience Targeting] faça o seguinte:

   1. No [!UICONTROL Included Audiences] selecione o segmento para o qual os dados do usuário foram convertidos em IDs universais.

      Você pode incluir segmentos adicionais, se desejar.

   1. No [!UICONTROL Targeting] configurações:

      1. Selecione o tipo de ID universal a ser direcionado.

         A configuração inclui as opções &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID],&quot; que pode incluir as subopções &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; e &quot;[!UICONTROL Unified ID2.0].&quot; Os destinos geográficos selecionados determinam as subopções disponíveis.

         Você pode selecionar ambos &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID],&quot; mas é possível selecionar apenas um tipo de ID universal por posicionamento. Ao selecionar IDs herdadas e IDs universais, a preferência de lances é dada às IDs universais.

      1. (Se necessário) Aceite os termos do contrato de serviço para usar IDs universais.

         Antes de converter os dados em um novo tipo de ID, um usuário na conta DSP deve aceitar os termos do contrato de serviço. Os termos devem ser aceitos apenas uma vez por tipo de ID, por conta.

Consulte &quot;[Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Práticas recomendadas para testes e validação de dados

Use as seguintes práticas recomendadas para [!DNL RampID]Segmentos com base em e segmentos com base em ID5, para os quais a medição de Adobe Analytics está disponível.

* Cerca de 24 horas depois de ativar um segmento, verifique a contagem de IDs convertidas para o segmento no [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se a contagem de ID for inesperada, entre em contato com a equipe de conta do Adobe.

  Consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot; para obter mais informações sobre como as contagens de segmentos podem variar.

* Não altere seus pacotes e posicionamentos existentes. No entanto, se você não tiver um orçamento incremental para testar as IDs universais, reduza os orçamentos originais para financiar os testes.

* Copie os pacotes e posicionamentos originais, ajuste os orçamentos com base no tamanho do teste e altere os públicos-alvo a serem usados [!DNL RampID]Segmentos com base em (para usuários autenticados) ou segmentos com base em ID5 (para usuários não autenticados) e verifique se os novos pacotes e posicionamentos gastam seu orçamento completo.

   * Para comparar o desempenho de segmentos com base em ID universal com o desempenho de inserções direcionadas a outros identificadores de público-alvo, como cookies ou IDs de publicidade móvel, crie uma campanha com uma inserção separada com base em ID universal e uma inserção herdada com base em ID.

     Para um teste de redirecionamento completo, direcione RampIDs para usuários autenticados e ID5s para usuários não autenticados.

     A comparação primária não deve ser a obtenção do melhor desempenho. Em vez disso, determine quais IDs estão sendo bem dimensionadas, o que pode informar sua otimização e alocações de orçamento posteriormente. O objetivo de longo prazo é compensar a perda de impressões e o tráfego do site quando os cookies forem descontinuados.

   * Para comparar o alcance total do navegador, selecione segmentos baseados em ID universal e ID herdada na mesma disposição. Use as mesmas configurações de campanha que o caso de uso anterior, exceto que não é necessário dividir o orçamento da campanha.

     A preferência de lance é fornecida para IDs universais, mas as IDs herdadas recebem lances quando as IDs universais não estão disponíveis. Compare o alcance em navegadores diferentes (incluindo Chrome, Safari e Mozilla).

     >[!NOTE]
     >
     >O limite de frequência se aplica a uma ID individual. Quando um usuário tem vários tipos de ID, você pode alcançar esse usuário mais do que o esperado.

* Lembre-se de que o alcance para segmentos de público-alvo autenticados é naturalmente menor do que o alcance para segmentos baseados em cookies, e que o uso de opções adicionais de direcionamento diminui ainda mais o alcance. Seja criterioso em usar o direcionamento granular, especialmente ao unir vários targets com instruções AND.

## Causas para variações de dados entre IDs de email e IDs universais {#universal-ids-data-variances}

* IDs de email com hash traduzidas para IDs 5:

  O modelo probabilístico tem uma variação de erro de +/- 5%. Isso significa que pode superestimar ou subestimar a contagem de público em 5%.

* IDs de email com hash traduzidas para [!DNL RampIDs]:

   * Quando vários perfis usam a mesma ID de email, a contagem de segmentos do DSP pode ser inferior à contagem de perfis na plataforma de dados do cliente. Por exemplo, no Adobe Photoshop, é possível criar uma conta da empresa e uma conta pessoal usando uma única ID de email. Mas se ambos os perfis pertencerem ao mesmo segmento, os perfis serão mapeados para uma ID de email e correspondentemente para uma [!DNL RampID].

   * A [!DNL RampID] pode ser atualizado para um novo valor. Se [!DNL LiveRamp] não reconhece uma ID de e-mail ou não pode mapeá-la para uma ID existente [!DNL RampID] em seu banco de dados, atribuirá um novo [!DNL RampID] à ID de e-mail. No futuro, quando eles puderem mapear a ID de email para outra [!DNL RampID] ou puder coletar mais informações sobre a mesma ID de email, eles atualizarão o [!DNL RampID] para um novo valor. [!DNL LiveRamp] refere-se a esta ação como atualização de um &quot;derivado&quot; [!DNL RampID] para um ambiente &quot;mantido&quot; [!DNL RampID]. No entanto, o DSP não obtém mapeamentos entre derivados e mantidos [!DNL RampIDs] e, portanto, não pode remover a versão anterior da RampID do segmento DSP. Nesse caso, a contagem de segmentos pode ser maior que a contagem de perfis.

     Exemplo: um usuário faz logon na variável [!DNL Adobe] site e visita a página do Photoshop. Se [!DNL LiveRamp] não tiver nenhuma informação existente sobre a ID de e-mail e, em seguida, atribuírem a ela um [!DNL RampID], digamos D123. Quinze dias depois, o usuário visita a mesma página, mas [!DNL LiveRamp] atualizou o [!DNL RampID] durante esses 15 dias e tiver reatribuído a [!DNL RampID] M123. Embora o segmento &quot;Entusiasta da Photoshop&quot; da plataforma de dados do cliente tenha apenas uma ID de email para o usuário, o segmento DSP tem duas RampIDs: D123 e M123.

## Solução de problemas

Se você não vir as contagens de usuários ou se os tamanhos de público-alvo estiverem baixos, verifique o seguinte:

* Se você usar [!DNL Flashtalking] ou [!DNL Google Campaign Manager 360] anúncios, verifique se os URLs de clickthrough dos anúncios estão anexados com as macros corretas. Veja as macros para [[!DNL Flashtalking] anúncios](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] anúncios](/help/integrations/analytics/macros-google-campaign-manager.md).

* Certifique-se de que o código correto e específico do parceiro de ID universal esteja implementado em seu site para corresponder aos eventos e às exposições dos anúncios no site. Trabalhe com o seu [!DNL LiveRamp] ou [!DNL ID5] representante, conforme necessário.

* (Para [!DNL RampIDs] e [!DNL UID 2.0] IDs) Certifique-se de que seus [A fonte de dados do DSP está configurada corretamente](/help/dsp/audiences/sources/source-manage.md#source-settings)e que as contagens de usuários sejam preenchidas para os segmentos de público-alvo gerados.

* Se o alcance for menor do que o esperado, verifique se a lógica do segmento de público-alvo não é muito granular.

Se você não conseguir resolver o problema, entre em contato com a equipe de conta do Adobe.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](/help/dsp/audiences/sources/source-manage.md)
>* [Criar e implementar um segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
