---
title: Criar um público-alvo reutilizável
description: Saiba como criar públicos-alvo reutilizáveis que consistem em segmentos de público-alvo e outros públicos-alvo salvos. Opcionalmente, use um agente de público-alvo assistido por IA descrevendo seu público-alvo em prompts em linguagem natural; o agente sugere segmentos de terceiros e cria expressões de público-alvo para usar como alvos ou exclusões.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# Criar um público-alvo reutilizável

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

É possível salvar e gerenciar públicos reutilizáveis, que são grupos de segmentos de público-alvo e até mesmo outros públicos salvos, que você pode usar como destinos ou exclusões para vários posicionamentos. Crie públicos-alvo manualmente ou use o agente de público-alvo assistido por IA para gerar novos públicos-alvo reutilizáveis usando todos os segmentos primários e de terceiros disponíveis para você, de acordo com seus requisitos declarados.

>[!NOTE]
>
>(Anunciantes para os quais o DSP converte IDs de email com hash em segmentos LiveRamp RampID) Os segmentos primários RampID que não são anexados a uma inserção ativa, programada ou pausada são pausados. O segmento é descrito na lista de segmentos como &quot;Pausado automaticamente&quot;.

## Criar manualmente um público-alvo reutilizável

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Nas configurações de [!UICONTROL New Audience]:

   1. Digite um **[!UICONTROL Audience Name]** exclusivo.

   1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

      Quando você compartilha um público-alvo, o público-alvo se torna disponível como um alvo ou exclusão para todos os anunciantes na conta. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para usuários aos quais os segmentos são compartilhados. Por exemplo, se você compartilhar um público contendo segmentos do Adobe Analytics com um anunciante que não está mapeado para a mesma conta [!DNL Analytics], o segmento não será visualizado nesse público para esse anunciante. Somente os segmentos disponíveis para esse anunciante são visualizados no público-alvo.

   1. Clique em **[!UICONTROL Save]**.

1. Clique no botão **[!UICONTROL Switch to manual mode]** no painel direito.

   A opção IA é o padrão.

1. Crie o público-alvo:

   >[!NOTE]
   >
   >À medida que você cria o público-alvo, os [dados detalhados sobre o tamanho do público-alvo](audience-about.md) são atualizados no painel direito

   * Para criar manualmente a lógica do segmento, usando segmentos disponíveis nas guias [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] e [!UICONTROL Saved Audiences]](audience-settings.md), faça o seguinte.

      * (Opcional) Procure um nome, uma descrição ou um caminho de segmento.

        Os resultados da pesquisa incluem segmentos com base nos termos exatos que você usa. Quando você insere vários termos, todos os termos devem ser encontrados para um segmento.

      * Para adicionar o primeiro segmento, localize o segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

      * Para adicionar um segmento a um grupo de segmentos existente:

         1. Clique no grupo de segmentos no painel direito.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

            *[!UICONTROL Exclude All]* não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, crie esse público-alvo como *[!UICONTROL Include Any]* e, em seguida, em um posicionamento, selecione esse público-alvo no menu Públicos-alvo excluídos.

         1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

            O grupo de segmentos é atualizado automaticamente com o novo segmento.

      * Para adicionar um novo grupo de segmentos:

         1. Clique em **[!UICONTROL + New Group]** no painel direito.

            1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para *[!UICONTROL And]* ou *[!UICONTROL Or]*, conforme necessário.

            1. Localize os segmentos para o novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

            1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

   * Para usar a lógica de segmento de um público-alvo existente:

      1. Copie a lógica do segmento do público-alvo existente de qualquer uma das seguintes maneiras:

         * Na exibição Todos os Públicos-alvo, mantenha o cursor sobre a linha de público-alvo e clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Nas configurações para o público existente, na parte superior do painel lógico do segmento, clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Em um editor de texto, crie manualmente a lógica do segmento usando IDs de segmento alfanuméricos e [sintaxe booleana](audience-segment-logic-syntax.md), e copie-a para a área de transferência.

      1. Clique em **[!UICONTROL paste in an audience rule to begin building]**, cole a lógica de segmento existente no campo de entrada e clique em **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se o público-alvo já incluir qualquer lógica de segmento, colar em uma nova lógica de segmento substituirá a lógica existente.

1. Clique em **[!UICONTROL Create]**.

## Criar um público-alvo reutilizável usando IA gerativa

*recurso do Beta*

*Suporte somente para inglês*

>[!NOTE]
>
>Esse recurso está no modo beta e está sujeito a alterações. Verifique se a expressão de público-alvo gerada representa o público-alvo que você deseja antes de criar o público-alvo e usá-lo para suas inserções.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Nas configurações de [!UICONTROL New Audience]:

   1. Digite um **[!UICONTROL Audience Name]** exclusivo.

   1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

      Quando você compartilha um público-alvo, o público-alvo se torna disponível como um alvo ou exclusão para todos os anunciantes na conta. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para usuários aos quais os segmentos são compartilhados. Por exemplo, se você compartilhar um público contendo segmentos do Adobe Analytics com um anunciante que não está mapeado para a mesma conta [!DNL Analytics], o segmento não será visualizado nesse público para esse anunciante. Somente os segmentos disponíveis para esse anunciante são visualizados no público-alvo.

   1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   1. Insira um ou mais prompts para descrever as características do público-alvo que você deseja incluir e excluir. Para enviar cada prompt, clique em ![Enviar prompt](/help/dsp/assets/submit-prompt.png "Enviar prompt").

      Para obter mais informações, consulte &quot;[Escrevendo prompts](#writing-prompts)&quot; e &quot;[Práticas recomendadas para criar um resumo de público-alvo](#audience-brief-best-practices).&quot;

      Quando aplicável, o agente sugere filtros de segmento adicionais para ajudar você a criar um resumo de público-alvo mais eficiente. Você pode aceitar ou rejeitar as sugestões.

      À medida que o agente de público-alvo encontra segmentos relevantes, ele cria uma expressão de público-alvo booleana com base em seus critérios. Ela também solicita sua aprovação antes de procurar segmentos correspondentes para montar o público-alvo. Como opção, você pode ignorar a solicitação e continuar especificando critérios de público adicionais.

   1. Quando o agente de público-alvo apresentar uma expressão de público-alvo que descreva adequadamente seu público-alvo, peça ao agente de público-alvo para continuar com a montagem do público-alvo.

      Você pode digitar &quot;prosseguir&quot;, &quot;ok&quot;, &quot;sim&quot; ou outra palavra semelhante. O agente lista todos os segmentos sugeridos para cada característica (como &quot;Pais&quot;). Expanda qualquer característica para ver detalhes sobre os segmentos individuais sugeridos para aquela característica.

   1. (Se necessário) Especifique critérios adicionais. Quando o agente de público-alvo apresentar uma expressão de público-alvo que atenda a todos os seus critérios, peça ao agente de público-alvo para continuar com a montagem do público-alvo.

      Para reunir o público, digite &quot;continuar&quot;, &quot;ok&quot;, &quot;ok&quot;, &quot;sim&quot; ou outra palavra semelhante. O agente lista todos os segmentos sugeridos para cada característica (como &quot;Pais&quot;). Expanda qualquer característica para ver detalhes sobre os segmentos individuais sugeridos para aquela característica.

1. Quando estiver satisfeito com o público-alvo montado, clique em **[!UICONTROL Create]** para criar o público-alvo especificado.

   >[!NOTE]
   >
   >Não é possível editar o público-alvo posteriormente usando o agente de público-alvo. Em vez disso, [edite a expressão de público-alvo manualmente](/help/dsp/audiences/reusable-audience-edit.md).

### Noções básicas para escrever prompts {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### O que um prompt deve incluir?

* Use uma linguagem clara e descritiva para descrever o público-alvo.

   * Você pode inserir frases completas ou apenas uma sequência de características. A pontuação não é necessária, exceto quando necessária para maior clareza.

   * Em geral, os prompts não diferenciam maiúsculas de minúsculas.

   * O agente de público-alvo reconhece os sinônimos mais comuns.

* Seja específico e forneça detalhes sobre todas as características de público-alvo que deseja incluir e sobre quaisquer características que deseje excluir especificamente. Quanto mais detalhes você fornecer, maior a chance de obter os resultados que atendam às suas necessidades.

* Identifique locais, tipos de dispositivos e provedores de dados que serão incluídos ou excluídos.

* Forneça iterativamente detalhes para refinar seus critérios e a expressão de público gerada antes de salvar o público.

* Saiba mais sobre o prompt por meio da experimentação.

  Se o prompt não estiver claro, o agente de público-alvo solicitará outro prompt para que você possa tentar novamente.

  O agente de público-alvo não salvará automaticamente uma expressão de público-alvo gerada como um público-alvo. Você só pode salvar um público-alvo clicando no botão [!UICONTROL Create], que está fora da área de prompt, para que você possa desfazer as alterações que não deseja manter.

Consulte &quot;[Práticas recomendadas para criar um resumo de público-alvo](#audience-brief-best-practices)&quot; para saber mais sobre como otimizar os prompts para públicos-alvo.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### O que você não pode incluir em um prompt?

* Referências a expressões de público-alvo existentes.

* Texto em idiomas além do inglês.

#### Exemplos de respostas do agente de público-alvo e como responder

Quando o agente de público-alvo precisar de uma resposta sua, você poderá responder usando palavras-chave na solicitação ou usando sinônimos comuns.

#### Agente de público-alvo fazendo uma pergunta

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Suas respostas afirmativas: &quot;prosseguir&quot;, &quot;ok&quot;, &quot;sim&quot;, ou outra palavra semelhante

Você também pode ignorar a solicitação e continuar a especificar critérios adicionais de público-alvo.

##### Agente de público-alvo solicitando que você escolha entre várias opções

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Sua resposta: `1`, `proceed`, `2`, `maximum reach` e assim por diante.

Você também pode ignorar a solicitação e continuar a especificar critérios adicionais de público-alvo.

### Práticas recomendadas para criar um resumo de público-alvo {#audience-brief-best-practices}

Um resumo de público-alvo é um writeup estratégico que define o público-alvo de uma campanha. Um resumo bem elaborado ajuda o agente de público-alvo da DSP a identificar os segmentos mais relevantes para montar seu público-alvo direcionável.

#### Componentes essenciais de um resumo de público-alvo eficiente

Inclua quantos tipos de atributos de público-alvo forem possíveis da lista a seguir no seu resumo. Seja específico quanto aos atributos que deseja excluir.

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demografia**

  Inclui atributos como faixa etária, gênero, estado civil, composição da família (tamanho da família, presença de filhos, famílias de várias gerações).

* **Indicadores Socioeconômicos**

  Estabelece capacidade financeira por meio de faixas de renda familiar (HHI), nível de educação, cargos/cargos, status de emprego e status de propriedade da casa.

* **Parâmetros Geográficos**

  Define o escopo de localização incluindo país/países, região (EMEA, APAC, NA), densidade populacional (urbana/suburbana/rural).

* **Interesses e afinidades**

  Identifica paixões e preferências como hobbies (esportes, artes, atividades ao ar livre), padrões de consumo de mídia, afinidades de marca e atividades de estilo de vida (viagens, restaurantes, entretenimento).

* **Psicografia**

  Captura a mentalidade e os valores, incluindo aspirações (busca de status, autoaprimoramento), valores principais (sustentabilidade, inovação, tradição), traços de personalidade (assumidores de riscos, primeiros adeptos) e motivações de compra.

* **Sinais comportamentais**

  Ações observáveis, incluindo comportamento de compra (frequência de compras, preferências de canal, fidelidade à marca), comportamento online (visitas a sites, engajamento de conteúdo, atividade de redes sociais) e comportamento offline (visitas a lojas, presença em eventos, associações).

* **Intenção no Mercado**

  Identifica a prontidão da compra por meio de categorias de produto/serviço sendo pesquisadas, cronograma de compra (imediato, curto prazo, longo prazo) e eventos de vida relevantes que acionam decisões de compra.

* **Estágio da vida**

  Compreensão da fase atual incluindo estágio de carreira (estudante, nível de entrada, meio de carreira, executivo, aposentado), estágio de família (recém-casados, novos pais, ninhos vazios) e transições de vida principal.

#### Exemplo de um resumo de público bem estruturado para uma campanha de prospecção

Este é um exemplo de um forte resumo de público-alvo de uma campanha para impulsionar a conscientização e a avaliação de um serviço de assinatura premium do kit de refeição:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de público-alvo](audience-about.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe da lógica do segmento de público-alvo](audience-segment-logic-syntax.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
