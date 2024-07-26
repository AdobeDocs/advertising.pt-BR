---
title: Configurações para planos de alcance de TV conectado
description: Consulte descrições das configurações para planos de alcance de TV conectada.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 84cf49c9e366938479e9fea2ede55925f1cb3e51
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Configurações para planos de alcance de TV conectado

| Parâmetro | Descrição | Obrigatório? |
| --- | --- | --- |
| [!UICONTROL Name] | O nome para identificar seu plano. | Sim |
| [!UICONTROL Advertiser] | O anunciante específico na conta para a qual o plano está sendo criado. | Sim |
| [!UICONTROL Media Type] | O tipo de mídia a ser incluída no plano.<br><br>Atualmente, somente [!UICONTROL Connected TV] está disponível. | Sim |
| [!UICONTROL Date Range] | As datas inicial e final do plano.<br><br>A data de início não pode ser anterior à data atual. O intervalo de datas não pode ser superior a 90 dias. | Sim |
| [!UICONTROL Goal Type] | O tipo de meta (como [!UICONTROL Budget]) a ser considerado para o plano.<br><br>Atualmente, somente [!UICONTROL Budget] está disponível. | Sim |
| [!UICONTROL Goal Value] | O valor da meta para a previsão. Para obter resultados de previsão mais precisos, use um valor > US$ 5.000. | Sim |
| [!UICONTROL Max Bid] | O valor máximo a ser pago por 1000 impressões. Se o tipo de mídia [!UICONTROL Connected TV] for selecionado, insira um valor de pelo menos US$ 10. | Sim |
| [!UICONTROL Frequency Cap] | O número de vezes que uma família única deve receber anúncios.<br><br>Ao implementar um plano e criar vários posicionamentos, aplique a configuração de limite de frequência no nível do pacote, não no nível do posicionamento, para garantir a entrega adequada. | Sim |
| [!UICONTROL Geo-Targeting] | Locais a serem incluídos ou excluídos como destinos. As opções incluem:<ul><li>Países, cidades, estados: clique na guia **[!UICONTROL Country/State/City]**; selecione se a área é um *País*, *Estado* ou *Cidade*; como opção, expanda qualquer local para exibir seus subcomponentes e clique em **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** ao lado do local.</li><li>Áreas de mercado designadas (DMAs) nos Estados Unidos: clique na guia **[!UICONTROL DMA]**; opcionalmente, expanda qualquer estado para exibir seus DMAs e clique em **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** ao lado do local.</li><li>Códigos postais: Você pode:<ul><li>Clique na guia **[!UICONTROL Search postal code]**, selecione o país, digite o nome completo da cidade ou as letras contidas no nome da cidade e pressione a tecla **[Enter]**, clique no nome correto da cidade para exibir todos os códigos postais da cidade, clique no código postal correto e clique em **[!UICONTROL Include]** ou **[!UICONTROL Exclude]**.</li><li>Clique na guia **[!UICONTROL Paste postal code]**, selecione o país, insira ou cole valores separados por vírgula e clique em **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Sim |
| [!UICONTROL Inventory Targeting] | Origens de inventário a serem incluídas ou excluídas como destinos. Selecione pelo menos um feed ou fonte. | Sim |
| [!UICONTROL Site/App Targeting] | Sites e aplicativos a serem incluídos ou excluídos como destinos. Insira uma URL por linha e clique em **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**. | Não |
| [!UICONTROL Audience Targeting] | Públicos a serem incluídos ou excluídos como destinos. | Não |
| [!UICONTROL Ad duration] | A duração dos anúncios a serem considerados no plano. | Não |

>[!MORELIKETHIS]
>
>* [Sobre a Ferramenta de Planejamento DSP](planner-about.md)
>* [Criar um Plano de Alcance de TV Conectado](planner-create.md)
>* [Duplicar um Plano de Alcance de TV Conectado](planner-duplicate.md)
>* [Editar um Plano de Alcance de TV Conectado](planner-edit.md)
>* [Exportar um Plano de Alcance de TV Conectada](planner-export.md)
>* [Regenerar a Previsão para um Plano de Alcance de TV Conectada](planner-forecast.md)
>* [Arquivar um Plano de Alcance de TV Conectada](planner-archive.md)
