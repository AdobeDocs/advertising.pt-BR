---
title: Sobre o [!UICONTROL Deal ID Inbox]
description: Saiba mais sobre o [!UICONTROL Deal ID inbox] recurso, que permite que você aceite ofertas privadas que já negociou com editores no [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conhecido como [!DNL AdX]), and [!DNL Magnite DV+] (antigo [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Sobre o [!UICONTROL Deal ID Inbox]

O DSP da publicidade [!UICONTROL Deal ID inbox] O permite configurar rapidamente as negociações que o DSP importou dos editores por meio das plataformas do lado do suprimento (SSPs), de modo que não seja necessário configurar cada negociação manualmente. Você pode aceitar as ofertas de estoque privado garantidas e não garantidas que você já negociou com editores em [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conhecido como [!DNL AdX]) e [!DNL Magnite DV+] (antigo [!DNL Rubicon]) do [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>O DSP publicitário é o primeiro DSP a integrar-se com o [!DNL FreeWheel] API.

No [!UICONTROL Deal ID inbox], você poderá ver os detalhes do negócio à medida que o editor os vir, acelerar a configuração do negócio e evitar erros de entrada manual.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

O DSP atualiza automaticamente todos os detalhes do negócio diariamente às 4h30 EST. Também atualiza todos os [!DNL FreeWheel] ofertas e atualiza ofertas existentes de [!DNL Google] e [!DNL Magnite DV+] por hora. Você também pode atualizar manualmente os detalhes do negócio para preencher novos negócios a qualquer momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para ofertas programáticas garantidas por meio de [!DNL Google Authorized Buyers], você deverá atingir pelo menos 90% do orçamento, caso contrário sua conta perderá o acesso a [!DNL Google] ofertas na [!UICONTROL Deal ID inbox].

## A implementação da [!UICONTROL Deal ID Inbox]

Para receber suas ofertas no [!UICONTROL Deal ID inbox], suas contas SSP devem mapear a conta DSP de sua organização para sua conta SSP. O DSP compartilhará os nomes das contas da organização com os SSPs relevantes. Entre em contato com a equipe de conta do Adobe para obter instruções.

Durante as negociações, peça ao editor para enviar o negócio para seu comprador em vez de para a conta pai do DSP. O identificador de negócios pode ser um nome ou uma ID, dependendo da SSP.

## Ações que você pode realizar em suas negociações

* **Revisar ofertas** para verificar se a SSP enviou o editor correto, as datas de ativação, o CPM e outros detalhes do negócio. Se o editor tiver cometido um erro, entre em contato com ele fora do DSP para que ele possa corrigir e reenviar o negócio.

* **Aceitar ofertas** após a revisão, e não aparecerão mais no [!UICONTROL Deal ID inbox]. As ofertas aceitas estão listadas em [!UICONTROL Inventory] > [!UICONTROL Deals] e estão prontos para direcionar nos posicionamentos dos anunciantes.

* **Ignorar ofertas** que não são necessários ou não são solicitados. As ofertas ignoradas são movidas para a [!UICONTROL Ignored Deals] na guia [!UICONTROL Deal ID inbox], que serve como um arquivo. O DSP não alerta SSPs e editores quando você ignora um acordo.

* **Modificar detalhes de ofertas já aceitas** de [!UICONTROL Inventory] > [!UICONTROL Deals] (não no [!UICONTROL Deal ID inbox]). Da mesma forma, quando os editores enviam alterações aos negócios, os anunciantes são responsáveis por implementar essas alterações no [!UICONTROL Inventory] > [!UICONTROL Deals] porque a variável [!UICONTROL Deal ID inbox] O não sincroniza alterações das SSPs após a configuração de ofertas.

## Que tipos de ofertas não podem ser aceitas?

Quando uma listagem de negócios não inclui uma ![Aceitar](/help/dsp/assets/accept.png) ícone ou um [!UICONTROL Accept] você não pode aceitá-lo no [!UICONTROL Deal ID inbox]. Em vez disso, você pode [criar os detalhes da ID de negócios manualmente](/help/dsp/inventory/deal-id-create.md).

Você não pode aceitar os seguintes tipos de negócios:

* [!DNL Google] ofertas que não estão em USD.

* [!DNL Magnite DV+] ofertas que não estão em USD

* [!DNL FreeWheel] ofertas que não estão na moeda da sua conta.

* Transações com data de término anterior a hoje.

* Antigo [!DNL Magnite DV+] negócios que foram rotulados como &quot;vários tipos de mídia&quot;.

Os detalhes da transação incluem o motivo pelo qual a transação não está disponível para aceitação.

>[!MORELIKETHIS]
>
>* [Aceitar uma oferta na caixa de entrada da ID de oferta](deal-id-inbox-accept.md)
>* [Visão Geral dos Recursos do Inventário](inventory-overview.md)

