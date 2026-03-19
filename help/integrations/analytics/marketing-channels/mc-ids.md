---
title: Usando Adobe Advertising IDs para criar  [!DNL Marketing Channels] regras
description: Saiba como usar Adobe Advertising IDs para criar regras de processamento para  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Usando Adobe Advertising IDs para criar [!DNL Marketing Channels] regras de processamento

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Você pode usar Adobe Advertising IDs ([ID AMO e EF ID](../ids.md)) para configurar [!DNL Marketing Channels] regras de processamento no Adobe Analytics. Use Adobe Advertising IDs para regras específicas para suas campanhas do Adobe Advertising. A ordem na qual você processa as regras determina se todos os dados possíveis são capturados corretamente.

## A ID do AMO nas regras de processamento

A ID do AMO é o código de rastreamento principal usado para reportar dados do Adobe Advertising no [!DNL Analytics]. A ID do AMO é uma concatenação de valores dinâmicos gerenciados pela Adobe para fornecer relatórios granulares no [!DNL Analytics]. Ele está armazenado em uma [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou dimensão rVar (AMO ID). A ID do AMO pode ser definida em [!DNL Analytics] de duas maneiras:

* Rastreamento de click-through: o Adobe Advertising define o parâmetro da cadeia de caracteres de consulta `s_kwcid` em um link e o [!DNL Analytics] seleciona o parâmetro da URL da página de aterrissagem quando ocorre um click-through.

* Rastreamento de view-through (Somente [!DNL DSP]): O [!DNL Last Event Service] detecta uma view-through no lado do servidor e envia a ID do AMO para [!DNL Analytics]. Nesse caso, a URL não contém um parâmetro `s_kwcid`.

Os valores dinâmicos nas IDs do AMO indicam o canal de marketing que foi rastreado:

* O prefixo na ID do AMO pode ser usado para identificar o canal de nível superior em [!DNL Marketing Channels].

* As frases de caracteres no corpo da ID do AMO indicam um tipo de campanha mais específico.

* O sufixo &quot;vt&quot; está presente para o tráfego de view-through [!DNL DSP] e pode ser usado para criar canais de click-through e view-through [!DNL DSP] separados.

O restante da ID do AMO pode ser ignorado.

| [!UICONTROL AMO ID] | Canal | Lógica da regra |
|--------|---------|--------------------|
| !ctv (sufixo) | [!UICONTROL DSP Connected TV ViewThrough] | Termina com |
| !d! (corpo) | [!UICONTROL Display Network] | Contém |
| !g! (corpo) | [!UICONTROL Google Search] | Contém |
| !s! (corpo) | [!UICONTROL Search Partner] | Contém |
| !u! (corpo) | [!UICONTROL Smart Shopping Campaign] | Contém |
| !ytv! (corpo) | [!UICONTROL YouTube Video Ad] | Contém |
| !sim! (corpo) | [!UICONTROL YouTube Search Ad] | Contém |
| !vp! (corpo) | [!UICONTROL Google Video Partners] | Contém |
| !vt (sufixo) | [!UICONTROL DSP ViewThrough] | Termina com |
| AL! (prefixo) | [!UICONTROL Paid Search] | Começa com |
| AC! (prefixo) | [!UICONTROL DSP Display] | Começa com |

## A ID EF nas regras de processamento

A EF ID do AMO (EF ID) é o segundo código de rastreamento usado na integração do [!DNL Analytics for Advertising]. Seu objetivo principal é rastrear e transmitir dados do evento [!DNL Analytics] para o Adobe Advertising. Sempre que ocorrer um click-through ou um view-through, é gerado um único ID EF, mesmo que seja exatamente o mesmo anúncio para o mesmo visitante. A ID de EF não é usada na interface do usuário de relatórios [!DNL Analytics] porque geralmente excede os 500k valores únicos por limite de variável em [!DNL Analytics], tornando-a inutilizável para relatórios. As métricas e os metadados do Adobe Advertising não são aplicados à ID EF; eles são aplicados apenas à ID AMO. A granularidade adicional do rastreamento é necessária para a otimização da campanha no Adobe Advertising, portanto, ambas as IDs são necessárias.

Embora a dimensão EF ID não seja usada diretamente nos relatórios [!DNL Analytics], a EF ID pode ser útil na criação de canais de marketing. O sufixo da ID EF indica o canal (exibição ou pesquisa) e se a visita foi orientada por um click-through ou um view-through. O delimitador na EF ID é um sinal de dois pontos, em vez do ponto de exclamação na AMO ID.

| Sufixo da ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Exemplos de regras de processamento para o Adobe Advertising

O conjunto de regras de exemplo a seguir se concentra nas regras dos canais de publicidade (Pesquisa paga, ClickThrough de exibição e ViewThrough de exibição). A regra recomendada para a detecção de Pesquisa paga (incluindo como essa regra interage com a lógica do Canal de marketing de pesquisa natural) e uma atualização opcional à regra de Domínios de referência naturais também são demonstradas.

**Observação:** a exibição pode ser separada como dois canais ou mesclada em um único canal com base na preferência do anunciante.

Outros canais são incluídos na captura de tela de exemplo para ilustrar a ordem recomendada de operações dos canais de publicidade em relação a outros canais em uma implementação típica.

>[!IMPORTANT]
>
>Consulte &quot;[Ordem das operações para [!DNL Marketing Channels] regras](#rule-order)&quot; para obter informações sobre a ordem em que suas regras devem ser processadas.

![Exemplo de um conjunto de regras de processamento](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Regra de pesquisa paga

A prática recomendada é incluir duas condições com o operador &quot;Qualquer&quot; para uma regra [!UICONTROL Paid Search]:

* Os dados de custo/clique/impressão contêm a ID do AMO, portanto, inclua a ID do AMO. A ID do AMO deve começar com &quot;AL!&quot; para alocar corretamente os dados de clique/custo/impressão para [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* As URLs para click-throughs [!UICONTROL Paid Search] sempre incluem o parâmetro de sequência de consulta `s_kwcid`, portanto, inclua-o para garantir que a desduplicação adequada ocorra se o visitante navegar de volta para a página de aterrissagem. Incluir &quot;AL!&quot; antes de `s_kwcid` alocar corretamente os dados de clique/custo/impressão para [!UICONTROL Paid Search].

Não defina o valor do canal para a ID do AMO. Em vez disso, defina-o como algo como Domínio de referência, Mecanismo de pesquisa + Palavra-chave ou Página. (Isso é relevante para todos os [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Exemplo de uma regra de Pesquisa Paga](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Exemplo de uma regra de Pesquisa Paga")

### Regra de pesquisa natural

Para [!UICONTROL Natural Search], verifique se suas [[!UICONTROL Paid Search] regras de detecção](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) incluem os parâmetros de cadeia de caracteres de consulta `ef_id` e `s_kwcid`. (Normalmente, isso é configurado automaticamente quando o Advertising Search, Social e Commerce é integrado ao [!DNL Analytics], mas verifique se um administrador do [!DNL Analytics] alterou a lógica após a configuração da integração.)

Defina a regra como &quot;Corresponde às regras de detecção de pesquisa natural&quot; (que geralmente é a configuração padrão desse canal).

![Exemplo de uma regra de Pesquisa Natural](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Exemplo de uma regra de Pesquisa Natural")

### Exibir regra de click-through #1

Crie um canal de marketing ClickThrough de exibição ao capturar somente click-throughs. Como a ID do AMO é a mesma para click-throughs e view-throughs, essa regra usa a variável EF ID e o parâmetro de sequência de consulta `ef_id`.

Às vezes, os click-throughs são rastreados pelo URL (o padrão). Em outros casos, os click-throughs são rastreados pelo Último Serviço de Evento no lado do servidor e, portanto, a URL não contém o parâmetro `ef_id`. A regra, portanto, verifica as condições em que a variável EF ID ou o parâmetro de cadeia de caracteres de consulta `ef_id` termina com &quot;:d&quot;. Use o operador &quot;`Any`&quot; porque você deseja que essa regra seja acionada para qualquer uma das condições.

![Exemplo de uma primeira regra ClickThrough de Exibição](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Exemplo de uma primeira regra ClickThrough de Exibição")

### Regra de domínios de referência naturais

(Opcional) A prática recomendada é adicionar uma condição &quot;É a primeira página da visita&quot; com o operador &quot;Qualquer&quot; à regra padrão [!UICONTROL Natural Referring Domains]. Embora essa regra seja opcional, ela pode ajudar a impedir que o caso de borda de referenciadores naturais seja definido quando o usuário clica no botão Voltar para retornar à página inicial.

![Exemplo de uma regra de Domínios de Referência Naturais](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Exemplo de uma regra de Domínios de Referência Naturais")

### Exibir regra de viewthrough de CTV

Para rastrear [!DNL DSP] view-throughs da TV conectada (CTV), crie uma regra na qual a ID do AMO termine com `"!ctv"`. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui o `ef_id` ou `s_kwcid` na URL e a regra requer apenas uma condição.

![Exemplo de uma regra ViewThrough de CTV de Exibição](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "Exemplo de uma regra ViewThrough de CTV de Exibição")

### Exibir regra de view-through

Para criar um canal Display ViewThrough, crie uma regra em que a ID de EF termine com &quot;:i&quot;. Como o visitante não clicou no anúncio, o rastreamento de view-through não inclui o `ef_id` ou `s_kwcid` na URL e a regra requer apenas uma condição.

![Exemplo de uma regra DisplayThrough](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Exemplo de uma regra DisplayThrough")

### Exibir regra de click-through #2

Para a segunda regra ClickThrough de exibição, defina **a ID do AMO começa com &quot;AC!&quot;**. Esta segunda regra existe para capturar os dados de clique/custo/impressão do canal de Exibição que vem diretamente do Adobe Advertising para o [!DNL Analytics]. Esses dados são atribuídos a uma ID AMO, mas não incluem uma URL com a sequência de consulta `ef_id`, portanto, essas ocorrências não são conectadas a uma ID AMO EF, que é o que a primeira regra ClickThrough de exibição captura.

![Exemplo de uma segunda regra ClickThrough de Exibição](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Exemplo de uma segunda regra ClickThrough de Exibição")

## Ordem de operações de [!DNL Marketing Channels] regras {#rule-order}

![Ordem ideal de operações para regras relacionadas ao Adobe Advertising](/help/integrations/assets/a4adc-mc-rule-order.png "Ordem ideal de operações para regras relacionadas ao Adobe Advertising")

* Colocar [!UICONTROL Paid Search] *antes* [!UICONTROL Natural Search]. Caso contrário, os dados de pesquisa paga podem ser alocados para pesquisa natural.

* Coloque o **primeiro** [!UICONTROL Display ClickThrough] *antes* [!UICONTROL Natural Referring Domains] e [!UICONTROL Natural Social].

* Quando você usar [!UICONTROL CTV view-throughs], coloque-o *antes* [!UICONTROL Display ViewThroughs]. Caso contrário, os view-throughs de CTV serão capturados como ViewThroughs de exibição.

* Coloque [!UICONTROL Display ViewThroughs] *depois* de outros canais, mas antes de [!UICONTROL Internal] e [!UICONTROL Direct] porque é possível que um view-through e um click-through não-[!DNL Advertising] possam ocorrer no mesmo evento de aterrissagem. Por exemplo, um visitante pode ver um anúncio do Adobe Advertising, obter uma impressão e ir para o site por meio de [!UICONTROL Natural Search].

  A prática recomendada é priorizar os outros canais (exceto [!UICONTROL Internal] e [!UICONTROL Direct]) em view-throughs.

* Alguns anunciantes podem optar por priorizar [!UICONTROL Display ViewThroughs] sobre [!UICONTROL Natural Referring Domains]. Faça isso trocando a ordem de processamento das duas regras.

* A regra **segundo** [!UICONTROL Display ClickThrough] existe para capturar os dados de clique/custo/impressão diretamente do Adobe Advertising para [!DNL Analytics]. Como esses dados são atribuídos apenas a uma ID do AMO, esses hits não são conectados a uma ID AMO EF. Se você não definir essa regra, todos os dados de clique/custo/impressão ficarão no canal [!UICONTROL Direct], que é o canal padrão para todos os dados que não correspondem a um [!DNL Marketing Channel]. Esta regra deve vir *após* a regra de view-through ou ela selecionará quaisquer view-throughs.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Fundamentos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por que os dados do canal podem variar entre o Adobe Advertising e o  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] com dados do Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para relatórios do Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising IDs usadas por [!DNL Analytics]](/help/integrations/analytics/ids.md)