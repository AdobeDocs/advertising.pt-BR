---
title: Uso da integração do DSP com o [!DNL Adobe] [!DNL Real-time CDP]
description: Saiba como habilitar o DSP para assimilar seus [!DNL Adobe] [!DNL Real-time CDP] segmentos primários.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL Adobe Real-Time CDP] para Universal IDs

*Recurso do Beta*

Use a integração do DSP com o [o [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), que faz parte do Adobe Experience Platform, para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

1. (Para converter endereços de email em [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar rastreamento para [!DNL Analytics] medição:

   1. (Se você ainda não tiver feito isso) Conclua tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e a variável [ID AMO e ID EF nos URLs de rastreamento](/help/integrations/analytics/ids.md).

   1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

      * **Para [!DNL RampIDs]:** Você deve implantar uma tag JavaScript adicional em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que fornecerá instruções para se registrar em um [!DNL LiveRamp] [!DNL LaunchPad] tag de [!DNL LiveRamp] Soluções de tráfego de autenticação. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante. É possível optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará na próxima etapa.

1. No Adobe Experience Platform, configure uma conexão de destino do Advertising DSP usando o [!UICONTROL Source Key] que foi gerado nas configurações da fonte DSP.

   Para obter instruções sobre como ativar a conexão de destino DSP, selecionar segmentos e acessar permissões de controle, consulte &quot;[Conexão com o Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   Os endereços de email de origem devem ser transformados em hash usando o algoritmo SHA -256.

1. Verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que o segmento está preenchendo, e compare o número de IDs universais com o número de endereços de email com hash originais.

   Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas. Para obter informações sobre as taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Os segmentos são atualizados a cada 24 horas. No entanto, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos reenviando-os do Real-Time CDP antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md).&quot;

Para solucionar problemas com o procedimento de conversão, entre em contato com a equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
