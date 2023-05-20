---
title: Visão geral da configuração de ofertas PG no [!DNL Freewheel]
description: Saiba mais sobre os pré-requisitos e as etapas adicionais necessárias para executar anúncios para ofertas programáticas garantidas com editores no [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Visão geral da configuração de ofertas programáticas garantidas no [!DNL Freewheel]

Configuração de ofertas programáticas garantidas com editores no [!DNL Freewheel] O requer permissões e etapas adicionais.

>[!PREREQUISITES]
>
>Trabalhe com a equipe de conta do Adobe para garantir que as [!DNL DSP] A conta do tem as seguintes permissões:
>
>* Permissão para usar o [!DNL FreeWheel] fluxo de trabalho programático garantido, que é necessário para enviar um anúncio para um contrato programático garantido para o [!DNL FreeWheel].
>
>* (Se você trabalhar com editores do Reino Unido que exigem uma [!DNL Clearcast] clock number com cada anúncio) Permissão para incluir clock numbers em seus anúncios.


## Fluxo de trabalho (WRK)

1. Crie um anúncio com o tipo de mídia especificado no contrato.

   Para alguns editores do Reino Unido, você deve incluir uma [!DNL Clearcast] clock number com seu anúncio.

1. [Aceitar a ID do negócio](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) que você já negociou com um editor em [!DNL Freewheel] usando a Caixa de entrada ID do contrato.

   Depois de aceitar o contrato, siga as instruções para 1) selecionar o anúncio a ser usado no contrato e 2) criar uma disposição padrão programática garantida para veicular o anúncio.

1. [Envie o anúncio para [!DNL Freewheel]](freewheel-submit.md)

   O anúncio deve ser enviado e aprovado antes de ser executado.

1. [Verifique o status de envio do anúncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Aceitar uma oferta na caixa de entrada da ID de oferta](deal-id-inbox-accept.md)
>* [Envie um anúncio para um contrato programático garantido para [!DNL Freewheel]](freewheel-submit.md)
>* [Verifique o status dos anúncios para [!DNL FreeWheel] Ofertas programáticas garantidas](freewheel-check-status.md)
>* [Códigos de erro para [!DNL Freewheel] Envio de anúncios](freewheel-error-codes.md)

