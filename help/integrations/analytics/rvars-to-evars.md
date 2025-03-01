---
title: Coletar dados históricos para IDs AMO e IDs EF para uso no Adobe Customer Journey Analytics
description: Saiba como coletar dados históricos para suas variáveis reservadas no Adobe Analytics para uso futuro no Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: 6bf9647910aa7b1f74cf2bd726f8de27a8641b38
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# Coletar dados históricos para IDs AMO e IDs EF para uso no Adobe Customer Journey Analytics

*Anunciantes com [!DNL Analytics for Advertising] e Somente Adobe Customer Journey Analytics*

Se você usar variáveis reservadas para capturar a [ID do AMO e a EF ID](ids.md) da sua integração do [!DNL Analytics for Advertising], poderá se preparar para uma integração futura entre o Adobe Advertising e o [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), que é a solução [!DNL analytics] da próxima geração da Adobe, copiando as variáveis reservadas para a AMO ID e a EF ID no [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) assim que possível. Isso permitirá a coleta de dados históricos para as IDs AMO e EF assim que você concluir a tarefa. A equipe de conta da Adobe informará se você usa variáveis reservadas e precisará concluir essa tarefa.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Por que preciso coletar dados históricos do Customer Journey Analytics?

O Customer Journey Analytics permite sincronizar dados do Adobe Experience Platform com o Adobe Analytics Analysis Workspace. Atualmente, o [!DNL Analytics Data Connector] para o Experience Platform não envia dados para as variáveis reservadas do [!DNL Analytics] para o Experience Platform. Como resultado, os dados para IDs AMO e IDs EF capturados por variáveis reservadas atualmente não estão disponíveis no Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

A Adobe Advertising está planejando uma implementação futura com o Customer Journey Analytics. Depois que a implementação for lançada, sua integração do [!DNL Analytics for Advertising] ainda exigirá que você colete dados de click-through<!-- Add back if we implement this:  and (DSP users) view-through data --> usando o rastreamento de [!DNL Analytics], mas você poderá exibir seus dados em 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> e 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> se sua organização tiver ambos os produtos. Quando o recurso for lançado, a Experience Platform começará a coletar dados para sua ID AMO e ID EF para uso no Customer Journey Analytics, mas não existirão dados históricos anteriores à data de lançamento.

Entretanto, você pode começar a coletar dados para suas IDs AMO e IDs EF <!-- [!DNL rVars] --> mais cedo criando uma [[!DNL Analytics] regra de processamento](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) simples para copiar suas IDs AMO e IDs EF <!-- [!DNL rVars] --> para o [!DNL eVars] agora. Depois de criar a regra de processamento, você começará a acumular dados para suas IDs AMO e IDs EF <!-- [!DNL rVars] --> assim que eles rastrearem novos eventos. Os dados históricos estarão disponíveis no Customer Journey Analytics assim que a implementação estiver disponível.

>[!NOTE]
>
>* A partir de 28 de fevereiro de 2025, esse processo rastreia dados de click-through, mas não dados de view-through.
>* As regras de processamento são aplicadas apenas aos novos dados recebidos. Elas não funcionam retroativamente para coletar dados anteriores.

## Copie suas Variáveis Reservadas para IDs AMO e IDs EF em [!DNL eVars]

Esta etapa é manual e deve ser concluída para cada conjunto de relatórios que rastreia AMO IDs e EF IDs <!-- [!DNL rVars] --> que você espera integrar ao Adobe Advertising no futuro.

1. [Criar uma regra de processamento](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) com as seguintes configurações:

   * Selecione o conjunto de relatórios para o qual você deseja migrar dados de ID AMO e ID EF <!-- [!DNL rVar] --> para o Experience Platform para uso pelo Customer Journey Analytics.

   * Para [!UICONTROL Rule Title], use um nome descritivo, como &quot;Copiar ID AMO e ID EF para eVars&quot;.

   * Na seção [!UICONTROL Always Execute], adicione duas ações para criar as novas eVars:

      * Para o `AMO ID`:

         1. Selecione **Substituir o valor de**.
         1. Selecione *\&lt;o eVar novo/não usado\>*.
         1. Selecione **Parâmetro De Cadeia De Caracteres De Consulta**.
         1. Digite `s_kwcid`.

        Exemplo: &quot;Substituir o valor de `rVar10` pelo parâmetro da cadeia de caracteres de consulta `s_kwcid&quot;

      * Para o `EF ID`:

         1. Selecione **Substituir o valor de**.
         1. Selecione *\&lt;o eVar novo/não usado\>*.
         1. Selecione **Parâmetro De Cadeia De Caracteres De Consulta**.
         1. Digite `ef_id`.

        Exemplo: Substituir o valor de `rVar11` pelo Parâmetro da Cadeia de Caracteres de Consulta `ef_id`

   * Para o [!UICONTROL Reason for rule], use uma observação descritiva, como &quot;A ID do AMO e a ID do EF serão transportadas para o AEP pelo Conector do Adobe Analytics.&quot;

1. Valide a regra de processamento salva.

   Após salvar a regra de processamento, os dados de `AMO ID` e `AMO EF ID` <!-- the existing reserved variables --> deverão ser idênticos aos dados das duas novas eVars para as quais foram copiados.

   Por exemplo, se o novo eVar `eVar142` estiver mapeado para `amo.s_kwcid(Context Data)`, os dados de `eVar142` e `AMO ID` deverão ser idênticos.

Para obter mais informações sobre como as regras de processamento são aplicadas, consulte &quot;[Como as regras de processamento funcionam](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)&quot;.

>[!MORELIKETHIS]
>
>* [Visão geral de [!DNL Analytics for Advertising]](overview.md)
