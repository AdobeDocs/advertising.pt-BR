---
title: '[!UICONTROL Simple Ad Serving] Configurações do negócio'
description: Saiba mais sobre as configurações disponíveis para o [!UICONTROL Simple Ad Serving] negócios.
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Configurações de oferta

## Novo [!UICONTROL Simple Ad Serving] Transações

### [!UICONTROL Select Ad Source]

| Parâmetro | Descrição |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | O tipo de mídia para este negócio: *[!UICONTROL Video],* *[!UICONTROL Display],* ou *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | O nome do publicador que está vendendo este estoque. Procure um editor inserindo pelo menos os dois primeiros caracteres no nome. Para adicionar um editor que não esteja listado, entre em contato com a equipe de conta do Adobe. |
| **[!UICONTROL Advertiser]** | Um único anunciante na conta que pode acessar esta oferta. Selecione também a campanha e (opcionalmente) o pacote no qual o contrato está disponível. |
| **[!UICONTROL Media Quality Assessment?]** | (Alguns usuários) Permite que o anúncio seja executado em outro DSP para verificação de terceiros. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | A única opção é *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Somente novas ofertas) Se deseja:<ul><li>*[!UICONTROL Create New]:* Para criar um anúncio para esta oferta.</li><li>*[!UICONTROL Select Ads]:* Para usar um anúncio existente para esta oferta.</li></ul> |
| **[!UICONTROL Ad Type]** | O tipo de anúncio para esta oferta. Se você for criar anúncios para o negócio, inclua o tamanho ou a duração do anúncio, conforme solicitado. As opções disponíveis variam de acordo com o tipo de mídia. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(Quando estiver usando anúncios existentes) Os anúncios a serem incluídos na oferta. Marque a caixa de seleção ao lado de cada anúncio a ser incluído.

### [!UICONTROL Select & Upload [Media Type]]

(Somente para novos anúncios) Telas para criar um novo [anúncio de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parâmetro | Descrição |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | O custo por 1000 impressões (CPM), conforme refletido no cartão de tarifa do seu contrato. Entre em contato com a equipe de conta do Adobe para obter esse valor. <br><br>Especificar também a moeda da transação. Todos os usuários podem selecionar USD ou, se a SSP oferecer suporte a moedas adicionais, a moeda da conta DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Opcional) Uma taxa estática de terceiros a ser rastreada como um custo não faturável e a moeda da transação.<br><br>Todos os usuários podem selecionar USD ou, se a SSP oferecer suporte a moedas adicionais, a moeda da conta DSP. **NOTA:** As taxas faturáveis são refletidas na [!UICONTROL Net CPM] métrica. |
| **[!UICONTROL Third Party Fee Description]** | (Opcional) Uma descrição das taxas de terceiros. |
| **[!UICONTROL Flight Dates]** | As datas de início e término do tráfego que usa esta oferta. As datas de voo devem ser incluídas nas datas de voo da campanha. As tags de anúncio retornam uma resposta somente durante o voo especificado.<br><br> A prática recomendada para criar uma campanha de veiculação de anúncios simples separada com um ano de duração e criar pixels de rastreamento dentro dela. |
| **[!UICONTROL Impressions]** | (Opcional) O número estimado de impressões que você espera executar usando esta oferta. Esse valor é usado somente para fins de rastreamento e para sinalizar quando as metas de entrega são atendidas; o editor controla a entrega de anúncios real. A prática recomendada é inserir um alto número de impressões para manter a tag ativa no DSP para que ela possa ser renovada ou estendida, se necessário. |
| **[!UICONTROL Deal Name]** | O nome do negócio. Insira um nome ou selecione *[!UICONTROL Auto Generate Deal Name]* para permitir que o DSP gere um nome com base nos detalhes do negócio.<br><br>Exemplo de um nome gerado automaticamente: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Somente leitura) Os anúncios que fazem parte do negócio. Para editar um anúncio, clique no nome do anúncio. Para remover um anúncio do contrato, clique em **[!UICONTROL X]** ao lado do nome do anúncio. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Sobre [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Criar um [!UICONTROL Simple Ad Serving] Negociação](simple-deal-create.md)
>* [Editar [!UICONTROL Simple Ad Serving] Configurações de oferta](simple-deal-edit.md)
>* [Exibir um Relatório Detalhado de uma Transação](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
