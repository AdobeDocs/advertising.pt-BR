---
title: Perguntas frequentes
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Perguntas frequentes xxx

## título

https://adobeadcloud.zendesk.com/agent/tickets/14214 Por padrão, o Adobe Analytics relata todos os eventos capturados em cada relatório. &quot;[!UICONTROL Unspecified]&quot;Os eventos representam eventos de conclusão de formulário que não foram conectados à Adobe Advertising. Por exemplo, no relatório da Plataforma de publicidade, as conversões orgânicas ou as conversões orientadas por uma campanha de email se encaixariam em &quot;não especificadas&quot;.

Você pode usar o filtro para remover eventos não especificados de relatórios removendo a marca de seleção da opção &quot;Incluir não especificado (nenhum)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323 Coloque as tags de evento do Analytics nos mesmos pontos que os pixels do Ad Cloud para garantir que XXX corresponda.

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323

P: Durante nossa auditoria de segurança interna, alguns recursos foram sinalizados como uma preocupação de segurança que foi habilitada quando integramos o Ad Cloud à instalação existente do Adobe Analytics.

A integração em questão ocorre entre o AdCloud e o Adobe Audience Manager. Esse recurso aumenta a taxa de correspondência da ID de visitante entre o AdCloud e o Adobe Audience Manager. Ele faz isso enviando solicitações de rede para pagead.l.doubleclick.net, star-mini.c10r.facebook.com e pug88000nf.pubmatic.com para determinar se esses serviços têm uma ID existente para o visitante que pode ser aproveitada. Essas são as solicitações de rede que foram sinalizadas como um risco de segurança e estão ocorrendo para todos os visitantes do site.

Nosso auditor está solicitando a desativação desse recurso. O que acontece se bloquearmos essas solicitações de rede?

R: Verificamos com nosso produto e eles mencionaram que os pixels em questão são para aumentar as taxas de correspondência de cookies entre o Ad Cloud, parceiros específicos de inventário/SSP (com relação ao DSP) e AAM.  Se forem removidos, o cliente poderá observar algum nível de diminuição da taxa de correspondência entre AAC/AAM e os parceiros de inventário para os quais os respectivos pixels são destinados, mas não esperaria que isso fosse substancial.

Para o Ad Cloud Search, vemos que a ID de organização do Experience Cloud do anunciante está configurada para o Mathworks, mas nossa equipe de produtos não vê a configuração do Mathworks para ativar públicos no Ad Cloud. Você está usando o Adobe Audience Manager para enviar Públicos-alvo para o Ad Cloud Search? Caso contrário, a remoção não afetará o fluxo de trabalho atual. O Atendimento ao cliente do AAM pode ajudar na remoção desses pixels se você não quiser que eles sejam acionados.

