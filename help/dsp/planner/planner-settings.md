---
title: Configurações para planos de alcance de TV conectado
description: Consulte descrições das configurações para planos de alcance de TV conectada.
feature: DSP Planner
source-git-commit: 72ee396019d5a444bd326fe659ce68eb3490a439
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Configurações para planos de alcance de TV conectado

*Recurso beta*

| Parâmetro | Descrição | Obrigatório? |
| --- | --- | --- |
| Nome | O nome para identificar seu plano. | Sim |
| Anunciante | O anunciante específico na conta para a qual o plano está sendo criado. | Sim |
| Tipo de mídia | O tipo de mídia a ser incluída no plano.<br><br>Atualmente, somente [!UICONTROL Connected TV] está disponível. | Sim |
| Intervalo de datas | As datas inicial e final do plano.<br><br>A data de início não pode ser anterior à data atual. O intervalo de datas não pode ser superior a 90 dias. | Sim |
| Tipo de meta | O tipo de meta (como [!UICONTROL Budget]) a ser considerado no plano.<br><br>Atualmente, somente [!UICONTROL Budget] está disponível. | Sim |
| Valor da meta | O valor da meta para a previsão. Para obter resultados de previsão mais precisos, use um valor > US$ 5.000. | Sim |
| Lance máximo | O valor máximo a ser pago por 1000 impressões. Se a variável [!UICONTROL Connected TV] tipo de mídia estiver selecionado, insira um valor de pelo menos US$ 10. | Sim |
| Limite de frequência | O número de vezes que uma família única deve receber anúncios.<br><br>Ao implementar um plano e criar várias disposições, aplique a configuração de limite de frequência no nível do pacote, não no nível da disposição, para garantir a entrega adequada. | Sim |
| Geolocalização | Locais a serem incluídos ou excluídos como destinos. | Sim |
| Direcionamento de inventário | Origens de inventário a serem incluídas ou excluídas como destinos. Selecione pelo menos um feed ou fonte. | Sim |
| Direcionamento de público | Públicos a serem incluídos ou excluídos como destinos. | Não |
| Duração do anúncio | A duração dos anúncios a serem considerados no plano. | Não |

>[!MORELIKETHIS]
>
>* [Sobre a ferramenta Planejador DSP](planner-about.md)
>* [Criar um plano de alcance de TV conectado](planner-create.md)
>* [Duplicar um plano de alcance de TV conectado](planner-duplicate.md)
>* [Editar um plano de alcance de TV conectado](planner-edit.md)
>* [Exportar um plano de alcance de TV conectada](planner-export.md)
>* [Regenerar a Previsão para um Plano de Alcance de TV Conectada](planner-forecast.md)
>* [Arquivar um plano de alcance de TV conectada](planner-archive.md)
