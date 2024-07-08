---
title: Suporte para ativação de IDs universais
description: Saiba mais sobre o suporte para importar seus segmentos de ID universais, criar segmentos personalizados para faixa IDs universais e converter outros identificadores usuário em seus segmentos primários para IDs universais para direcionamento sem cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Suporte para ativação de IDs universais

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*recurso de beta*

DSP suporta IDs universais e baseadas em pessoas para direcionamento sem cookies dispositivo únicos (não entre dispositivo) em formatos digitais suportados pelo DSP.

* Você pode enviar manualmente seus [ ][!DNL LiveRamp] [!DNL RampIDs]autenticados diretamente para DSP usando o [!DNL LiveRamp] [!DNL Connect] painel. Consulte &quot;[Manualmente Importar segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP podem assimilar seus segmentos primários compostos por IDs de email com hash incorporados na sua plataforma de dados do cliente (CDP) e converter-los e [!DNL LiveRamp] [!DNL RampIDs] [!DNL Unified ID 2.0 (UID2.0)] IDs. Para obter mais informações sobre as plataformas de dados do cliente suportadas, os recursos disponíveis para cada tipo de ID universal compatível e as workflows relacionadas, consulte &quot;[Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)&quot;.

* Você pode criar segmentos personalizados que faixa usuários associados a IDs universais do ID5 que estão expostos a anúncios de desktop dispositivos móveis e que visita páginas da Web específicas. O ID5 usa um modelo probabilístico para atribuir uma ID derivada de vários sinais usuário e sinais navegador. Para obter instruções, consulte &quot;[Criar e implementar um segmento](/help/dsp/audiences/custom-segment-create.md) personalizado&quot;.

* Segmentos de terceiros de alguns fornecedores podem incluir automaticamente IDs universais, além de usuários rastreados por cookies ou IDs dispositivo. Por exemplo, os segmentos de [!DNL Eyeota] podem incluir automaticamente IDs ID5, e segmentos a partir de [!DNL Lotame] podem incluir IDs UID2.0. Os detalhes da segmento incluem o tamanho para cada tipo. A taxa de uso usual para cada segmento, que é declarado ao lado do nome segmento, se aplica; nenhuma taxa adicional é cobrada para as IDs de ID5.

## Relatórios por tipo de ID universal

* **Relatórios personalizados:** Custo, impressão, clique, conversão e frequência dados por tipo de ID universal estão disponíveis em relatórios personalizados.

* **[!DNL Analytics]relatórios:** Os anunciantes que [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) implementaram todas as etapas necessárias podem ver conversões visualização por tipo de ID universal.[!DNL Analytics]

  >[!IMPORTANT]
  >
  >Para obter conversão atribuição adequadas, verifique se os URLs de clickthrough para seus anúncios incluem a [EF ID e a ID](/help/integrations/analytics/ids.md) do AMO.

* **Detalhes do segmento:** Para todos os tipos de segmento, os detalhes da segmento incluem o público-alvo por tipo de ID universal e, pelo tipo de dispositivo rastreado por cookies ou IDs dispositivo.

## Como Target um público-alvo de ID universal em suas disposições

>[!NOTE]
>
>Não é possível alterar os tipos de ID direcionados em uma posicionamento ao vivo. Se necessário, é possível duplicado uma posicionamento online e alterar os tipos de ID direcionados nas novas posicionamento.

Em uma nova posicionamento programada ou pausada, faça o seguinte:

1. [!UICONTROL Geo-Targeting] Na seção, especifique as áreas geográficas a serem Direcionamento. Cada parceiro de ID universal permite usuário direcionamento somente em áreas geográficas específicas, e apenas tipos de ID elegíveis estão disponíveis nas [!UICONTROL Targeting] configurações.

1. [!UICONTROL Audience Targeting] Na seção, faça o seguinte:

   1. Na configuração [!UICONTROL Included Audiences] , selecione a segmento para a qual usuário dados foram convertidos em IDs universais.

      Você pode incluir segmentos adicionais, se desejar.

   1. [!UICONTROL Targeting] Nas configurações:

      1. Selecione o tipo de ID universal a ser Direcionamento.

         A configuração inclui as opções &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID]&quot;, que podem incluir as sub opções &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]e &quot;[!UICONTROL Unified ID2.0].&quot; As metas geográficas selecionadas determinam as sub opções disponíveis.

         Você pode selecionar &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID], mas pode selecionar apenas um tipo de ID universal por posicionamento. Quando você seleciona IDs herdadas e IDs universais, a preferência de lance é dada a IDs universais.

      1. (Se necessário) Aceite os termos do contrato de serviço para o uso de IDs universais.

         Antes de converter dados a um novo tipo de ID, uma usuário no DSP conta deve aceitar os termos do contrato de serviço. Os termos devem ser aceitos apenas uma vez por tipo de ID, por conta.

Consulte &quot;[Posicionamento Configurações](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Práticas recomendadas para teste e validação de dados

Utilize as seguintes práticas recomendadas para [!DNL RampID]segmentos com base em - e segmentos com base em ID5, para os quais Adobe Analytics medição está disponível.

* Cerca de 24 horas depois de ativar uma segmento, verifique a contagem de IDs convertida para o segmento em [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se a contagem de ID for inesperada, entre em contato com sua equipe de conta Adobe Systems.

  Consulte &quot;[Causas de variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot; para obter mais informações sobre como as contagens do segmento podem variar.

* Não altere seus pacotes e disposições existentes. No entanto, se você não tiver orçamento incremental para teste IDs universais, reduza os orçamentos originais para financiar os testes.

* Copie seus pacotes e disposições originais, ajuste os orçamentos com base no tamanho do teste, altere os públicos-alvo para usar [!DNL RampID]segmentos baseados em (para usuários autenticados) ou segmentos baseados em ID5 (para usuários não autenticados) e verifique se os novos pacotes e disposições gastam seus orçamentos completos.

   * Para comparar o desempenho de segmentos com base em ID universal com o desempenho de disposições direcionamento outros identificadores público-alvo, como cookies ou IDs publicidade para dispositivos móveis, crie uma campanha com um posicionamento universal baseado em ID separado e um posicionamento herdado baseado em ID.

     Para um teste de redirecionamento completo, Direcionamento tanto RampIDs para usuários autenticados quanto ID5s para usuários não autenticados.

     Obter o melhor desempenho não deve ser a comparação principal. Em vez disso, determine quais IDs estão dimensionando bem, o que pode informar suas alocações de otimização e orçamento posteriormente. O objetivo a longo prazo é compensar as impressões perdidas e o tráfego no site quando os cookies forem descontinuados.

   * Para comparar o alcance total navegador, Direcionamento segmentos universais baseados em ID e segmentos herdados baseados em ID no mesmo posicionamento. Use as mesmas configurações campanha que o caso de uso anterior, exceto por não precisar dividir o orçamento campanha.

     A preferência de lance é dada a IDs universais, mas as IDs herdadas recebem ofertas quando IDs universais não estão disponíveis. Certifique-se de comparar o alcance em diferentes navegadores (incluindo Cromo, Safari e Mozilla).

     >[!NOTE]
     >
     >A limitação de frequência se aplica a uma ID individual. Quando um usuário tem vários tipos de ID, você pode atingir essa usuário mais do que espera.

* Lembre-se de que o alcance para segmentos de público-alvo autenticados é naturalmente menor do que o alcance para segmentos baseados em cookie, e que usar opções adicionais de direcionamento diminui ainda mais seu alcance. Seja criterioso sobre o uso de direcionamento granulares, especialmente ao unir várias metas com declarações AND.

## Causas de variações de dados entre IDs de email e IDs universais {#universal-ids-data-variances}

* IDs de email com hash traduzidas para ID5 IDs:

  O modelo probabilístico apresenta um erro variação de +/- 5%. Isso significa que ele pode superestimar ou subestimar a contagem de público-alvo em 5%.

* IDs de email com hash traduzidas para [!DNL RampIDs]:

   * Quando vários perfis usam a mesma ID de email, a DSP segmento contagem pode ser menor do que a contagem perfil na plataforma de dados do cliente. Por exemplo, em Adobe Photoshop, você pode criar uma empresa conta e uma conta pessoal usando uma única ID de email. Mas se ambos os perfis pertencem à mesma pessoa, os perfis mapeiam para uma ID de email e correspondem a um [!DNL RampID].

   * É [!DNL RampID] possível atualizar para um novo valor. Se [!DNL LiveRamp] não reconhecer uma ID de email ou não conseguir mapeá-la para um existente [!DNL RampID] no banco de dados, ela atribui um novo [!DNL RampID] à ID de email. No futuro, quando eles puderem mapear a ID de email para outra [!DNL RampID] ou poder coletar mais informações sobre a mesma ID de email, eles atualizam para [!DNL RampID] um novo valor. [!DNL LiveRamp] refere-se a esta ação como atualização de um &quot;derivado&quot; [!DNL RampID] para um &quot;mantido&quot; [!DNL RampID]. No entanto, DSP não obtém mapeamentos entre derivados e mantidos [!DNL RampIDs] e, portanto, não podem remover a versão anterior do RampID do DSP segmento. Nesse caso, a contagem de segmento pode ser maior do que a contagem perfil.

     Exemplo: um usuário faz logon no [!DNL Adobe] site e visita o Photoshop página. Se [!DNL LiveRamp] não tiver nenhuma informação existente sobre a ID de email, eles atribuem uma derivada [!DNL RampID], digamos D123. Quinze dias depois, o usuário visita a mesma página, mas [!DNL LiveRamp] atualizou durante [!DNL RampID] esses 15 dias e reatribuíui o [!DNL RampID] para M123. Mesmo que o segmento &quot;Entusiasta do Photoshop&quot; da plataforma de dados do cliente tenha apenas uma ID de email para o usuário, o DSP segmento tem duas RampIDs: D123 e M123.

## Solução de problemas

Se você não vir usuário contagens ou se seus tamanhos de público-alvo forem baixos, verifique o seguinte:

* Se você usar ou [!DNL Google Campaign Manager 360] anúncios[!DNL Flashtalking], verifique se os URLs de clickthrough de seus anúncios estão anexados com as macros corretas. Consulte as macros para [[!DNL Flashtalking] anúncios](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] anúncios](/help/integrations/analytics/macros-google-campaign-manager.md).

* Certifique-se de que a ID correta e universal parceiro código específico seja implementado em seu site para corresponder a eventos no site e exposições publicidade. Entre em contato com seu [!DNL LiveRamp] representante, [!DNL ID5] conforme necessário.

* (Para [!DNL RampIDs] e [!DNL UID 2.0] IDs) Verifique se as [DSP fonte de dados estão configuradas corretamente](/help/dsp/audiences/sources/source-manage.md#source-settings) e se usuário contagens são preenchidas para os segmentos de público-alvo gerados.

* Se o seu alcance for menor do que você espera, verifique se a lógica de segmento de público não é muito granular.

* Certifique-se de que as configurações campanha, pacote e posicionamento estejam corretas.<!-- wording-->

Se você não conseguir resolver o problema, entre em contato com sua equipe de conta Adobe Systems.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar a ID universal Audiences](/help/dsp/audiences/sources/source-manage.md)
>* [Criar e implementar um segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar manualmente de segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Sobre o gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
