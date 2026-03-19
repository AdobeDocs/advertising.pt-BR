---
title: Configurar um contrato programático garantido
description: Saiba como configurar um contrato programático garantido (PG) que você negociou com um editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 54f69e4c0fa20b918a037cc5d2003d67db889913
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Configurar um contrato programático garantido

*[Somente plataformas do lado do suprimento com suporte](programmatic-guaranteed-about.md)*

Depois de negociar um contrato programático garantido (PG) com um editor suportado, você pode configurar o contrato no DSP usando o [!DNL Deal ID Inbox] ou inserindo manualmente os detalhes do contrato.

>[!NOTE]
>
> Para ofertas PG, o editor lida com todo o ritmo do orçamento, limite de orçamento e direcionamento. Todos os SSPs que permitem PG por meio do DSP confirmam que o editor pode configurar limite de orçamento.
>
> A configuração de ofertas programáticas garantidas com editores em [!DNL FreeWheel] requer permissões e etapas adicionais. Consulte &quot;[Visão geral da configuração de ofertas programáticas garantidas no [!DNL FreeWheel]](freewheel-overview.md)&quot; para obter mais informações.

## Configurar um negócio programático garantido usando o [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

O método a seguir é o procedimento preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers] e [!DNL Magnite DV+].

1. [Aceite o acordo](deal-id-inbox-accept.md).

1. Depois de salvar o contrato, selecione o pixel de rastreamento dos anúncios (ou o pixel de rastreamento 1x1 para anúncios gerenciados pelo editor) a ser usado para o contrato e crie uma disposição padrão programática garantida (PG), conforme solicitado.

   Criar uma disposição PG padrão para o negócio é obrigatório para entregar 100% da sua compra. Esse tipo de posicionamento não tem direcionamento, portanto, o DSP pode retornar um lance para cada solicitação de lance do editor.

   * Se você estiver aceitando um único contrato, será automaticamente redirecionado para o fluxo de trabalho de criação de posicionamento padrão de PG.

     Todas as [!DNL FreeWheel] ofertas são propostas como uma única oferta.

   * Se você estiver aceitando uma proposta com várias IDs de contrato PG, identifique cada posicionamento padrão PG que você precisa criar. Depois de criar todos os posicionamentos necessários, o botão Continuar será ativado.

1. (Opcional) Direcione o contrato PG em posicionamentos PG ou não-PG adicionais clicando em ![menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Uma oferta pode visar vários posicionamentos que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

## Configurar manualmente um contrato programático garantido

Use este método para todos os outros SSPs.

1. [Configurar manualmente os detalhes da ID de negócios](deal-id-create.md).

1. Depois de salvar a oferta, selecione os pixels de rastreamento de anúncios (ou 1x1 para anúncios gerenciados pelo editor) a serem usados para a oferta e crie uma disposição padrão PG, conforme solicitado.

   Criar uma disposição padrão PG para o negócio é obrigatório para entregar 100% da sua compra. Esse tipo de posicionamento não tem direcionamento, portanto, o DSP pode retornar um lance para cada solicitação de lance do editor.

1. (Opcional) Direcione o contrato PG em posicionamentos PG ou não-PG adicionais clicando em ![menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Uma oferta pode visar vários posicionamentos que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

>[!MORELIKETHIS]
>
>* [Sobre ofertas programáticas garantidas](programmatic-guaranteed-about.md)
>* [Dicas para negociar um contrato programático garantido](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Enviar um anúncio para um contrato programático garantido com o  [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceitar um contrato no [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Criar manualmente os detalhes da ID de negócios](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)
>* [Visão geral dos recursos de inventário no Advertising DSP](inventory-overview.md)
