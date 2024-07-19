---
title: Usando o  [!DNL Roku] Inventário
description: Saiba mais sobre a parceria do DSP com o  [!DNL Roku], incluindo opções de inventário, fornecedores de rastreamento de terceiros aprovados e práticas recomendadas para posicionamentos específicos do  [!DNL Roku].
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Usando o Inventário [!DNL Roku]

O Advertising DSP fornece recursos para publicidade em [!DNL Roku].

## Correspondência de público

A parceria do [!DNL Roku] e do DSP corresponde seus públicos do [!DNL DSP] a [!DNL Roku] IDs para direcionamento de público determinístico 1:1 no inventário [!DNL Roku].

## [!DNL Roku] Opções de inventário

Você pode a) configurar IDs de negócios privadas diretamente com [!DNL Roku] e inserir os dados da ID de negócios no DSP ou b) visitar a Galeria [!DNL On Demand] para assinar [!DNL Roku] perfis:

>[!NOTE]
>
>O inventário [!DNL Roku] não está disponível em marketplaces e bolsas abertos.

* Para suas ofertas privadas, [configure informações sobre as IDs de negócios no DSP](/help/dsp/inventory/deal-id-create.md) e direcione &quot;[!UICONTROL Roku Network - Audience]&quot; e &quot;[!UICONTROL The Roku Channel - Audience]&quot; em [!DNL Roku] posicionamentos.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Você pode [assinar o seguinte [!DNL Roku] inventário na [!DNL On Demand] Galeria](/help/dsp/inventory/on-demand-inventory-subscribe.md) e depois direcionar qualquer oferta aprovada em [!DNL Roku] posicionamentos:

   * &quot;[!UICONTROL Roku Network - Audience]&quot; para inventário no ecossistema [!DNL Roku] com parceiros de conteúdo premium, como [!DNL The CW], [!DNL ABC] e [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; para [!DNL Roku] conteúdo de aplicativo (O&amp;O) próprio e operado.

### Vantagens de personalizar mercados privados com o [!DNL Roku]

As ofertas privadas permitem personalizar os parâmetros da negociação de acordo com suas necessidades.

* **Preços negociados:** trabalhe com a equipe de vendas [!DNL Roku] para negociar e estruturar um negócio que atenda às suas necessidades de campanha.

* **Prioridade de escala:** os marketplaces privados (PMPs) recebem prioridade mais alta do que as ofertas sempre ativas (como [!DNL On Demand] ofertas).

* **Gerenciamento de Frequência:** o limite de frequência padrão [!DNL Roku] é de um (1) anúncio por 30 minutos por usuário, mas você pode personalizar o limite por hora, dia, semana, mês ou período inteiro de voo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Direcionamento de Dados:** [!DNL Roku] públicos-alvo são criados a partir de [!DNL Roku] sinais de dispositivo e de TV, dados rastreados por [!DNL The Roku Channel] (como afinidade de gênero de TV, comportamento de transmissão de TV e status de assinatura de cabo) e dados adicionais do [!DNL Roku] sistema de CRM (relacionamento com o cliente).

* incluir na lista de bloqueios **[!DNL Roku]Direcionamento de conteúdo:** As ofertas privadas podem direcionar aplicativos por gênero, aplicação da pesquisa de aplicativo, eventos sazonais e de tipoes e apresentações somente no [!DNL The Roku Channel].

## [!DNL Roku] Posicionamentos

Em campanhas DSP, [crie [!DNL Roku] posicionamentos específicos](/help/dsp/campaign-management/placements/placement-create.md) usando o tipo de posicionamento &quot;[!UICONTROL Connected TV (Roku)].&quot; Incluir [!DNL Roku] posicionamentos em [!DNL Roku] pacotes específicos com metas definidas.

Cada posicionamento de [!DNL Roku] deve ter como alvo pelo menos um negócio ou origem de [!DNL Roku]. Para usar a correspondência de público-alvo do DSP com [!DNL Roku], inclua um ou mais segmentos de público-alvo que possam ser comparados com o conjunto de dados determinísticos [!DNL Roku] (aceitação).

### [!DNL Roku]-Aprovados Fornecedores De Rastreamento De Terceiros

[!DNL Roku] posicionamentos podem incluir pixels de eventos de terceiros e pixels de conversão dos seguintes fornecedores: [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] e [!DNL Research Now].

### Práticas recomendadas por estratégia de posicionamento

Estas são as práticas recomendadas para posicionamentos específicos do [!DNL Roku].

Para maximizar o alcance incremental:

* Suprima públicos expostos em [!DNL Roku O&O] excluindo públicos que você já atingiu usando [!DNL The Roku Channel].

* Suprima os públicos expostos em [!DNL All Roku] excluindo os públicos que você já atingiu na plataforma [!DNL Roku].

Para a configuração mais rápida:

* Direcione ofertas existentes e sempre ativas para [!DNL The Roku Channel] no [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para acessar rapidamente o [!DNL Roku] inventário próprio e operado.
* Faça o direcionamento de ofertas existentes e sempre ativas para [!DNL Roku Network] no [[!DNL On Demand] Inventário](/help/dsp/inventory/on-demand-inventory-subscribe.md) para atingir rapidamente a escala na plataforma [!DNL Roku].

Para escala máxima:

* Personalize um marketplace privado de [!DNL Roku] para acesso priorizado ao fornecimento de [!DNL Roku] a um preço negociado.

>[!MORELIKETHIS]
>
>* [Criar manualmente os detalhes da ID do contrato](/help/dsp/inventory/deal-id-create.md)
> * [Assinar e solicitar acesso a [!DNL On Demand] Contratos de Inventário Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Criar um posicionamento](/help/dsp/campaign-management/placements/placement-create.md)
