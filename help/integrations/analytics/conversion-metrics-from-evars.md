---
title: "Criar métricas de conversão a partir do Adobe Analytics [!DNL eVars] e props"
description: "Configurar métricas de evento bem-sucedido personalizadas usando [!DNL eVar]- e [!DNL prop]dados a nível da UE."
feature: Integration with Adobe Analytics, Conversions
source-git-commit: 71ffd021b31154a2ed2a522049f656a13d364d00
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Criar métricas de conversão a partir do Adobe Analytics [!DNL eVars] e [!DNL props]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Você pode usar as métricas de evento de sucesso para otimizar pacotes DSP e campanhas de Pesquisa, Social e Comércio com base nos dados do site da Adobe Analytics que melhor se ajustam aos objetivos de sua marca. É possível configurar métricas de evento bem-sucedidas personalizadas com base em suas [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) e [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) por funil [!DNL eVar]- e [!DNL prop]em um evento. Outro [!DNL Analytics] métricas, incluindo métricas de conversão padrão, personalizada e reservada e métricas de tráfego, são disponibilizadas automaticamente no DSP e em Pesquisa, Social e Comércio.

![Exemplo de uso](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exemplo de uso")

A maioria das tarefas a seguir deve ser executada por um [!DNL Analytics] administrador ou outro usuário. Se precisar de assistência, entre em contato com (usuários do DSP) a equipe de suporte técnico do DSP em `adcloud_support@adobe.com` ou (Usuários de pesquisa, redes sociais e comércio) sua Equipe de conta do Adobe.

1. Entrada [!DNL Analytics], [criar um evento bem-sucedido de espaço reservado](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Use os seguintes parâmetros adicionais:

   **Tipo:** `Counter`

   **Polaridade:**  ou `Up is Good` ou `Up is Bad`

   **Visibilidade:** `Visible Everywhere`

   **Gravação de evento único:** `Always Record Event`

   **Participação:** `Enabled`

   Você não precisa implementar o novo evento no site da sua marca porque ele usa dados existentes que já foram capturados.

1. Criar e validar uma regra de processamento no [!DNL Analytics]:

   >[!NOTE]
   >
   >Somente [!DNL Analytics] administradores de conta podem criar regras de processamento, a menos que tenham concedido permissão para não administradores.

   1. [Criar uma regra de processamento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), usando a seguinte configuração:

      * Para a condição que deve ser atendida, especifique o [!DNL eVars] ou [!DNL props].

        Você pode configurar níveis adicionais de granularidade, conforme necessário, para garantir a criação dos eventos mais precisos.

        >[!TIP]
        >
        >A prática recomendada é usar apenas um [!DNL eVar] ou [!DNL prop].

      * Para a ação, selecione **Definir evento** e selecione o evento de espaço reservado.

   1. Entrada [!DNL Analytics] [!DNL Analysis Workspace], [criar um projeto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) e puxe o novo evento em uma tabela de forma livre para garantir que os dados sejam preenchidos para o [!DNL eVar] ou [!DNL prop] métrica.

1. Entre em contato com a equipe de conta do Adobe para sincronizar a nova métrica no Adobe Advertising.

Depois que a métrica estiver disponível, você poderá usá-la para criar um objetivo, que poderá ser atribuído a um portfólio de Pesquisa, Social e Comércio ou usar como [meta personalizada](/help/dsp/optimization/custom-goal-about.md) para um pacote DSP.

Para obter mais informações sobre como criar objetivos, consulte o capítulo do Guia de Otimização em &quot;Objetivos&quot;, que está disponível no Search, Social e Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->