---
title: Gerenciar sitelinks compartilhados
description: Saiba como criar e gerenciar extensões compartilhadas do sitelink.
exl-id: 33d52179-b968-4eab-a1b9-b10ff20948e3
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Gerenciar sitelinks compartilhados

*[!DNL Google Ads]e [!DNL Microsoft Advertising] somente*

Crie e gerencie sitelinks compartilhados no nível de conta para qualquer site sincronizado [!DNL Google Ads] ou [!DNL Microsoft Advertising] da conta do [!UICONTROL Extensions] > [!UICONTROL Sitelinks] biblioteca.

## Criar um sitelink compartilhado

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Insira o [configurações de sitelink compartilhadas](#shared-sitelink-settings).

1. Clique em **[!UICONTROL Post]**.

Depois de criar um sitelink, você pode [atribuí-lo a uma conta, campanha ou grupo de publicidade](sitelink-extension-associate.md).

## Editar configurações de sitelink compartilhadas

É possível editar um sitelink compartilhado de cada vez.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Marque a caixa de seleção ao lado do link de site a ser editado.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite o [configurações de sitelink compartilhadas](#shared-sitelink-settings).

1. Clique em **[!UICONTROL Post]**.

## Excluir sitelinks compartilhados

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Marque a caixa de seleção ao lado de cada link de site compartilhado que você deseja excluir.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Na barra de ferramentas, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") e selecione **[!UICONTROL Delete]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

## Configurações de sitelink compartilhado {#shared-sitelink-settings}

Para obter políticas adicionais e motivos para desaprovação do sitelink, consulte [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) e [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) requisitos de extensão do sitelink.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** O texto a ser exibido para o link. Pode incluir até 25 caracteres de byte único ou 12 caracteres de byte duplo. O texto do link deve ser exclusivo na conta ou campanha.

>[!NOTE]
>
>([!DNL Google Ads]) O texto existente de 35 caracteres é exibido em anúncios em desktops e tablets, mas não em dispositivos móveis.

**[!UICONTROL Status]:** O status de exibição do sitelink:  *[!UICONTROL Active]* ou *[!UICONTROL Deleted]* (somente sitelinks existentes). O padrão para novos sitelinks é *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Texto extra que o mecanismo de pesquisa pode exibir sob o texto do link. Para incluir uma descrição, informe valores para ambos os campos de descrição. Cada campo de descrição pode incluir até 35 caracteres de byte único ou 17 caracteres de byte duplo.

**[!UICONTROL Start Date]:** (Campanhas com sitelinks herdados existentes ou sem sitelinks; opcional) a primeira data em que o sitelink pode ser exibido com anúncios na campanha. O padrão para novos sitelinks é o dia atual. Para especificar uma data inicial futura, insira uma data no formato MM/DD/AAAA ou M/D/AAAA, ou clique em e selecione uma data.

**[!UICONTROL End Date]:** (Opcional) A última data em que o sitelink pode ser exibido com anúncios na campanha. Por padrão, o sitelink pode ser exibido indefinidamente. Para especificar uma data final, insira uma data no formato MM/DD/AAAA ou M/D/AAAA, ou clique em e selecione uma data.

**[!UICONTROL Mobile Preference]:** (Opcional) Permite que a rede tente exibir a extensão de anúncio para usuários de dispositivos móveis em vez de usuários de desktop ou tablet. Por padrão, a opção não está ativada e a extensão de anúncio aparece em qualquer tipo de dispositivo.

>[!NOTE]
>
>A rede não garante que exibirá a extensão do anúncio no tipo de dispositivo preferencial.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** O URL da página de aterrissagem para o qual os usuários do mecanismo de pesquisa são direcionados quando clicam no anúncio. Inclua quaisquer parâmetros que determinem o conteúdo da página. Se você inserir um valor, ele substituirá o URL base do anúncio.

Depois de salvar o registro, o URL base inclui todos os parâmetros de acréscimo configurados para a campanha ou conta.

>[!NOTE]
>
>* (Contas com URLs finais) O URL base pode conter redirecionamentos dentro do domínio ou subdomínio da página inicial, mas nenhum redirecionamento fora do domínio da página inicial. A rede de publicidade extrai o domínio deste URL e adiciona quaisquer caminhos de exibição opcionais para o anúncio, para criar o URL de exibição do anúncio.
>* ([!DNL Google Ads]) Cada sitelink em uma campanha ou grupo de anúncios deve ter uma página de aterrissagem exclusiva e o conteúdo de cada página de aterrissagem do sitelink deve ter aproximadamente 80% de conteúdo exclusivo. Por exemplo, não é possível ter sitelinks com links para várias âncoras na mesma página.
>* ([!DNL Google Ads]) Evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

**[!UICONTROL Tracking Template]:** (Opcional) O modelo de rastreamento ou URL de rastreamento, que especifica todos os redirecionamentos e parâmetros de rastreamento do domínio fora da página de aterrissagem e também incorpora o URL da página final/de aterrissagem em um parâmetro. Exemplo: `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir um redirecionamento.

* Para rastreamento de conversão de Adobe Advertising, que é aplicado quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot;O e o &quot;Upload automático&quot; do Search, Social e Commerce adicionam automaticamente os prefixos de seu próprio código de rastreamento de cliques ao salvar o registro.

* Para obter os parâmetros compatíveis que incorporam o URL final, consulte o ([!DNL Microsoft Advertising] somente) [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] somente) os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Disponível [!DNL ValueTrack] Parâmetros&quot; na [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348).

* Opcionalmente, é possível incluir parâmetros de URL e quaisquer parâmetros personalizados definidos para a campanha, separados por &quot;E&quot; comercial (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Opcionalmente, é possível adicionar redirecionamentos e rastreamento de terceiros.

>[!NOTE]
>
>* Quando as configurações da campanha incluem &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; O Search, Social e Commerce adiciona automaticamente os prefixos de redirecionamento e código de rastreamento ao salvar o registro.
>* O modelo de rastreamento no nível mais granular substitui os valores em todos os níveis superiores. Por exemplo, se as configurações da conta e as configurações de palavra-chave incluírem um valor, o valor da palavra-chave será aplicado.
>* ([!DNL Google Ads]) Se você atualizar um modelo de rastreamento no nível do sitelink ou da palavra-chave, os anúncios relevantes serão reenviados para revisão. É possível atualizar os modelos de rastreamento nos níveis de conta, campanha ou grupo de anúncios sem reenviar os anúncios para aprovação.
>* ([!DNL Microsoft Advertising]) É possível atualizar os modelos de rastreamento em qualquer nível sem reenviar os anúncios para aprovação.
>* Para [!DNL Google Ads], evite usar macros, que não são substituídas por cliques de fontes que permitem o rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

>[!MORELIKETHIS]
>
>* [Sobre extensões do sitelink](sitelink-extension-about.md)
>* [Associar sitelinks compartilhados a contas, campanhas e grupos de anúncios](sitelink-extension-associate.md)
