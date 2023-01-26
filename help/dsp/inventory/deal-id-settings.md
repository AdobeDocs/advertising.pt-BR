---
title: Configurações de ID de contrato manual
description: Consulte descrições das configurações para IDs de negócios inseridas manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Configurações de ID de contrato manual

| Seção | Parâmetro | Descrição | Obrigatório | Editável |
|---------|-----------|-------------|----------|----------|
| [Detalhes do contrato] | [!UICONTROL Deal name] | O nome para identificar a [!UICONTROL Deal ID] em Advertising DSP. Insira um nome ou selecione **[!UICONTROL Auto-name]** permitir DSP gerar um nome com base nos detalhes da negociação.<br><br>Exemplo de um nome gerado automaticamente: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Sim | Sim |
|  | [!UICONTROL External deal ID] | A ID usada pelo editor e pela SSP para identificar essa negociação. | Sim | Não |
|  | [!UICONTROL Publisher] | O nome do editor que está vendendo este inventário. | Sim | Não |
|  | [!UICONTROL SSP] | A plataforma do lado do suprimento (PUP) pela qual esse negócio é executado. | Sim | Não |
|  | [!UICONTROL Media type] | O tipo de mídia comprada por meio desse negócio: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]* ou *[!UICONTROL Audio]*. As opções variam de acordo com a SSP.<br><br> Se a negociação permitir vários tipos de mídia, selecione o tipo de mídia para a disposição padrão quando você criar a negociação. Mais tarde, você pode alterar o valor, ou pode apenas [anexe uma nova disposição com o tipo de mídia adicional](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sim | Não |
|  | [!UICONTROL Deal type] | Compromisso de negócio e estrutura de preços:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Você e o editor não se comprometeram com um número fixo de deliveries de impressão. A operação especifica o preço mínimo do inventário, embora o CPM possa flutuar e aumentar em função das condições de mercado.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Você e o editor não se comprometeram com um número fixo de deliveries de impressão. O preço é a uma taxa fixa negociada.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Você e o editor concordaram com um número predefinido de impressões, direcionamento, datas de voo e preço fixo.<br><br><b>Observação:</b> As ofertas garantidas exigem datas de voo e um número específico de impressões no [!UICONTROL Tracking] seção. Você também deve criar uma disposição programática garantida (PG) padrão para o negócio e, como opção, pode usar a negociação para outras disposições.</li></ul> | Sim | Não |
|  | [!UICONTROL CPM] | O custo negociado por 1000 impressões (CPM). | Sim | Sim |
|  | [Moeda] | A moeda do negócio.<br><br>Todos os PUP aceitam acordos em USD. Quando o SSP aceitar a moeda da sua conta DSP, essa moeda também estará disponível. | Sim | Não |
|  | [!UICONTROL Billing method] | Todas as IDs de negócios são [!DNL Adobe]-financiados e faturados. DSP paga todos os fornecedores de mídia disponíveis com base no uso, gerencia discrepâncias com os fornecedores e envia uma fatura consolidada para a conta. Esta opção incorre em comissões adicionais, tal como descrito no cartão de crédito da conta. | Sim | Não |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | O endereço de email da conta de usuário que pode acessar a negociação. | Não | Sim |
|  | [!UICONTROL Advertisers that can access this deal] | Os anunciantes específicos na conta que podem acessar este negócio.<br><br><b>Observação:</b> Você pode compartilhar a negociação com anunciantes em contas adicionais da [!UICONTROL Deals] exibir. Na linha de negociação, clique em **[!UICONTROL #]**, clique em **[!UICONTROL share]** e, em seguida, compartilhe a negociação com um endereço de email. | Sim | Sim |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | As datas de início e término do tráfego que usa essa negociação. Essas datas são somente para fins de rastreamento e não afetam a entrega do anúncio.<br><br><b>Dica:</b> No [!UICONTROL Inventory] > [!UICONTROL Deals] , a [!UICONTROL Pacing & Budget] mostra como a negociação está indo para a data de voo e o objetivo de impressão especificados. Se o delivery estiver em um ritmo menor ou maior, entre em contato com o editor para ajustar o volume que ele está enviando por meio da negociação. | Negociações garantidas: Sim<br>Negociações não garantidas: Não | Sim |
|  | [!UICONTROL Impressions] | (Opcional para ofertas não garantidas) O número estimado de impressões que você espera executar usando esse negócio. Esse valor é somente para fins de rastreamento; o editor controla o delivery. | Negociações garantidas: Sim<br>Negociações não garantidas: Não | Sim |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Criar manualmente detalhes da ID do contrato](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)
>* [Sobre inventário privado](private-inventory-about.md)

