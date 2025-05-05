---
title: Usando a Integração do DSP com o  [!DNL Adobe] [!DNL Real-time CDP]
description: Saiba como habilitar o DSP para assimilar seus  [!DNL Adobe] [!DNL Real-time CDP] segmentos primários.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Converter IDs de Usuário de [!DNL Adobe Real-Time CDP] em IDs Universais

*recurso do Beta*

Use a integração do DSP com [o [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=pt-BR), que faz parte da Adobe Experience Platform, para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

1. (Para converter endereços de email para [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar rastreamento para medição de [!DNL Analytics]:

   1. (Se ainda não tiver feito isso) Conclua todos os [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e a [ID do AMO e a ID do EF nas URLs de rastreamento](/help/integrations/analytics/ids.md).

   1. Registre-se com o parceiro de ID universal e implante o código específico da ID universal em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e dispositivos móveis (mas não em aplicativos móveis) para view-throughs:

      * **Para [!DNL RampIDs]:** você deve implantar uma marca JavaScript adicional em suas páginas da Web para corresponder às conversões de IDs em navegadores da Web para desktop e para dispositivos móveis (mas não em aplicativos móveis) para view-throughs. Entre em contato com a equipe de conta do Adobe, que lhe dará instruções para se registrar para uma tag [!DNL LiveRamp] [!DNL LaunchPad] das Soluções de tráfego de autenticação [!DNL LiveRamp]. A inscrição é gratuita, mas você deve assinar um contrato. Depois de se registrar, sua equipe de conta do Adobe gerará e fornecerá uma tag exclusiva para sua organização implementar em suas páginas da Web.

1. [Crie uma fonte de público-alvo](source-manage.md) para importar públicos-alvo para sua conta DSP ou para uma conta de anunciante. Você pode optar por converter os identificadores de usuário em qualquer um dos [formatos de ID universal disponíveis](source-about.md).

   As configurações de origem incluirão uma chave de origem gerada automaticamente, que você usará na próxima etapa.

1. No Adobe Experience Platform, configure uma conexão de destino do Advertising DSP usando o [!UICONTROL Source Key] que foi gerado nas configurações de origem do DSP.

   Para obter instruções sobre como ativar a conexão de destino DSP, selecionar segmentos e acessar permissões de controle, consulte &quot;[conexão Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=pt-BR).&quot;

   Os endereços de email de origem devem ser transformados em hash usando o algoritmo SHA -256.

1. Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está preenchendo e compare o número de IDs universais com o número de endereços de email com hash originais.

   Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

Os segmentos são atualizados a cada 24 horas. No entanto, a inclusão em um segmento expira após 30 dias por padrão ou após um período de expiração especificado pelo cliente. Atualize seus segmentos reenviando-os do Real-Time CDP antes da expiração. Para solicitar a expiração de um segmento personalizado, entre em contato com a equipe de conta do Adobe.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Conexão Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=pt-BR)
>* [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=pt-BR) do Adobe Experience Platform
>* [Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
