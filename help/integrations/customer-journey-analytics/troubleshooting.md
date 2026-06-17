---
title: Solução de problemas de dados do Adobe Advertising no Customer Journey Analytics
description: Saiba como solucionar e resolver problemas de dados do Adobe Advertising no Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 66601570e815870c96b93e3a224bd61e8852d680
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 0%

---

# Solução de problemas de dados do Adobe Advertising no Customer Journey Analytics

A seguir estão possíveis problemas de dados e suas causas.

## Relatório de resumo

+++ Nenhum dado de relatório de resumo está disponível no Customer Journey Analytics para Advertising DSP ou Advertising Search, Social e Commerce.

Verifique o seguinte:

* O feed do Adobe Advertising para o Customer Journey Analytics está ativado. Verifique com a equipe de conta da Adobe.

* Sua dimensão/classificação/conjunto de dados de pesquisa da Adobe Advertising e seu conjunto de dados de resumo estão incluídos na conexão com o Customer Journey Analytics.

* Suas dimensões e métricas de resumo do Adobe Advertising estão incluídas na visualização de dados do Customer Journey Analytics.

* O Customer Journey Analytics Workspace está referenciando a visualização de dados correta.

Se você verificar todas as configurações acima, mas ainda não visualizar os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++ Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para o Anunciante 1, mas não para o Anunciante 2.

Verifique se o feed do Adobe Advertising para o Customer Journey Analytics está ativado para o Anunciante 2. Verifique com a equipe de conta da Adobe.

Se o feed estiver habilitado para um anunciante, mas você ainda não vir os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++ (Usuários do Search, Social e Commerce) Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para uma conta do [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mas não para outra conta.

Verifique se o feed do Adobe Advertising para o Customer Journey Analytics está ativado para a conta de rede de anúncios específica. Verifique com a equipe de conta da Adobe.

Se o feed estiver habilitado para uma conta, mas você ainda não vir os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta da rede de publicidade.
.

+++

+++ Os dados de relatórios de resumo no Customer Journey Analytics Workspace são diferentes dos dados no Advertising DSP ou Advertising Search, Social e Commerce, ou os dados de resumo estão ausentes em algumas campanhas e entidades de campanhas.

Verifique o seguinte:

* Você está usando os mesmos intervalos de datas no [!DNL Workspace] e no relatório do Adobe Advertising.

* Nenhum filtro ou segmento aplicado em [!DNL Workspace] e no relatório do Adobe Advertising está causando diferenças nos dados.

Se tiver certeza de uma discrepância de dados, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta da rede de publicidade.
. Inclua capturas de tela e planilhas para mostrar evidências da discrepância. Sua equipe de conta da Adobe pode corrigir retroativamente o feed de dados para resolver a discrepância, se necessário.

+++

## Relatórios no nível do evento

+++ Cenário: dados de conversão (como `Page Views`) não estão disponíveis para uma dimensão de relatório (como `Campaign`) no CJA Customer Journey Analytics Workspace.

Verifique o seguinte, começando pelos itens com menos barreiras:

* As métricas de conversão aplicáveis são eventos da Web/online, que o Adobe Advertising pode atribuir às dimensões.

* Você está usando a visualização de dados correta.

* O Adobe Advertising está rastreando click-throughs e viewthroughs no site aplicável. <!-- Link to validation instructions in the user guide -->

* Na conexão Customer Journey Analytics do conjunto de dados de classificações, os valores das configurações [!DNL Key] e [!DNL Matching Key] estão corretos: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* O serviço [!DNL Adobe Advertising] é adicionado à sequência de dados do Adobe Experience Platform, o esquema mapeado para a sequência de dados é `XDM ExperienceEvent Schema` e o grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` é adicionado ao esquema.

* As configurações do Adobe Advertising são definidas corretamente na extensão WebSDK e publicadas.

Se você verificar todas as configurações acima, mas ainda não visualizar os dados de conversão, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta da rede de publicidade.
.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* [Adobe Advertising IDs usadas por [!DNL Customer Journey Analytics]](ids.md)
>* [Pré-requisitos](prerequisites.md)
>* [Configurar a coleta de dados, a transferência de dados e os relatórios](set-up.md)
>* [Métricas e dimensões do Adobe Advertising no Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuários do Adobe Analytics) [Coletar dados históricos para IDs AMO e IDs EF para uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
