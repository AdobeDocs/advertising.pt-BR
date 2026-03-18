---
title: Sobre [!UICONTROL CCPA Opt-out-of-Sale] segmentos e relatórios
description: Saiba mais sobre como criar segmentos para rastrear IDs de solicitações de cancelamento de venda do CCPA e como recuperar relatórios das IDs.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 7cf17457ba777d2dfe9fc1607f9891a340da9031
workflow-type: tm+mt
source-wordcount: '245'
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
