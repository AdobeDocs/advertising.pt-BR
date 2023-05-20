---
title: Sobre o gerenciamento de público-alvo na publicidade do DSP
description: Saiba mais sobre os recursos de gerenciamento de público-alvo.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Sobre o gerenciamento de público-alvo na publicidade do DSP

No DSP, é possível criar e gerenciar segmentos de público-alvo e conjuntos de público-alvo, que você pode usar como alvos para seus posicionamentos:

* Você pode coletar seus próprios dados de público-alvo primários criando e implementando segmentos. Posteriormente, você pode redirecionar os usuários no segmento com anúncios ou impedir que eles recebam anúncios. Você pode criar os seguintes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a) usuários expostos a anúncios de dispositivos de desktop, móveis e CTV e b) usuários que visitam páginas da Web específicas.

   * [Segmentos de não participação na venda do CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para rastrear as IDs de usuários de solicitações de cancelamento de venda do consumidor em seu site, de acordo com a California Consumer Privacy Act (CCPA). Você pode recuperar relatórios mensais das IDs de usuário de solicitações de recusa de venda.

      Para obter mais informações sobre o suporte de publicidade do Adobe para solicitações de recusa de venda do CCPA, consulte [Suporte de publicidade Adobe para a California Consumer Privacy Act: suporte de recusa do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* Você pode criar uma biblioteca de público-alvo de [públicos-alvo reutilizáveis](/help/dsp/audiences/reusable-audience-create.md). Os públicos-alvo salvos são compostos por qualquer segmento de público-alvo disponível e qualquer outro público-alvo salvo. Todas as alterações feitas em um público-alvo salvo são automaticamente aplicadas a todos os posicionamentos que direcionam ou excluem o público-alvo e a todos os outros públicos que incluem o público-alvo salvo.

   Públicos-alvo salvos permitem que os planejadores de mídia agrupem públicos-alvo conforme necessário, incluindo e excluindo vários segmentos que utilizam lógica booleana complexa. O tamanho de cada segmento individual e o tamanho total do público são indicados à medida que você cria um público. Os executores de campanha podem simplesmente selecionar um ou mais públicos-alvo salvos como alvos de posicionamento, em vez de configurar manualmente os alvos de público-alvo para cada posicionamento.

Outros tipos de público-alvo também estão disponíveis para o direcionamento de posicionamento.

## Importação de segmentos de dados próprios e de terceiros

O DSP pode importar seus próprios segmentos de dados primários da sua plataforma de gerenciamento de dados (DMP) e fornecê-los a qualquer conjunto de anunciantes, conforme necessário.

O DSP é um destino integrado para [o [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), permitindo que você compartilhe segmentos primários autenticados com anunciantes e usuários aprovados para ativação de campanha. Para saber mais sobre a integração do Real-Time CDP, consulte a [Seção Origens](/help/dsp/audiences/sources/source-about.md).

O DSP também pode importar segmentos personalizados de terceiros, incluindo combinações complexas de segmentos de terceiros. Você pode fornecer os segmentos a qualquer conjunto de anunciantes, conforme necessário.

Entre em contato com a equipe de conta do Adobe para obter mais informações.

## Públicos-alvo disponíveis como alvos de posicionamento

Você pode direcionar seus posicionamentos para todos os tipos de público a seguir.

* Todos os conjuntos de públicos-alvo criados pelo usuário que foram salvos no DSP.

* Todos os segmentos de público-alvo criados pelo usuário que foram criados no DSP:

   * Segmentos personalizados para usuários que visitaram páginas da Web específicas e usuários expostos a impressões de anúncios específicos.

   * Segmentos de público-alvo de não participação na venda do CCPA para usuários que enviaram solicitações de não participação na venda em seu site, de acordo com a California Consumer Privacy Act (CCPA).

* Todos os segmentos de dados primários importados.

* Todos os seus segmentos de dados personalizados de terceiros importados.

* (Posicionamentos direcionados somente aos EUA) [Todos os segmentos de dados de terceiros disponíveis para clientes DSP de mais de 30 provedores](/help/dsp/audiences/third-party-data-providers.md), incluindo [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]e muito mais.

   Você pode direcionar segmentos específicos, que direcionam usuários com base nos dados do público-alvo (por exemplo, usuários com demografia, interesses ou intenções específicos e/ou perfis comportamentais). Você pode procurar por provedor de dados e categoria, procurar segmentos por nome ou ID de segmento, ou filtrar os resultados por provedor de dados, tamanho total do segmento, contagem de navegadores da Web ou contagem de dispositivos.

   Os segmentos de terceiros incorrem em taxas adicionais, que são indicadas ao lado de cada nome de segmento.

* (Anunciantes com o Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics que usam somente tags de conversão JavaScript do Adobe Advertising ) Todos os segmentos de público-alvo primários, secundários ou de terceiros disponíveis criados no [!DNL Real-Time CDP], criado no Audience Manager ou publicado no Adobe Experience Cloud a partir do Audience Manager ou [!DNL Analytics].

   Os preços para o uso dos segmentos são pré-negociados e não são visíveis no DSP.

   Segmentos de [!DNL Analytics] estão disponíveis cerca de uma hora depois de criá-los ou publicá-los como públicos-alvo do Experience Cloud. Segmentos provenientes diretamente do Audience Manager ou [!DNL Real-Time CDP] estão disponíveis em 24 horas após o compartilhamento.

   >[!NOTE]
   >
   >Consulte a documentação para [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), e [o [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) para obter informações sobre como configurar e coletar dados para segmentos nessas soluções.

## Dados de tamanho do público

Nas configurações de público-alvo salvas e de posicionamento, você pode ver dados detalhados sobre o tamanho do público-alvo:

* O tamanho total e ativo do público desduplicado em todos os segmentos selecionados e salvos é exibido e você pode exibir detalhes por tipo de dispositivo (navegador, celular ou TV conectada).

   ![o tamanho combinado do público-alvo](/help/dsp/assets/audience-size.png)

* Para segmentos individuais e públicos-alvo salvos, o tamanho total do público-alvo e o CPM (quando aplicável) são exibidos ao lado do nome do segmento. Você pode ver mais detalhes sobre o segmento, incluindo o tamanho por tipo de dispositivo (navegador, celular ou TV conectada). Para públicos salvos, o tamanho total é o total desduplicado.

   ![o tamanho do segmento individual](/help/dsp/assets/audience-size-segment.png)

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

* Todos os segmentos primários importados disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos primários compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos primários com usuários adicionais.

* Todos os segmentos personalizados de terceiros disponíveis para o usuário.

   Não é possível editar ou compartilhar segmentos de terceiros que foram compartilhados com você. Entre em contato com a equipe de conta do Adobe se precisar compartilhar segmentos de terceiros com usuários adicionais.

>[!MORELIKETHIS]
>
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Configurações de público](audience-settings.md)
>* [Sintaxe da lógica do segmento de público-alvo](audience-segment-logic-syntax.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar uma [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

