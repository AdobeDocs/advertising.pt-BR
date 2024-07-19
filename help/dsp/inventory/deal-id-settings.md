---
title: Configurações da ID de oferta manual
description: Consulte descrições das configurações para IDs de negócios inseridas manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Configurações da ID de oferta manual

| Seção | Parâmetro | Descrição | Obrigatório | Editável |
|---------|-----------|-------------|----------|----------|
| [Detalhes do contrato] | [!UICONTROL Deal name] | O nome para identificar seu [!UICONTROL Deal ID] no Advertising DSP. Insira um nome ou selecione **[!UICONTROL Auto-name]** para permitir que o DSP gere um nome com base nos detalhes do negócio.<br><br>Exemplo de um nome gerado automaticamente: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Sim | Sim |
| | [!UICONTROL External deal ID] | A ID usada pelo editor e pelo SSP para identificar esta oferta. | Sim | Não |
| | [!UICONTROL Publisher] | O nome do publicador que está vendendo este estoque. | Sim | Não |
| | [!UICONTROL SSP] | A plataforma do lado do suprimento (SSP) pela qual este negócio é executado. | Sim | Não |
| | [!UICONTROL Media type] | O tipo de mídia comprado através desta oferta: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* ou *[!UICONTROL Publisher Managed]*. As opções variam de acordo com a SSP.<br><br> Se o contrato permitir vários tipos de mídia, selecione o tipo de mídia para o posicionamento padrão ao criar o contrato. Posteriormente, você poderá alterar o valor ou apenas [anexar um novo posicionamento com o tipo de mídia adicional](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sim | Não |
| | [!UICONTROL Deal type] | O compromisso de negócios e a estrutura de preços:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: você e o editor não confirmaram um número fixo de entregas de impressão. O acordo especifica o preço mínimo para o inventário, embora a CPM possa flutuar e aumentar dependendo das condições de mercado.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: você e o editor não confirmaram um número fixo de entregas de impressão. Os preços estão a uma taxa fixa negociada.</li><li>*[!UICONTROL Guaranteed (fixed)]*: você e o editor concordaram com um número predefinido de impressões, direcionamento, datas de veiculação e preço fixo.<br><br><b>Observação:</b> ofertas garantidas exigem datas de voo e um número especificado de impressões na seção [!UICONTROL Tracking]. Você também deve criar uma disposição programática padrão garantida (PG) para o negócio e, como opção, usar o negócio para outros posicionamentos.</li></ul> | Sim | Não |
| | [!UICONTROL CPM] | O custo negociado por mil impressões (CPM). | Sim | Sim |
| | [Moeda] | A moeda da transação.<br><br>Todos os SSPs aceitam ofertas em USD. Quando a SSP aceitar a moeda de sua conta DSP, essa moeda também estará disponível. | Sim | Não |
| | [!UICONTROL Billing method] | Todas as IDs de negócios são financiadas por [!DNL Adobe] e faturadas. O DSP paga todos os fornecedores de mídia disponíveis com base no uso, gerencia discrepâncias com os fornecedores e envia uma fatura consolidada para a conta. Essa opção incorre em taxas adicionais, conforme descrito no cartão de taxa da conta. | Sim | Não |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | O endereço de email da conta de usuário que pode acessar a oferta. | Não | Sim |
| | [!UICONTROL Advertisers that can access this deal] | Os anunciantes específicos na conta que podem acessar esta oferta.<br><br><b>Observação:</b> você pode compartilhar a oferta com anunciantes em contas adicionais da exibição [!UICONTROL Deals]. Na linha de negócios, clique em **[!UICONTROL #]**, clique em **[!UICONTROL share]** e compartilhe o negócio com um endereço de email. | Sim | Sim |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | As datas de início e término do tráfego que usa esta oferta. Essas datas são somente para fins de rastreamento e não afetam a entrega de anúncios.<br><br><b>Dica:</b> na exibição [!UICONTROL Inventory] > [!UICONTROL Deals], a coluna [!UICONTROL Pacing & Budget] mostra como a negociação está se aproximando da data de voo e da meta de impressão especificadas. Se o delivery estiver aquém ou acima do ritmo, entre em contato com seu editor para ajustar quanto volume ele está enviando através do negócio. | Ofertas garantidas: Sim<br>Ofertas não garantidas: Não | Sim |
| | [!UICONTROL Impressions] | (Opcional para ofertas não garantidas) O número estimado de impressões que você espera executar usando esta oferta. Esse valor é somente para fins de rastreamento; o editor controla a entrega de anúncios. | Ofertas garantidas: Sim<br>Ofertas não garantidas: Não | Sim |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Criar manualmente os detalhes da ID do contrato](deal-id-create.md)
>* [Parceiros SSP](ssp-partners.md)
>* [Sobre Inventário Privado](private-inventory-about.md)
