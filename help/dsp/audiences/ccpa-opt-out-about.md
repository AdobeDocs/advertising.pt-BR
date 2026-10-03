---
title: Sobre [!UICONTROL CCPA Opt-out-of-Sale] segmentos e relatórios
description: Saiba mais sobre como criar segmentos para rastrear IDs de solicitações de cancelamento de venda do CCPA e como recuperar relatórios das IDs.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
TQID: 'https://experienceleague.adobe.com/Bp8Fj0z7lqSXmHd-aJQa6ocQyj6FVQuydArNBucpJp4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 2b670c6e-542a-5afe-b96b-d9ce7818cd55
    internal-label: DSP Segments
  - id: b2025470-04ef-4dd9-bdd4-44407644aeb6
    internal-label: Compliance
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: Segments
  - id: c867fa1b-f589-43fa-b071-3c62f0038f23
    internal-label: CCPA
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%
---
# Sobre [!UICONTROL CCPA Opt-out-of-Sale] segmentos e relatórios

Você pode rastrear as IDs de usuários a partir de solicitações de cancelamento de venda do consumidor em seu site, de acordo com a California Consumer Privacy Act (CCPA), [criando e implementando um segmento de cancelamento de venda do CCPA](ccpa-opt-out-segment-create.md). Os usuários permanecem em segmentos de cancelamento de venda do CCPA indefinidamente.

Depois que a tag de pixel de segmento é implementada, o Adobe Advertising começa a coletar um pool de IDs em nome do anunciante.

## Relatórios de cancelamento de venda do consumidor

O Adobe Advertising gera relatórios mensais de IDs que os clientes enviaram para solicitações de recusa de venda para a conta. Os dados consolidam solicitações capturadas usando segmentos de cancelamento de venda do CCPA que foram criados no DSP e quaisquer envios feitos por meio da API do Privacy Service.  Os relatórios são gerados no primeiro dia de cada mês do mês anterior. Por exemplo, a lista mensal de usuários de junho está disponível em 1º de julho.

Cada relatório está disponível como um arquivo de texto separado por tabulação e compactado no formato GZIP. As IDs de usuário capturadas nos segmentos de cancelamento de venda do CCPA são identificadas por segmento e pelo anunciante.

Você pode [recuperar links para os relatórios mensais](ccpa-opt-out-segment-report-retrieve.md) criados nos últimos três meses, no DSP ou usando o DSP [!DNL Trafficking API]. Cada link é válido por sete dias, mas é atualizado sempre que um cliente tenta recuperar um.

>[!MORELIKETHIS]
>
>* [Suporte do Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento de venda](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Recuperar relatórios de cancelamento de venda do consumidor](ccpa-opt-out-segment-report-retrieve.md)
>* [Sobre o gerenciamento de público-alvo](audience-about.md)
