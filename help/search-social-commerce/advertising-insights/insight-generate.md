---
title: Gerar um [!DNL Advertising Insight]
description: Saiba como criar um [!DNL Advertising Insight].
exl-id: 242095c9-25f0-4954-b1a8-5ea3db312afd
feature: Search Advertising Insights
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Gerar um [!DNL Advertising Insight]

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Clique no insight que deseja gerar.

3. Especifique as configurações de insight:

   1. (Alguns relatórios; opcional) especifique os intervalos de datas para o insight.

   2. (A maioria dos insights) Selecione o portfólio a ser analisado.

      Em geral, todos os portfólios otimizados e ativos que contêm campanhas ativas estão disponíveis. Para alguns insights, você pode filtrar a lista de portfólios para incluir **[!UICONTROL Only Optimized Portfolios]**.

      Para [!UICONTROL Day of Week] insights, somente portfólios com gastos suficientes e que também gastaram para o target nos últimos dois dias estão disponíveis.

   3. ([!UICONTROL Event Path Beta] insight somente) Faça o seguinte:

      1. Selecione o **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (para carregar um [!UICONTROL Channel Assist Report] ou [!UICONTROL Campaign Assist Report] e classificar os eventos do usuário em grupos distintos para análise) ou *[!UICONTROL Analyze classified events]* (para carregar grupos de eventos e usá-los para gerar o insight).

      1. Clique em **[!UICONTROL Select]** para localizar um arquivo no formato XLSX e ZIP (XLSX compactado) e clique em **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] insight somente) Faça o seguinte:

      1. Insira o **[!UICONTROL Advertiser Name]** e **[!UICONTROL Account Name]**.

      1. Selecione o **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* ou *[!UICONTROL United Kingdom]*), e o **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* ou *[!UICONTROL German]*).

      1. Clique em **[!UICONTROL Select]** para localizar relatórios de campanha, palavra-chave e histórico de alterações baixados para a conta na [!DNL Google Ads] interface de usuário da web e um arquivo de bulksheet baixado para a conta no [!DNL Google Ads Editor] aplicação. Clique em **[!UICONTROL Upload]**.

         Todos os arquivos devem estar no formato CSV, TSV, TXT ou ZIP (CSV, TSV ou TXT compactados).

   5. ([!UICONTROL Location Target Performance] somente insight; opcional) Para agregar os dados diariamente em vez de como resumo, selecione a variável **[!UICONTROL Time Aggregation]** de *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] insight somente) Faça o seguinte:

      1. No **[!UICONTROL Step]** especifique o número de níveis de gastos pretendidos, ou etapas, a serem incluídos no insight. O valor pode estar entre três (3) e 100.

      1. No **[!UICONTROL Type]** selecione o tipo de simulação:

         * *[!UICONTROL Optimized Multi-portfolio]*: gera uma única simulação em vários portfólios com o mesmo objetivo e moeda.

         * *[!UICONTROL Individual Normalized]*: gera uma simulação individual para cada portfólio selecionado. Os portfólios podem ter objetivos e moedas diferentes.

   7. ([!UICONTROL Portfolio Launch] insight somente; opcional) Para especificar uma data de lançamento no futuro, especifique uma data no campo **[!UICONTROL Optional Date]** campo.

   8. ([!UICONTROL Quality Score] insight only) Selecione a rede de anúncios aplicável.

   9. ([!UICONTROL Query Cross Matching] somente insight) Na **[!UICONTROL Google Accounts]** selecione a conta.

4. Clique em **[!UICONTROL Generate Insight]**.

   Você receberá uma notificação quando o trabalho for concluído ou falhar com base em [configurações de notificação definidas](/help/search-social-commerce/notifications/notification-edit.md) para [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Sobre [!UICONTROL Advertising Insights]](insight-about.md)
>* [Exibir ou salvar um [!DNL Advertising Insight]](insight-view-save.md)
>* [Excluir um [!DNL Advertising Insight]](insight-delete.md)
