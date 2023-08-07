---
title: Configurar um acordo programático garantido
description: Saiba como configurar um contrato programático garantido (PG) que você negociou com um editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: d5a291c8d1f464e1c22777512d29f4e041bb7988
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Configurar um acordo programático garantido

*[Somente plataformas do lado da fonte compatíveis](programmatic-guaranteed-about.md)*

Depois de negociar um contrato programático garantido (PG) com um editor suportado, é possível configurar o contrato no DSP usando o [!DNL Deal ID inbox] ou inserindo manualmente os detalhes do negócio.

>[!NOTE]
>
> Para ofertas PG, o editor lida com todo o ritmo do orçamento, limite de orçamento e direcionamento. Todos os SSPs que permitem PG por meio de DSP confirmam que o editor pode configurar limite de orçamento.
>
> Configuração de ofertas programáticas garantidas com editores no [!DNL FreeWheel] O requer permissões e etapas adicionais. Consulte &quot;[Visão geral da configuração de ofertas programáticas garantidas no [!DNL FreeWheel]](freewheel-overview.md)&quot; para obter mais informações.

## Configurar um acordo programático garantido usando o [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

O método a seguir é o procedimento preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers], e [!DNL Magnite DV+].

1. [Aceite o acordo](deal-id-inbox-accept.md).

1. Depois de salvar o negócio, selecione os anúncios (ou o pixel de rastreamento 1x1 para anúncios gerenciados pelo editor) que serão usados para o negócio e crie uma disposição padrão programática garantida (PG), conforme solicitado.

   Criar uma disposição PG padrão para o negócio é obrigatório para entregar 100% da sua compra. Esse tipo de posicionamento não tem direcionamento, portanto, o DSP pode retornar um lance para cada solicitação de lance do editor.

   * Se você estiver aceitando um único contrato, será automaticamente redirecionado para o fluxo de trabalho de criação de posicionamento padrão de PG.

     Todos [!DNL FreeWheel] são propostos como um único acordo.

   * Se você estiver aceitando uma proposta com várias IDs de contrato PG, identifique cada posicionamento padrão PG que você precisa criar. Depois de criar todos os posicionamentos necessários, o botão Continuar será ativado.

1. (Opcional) Direcione o contrato PG em inserções PG ou não PG adicionais clicando em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Uma oferta pode visar vários posicionamentos que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

## Configurar manualmente uma oferta programática garantida

Use este método para todos os outros SSPs.

1. [Configurar manualmente os detalhes da ID de negócios](deal-id-create.md).

1. Depois de salvar o negócio, selecione os anúncios (ou o pixel de rastreamento 1x1 para anúncios gerenciados pelo editor) que serão usados para o negócio e crie um posicionamento padrão PG, conforme solicitado.

   Criar uma disposição padrão PG para o negócio é obrigatório para entregar 100% da sua compra. Esse tipo de posicionamento não tem direcionamento, portanto, o DSP pode retornar um lance para cada solicitação de lance do editor.

1. (Opcional) Direcione o contrato PG em inserções PG ou não PG adicionais clicando em ![Menu Opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Uma oferta pode visar vários posicionamentos que suportam qualquer combinação de tipos de mídia (como TV conectada, desktop e áudio).

>[!MORELIKETHIS]
>
>* [Sobre Ofertas Programáticas Garantidas](programmatic-guaranteed-about.md)
>* [Dicas para negociar um acordo programático garantido](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Enviar um anúncio para uma oferta programática garantida com [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceitar uma oferta na caixa de entrada da ID de oferta](deal-id-inbox-accept.md)
>* [Criar manualmente detalhes da ID do contrato](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)
>* [Visão Geral dos Recursos do Inventário](inventory-overview.md)
