---
title: Criar palavras-chave negativas
description: Saiba como criar palavras-chave negativas para campanhas de pesquisa e grupos de anúncios.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/NjLsCcI2-1kWIAfZOv4-IJytuPKUfQWO0OG7ptEDe9w
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# Criar palavras-chave negativas

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] e contas [!DNL Baidu] existentes apenas*

Você pode criar palavras-chave negativas para um grupo de anúncios de pesquisa ou campanha direcionada à pesquisa ou exibição/rede nativa. Palavras-chave negativas não acionam anúncios.

>[!NOTE]
>Você também pode criar e editar palavras-chave negativas nas [configurações do grupo de anúncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) e [configurações da campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Para criar muitas palavras-chave negativas de uma só vez, use [bulksheets de campanha](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar") e em **[!UICONTROL Campaign]** para criar palavras-chave negativas no nível da campanha ou **[!UICONTROL Ad Group]** para criar palavras-chave negativas no nível do grupo de anúncios.

1. Selecione a rede de publicidade, a conta, a campanha e (quando relevante) o grupo de publicidade e clique em **[!UICONTROL Continue]**.

1. Insira as palavras-chave negativas. Use a sintaxe a seguir, sem um sinal de menos (`-`):

   * Correspondência ampla negativa: `keyword` (sem suporte de [!DNL Microsoft Advertising])

   * Correspondência de frase negativa: `"keyword"`

   * Correspondência exata negativa: `[keyword]`

   Separe vários valores com vírgulas ou insira-os em linhas separadas. Você pode inserir ou colar até 2.000 palavras-chave negativas em uma operação. Consulte também os seguintes requisitos e restrições:

   * Tamanho máximo de caracteres: [!DNL Baidu]: 30 byte único ou 15 bytes duplos; [!DNL Microsoft Advertising]: 100 byte único ou 50 byte duplo; [!DNL Google Ads] e [!DNL Yahoo! Japan Ads]: 80 byte único ou 40 byte duplo.

   * [!DNL Baidu] permite somente um tipo de correspondência por palavra-chave por grupo de publicidade. Por exemplo, o Grupo de Anúncios 1 não pode incluir `"keyword"` e `[keyword]`.

   * [!DNL Google Ads]: Cada palavra-chave não pode consistir em mais de 10 palavras e pode incluir apenas letras, dígitos e os seguintes caracteres especiais: espaço `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: cada palavra-chave pode ter no máximo sete palavras, exceto palavras de interrupção. Cada [!DNL Yandex ad group] pode incluir no máximo 200 palavras-chave.

1. Clique em **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Sobre palavras-chave](keyword-about.md)
>* [Gerenciar palavras-chave licitáveis](keyword-manage.md)
>* [Alterar o status de palavras-chave e palavras-chave negativas](keyword-status-edit.md)
