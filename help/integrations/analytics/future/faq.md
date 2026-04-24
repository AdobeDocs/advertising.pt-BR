---
title: Perguntas frequentes
description: xxx
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Perguntas frequentes xxx

## título

https://adobeadcloud.zendesk.com/agent/tickets/14214
Por padrão, o Adobe Analytics relata todos os eventos capturados em cada relatório. "[!UICONTROL Unspecified]" eventos representam eventos de conclusão de formulário que não foram conectados ao Adobe Advertising. Por exemplo, no relatório da Plataforma de publicidade, as conversões orgânicas ou as conversões orientadas por uma campanha de email se encaixariam em "não especificadas".

Você pode usar o filtro para remover eventos não especificados de relatórios removendo a marca de seleção da opção &quot;Incluir não especificado (nenhum)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323
Coloque as tags de evento do Analytics nos mesmos pontos que os pixels do Ad Cloud para garantir que XXX corresponda.

## título

https://adobeadcloud.zendesk.com/agent/tickets/24323

P: Durante nossa auditoria de segurança interna, alguns recursos foram sinalizados como uma preocupação de segurança que foi habilitada quando integramos o Ad Cloud à instalação existente do Adobe Analytics.

A integração em questão ocorre entre o AdCloud e o Adobe Audience Manager. Esse recurso aumenta a taxa de correspondência da ID de visitante entre o AdCloud e o Adobe Audience Manager. Ele faz isso enviando solicitações de rede para pagead.l.doubleclick.net, star-mini.c10r.facebook.com e pug88000nf.pubmatic.com para determinar se esses serviços têm uma ID existente para o visitante que pode ser aproveitada. Essas são as solicitações de rede que foram sinalizadas como um risco de segurança e estão ocorrendo para todos os visitantes do site.

Nosso auditor está solicitando a desativação desse recurso. O que acontece se bloquearmos essas solicitações de rede?

R: Verificamos com nosso produto e mencionamos que os pixels em questão são para aumentar as taxas de correspondência de cookies entre o Ad Cloud, parceiros específicos de inventário/SSP (em relação ao DSP) e o AAM.  Se forem removidos, o cliente poderá observar algum nível de redução na taxa de correspondência entre o AAC/AAM e os parceiros de inventário para os quais os respectivos pixels são destinados, mas não esperaria que fosse substancial.

Para o Ad Cloud Search, vemos que a ID da organização da CX Enterprise do anunciante está configurada para o Mathworks, mas nossa equipe de produtos não vê a configuração do Mathworks para ativar públicos no Ad Cloud. Você está usando o Adobe Audience Manager para enviar Públicos-alvo para o Ad Cloud Search? If not, removing these doesn&#39;t have an impact on current workflow. AAM Customer Care can assist with the removal of these pixels if you don’t want them to be fired.

