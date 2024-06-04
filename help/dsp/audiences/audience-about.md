---
title: Sobre o gerenciamento de público-alvo na publicidade do DSP
description: Saiba mais sobre os recursos de gerenciamento de público-alvo.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 94c41ec311ed79897e1e26a650605c0213450071
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---

# Sobre o gerenciamento de público-alvo na publicidade do DSP

No DSP, é possível criar e gerenciar segmentos de público-alvo e conjuntos de público-alvo, que você pode usar como alvos para seus posicionamentos:

* Colete seus próprios dados de público-alvo primários criando e implementando segmentos de DSP. Posteriormente, você pode redirecionar os usuários no segmento com anúncios ou impedir que eles recebam anúncios. Você pode criar os seguintes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a) usuários expostos a anúncios de dispositivos móveis e de desktop e b) usuários que visitam páginas da Web específicas. A tag de rastreamento pode rastrear usuários baseados em cookies ou usuários associados a IDs universais de ID5.

   * [Segmentos de não participação na venda do CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear as IDs de usuários de solicitações de cancelamento de venda do consumidor em seu site, de acordo com a California Consumer Privacy Act (CCPA). Você pode recuperar relatórios mensais das IDs de usuário de solicitações de recusa de venda.

     Para obter mais informações sobre o suporte do Adobe Advertising para solicitações de recusa de venda do CCPA, consulte [Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento da participação do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Recurso Beta) [Obter e usar IDs universais para direcionamento sem cookies](/help/dsp/audiences/universal-ids.md):

   * Envie manualmente o seu certificado [!DNL LiveRamp] [!DNL RampID] segmentos diretamente para o DSP.

   * Permitir que o DSP importe segmentos primários da sua plataforma de dados do cliente e traduza-os para tipos de ID universal compatíveis.

   * Inclua segmentos de terceiros que contenham IDs universais em seus destinos de posicionamento sem etapas extras.

* Criar uma biblioteca de público-alvo de [públicos-alvo reutilizáveis](/help/dsp/audiences/reusable-audience-create.md). Os públicos-alvo salvos são compostos por qualquer segmento de público-alvo disponível e qualquer outro público-alvo salvo. Todas as alterações feitas em um público-alvo salvo são automaticamente aplicadas a todos os posicionamentos que direcionam ou excluem o público-alvo e a todos os outros públicos que incluem o público-alvo salvo.

  Públicos-alvo salvos permitem que os planejadores de mídia agrupem públicos-alvo conforme necessário, incluindo e excluindo vários segmentos que utilizam lógica booleana complexa. O tamanho de cada segmento individual e o tamanho total do público são indicados à medida que você cria um público. Os executores de campanha podem simplesmente selecionar um ou mais públicos-alvo salvos como alvos de posicionamento, em vez de configurar manualmente os alvos de público-alvo para cada posicionamento.

Outros tipos de público-alvo também estão disponíveis para o direcionamento de posicionamento.

## Importação de segmentos de dados próprios e de terceiros

Você tem muitas opções para importar segmentos de dados primários e de terceiros para o DSP, usando a interface do usuário DSP e/ou por meio de serviços de importação personalizados.

* O DSP pode obter seu Adobe Audience Manager e outros [!DNL Adobe] públicos-alvo para direcionamento. Para obter os pré-requisitos e as instruções, consulte &quot;[Importar segmentos do Adobe Audience Manager para direcionamento de anúncios](/help/integrations/audience-manager/import-audiences.md).

* O DSP pode traduzir segmentos de dados primários de plataformas de dados de clientes compatíveis para segmentos com IDs universais usando o [Recurso de origens](/help/dsp/audiences/sources/source-about.md). Também é possível [enviar manualmente seu certificado [!DNL LiveRamp] [!DNL RampID] Segmentos diretamente para DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

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

  Taxas adicionais são cobradas por impressões entregues a IDs universais. Consulte &quot;[Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)&quot; para taxas.

* Todos os seus segmentos de dados personalizados de terceiros importados.

* (Posicionamentos direcionados somente aos EUA) [Todos os segmentos de dados de terceiros disponíveis para clientes DSP de mais de 30 provedores](/help/dsp/audiences/third-party-data-providers.md), incluindo [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]e muito mais.

  Você pode direcionar segmentos específicos, que direcionam usuários com base nos dados do público-alvo (por exemplo, usuários com demografia, interesses ou intenções específicos e/ou perfis comportamentais). Você pode procurar por provedor de dados e categoria, procurar segmentos por nome ou ID de segmento, ou filtrar os resultados por provedor de dados, tamanho total do segmento, contagem de navegadores da Web ou contagem de dispositivos.

  Os segmentos de terceiros incorrem em taxas adicionais, que são indicadas ao lado de cada nome de segmento.

* (Anunciantes com o Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics que usam somente tags de conversão JavaScript do Adobe Advertising) Todos os segmentos de público-alvo primários, secundários ou de terceiros disponíveis criados no [!DNL Real-Time CDP], criado no Audience Manager ou publicado no Adobe Experience Cloud a partir do Audience Manager ou [!DNL Analytics].

  Os preços para o uso dos segmentos são pré-negociados e não são visíveis no DSP.

  Segmentos de [!DNL Analytics] estão disponíveis cerca de uma hora depois de criá-los ou publicá-los como públicos-alvo do Experience Cloud. Segmentos provenientes diretamente do Audience Manager ou [!DNL Real-Time CDP] estão disponíveis em 24 horas após o compartilhamento.

  >[!NOTE]
  >
  >Consulte a documentação para [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), e [o [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) para obter informações sobre como configurar e coletar dados para segmentos nessas soluções.

## Dados de tamanho do público

Em Públicos-alvo > Todos os públicos-alvo e na seção Direcionamento de público das configurações de posicionamento, você pode filtrar cada lista de segmentos por intervalo de tamanho, incluindo o intervalo total e intervalos separados para tipos de dispositivo específicos ou tipos de ID universal.

![filtrar por tamanho do público](/help/dsp/assets/audience-size-filter.png)

Você também pode ver dados detalhados sobre o tamanho do público-alvo:

* O tamanho total e ativo do público desduplicado em todos os segmentos selecionados e salvos é exibido e você pode exibir detalhes por tipo de dispositivo (navegador, celular ou TV conectada).

  ![o tamanho combinado do público-alvo](/help/dsp/assets/audience-size.png)

* Para segmentos individuais, o tamanho total do público-alvo e o CPM (quando aplicável) são exibidos ao lado do nome do segmento.

  ![o tamanho do segmento individual](/help/dsp/assets/audience-size-segment.png)

* Você pode ver mais detalhes sobre um segmento individual ou público-alvo salvo, incluindo o tamanho por navegador, celular, TV conectada e parceiro de tipo de ID universal. Para públicos salvos, o tamanho total é o total desduplicado.

  ![o segmento individual ou os detalhes do público-alvo salvo](/help/dsp/assets/audience-size-segment-details.png)

## As Visualizações de Públicos-alvo

### A visualização Todos os públicos-alvo

No [!UICONTROL All Audiences] exibir ou Biblioteca de público-alvo, você pode salvar e gerenciar públicos-alvo reutilizáveis, que incluem grupos de segmentos de público-alvo e até mesmo outros públicos-alvo salvos. Você pode usar públicos-alvo como destinos para vários posicionamentos. O número de disposições em que cada público-alvo é usado é indicado ao lado do nome da disposição.

Você pode editar, clonar, excluir, exportar ou compartilhar qualquer público-alvo.

### A visualização Segmentos

No [!UICONTROL Segments] todos os usuários podem criar segmentos personalizados adicionais.

A variável [!UICONTROL Segments] Essa visualização também lista os seguintes tipos de segmentos:

* Todos os segmentos personalizados criados pelo usuário disponíveis para o usuário.

  É possível visualizar tags de rastreamento para qualquer um dos segmentos personalizados que você criou e compartilhar esses segmentos com outros usuários. Também é possível editar ou excluir os segmentos personalizados criados.

  Você não pode editar ou compartilhar segmentos personalizados que outros usuários compartilharam com você.

* Todos os segmentos primários importados como estão e que estão disponíveis para o usuário.

  Não é possível editar ou compartilhar segmentos primários compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos primários com usuários adicionais.

* Todos os segmentos personalizados de terceiros disponíveis para o usuário.

  Não é possível editar ou compartilhar segmentos de terceiros que foram compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos de terceiros com usuários adicionais.

### A Visão de Fontes

No [!UICONTROL Sources] Na visualização, você pode configurar fontes para segmentos primários em plataformas de dados do cliente compatíveis que você deseja converter em segmentos que contêm tipos de ID universal especificados. As configurações de origem incluem uma chave de origem gerada automaticamente, que você fornecerá à plataforma de dados do cliente para estabelecer a conexão.

Para obter mais informações sobre as plataformas de dados do cliente compatíveis, os tipos de ID universal compatíveis e os workflows para configurar conexões com cada plataforma de dados do cliente, consulte &quot;[Sobre Origens](/help/dsp/audiences/sources/source-about.md).&quot;

Os segmentos traduzidos estão disponíveis para inclusão em públicos reutilizáveis e em configurações de posicionamento para direcionamento sem cookies.

>[!MORELIKETHIS]
>
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar uma [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Importar segmentos autenticados manualmente do [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
