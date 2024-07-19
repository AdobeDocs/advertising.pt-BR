---
title: Visão geral da configuração de ofertas PG no  [!DNL Freewheel]
description: Saiba mais sobre os pré-requisitos e as etapas extras necessárias para executar anúncios de ofertas programáticas garantidas com editores no  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Visão Geral da Configuração de Ofertas Programáticas Garantidas no [!DNL Freewheel]

A configuração de ofertas programáticas garantidas com editores em [!DNL Freewheel] requer permissões e etapas adicionais.

>[!PREREQUISITES]
>
>Trabalhe com a equipe de conta do Adobe para garantir que a conta do [!DNL DSP] tenha as seguintes permissões:
>
>* Permissão para usar o fluxo de trabalho programático garantido [!DNL FreeWheel], que é necessário para enviar um anúncio para uma oferta programática garantida para [!DNL FreeWheel].
>
>* (Se você trabalhar com editores do Reino Unido que exigem um clock number [!DNL Clearcast] com cada anúncio) Permissão para incluir clock numbers em seus anúncios.

## Fluxo de trabalho (WRK)

1. Crie um anúncio com o tipo de mídia especificado no contrato.

   Para alguns editores do Reino Unido, você deve incluir um clock number [!DNL Clearcast] no seu anúncio.

1. [Aceite a ID de negócio](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) que você já negociou com um editor em [!DNL Freewheel] usando a Caixa de Entrada da ID de Negócio.

   Depois de aceitar o contrato, siga as instruções para 1) selecionar o anúncio a ser usado no contrato e 2) criar uma disposição padrão programática garantida para veicular o anúncio.

1. [Enviar o anúncio para  [!DNL Freewheel]](freewheel-submit.md)

   O anúncio deve ser enviado e aprovado antes de ser executado.

1. [Verifique o status de envio do anúncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Aceitar um acordo na Caixa de Entrada da ID do acordo](deal-id-inbox-accept.md)
>* [Enviar um anúncio para uma oferta programática garantida para [!DNL Freewheel]](freewheel-submit.md)
>* [Verifique o status dos anúncios para [!DNL FreeWheel] Ofertas programáticas garantidas](freewheel-check-status.md)
>* [Códigos de erro para [!DNL Freewheel] Envio de anúncios](freewheel-error-codes.md)
