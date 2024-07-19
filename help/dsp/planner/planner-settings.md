---
title: Configurações para planos de alcance de TV conectado
description: Consulte descrições das configurações para planos de alcance de TV conectada.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 8574d76fd322cb1cbc6aaaf316e7ad2f961a9f6c
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Configurações para planos de alcance de TV conectado

| Parâmetro | Descrição | Obrigatório? |
| --- | --- | --- |
| Nome | O nome para identificar seu plano. | Sim |
| Anunciante | O anunciante específico na conta para a qual o plano está sendo criado. | Sim |
| Tipo de mídia | O tipo de mídia a ser incluída no plano.<br><br>Atualmente, somente [!UICONTROL Connected TV] está disponível. | Sim |
| Intervalo de datas | As datas inicial e final do plano.<br><br>A data de início não pode ser anterior à data atual. O intervalo de datas não pode ser superior a 90 dias. | Sim |
| Tipo de meta | O tipo de meta (como [!UICONTROL Budget]) a ser considerado para o plano.<br><br>Atualmente, somente [!UICONTROL Budget] está disponível. | Sim |
| Valor da meta | O valor da meta para a previsão. Para obter resultados de previsão mais precisos, use um valor > US$ 5.000. | Sim |
| Lance máximo | O valor máximo a ser pago por 1000 impressões. Se o tipo de mídia [!UICONTROL Connected TV] for selecionado, insira um valor de pelo menos US$ 10. | Sim |
| Limite de frequência | O número de vezes que uma família única deve receber anúncios.<br><br>Ao implementar um plano e criar vários posicionamentos, aplique a configuração de limite de frequência no nível do pacote, não no nível do posicionamento, para garantir a entrega adequada. | Sim |
| Geolocalização | Locais a serem incluídos ou excluídos como destinos. | Sim |
| Direcionamento de inventário | Origens de inventário a serem incluídas ou excluídas como destinos. Selecione pelo menos um feed ou fonte. | Sim |
| Direcionamento de público | Públicos a serem incluídos ou excluídos como destinos. | Não |
| Duração do anúncio | A duração dos anúncios a serem considerados no plano. | Não |

>[!MORELIKETHIS]
>
>* [Sobre a Ferramenta de Planejamento DSP](planner-about.md)
>* [Criar um Plano de Alcance de TV Conectado](planner-create.md)
>* [Duplicar um Plano de Alcance de TV Conectado](planner-duplicate.md)
>* [Editar um Plano de Alcance de TV Conectado](planner-edit.md)
>* [Exportar um Plano de Alcance de TV Conectada](planner-export.md)
>* [Regenerar a Previsão para um Plano de Alcance de TV Conectada](planner-forecast.md)
>* [Arquivar um Plano de Alcance de TV Conectada](planner-archive.md)
