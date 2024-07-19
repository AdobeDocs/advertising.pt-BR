---
title: Sobre o Gerenciamento de público-alvo no Advertising DSP
description: Saiba mais sobre os recursos de gerenciamento de público-alvo.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Sobre o Gerenciamento de público-alvo no Advertising DSP

No DSP, é possível criar e gerenciar segmentos de público-alvo e conjuntos de público-alvo, que você pode usar como alvos para seus posicionamentos:

* Colete seus próprios dados de público-alvo primários criando e implementando segmentos de DSP. Posteriormente, você pode redirecionar os usuários no segmento com anúncios ou impedir que eles recebam anúncios. Você pode criar os seguintes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a) usuários expostos a anúncios de dispositivos móveis e de desktop e b) usuários que visitam páginas da Web específicas. A tag de rastreamento pode rastrear usuários baseados em cookies ou usuários associados a IDs universais de ID5.

   * [Segmentos de não participação na venda da CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear as IDs de usuários a partir de solicitações de não participação na venda do consumidor em seu site, de acordo com a California Consumer Privacy Act (CCPA). Você pode recuperar relatórios mensais das IDs de usuário de solicitações de recusa de venda.

     Para obter mais informações sobre suporte do Adobe Advertising para solicitações de recusa de venda do CCPA, consulte [Suporte do Adobe Advertising para a California Consumer Privacy Act: suporte de recusa do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Recurso do Beta) [Obter e usar IDs universais para direcionamento sem cookies](/help/dsp/audiences/universal-ids.md):

   * Envie manualmente os segmentos autenticados do [!DNL LiveRamp] [!DNL RampID] diretamente para o DSP.

   * Permitir que o DSP importe segmentos primários da sua plataforma de dados do cliente e traduza-os para tipos de ID universal compatíveis.

   * Inclua segmentos de terceiros que contenham IDs universais em seus destinos de posicionamento sem etapas extras.

* Crie uma biblioteca de público-alvo de [públicos-alvo reutilizáveis](/help/dsp/audiences/reusable-audience-create.md). Os públicos-alvo salvos são compostos por qualquer segmento de público-alvo disponível e qualquer outro público-alvo salvo. Todas as alterações feitas em um público-alvo salvo são automaticamente aplicadas a todos os posicionamentos que direcionam ou excluem o público-alvo e a todos os outros públicos que incluem o público-alvo salvo.

  Públicos-alvo salvos permitem que os planejadores de mídia agrupem públicos-alvo conforme necessário, incluindo e excluindo vários segmentos que utilizam lógica booleana complexa. O tamanho de cada segmento individual e o tamanho total do público são indicados à medida que você cria um público. Os executores de campanha podem simplesmente selecionar um ou mais públicos-alvo salvos como alvos de posicionamento, em vez de configurar manualmente os alvos de público-alvo para cada posicionamento.

Outros tipos de público-alvo também estão disponíveis para o direcionamento de posicionamento.

## Importação de segmentos de dados próprios e de terceiros

Você tem muitas opções para importar segmentos de dados primários e de terceiros para o DSP, usando a interface do usuário DSP e/ou por meio de serviços de importação personalizados.

* O DSP pode obter seus públicos-alvo da Adobe Audience Manager e de outros [!DNL Adobe] para direcionamento. Para obter os pré-requisitos e as instruções, consulte &quot;[Importar segmentos do Adobe Audience Manager para direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).

* O DSP pode converter segmentos de dados primários de plataformas de dados de clientes compatíveis em segmentos com IDs universais usando o [recurso Fontes](/help/dsp/audiences/sources/source-about.md). Você também pode [enviar manualmente seus segmentos [!DNL LiveRamp] [!DNL RampID] autenticados diretamente para o DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* O DSP pode importar outros segmentos de dados primários diretamente da sua plataforma de gerenciamento de dados (DMP) e fornecê-los a qualquer conjunto de anunciantes, conforme necessário.

* O DSP pode importar segmentos personalizados de terceiros, incluindo combinações complexas de segmentos de terceiros. Você pode fornecer os segmentos a qualquer conjunto de anunciantes, conforme necessário.

Entre em contato com a equipe de conta do Adobe para obter mais informações.

## Públicos-alvo disponíveis como alvos de posicionamento

Você pode direcionar seus posicionamentos para todos os tipos de público a seguir.

* Todos os conjuntos de públicos-alvo criados pelo usuário que foram salvos no DSP.

* Todos os segmentos de público-alvo criados pelo usuário que foram criados no DSP:

   * Segmentos personalizados para usuários que visitaram páginas da Web específicas e usuários expostos a impressões de anúncios específicos.

     Nenhuma taxa é incorrida para impressões entregues a IDs universais.

   * Segmentos de público-alvo de não participação na venda do CCPA para usuários que enviaram solicitações de não participação na venda em seu site, de acordo com a California Consumer Privacy Act (CCPA).

* Todos os segmentos de dados primários importados, incluindo segmentos que foram traduzidos para IDs universais.

  Taxas adicionais são cobradas por impressões entregues a IDs universais. Consulte &quot;[Sobre fontes de público-alvo primários](/help/dsp/audiences/sources/source-about.md)&quot; para obter taxas.

* Todos os seus segmentos de dados personalizados de terceiros importados.

* (Posicionamentos direcionados somente aos EUA) [Todos os segmentos de dados de terceiros disponíveis para clientes DSP de mais de 30 provedores](/help/dsp/audiences/third-party-data-providers.md), incluindo [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]),[!DNL Lotame], [!DNL Neustar] e muitos outros.

  Você pode direcionar segmentos específicos, que direcionam usuários com base nos dados do público-alvo (por exemplo, usuários com demografia, interesses ou intenções específicos e/ou perfis comportamentais). Você pode procurar por provedor de dados e categoria, procurar segmentos por nome ou ID de segmento, ou filtrar os resultados por provedor de dados, tamanho total do segmento, contagem de navegadores da Web ou contagem de dispositivos.

  Os segmentos de terceiros incorrem em taxas adicionais, que são indicadas ao lado de cada nome de segmento.

* (Anunciantes com Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics que usam somente as tags de conversão do Adobe Advertising JavaScript) Todos os seus segmentos de público-alvo primários, secundários ou de terceiros disponíveis criados no [!DNL Real-Time CDP], criados no Audience Manager ou publicados no Adobe Experience Cloud a partir do Audience Manager ou [!DNL Analytics].

  Os preços para o uso dos segmentos são pré-negociados e não são visíveis no DSP.

  Segmentos do [!DNL Analytics] estão disponíveis cerca de uma hora depois de você criá-los ou publicá-los como públicos-alvo do Experience Cloud. Segmentos provenientes diretamente do Audience Manager ou do [!DNL Real-Time CDP] estão disponíveis em 24 horas após serem compartilhados.

  >[!NOTE]
  >
  >Consulte a documentação do [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html) e [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) para obter informações sobre como configurar e coletar dados para segmentos nessas soluções.

## Dados de tamanho do público

Em Públicos-alvo > Todos os públicos-alvo e na seção Direcionamento de público das configurações de posicionamento, você pode filtrar cada lista de segmentos por intervalo de tamanho, incluindo o intervalo total e intervalos separados para tipos de dispositivo específicos ou tipos de ID universal.

![filtrar por tamanho de público](/help/dsp/assets/audience-size-filter.png)

Você também pode ver dados detalhados sobre o tamanho do público-alvo:

* O tamanho total e ativo do público desduplicado em todos os segmentos selecionados e salvos é exibido e você pode exibir detalhes por tipo de dispositivo (navegador, celular ou TV conectada).

  ![o tamanho combinado do público-alvo](/help/dsp/assets/audience-size.png)

* Para segmentos individuais, o tamanho total do público-alvo e o CPM (quando aplicável) são exibidos ao lado do nome do segmento.

  ![o tamanho de segmento individual](/help/dsp/assets/audience-size-segment.png)

* Você pode ver mais detalhes sobre um segmento individual ou público-alvo salvo, incluindo o tamanho por navegador, celular, TV conectada e parceiro de tipo de ID universal. Para públicos salvos, o tamanho total é o total desduplicado.

  ![o segmento individual ou os detalhes do público-alvo salvo](/help/dsp/assets/audience-size-segment-details.png)

## As Visualizações de Públicos-alvo

### A visualização Todos os públicos-alvo

Na exibição [!UICONTROL All Audiences] ou Biblioteca de público-alvo, você pode salvar e gerenciar públicos-alvo reutilizáveis, que incluem grupos de segmentos de público-alvo e até mesmo outros públicos-alvo salvos. Você pode usar públicos-alvo como destinos para vários posicionamentos. O número de disposições em que cada público-alvo é usado é indicado ao lado do nome da disposição.

Você pode editar, clonar, excluir, exportar ou compartilhar qualquer público-alvo.

### A visualização Segmentos

Na visualização [!UICONTROL Segments], todos os usuários podem criar segmentos personalizados adicionais.

A exibição [!UICONTROL Segments] também lista os seguintes tipos de segmento:

* Todos os segmentos personalizados criados pelo usuário disponíveis para o usuário.

  É possível visualizar tags de rastreamento para qualquer um dos segmentos personalizados que você criou e compartilhar esses segmentos com outros usuários. Também é possível editar ou excluir os segmentos personalizados criados.

  Você não pode editar ou compartilhar segmentos personalizados que outros usuários compartilharam com você.

* Todos os segmentos primários importados como estão e que estão disponíveis para o usuário.

  Não é possível editar ou compartilhar segmentos primários compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos primários com usuários adicionais.

* Todos os segmentos personalizados de terceiros disponíveis para o usuário.

  Não é possível editar ou compartilhar segmentos de terceiros que foram compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos de terceiros com usuários adicionais.

### A Visão de Fontes

No modo de exibição [!UICONTROL Sources], é possível configurar fontes para segmentos primários em plataformas de dados do cliente com suporte que você deseja converter em segmentos que contêm tipos de ID universal especificados. As configurações de origem incluem uma chave de origem gerada automaticamente, que você fornecerá à plataforma de dados do cliente para estabelecer a conexão.

Para obter mais informações sobre as plataformas de dados do cliente com suporte, os tipos de ID universal com suporte e os fluxos de trabalho para configurar conexões com cada plataforma de dados do cliente, consulte &quot;[Sobre Fontes](/help/dsp/audiences/sources/source-about.md).&quot;

Os segmentos traduzidos estão disponíveis para inclusão em públicos reutilizáveis e em configurações de posicionamento para direcionamento sem cookies.

>[!MORELIKETHIS]
>
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](/help/dsp/audiences/sources/source-manage.md)
>* [Importar manualmente os segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
