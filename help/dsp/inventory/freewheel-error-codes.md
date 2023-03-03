---
title: Códigos de erro para [!DNL FreeWheel] Envio de anúncios
description: Referencie os códigos de erro retornados para envio de anúncios a [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# Códigos de erro para [!DNL FreeWheel] Envio de anúncios

As mensagens de erro para envios de anúncios com falha podem vir do DSP publicitário ou do [!DNL FreeWheel]. Mensagens de erro são mostradas na variável [!UICONTROL API Response] na [[!UICONTROL Freewheel Status] caixa de diálogo](freewheel-check-status.md).

## Erros internos de publicidade do DSP

| Mensagem de erro | Descrição | Próximas etapas |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] ainda não respondeu que o envio foi bem-sucedido ou falhou. | Verifique o status novamente em 10 minutos. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] não aceita anúncios do Reino Unido sem clock numbers atribuídos. | Atribua um clock number ao anúncio e reenvie o anúncio. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | O transcodificador não havia terminado de transcodificar o anúncio quando você tentou enviá-lo. | Aguarde dez minutos e reenvie o anúncio. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | O contrato enviado não está configurado como um contrato programático garantido. [!DNL FreeWheel] O aceita somente ofertas garantidas. | Configure a ID de acordo como um acordo programático garantido. O anúncio é enviado automaticamente para [!DNL FreeWheel] ao salvar a disposição padrão programática garantida no final do fluxo de trabalho da ID de negócios. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | A ID de negócios enviada não existe ou não está ativa no Adobe. | Certifique-se de que o contrato esteja ativo e, em seguida, reenvie o anúncio. |
| [!DNL \[public_id=]\&lt;deal>] não existe | A ID de negócios enviada não existe no [!DNL FreeWheel] fim. | Entre em contato com [!DNL FreeWheel] representante para confirmar a ID do negócio. |
| [!DNL Ad with identifier] \&lt;*nome do anúncio*\> [!DNL was not found.] | A chave do anúncio enviado não existe ou não está ativa no Adobe. | Encontre a chave do anúncio correta e envie o anúncio novamente. |
| [!DNL Pending Submission] | O envio ainda está pendente. | Atualize a página. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Erros de API

| Código | Significado | Descrição | Próximas etapas |
|--- |--- |--- |--- |
| 401 | Não autorizado | Credenciais de acesso incorretas, ausentes ou inválidas. | Entre em contato com a equipe de conta do Adobe. |
| 403 | Proibido | O servidor compreendeu a solicitação, mas se recusa a autorizá-la. | Entre em contato com a equipe de conta do Adobe. |
| 404 | Não encontrado | O recurso solicitado não está disponível. Se a Creative ID não for encontrada na operação PUT, um 404 será retornado. | Entre em contato com a equipe de conta do Adobe. |
| 405 | Método não permitido | Foi feita uma solicitação de um recurso usando um método de solicitação sem suporte desse recurso (por exemplo, usando GET em um método que requer que os dados sejam enviados por POST ou usando PUT em um recurso somente leitura). | Entre em contato com a equipe de conta do Adobe. |
| 408 | Tempo limite da solicitação | Ocorreu um tempo limite durante o processamento desta solicitação. Os tempos limite geralmente são causados por solicitações simultâneas de acesso exclusivo a determinados recursos. | Reenvie a solicitação quando receber este status. Se o problema persistir, entre em contato com a equipe de conta da Adobe. |
| 422 | Entidade Não Processável | Recurso inválido. Esse erro ocorre quando o corpo da solicitação é inválido ou o recurso criado/atualizado é inválido (por exemplo, se a ID do contrato não foi encontrada). Consulte [Erros 422 da API FreeWheel](#freewheel-422-errors) para obter mais informações. | Entre em contato com a equipe de conta do Adobe. |
| 500 | Erro interno do servidor | Erro de sistema de API. | Entre em contato com a equipe de conta do Adobe. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Erros de API 422 {#freewheel-422-errors}

| Código | Código HTTP | Descrição |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Os dados da solicitação estão em formato json inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_VALIDATION_FAILURE | 422 | Os dados da solicitação não têm campos obrigatórios ou têm um tipo de dados inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_DEAL_INVALID | 422 | O negócio está configurado incorretamente ou não existe. Verifique a mensagem de erro para obter detalhes. |
| DATA_DEAL_GET_FAILURE | 422 | O negócio não foi encontrado ou sua configuração tem um problema. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | O URL criativo é inválido. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_LINK_FAILURE | 422 | O criativo não foi vinculado aos nós da unidade de publicidade do negócio. Verifique a mensagem de erro para obter detalhes. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | O criativo não foi atualizado. Verifique a mensagem de erro para obter detalhes. |
| DATA_DSP_GET_FAILURE | 422 | O DSP não existe dentro do sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | O criativo não foi desvinculado das unidades de publicidade. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | O criativo não foi excluído. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | O URL não foi detectado. |
| DATA_ENTITY_NOT_FOUND | 422 | O criativo não existe. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Visão geral da configuração de ofertas programáticas garantidas no [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Aceitar uma oferta na caixa de entrada da ID de oferta](deal-id-inbox-accept.md)
>* [Envie um anúncio para um contrato programático garantido para [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Verifique o status dos anúncios para [!DNL FreeWheel] Ofertas programáticas garantidas](/help/dsp/inventory/freewheel-check-status.md)

