---
title: Códigos de erro para  [!DNL FreeWheel] envios de anúncios
description: Referencie os códigos de erro retornados para envio de anúncios a  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 3%

---

# Códigos de erro para [!DNL FreeWheel] envios de anúncios

As mensagens de erro para envio de anúncios com falha podem vir do Advertising DSP ou do [!DNL FreeWheel]. Mensagens de erro são mostradas na coluna [!UICONTROL API Response] na caixa de diálogo [[!UICONTROL Freewheel Status]](freewheel-check-status.md).

## Erros internos do Advertising DSP

| Mensagem de erro | Descrição | Próximas etapas |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] ainda não respondeu que o envio foi bem-sucedido ou falhou. | Verifique o status novamente em 10 minutos. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] não aceita anúncios do Reino Unido sem clock numbers atribuídos. | Atribua um clock number ao anúncio e reenvie o anúncio. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | O transcodificador não havia terminado de transcodificar o anúncio quando você tentou enviá-lo. | Aguarde dez minutos e reenvie o anúncio. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | O contrato enviado não está configurado como um contrato programático garantido. [!DNL FreeWheel] aceita somente ofertas garantidas. | Configure a ID de acordo como um acordo programático garantido. O anúncio é enviado automaticamente para [!DNL FreeWheel] quando você salva a disposição padrão programática garantida no final do fluxo de trabalho da ID de negócio. |
| [!DNL Invalid external_deal_id:] \&lt;id_do_negócio\> | A ID de negócios enviada não existe ou não está ativa no Adobe. | Certifique-se de que o contrato esteja ativo e, em seguida, reenvie o anúncio. |
| [!DNL \[public_id=]\&lt;negócio\>] não existe | A ID de negócios enviada não existe na extremidade [!DNL FreeWheel]. | Entre em contato com o representante do [!DNL FreeWheel] para confirmar a ID do negócio. |
| [!DNL Ad with identifier] \&lt;*nome do anúncio*\> [!DNL was not found.] | A chave do anúncio enviado não existe ou não está ativa no final do Adobe. | Encontre a chave do anúncio correta e envie o anúncio novamente. |
| [!DNL Pending Submission] | O envio ainda está pendente. | Atualize a página. |

{style="table-layout:auto"}

## [!DNL Freewheel] erros de API

| Código | Significado | Descrição | Próximas etapas |
|--- |--- |--- |--- |
| 401 | Não autorizado | Credenciais de acesso incorretas, ausentes ou inválidas. | Entre em contato com a equipe de conta da Adobe. |
| 403 | Proibido | O servidor compreendeu a solicitação, mas se recusa a autorizá-la. | Entre em contato com a equipe de conta da Adobe. |
| 404 | Não encontrado | O recurso solicitado não está disponível. Se a Creative ID não for encontrada na operação do PUT, um 404 será retornado. | Entre em contato com a equipe de conta da Adobe. |
| 405 | Método não permitido | Foi feita uma solicitação de um recurso usando um método de solicitação não compatível com esse recurso (por exemplo, usar o GET em um método que requer que os dados sejam enviados por POST ou usar o PUT em um recurso somente leitura). | Entre em contato com a equipe de conta da Adobe. |
| 408 | Tempo limite da solicitação | Ocorreu um tempo limite durante o processamento desta solicitação. Os tempos limite geralmente são causados por solicitações simultâneas de acesso exclusivo a determinados recursos. | Reenvie a solicitação quando receber este status. Se o problema persistir, entre em contato com a equipe de conta da Adobe. |
| 422 | Entidade Não Processável | Recurso inválido. Esse erro ocorre quando o corpo da solicitação é inválido ou o recurso criado/atualizado é inválido (por exemplo, se a ID do negócio não foi encontrada). Consulte [Erros 422 da API FreeWheel](#freewheel-422-errors) para obter mais informações. | Entre em contato com a equipe de conta da Adobe. |
| 500 | Erro interno do servidor | Erro de sistema de API. | Entre em contato com a equipe de conta da Adobe. |

{style="table-layout:auto"}

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
| DATA_DSP_GET_FAILURE | 422 | O DSP não existe no sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | O criativo não foi desvinculado das unidades de publicidade. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | O criativo não foi excluído. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | O URL não foi detectado. |
| DATA_ENTITY_NOT_FOUND | 422 | O criativo não existe. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Visão geral da configuração de ofertas programáticas garantidas no [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Aceitar um contrato no [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Enviar um anúncio para uma oferta programática garantida para [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Verificar o status dos anúncios de um [!DNL FreeWheel] PG_deal](/help/dsp/inventory/freewheel-check-status.md)
